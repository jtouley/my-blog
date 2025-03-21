# 🚀 Jekyll Blog with GitHub Pages and Substack Integration

This is my **personal tech blog** built with **Jekyll**, hosted on **GitHub Pages**, and auto-publishing to **Substack** via RSS. This README serves as a quick reference for maintaining the blog and guiding others through setting up a similar environment.

---

## 📝 **How to Add or Update Blog Posts**
1. **Create a new Markdown file** in the `_posts/` directory:
   ```bash
   cd ~/Documents/GitHub/my-blog/_posts
   touch YYYY-MM-DD-your-post-title.md
   code .
   ```

2. **Add the front matter and content**:

   ```
   ---
   layout: post
   title: "Your Post Title"
   date: YYYY-MM-DD
   categories: tech automation
   ---
   Your blog post content goes here.
   ```

3. **Include images**:
   • Save images in the assets/images/ directory.
   • Use absolute URLs to ensure they load correctly on Substack:

   ```
   ![Description](https://jtouley.github.io/my-blog/assets/images/your-image.png)
   ```

4. **Commit and push the new post**:

   ```
   git add _posts/YYYY-MM-DD-your-post-title.md
   git commit -m "Added new blog post"
   git push origin main
   ```

5. **Check the live site**:

   ```
   https://jtouley.github.io/my-blog/
   ```

Substack will **automatically pull new posts** via RSS.

## 🛠️ Running Jekyll Locally

To see your changes before pushing:
1. Navigate to your blog directory:

   ```
   cd ~/Documents/GitHub/my-blog
   ```

2. Serve the site locally:

   ```
   bundle exec jekyll serve
   ```

3. Open your browser to:

   ```
   http://127.0.0.1:4000/my-blog/
   ```

4. **Make edits and refresh** to see changes in real-time.

## 🌐 Setting Up Your Own Jekyll Blog
1. **Install Prerequisites (Mac):**

   ```
   brew install ruby
   gem install jekyll bundler
   ```

2. **Create a New Blog:**

   ```
   jekyll new my-blog
   cd my-blog
   bundle install
   ```

3. **Configure _config.yml:**

   ```
   url: "https://YOUR_USERNAME.github.io"
   baseurl: "/my-blog"
   theme: minima
   plugins:
     - jekyll-feed
   permalink: /:categories/:year/:month/:day/:title.html
   ```

4. **Test Locally:**

   ```
   bundle exec jekyll serve
   ```

5. **Deploy to GitHub Pages:**

   ```
   git init
   git remote add origin https://github.com/YOUR_USERNAME/my-blog.git
   git add .
   git commit -m "Initial commit"
   git push -u origin main
   ```

6. **Enable GitHub Pages:**
   • Go to **Settings → Pages**
   • Set the **branch to main** and save.

## 🔗 RSS and Substack Integration
1. Ensure the RSS feed is available at:

   ```
   https://YOUR_USERNAME.github.io/my-blog/feed.xml
   ```

2. **Connect to Substack:**
   • Go to **Substack → Settings → Import**
   • Enter your RSS feed URL
   • Click **Import**

## 📝 Troubleshooting
• **404 Errors on Posts:** Check the baseurl setting and your permalink structure.
• **Images Not Appearing on Substack:** Use **absolute URLs** and ensure images are correctly stored in assets/images/.

## 📧 Questions or Feedback

Feel free to open an issue or reach out if you have questions about the setup or need help.

Happy blogging! 🚀