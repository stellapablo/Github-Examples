```
Markdown 
```

Is a markup language that offers a lean approach to content editing by shielding content creators from the overhead of HTML. While HTML is great for rendering content exactly how it was intended, it takes up a lot of space and can be unwieldy to work with, even in small doses. The invention of Markdown offered a great compromise between the power of HTML for content description and the ease of plain text for editing.

In this unit, we'll discuss the structure and syntax of Markdown. We'll also cover features of GitHub-Flavored Markdown (GFM), which are syntax extensions that allow you to integrate GitHub features into content.

# Emphasize text
The most important part of any communication on GitHub is usually the text itself, but how do you show that some parts of the text are more important than others?

Using italics in text is as easy as surrounding the target text with single asterisks (*) or single underscores (_). Just be sure to close an emphasis with the same character with which you opened it. Be observant how you combine the use of asterisks and underscores. Here are several examples:

Create bold text by using two asterisks (**) or two underscores (__).

## Declare headings
HTML provides content headings, such as the <h1> tag. In Markdown, this is supported via the # symbol. Just use one # for each heading level from 1-6.

# Link to images and sites
![Link an image.](/learn/azure-devops/shared/media/mara.png)
[Link to Microsoft Training](/training)

# Make lists
You can define ordered or unordered lists. You can also define nested items through indentation.

Ordered lists start with numbers.
Unordered lists can use asterisks or dashes (-).

# Build tables
You can construct tables using a combination of pipes (|) for column breaks and dashes (-) to designate the prior row as a header.

Copy
First|Second
-|-
1|2
3|4

# Quote text
You can create blockquotes using the greater than (>) character.

# Fill the gaps with inline HTML
If you come across an HTML scenario not supported by Markdown, you can use that HTML inline.

Here is a<br />line break

# Work with code
Markdown provides default behavior for working with inline code blocks delimited by the backtick (`) character. When decorating text with this character, it's rendered as code.

This is `code`.

If you have a code segment spanning multiple lines, you can use three backticks (```) before and after to create a fenced code block.

```markdown
var first = 1;
var second = 2;
var sum = first + second;
```

```javascript
var first = 1;
var second = 2;
var sum = first + second;
```

# Cross-link issues and pull requests
GFM supports various shortcode formats to make it easy to link to issues and pull requests. The easiest way to do this is to use the format #ID, such as #3602. GitHub automatically adjusts longer links to this format if you paste them in. There are also additional conventions you can follow, such as if you're working with other tools or want to specify other projects/branches.


# Mention users and teams
Typing an @ symbol followed by a GitHub username sends a notification to that person about the comment. This is called an "@mention", because you're mentioning the individual. You can also @mention teams within an organization.

# Track task lists
You can create task lists within issues or pull requests using the following syntax. These can be helpful to track progress when used in the body of an issue or pull request.

markdown

- [x] First task
- [x] Second task
- [ ] Third task

# Slash commands
Slash commands can save you time by reducing the typing required to create complex Markdown.
You can use slash commands in any description or comment field in issues, pull requests, or discussions where that slash command is supported.