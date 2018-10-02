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
There are many ways to run Python scripts.

In a shell:
```sh
python my_script.py
```

In an IPython console or a Jupyter notebook:
```python
%run my_script.py
```

1. Write and run code interactively
2. Run scripts in a sequence
3. Automate the sequence


`@script`



---
## Avoid code repetition

```yaml
type: "FullSlide"
key: "ffe2e848d0"
```

`@part1`
While working on a project, you may notice common patterns.

For example, every script that produces a file might include
```python
with open(filename, 'w') as f:
    f.write(contents)
```

Don't repeat code! Reuse it!

If we were working with a monolithic file, we could define a function that produces files and use it throughout the file.

When working with modular files, we will have to save our function definition in a Python code file called a module.


`@script`



---
## Scripts versus modules

```yaml
type: "FullSlide"
key: "ae33b5d1d6"
```

`@part1`
To avoid code repetition in your scripts, you can move class and function definitions into modules.

The key difference between scripts and modules is same how they are used. 

| Action | Filetype | Goal                            |
|--------|----------|---------------------------------|
| Run    | Script   | Do things, e.g. create a plot   |
| Import | Module   | Define classes and/or functions |


`@script`
It is possible for the same file to be used as both a module and a script.
```python
#
def say_hi():
    print("Hi!")

if __name__ == '__main__':
    say_hi()
```


---
## Insert title here...

```yaml
type: "FullSlide"
key: "919381ac3b"
```

`@part1`
Step 1. Write a function named `to_file` that saves a Python object to a file.
```python
def to_file(filename, contents):
    with open(filename, 'w') as f:
        f.write(contents)
```
Step 2. Save the function in a file called `my_module.py`.

Step 3. In every script that produces a file, import the `to_file` function.

```python
import my_module
answer = "The answer to life is 42."
my_module.to_file('answer.txt', answer)
```


`@script`



---
## Avoid code repetition (2)

```yaml
type: "FullSlide"
key: "ce9b795f3d"
```

`@part1`
When working with modular scripts, will need to use the `import` statement to make the function definition available in each file.

The


`@script`



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


