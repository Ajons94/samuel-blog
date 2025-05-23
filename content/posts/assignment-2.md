
# Assignment 2: Static Personal Blog Website


## Objective

The objective was to create and deploy a static personal blog website named `samuel-blog`, using Git for version control, documenting the process in Markdown, and integrating previous work. The website must be accessible via a public URL, showcasing vibrant assignment posts.

## Requirements and Implementation

### I. Website Setup and Deployment

**Deployment**:
- **Platform**: Deployed on GitHub Pages, accessible at `[your-website-url]` (e.g., `https://username.github.io/samuel-blog/`).
- **Process**:
  1. Initialized a Hugo project: `hugo new site samuel-blog && cd samuel-blog && git init`.
  2. Added the Ananke theme: `git submodule add https://github.com/theNewDynamic/gohugo-theme-ananke themes/ananke`.
  3. Configured `hugo.toml` with `baseURL`, `theme = "ananke"`, and `custom_css = ["css/custom.css"]`.
  4. Created a GitHub repository (`samuel-blog`) and enabled GitHub Pages on the `gh-pages` branch.
  5. Generated the `public/` directory with `hugo` and pushed it to `gh-pages`.
  6. Confirmed the site is live at the GitHub Pages URL.

**Integration**:
- Added a link to my [Assignment 1 report](/posts/assignment-1/) on the homepage and `/posts/` page, accessible via styled cards.

### II. Version Control with Git

**Repository Management**:
- **Repository**: [github.com/username/samuel-blog](https://github.com/username/samuel-blog) (replace with your actual repo URL).
- **Commits**: Made at least five meaningful commits, each representing a development milestone:
  1. **Initial setup**: Created Hugo site and added Ananke theme (`git commit -m "Initialize Hugo site with Ananke theme"`).
  2. **Custom styles**: Added `static/css/custom.css` for vibrant card and hero designs (`git commit -m "Add custom CSS for hero section and assignment cards"`).
  3. **Homepage template**: Created `layouts/index.html` with hero section (`git commit -m "Add homepage with hero section and Explore All Posts button"`).
  4. **Posts page**: Added `layouts/posts/list.html` for four-card layout with download links (`git commit -m "Add posts list template with styled cards"`).
  5. **Content and deployment**: Added posts (`assignment-1.md`, `assignment-2.md`) and deployed to GitHub Pages (`git commit -m "Add assignment posts and deploy to GitHub Pages"`).
- **Rationale**: Commits reflect logical progression, avoiding trivial changes for clarity.

### III. Documentation

**Markdown Report**:
- This document details the entire process:
  - **Setup**: Chose Hugo for its speed and Markdown support, with Ananke for a responsive, customizable design.
  - **Deployment**: Selected GitHub Pages for free, reliable hosting and Git integration.
  - **Git Process**: Structured commits to track development, viewable via `git log`.
  - **Tools**:
    - **Hugo**: Fast static site generator, ideal for blogs.
    - **Ananke Theme**: Customized with vibrant colors (`#ff4b5c`, `#00adb5`, `#f4a261`).
    - **Git/GitHub**: Managed version control and deployment.
    - **Markdown**: Used for posts and documentation.
  - **Challenges**: Resolved a 404 error on `/posts/` by adding posts to `content/posts/` with `draft: false`.

### IV. Submission Format

- **Website URL**: `[your-website-url]` (e.g., `https://username.github.io/samuel-blog/`).
- **Submission**: Emailed the URL to `canting@buaa.edu.cn` as required.
- **Repository**: Publicly accessible at [github.com/username/samuel-blog](https://github.com/username/samuel-blog).

## Suggested Tools and Frameworks

I used **Hugo** with the **Ananke theme**, as recommended, for its simplicity and performance. Hugo’s Markdown support and theme flexibility enabled a vibrant, user-friendly blog. I avoided advanced frameworks like VuePress or React to focus on core requirements and ease of use.

## Grading Rubric

| Criteria                     | Points | Implementation Notes |
|------------------------------|--------|----------------------|
| HTML functionality           | 3      | Custom `index.html` and `list.html` with responsive cards and navigation. |
| Git usage and commits        | 3      | 5+ meaningful commits in public GitHub repo. |
| Documentation quality        | 3      | Comprehensive Markdown report covering all requirements. |
| Accessibility of website      | 3      | Live on GitHub Pages, tested on multiple devices. |
| Integration of previous work | 3      | Linked Assignment 1 in `/posts/` and homepage cards. |
| **Bonus**: Advanced frameworks | +3     | Not pursued; prioritized Hugo simplicity. |

## Tips & Suggestions Applied

- **Project Structure**: Planned templates (`layouts/index.html`, `layouts/posts/list.html`) and content (`content/posts/`) for logical commits.
- **Testing**: Tested site on desktop and mobile for responsiveness.
- **Resources**: Leveraged Hugo documentation, Ananke theme guides, and GitHub Pages tutorials.

## Additional Resources Used

- [Hugo Documentation](https://gohugo.io/documentation/)
- [Git Cheat Sheet](https://education.github.com/git-cheat-sheet-education