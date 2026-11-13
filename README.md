# Technical Writing – Course Documentation

A structured record of concepts, tools, commands and practical work covered in the Technical Writing course.

**Table of Contents**
 1. Latex
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


Google Docs is a free, web-based word-processing application developed by Google. It allows users to create, edit, format and share documents online. It also supports real-time collaboration, making it useful for academic and professional work.

**Key Features:**

* Document Creation and Editing:- Create new documents, edit existing files and organise content using different formatting options.
* Text Formatting:- Change font styles, sizes, colours, alignment, line spacing and paragraph formatting.
* Headings and Styles:- Use predefined heading styles to organise documents and create a clear document structure.
* Tables, Images and Charts:- Insert tables, images, drawings, charts and hyperlinks to improve document presentation.
* Lists and Page Formatting:- Create numbered lists, bullet points, page breaks, headers, footers and page numbers.
* Real-Time Collaboration:- Multiple users can work on the same document simultaneously and see changes instantly.
* Comments and Suggestions:- Add comments, suggest modifications and review edits without directly changing the original content.
* Sharing and Permissions:- Share documents through links and assign Viewer, Commenter or Editor access.
* Version History:- View previous versions of a document, track changes and restore earlier versions when required.
* Cloud Storage and Accessibility:- Documents are automatically saved to Google Drive and can be accessed from different devices.

**Important Tools and Options:**


| Tool | Purpose |
|---|---|
| Font and Font Size | Changes the appearance and size of text. |
| Bold, Italic and Underline | Highlights or emphasizes important text. |
| Text Alignment | Aligns text to the left, right, center or justifies it. |
| Insert Table | Organizes information into rows and columns. |
| Insert Image | Adds pictures to a document. |
| Word Count | Displays the total number of words in a document. |
| Page Numbers | Adds page numbers to the document. |
| Find and Replace | Searches for text and replaces it with other text. |
| Table of Contents | Creates a list of document headings. |
| Version History | Shows previous versions of a document. |



**Collaboration and Sharing:**

Google Docs provides tools for working with other users.

* Viewer: Can only view the document.
* Commenter: Can view and add comments.
* Editor: Can make direct changes to the document.
* Comments allow users to provide feedback.
* Suggesting mode allows edits to be reviewed before acceptance.

**Practical Applications**:

* Preparing assignments, reports and project documentation.
* Creating notes and study materials.
* Writing collaborative research papers.
* Sharing documents with classmates and teachers.
* Maintaining and organising academic records.

**Advantages of Google Docs:**

* Free and easy to use.
* Automatic saving of changes.
* Supports real-time collaboration.
* Accessible from different devices.
* Allows easy sharing and document management.
* Reduces the need for manual file transfers.

**Learning Outcomes:**

* Create and format professional documents.
* Use headings, tables, images and hyperlinks.
* Collaborate with others in real time.
* Manage document sharing permissions.
* Track changes using comments and version history.
* Store and access documents through Google Drive.





## 5. Git – Version Control

Git is a distributed version control system used to track changes in files and manage projects.


### Git Commands and Their Functions

| Command | Purpose |
|---|---|
| `git --version` | Checks the installed Git version. |
| `git init` | Creates a new Git repository. |
| `git clone URL` | Copies an existing repository to your computer. |
| `git status` | Shows the current status of files. |
| `git add filename` | Adds a specific file to the staging area. |
| `git add .` | Adds all modified and new files to the staging area. |
| `git commit -m "message"` | Saves staged changes with a message. |
| `git log` | Displays the commit history. |
| `git diff` | Shows unstaged changes. |
| `git branch` | Lists available local branches. |
| `git branch branch-name` | Creates a new branch. |
| `git switch branch-name` | Switches to another branch. |
| `git merge branch-name` | Merges another branch into the current branch. |
| `git remote -v` | Displays remote repository URLs. |
| `git push` | Uploads local commits to a remote repository. |
| `git pull` | Downloads and integrates remote changes. |
| `git fetch` | Downloads remote updates without merging them. |
| `git restore filename` | Discards unstaged changes in a file. |
| `git revert commit-id` | Reverses an earlier commit by creating a new commit. |
| `git rm filename` | Removes a file and stages its deletion. |
| `git stash` | Temporarily saves uncommitted changes. |

