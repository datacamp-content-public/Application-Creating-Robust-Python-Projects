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
Welcome to the course!
In this video, you will learn about Python Project Principles.


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
In the Creating Robust Python Projects course overall,
you will learn to follow principles and best practices,
and to use helpful technologies and techniques
for writing and editing Python code and documentation.


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
A project is a folder with project files inside.
I like to think of each project as a chance to
practice empathy for people who might want to use your code.
Time spent on crafting a good project is an investment in the future.

Project files can be in subdirectories or in the top-level directory.
In this example, all of the files are at the top level except for analysis.ipynb, which is in the "code" subdirectory.
This brings us to our first Python Project Principle: Modularity.


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
Analysis.ipynb is not in line with the Modularity Principle,
because every step in the analysis is done by one file.
A more modular approach would be to have one file for each step in the analysis.


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
2. create a separate larger file later. {{2}}


`@script`
The opposite of modular is monolithic.
A monolithic file, like the analysis.ipynb file we say earlier,
might contain all of the project's code, docs, and output.

This can be very convenient, but this convenience comes at a price. 

To get the best of both worlds start small
and then create a separate large file later on.


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
- call the functions in `scripts`. {{3}}


`@script`
If you begin to notice patterns in the code, it is time to start thinking about the next Python Project Principle: Reusability.
According to the Reusability Principle, you should reuse code instead of repeating it. 
To avoid code repetition, you will need to use functions.
Functions are reusable blocks of code that can be defined once and then called as many times as needed to get the job done.
To take our use of functions to the next level, we will define functions in files called modules and then call the functions in files called scripts.


---
## Modules versus Scripts

```yaml
type: "FullSlide"
key: "ae33b5d1d6"
```

`@part1`
Modules and scripts
- are Python code files that
- have `.py` extensions.

Modules and scripts differ in how and why they are used.{{1}}

| Filetype |  How?  |       Why?       |
|:--------:|:------:|:----------------:|
| Module   | Import | Define functions |
| Script   | Run    |  Call functions  |
{{1}}


`@script`
Modules and scripts are Python code files with .py extensions.
They differ only in how and why they are used.
Modules are imported to define functions (and other Python objects),
while scripts are run to perform actions (typically by calling functions).


---
## Importing Modules

```yaml
type: "FullSlide"
key: "919381ac3b"
```

`@part1`
1. A module named `say`, which uses the `def` statement to define a function named `hello` that prints `Hello World!`:
```python
def hello():
       print("Hello World!")
```

2. A script named `greet`, which imports the `say` module and calls the `hello` function:{{1}}
```python
import say
say.hello()
```{{1}}


`@script`
Here is an example of a module named say that defines a function named hello.
Next, there is an example of script that imports the say module and calls its hello function.
I do not include the .py extension when referring to modules and scripts, nor do I include parentheses in functions names.


---
## Running Modules as Scripts

```yaml
type: "FullSlide"
key: "4b698e100b"
```

`@part1`
It is possible for the same file to be used as both a module and a script.

To demonstrate this, we could add the code below to the end of the `say` module: {{1}}
```python
if __name__ == '__main__':
    hello()
```
{{1}}

The code above calls the `hello` function only when `say` is run as a script. {{2}}

The `if` statement prevents `hello` from being called when `say` is imported. {{3}}

What would happen if `say` included the function call, but not the `if` statement? {{4}}

Running `greet` would print "Hello World!" twice: once when `say` is imported and then a second time when `greet` calls `hello`. {{5}}


`@script`
A Python code file can be used as both a module and a script.

To make a module/script hybrid we need to use an if statement that calls a function only when the file is run as a script and not when it is imported as a module. 

In the example of the say module and greet script, this if statement allows say to print "Hello World!" when it is run, but also keeps the hello function from being called when say is imported.

What if we added the function call to say without the if statement? 
In that case, running greet would print "Hello World!" twice:
The first time when say is imported and then again when greet calls the hello function.

Python code files, regardless of whether they are modules or scripts, are executed immediately upon import.


---
## Running Scripts

```yaml
type: "FullSlide"
key: "4de73bc2a6"
```

`@part1`
Scripts in data science projects are typically run in a particular order.

This order can be visualized as a diagram called a directed acyclic graph (DAG): {{1}}

![](https://assets.datacamp.com/production/repositories/3687/datasets/3d4fdb37d0924a05ab75fcc786dc590b33dbbf4b/simple_dag.png) {{1}}

Each script handles one step in the process and imports the tools it needs from modules that are included in the project. {{2}}

To run a series of scripts, use the `import` statement as in the example below.{{3}}
```python
import get_data, clean_data, fit_model, evaluate_model
```{{3}}


`@script`
Scripts in data science projects are typically run in a sequence that be shown as a directed acyclic graph.

In the sequence, each script does one job and imports the tools it needs from modules in the project.

It can be tedious to run each script one after another.
Your first instinct may be to combine the scripts into a monolithic file.
Instead, you could write a script to run all of the other scripts in the project.
A clever way to do this is to use the import statement.
You can import one script per line or include all of the scripts on one line separated by commas.

I think it's worth repeating: Python code files, regardless of whether they are modules or scripts, are executed immediately upon import.


---
## Running Projects

```yaml
type: "FullSlide"
key: "bfeb750a7e"
```

`@part1`
Code that runs scripts is most useful in a top-level script called `__main__.py`.

`__main__.py` can be executed from outside of the project using the project name. {{2}}

This can be setup to work anywhere in the file system, but for now we will run projects from one level above the project directory. {{2}}

Interestingly, this works even if the project is turned into a zip file. {{2}}

A great example of how we can enjoy the {{3}}
- convenience of including everything in a single file and {{3}}
- without sacrificing modularity! {{3}}


`@script`
The script that uses the import statement to execute all of the other scripts in a project should be at the top level and will be most useful if it is named __main__.py.
Double underscores around Python names are pronounced dunder.
This indicates that the name is special and has some superpowers. 
In the case of __main__.py, the main superpower is that this script can be executed from outside a project using the project name. This will work even if


---
## Let's practice working with scripts and modules!

```yaml
type: "FinalSlide"
key: "45042a1bd2"
```

`@script`


