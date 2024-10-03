---
layout: post
title: "How to Create a Static Website Like this  using Chirpy Starter Template"
date: 2024-09-09
categories: [Web Development, Jekyll]
tags: [Chirpy, Jekyll, Static Website, Tutorial]
---

# How to Create a Static Website Like this  using Chirpy Starter Template

## Prerequisites

Before you begin, ensure the following tools are installed on your system:

1. **Ruby and Bundler**  
   Ruby is required to build the Jekyll site, and Bundler helps manage the gems (Ruby libraries). To install:

   - On Ubuntu or Debian-based systems:
     ```bash
     sudo apt update
     sudo apt install ruby-full build-essential zlib1g-dev
     gem install bundler
     ```

   - On Fedora or Red Hat-based systems:
     ```bash
     sudo dnf install ruby ruby-devel @development-tools
     gem install bundler
     ```

   - On Windows:
     - Download and install Ruby from [RubyInstaller](https://rubyinstaller.org/)
     - During installation, make sure to check the option "Add Ruby executables to your PATH"
     - Open a new command prompt and run:
       ```
       gem install bundler
       ```

2. **g++ Compiler**  
   Some gems, like `eventmachine`, need to be compiled using g++. To install:

   - On Ubuntu or Debian-based systems:
     ```bash
     sudo apt install g++
     ```

   - On Fedora or Red Hat-based systems:
     ```bash
     sudo dnf install gcc-c++
     ```

   - On Windows:
     - Install [MinGW-w64](https://mingw-w64.org/doku.php/download) which includes g++
     - Add the MinGW-w64 bin directory to your system PATH

3. **Node.js and npm** (Optional but recommended)  
   Node.js is useful for managing JavaScript dependencies.
   - Download and install from [Node.js official website](https://nodejs.org/)

4. **Git**  
   Git is required to manage your project repository. To install:

   - On Ubuntu or Debian-based systems:
     ```bash
     sudo apt install git
     ```

   - On Fedora or Red Hat-based systems:
     ```bash
     sudo dnf install git
     ```

   - On Windows:
     - Download and install from [Git for Windows](https://gitforwindows.org/)

## 1. Clone the Chirpy Starter Template

Start by cloning the Chirpy template repository from GitHub.

- Run the following commands:
  ```bash
  git clone https://github.com/cotes2020/jekyll-theme-chirpy.git
  cd jekyll-theme-chirpy
  ```

## 2. Install Dependencies

Now, install the necessary Ruby gems.

- Run:
  ```bash
  bundle install
  ```
This will install all the dependencies listed in the Gemfile.

## 3. Build and Serve Your Website Locally

Once all dependencies are installed, build and preview your site locally.

- Use the command:
  ```bash
  bundle exec jekyll serve
  ```
Your static website should be available at `http://localhost:4000`.

## 4. Deploy Your Website to GitHub Pages

To deploy your website using GitHub Pages:

1. Push your project to a GitHub repository.
2. Ensure you've set up GitHub Actions with the appropriate `pages-deploy.yml` file for automatic deployment.
3. GitHub will automatically publish your site to `<username>.github.io`.

## Additional Configuration

### Customizing the Site
Modify `_config.yml` to adjust settings like your site's title, description, URL, etc.

### Creating Blog Posts
Add Markdown files to the `_posts` directory for new blog posts. Each file should follow the format `YYYY-MM-DD-title-of-the-post.md`.

## Troubleshooting

If you encounter any issues during the setup or deployment process, here are some common solutions:

1. **Ruby version mismatch**: Ensure you're using a Ruby version compatible with the Chirpy theme. Check the `.ruby-version` file in the project root.

2. **Gem installation errors**: If you encounter errors while installing gems, try running `bundle update` before `bundle install`.

3. **Jekyll build errors**: Make sure all required dependencies are installed. You might need to run `bundle exec jekyll build` to see more detailed error messages.

4. **GitHub Pages deployment issues**: Verify that your repository settings are correct and that the GitHub Actions workflow is properly configured.

## Conclusion

By following this guide, you've successfully set up a static website using the Chirpy Starter Template. You can now customize your site, add content, and share your work with the world through GitHub Pages. Remember to refer to the [Chirpy theme documentation](https://github.com/cotes2020/jekyll-theme-chirpy#documentation) for more advanced customization options and features.

Happy blogging!