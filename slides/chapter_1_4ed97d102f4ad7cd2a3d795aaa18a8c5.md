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

Learning Goal: Establish principles to follow for all projects

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

To get the benefits of modularity and the convenience of a single file:
1. start with small files and then
2. combine them into a larger file later on.


`@script`
Monolithic files can be convenient, but are a bad starting point.


---
## Don't Repeat Yourself (DRY)

```yaml
type: "FullSlide"
key: "ffe2e848d0"
```

`@part1`
While working on a project, you may notice common patterns.

Don't repeat code! Reuse it!

One way to deal with code repetition is to define a function.

Defining the same function in multiple code files would be repetitive.

Instead, we will 
- save our function definitions in `modules` and 
- use the definitions in `scripts`.


`@script`



---
## Scripts versus modules

```yaml
type: "FullSlide"
key: "ae33b5d1d6"
```

`@part1`
Scripts and modules
- are plain-text files that
- have `.py` extensions and
- contain only Python code.

Scripts and modules differ in how and why they are used. 

| Verb   | Filetype | Goal             |
|--------|----------|------------------|
| Run    | Script   | Perform actions  |
| Import | Module   | Define objects   |


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
## Running Scripts

```yaml
type: "FullSlide"
key: "4de73bc2a6"
```

`@part1`
Scripts in data science projects are typically run in a particular order.

This order can be visualized as a diagram called a directed acyclic graph (DAG). 

![](https://ndownloader.figshare.com/files/13168322/preview/13168322/preview.jpg)

Each script
- handles one and only one step in the process
- imports the tools it needs from modules that are included in the project.

It is common to run scripts in a shell, for example Bash (Bourne again shell).


`@script`



---
## Importing modules

```yaml
type: "FullSlide"
key: "919381ac3b"
```

`@part1`
1. Create a module named `say.py`, which uses the `def` statement to define a function called `hello`:
```python
def hello():
       print("Hello World!")
```

2. Create a script called `greet.py`, which imports the `say` module and calls the `hello` function:
```python
import say
say.hello()
```
3. Type `python greet.py` in a shell and press Enter.


`@script`



---
## Running modules as scripts

```yaml
type: "FullSlide"
key: "4b698e100b"
```

`@part1`
It is possible for the same file to be used as both a module and a script.

To demonstrate this, add the code below to the end of `say.py`:
```python
if __name__ == '__main__':
    hello()
```

The code above calls the `hello` function only when `say` is run as a script. 

The `if` statement prevents `hello` from being called when `say` is imported as a module.

Adding `hello()` to `say.py` without the `if` statement, would make `greet.py` print `Hello World!` twice!.


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
1. Create a directory called `my_project`
2. Make a copy of `say.py` called `__main__.py` 
3. Move `__main__.py` into `my_project`
4. Run the project

```bash
mkdir my_project
cp say.py __main__.py
mv __main__.py my_project
python my_project
```

You can zip the whole project and then run the zip file:
```bash
python -m zipfile -c my_project.zip my_project/*
python my_project.zip
```


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


