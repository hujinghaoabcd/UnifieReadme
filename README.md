<p align="center"><img src="Material/readme.svg"  width='30%'/></p>

<h1 align='center'>UnifieReadme</h1>

<p align="center">
<a href=""><img src="https://img.shields.io/badge/version-0.1-yellow.svg" /></a>
<a href=""><img src="https://img.shields.io/badge/author-Jinghao%20Hu-orange.svg" /></a>
<a href="https://www.python.org/downloads/"><img src="https://img.shields.io/badge/markdown-1.0%7C2.0%7C3.0%7C4.0-blue.svg" /></a>
<a href="http://opensource.org/licenses/MIT"><img src="https://img.shields.io/badge/license-MIT-green.svg" /></a>
</p>

> **UnifieReadme**: A README generator that standardizes project documentation, ensuring clarity and consistency across your codebase.

[English](README.md) | [中文](README_CN.md)

---

## Table of Contents

- [Background](#background)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
  - [Command Line Usage](#command-line-usage)
- [API](#api)
  - [I/O Functions](#io-functions)
  - [Formatting Functions](#formatting-functions)
- [Documentation](#documentation)
- [Authors](#authors)
- [Contributing](#contributing)
- [License](#license)

---

## Background

Creating and maintaining consistent README files is essential for collaborative projects. **UnifieReadme** simplifies this process by offering a standardized README template and automated text-to-markdown conversion, ensuring all your project documentation stays uniform and easy to read.

---

## Features

- **Standardized Templates**: Provides a consistent structure for README files across projects.
- **Markdown Conversion**: Converts plain text to markdown format.
- **Customizable**: Easily modify templates to suit project-specific requirements.

---

## Installation

This project requires [Node.js](http://nodejs.org) and [npm](https://npmjs.com). Ensure these are installed before proceeding.

```sh
$ npm install --global unifie-readme
```

---

## Usage

UnifieReadme offers tools to convert plain text to markdown format and generate standardized README templates. Be sure your text files follow markdown syntax to avoid conversion errors.

```javascript
const fs = require('fs');
const unifieReadme = require('unifie-readme');

const txtFile = fs.readFileSync('file.txt', 'utf-8');
const markdown = unifieReadme.convertToMarkdown(txtFile);

fs.writeFileSync('file.md', markdown);
```

---

### Command Line Usage

Generate a `README.md` file directly using the command line:

```sh
$ unifie-readme --help

  Usage:
    $ unifie-readme <input> <output>

  Options:
    --help, -h     Show help options
    --version, -v  Show version number

  Examples:
    $ unifie-readme input.txt output.md
```

Replace `input.txt` and `output.md` with the actual paths for your source and output files. The markdown file will be saved to `output.md`.

---

## API

### I/O Functions

| Function          | Description                                                             | Status |
| ----------------- | ----------------------------------------------------------------------- | ------ |
| `convertToMarkdown` | 📄 Converts text files into markdown format, ensuring consistency.      | ✅      |
| `loadTemplate`    | 📥 Loads a predefined README template for customization.                | ✅      |
| `exportMarkdown`  | 💾 Saves the generated markdown file to the specified location.         | ✅      |

### Formatting Functions

| Function              | Description                                                       | Status |
| --------------------- | ----------------------------------------------------------------- | ------ |
| `validateMarkdown`    | ✔️ Validates markdown syntax and structure for standard formatting. | ✅      |
| `addSection`          | ➕ Adds a new section to the markdown template.                    | ✅      |
| `removeSection`       | ➖ Removes a specified section from the template.                  | ✅      |

---

## Documentation

- [Configuration]()
- [Design]()
- [Build Guide](docs/build.md)
- [Statistics]()

---

## Authors

Maintained by [Jinghao Hu](https://github.com/hujinghaoabcd).

---

## Contributing

Special thanks to those who contributed to this project:

<a href="graphs/contributors"><img src="https://opencollective.com/standard-readme/contributors.svg?width=800&button=false" /></a>

---

## Join Us!

Spotted an error or have suggestions? Submit a [pull request](https://github.com/hujinghaoabcd/UnifieReadme/pulls) to improve UnifieReadme.

---

## License

Distributed under the [MIT License © 2024 Jinghao Hu | UCAS](LICENSE). See `LICENSE` for more details.
