## Python Packaging for dinguses


Is packaging confusing for you? Have you reread [docs](https://docs.python.org/3/tutorial/modules.html#packages) and [tutorials](https://python-packaging.readthedocs.io) over and over again? 

Are Stack Overflow [answers](https://stackoverflow.com/questions/6323860/sibling-package-imports/27878845) making you feel increasingly insecure about your reading comprehension skills? 

This is an example package to remind myself and other dinguses how to create notebooks and packages for development and analysis projects...AND TO ONCE AND FOR ALL BREAK FREE OF THE DREADED "NO MODULE NAMED" ERROR!


### 1. Packages, Modules and Imports

### 2. Setup.py and \_\_init\_\_.py, wut do they do?

### 3. Pipenv is your best friend (if you don't have any friends)

Pipenv is great (!!link to docs and such)

#### pipenv install vs pipenv install --dev

```pipenv install --dev . -e ```

- lets you install the working directory "."
    - in "dev" mode (meaning it's not going to install the same way if you distribute the package)
    - in edit mode ("-e"), which allows you to edit the installed package (very good for slowly turning your dingus code into better dingus code)

## The workflow

### Part 1: getting it set up

0. USE A VCS YA DINGUS (GIT INIT RIGHT MEOW) 

1. pipenv install --\<three | two>

2. Set up your directory

    ```
    dingus/                   top level package
        notebooks/            put ur dingus notebooks here, dingus

        src/                  put ur dingus code here, dingus
            __init__.py
            dinguscode1.py    or use sub directories like a non-dingus
            dinguscode2.py  
        setup.py              use setuptools.setup and specify 'src' in package
                                (or use find_packages to automatically detect)
    ```

3. Install your package in --dev and -e modes 
    ``` 
    $ pipenv install --dev . -e
    ```

### Note on the environment

- install pylint inside the environment (pipenv install --dev pylint)
