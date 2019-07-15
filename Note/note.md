## data

test one for data.

data  | test  | train
--|---|--
1  | 10  | +
2  | 30  | -
3  | 90  | *
4  | 100  | /

Week 1

Fri.

@Yuepei Li please join @Yijia Huang and @Long Vu and @Kamsi in contributing to the **Boa infrastructure**

gitpage:
https://github.com/boalang

HomePage:
http://boa.cs.iastate.edu/boa/index.php

1. read the book chapter on Boa,
2. get a Boa account and write a new query based on existing queries,
3. clone and get the Boa compiler to run locally, and
4. fix an open bug in the compiler.

review book-boa.pdf and boaTutorial.doxc

Talk with @Hamid on Thurday. Decided to contribute on **project NR** (non-redundant protein).


## book-boa.pdf

Boa: an Enabling Language and Infrastructure for Ultra-large Scale MSR Studies

MSR (mining software repositories) at large-scale is important.
Boa is a domain specific language.

### Objectives, why need boa

### what is boa

- Architecture
- submit task
- obtain result

### Boa's Syntax and Semantics

- build-in type (basic type) and compound type

![basic type in boa](images/2019/05/Image 5-17-19 at 10.53 AM.jpg)

array map stack set

- output aggregator
- loop with quantifiers (foreach, exists, ifall)
- user-defined functions

### Mining Project and Repository Metadata

- Types for Mining Software Repositories
  - Project
  - Person
  - CodeRepository
  - Revision
  - ChangedFile
- Examples
  - Mining Top-10 Programming Languages
  - Mining revisions thatx bugs
  - Computing Project Churn Rates

``` c++
// count top-10 languages
counts: output top(10) of string weight int;
foreach (i: int; input.programming_languages[i])
    counts << input.programming_languages[i] weight 1;
```

### Mining Source Code with Visitors

- Types for Mining Source Code
- Intrinsic Functions
- Visitor Syntax
- Examples
  - Mining AST count
  -


## boaTutorial

- install apache ant (what is this?)
  - https://www.mkyong.com/ant/how-to-apache-ant-on-mac-os-x/
- install protoc (what is this?)
  - https://medium.com/@erika_dike/installing-the-protobuf-compiler-on-a-mac-a0d397af46b8
  - how to uninstall: make uninstall
  - protobuf-2.5.0 (we need this version) : https://github.com/protocolbuffers/protobuf/releases?after=v2.6.1
  - miss package ,....V3? Maybe you need administration access.
  - no such file: ```brew install libtool```(https://github.com/fermentation/ferment/issues/17)
- Change build.xml
  - line 88 : <apply executable="/usr/local/bin/protoc" parallel="true">

# Knowledge

[svd](https://hadrienj.github.io/posts/Deep-Learning-Book-Series-2.8-Singular-Value-Decomposition/)
