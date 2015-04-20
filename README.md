# gitbook-plugin-include-highlight

Highlight code in referenced source files.

This is heavy based on [gitbook-plugin-include](https://github.com/rlmv/gitbook-plugin-include)

Add !CODEFILE  to your Markdown file with file path to your file that contains code.
This will pre-process file contents and wrap them in in highlight code block. 

Syntax will be picked up by file extension.
example usage:

```
!CODEFILE "../../src/notSoAwsomeApp/file.ts"
```
gets file and displays code bloc highlight depending on file extension (TypeScript in this case).

Please note that file extension should match one of [highlightjs css class](http://highlightjs.readthedocs.org/en/latest/css-classes-reference.html)

## Install 

Add to your `book.json` plugin list:
```
{
    "plugins" : [ "include-highlight" ],
}
```


##TODO
Add convenient way to map file extensions that don't match syntax used in contents.

Currently only Gherkin feature files used for example in Cucumber
```
almostGreat.feature
```
are mapped to use gherkin as highlight.
