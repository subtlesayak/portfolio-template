# Portfolio Template

## Brief Intro

This is a simple portfolio website template for people who want a clean personal site without learning a heavy framework. Most edits happen in text files and folders, so you can focus on your work instead of fighting the website.

You can use it for design work, photography, writing, student projects, experiments, or any mix of sections that fits your interests. A live example of this template style is here: https://subtlesayak.github.io/

This template is based on the original `artofpilgrim/portfolio-template` idea: keep the website as plain HTML, CSS, JavaScript, folders, and text files. You do not need React, Node, a database, or a build step.

## What You Get

- A portfolio grid on `index.html`.
- A reusable project detail page for each project folder.
- A Photography tab for event or collection-style photo galleries.
- An Articles tab for simple writing or process notes.
- An About page that reads your summary, skills, software, education, and experience from text files.
- Auto, dark, and light theme control.
- Thumbnail size controls on portfolio and photography grids.
- A small e-ink style page transition toggle.
- A sitemap page.
- Starter folders you can copy instead of building from nothing.
- A local validation script that catches missing files before you publish.

## The Shortest Possible Setup

If you are new to GitHub, do this slowly. It is normal if it feels weird the first time.

1. Open this repo on GitHub.
2. Click `Use this template` or download the ZIP.
3. Create your own repository.
4. Put the files in your repository.
5. Edit the text files in `Config/`.
6. Replace the example project content in `Projects/`.
7. Turn on GitHub Pages for your repository.
8. Visit your GitHub Pages URL.

You can make a working portfolio by editing only `.txt` files and replacing images.

## Choose Your Sections

The default sections are:

```txt
Portfolio     your main project grid
Photography   optional photo galleries or visual collections
Articles      optional writing, notes, tutorials, or process posts
About         your profile, skills, education, and experience
```

Think of `Photography` and `Articles` as examples, not rules. Change them to match your interests.

Examples:

```txt
Designer:     Portfolio, Photography, Articles, About
Photographer: Portfolio, Photo Essays, Gear Notes, About
Developer:    Projects, Experiments, Writing, About
Student:      Work, Class Projects, Sketchbook, About
Artist:       Gallery, Process, Exhibitions, About
```

Beginner-safe way to customize sections:

1. Keep the file names the same at first.
2. Change the visible tab text in the navigation.
3. Replace the content in the matching folders and text files.
4. Only rename files like `articles.html` or `photography.html` after you are comfortable updating links.

The About section is usually worth keeping. It helps visitors understand who you are, what you do, what tools you use, and how to contact you.

## Folder Map

```txt
Config/                         Your profile, project list, about text, articles list, site text
Projects/                       One folder per portfolio project
Projects/Photography/           Main photography collection
Projects/Photography/Collections/ Optional extra photography collections
Articles/                       One folder per article
Resources/                      Favicon and shared placeholder assets
Templates/                      Folders to copy when adding new work
CSS/                            Styling files
JS/                             Browser scripts that read your text files
tools/validate-content.js       Optional local checker
index.html                      Portfolio page
photography.html                Photography page
articles.html                   Articles page
about.html                      About page
sitemap.html                    Simple sitemap
```

## Edit Your Profile

Open `Config/userinformation.txt`.

The first lines mean:

```txt
/Resources/placeholders/profile.svg       profile image path
Your Name                                 your displayed name
Your Role @ Studio or Company             your role/title
Your City, Country                        your location
A short one-line intro...                 optional intro sentence
https://github.com/your-username          social link
https://www.linkedin.com/in/your-username social link
your.email@example.com                    email link
```

Rules:

- Keep the first four lines in the same order.
- The intro line is optional, but useful.
- Social links can be removed or reordered.
- Email addresses automatically become email buttons.
- A PDF resume can be added later with a line like `resume:/Resources/resume/resume.pdf`.

Before adding a resume PDF, read `SECURITY-CHECKLIST.md`.

## Edit The About Page

The About page is your profile section. Use it for the short story behind the work: who you are, what you make, what you are learning, and what kind of work you want next.

The About page uses these files:

```txt
Config/summary.txt          one paragraph about you
Config/software.txt         one software/tool per line
Config/skills.txt           one skill per line
Config/productions.txt      experience, education, projects, certificates
Config/recommendations.txt  optional recommendations
```

If you do not have recommendations yet, leave `Config/recommendations.txt` empty.

## Add A Project

The easiest beginner workflow is copy, rename, edit.

1. Copy `Templates/Project Template/`.
2. Paste it inside `Projects/`.
3. Rename the copied folder, for example `My Poster Project`.
4. Copy an existing project HTML file, such as `Projects/Example Project/template-project.html`.
5. Put that copied HTML file inside your new project folder.
6. Rename the HTML file, for example `my-poster-project.html`.
7. Edit your new folder's `description.txt`.
8. Edit your new folder's `media.txt`.
9. Edit your new folder's `stats.txt`.
10. Edit your new folder's `categories.txt`.
11. Open `Config/projects.txt` and add the exact folder name on its own line.

