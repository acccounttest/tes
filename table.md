
<table><tr><td>
<pre>
<h1>| **Hello** |</h1>
```language
| ^^^^^^^^^ |
| ^^^^^^^^^ |
| ^^^^^^^^^ |
```
</pre>
</td></tr></table>


<table><tr><td>
<pre>

<center><h1>| **Hello** |</h1></center>
```language
| ^^^^^^^^^ |
| ^^^^^^^^^ |
| ^^^^^^^^^ |

</pre>
</td></tr></table>

 1. fenced code block inside a list item
| ^ punctuation.definition.list_item
    ```language
|^^^^^^^^^^^^^^^ meta.paragraph.list
|   ^^^ punctuation.definition.raw.code-fence.begin
|      ^^^^^^^^ constant.other.language-name
|   ^^^^^^^^^^^ meta.code-fence
    
|^^^^ meta.paragraph.list markup.raw.code-fence
    ```
|   ^^^ punctuation.definition.raw.code-fence.end
    test
|   ^^^^^ meta.paragraph.list - markup.raw.code-fence
