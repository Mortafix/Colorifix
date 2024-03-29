![PyPI - Python Version](https://img.shields.io/pypi/pyversions/colorifix)
[![PyPI](https://img.shields.io/pypi/v/colorifix?color=red)](https://pypi.org/project/colorifix/)
[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)

# Setup

```
pip3 install colorifix
```

# Requirements
* Python 3.6+

# Usage
It's very simple to use, just remember three symbols:
* `#` to set a **color**
* `@` to set a **style**
* `!` to set a **background**
```python
from colorifix.colorifix import paint

paint("[#red]String to color in red [#blue]and in blue")
paint("[#yellow !green]One color and background at a time,[#red #cyan] last set win")
paint("[@bold @underline]Many styles in one [@dim]string")
paint("[#44 !123]You can use int bash colors")
```
![Examples](images/examples.png)
### Remove styles
You can **remove** every part of a style with the symbol `/` followed by the symbol of the style you want to remove. You can use it alone to remove every styles, it will remove every styles anyway at the end of the string.
```python
paint("[#yellow @underline]This is a yellow underline string[/@], now only yellow[/].")
```
![Remove example](images/remove.png)
### Print or not print
You can choose to **print** the string or just **save** it in a variable.
```python
colored_str = paint("[!black @dim]Hello Color![/]") # save it
ppaint("[!42]Again![/]") # print it directly
paint("[!42]Again![/]", False) # print it from main function, same as above
```

# Colors
To disaply all different colors, you can use the function `sample`
```python
from colorifix.colorifix import sample

sample()  # base colors
sample(complete=True)  # to display all bash int colors
```
![Base colors](images/colors.png)
