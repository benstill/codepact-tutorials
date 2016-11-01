# CodePact Templates in Markdown

CodePact templates create legal agreements on a web interface that you can sign electronically.

It's simple to create CodePact Templates (**Templates**) with **options, variables and guidance** using:

- [Markdown documents](https://help.github.com/articles/github-flavored-markdown/) (explained in this tutorial); or
- [Word Documents (explained here)](http://guide.codepact.com/introduction/).

Using markdown is better because you can store them on [Github](http://github.com). There are some complete templates [here](http://github.com/codepact) - they're **open source**, so feel free to fork and submit pull requests!

It'll only take you 10 seconds to make your first CodePact template from Markdown:

1.  Login to http://codepact.com and go to https://codepact.com/newEnter (or click "Create Template" on the dash).

2.  On the left panel, click "Add Example Markdown Agreement" (or copy and paste the markdown from a template [here](http://github.com/codepact)).

4.  Click "Save New Draft" to see the template preview then click "Finalize".  Now you can use the template to create an agreement.

## Template Basics

Every legal agreement covers a list of topics (usually there's an index).  Each topic heading is followed by a clause.  Topic headings can't be longer than 50 characters.

In a CodePact template, there are two main possibilities.

**1.  Topic Heading with One Clause Option**

All you need is a topic heading (## Markdown heading) and normal text for the clause after it.  Example:

```markdown
## Topic Heading

This is the clause text right here.

```

**2.  Topic Heading with Multiple Clause Options**

If there are *clause options* you need a topic heading (## Markdown heading), clause option summaries (### Markdown heading) and the clause text (normal text). Example:

```markdown
## Topic Heading

These are the notes for the topic explanation.  This text is optional, but useful to explain the options.

### This clause option number 1 - usually a clause summary.

This is the clause text for clause option number 1.

### This clause option number 2  - usually a clause summary.

This is the clause text for clause option number 2.

```

## Variables Section

To create a variable in a markdown template, all you need to do is write words {{like this}} in the clause text (use two curly braces on either side).

When you open the document on the CodePact interface, you'll then have the ability to insert text.  Here's what it looks like.

```markdown
## Topic Heading

This is the clause text.  You will want to insert {{your name}} in the curly braces.
```

You can also add:

- default text; and
- guidance to variables,

like this - note that this information goes at the end of the document in a topic called "Variables".

```markdown
## Variables

#### your name

This is the default text in the variable when you open it

`Guidance` This is the guidance text that's displayed when you open the variable.
```
This is what that looks like:

![](http://guide.codepact.com/content/images/2015/09/cp_variables.png)

You don't need to add guidance - you can use default text only if you prefer.

You can also create multiline default text and guidance for variables.

```markdown
## Variables

#### your name

- this is the first list item;
- this is the second list item; and
- this is the last list item.

`Guidance` This is the guidance text that's displayed when you open the variable.

This is the second line of the guidance text that's displayed when you open the variable.
```

## Definitions Section

You need three things for definition functionality in a CodePact template:

- the use of capitalised terms in template clauses;
- the last topic (or second last if there's a variable topic) of the template called "Definitions" (## heading); and
- a list of the defined terms (### heading).

Here's what the end of a CodePact document often looks like.

```markdown
## Definitions

### Agreement
means the agreement arising between the parties in accordance with this document and the other documents referred to by this document.

### Background IP
means the Intellectual Property Rights owned by Developer prior to the creation of the Agreement.

### Contributed IP
means the Intellectual Property Rights owned by Client prior to the creation of the Agreement.

### Services IP
means the Intellectual Property Rights created under the Agreement by the Provider.

## Variables

#### your name

This is the default text in the variable when you open it

`Guidance` This is the guidance text that's displayed when you open the variable.
```

## Header Section

The title section is the most prescriptive part of the Template because it sets up parameters for the rest of the Template.

Here's an example:

```Markdown
# Example Agreement Title

`Purpose` Agreement governs a software developer working for a client in a fixed fee or hourly context.

`Party 1 Name` Developer

`Party 2 Name` Client
```

A valid Template requires the following elements:

<table>
<tbody>
<tr>
<td><strong>One Hash (#) Heading</strong></td>
<td>The name of the agreement</td>
</tr>
<tr>
<td><strong>Inline Code Ticks</strong> around the words "Purpose"</td>
<td>Purpose description of the agreements created from the template</td>
</tr>
<tr>
<td><strong>Inline Code Back-ticks</strong> around the words "Party 1 Name"</td>
<td>The defined short name of the first party - used throughout the rest of the document</td>
</tr>
<tr>
<td><strong>Inline Code Back-ticks</strong> around the words "Party 2 Name"</td>
<td>The defined short name of the second party - used throughout the rest of the document</td>
</tr>
</tbody>
</table>

There's a screen shot below of how CodePact's interface displays the information.

![](http://guide.codepact.com/content/images/2015/09/cp_title.png)
