# CodePact Templates in Markdown

CodePact templates create legal agreements on a web interface that you can sign electronically.

It's simple to create CodePact Templates (**Templates**) with **options, variables and guidance** using [Markdown documents](https://guides.github.com/features/mastering-markdown/).

Markdown is a simple programming language that is widely used to create documents. It is simple to read, and even simpler to write - as long as you keep in mind some key concepts:
- line breaks matter. We use them to separate paragraphs and titles. Or two paragraphs.
- Sometimes spaces are important - or you might have a space where you shouldn't
- uppercase / lowercase can also matter - for example when defining headings or some variables. We've put a :interrobang: symbol to show a potential gotcha.
- for formatting, keep [this guide] (https://help.github.com/articles/basic-writing-and-formatting-syntax/) handy. More [advanced formatting here](https://help.github.com/articles/organizing-information-with-tables/).

If you try to load your template into CodePact and get an error, it is usually something relating to a Markdown issue. Go through your template and check linespaces and case.

It'll only take you 10 seconds to make your first CodePact template from Markdown:

1.  Login to http://codepact.com and go to https://codepact.com/newEnter (or click "Create Template" on the dash).

2.  On the left panel, click "Add Example Markdown Agreement" (or copy and paste the markdown from a template [here](http://github.com/codepact)).

4.  Click "Save New Draft" to see the template preview then click "Finalize".  Now you can use the template to create an agreement.

Another option is to store your templates on [Github](http://github.com), with either a free or paid account. There are some complete templates [here](http://github.com/codepact) - they're **open source**, so feel free to fork and submit pull requests!

To add your template stored on GitHub, in CodePact go to Templates > Create > Add Github Agreement. You can now create new agreements with your template. If you need to make changes, make the update on GitHub, and [create a release](https://help.github.com/articles/creating-releases/) :interrobang: You'll notice a pink cog appear next to your template, which you can click to apply these updates when you're ready.

## Template Basics

Every legal agreement covers a list of topics (usually there's an index).  Each topic heading is followed by a clause.  Topic headings can't be longer than 50 characters. 
:interrobang: Make sure you have a space between the ## and your topic title. Each word needs to have first letter uppercase, and there needs to be a line break between your heading and the text following.

In a CodePact template, there are two options:

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

To create variables in your template, all you need to do is write words {{like this}} in the clause text (use two curly braces on either side). When you create your agreement in CodePact, you'll be asked to define that variable.


```markdown
## Topic Heading

This is the clause text.  You will want to insert {{your name}} in the curly braces.
```

You can also add:

- default text; and
- guidance to variables,

like this - note that this information goes at the end of the document in a topic called "Variables". Don't worry - this won't appear in your final agreement as a topic called "variables". :interrobang: But it is important that you use the name "Variables" otherwise it won't get picked up.

```markdown
## Variables

#### your name

This is the default text in the variable when you open it

`Guidance` This is the guidance text that's displayed when you open the variable.
```

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

Definitions are a useful feature - you can add words to your agreement document (either as part of the template or in the text you add). Then in this special Definitions area you can explain what they mean. As long as you stick to the rules (first letter caps, and use the same spelling) then CodePact will automatically create definition links to this Definition section.

You need three things for definition functionality in a CodePact template:

1. the use of first letter capitalised terms in your template clauses;
2. the last topic (or second last if there's a variable topic) of the template called "Definitions" (## heading); and
3. a list of the defined terms (### heading).

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
