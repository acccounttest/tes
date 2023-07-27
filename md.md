TheBrain Markdown Reference
Markdown starts with plain text and allows document formatting with easy-to-type markup. The formatting tags are hidden when you are not editing your document. In addition to the ability to type formatting tags, most tags can be inserted and removed using the toolbar at the top of the notes editor.

Markdown Visibility
TheBrain 13 introduces the ability to toggle Markdown tag visibility even while actively editing notes.

When Markdown is hidden, only the tags for commonly-used formatting options in the below list can be typed:

Headings
Unordered lists
Ordered lists
Checkboxes (checked and unchecked)
Horizontal rules
Blockquotes
Math expressions
Standard Markdown
TheBrain supports the following subset of Markdown:

 	Plain text	Explanation/Result
	
A paragraph
 
Another paragraph.
Paragraphs are simply a single run-on line of text with no breaks, followed by two line breaks between other paragraphs.
	
# Title
Title
Different levels of headings can be achieved with by varying the number of # characters at the start of a line from 1 to 6.

	
## Subtitle
Subtitle
Slightly smaller than a Title.

	
### Heading
Heading
Slightly smaller than a Subtitle.

	
#### Sub-heading
Subheading
Smaller than a Heading.

	
> A blockquote
Start a line with > to get
A blockquote
	
*Italic* emphasis
Italic emphasis
	
**Bold** emphasis
Bold emphasis
	
Inline `code` style
Inline code style (monospaced formatting)
	
* A bullet list
* Unordered items
A bullet list
Unordered items
	
1. Numbered list
2. Ordered items
Numbered list
Ordered items
 	
[a link](https://en.
wikipedia.org/wiki/URL)
This is a link to a Wikipedia page.

Links to thoughts (Local Thought URLs) are done in the same manner, with a brain: link: [A thought](brain://...)
	
![alt text](https://en.
wikipedia.org/wiki/Image
"Embedded image")


In the desktop and mobile clients, add images using copy-and-paste or drag-and-drop. Images can be resized from full width (100%) down to 5%. An image at 50% width is indicated by appending #$width=50p$ to the image address.
	
Horizontal rule

---

Between paragraphs
Horizontal rule

Between paragraphs

\* Escaped text
* Escaped text

Use \ to escape single characters that would otherwise be interpretted as markdown formatting commands. In this example, the line would be a bulleted list if the backslash were not present.

 

Minor Changes to Markdown
Except for <br>, TheBrain ignores HTML tags and just treats them as plain text. TheBrain changes the meaning of the following Markdown characters:

 	
First line
Another line
First line
Another line

Newline characters (when you press Enter/Return) are always respected whereas traditional Markdown would ignore single line breaks unless the line ended with space.
	
+ Done (checked)
- To do (unchecked)
* Normal bullet item
  Done (checked)
  To do (unchecked)
Normal bullet item
 

TheBrain Extensions to Markdown
TheBrain extends Markdown to add support for the following formatting:

	
:-- Left justified
Left justified

Line justification is specifed by adding :-- :-: or --: at the start of the line.
	
:-: Centered
Centered
	
--: Right justified
Right justified
	
```
Code block
across multiple lines.
```
Code block
across multiple lines.

Code blocks are monospaced and ignore markdown formatting within them.
	
_{Underlined}_ text
Underlined text
	
The game is -{almost}- over
The game is almost over.

Add strikethrough to a word or phrase with a single hyphen on either side.
	
10^2 = 100
102 = 100

Superscript is supported using ^ as a delimiter. These tags are slighty different in that they can be applied just at the start of the text to be affected and end automatically at punctuation or a space. To extend beyond punctuation, add a second ^ at the end also.
	
H~2~O is water
H2O is water.

Subscript is supported using ~ as a delimiter in a similar manner as superscript.
 	
:{Red on yellow:(style=
"background-color:#ffff00;
color:#aa0000"):}:
Red on yellow

Attributes for text foreground and background colors are applied by prefixing the style attribute with :( and ending it with :). The span indicating the text to which the attribute should apply is specified by surrounding it with :{ and }:. If an attribute is placed outside of a span, it will be applied to the entire line of text.
	
:{Text in a special font
:(style="font-family:
Lobster;font-size:150%"):}:
Text in a special font

Attributes for font-family and font-size are also supported by TheBrain. Note that there is no UI for specifying font-size at this time.
	
$$\frac{n!}{k!(n-k)!} = \binom{n}{k}$$


Enclose a LaTeX expression within $$ tags to render math directly in the notes editor.

Provides support for: Simple algebraic equations, Fractions and continued fractions, Exponents and subscripts, Trigonometric formulae, Square roots and n-th roots, Calculus symbols (limits, derivatives, integrals), Big operators (e.g. product, sum), Big delimiters (using \left and \right), Greek alphabet, and much more...
 

TheBrain Table Extensions to Markdown
Similar to tables in GitHub Flavored Markdown with several powerful additions.

|Planet|Namesake|
|Mercury|Roman god of speed|
|Venus|Roman god of love|
|Earth|Variation of "the ground" in many languages|
|Mars|Roman god of war|
Planet	Namesake
Mercury	Roman god of speed
Venus	Roman god of love
Earth	Variation of "the ground" in many languages
Mars	Roman god of war
Each line of a table must start and end with |
No dividing line after the header of |---|---| should be added
The first line is treated as a header row. To hide the header row, use an empty line of two | characters
Column widths are automatically determined based on the contents
|Item|Description|--: Price|
|Phone|Includes:{nl}* Holographic display{nl}* Telepathic UI|1,000.00|
|Case|Shock resistant hard shell|19.00|
Item	Description	Price
Phone	Includes:
Holographic display
Telepathic UI
1,000.00
Case	Shock resistant hard shell	19.00
Multi-line cells are supported using {nl} to denote new lines
Lines can utilize tags to include bullets, headings, etcetera
Justify a cell using appropriate justification prefix at the start of the cell
To justify a column, place the justification prefix in the header row
To justify the table itself, place the justification prefix at the start of the header row, before the first |
|Planet|Namesake|:(table="foreground-color:#fff8f8f2;background-color:#ff282c34;alt-background-color:#ff32363f;line-color:#ff454c5a;
first-row-foreground-color:#fff9264c;first-row-background-color:#ff212329;first-row-line-color:#ff373d48;
first-column-foreground-color:#ffa6e22e;first-column-background-color:#ff212329;first-column-line-color:#ff373d48;column-widths:-1,110"):
|Mercury|Roman god of speed|
|Venus|Roman god of love|
|Earth|Variation of "the ground" in many languages|
|Mars|Roman god of war|
Planet	Namesake
Mercury	Roman god of speed
Venus	Roman god of love
Earth	Variation of "the ground" in many languages
Mars	Roman god of war
Include a :(table=""): tag at the end of a table header line to allow custom styling
Insert attributes such as foreground-color:#ffffe050 between the quotes, separated by semicolons
Hex values for each attribute are in AARRGGBB format
Column widths can be assigned with the column-widths attribute
Column width values are in pixels and begin sequentially at the first column in the table. -1 represents a column that has no value assigned.
