# Coding Best Practices 1

---
**Overview.**  Now that we know a bit about how to code, we discuss how to code in an **effective** and **readable** manner.

**Pythons.**  Jupyter, comments, debugging,

---

## Structuring code within Jupyter

Lets take a quick step back and discuss how to **use** Jupyter to create effective, readable code. Often we are writing much longer programs. In this case it would be silly to have every single cell be composed of just one line. Why? Lots of reasons, but the most important reasons is that that reading the code AND understanding it's context within the whole program would be very hard to do. **And readable code is something that we should aspire to.**

**Use a code cell for a certain task.** For example, one code cell is dedicated to reading in the data. Another code cell performs one manipulation of the data (which could take multiple lines of code), another code cell performs a different manipulation, and then another is dedicated to plotting a figure. So each code cell is accomplishing a specific task at hand. Why not put everything in one code cell? Again, this is problematic regarding readability.

Applying this practice is also important because chopping up the code into different cells helps debugging. For example, you may have aspects of your code that works, but other parts are having problems. Trust us, this will happen often -- there is no avoiding it. So rather than running the whole program over and over again to debug only a subset, you have that subset of code in its own cell and then work on that on its own.

Let's give it a try.  Type these commands into **one** code cell:

```python
a = 'some'
b = 'thing'
c = a + b
print('c =', c)
```
When we run the code, we see that the first three lines produce no output.  The last one produces the output `c = something`. What we have now is one code cell performing one distinct task.

## Using Markdown to facilitate readability

One of the nice features of Jupyter is that it can mix nicely formatted text via Markdown with code. This allows you to describe, at a high-level the steps that your analysis is walking through. The "high-level" aspect of this is nice in that you can structure your notebook where, say your Manager, can follow your steps without having to delve deep into the details of the code. Moreover, this allows us to "tell the story" when working with data.

For example, in the cell above the code discussed above, you could insert a cell saying something to the effect:
```Markdown
# Creating a word by addition
Here is an example where I am using the addition function on strings to create the word something
```

**Exercise.** Do this. Remind yourself how to create a markdown cell and insert the markdown code above the "something" code cell.

## Add comments to your code

We also want to mechanically explain what individual lines of code our doing. One of the rules of good code is that **we explain what we've done---in the code**.  Think about this aspect as writing and explaining code that one of our classmates can understand without help. These explanations are referred to as comments.

Add a comment with the hash character (#).  Anything in a line after a hash is a comment, meaning it's ignored by Python.  Here are some examples:

```python
# everything that appears after this symbol (in the same line) is a comment!
# comments help PEOPLE understand the code, but PYTHON ignores them!
# we're going to add 4 and 5
4 + 5           # here we're doing it
print(4+5)      # here we're printing it
```

We often put comments like this in our code.  Not quite this basic, but close. One of the unwritten "laws of nature" in programming is that code is read much more often than it is written. See these links...they're awesome:
[1](http://docs.python-guide.org/en/latest/writing/style/) [2](https://blogs.msdn.microsoft.com/oldnewthing/20070406-00/?p=27343) [3](https://blog.codinghorror.com/when-understanding-means-rewriting/).

Writing informative comments will not only lead to others thanking you for saving them time, but you will find that you thank yourself very frequently.

Final point on comments: **Update your comments as you update your code!** Nothing is worse than finding comments that contradict the code. So as you modify your code, modify your comments. Again, so when you take a break and return to what your doing, you know what's up.

**Exercise moving forward.** Practice writing comments **all the time**. Whenever you learn something new, write a comment explaining it in your code. It feels tedious, but the best coders always explain their work. It's a good habit to develop.
