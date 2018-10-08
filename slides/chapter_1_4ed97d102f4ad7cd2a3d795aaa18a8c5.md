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
## What will you learn?

```yaml
type: "FullSlide"
key: "867f3e4a7b"
```

`@part1`
Learning Objectives: 
- Follow principles and best practices for working on Python projects.{{1}}
- Use helpful technologies and techniques to save time and get better results!{{2}}
- Write Python code and documentation that is organized and easy to {{3}}
    - read, {{3}}
    - use, {{3}}
    - maintain, and {{3}}
    - share. {{3}}


`@script`
Project come in all shapes and sizes.

Project deliverables may be
- a document describing an analysis,
- a web app that enables exploration of a dataset,
- a program that allows runs


---
## What is a Project?

```yaml
type: "FullSlide"
key: "849662964a"
```

`@part1`
A project is a directory that contains project files.

Also, an opportunity to exercise empathy for anyone who might use your code (including your future self!) {{1}}

Project files may be organized into subdirectories or kept at the top-level.{{2}}

```
my_project
├── LICENSE
├── README.md
├── code
│   └── analysis.ipynb
└── requirements.txt
```{{3}}

First Python Project Principle: Modularity 
{{4}}


`@script`



---
## What is a Project?

```yaml
type: "FullSlide"
key: "d238684b3c"
disable_transition: true
```

`@part1`
A project is a directory that contains project files.

Also, an opportunity to exercise empathy for anyone who might use your code (including your future self!)

Project files may be organized into subdirectories or kept at the top-level.

```
my_project
├── LICENSE
├── README.md
├── code
│   └── analysis.ipynb   <= Not modular!
└── requirements.txt
```

First Python Project Principle: Modularity


`@script`



---
## Modular versus Monolithic

```yaml
type: "FullSlide"
key: "d00704249b"
```

`@part1`
The opposite of modular is monolithic.

A monolithic file, like `analysis.ipynb`, could contain all project {{1}}
- code, {{1}}
- documentation, and {{1}}
- output. {{1}}

To get the benefits of modularity and the convenience of a single file: {{2}}
1. start with small files and then {{2}}
2. combine them into a larger file later on. {{2}}


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

Reusability Principle: Don't repeat code! Reuse it! {{1}}

One way to avoid code repetition is to {{2}}
- define a block of reusable code called a function, and {{2}}
- replace the repetitive code with function calls. {{2}}

To further improve the modularity and reusability of our code, we will {{3}}
- define functions in `modules` and {{3}}
- use the functions in `scripts`. {{3}}


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

Scripts and modules differ in how and why they are used.{{1}}

| Filetype | Verb   | Goal             |
|----------|--------|------------------|
| Script   | Run    | Perform actions  |
| Module   | Import | Define objects   |
{{1}}


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

This order can be visualized as a diagram called a directed acyclic graph (DAG). {{1}}

![](https://assets.datacamp.com/production/repositories/3687/datasets/3d4fdb37d0924a05ab75fcc786dc590b33dbbf4b/simple_dag.png) {{1}}

Each script {{2}}
- handles one and only one step in the process {{2}}
- imports the tools it needs from modules that are included in the project. {{2}}

It is common to run scripts in a shell, for example Bash (Bourne again shell). {{3}}


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

2. Create a script called `greet.py`, which imports the `say` module and calls the `hello` function:{{1}}
```python
import say
say.hello()
```{{1}}
3. Type `python greet.py` in a shell and press Enter. {{2}}


`@script`



---
## Running modules as scripts

```yaml
type: "FullSlide"
key: "4b698e100b"
```

`@part1`
It is possible for the same file to be used as both a module and a script.

To demonstrate this, add the code below to the end of `say.py`: {{1}}
```python
if __name__ == '__main__':
    hello()
```
{{1}}

The code above calls the `hello` function only when `say` is run as a script. {{2}}

The `if` statement prevents `hello` from being called when `say` is imported as a module. {{3}}

Adding `hello()` to `say.py` without the `if` statement, would make `greet.py` print `Hello World!` twice!. {{4}}


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
1. Make a directory (`mkdir`) called `my_project`
2. Create a copy (`cp`) of `say.py` called `__main__.py` 
3. Move (`mv`) `__main__.py` into `my_project`
4. Run the project like you would run a script

```bash
mkdir my_project
cp say.py __main__.py
mv __main__.py my_project
python my_project
```{{1}}
You can zip the whole project and then run the zip file:
{{2}}
```bash
python -m zipfile -c my_project.zip my_project/*
python my_project.zip
```{{2}}


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
## Let's practice running scripts and importing modules!

```yaml
type: "FinalSlide"
key: "45042a1bd2"
```

`@script`


