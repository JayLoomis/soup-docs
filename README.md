# Beautiful Soup Documentation Project
Enhanced documentation for Beautiful Soup

## Introduction

Leonard Richardson's
[Beautiful Soup](https://www.crummy.com/software/BeautifulSoup/) is an
excellent Python package for dealing with markup files, especially HTML.
However, as with so many great libraries, I found my learning curve to be
steepended by the way the documentation presented it. This project is my
attempt to improve the documentation experience. I'm doing this mostly
because I want to keep using Beautiful Soup in my own work, and I want a
useful reference.

## Beautiful Soup overview

The basic functionality of Beautiful Soup is pretty straightforward: you give
it some markup text and it creates a representation of that markup as nested
objects. Most of the members of those objects represent ways to move around
the objects to find what you need.

People often talk about Beautiful Soup as a great tool for wrangling sketchy
HTML. I can't really attest to this, because I've only used it for my own
content, and I'm pretty fastidious when it comes to well-formedness and 
prettiness of markup. I can say from personal experience that it works extremely
well for navigating clean HTML, and I believe what I've heard about the messy
stuff, too.

It's my view that using the `html` package to parse your way through HTML
maually is a rookie mistake (one that I was prompted to make by misleading
comments in Python books that should have known better). Unless there's an
extraordinarily good reason to (and I honestly can't think of one), only a
chump would pass up BeautifulSoup for Python HTML work.

## How to use these docs

I've organized this documentation into three parts:

-   [Conceptual Overview](conceptual_overview.md) gives an overview of how the
    package works. It walks you through the individual tasks with all the
    gotchas and caveats described.
    
-   [How-to](how-to.md) gives succinct instructions for indiviudal tasks with code
    examples.
    
-   [Reference](reference.md) describes each programming element in the package in
    detail.

If you're excited to just get something working without really understanding
what's going on, then I don't agree with your methods, but you should go to
[How-to](how-to.md).

If you're the sort of person who wants to know how things work before tinkering
around with them, then I commend you, and you should start with
[Conceptual Overview](conceptual_overview.md).

If looking at the inner-workings of something best helps you understand things,
or if you've used Beautiful Soup before and just need to remember syntax, the
[Reference](reference.md) is the place for you.

## Disclaimer

I didn't ask permission to do this work. I have no affiliation with Leonard
Richardson. Nothing here is official, or guaranteed to be up-to-date with the
code. I'm trying hard to be accurate to the latest (macOS) `pip`-accessible
version at the time of writing, which is 4.5.1.

If I get this to a state that I'm happy with, maybe I'll reach out to Mr.
Richardson to offer it up in a more official way. But probably not, because
that kind of interaction is pretty uncomfortable ("Hi, I'm a technical
writer, and I didn't like the work you did documenting your really great
project that you didn't get paid for.").

## Important links

The source of truth must naturally come from the developer:

-    [Beautiful Soup official site](https://www.crummy.com/software/BeautifulSoup/)
-    [Official documentation](https://www.crummy.com/software/BeautifulSoup/bs4/doc/)

<!--
----|----|10--|----|20--|----|30--|----|40--|----|50--|----|60--|----|70--|----|
-->
