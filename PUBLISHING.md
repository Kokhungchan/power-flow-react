# Publishing Guide

## Prerequisites

1. Ensure you have a GitHub account
2. Your repository is at: https://github.com/Kokhungchan/power-flow
3. Git is installed and configured

## Steps to Publish

### 1. Build the Project

```bash
npm run build
```

This creates the `dist/power-flow-card.js` file.

### 2. Commit and Push Changes

```bash
git add .
git commit -m "Release v1.0.2 - Add CSS customization support"
git push origin main
```

### 3. Create a GitHub Release

1. Go to: https://github.com/Kokhungchan/power-flow/releases
2. Click "Create a new release"
3. Tag version: `v1.0.2`
4. Release title: `v1.0.2 - CSS Customization Support`
5. Description:
   ```
   ## What's New
   - ✨ Added CSS customization via config
   - 🎨 Customizable flow line colors
   - 🔧 Customizable card styling
   - 🐛 Fixed animation issues
   
   ## Installation
   See README for installation instructions via HACS or manual installation.
   ```
6. Click "Publish release"

### 4. Submit to HACS (if not already done)

If this is your first time submitting to HACS:

1. Go to: https://github.com/hacs/default
2. Fork the repository
3. Add your repository to `custom_components/hacs/repositories.json`
4. Create a pull request

Your `hacs.json` is already configured correctly.

### 5. Update Version

After publishing, update version for next release:

```bash
npm version patch  # for 1.0.3
# or
npm version minor  # for 1.1.0
# or
npm version major  # for 2.0.0
```

## Testing Before Publishing

Test locally in Home Assistant:

1. Copy `power-flow-card.js` to `/config/www/`
2. Add resource in Home Assistant:
   - URL: `/local/power-flow-card.js`
   - Type: JavaScript Module
3. Test the card with your configuration

## Checklist

- [ ] Code builds without errors (`npm run build`)
- [ ] README is up to date
- [ ] Version number is updated in `package.json`
- [ ] All changes are committed
- [ ] GitHub release is created
- [ ] HACS repository is updated (if applicable)
