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

## Configuration
You can map file extensions that don't match syntax used in contents by adding a mapping in your `book.json` plugins config section:
```
"pluginsConfig": {
  "include-highlight": {
    "extensionToLanguage": {
      "ps1": "powershell"
    }
  }
}
```

The plugin is pre-configured with the following mappings:
```
{
	'feature': 'gherkin',
	'pde': 'processing',
	'ps1': 'powershell'
}
```
