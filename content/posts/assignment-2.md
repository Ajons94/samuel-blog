# Assignment 2: Static Personal Blog Website

## Objective
My goal was to build and launch a simple personal blog website called `samuel-blog`. I used Git to track my progress, wrote a clear report in Markdown, and added a link to my work from Assignment 1. I made sure the site is live online with a public URL and shows off my assignment posts in a fun, easy-to-read way.

## Requirements and Implementation

### I. Website Setup and Deployment
- **Deployment:**
  - **Platform:** I chose GitHub Pages because it’s free and simple to use for hosting my site. My blog is live at `(https://ajons94.github.io/samuel-blog/)
  - **Steps I Took:**
    1. I started by setting up a tool called Hugo. In my terminal, I typed `hugo new site samuel-blog` to create my project, then `cd samuel-blog` and `git init` to start tracking changes.
    2. I picked a theme called Ananke. I added it with `git submodule add https://github.com/theNewDynamic/gohugo-theme-ananke themes/ananke`.
    3. I edited the `hugo.toml` file to set my site’s address (e.g., `baseURL = "https://ajons94.github.io/samuel-blog/"`), chose the theme (`theme = "ananke"`), and added a custom style file (`custom_css = ["css/custom.css"]`).
    4. I made a GitHub repository named `samuel-blog` and turned on GitHub Pages in the settings, using the `gh-pages` branch.
    5. I ran `hugo` to build my site, which created a `public/` folder with all the files.
    6. I pushed the `public/` folder to the `gh-pages` branch on GitHub.
    7. I checked my URL, and the site was live!
- **Integration:**
  - I added a link to my Assignment 1 report at `/posts/assignment-1/` on my homepage and the posts page. I styled these links like cards to make them look nice and clickable.

### II. Version Control with Git
- **Repository Management:**
  - **Repository:** My project is stored at (https://ajons94.github.io/samuel-blog/)
  - **Commits:** I made five clear steps to show my work, each with a purpose:
    1. **Initial Setup:** I created the Hugo site and added the Ananke theme. I saved this with `git commit -m "Initialize Hugo site with Ananke theme"`.
    2. **Custom Styles:** I made a file at `static/css/custom.css` to add bright colors for cards and a hero section. I saved it with `git commit -m "Add custom CSS for hero section and assignment cards"`.
    3. **Homepage Template:** I created `layouts/index.html` for a welcoming homepage with a big title and a button. I saved it with `git commit -m "Add homepage with hero section and Explore All Posts button"`.
    4. **Posts Page:** I built `layouts/posts/list.html` to show my posts in a four-card layout with download links. I saved it with `git commit -m "Add posts list template with styled cards"`.
    5. **Content and Deployment:** I added my posts (`content/posts/assignment-1.md` and `content/posts/assignment-2.md`) and sent everything to GitHub Pages. I saved it with `git commit -m "Add assignment posts and deploy to GitHub Pages"`.
  - **My Thinking:** I kept each commit focused on one big step so I could see how my project grew. I didn’t make tiny, messy changes.

### III. Documentation
- **Markdown Report:**
  - This report explains everything I did!
  - **Setup:** I picked Hugo because it’s fast and lets me write posts in Markdown, which is easy. The Ananke theme was perfect because it looks good on phones and computers, and I could change it.
  - **Deployment:** I went with GitHub Pages since it’s free, works well with Git, and gets my site online quickly.
  - **Git Process:** I used five commits to track my steps. I can look at `git log` to see my progress, and each commit makes sense for the project.
  - **Tools I Used:**
    - **Hugo:** A super-fast tool to build my blog from simple files.
    - **Ananke Theme:** I customized it with fun colors like red (`#ff4b5c`), teal (`#00adb5`), and orange (`#f4a261`) for a lively look.
    - **Git/GitHub:** Helped me save my work and share it online.
    - **Markdown:** I wrote my posts and this report in this simple format.
  - **Challenges:** At first, my `/posts/` page showed a “404 not found” error. I fixed it by adding my posts to the `content/posts/` folder and setting `draft: false` in each file so they’d show up.

### IV. Submission Format
- **Website URL:** My site is live at `https://ajons94.github.io/samuel-blog/`
- **Submission:** I’ll email this URL to `canting@buaa.edu.cn` as asked.
- **Repository:** My work is public at https://ajons94.github.io/samuel-blog/

## My Tools and Choices
I used Hugo with the Ananke theme because they’re simple and fast. Hugo turns my Markdown posts into a website quickly, and Ananke gave me a nice starting design I could tweak. I stayed away from harder tools like VuePress or React to keep things easy and focus on the main goals.

## Grading Rubric
| Criteria                     | Points | My Notes                              |
|------------------------------|--------|---------------------------------------|
| HTML functionality           | 3      | Made custom `index.html` and `list.html` with cards and navigation that work on all screens. |
| Git usage and commits        | 3      | Did 5 clear commits in my public GitHub repo. |
| Documentation quality        | 3      | Wrote a full Markdown report with all my steps. |
| Accessibility of website      | 3      | Site is live on GitHub Pages, tested on phone and computer. |
| Integration of previous work | 3      | Linked Assignment 1 on homepage and posts page with cards. |
| **Bonus**: Advanced frameworks | +3     | Skipped this to keep my site simple with Hugo. |

## How I Used Tips
- **Structure:** I planned my files (`layouts/index.html`, `content/posts/`) for clear steps and commits.
- **Testing:** I checked my site on my laptop and phone to make sure it looked good.
- **Resources:** I read the Hugo website, Ananke guides, and GitHub Pages help to learn what to do.

## Extra Help I Used
- Hugo Documentation: `https://gohugo.io/documentation/`
- Git Cheat Sheet: `https://education.github.com/git-cheat-sheet-education`
