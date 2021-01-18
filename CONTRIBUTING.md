# Contributing

## Github Flow

For this project we will use the [Github workflow](https://guides.github.com/introduction/flow/) development model. Please reade the guide at the provided link to have an idea of how it works.

In short, 
- Every module will have its own branch, named using the style `module_x_y`
- You should add the Jupyter notebook or Python files in the appropriate folder, i.e.
    - Each module will have a folder named `module_x`
    - Each submodule will have a folder name `module_x.y`
- When you finish developing your module, open a pull request to ask the other instructors to review what you've done
- After the pull request is approved, it will be merged in the `main` branch.

For example, if you have to create the code for module `1.3`, you should create the branch `module_1_3`, create (if does not exist) the folder `module_1`, and then the folder `module_1.3` inside it. You will write all the code inside that folder. When you have finished, you will open a pull request and the other instructors will review it.

## Code Conventions

We will follow the standard Python code conventions, as described in [PEP 8](https://www.python.org/dev/peps/pep-0008/) 
and [PEP 257](https://www.python.org/dev/peps/pep-0257/).
Here we present a quick summary of the most important conventions:

- All files **must** be encoded in UTF-8 format.
- Indentation: use 4 spaces per indentation level.
- Function and variable names: 
function names should be lowercase, with words separated by underscores as necessary to improve readability.
Variable names follow the same convention as function names.
  - Examples: ```def function_name(x), variable_name = 5```
- Constants: Constants are usually defined on a module level and written in all capital letters with 
underscores separating words. Examples include MAX_OVERFLOW and TOTAL.
  - If you use constants, please **always** define them at the top of the notebook.
- Class names should normally use the CapWords convention, e.g. `ClassName`.
- Avoid variable and function names that avoid built-in functions or libraries, as for example `sys`, `type`, `string`, 
`global`, `lambda`, etc.
- If you write externals classes or functions, please comment them with [docstrings](https://www.python.org/dev/peps/pep-0257/).

An example of well-written code is:
```python
def function_name(parameter_one, parameter_two=1):
    """Returns the first parameter to the power of the second parameter.

    Arguments:
    parameter_one -- a base.
    parameter_two -- an exponent (default 1).
    """
    return parameter_one ** parameter_two
```


Please keep the spacing consistent. A good idea is to use a code prettifier; 
there is one available for Jupyter in the [extensions](jupyter_contrib_nbextensions). 
After you enable the extensions (see below), you can install the prettifier by running
```jupyter nbextension enable code_prettify/code_prettify``` in a terminal, or using
the provided web interface as explained below.

In Markdown cells, by convention, you should denote methods and function names with trailing
parentheses, e.g. `method()`, `find()`, etc., to help the reader discriminate them from variables.

## Useful tools

The package `jupyter_contrib_nbextensions` provides a set of useful Jupyter extensions
which you may find helpful while working on this project.

Extensions are automatically installed if you used the provided `requirements.txt`;
however, you need to tell Jupyter to use them by running 
`jupyter contrib nbextension install --user`
in your virtual environment.


After you installed the extensions, you can enable them in your browser from 
Jupyter's extension manager, by navigating to ```http://localhost:8888/tree#nbextensions_configurator```
(replace ```http://localhost:8888/``` with the address of your Jupyter server, if needed).

Some recommended extensions are:
- Code prettifier, self-explanatory;
- Table of contents, which comes in handy when working with large notebooks;
- Live Markdown Preview, self-explanatory;
- Scratchpad, which allows you to fire a throwaway cell by pressing CTRL+B.
