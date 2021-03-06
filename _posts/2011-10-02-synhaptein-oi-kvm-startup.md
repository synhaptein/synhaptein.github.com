---
layout: post
title: OpenIndiana KVM startup script
categories: [synhaptein]
tags: []
description:
---

This week, I tried the new openindiana release 151a to use kvm. There's a good post from Gray Matter Boundaries, [Installing KVM and Creating a Debian VM in OpenIndiana 151a](http://www.graymatterboundaries.com/?p=158). I installed a first vm and it works nicely! So how do I start it automatically? I'm not a sysadmin, but I create a smf and a bash script that start every *.sh in /etc/kvm. It's simple, probably not perfect and it won't halt your vms on reboot/halt, but it did what I needed! Maybe it will help someone else. By the way, if you find a bug or want to suggest an improvement, just email me at phil (at) p15x.com!

/etc/init.d/kvm (the startup script):

``` bash
#!/bin/sh

FILES=/etc/kvm/*.sh

for f in $FILES
do
        $f &
done
```

kvm.xml (smf config)

``` xml
<?xml version="1.0"?>
<!DOCTYPE service_bundle SYSTEM "/usr/share/lib/xml/dtd/service_bundle.dtd.1">
<service_bundle type='manifest' name='kvm'>
   <service name='system/kvm' type='service' version='1'>
     <create_default_instance enabled='false' />
     <single_instance/>
     <dependency name='multi-user-server'
          grouping='require_all'
          restart_on='none'
          type='service'>
        <service_fmri value='svc:/milestone/multi-user-server:default'/>
      </dependency>
     <exec_method type='method' name='start' exec='/etc/init.d/kvm' timeout_seconds='-1' />
     <exec_method type='method' name='stop' exec=':kill' timeout_seconds='-1' />
     <stability value='Unstable' />
     <template>
     <common_name>
       <loctext xml:lang='C'> KVM start </loctext>
     </common_name>
     </template>
    </service>
 </service_bundle>
```

Install the smf config for kvm

``` bash
svccfg import kvm.xml
svcadm enable kvm
```

That's it, your vms should be started on reboot!
