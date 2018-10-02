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

A monolithic file could, for example, contain all project
- code,
- documentation, and
- output.

To get the best of both worlds,
1. start with small Python code files called scripts and then
2. combine the scripts into a larger file later on.


`@script`
Monolithic files can be convenient, but are a bad starting point.


---
## Python scripts

```yaml
type: "FullSlide"
key: "4de73bc2a6"
```

`@part1`
Scripts
- are plain-text files that
- have `.py` extensions and
- contain Python code.

Scripts in data science projects are typically run in a particular order.

This order can visualized as a diagram called a directed acyclic graph (DAG). 

![](https://ndownloader.figshare.com/files/13168322/preview/13168322/preview.jpg)


`@script`



---
## Running scripts

```yaml
type: "FullSlide"
key: "d28e7b40dc"
```

`@part1`
There are many ways to run a Python script.

In a shell:
```sh
python my_script.py
```

In an IPython console or a Jupyter notebook:
```python
%run my_script.py
```

The key is to start thinking of an analysis as a set of steps. 

Each step is done by a script.


`@script`



---
## Scripts versus Modules

```yaml
type: "FullSlide"
key: "ffe2e848d0"
```

`@part1`
Scripts and modules
- are plain-text files that
- have `.py` extensions and
- contain Python code.

The key difference is how you use them.

| Action | Filetype | Goal                            |
|--------|----------|---------------------------------|
| Run    | Script   | Do things, e.g. make a plot     |
| Import | Module   | Define classes and/or functions |


`@script`
It is possible for the same file to be used as both a module and a script.


---
## Importing modules

```yaml
type: "FullSlide"
key: "ab730708e1"
center_content: false
```

`@part1`



`@script`
The Python programming language has a [Batteries Included Philosophy](https://www.python.org/dev/peps/pep-0206/#batteries-included-philosophy). This means that


---
## Running a module as a script

```yaml
type: "FullSlide"
key: "4b698e100b"
```

`@part1`



`@script`



---
## Final Slide

```yaml
type: "FinalSlide"
key: "45042a1bd2"
```

`@script`


