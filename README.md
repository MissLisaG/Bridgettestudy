# Study Resources Website

A complete, password-protected educational website with video library, downloads, and external links.

## Features

- **3 Password-Protected Class Sections** - Each class has its own password and dedicated resource area
- **Video Repository** - Embedded YouTube videos organized by category
- **Download Center** - GitHub-integrated file downloads for study materials
- **External Links** - Curated list of educational resources
- **Responsive Design** - Works on desktop, tablet, and mobile devices
- **Clean, Professional Interface** - Easy navigation and modern styling

## Files Included

- `index.html` - Landing page with class selection
- `class1.html` - Password-protected Class 1 page
- `class2.html` - Password-protected Class 2 page
- `class3.html` - Password-protected Class 3 page
- `videos.html` - Video library page
- `downloads.html` - Download center with GitHub links
- `links.html` - External resources page
- `styles.css` - Complete stylesheet
- `README.md` - This file

## Quick Setup

### 1. Change Class Passwords

**Important:** Change the default passwords before deploying!

Edit each class file (`class1.html`, `class2.html`, `class3.html`) and find this line:

```javascript
const CLASS_PASSWORD = 'class1pass';  // CHANGE THIS!
```

Replace with your own secure password for each class.

### 2. Customize Content

#### Class Names
In `index.html`, update the class names and descriptions:
```html
<h2>Class 1</h2>
<p>Access materials and resources for Class 1</p>
```

#### Add Your Resources
In each class page, update the download links and assignments with your actual file links.

### 3. Add Videos

In `videos.html`, replace the placeholder YouTube URLs:

1. Go to your YouTube video
2. Click "Share" → "Embed"
3. Copy the video ID from the URL (e.g., `dQw4w9WgXcQ`)
4. Update the iframe src:
```html
<iframe src="https://www.youtube.com/embed/YOUR-VIDEO-ID" ...>
```

### 4. Set Up GitHub Downloads

#### Option A: GitHub Repository (Recommended)

1. Create a new GitHub repository
2. Create folders: `study-guides/`, `worksheets/`, `templates/`
3. Upload your files to these folders
4. Get the raw file URLs (click file → "Raw" button)
5. Update links in `downloads.html`:
```html
https://github.com/YOUR-USERNAME/YOUR-REPO/raw/main/path/to/file.pdf
```

#### Option B: Direct File Links

If you prefer hosting files elsewhere:
1. Upload files to your web host
2. Get direct download links
3. Replace GitHub URLs in `downloads.html`

### 5. Deploy to GitHub Pages

1. Create a new GitHub repository
2. Upload all files to the repository
3. Go to Settings → Pages
4. Select "Deploy from a branch"
5. Choose "main" branch and "/ (root)" folder
6. Click Save
7. Your site will be live at: `https://YOUR-USERNAME.github.io/REPO-NAME/`

## Customization Guide

### Change Colors

Edit `styles.css` and modify the color variables:

```css
:root {
    --primary-color: #2563eb;      /* Main blue color */
    --secondary-color: #1e40af;    /* Darker blue */
    --accent-color: #3b82f6;       /* Light blue */
}
```

### Update Site Name

Replace "Study Hub" in the navigation of each HTML file:

```html
<h1 class="nav-logo">Your School Name</h1>
```

### Add More Classes

To add a 4th class:
1. Copy `class3.html` → `class4.html`
2. Update the password variable
3. Update content
4. Add a card in `index.html`:
```html
<div class="class-card">
    <div class="class-icon">📖</div>
    <h2>Class 4</h2>
    <p>Description</p>
    <a href="class4.html" class="btn">Enter Class</a>
</div>
```

### Add More Video Categories

In `videos.html`, add a new section:

```html
<div class="content-section">
    <h2>New Category</h2>
    <div class="video-grid">
        <!-- Add video cards here -->
    </div>
</div>
```

### Add More Link Categories

In `links.html`, add a new section:

```html
<div class="content-section">
    <h2>New Link Category</h2>
    <ul class="links-list">
        <!-- Add link items here -->
    </ul>
</div>
```

## Security Notes

### Password Protection

⚠️ **Important**: The password protection uses client-side JavaScript, which is suitable for basic classroom use but NOT for highly sensitive content.

**How it works:**
- Passwords are checked in the browser
- Correct password unlocks content for the current session
- Sessions expire when browser is closed
- Prevents casual access but not determined attackers

**For stronger security:**
- Use a proper authentication system (requires backend server)
- Consider platforms like Google Classroom or Canvas
- Or use GitHub's built-in authentication features

### Recommended Use Cases

✅ **Good for:**
- Class materials and assignments
- Study guides and worksheets
- Video tutorials
- General educational content
- Controlling student access to different class sections

❌ **Not suitable for:**
- Highly confidential information
- Personal student data
- Exam answers or test banks
- Sensitive school records

## Maintenance

### Regular Updates

1. **Add new content** by editing the respective HTML files
2. **Update GitHub files** - just replace files in your repository
3. **Change videos** - update the YouTube embed URLs
4. **Modify links** - add/remove links in `links.html`

### Testing

Always test after making changes:
1. Check all passwords work correctly
2. Verify all download links are functional
3. Test video embeds load properly
4. Ensure responsive design on mobile devices

## Troubleshooting

### Videos Not Loading
- Check YouTube URL format: `https://www.youtube.com/embed/VIDEO-ID`
- Ensure video is not private or age-restricted
- Verify iframe embed is enabled for the video

### Downloads Not Working
- Check GitHub URLs are in "raw" format
- Verify file permissions in repository
- Test links in incognito/private browsing mode

### Passwords Not Working
- Check for typos in password string
- Ensure quotes are correct: `'password'` not `"password"`
- Clear browser cache and try again
- Check sessionStorage is enabled in browser

### Mobile Display Issues
- Clear cache on mobile device
- Check viewport meta tag is present
- Verify CSS media queries are working

## Support

For issues or questions:
1. Check this README first
2. Review the HTML/CSS comments in the code
3. Search GitHub or Stack Overflow for similar issues
4. Consider hiring a web developer for advanced customization

## License

This template is free to use and modify for educational purposes.

## Credits

Created for educational use. Feel free to customize and adapt for your classroom needs.
