
<table><tr><td>
<pre>

```language
| **Hello** |
| ^^^^^^^^^ |
| ^^^^^^^^^ |
| ^^^^^^^^^ |
```
</pre>
</td></tr></table>


<table><tr><td>
<pre>

<pre>| **Hello** |</pre>
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
