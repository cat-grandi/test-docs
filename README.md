# Documentation Structure

<p>
Effective and accessible documentation is crucial for any software project. It ensures that developers, users, and stakeholders can easily understand the project’s goals, features, and workflows. This guide provides a detailed approach to setting up documentation that is tightly integrated into the repository and designed to be directly usable by contributors and users.

In this guide, we cover:
- How to structure documentation for clarity and maintainability.
- Best practices for writing and organizing content.
- Tips for leveraging repository features like Markdown rendering.

By the end, you’ll have a framework for creating documentation that not only supports your project’s needs but also enhances collaboration and usability.
<br/>
</p>
<p>
<table>
<tbody>
<tr><td width="10000">
<details>
<summary>
<img src="../assets/icons/toc.svg" alt="Table of Contents">
</summary>
<p>

1. [Repo-Native Documentation](#repo-native-documentation)
   1. [What is Repo-Native Documentation?](#what-is-repo-native-documentation)
   2. [Advantages of Repo-Native Documentation](#advantages-of-repo-native-documentation)
   3. [Why Choose Repo-Native Documentation?](#why-choose-repo-native-documentation)
   4. [The Documentation Directory](#the-documentation-directory)
   5. [Markdown Files](#markdown-files)
   6. [The GitHub Folder](#the-github-folder)
   7. [Importance of the README File](#importance-of-the-readme-file)
   8. [Best Practices](#best-practices)
</p>
</td></tr>
</tbody>
</table>
</p>

## Repo-Native Documentation

### **What is Repo-Native Documentation?**

Repo-native documentation refers to documentation designed to be read, used, and maintained directly within a repository. Unlike external websites or wikis, this approach ensures that all project-related information is immediately accessible within the repository itself, making it a seamless part of the development and collaboration process.

**Key Characteristics:**
- **Optimized for Repository Viewing:** Written in formats like Markdown to render natively on platforms like GitHub or GitLab.
- **Integrated with Codebase:** Lives alongside the source code and evolves with it, ensuring consistency across versions.
- **Accessible to All Contributors:** Enables developers and users to navigate and contribute to the documentation without leaving the repository.

### **Advantages of Repo-Native Documentation**

1. **Ease of Access**  
   Documentation is immediately available to anyone browsing the repository, without the need for external tools or hosting.

2. **Version Control Integration**  
   Changes to the documentation are tracked alongside code updates, ensuring alignment between the documentation and the project itself. Contributors can review and suggest changes through the same pull request workflow used for code.

3. **Contributor-Friendly Workflow**  
   Because it resides in the repository, updating the documentation becomes as straightforward as updating the code, encouraging collaboration and minimizing barriers to contribution.

4. **Cost-Effectiveness**  
   Repo-native documentation takes advantage of free or built-in repository features like Markdown rendering, removing the need for paid hosting or external tools.

5. **Self-Containment**  
   By centralizing all project materials—code, documentation, and assets—in one location, repo-native documentation reduces confusion and makes the project easier to manage.

### **Why Choose Repo-Native Documentation?**

Repo-native documentation is especially suited for:
- **Open Source Projects:** Ensures contributors and users can access, understand, and contribute to documentation without additional setup.
- **Internal Tools and Libraries:** Facilitates collaboration among team members by integrating documentation into their existing workflows.
- **Projects Requiring Version-Specific Docs:** Makes it easy to maintain documentation for multiple versions by branching alongside the codebase.

By adopting a repo-native approach, you ensure that your documentation remains accessible, synchronized, and easy to maintain, ultimately enhancing the user and contributor experience.

> [!TIP]
> If you are working on an open-source project (a public repository), or have a paid GitHub account (GitHub Pro, Team, or Enterprise plan), your documentation can be hosted using GitHub Pages[^2] or the GitHub Wiki[^1] feature.
> 
> These options are more user-friendly and provide additional features like custom domains, themes, and search functionality.

[^1]: https://docs.github.com/en/communities/documenting-your-project-with-wikis/about-wikis
[^2]: https://docs.github.com/en/pages/getting-started-with-github-pages/about-github-pages

### The Documentation Directory<br/><sup>[docs/](/docs/)</sup>

The `docs/` directory is the heart of repo-native documentation. It is typically located at the root of the repository and contains most (if not all) of the documentation files and assets needed to organize and present the project's information.

**Purpose:**  
The `docs/` directory serves as a dedicated space to centralize documentation, ensuring it is easy to locate, maintain, and expand. Its contents are often structured to align with the broader goals of the repository, such as onboarding new users, providing API references, or offering usage instructions.

**Common Contents:**  
A well-organized `docs/` directory may include:
- **Markdown files:** Core documentation, such as `installation.md`, `usage.md`, and `api_reference.md`.
- **Assets:** Supporting resources, such as images, diagrams, or charts (`assets/`).
- **Configuration files:** Files for tools like `MkDocs`, `Sphinx`, or `ReadTheDocs`.

> [!NOTE] 
> While most projects include a `docs/` directory, its purpose varies. Some repositories use it for documentation intended for website rendering, while others ensure the files are directly readable within the repository. Repo-native documentation prioritizes the latter.

**Example Structure:**
```plaintext
docs/
├── index.md         # Landing page for documentation
├── getting_started.md # Initial setup and installation
├── usage.md         # Usage guidelines
├── api_reference.md # API documentation
├── assets/          # Images or diagrams
└── configuration/   # Config files for documentation tools (optional)
```

### Markdown Files

Markdown (`.md`) is the primary format used for repo-native documentation. It is a lightweight markup language designed for readability, simplicity, and compatibility with platforms like GitHub and `ReadTheDocs`.

**Why Markdown?**
- **Human-Readable:** The plain text format ensures that even the raw files are understandable.
- **Easy to Write:** Markdown syntax is straightforward, requiring no complex formatting tools.
- **Built-In Rendering:** Platforms like GitHub natively render Markdown files, making them accessible directly from the repository.

**Key Features:**
- **Flexibility:** Markdown supports headings, lists, tables, images, and links.
- **GitHub Enhancements:** GitHub extends Markdown with features like task lists, tables, and callouts. However, these may not render properly in other viewers.

> [!WARNING]
> This repository uses GitHub-flavored Markdown (GFM). If you plan to use external Markdown tools, ensure compatibility or avoid relying on GitHub-specific features.

**Markdown Resources:**
- [Markdown Guide](https://www.markdownguide.org/)
- [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/)
- [CommonMark Spec](https://spec.commonmark.org/0.29/)
- [Markdown Cheat Sheet | GeeksforGeeks](https://www.geeksforgeeks.org/markdown-cheat-sheet)

### The GitHub Folder<br/><sup>[.github/](/.github/)</sup>

The `.github` folder is a special directory for managing GitHub-specific features, such as workflows, templates, and community health files. While it may not be part of the core `docs/` directory, it often complements documentation efforts.

**Purpose:**  
The `.github` folder centralizes files related to GitHub functionalities, ensuring that project-specific configurations and guidelines are easy to locate.

**Common Files in `.github/`:**
| File/Folder         | Description                                                  |
|---------------------|--------------------------------------------------------------|
| `CODE_OF_CONDUCT.md`| Defines community engagement standards.                      |
| `CONTRIBUTING.md`   | Provides instructions for contributing to the project.       |
| `FUNDING.yml`       | Enables the "Sponsor" button on the repository page.         |
| `GOVERNANCE.md`     | Explains project governance policies.                        |
| `SECURITY.md`       | Details how to report security vulnerabilities.              |
| `SUPPORT.md`        | Outlines how to get help with the project.                   |
| `README.md`         | The repository’s main landing page.                          |
| `ISSUE_TEMPLATE/`   | Templates for creating GitHub issues.                        |
| `PULL_REQUEST_TEMPLATE.md` | Default template for pull requests.                  |
| `workflows/`        | YAML files defining GitHub Actions workflows.                |

**Special Files:**  
Certain files in `.github/` are recognized by GitHub and trigger specific behaviors:
- `CONTRIBUTING.md`: Linked when creating a new issue or pull request.
- `CODE_OF_CONDUCT.md`: Displayed in the repository’s community guidelines.
- `README.md`: Rendered as the main landing page if no file exists in the root.
- `LICENSE`: Displayed on the repository’s main page.

> [!NOTE]
> GitHub prioritizes specific files when displaying tabs on the repository's main page. Their order of preference is:  
> 1. Files in `.github/`  
> 2. Files in the repository root  
> 3. Files in the `docs/` folder  

### Importance of the README File

The `README.md` file is the first point of contact for anyone visiting the repository. It acts as the repository’s "homepage" and sets the tone for the project.

**Key Roles:**
- **Overview:** Briefly explain the project’s purpose, scope, and value.
- **Guidance:** Include links to key documentation (e.g., files in the `docs/` directory).
- **Call to Action:** Highlight how users can get started, contribute, or provide feedback.

**Best Practices for README:**
1. Start with a short, engaging description of the project.
2. Include a table of contents for larger README files.
3. Link to additional resources in the `docs/` directory.
4. Provide installation and usage instructions.
5. Include licensing and contribution information.

### Best Practices for the Documentation Directory

1. **Consistent Structure:** Use a predictable layout for ease of navigation.
2. **Separation of Concerns:** Keep assets (e.g., images, stylesheets) in a dedicated folder like `assets/`.
3. **Relative Links:** Use relative paths to link between files, ensuring compatibility across branches and forks.
4. **Clear Naming:** Use descriptive filenames, like `installation.md` instead of `doc1.md`.
5. **Update Regularly:** Synchronize documentation with the latest project changes.

## Structure

### Documentation Sections

Each section of the documentation serves a specific purpose and provides information on different aspects of the project. The following sections are commonly found in software project documentation:

1. **Index Page:** The home page of the documentation that provides an overview of the project, its purpose, and key features.
2. **Getting Started:** A guide for new users to quickly get up and running with the project.
3. **Usage and Reference:** Detailed instructions on how to use the project, including API documentation.
4. **Guides and Concepts:** Advanced knowledge for deeper understanding and integration of the project.
5. **Contribution Info:** Guidelines for contributors, including coding standards and how to contribute to the project.
6. **Extras:** Additional content such as tutorials, examples, FAQs, and the project's roadmap.
7. **License:** Information about the project's license, including terms and conditions for use and distribution.
8. **Optional Sections:** Additional directories for examples, tutorials, and assets can be included based on the project's needs.
9. **Assets:** A directory for images, diagrams, or other assets used in the documentation.
10. **Examples:** A directory containing example scripts or use cases to demonstrate the project.
11. **Tutorials:** A directory containing step-by-step tutorials for specific use cases.
12. **Changelog:** A record of major changes, features, and fixes in the project.


```bash
docs/
├── index.md              # Home page with an overview of the project.
├── getting-started.md    # Step-by-step guide for new users.
├── installation.md       # Detailed installation instructions.
├── usage/
│   ├── basics.md         # Overview of basic functionality and examples.
│   ├── advanced.md       # Advanced usage patterns and techniques.
│   └── cli.md            # Documentation for command-line tools (if applicable).
├── reference/
│   ├── api/
│   │   ├── module1.md    # API reference for Module 1.
│   │   ├── module2.md    # API reference for Module 2.
│   │   └── ...           # Additional modules or classes.
│   └── data-models.md    # Reference for data structures, schemas, or models.
├── guides/
│   ├── integration.md    # How to integrate with other tools/systems.
│   ├── customization.md  # Guidance on extending/customizing the project.
│   └── troubleshooting.md# Common issues and their solutions.
├── concepts/
│   ├── architecture.md   # Overview of the project's design and architecture.
│   ├── terminology.md    # Explanation of key terms used in the project.
│   └── workflows.md      # High-level workflows and use cases.
├── contributing.md       # Guide for contributors, including coding standards.
├── changelog.md          # Record of major changes, features, and fixes.
├── roadmap.md            # Planned features or future development goals.
├── faq.md                # Frequently Asked Questions.
└── license.md            # Project's license information.

# Optional Directories
├── examples/             # Directory containing example scripts and use cases.
│   ├── example1.md
│   └── example2.md
├── tutorials/            # Step-by-step tutorials for specific use cases.
│   ├── tutorial1.md
│   └── tutorial2.md
└── assets/               # Images, diagrams, or other assets for documentation.
```

## Sections

### Index Page

The index page serves as the home page for the documentation and should provide a high-level overview of the project. It should include the following:

| Section       | Description                                                  |
|---------------|--------------------------------------------------------------|
| Introduction  | Brief introduction to the project, its purpose, and features. |
| Key Features  | A list of the main features or capabilities of the project.  |
| Table of Contents | A list of links to the main sections of the documentation.  |

### Getting Started

The getting started guide is aimed at new users who want to quickly get up and running with the project. It should include the following:

| Section       | Description                                                  |
|---------------|--------------------------------------------------------------|
| Installation  | Step-by-step instructions for installing the project.       |
| Quick Start   | A simple example or tutorial to help users get started.     |
| Configuration | Information on how to configure the project for specific use cases. |

### Usage and Reference

The usage and reference section provides detailed instructions on how to use the project and includes API documentation. It should include the following:

| Section       | Description                                                  |
|---------------|--------------------------------------------------------------|
| Basics        | An overview of basic functionality and examples.            |
| Advanced      | Advanced usage patterns and techniques.                     |
| Command Line  | Documentation for command-line tools (if applicable).       |
| API Reference | Detailed documentation for the project's API.               |
| Data Models   | Reference for data structures, schemas, or models.          |

### Guides and Concepts

The guides and concepts section provides advanced knowledge for deeper understanding and integration of the project. It should include the following:

| Section       | Description                                                  |
|---------------|--------------------------------------------------------------|
| Integration   | How to integrate the project with other tools or systems.   |
| Customization | Guidance on extending or customizing the project.           |
| Troubleshooting | Common issues and their solutions.                        |
| Architecture  | Overview of the project's design and architecture.          |
| Terminology   | Explanation of key terms used in the project.               |
| Workflows     | High-level workflows and use cases for the project.         |

### Contribution Info

The contribution info section provides guidance for contributors, including coding standards and how to contribute to the project. It should include the following:

| Section       | Description                                                  |
|---------------|--------------------------------------------------------------|
| Contributing  | Guidelines for contributing to the project.                 |
| Coding Standards | Coding conventions and best practices.                     |

### Extras

The extras section includes additional content such as tutorials, examples, FAQs, and the project's roadmap. It should include the following:

| Section       | Description                                                  |
|---------------|--------------------------------------------------------------|
| Examples      | Example scripts or use cases to demonstrate the project.    |
| Tutorials     | Step-by-step tutorials for specific use cases.              |
| FAQ           | Frequently asked questions and their answers.               |
| Changelog     | Record of major changes, features, and fixes.               |
| Roadmap       | Planned features or future development goals.               |

### License

The license section provides information about the project's license, including terms and conditions for use and distribution.

<!-- # Notes
- All files are written in Markdown (.md) to ensure compatibility with tools like GitHub Pages or ReadTheDocs.
- Cross-link sections using relative links (e.g., `[Usage Guide](usage/basics.md)`) for better navigation.
- Use consistent naming conventions for clarity.
- If the project includes a lot of autogenerated content (e.g., API references), consider a script to update these sections automatically.

# Key Features
1. **Index Page:** A summary of the project, including purpose and features.
2. **Getting Started:** Helps new users get up and running quickly.
3. **Usage and Reference:** Detailed instructions and API documentation.
4. **Guides and Concepts:** Advanced knowledge for deeper understanding and integration.
5. **Contribution Info:** Encourage and guide contributors.
6. **Extras:** Tutorials, examples, FAQ, and roadmap for additional context. -->

## Benefits

Well-structured documentation provides many benefits to those who interact with the project.

### Benefits for Developers

Documentation helps developers:
- **Navigate** the codebase
- **Understand** the project's architecture
- **Contribute** effectively
- **Follow** coding standards and best practices
- **Onboard** new contributors

### Benefits for Users

Documentation helps users:
- **Install** and **use** the software
- **Troubleshoot** common issues
- **Integrate** it with other tools
- **Extend** or **customize** its functionality

### Benefits for Project Managers

Documentation helps project managers:
- **Track** project progress
- **Plan** future releases
- **Communicate** changes through release notes

### Benefits for Support Staff

Documentation helps support staff:
- **Provide** effective support
- **Resolve** user issues
- **Maintain** FAQs and troubleshooting guides
