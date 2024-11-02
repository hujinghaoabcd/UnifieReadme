<p align="center"><img src="Material/readme.svg"  width='20%'/></p>

<h1 align='center'>UnifieReadme</h1>

<p align="center">
<a href=""><img src="https://img.shields.io/badge/version-0.1-yellow.svg" /></a>
<a href=""><img src="https://img.shields.io/badge/author-Jinghao%20Hu-orange.svg" /></a>
<a href="https://www.python.org/downloads/"><img src="https://img.shields.io/badge/markdown-1.0%7C2.0%7C3.0%7C4.0-blue.svg" /></a>
<a href="http://opensource.org/licenses/MIT"><img src="https://img.shields.io/badge/license-MIT-green.svg" /></a>
</p>

> **UnifieReadme**: 一个用于生成统一 README 模板的工具，确保项目文档的清晰与一致性。

[English](README.md) | [中文](README_CN.md)

---

## 目录

- [背景](#背景)
- [功能](#功能)
- [安装](#安装)
- [使用方法](#使用方法)
  - [命令行使用](#命令行使用)
- [API](#api)
  - [I/O 功能](#io-功能)
  - [格式化功能](#格式化功能)
- [文档](#文档)
- [作者](#作者)
- [贡献](#贡献)
- [许可证](#许可证)

---

## 背景

在协作项目中，创建和维护一致的 README 文件至关重要。**UnifieReadme** 提供了一个标准的 README 模板和自动文本到 markdown 的转换功能，确保所有项目文档的统一性和易读性。

---

## 功能

- **标准化模板**：为各项目提供一致的 README 文件结构。
- **Markdown 转换**：将纯文本转换为 markdown 格式。
- **可自定义**：轻松修改模板以适应特定项目需求。

---

## 安装

本项目需要 [Node.js](http://nodejs.org) 和 [npm](https://npmjs.com)。请确保这些已安装。

```sh
$ npm install --global unifie-readme
```

---

## 使用方法

UnifieReadme 提供了将纯文本转换为 markdown 格式并生成标准化 README 模板的工具。确保您的文本文件遵循 markdown 语法，以避免转换错误。

```javascript
const fs = require('fs');
const unifieReadme = require('unifie-readme');

const txtFile = fs.readFileSync('file.txt', 'utf-8');
const markdown = unifieReadme.convertToMarkdown(txtFile);

fs.writeFileSync('file.md', markdown);
```

---

### 命令行使用

直接使用命令行生成 `README.md` 文件：

```sh
$ unifie-readme --help

  使用方法：
    $ unifie-readme <输入文件> <输出文件>

  选项：
    --help, -h     显示帮助选项
    --version, -v  显示版本号

  示例：
    $ unifie-readme input.txt output.md
```

将 `input.txt` 和 `output.md` 替换为实际的源文件和输出文件路径。生成的 markdown 文件将保存到 `output.md`。

---

## API

### I/O 功能

| 功能                 | 描述                                                             | 状态 |
| -------------------- | ---------------------------------------------------------------- | ---- |
| `convertToMarkdown`  | 📄 将文本文件转换为 markdown 格式，确保一致性。                    | ✅   |
| `loadTemplate`       | 📥 加载预定义的 README 模板以供自定义。                           | ✅   |
| `exportMarkdown`     | 💾 将生成的 markdown 文件保存到指定位置。                          | ✅   |

### 格式化功能

| 功能                  | 描述                                                              | 状态 |
| --------------------- | ----------------------------------------------------------------- | ---- |
| `validateMarkdown`    | ✔️ 验证 markdown 语法和结构，确保格式标准。                       | ✅   |
| `addSection`          | ➕ 在 markdown 模板中添加新的部分。                               | ✅   |
| `removeSection`       | ➖ 从模板中删除指定部分。                                         | ✅   |

---

## 文档

- [配置文档]()
- [设计文档]()
- [构建指南](docs/build.md)
- [统计文档]()

---

## 作者

由 [Jinghao Hu](https://github.com/hujinghaoabcd) 维护。

---

## 贡献

感谢以下参与项目的贡献者：

<a href="graphs/contributors"><img src="https://opencollective.com/standard-readme/contributors.svg?width=800&button=false" /></a>

---

## 加入我们！

发现问题或有建议？提交 [pull request](https://github.com/hujinghaoabcd/UnifieReadme/pulls) 来改进 UnifieReadme 吧！

---

## 许可证

根据 [MIT License © 2024 Jinghao Hu | UCAS](LICENSE) 分发。详情请查阅 `LICENSE`。

