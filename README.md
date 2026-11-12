# Technical Writing – Course Documentation

A structured record of concepts, tools, commands and practical work covered in the Technical Writing course.

**Table of Contents**
 1. Latex
- 1.1 Introduction to LaTeX
- 1.2 Mathematical Typesetting
- 1.3 Tables, Colours and Figures
- 1.4 LaTeX Picture Environment
- 1.5 Document Formatting and Advanced Features
 2. Beamer – Presentations
 3. Doxygen – Code Documentation
 4. Google Docs
 5. Git – Version Control
 6. GitHub – Repository Management
 7. Git Best Practices
 8. Learning Outcomes
## 1. Latex 
### 1.1 Introduction to LaTeX

LaTeX is a document preparation system used to create professional reports, research papers and technical documents.

Key Concepts:

* Document classes and structure
* Sections and subsections
* Environments and formatting
* Text alignment, lists and font sizes
* LaTeX editors: Overleaf and TeXstudio

### 1.2 Mathematical Typesetting

LaTeX provides commands for writing mathematical expressions and equations.

**Important Commands:**

Command	Purpose
* `\frac{a}{b}`	- Used for Fractions
* `\sqrt{x}` -	Used for Square roots
* `\sum`	- Used for Summation
* `\int`	- Used for Integration
* `\begin{matrix}` - Used for	Matrices
* `^ and _`	- Used forSuperscripts and subscripts
* `\begin{align}`	- Used for Aligned equations

### 1.3 Tables, Colours and Figures

LaTeX supports visual elements to improve document presentation.

* tabular – Create tables.
* xcolor – Add colours.
* graphicx – Insert external images.
* figure – Create figure environments.
* \caption{} – Add captions.
* \label{} and \ref{} – Cross-reference figures and tables.
* subcaption – Create subfigures.

### 1.4 LaTeX Picture Environment

The Picture Environment is used to create simple diagrams and illustrations directly in LaTeX.

**Important Commands:**

* ` \put()` – Position objects.
* `\line()` – Draw lines.
* `\vector()` – Draw arrows.
* `\circle{}` – Draw circles.
* `\framebox{}` – Create boxes.
* `\oval{}` – Create oval shapes.
* `\multiput()` – Repeat objects.

### 1.5 Document Formatting and Advanced Features

Advanced LaTeX features help create well-structured and professionally formatted documents.

* Page layout, margins and spacing.
* Font styles and background colours.
* Custom headings and section numbering.
* Boxes, lines and paragraph formatting.
* Indexing and bibliography using BibTeX.
* Cross-referencing and document organisation.

## 2. Beamer – Presentations

Beamer is a LaTeX document class used to create professional presentations. It allows users to prepare structured slides containing text, mathematical equations, images, tables and diagrams.

Key Features:

* Creates presentations using LaTeX commands.
* Supports themes, colours and custom layouts.
* Allows mathematical equations and scientific notation.
* Supports images, tables, lists and diagrams.
* Provides overlays and animations to reveal content step by step.
* Supports navigation symbols, hyperlinks and slide transitions.

**Basic Structure of a Beamer Presentation:**

A Beamer document generally consists of a document class, packages, title information and individual frames (slides).

```latex
\documentclass{beamer}
\usetheme{Madrid}
\title{My Presentation}
\author{Your Name}
\date{\today}
\begin{document}
\begin{frame}
    \titlepage
\end{frame}
\begin{frame}{Introduction}
    Welcome to my presentation.
\end{frame}
\end{document}
```
**Themes and Customisation:**

Beamer provides different themes to customise the appearance of presentations.

* Madrid – Structured and professional layout.
* Berlin – Navigation-oriented design.
* Warsaw – Includes navigation elements.
* CambridgeUS – Formal presentation style.
* Custom colours, fonts and backgrounds can also be applied.

Example:

\usetheme{Madrid}


 \usecolortheme{beaver}

**Frames and Slide Formatting:**

* `\begin{frame}` – Creates a new slide.
* `\frametitle{}` – Defines the slide title.
* `\framesubtitle{}` – Adds a subtitle.
* `\titlepage` – Displays presentation title information.
* `\section{}` – Organises slides into sections.

**Lists, Images and Tables:**

Beamer supports different types of content within slides.

* Itemised and numbered lists.
* Inserting images using the graphicx package.
* Creating tables using the tabular environment.
* Displaying mathematical equations.
* Including diagrams and charts.

**Overlays and Animations:**

Overlays allow presentation content to appear gradually instead of displaying everything at once.

Common commands:

* `\pause` – Reveals content step by step.
* `\only<>{}` – Displays content on selected slides.
* `\uncover<>{}` – Reveals content while reserving its space.
* `\alert{}` – Highlights important text.

