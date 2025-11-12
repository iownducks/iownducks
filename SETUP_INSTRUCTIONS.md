# 🎨 GitHub Profile Setup Instructions

Follow these steps to set up your beautiful GitHub profile!

## 📋 Step 1: Create Special Profile Repository

1. Go to GitHub and create a **NEW repository**
2. Name it **exactly** the same as your GitHub username
   - Example: If your username is `johndoe`, create a repo named `johndoe`
3. Make it **PUBLIC**
4. Check the box "Add a README file"
5. Click "Create repository"

GitHub will show a message saying "You found a secret!" - this is the special profile README!

---

## ✏️ Step 2: Customize Your README

Open the `README.md` file I created and replace the following:

### Required Changes:
- `[Your Name]` → Your actual name
- `YOUR_GITHUB_USERNAME` → Your GitHub username (appears multiple times)
- `yourusername` → Your social media usernames
- `your.email@example.com` → Your email
- `yourwebsite.com` → Your portfolio website (or remove if you don't have one)
- `Your Location` → Your city/country

### Optional Customizations:
- Update the typing animation text in the first section
- Modify the "About Me" code block with your real info
- Add/remove technologies you actually use
- Update the "currentFocus" and "funFact" fields
- Replace `project1` and `project2` with your actual project names

---

## 🐍 Step 3: Enable Snake Animation (Optional but Cool!)

The snake eats your contributions! To enable it:

1. In your profile repository, create this folder structure:
   ```
   .github/workflows/
   ```

2. Inside `workflows`, create a file named `snake.yml`

3. Add this content:

```yaml
name: Generate Snake

on:
  schedule:
    - cron: "0 */6 * * *"  # Run every 6 hours
  workflow_dispatch:

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3

      - uses: Platane/snk@v3
        with:
          github_user_name: YOUR_GITHUB_USERNAME
          outputs: |
            dist/github-contribution-grid-snake-dark.svg
            dist/github-contribution-grid-snake.svg

      - name: Push to output branch
        uses: crazy-max/ghaction-github-pages@v3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```

4. Replace `YOUR_GITHUB_USERNAME` with your username
5. Commit the file
6. Go to "Actions" tab in your repository and enable workflows
7. Manually run the "Generate Snake" workflow

---

## 🎨 Step 4: Choose Your Theme

The profile uses the "tokyonight" theme. You can change it to:

- `radical`
- `merko`
- `gruvbox`
- `dracula`
- `monokai`
- `vue`
- `dark`
- `onedark`
- `cobalt`
- `synthwave`
- `highcontrast`
- `nord`
- `algolia`
- `great-gatsby`
- `darcula`
- `bear`
- `solarized-dark`
- `solarized-light`
- `chartreuse-dark`
- `tokyonight`

Just replace `theme=tokyonight` with your preferred theme in all the badge URLs.

---

## 🔧 Step 5: Upload to GitHub

1. Copy the contents of your customized `README.md`
2. Go to your GitHub profile repository
3. Click on the `README.md` file
4. Click the pencil icon (Edit)
5. Paste your customized content
6. Scroll down and click "Commit changes"

---

## ✨ Step 6: See Your Beautiful Profile!

Visit your GitHub profile: `https://github.com/YOUR_GITHUB_USERNAME`

Your profile should now display the beautiful animated README!

---

## 🎯 Pro Tips

### Pin Your Best Repositories
1. Go to your GitHub profile
2. Click "Customize your pins"
3. Select your 6 best projects
4. These will show at the top of your profile

### Update Featured Projects
In the README, replace:
```markdown
[![ReadMe Card](https://github-readme-stats.vercel.app/api/pin/?username=YOUR_GITHUB_USERNAME&repo=project1&theme=tokyonight)](https://github.com/YOUR_GITHUB_USERNAME/project1)
```

With your actual project names.

### Add Blog Posts (Advanced)
To auto-update blog posts:
1. Install the [Blog Post Workflow](https://github.com/gautamkrishnar/blog-post-workflow) GitHub Action
2. It will automatically fetch your latest blog posts from Medium, Dev.to, or your RSS feed

---

## 🐛 Troubleshooting

**Stats not showing?**
- Make sure your repository is public
- Wait a few minutes for the APIs to refresh
- Check that you replaced ALL instances of `YOUR_GITHUB_USERNAME`

**Snake animation not working?**
- Make sure GitHub Actions are enabled
- Check that the workflow ran successfully in the Actions tab
- The snake takes about 5-10 minutes to generate the first time

**Profile not updating?**
- Clear your browser cache
- Wait a few minutes (GitHub caches profile READMEs)
- Make sure you committed the changes

---

## 🌟 Additional Resources

- [GitHub Profile README Generator](https://rahuldkjain.github.io/gh-profile-readme-generator/)
- [Shields.io](https://shields.io/) - Create custom badges
- [Simple Icons](https://simpleicons.org/) - Find logos for technologies
- [GitHub Stats](https://github.com/anuraghazra/github-readme-stats)
- [Awesome GitHub Profile README](https://github.com/abhisheknaiidu/awesome-github-profile-readme)

---

Need help? Feel free to customize it further or ask questions!
