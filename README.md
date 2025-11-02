
You should **always work on the `main` branch** for your day-to-day blogging activities.

And you should **always run the Hexo commands in the `root`** of the Hexo project.

## Your workflow on the `main` branch:

### ✅ Always do these on `main`:
- Write new posts: `hexo new "Post Title"`
- Edit existing posts
- Modify `_config.yml` 
- Install themes or plugins
- Test locally: `hexo server`
- **Deploy:** `hexo clean && hexo g -d`
- **Backup source files:** `git add . && git commit && git push origin main`

### ❌ Never manually work on `gh-pages`:
- The `gh-pages` branch is **automatically managed** by `hexo deploy`
- It only contains generated HTML/CSS/JS files
- You should never edit files directly on `gh-pages`

## Branch purposes:
- **`main` branch** = Your workspace (source files, posts, config)
- **`gh-pages` branch** = Auto-generated website files (hands-off)

## Quick check:
```bash
git branch  # Should show * main (you're on main)
```

If you're ever on the wrong branch:
```bash
git checkout main  # Switch back to main
```

**Always work on `main` and let Hexo handle the `gh-pages` branch automatically.** 🎯

## Theme

1. Use the first approach to install a theme: Download the tar.gz file from the theme's GitHub repository and extract it into the `themes` directory of your Hexo project. Then, update the `_config.yml` file in the root to set the theme to the extracted theme directory.
2. To fine tune the new theme, go to `themes/<theme-name>/_config.yml` and modify the settings.