**Compiling a Beamer Presentation:**

1. Write the presentation using LaTeX commands.
2. Select a suitable Beamer theme.
3. Add slides using the frame environment.
4. Insert required images, tables and equations.
5. Compile the document using Overleaf or a LaTeX editor.
6. Generate and review the final PDF presentation.

## 3. Doxygen – Code Documentation
Doxygen is an open-source documentation generator that extracts information from specially formatted comments in source code. It supports languages such as C, C++, Python and Java and generates documentation in formats such as HTML, LaTeX and PDF.

**Key Features:**

* Automatically generates documentation from source code.
* Documents functions, classes, variables and modules.
* Creates cross-references, call graphs and inheritance diagrams.
* Supports multiple output formats.
* Integrates with software development workflows.

**Installation:**

* Windows: Download and install Doxygen from its official website.
* macOS: brew install doxygen
* Linux: sudo apt-get install doxygen

Check the installed version:

`doxygen --version`


**Doxygen Comment Syntax:**


Doxygen uses specially formatted comments to document code.


C/C++ Example:

```cpp
/**
 * @brief Calculates the sum of two numbers.
 * @param a First number.
 * @param b Second number.
 * @return Sum of both numbers.
 */

 
int add(int a, int b);
```

Python Example:
```python
def add(a, b):
 """
    @brief Calculates the sum of two numbers.
    @param a First number.
    @param b Second number.
    @return Sum of both numbers.
    """
    return a + b
```

**Common Doxygen Commands:**

* @brief -	Short description
* @param -	Describes parameters
* @return -	Describes return values
* @author -	Specifies author
* @version -	Specifies version
* @see -	References related elements
* @note	- Adds additional information
* @warning -	Highlights warnings

**Documenting Classes and Functions:**

* Documents class names, member variables and methods.
* Describes function parameters and return values.
* Explains the purpose and behaviour of code.
* Documents relationships between classes.

**Configuration and Documentation Generation:**

Doxygen uses a configuration file called *Doxyfile*.

1. Generate the configuration file:

`doxygen -g Doxyfile`

2. Edit the configuration settings.
3. Specify source files and output directories.
4. Generate documentation:

`doxygen Doxyfile`

5. Open the generated HTML documentation at html/index.html.

**Advanced Features:**

* Class diagrams and inheritance diagrams.
* Function call graphs.
* Cross-referencing between code elements.
* Graphviz integration for visual diagrams.
* HTML and LaTeX/PDF output generation.
  
## 4. Google Docs

Google Docs is a web-based word-processing tool developed by Google. It allows users to create, edit, format and share documents online.

**Key Features:**

* **Document Creation and Formatting:** Create documents and format text using fonts, headings, colours and paragraph alignment.
* **Tables and Images:** Insert tables, images, charts and hyperlinks into documents.
* **Comments and Suggestions:** Add comments and suggest edits without directly changing the original content.
* **Real-Time Collaboration:** Multiple users can edit the same document simultaneously.
* **Sharing and Access Permissions:** Share documents with others and control viewing, commenting and editing permissions.
* **Version History:** View previous versions of a document and restore earlier changes when required.
* **Cloud Storage and Accessibility:** Automatically saves changes to Google Drive and allows access from different devices.



## 5. Git – Version Control

Git is a distributed version control system used to track changes in files and manage projects.

**Essential Git Commands:**
* git --version
* git init
* git status
* git add .
* git commit -m "Initial commit"
* git log
* git diff
* git branch
* git switch -c feature
* git merge feature
* git restore filename
* git revert commit_id
* git pull
* git fetch

Important Concepts:

* Working directory and staging area.
* Repository and commits.
* Branching and merging.
* Merge conflicts.
* Version history.

## 6. GitHub – Repository Management

GitHub is a web-based platform used to host Git repositories and collaborate on projects.

**Important Operations:**

* Creating repositories.
* Uploading and managing files.
* Cloning repositories.
* Pushing and pulling changes.
* Creating branches.
* Forking and pull requests.
* Resolving merge conflicts.
* Writing README documentation.

## 7. Git Best Practices

1. Use meaningful headings and file names.
2. Write clear and concise documentation.
3. Commit changes regularly.
4. Use descriptive commit messages.
5. Maintain organised repositories.
6. Review changes before merging.
7. Never upload passwords or API keys.

## 8. Learning Outcomes

Through this course, I gained practical knowledge of:

* Creating professional documents using LaTeX.
* Writing mathematical equations and designing tables in LaTeX.
* Inserting figures and creating diagrams in LaTeX.
* Preparing presentations using Beamer.
* Generating code documentation using Doxygen.
* Collaborating through Google Docs.
* Managing projects using Git and GitHub.
* Understanding version control and repository management.