### Basic Git Workflow

| Step | Command | Function |
|---|---|---|
| 1 | `git status` | Checks modified files. |
| 2 | `git add .` | Stages changes. |
| 3 | `git commit -m "message"` | Saves changes locally. |
| 4 | `git push` | Uploads changes to GitHub. |


**Commonly Used Git Commands for Undoing Changes**

* git restore filename – Discards unstaged changes in a file.
* git reset HEAD filename – Removes a file from the staging area while keeping its changes in the working directory.
* git revert commit-id – Reverses a previous commit by creating a new commit.

**Importance of Git Commands:**

* Help track changes made to source code.
* Allow developers to work on different branches.
* Make collaboration easier.
* Help recover from mistakes.
* Maintain a history of project development.


## 6. GitHub – Repository Management

GitHub is a web-based platform used to host and manage software projects. It uses Git for version control and allows developers to store code, track changes, collaborate with others, and share their work.

 ** Important Features of GitHub**

1. Repository:- A repository is a storage location for project files, source code, documentation, and other resources. It keeps all project-related files organized in one place.

2. README File:- A README file provides information about a project, including its purpose, features, installation instructions, and usage. It is usually written in Markdown.

3. Branches:- Branches allow developers to work on different features or changes without directly modifying the main branch.

4. Commits:- A commit records changes made to files in a repository. Each commit contains a message describing the changes.

5. Pull Requests:- Pull Requests allow developers to propose changes and request that they be reviewed before being merged into another branch.

6. Issues:- Issues are used to report bugs, suggest improvements, and track project-related tasks.

7. Forking:- Forking creates a personal copy of another user's repository. It allows developers to experiment with or modify a project independently.

8. GitHub Actions:- GitHub Actions is an automation feature used to perform tasks such as running tests, building applications, and deploying projects.

### 6.2 Common GitHub Operations

| Operation | Purpose |
|---|---|
| Create Repository | Creates a new project repository. |
| Upload Files | Adds files to a repository. |
| Edit Files | Modifies existing repository files. |
| Commit Changes | Saves changes with a descriptive message. |
| Create Branch | Creates a separate development branch. |
| Create Pull Request | Proposes changes for review. |
| Merge Pull Request | Combines approved changes into another branch. |

### 6.3 Basic GitHub Workflow

A typical workflow for managing a project on GitHub involves the following steps:

1. Create a new repository on GitHub.
2. Add project files such as source code and README.md.
3. Commit changes with meaningful messages.
4. Create branches when working on new features.
5. Push local changes to the remote repository.
6. Open a Pull Request to propose changes.
7. Review and merge approved changes.

### 6.4 Markdown in GitHub

GitHub supports Markdown, a lightweight markup language used to format documentation.

Some commonly used Markdown elements are:

- `# Heading` – Creates a main heading.
- `## Subheading` – Creates a second-level heading.
- `**Bold Text**` – Makes text bold.
- `*Italic Text*` – Makes text italic.
- `- Item` – Creates a bullet point.
- `[Link Text](URL)` – Adds a hyperlink.
- `![Alt Text](image-url)` – Adds an image.
- `` `code` `` – Displays inline code.

**Example:**

```markdown
# My Project

This is a sample project.

## Features
- Easy to use
- Open source
- Well documented

**Important:** This project uses GitHub.
```

### 6.5 Advantages of GitHub

- Provides online storage for project files.
- Makes collaboration easier among developers.
- Maintains a history of project changes.
- Helps manage bugs and development tasks.
- Allows developers to share projects publicly or privately.
- Supports automated testing and deployment.

### 6.6 Learning Outcomes

After learning GitHub, I understood how to:

- Create and manage repositories.
- Upload, edit, and organize project files.
- Write documentation using Markdown.
- Track changes through commits.
- Understand branches and pull requests.
- Collaborate with other developers.


## 7. Git Best Practices

Git best practices are guidelines that help developers manage code efficiently, maintain a clean project history, and collaborate with other developers. Following these practices makes version control more organized and reduces errors during software development.

### 7.1 Write Meaningful Commit Messages

Every commit should have a short and descriptive message explaining the changes made.

