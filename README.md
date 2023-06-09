<p align="center"><img src="https://sdasddas.oss-cn-hangzhou.aliyuncs.com/keyan/202304082356547.png" /></p>

<h1 align='center'>UnifieReadme</h1>

<p align="center">
<a href=""><img src="https://img.shields.io/badge/version-0.1-yellow.svg" /></a>
<a href=""><img src="https://img.shields.io/badge/auther-Jinghao Hu-orange.svg" /></a>
<a href="https://www.python.org/downloads/"><img src="https://img.shields.io/badge/markdown-1.0%7C2.0%7C3.0%7C4.0-blue.svg" /></a>
<a href="http://opensource.org/licenses/MIT"><img src="https://img.shields.io/badge/license-MIT-green.svg" /></a>
</p>


> UnifieReadme : Create a uniform README template for all projects to ensure consistency and clarity of the code base.

<!-- ![](https://sdasddas.oss-cn-hangzhou.aliyuncs.com/keyan/202304091349962.png) -->
![](https://sdasddas.oss-cn-hangzhou.aliyuncs.com/keyan/202304082359019.png)

English | [中文](https://github.com/hujinghaoabcd/UnifieReadme/blob/main/README_CN.md)

---
## Table of Contents

<!-- - [Security](#security) -->
- [Background](#background)
- [Features](#Features)
- [Install](#install)
- [Usage](#usage)
    - [Generator](#generator)
- [API](#api)
- [Documentation](#Documentation)
- [Authors](#Authors)
- [Contributing](#contributing)
- [License](#license)

<!-- ## Security

... -->
---
## Background

The README file should tell people why the package or software is being used, how to install it, and how to use it. Unifying README files can make it easier to create and maintain README files.

---
## Features

 - **Harmonization :** Ensure consistency and clarity of the code base.

 - **Customizable :** Users can modify and customize it according to their needs.
---

## Install

This project uses [node](http://nodejs.org) and [npm](https://npmjs.com). Go check them out if you don't have them locally installed.

```sh
$ npm install --global unifile-readme-spec
```
---
## Usage

Please note that unifilereadme package only provides the function of converting txt files to markdown format, if your txt file does not meet the syntax requirements of markdown format, the converted result may have unexpected errors.

```javascript
const fs = require('fs');
const unifilereadme = require('unifilereadme');

const txtFile = fs.readFileSync('file.txt', 'utf-8');
const markdown = unifilereadme(txtFile);

fs.writeFileSync('file.md', markdown);
```
---
### Generator

You can also use the command line tool to generate a README.md file:

```sh
$ unifilereadme --help

  Usage
    $ unifilereadme <input> <output>

  Options
    --help, -h  Show help options
    --version, -v  Show version number

  Examples
    $ unifilereadme input.txt output.md
```

Where input.txt is the path of the txt file to be converted and output.md is the path of the generated markdown file. You can replace these two parameters according to the actual situation. The generated markdown file will be saved in the output.md file.

---
## API

- I/O Functions

| Function                                          | Description                                   | Finish |
| :------------------------------------------------ | :-------------------------------------------- | :----- |
| create_grid                                       | 🌐 Creates a grid from  geotiff.               | ✅      |
| read_raster                                       | 🌏 Reads raster data from geotiff.             | ✅      |
| to_raster &nbsp; &nbsp; &nbsp; &nbsp;&nbsp;&nbsp; | 🗺️ Write grids to raster files (e.g. geotiff). | ✅      |

- FLOW Functions

| Function        | Description                              | Finish |
| :-------------- | :--------------------------------------- | :----- |
| water_supply    | ⤴️ Calculate water service supply.        | ❌      |
| water_demand    | ⤵️ Calculate water service demand.        | ❌      |
| water_direction | 🏳️ Calculate the water service direction. | ❌      |


- Accumulate Functions


| Function       | Description                             | Finish |
| :------------- | :-------------------------------------- | :----- |
| raster_flow    | 🚀 Calculate raster-scale water flow.    | ❌      |
| watershed_flow | ⭐ Calculate watershed scale water flow. | ❌      |

- View Functions:


| Function                                          | Description                                                  | Finish |
| :------------------------------------------------ | :----------------------------------------------------------- | :----- |
| view_plot &nbsp; &nbsp; &nbsp; &nbsp;&nbsp;&nbsp; | 📊 Draw a water service view.   &nbsp; &nbsp; &nbsp; &nbsp;&nbsp;&nbsp;&nbsp; &nbsp; &nbsp; &nbsp;&nbsp;&nbsp; | ❌      |

---

## Documentation
 - [configuration]()
 - [design]()
 - [build](docs/build.md) 
 - [statistics]()
---
## Authors

[@JinghaoHu](https://github.com/hujinghaoabcd).
---
## Contributing

Thanks to the following people who participated in the project:

<a href="graphs/contributors"><img src="https://opencollective.com/standard-readme/contributors.svg?width=800&button=false" /></a>

---

## Welcome to join !

Found a mistake? There is something meaningless? Send me a [pull request](https://github.com/hujinghaoabcd/UnifieReadme/pulls) !

---

## License

[MIT © JinghaoHu.](../LICENSE)