# How-to

You get a lot of power when you use Beautiful Soup. Sometimes that power comes
with some gotchas or complications. This page is your guide to carefree parsing.

## Changing the parsed tree

Beautiful Soup parses your input HTML into a series of nested objects that
represent the hierarchical structure of an HTML document. You can make changes
to those objects in a variety of ways:

-   Remove elements
-   Insert elements into an existing tag
-   Change the name of a tag
-   Delete an element
-   Cut a tag out of the tree
-   Replace an element with another one
-   Add or remove enclosing tags for an element
-   Copy elements from one one tag to another

### Remove elements

Removing elements from the tree is pretty easy:

#### To delete a tag from the tree

```python
html = '<div><ul><li>one</li><li>two</li><li>three</li><li>four</li></ul></div>'

soup = BeautifulSoup(html, 'html.parser')

tag = soup.ul

tag.decompose()
```

Note that [decompose] removes the calling tag along with all of its contents and
destroys it. You may not want to take a drastic step.

#### To remove a containing tag while leaving its contents behind

```python
html = '<div><ul><li>one</li><li>two</li><li>three</li><li>four</li></ul></div>'

soup = BeautifulSoup(html, 'html.parser')

tag = soup.ul

tag.unwrap()
# <ul></ul>
```

The tag still exists, but its contents are lesft in the tree with the same
parent it used to have.

### Copy elements from one one tag to another

There are many scenarios in which you want to move the contents of one tag into
another tag. This can be trivial or tricky depending on the specifics. Here are
a few examples.

You might think that a good way to copy tags from one tag to another (perhaps
changing some of them along the way) would be to iterate through the contents of
the source tag, inserting each into the new tag. Like this:

```python
html = '<div><ul><li>one</li><li>two</li><li>three</li><li>four</li></ul></div>'

soup = BeautifulSoup(html, 'html.parser')

old_list = soup.ul

new_list = soup.new_tag('ol')

for element in old_list.contents:
    new_list.append(element)
```

The results are not what you hoped:

```python
new_list
# <ol><li>one</li><li>three</li></ol>

old_list
# <ul><li>two</li><li>four</li></ul>
```
The problem is that when you append an element to a tag, it gets removed from
the old tag. This means that you'll encounter some indexing problems with the
list you're iterating through. You'll only get every other item in the new list.

The easiest way to fix this problem is to iterate through the list in reverse
order, so that the removal of any given item will not affect the index of items
you haven't seen yet:

```python
html = '<div><ul><li>one</li><li>two</li><li>three</li></ul></div>'

soup = BeautifulSoup(html, 'html.parser')

old_list = soup.ul

new_list = soup.new_tag('ol')

for element in reversed(old_list.contents):
    new_list.append(element)
```


<!--
----|----|10--|----|20--|----|30--|----|40--|----|50--|----|60--|----|70--|----|
-->
