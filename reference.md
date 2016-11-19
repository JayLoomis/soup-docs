# Reference

## Objects

Beautiful Soup defines four fundamentally important data types:

| Type                                                | Description                                                            |
| --------------------------------------------------- | ---------------------------------------------------------------------- |
| [**bs4.BeautifulSoup**](#beautifulsoup)             | The core object for an instance of parsed markup, contains the others. |
| [**bs4.element.Tag**](#tag)                         | Represents elements that can contain children.                         |
| [**bs4.element.NavigableString**](#navigablestring) | Represents text elements.                                              |
| [**bs4.element.Comment**](#comment)                 | Like **NavigableString**, but renders with comment taggin in markup.   |

### BeautifulSoup

The **BeautifulSoup** class (**bs4.BeautifulSoup**) is

### Tag

The **Tag** class (**bs4.element.Tag**) is the primary data type used by
Beautiful Soup to represent markup element data. You use the properties and
methods of **Tag** for most navigation of HTML strings.

| Property                                     | Description                                                                                       |
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

#### Tag.attrs

A dictionary containing all of the attributes set for the **Tag**.

The keys are the names of the attributes as they appear in the source text.

If an HTML attribute can have multiple values (most commonly _`class`_),
BeautifulSoup represents its value as a list. This is true even if there is only
a single value for that class in the present instance.

You can also use the **Tag**'s identifier as an alias for _attrs_, using
dictionary key notation with it to get and set values. For example: 

```python
href = tag.attrs['href']
```

Is functionally identical to:

```python
href = tag['href']
```

You can treat the **Tag** identifier as you would a dictionary in other ways,
too.

##### See also

-   [**Tag**](#tag)
-   [Reference](#reference)

<!--
----|----|10--|----|20--|----|30--|----|40--|----|50--|----|60--|----|70--|----|
-->

#### Tag.children

#### Tag.contents

#### Tag.next_element

#### Tag.next_elements

#### Tag.next_sibling

#### Tag.next_siblings

#### Tag.parent

#### Tag.parents

#### Tag.previous_element

#### Tag.previous_elements

#### Tag.previous_sibling

#### Tag.previous_siblings

#### Tag.string

#### Tag.strings

#### Tag.stripped_strings

#### Tag.<_tag name_>



### NavigableString

The **NavigableString** class (**bs4.element.NavigableString**) is 

### Comment

The **Comment** class (**bs4.element.Comment**) is essentially the same thing
as the [**NavigableString**](#navigablestring) class. The only ovious
difference is that when rendered in markup, its text is surrounded by comment
tags (\<\!\-- --\>).

Because **Comment** is a distinct class from both [**Tag**](#tag) and
[**NavigableString**](#navigablestring), you avoid all of the special-case
shenanigans you would have to handle otherwise.

#### See also

-   [Objects](#objects)
-   [Reference](#reference)

<!--
----|----|10--|----|20--|----|30--|----|40--|----|50--|----|60--|----|70--|----|
-->
