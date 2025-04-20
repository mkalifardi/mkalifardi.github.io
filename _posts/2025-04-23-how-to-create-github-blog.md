---
layout: post
title: "How to Create a GitHub Blog with Jekyll, Git, VS Code, and Ruby (Steps 1–6)"
date: 2025-04-23
tags: [github-pages, jekyll, blog-setup, ruby, git, vscode, tutorial]
---

Creating your own blog using **GitHub Pages** is one of the easiest and most powerful ways to start publishing online — for free. In this tutorial, I’ll guide you step-by-step through building your blog using **Jekyll**, **Git**, **VS Code**, and **Ruby**, based on my experience setting up [mkalifardi.github.io](https://mkalifardi.github.io).

---

#### Step 1: Install the Required Tools

Make sure these tools are installed:

| Tool          | Purpose                        | Link                                 |
|---------------|--------------------------------|--------------------------------------|
| **Git**       | Version control & pushing code | [git-scm.com](https://git-scm.com/) |
| **VS Code**   | Code editor                    | [code.visualstudio.com](https://code.visualstudio.com/) |
| **Ruby + DevKit** | Required for Jekyll        | [rubyinstaller.org](https://rubyinstaller.org/) |
| **GitHub account** | To host your blog         | [github.com](https://github.com/) |

> On Windows, install Ruby with DevKit and install it to a path like `D:\Ruby`.

---

#### Step 2: Install Jekyll and Bundler

After installing Ruby, open **PowerShell** or your terminal and install Jekyll:

```bash
gem install bundler jekyll
```

Check versions:

```bash
ruby -v
jekyll -v
```

If you see version numbers, Ruby and Jekyll are ready.

#### Step 3: Create Your Blog Locally
Now generate a new blog using Jekyll.

```bash
jekyll new mkalifardi.github.io
cd mkalifardi.github.io
```

Then install project dependencies:

```bash
Copy
Edit
bundle install
```

Preview your blog locally:

```bash
Copy
Edit
bundle exec jekyll serve
```

Open your browser and go to:
👉 http://localhost:4000

✅ You’ll see your blog live on your machine!

#### Step 4: Open the Blog in VS Code
Use VS Code to edit your blog:

```bash
code .
```

You’ll see key files and folders like:
- _posts/ → your blog posts
- _config.yml → site title, description, etc.
- index.md, about.md → content pages
- assets/ → images and files

####  Step 5: Customize _config.yml
Edit _config.yml to personalize your blog:

```yaml
title: mnote
description: A digital notebook for infrastructure, transport, and finance.
theme: minima
url: "https://mkalifardi.github.io"
```

You can also:
- Add social links
- Change the theme
- Enable plugins

####  Step 6: Push Your Blog to GitHub
Now publish it to GitHub.

#####  Step 6.1: Create a GitHub Repository
- Go to GitHub and create a new repo named:
mkalifardi.github.io

GitHub Pages uses this special name to auto-host your blog at https://mkalifardi.github.io.

#####  Step 6.2: Push Your Site
In your terminal:

```bash
git init
git remote add origin https://github.com/mkalifardi/mkalifardi.github.io.git
git add .
git commit -m "Initial blog setup"
git push -u origin main
```
🌍 Step 6.3: Enable GitHub Pages
- Go to your repo’s Settings → Pages
- Set the Source to: main branch
- Save

✅ Your blog will be live at:

https://mkalifardi.github.io

That’s it! You've now:

- Set up all required tools
- Installed Jekyll locally
- Created a blog site
- Customized it
- And published it online