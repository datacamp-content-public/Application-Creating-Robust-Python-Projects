---
title: Insert title here
key: 4ed97d102f4ad7cd2a3d795aaa18a8c5

---
## Python Project Principles

```yaml
type: "TitleSlide"
key: "d142446732"
```

`@lower_third`

name: Martin Skarzynski
title: Co-Chair, Foundation for Advanced Education in the Sciences (FAES)


`@script`



---
## The Modularity Principle

```yaml
type: "FullSlide"
key: "867f3e4a7b"
```

`@part1`
Lesson Goal: Establish principles to follow for all projects.

The modularity principle is especially important.

Modularity makes code easier to 
- organize, 
- maintain, 
- debug,
- test, and
- reuse.


`@script`
Project come in all shapes and sizes.

Project deliverables may be
- a document describing an analysis,
- a web app that enables exploration of a dataset,
- a program that allows runs


---
## Modular versus Monolithic

```yaml
type: "FullSlide"
key: "d00704249b"
```

`@part1`
The opposite of modular is monolithic.

An example of a monolithic file is a Jupyter Notebook that contains all project
- code,
- documentation, and
- output.

To get the best of both worlds,

1. write modular Python code files and then
2. combine into monolithic files.


`@script`
Monolithic files can be convenient, but are a bad starting point.


---
## Modularity in Practice

```yaml
type: "FullSlide"
key: "ffe2e848d0"
```

`@part1`
Main ways to practice modularity:
- Write scripts to run in a sequence.
- Write modules and import code.

You can use Jupyter notebooks without sacrificing modularity!

Code sharing done right:
- A python package that allows me to download and analyze the data
- A Jupyter Notebook in Google Colab that I can run in my browser
- A Binder environment that
In the R programming language, library are loaded with the `library` or `require` functions, whereas scripts are loaded with source`


`@script`



---
## What are modules?

```yaml
type: "FullSlide"
key: "d28e7b40dc"
```

`@part1`
Modules are

- plain-text files that
- have a `.py` extension and
- contain Python code. 

Modules allow code resusability
- Variables,
- Functions, and
- Classes


`@script`



---
## Modules versus scripts

```yaml
type: "FullSlide"
key: "ab730708e1"
center_content: false
```

`@part1`
Modules are similar to scripts in that both

- are plain-text files that
- have a `.py` extension and
- contain Python code.

The distinction is that modules should define
- Variables,
- Functions, and/or
- Classes.


`@script`
The Python programming language has a [Batteries Included Philosophy](https://www.python.org/dev/peps/pep-0206/#batteries-included-philosophy). This means that


---
## Final Slide

```yaml
type: "FinalSlide"
key: "45042a1bd2"
```

`@script`


