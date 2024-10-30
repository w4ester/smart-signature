# Smart Email Signature Generator
A web-based tool for creating dynamic, personalized email signatures with smart bookmarks.

## Quick Start
1. **Local Testing**
```bash
# Create a new directory
mkdir smart-signature
cd smart-signature

# Save the HTML file as index.html
```

2. **Immediate Testing**
- Double-click the `index.html` file to open it in your default browser
- Or right-click and select "Open with" to choose a specific browser

## Deployment Guide

### GitHub Pages Deployment (Using GitHub Actions)

1. **Repository Setup**
```bash
# Initialize a new git repository
git init
git add index.html
git commit -m "Initial commit"

# Create a new repository on GitHub
# Then push your code
git remote add origin your-repo-url
git branch -M main
git push -u origin main
```

2. **GitHub Actions Configuration**
- Create folder structure: `.github/workflows/`
- Create `static.yml` inside workflows folder with the provided GitHub Actions workflow
- Commit and push the workflow file:
```bash
git add .github/workflows/static.yml
git commit -m "Add GitHub Pages deployment workflow"
git push
```

3. **Enable GitHub Pages**
- Go to repository Settings > Pages
- Under "Source", select "GitHub Actions" as the source
- Your site will be available at: `https://username.github.io/repository-name`

### Alternative Deployment Options

#### Using Netlify Drop
1. Go to [Netlify Drop](https://app.netlify.com/drop)
2. Drag and drop your `index.html` file
3. Wait for deployment (usually takes seconds)
4. Access your site at the provided Netlify URL

#### Using Apache
```bash
# Usually located at:
# Ubuntu/Debian: /var/www/html/
# CentOS/RHEL: /var/www/html/
# macOS: /Library/WebServer/Documents/
sudo cp index.html /var/www/html/
```

#### Using Nginx
```bash
# Usually located at:
# Ubuntu/Debian: /usr/share/nginx/html/
# CentOS/RHEL: /usr/share/nginx/html/
sudo cp index.html /usr/share/nginx/html/
```

## Integration Instructions

### 1. Gmail
1. Open Gmail Settings (⚙️)
2. Click "See all settings"
3. Scroll to "Signature"
4. Create new signature
5. Use the "Copy Signature" button from the generator
6. Paste into Gmail signature editor
7. Save changes

### 2. Outlook
1. Open Outlook
2. File > Options > Mail > Signatures
3. Click "New"
4. Use the "Copy Signature" button from the generator
5. Paste into signature editor
6. Save

### 3. Apple Mail
1. Mail > Preferences > Signatures
2. Click "+" to add new signature
3. Use the "Copy Signature" button from the generator
4. Paste into signature field
5. Save

## Security Considerations

1. **Data Privacy**
- All data is processed locally in the browser
- No data is sent to any external servers
- User information is not stored permanently

2. **Link Security**
- All links are generated with HTTPS by default
- Visibility rules are enforced client-side

## Customization

### Modifying Templates
To add or modify templates:

1. Locate the `getTemplateHTML` function in the code
2. Add a new case for your template:
```javascript
case 4: // Your new template
    return `
        <div style="your-styles">
            <!-- Your template HTML -->
        </div>
    `;
```

### Changing Colors
The main colors are defined in CSS variables at the top of the file:
```css
:root {
    --primary-color: #2563eb;
    --secondary-color: #1e40af;
    --background-color: #f3f4f6;
}
```

## Browser Compatibility
- Chrome 80+
- Firefox 75+
- Safari 13+
- Edge 80+
- Opera 67+

## Troubleshooting

### Common Issues

1. **Signature Not Copying**
- Ensure you're using the "Copy Signature" button
- Try using keyboard shortcuts (Ctrl+C/Cmd+C) as fallback

2. **Styles Not Appearing in Email Client**
- Some email clients strip certain CSS
- Use the "Download HTML" option and test in your email client
- Adjust template styles if necessary

3. **Links Not Working**
- Verify all URLs include `http://` or `https://`
- Test links in preview before copying

4. **GitHub Pages Not Updating**
- Check Actions tab for deployment status
- Ensure workflow has necessary permissions
- Verify repository settings are correct

### Support

For issues or feature requests:
1. Test in multiple browsers
2. Clear browser cache
3. Use the latest version
4. Check console for errors (F12 in most browsers)
5. Check GitHub Actions logs for deployment issues

## Future Developments
Planned features:
- Image upload support
- Custom CSS editor
- Template import/export
- Signature backup/restore
- Analytics integration

## License
- 4ester License - Modify and sahre to use in a project(s)