**Examples:**

```bash
git commit -m "Add login functionality"
git commit -m "Fix navigation menu bug"
git commit -m "Update project documentation"
```

Avoid unclear messages such as:
- `changes`
- `update`
- `final work`

### 7.2 Commit Changes Frequently

- Make small and meaningful commits instead of combining many unrelated changes.
- Commit after completing a specific task or feature.
- Frequent commits make it easier to identify and reverse mistakes.

### 7.3 Use Branches for New Features

Branches allow developers to work on new features without affecting the main branch.

**Example:**

```bash
git branch feature-login
git switch feature-login
```

After completing the feature, changes can be merged into the main branch.

### 7.4 Pull Before Pushing

Before uploading changes, retrieve the latest updates from the remote repository.

```bash
git pull
git push
```

This helps keep the local and remote repositories synchronized and reduces conflicts.

### 7.5 Do Not Commit Unnecessary Files

Avoid adding temporary files, generated files, passwords, API keys, and other sensitive information to a repository.

A `.gitignore` file can be used to specify files and folders that Git should ignore.

**Example:**

```text
node_modules/
*.log
.env
```

### 7.6 Review Changes Before Committing

Use the following commands to check your changes:

- `git status` – Checks which files have been modified.
- `git diff` – Shows the changes made to files.
- `git diff --staged` – Shows changes added to the staging area.

Reviewing changes helps prevent accidental commits.

### 7.7 Avoid Working Directly on the Main Branch

- Use separate branches for new features and bug fixes.
- Test changes before merging them.
- Keep the main branch stable and reliable.

### 7.8 Keep the Repository Organized

- Use meaningful file and folder names.
- Maintain an updated README.md file.
- Remove unnecessary files.
- Organize source code and documentation properly.

### 7.9 Handle Merge Conflicts Carefully

A merge conflict occurs when Git cannot automatically combine changes made to the same part of a file.

To resolve conflicts:

1. Open the file containing the conflict.
2. Identify the conflicting changes.
3. Edit the file and keep the correct content.
4. Stage the resolved file.
5. Commit the resolution if required.

### 7.10 Back Up and Protect Your Work

- Push important commits to a remote repository regularly.
- Never share passwords, access tokens, or private keys.
- Use private repositories when project content should not be publicly accessible.
- Review repository permissions before adding collaborators.

### Conclusion

Following Git best practices helps maintain clean project history, prevent accidental data loss, improve collaboration, and make software development more efficient.



## 8. Learning Outcomes

Through this Technical Writing course, I gained practical knowledge of various tools and technologies used for technical documentation, presentations, code documentation, and version control.

**LaTeX**

- Learned to create structured technical documents using LaTeX.
- Understood document formatting, mathematical equations, tables, and figures.
- Learned to organize documents using sections, subsections, and references.
- Gained experience in preparing professional academic documents.

**Beamer – Presentations**

- Learned to create presentations using LaTeX Beamer.
- Understood how to organize content into slides and frames.
- Explored themes, colors, and formatting options.
- Learned to create structured academic presentations.

**Doxygen – Code Documentation**

- Understood the importance of documenting source code.
- Learned to write documentation comments in C++ and Python.
- Explored how Doxygen generates documentation from source code.
- Understood how documentation improves code readability and maintenance.

**Google Docs**

- Learned to create and format online documents.
- Understood the use of headings, tables, images, and page formatting.
- Explored real-time collaboration, comments, and sharing permissions.
- Learned to manage document versions and work with others.

 **Git – Version Control**

- Understood the fundamentals of version control.
- Learned to initialize repositories and track file changes.
- Practiced staging, committing, branching, and merging.
- Understood how Git helps maintain project history and manage code changes.

**GitHub – Repository Management**

- Learned to create and manage GitHub repositories.
- Understood how to upload, edit, and organize project files.
- Practiced writing project documentation using Markdown.
- Explored commits, branches, pull requests, and collaboration features.

**Overall Learning**

This course helped me understand the importance of technical writing in software development and academic work. I gained practical experience with tools used to prepare documentation, create presentations, document code, collaborate on projects, and manage software versions.

These skills will help me communicate technical information more effectively and maintain well-organized project documentation.


