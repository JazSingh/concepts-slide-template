---
author: Steven Both, Toby Rufinus, Jaspreet Singh, Daniël Stekelenburg
title: Scala
subtitle: Lightweight Modular Staging
theme: uucs
mainfont: Ubuntu Light
sansfont: Ubuntu Light
---

Now that we are familiar with Scala...

. . .

lets look at an awesome library implemented in Scala.

. . .

Lightweight Modular Staging (LMS)

---

#LMS is..

'A library-based multi-stage programming approach that uses types to distinguish between binding time.'

---

#Outline

* A gentle introduction to LMS
* Generative Programming
* Language virtualization
* Intermediate representation
* How do we program in LMS?

---

#A gentle introduction to LMS

##Power function in Scala

```Scala
def power(b: Double, x: Int): Double =
  if (x == 0) 1.0 else b * power(b, x - 1)
```

##Power function in Scala LMS

```Scala
trait PowerA { this: Arith =>
  def power(b: Rep[Double], x: Int): Rep[Double] =
    if (x == 0) 1.0 else b * power(b, x - 1)
}
```

---

#A gentle introduction to LMS

##What did we just see?

* ```T``` versus ```Rep[T]```
* ```def``` versus  ```trait```

---

#Generative Programming

##What is generative programming?

---

#Generative Programming

##Commonalities of LMS and generative programming

---

#Generative Programming

##Differences of LMS and generative programming

---

#Language Virtualization

---

#Intermediate representation

---


<!-- Local Variables:  -->
<!-- pandoc/write: beamer -->
<!-- pandoc/latex-engine: "xelatex" -->
<!-- pandoc/template: "beamer-template.tex" -->
<!-- End:  -->
