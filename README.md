# launch-code-editor

Open file with line numbers in editor from Node.js.

This package is forked from [launch-editor](https://github.com/yyx990803/launch-editor)

support launching specified editor in process.

## Why

Changed too much and deviated from the original design of `launch-editor`. So created this package to work out cases when you need to launch specified editor in process

## Usage

``` js
const launch = require('launch-editor')

launch(
  // filename:line:column
  // both line and column are optional
  'foo.js:12:34',
  // try specific editor bin first (optional)
  'code',
  // callback if failed to launch (optional)
  (fileName, errorMsg) => {
    // log error if any
  }
)
```

### Supported editors

| Value | Editor | Linux | Windows | OSX |
|--------|------|:------:|:------:|:------:|
| `atom` | [Atom](https://atom.io/) |✓|✓|✓|
| `code` | [Visual Studio Code](https://code.visualstudio.com/) |✓|✓|✓|
| `code-insiders` | [Visual Studio Code Insiders](https://code.visualstudio.com/insiders/) |✓|✓|✓|
| `sublime` | [Sublime Text](https://www.sublimetext.com/) |✓|✓|✓|
| `webstorm` | [WebStorm](https://www.jetbrains.com/webstorm/) |✓|✓|✓|