### Project `description.txt`

Use exactly five sections separated by `---`:

```txt
Project Title
---
Short project description.
---
Figma, Photoshop, Branding
---
Projects/My Poster Project/thumbnail.jpg
---
my-poster-project.html
```

Important:

- The folder name in `Config/projects.txt` must match the folder name exactly.
- The HTML filename in `description.txt` must match the real HTML file exactly.
- The thumbnail path is used on the portfolio grid.

### Project `media.txt`

Use one media item per line:

```txt
image-one.jpg
Caption for image one.

image-two.jpg
Caption for image two.
```

Supported project media:

- Local images: `jpg`, `jpeg`, `png`, `gif`, `webp`, `svg`, `avif`
- Videos: `mp4`, `webm`
- YouTube links
- Sketchfab links
- Before/after image pairs separated by ` // `

Example before/after line:

```txt
before.jpg // after.jpg
```

### Project `stats.txt`

Stats are simple label/value lines:

```txt
Role: Designer
Timeline: 2026
Tools: Figma, Photoshop
Collaborators: Your team
```

### Project `categories.txt`

Add one category slug per line:

```txt
uiux
branding
```

Category names and descriptions live in `Config/categories.txt`.

## Add Photography

The main photography collection lives in `Projects/Photography/`.

To add photos to the starter collection:

1. Put image files inside `Projects/Photography/`.
2. Add each filename to `Projects/Photography/media.txt`.
3. Edit `Projects/Photography/entry.txt`.
4. Optional: add smaller thumbnail files with the same filenames inside `Projects/Photography/thumbs/`.

### Add A Separate Photography Collection

Use this when you want one folder per event, trip, shoot, or client.

1. Copy `Templates/Photography Collection Template/`.
2. Paste it inside `Projects/Photography/Collections/`.
3. Rename the copied folder, for example `Street Walk`.
4. Put photos inside that folder.
5. Put optional thumbnails inside that folder's `thumbs/` folder.
6. Edit that folder's `entry.txt` and `media.txt`.
7. Add the folder name to `Projects/Photography/collections.txt`.

Keep the line `.` in `collections.txt` if you still want the root `Projects/Photography/` collection to appear.

## Add An Article

1. Copy `Templates/Article Template/`.
2. Paste it inside `Articles/`.
3. Rename the folder, for example `My First Article`.
4. Edit `Articles/My First Article/article.txt`.
5. Add `My First Article` to `Config/articles.txt`.

Article files use four sections:

```txt
Article Title
---
Month Year
---
Short summary shown on the card.
---
Article body goes here.
```

Article body supports simple formatting:

```txt
# Big Heading
## Smaller Heading
**bold text**
*italic text*
---
```

## Change The Last Updated Line

Open `Config/site.txt` and edit the line:

```txt
Last updated: Month Year
```

This appears quietly near the bottom of the site with a sitemap link.

## Preview Locally

If you have Python installed, run this from the project folder:

```bash
python -m http.server 8000
```

Then open:

```txt
http://localhost:8000
```

If you use VS Code, the Live Server extension is also fine.

Do not judge the site by double-clicking `index.html`; some browsers block local `fetch()` calls from plain files.

## Validate Before Publishing

If you have Node.js installed, run:

```bash
node tools/validate-content.js
```

This checks for common mistakes:

- Missing config files.
- Missing project `description.txt`, `media.txt`, or `stats.txt`.
- Broken local image/media references.
- Incorrect `---` section counts.
- Missing photography collection files.
- Missing article files.

If the validator passes, you will see:

```txt
Content validation passed.
```

## Publish With GitHub Pages

1. Push your repository to GitHub.
2. Go to repository `Settings`.
3. Open `Pages`.
4. Choose `Deploy from a branch`.
5. Choose branch `main` and folder `/root`.
6. Save.
7. Wait for GitHub to build the site.
8. Open the URL GitHub gives you.

If changes do not show instantly, wait a minute and refresh.

## Before You Commit

Read `SECURITY-CHECKLIST.md` before publishing. The short version:

- Do not commit private resumes unless you really want them public.
- Do not commit ID documents, invoices, contracts, or client-confidential work.
- Do not commit `.env` files, API keys, passwords, private keys, or tokens.
- Check your photos for location metadata if privacy matters.
- Replace all placeholder links and email addresses.

## Credits

This template was adapted from the plain-file workflow of `artofpilgrim/portfolio-template`, with extra beginner docs, photography collections, articles, theme controls, sitemap, and validation helpers.
