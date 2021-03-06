---
layout: post
title: Another scala option in java
categories: [synhaptein]
tags: []
description:
---

Scala on valentine's day is still awesome! I was doing some standard java development today and it remembered me a guy who use a custom implementation
of scala option in java because he really missed it (I must admitted, I was in the same mood). I google it and found some interesting simple implementation. Here's
what I did on my side based on [The “Option” Pattern](http://www.codecommit.com/blog/scala/the-option-pattern).

``` java
package com.synhaptein;

public abstract class Option<T> implements Iterable<T> {
  public static None None = new None<Object>();
  public static <T> Some<T> Some(T p_value) {
    return new Some<T>(p_value);
  }

  public abstract T get();
  public abstract T getOrElse(T p_value);
}
```

``` java
package com.synhaptein;

import java.util.ArrayList;
import java.util.Iterator;
import java.util.List;

public class Some<T> extends Option<T>  {
  private T m_value;

  public Some(T p_value) {
    m_value = p_value;
  }

  public Iterator<T> iterator() {
    List<T>  list = new ArrayList<T>();
    list.add(m_value);
    return list.iterator();
  }

  @Override
  public T get() {
    return m_value;
  }

  @Override
  public T getOrElse(T p_value) {
    return m_value;
  }
}
```

``` java
package com.synhaptein;

import java.util.Collections;
import java.util.Iterator;

public class None<T> extends Option<T> {
  public Iterator<T> iterator() {
    return Collections.<T>emptyList().iterator();
  }

  public T get() {
    throw new UnsupportedOperationException("Cannot resolve value on None");
  }

  public T getOrElse(T p_value) {
    return p_value;
  }
}
```

Here's my personal addition: import static! It removes the need of adding new Some<T> or new None<T> so it feels more
like scala. The downside is that None is not typed with T… but it's not null!

``` java
package com.synhaptein;
import static com.synhaptein.Option.*;

public class OptionTests {

  public static void printOption(Option<String> p) {
    System.out.println(p.getOrElse("Doe"));
  }

  public static void main(String[] args) {
    Option<String> firstName = Some("test");
    Option<String> lastName = None;

    printOption(None);
    printOption(firstName);

    try {
      System.out.println(lastName.get());
    }
    catch (UnsupportedOperationException e) {
      System.out.println("Should throw an exception");
    }

    for(String s : firstName) {
      System.out.println(s);
    }
  }
}
```
