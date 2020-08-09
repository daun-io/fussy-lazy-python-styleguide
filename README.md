# Fussy lazy python styleguide
[Beautiful is better than ugly, Readability counts](https://www.python.org/dev/peps/pep-0020/). But it takes time and efforts to figure out best answers.  
[We're standing on the shoulders of giants](https://github.com/trending/python), styling should be easy and fast.

# IDE
We recommend [vscode](https://code.visualstudio.com/) for best community supports and latest features

# Documented Rules

We use linter to keep rules in mind however you can also check [one of best practice](https://google.github.io/styleguide/pyguide.html)

# Linter

**Use pylint.** Pylint is a Python static code analysis tool which looks for programming errors, helps enforcing a coding standard, sniffs for code smells and offers simple refactoring suggestions.

```
pip install pylint
```
You can manually lint your scripts before commit like this.
```
pylint your_script.py
```
However you'll probably forget about linting if you're doing it manually everytime. You can discover ways of integrating your linter within [vscode](https://code.visualstudio.com/docs/python/linting).  
Keep trying to get better scores from pylint so you can achieve better code.

# Formatter

## Import-order sorting

**Use isort.** isort is a Python utility / library to sort imports alphabetically, and automatically separated into sections and by type. It provides a command line utility, Python library and plugins for various editors to quickly sort all your imports. It requires Python 3.6+ to run but supports formatting Python 2 code too.

```
pip install isort
```
You can manually format your scripts before commit like this.
```
black your_script.py
```

## Overall formatting

**Use black.** Black is the uncompromising Python code formatter. By using it, you agree to cede control over minutiae of hand-formatting. In return, Black gives you speed, determinism, and freedom from pycodestyle nagging about formatting. You will save time and mental energy for more important matters.

```
pip install black
```
You can manually format your scripts before commit like this.
```
black your_script.py
```
You should also check for the integration which [helps formatting for everytime you save your code.](https://code.visualstudio.com/docs/python/editing#_run-selectionline-in-terminal-repl)

Although **isort** and **black** has different style of formatting for some importing stuffs you can control it by executing isort first and black later.

```
isort your_script.py && black your_script.py
```

## Docstring

**Use [autodocstring](https://marketplace.visualstudio.com/items?itemName=njpwerner.autodocstring).** autodocstring is a vscode extension to quickly generate docstrings for python functions. Among docstring formats that autodocstring supports, we recommend 'Google' format.

# Efforts to cover more laziness

You can also check following toolings.

* [PathIntellisense](https://marketplace.visualstudio.com/items?itemName=christian-kohler.path-intellisense) for autocompleting file path
* [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode) for formatting surroundings scripts (including .json, .yaml, etc)

