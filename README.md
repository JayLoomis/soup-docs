# Beautiful Soup Documentation Project
Enhanced documentation for Beautiful Soup

## Introduction

Leonard Richardson's
[Beautiful Soup](https://www.crummy.com/software/BeautifulSoup/) is an
excellent Python package for dealing with markup files, especially HTML.
However, as with so many great libraries, its documentation isn't great, and
artificially increases the learning curve. This project is my attempt to
improve the documentation experience. I'm doing this mostly because I want to
keep using Beautiful Soup in my own work, and I want a useful reference.

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

## Reference

### Objects

Beautiful Soup defines four fundamentally important data types:

| Type                                                | Description                                                            |
| --------------------------------------------------- | ---------------------------------------------------------------------- |
| [**bs4.BeautifulSoup**](#beautifulsoup)             | The core object for an instance of parsed markup, contains the others. |
| [**bs4.element.Tag**](#tag)                         | Represents elements that can contain children.                         |
| [**bs4.element.NavigableString**](#navigablestring) | Represents text elements.                                              |
| [**bs4.element.Comment**](#comment)                 | Like **NavigableString**, but renders with comment taggin in markup.   |

#### Tag

The **Tag** class (**bs4.element.Tag**) is the primary data type used by
Beautiful Soup to represent markup element data. 

| Attribute                                    | Description                                                                                       |
| -------------------------------------------- | ------------------------------------------------------------------------------------------------- |
| [_attrs_](#tagattrs)                         | A dictionary containing the element's attributes.                                                 |
| [_children_](#tagchildren)                   | An generator to iterate through the direct children of this element.                              |
| [_contents_](#tagcontents)                   | A list of all the direct children of this element.                                                |
| [_next_element_](#tagnext_element)           | The next markup element in the source text.                                                       |
| [_next_elements_](#tagnext_elements)         | A generator to iterate through all the following elements.                                        |
| [_next_sibling_](#tagnext_sibling)           | The next markup element with the same parent as this one.                                         |
| [_next_siblings_](#tagnext_siblings)         | A generator to iterate through all the following elements with the same parent as this one.       |
| [_parent_](#tagparent)                       | The tag that directly contains this one.                                                          |
| [_parents_](#tagparents)                     | A generator to iterate through all the ancestors of this element up to the document level.        |
| [_previous_element_](#tagprevious_element)   | The markup element that precedes this one.                                                        |
| [_previous_elements_](#tagprevious_elements) | A generator to iterate through all the preceding elements.                                        |
| [_previous_sibling_](#tagprevious_sibling)   | The previous element with the same parent as this one.                                            |
| [_previous_siblings_](#tagprevious_siblings) | A generator to iterate through all the previous elements with the same parent as this one.        |
| [_string_](#tagstring)                       | The string inside this element, if this element has only one child that is a **NavigableString**. |
| [_strings_](#tagstrings)                     | A generator to iterate through all of the **NavigableString**s in the element.                    |
| [_stripped_strings_](#tagstripped_strings)   | As _strings_, but generates the strings with leading and trailing whitespace removed.             |
| [<_tag name_>](#tagtag-name)                 | The first instance of the specified tag in this element (equivalent to **Tag**.**find**()).       |

##### Tag.attrs

##### Tag.children

##### Tag.contents

##### Tag.next_element

##### Tag.next_elements

##### Tag.next_sibling

##### Tag.next_siblings

##### Tag.parent

##### Tag.parents

##### Tag.previous_element

##### Tag.previous_elements

##### Tag.previous_sibling

##### Tag.previous_siblings

##### Tag.string

##### Tag.strings

##### Tag.stripped_strings

##### Tag.<_tag name_>



#### NavigableString
<!--
----|----|10--|----|20--|----|30--|----|40--|----|50--|----|60--|----|70--|----|
-->
