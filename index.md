---
title: FP Dag 2022
description: 22 April, 2022
---

## Welcome

The Dutch Functional Programming Day *(also known as the FP Dag)* is
an annual gathering of researchers, students, and practitioners
sharing a common interest in functional programming. The day features
talks that cover the latest advances in research, teaching, and
applications in functional programming in the broadest sense. Coffee
and lunch breaks provide ample opportunity for networking with your
colleagues and meeting new people. Experts and newcomers to the field
are equally welcome.

## When and where

The FP Dag will take place on April 22nd 2022, in the
[Boothzaal](http://www.cs.uu.nl/docs/reach/booth/) of the Utrecht
University's Library on the Utrecht Science Park. There is a tram
nearby with regular trams to and from Utrecht CS.

## Schedule


|:-----------:|:--------------------------------------------------|:---------------------------------------------------------------------------|
| 09:30-10:00 | **Registration**                                  |                                                                            |
| 10:00-10:25 | [Manuel Chakravarty](#manuel-chakravarty)         | Scripting Blockchains — Functional or Imperative?                          |
| 10:25-10:50 | [Olav de Haas](#olaf-de-haas)                     | Mechanizing proof outlines for imperative programs in Agda                 |
| 10:50-11:15 | [Johan Hidding](#johan-hidding)                   | Entangled - Literate Programming Improved                                  |
| 11:15-11:45 | **Break**                                         |                                                                            |
| 11:45-12:10 | Roger Bosman                                      | Getting a handle on (scoped) effects                                       |
| 12:10-12:35 | [Tom Verhoeff](#tom-verhoeff)                     | Backtracking without (Explicit) Recursion                                  |
| 12:35-13:00 | Trevor McDonell                                   | Accelerate                                                                 |
| 13:00-14:30 | **Lunch**                                         |                                                                            |
| 14:30-14:55 | [Steffen Michels](#steffen-michels)               | VIIA - A Complex Real-World TOP Application                                |
| 14:55-14:20 | [Pieter Koopman](#pieter-koopman)                 | Reducing the Power Consumption of IoT with Task-Oriented Programming       |
| 14:20-14:50 | **Break**                                         |                                                                            |
| 14:50-15:15 | [Birthe van den Berg](#birthe-van-den-berg)       | Forward- or Reverse-Mode Automatic Differentiation: What's the Difference? |
| 15:15-15:40 | Kiara Grouwstra                                   | Typed program synthesizers: machine learning in Haskell                    |
| 15:40-16:05 | [Alejandro Serrano Mena](#alejandro-serrano-mena) | The story of kind-generics: Generic Programming for GADTs                  |
| 16:05-16:15 | Business meeting                                  |                                                                            |
| 16:15-17:00 | Borrel                                            |                                                                            |
| 17:30       | Dinner                                            |                                                                            |

## Abstracts

### Manuel Chakravarty - Scripting Blockchains — Functional or Imperative?<a id="manuel-chakravarty"></a>

 The ledger model of the world’s first and largest blockchain, Bitcoin,
 constitutes a directed acyclic graph (DAG). Just as in the case of
 classic dataflow languages, the Bitcoin DAG can be seen as the
 execution trace of a functional program, even if the limited
 scriptability of Bitcoin makes this a fairly limited functional
 program. It was the aim of the world’s second largest blockchain,
 Ethereum, to lift those limits. Unfortunately, Ethereum did so by
 replacing the functional ledger model by an imperative one using
 shared mutable state. Is this change of paradigm essential? Or can we
 have our cake and eat it, too — can we preserve Bitcoin’s functional
 ledger model, while achieving Ethereum’s expressiveness?

 The answer is: yes, we can! Our extended version of Bitcoin’s ledger
 model, which forms the basis of the smart contract layer of the
 Cardano blockchain, serves as the constructive proof. Less clear is
 the choice of programming abstraction for such a functional blockchain
 scripting system. An attractive option appears to be an abstraction
 based on automata.

 In this talk, I will explain how Bitcoin and Ethereum’s ledger models
 correspond to functional and imperative programming, respectively, and
 how we extended Bitcoin’s model to achieve Ethereum-level
 expressiveness. Afterwards, I will discuss some of the open questions
 around the choice of programming abstractions and how automata might
 provide a way forward.

### Olav de Haas - Mechanizing proof outlines for imperative programs in Agda <a id="olaf-de-haas"></a>

Formal verification of imperative programs can be carried out on paper
by annotating programs to obtain an outline of a proof. This process
has been mechanized by the introduction of separation logic and
computer assisted verification tools. However, the tools fail to
achieve the readability and convenience of manual paper proof
outlines. This is a pity, because getting ideas and proofs across is
essential for scientific research. We introduce a mechanization for
proof outlines of imperative programs to interactively write human
readable outlines in the dependently typed programming language and
proof assistant Agda. We achieve this by introducing practical syntax
and proof automation to write concise proof outlines for a simple
imperative programming language based on λ-calculus. The proposed
solution results in proof outlines that combine the readability of
paper proof outlines and the precision of mechanization.

### Johan Hidding - Entangled - Literate Programming Improved<a id="johan-hidding"></a>

Science is facing a major problem known as the reproducibility
crisis. One of the supposed causes of this crisis is the lack of
proper documentation and communication about the software used in the
production of scientific results. To improve this situation, we should
give researchers better tools to help them communicate software
methodology. One such avenue of approach is to improve the usability
of literate programming methods.  Programming with Entangled starts by
creating Markdown files with embedded code blocks. These code blocks
are live tangled to compilable source code. The source code can then
also be edited, and Entangled feeds any changes back to the original
content in the Markdown files. By taking this approach, Entangled
functions independent of programming language or text editor.  Having
a daemon that compiles annotated Markdown to source code, and possibly
embeds research results into a science paper raises some interesting
issues with the programmability of such a system. Entangled embeds a
build-system (driven by Shake) and is entirely configurable through
Dhall.  Incidentally, I found that using strongly typed functional
languages offer abstractions that are the easiest to embed in a piece
of scientific prose, of which I'll show some examples.

### Tom Verhoeff - Backtracking without (Explicit) Recursion<a id="tom-verhoeff"></a>

I show how backtracking can be discovered naturally without using a
recursive function (nor using a loop with an explicit stack). Rather,
my approach involves a form of self application that can be elegantly
expressed in an object-oriented program, and that is reminiscent of
how recursion is done in lambda calculus. It also illustrates why
reasoning about object-oriented programs can be hard. I illustrate it
in Haskell where it naturally gives rise to monads and their
composition.

### Steffen Michels - VIIA - A Complex Real-World TOP Application<a id="steffen-michels"></a>

We present VIIA (Vessel Information Integrating Application), as an
example of a real-world full-stack application written in a purely
functional language. The application is developed for the Dutch Coast
Guard for continuously monitoring the North Sea and identifying
potential risks. The main selling point is a powerful query engine which
can deal with contradicting information from multiple sources, while at
the same time providing an intuitive query language for the end-user.
The system is very efficient and can deal with high data volumes of
thousands of positions per second. We show how developing such
application profits from traditional FP, as well as TOP (task-oriented
programming) a paradigm for developing purely-functional, iterative,
distributed web applications. 

### Pieter Koopman - Reducing the Power Consumption of IoT with Task-Oriented Programming <a id="pieter-koopman"></a>

Limiting the energy consumption of IoT nodes is a hot topic in green
computing. For battery-powered devices this necessity is obvious. The
enormous growth of the number of IoT nodes makes energy efficiency
important for every node in the IoT. In this talk, we show how we can
automatically compute execution intervals for our Task Oriented
Programs for the IoT. These intervals offer the possibility to save
energy by bringing the microprocessor driving the IoT node into a
low-power sleep mode until the task need to be executed. We do allow
an arbitrary number of tasks on the IoT nodes and achieve significant
reductions of the energy consumption by bringing the microprocessor in
sleep mode as much as possible. We have seen energy reductions of an
order of magnitude without imposing any constraints on the tasks to be
executed on the IoT nodes.

### Birthe van den Berg - Forward- or Reverse-Mode Automatic Differentiation: What's the Difference? <a id="birthe-van-den-berg"></a>

Automatic differentiation (AD) has been a topic of interest for
researchers in many disciplines, with increased popularity since its
application to machine learning and neural networks. The technique has
two principal variants, forward-mode and reverse-mode AD; the former
being more understand- able, the latter being more efficient. Although
many researchers appreciate and know how to apply the two variants,
only a few understand the underlying processes, though a vast amount
of literature is devoted to explaining their details. In this Pearl,
we instead aim to give a self-contained explanation of AD that departs
from nothing more than basic high-school differentiation and essential
functional programming techniques, augmented with three fundamental
abstractions. Specifically, these abstractions are: (1) a module over
a semiring, (2) a modest, but powerful, generalisation of Clifford’s
algebra of dual numbers, and (3) the Kronecker delta function. With
these abstractions, reified as Haskell type classes, we can view
different differentiation techniques as an instance of a single
abstract computation, the definition of which fits on a single
line. More precisely, we show how we can derive symbolic
differentiation, forward-mode, and reverse-mode AD, by reasoning over
the appropriate symbolic, dense, and sparse function spaces. From
there, we can optimise even further by sharing computations and using
a Cayley-style or array-based representation. Further extensions to
the framework include operator overloading, sharing sub-expressions,
higher-order differentia- tion, and more. With these abstractions and
insights in place, this Pearl seeks—once and for all—to untangle the
mystery of forward and, in particular, reverse-mode AD, making the
technique more comprehensible, also for the non-expert.

### Alejandro Serrano Mena -  The story of kind-generics: Generic Programming for GADTs <a id="alejandro-serrano-mena"></a>

What led two PhD students at UU to develop yet another generic
programming library? In this talk/story we look at those reasons, and
how step by step the kind-generics library came into existence.

## Contact

* Gabriele Keller (g.k.keller@uu.nl) 
* Wouter Swierstra (w.s.swierstra@uu.nl)


## Dinner

We will end the day with a joint dinner (at your own expense). We'll
provide more information about the dinner plans later.

## Registration

Registration is free of charge, but please [register
before April 15th](https://forms.gle/zjf54Km2xiiWcz6r5). Lunch and
coffee will be provided.


