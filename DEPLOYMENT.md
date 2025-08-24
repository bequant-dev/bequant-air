# BeQuant Theme Deployment Guide

This guide will help you deploy your customized BeQuant Discourse theme to your forum.

## Prerequisites

- GitHub account
- Discourse forum with admin access
- Basic knowledge of Git

## Step 1: Fork and Customize

### 1.1 Fork the Repository
1. Go to your forked `bequant-air` repository
2. Update the `about.json` file with your repository URL:
   ```json
   {
     "name": "BeQuant Theme",
     "about_url": "https://bequant.dev",
     "license_url": "https://github.com/YOUR_USERNAME/bequant-air/blob/main/LICENSE"
   }
   ```

### 1.2 Customize Colors (Optional)
If you want to adjust the colors further, edit the color schemes in `about.json`:

```json
"color_schemes": {
  "bequant-light": {
    "primary": "your-custom-primary",
    "secondary": "your-custom-secondary",
    "tertiary": "your-custom-accent"
  }
}
```

## Step 2: Deploy to GitHub

### 2.1 Initialize Git Repository
```bash
cd bequant-air
git init
git add .
git commit -m "Initial BeQuant theme customization"
```

### 2.2 Push to GitHub
```bash
git remote add origin https://github.com/YOUR_USERNAME/bequant-air.git
git branch -M main
git push -u origin main
```

## Step 3: Install on Discourse

### 3.1 Access Discourse Admin
1. Go to your Discourse forum
2. Sign in as an administrator
3. Navigate to **Admin** → **Customize** → **Themes**

### 3.2 Install Theme
1. Click **Install** → **From a git repository**
2. Enter your repository URL: `https://github.com/YOUR_USERNAME/bequant-air`
3. Click **Install**
4. Wait for the installation to complete

### 3.3 Enable Theme
1. Find your theme in the themes list
2. Click **Enable** to make it the active theme
3. Click **Set as default** to make it the default for new users

## Step 4: Configure Color Schemes

### 4.1 Enable Color Schemes
1. Go to **Admin** → **Customize** → **Colors**
2. Find "BeQuant Light" and "BeQuant Dark"
3. For each color scheme:
   - Click **Edit**
   - Check **"Color scheme can be selected by users"**
   - Click **Save**

### 4.2 Test Theme Switching
1. Go to your forum's main page
2. Look for the theme toggle button in the top-right corner
3. Click it to switch between light and dark modes
4. Verify that the theme preference is saved

## Step 5: Configure Theme Components

### 5.1 Search Banner (Optional)
If you want to use the search banner component:
1. Go to **Admin** → **Customize** → **Theme Components**
2. Find "Discourse Search Banner"
3. Click **Enable**
4. Set the **Plugin Outlet** to **"Below Site Header"**

### 5.2 Category Boxes (Optional)
For modern category boxes:
1. Go to **Admin** → **Site Settings** → **Categories**
2. Set **"Category Boxes with Subcategories"** to **enabled**

## Step 6: Test and Verify

### 6.1 Test Light Mode
- Verify all elements are properly visible
- Check that the theme toggle shows a moon icon
- Test navigation and user interactions

### 6.2 Test Dark Mode
- Click the theme toggle to switch to dark mode
- Verify the toggle shows a sun icon
- Check that all text is readable
- Test all interactive elements

### 6.3 Test Responsiveness
- Test on desktop, tablet, and mobile devices
- Verify the theme toggle is accessible on all screen sizes
- Check that all components work properly

## Troubleshooting

### Theme Not Installing
- **Check Repository URL**: Ensure the GitHub URL is correct
- **Verify Permissions**: Make sure the repository is public
- **Check Discourse Logs**: Look for error messages in admin logs

### Theme Toggle Not Working
- **Enable Color Schemes**: Ensure both color schemes are enabled for users
- **Check JavaScript**: Open browser console for any errors
- **Clear Cache**: Clear browser cache and reload

### Styling Issues
- **Check CSS Conflicts**: Disable other themes temporarily
- **Verify SCSS Compilation**: Check that all SCSS files are properly compiled
- **Browser Compatibility**: Test in different browsers

### Performance Issues
- **Optimize Images**: Ensure any custom images are optimized
- **Minimize CSS**: Consider minifying CSS for production
- **CDN Usage**: Use a CDN for better performance

## Maintenance

### Regular Updates
1. **Monitor Discourse Updates**: Keep track of Discourse version changes
2. **Update Dependencies**: Regularly update theme dependencies
3. **Test Compatibility**: Test theme with new Discourse versions

### Backup Strategy
1. **Version Control**: Keep all changes in Git
2. **Regular Backups**: Backup your theme files regularly
3. **Documentation**: Keep track of all customizations

### User Feedback
1. **Monitor Usage**: Track theme usage and user preferences
2. **Collect Feedback**: Gather user feedback on theme experience
3. **Iterate**: Make improvements based on user input

## Advanced Customization

### Custom CSS
Add custom CSS to `common/common.scss`:
```scss
// Your custom styles here
.custom-element {
  color: var(--tertiary);
  background: var(--secondary);
}
```

### Custom JavaScript
Add custom JavaScript to `common/header.html`:
```html
<script>
// Your custom JavaScript here
document.addEventListener('DOMContentLoaded', function() {
  // Custom functionality
});
</script>
```

### Custom Components
Create new theme components by adding files to the appropriate directories:
- `scss/` for additional styling
- `javascripts/` for custom JavaScript
- `common/` for shared components

## Support and Resources

### Documentation
- [Discourse Theme Development](https://docs.discourse.org/)
- [Material Design Guidelines](https://m3.material.io/)
- [SCSS Documentation](https://sass-lang.com/documentation)

### Community
- [Discourse Meta](https://meta.discourse.org/)
- [Discourse Theme Development Forum](https://meta.discourse.org/c/theme)

### Tools
- [Discourse Theme CLI](https://github.com/discourse/discourse_theme)
- [Discourse Development Environment](https://github.com/discourse/discourse_docker)

---

**Need Help?** Create an issue in your GitHub repository or contact the BeQuant team for support. 