# Coding Best Practices 2

---
**Overview.**  Dude's we are rolling now. We know a lot, lets make sure that we can execute what we know in a clear and readable manner. This is where style matters.

---

## Programming style

Yes, style counts.  We're not only trying to get something done, we're also communicating with others who may look at our code and possibly use it.  A clear style makes that communication more effective.

Here are two resources with specific style guides. There is the classic "[PEP8](https://www.python.org/dev/peps/pep-0008/)" and Google's [style guide](https://github.com/google/styleguide/blob/gh-pages/pyguide.md) for python. We took the liberty to pull some lessons from these guides for you to keep in mind.

## Put an overall summary of your program at the top.

In a Jupyter notebook, just create a markdown cell and describe what it does and your name (so we have someone to blame!). In a ``.py`` file, do it all in triple quotes.  

Same idea for functions. When writing a function, create a docstring which should give enough information to write a call to the function without reading the function's code. Here is an example from before.
```python
def squareme(number):
    """
    Takes numerical input and returns its square
    """
    return number**2       
```


## Lines should be no longer than 79 characters.

Yes, we are fortunate to be endowed with large monitors. This does not mean that we should have one line of code that spans all 30 inches. Why, this is about readability and short one line statements are easy to read.

Here is an example. How would you like to figure out what is going on with this on line of code:
```
b = @(g,z_hat,Omega) d.^(1+(-1).*sigma).*z_hat.^((-1)+sigma+((g+(-1).*mu).^2.*upsilon.^(-4)+2.*((-1).*g+g.*gamma+delta+rho).*upsilon.^(-2)).^(1/2)+((-1).*g+mu).*upsilon.^(-2)).*(1+(-1).*((-1).*g+g.*gamma+delta+rho).*((-1).*g+g.*gamma+delta+rho+(-1).*((-1)+sigma).*((-1).*g+mu+(1/2).*((-1)+sigma).*upsilon.^2)).^(-1));
```
Not really right? True story, this is from code associated with a paper one of the Data Bootcamp team members.

How do I know how many are 79 characters. Good question. First, traditional IDEs or text editors like Atom will have a faint line often indicating where you should stop. Second, in Jupyter, we often think that the middle of the screen is the dividing line. Also, if your command window has a scroll bar, you went too far.

There are times when to break the rules. Like in life, you will know it when you see it.

## Spacing

Here are some spacing rules that we like...

* Skip two lines before and after a function definition.

* Skip lines here and there where you think it makes sense.

## Use functions for repetitive tasks

Often you will have to perform some task repeatedly. For these repeat tasks create a function that can perform them. For example, we may have to square a number many, many times. Solution: create a function that squares numbers.

Why should we do this... big picture is that its about readability and debugging, but here are some reasons:

* It allows us to see and conceive of code in sub-components where some of these components are the functions. So as you read through, create, a larger file, these functions are a clearly defined sub-component.   

* This allows us to reuse code rather than constantly have to rewrite the same thing over and over. This will prevent "fat finger" type coding errors. In the ``squareme`` example, if you were always exponenting different things, you might accidently type ``*`` rather than ``**``.

* They also facilitate debugging. Again errors are going to happen. So the solution is to create code that allows for the identification and quick correction of errors. How do functions help? First, because your code is broken down into sub-components you can isolate where the problem is. Second, when you correct and test your fix, you only need to test and execute that one function, not the whole thing. In other words, you can find and correct the problem much faster than if functions were not used.

One final point from Google "Prefer small and focused functions." If it is long, think about whether it can be broken up without harming the structure of the program. The point here is that keeping your functions short and simple makes it easier for other people to read and modify your code.


## Naming

From the Google guide "Function names, variable names, and filenames should be descriptive; eschew abbreviation. In particular, do not use abbreviations that are ambiguous or unfamiliar to readers outside your project, and do not abbreviate by deleting letters within a word."

## BE CONSISTENT

Don't do random stuff. Pick a style and stick with it. When you name functions, files, etc. pick a naming style and stick to it. When using white space, pick your preferred method and stick to it. You get the idea. When you are handed code, take a few minutes to look at the code around you and determine its style and follow it. If code you add to a file looks drastically different from the existing code around it, it throws readers out of their rhythm when they go to read it. Avoid this.
