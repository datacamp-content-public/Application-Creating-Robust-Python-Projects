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
## Modularity and Reusability

```yaml
type: "FullSlide"
key: "867f3e4a7b"
```

`@part1`
A project is a directory that contains project files.

Learning Goal: Establish principles to follow for all projects.

Following the Modularity and Reusability Principles makes code easier to 
- read,
- organize, 
- maintain, 
- debug, and
- test.


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

The benefits of modularity with the convenience of a single file:
1. start with small code files called scripts and then
2. combine the scripts into a larger file later on.


`@script`
Monolithic files can be convenient, but are a bad starting point.


---
## Python Scripts

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
## Don't Repeat Yourself (DRY)

```yaml
type: "FullSlide"
key: "ffe2e848d0"
```

`@part1`
While working on a project, you may notice common patterns.

Don't repeat code! Reuse it!

If code repeats in one file, we could define a function and use it throughout the file.

Defining the same function in multiple scripts would be repetitive.

Instead, we will save our function definition in a Python code file called a module.

Moving function definitions to modules -> smaller scripts.


`@script`



---
## Scripts versus modules

```yaml
type: "FullSlide"
key: "ae33b5d1d6"
```

`@part1`
Modules allow us to avoid code repetition, by making class and function definitions available throughout a project.

We can use the `import` statement to make the function definition available in each file that needs it.

Scripts and modules are similar in many ways, but differ in how and why they are used. 

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
## Importing modules

```yaml
type: "FullSlide"
key: "919381ac3b"
```

`@part1`
Inside of a directory called `my_project`, create 2 Python code files:

1. A module named `say.py`, which uses the `def` statement to define a function called `hello`:
```python
def hello():
    print("Hello World!")
```

2. A script named `greet.py`, which uses the `import` statement to import the `say` module:
```python
import say
```


`@script`



---
## Running scripts

```yaml
type: "FullSlide"
key: "d28e7b40dc"
```

`@part1`
Right now, running `greet.py` will have no effect. 

To print "Hello World",

1. Add a function call to `greet.py`:
```python
import say
say.hello()
```

2. Run the `greet.py` script in a shell: 
```bash
python greet.py
```


`@script`



---
## Running modules as scripts

```yaml
type: "FullSlide"
key: "4b698e100b"
```

`@part1`
It is possible for the same file to be used as both a module and a script.

Add the code below to `say.py`:
```python
if __name__ == '__main__':
    hello()
```
Now running `say.py` in a shell will also print "Hello World".

The difference is that we can import the `hello` function from `say.py`, but not `greet.py`.

This approach works best when we only want to call one function from a module.


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
## Running projects

```yaml
type: "FullSlide"
key: "bfeb750a7e"
```

`@part1`
1. Create a copy of `say.py` called `__main__.py` 
2. Go up one level in your folder system
3. Run the project

```bash
cp say.py __main__.py
cd ..
python my_project
```

You can zip the whole project and run it:
```bash
python -m zipfile -c my_project.zip my_project/*
python my_project.zip
```

The convenience of a single file without sacrificing modularity!


`@script`
Running an entire project

1. Create a `__main__.py` file in a directory called `my_project`
2. Include code in the file, e.g. `print("This is my project!")`
3. Run `python my_project`

Some advantages of this are:
You can zip the whole project and still run `__main__.py`
```bash
python -m zipfile -c my_project.zip my_project/*
python my_project.zip
```

Later in the course we will learn other ways to distribute Python code.


---
## Final Slide

```yaml
type: "FinalSlide"
key: "45042a1bd2"
```

`@script`


