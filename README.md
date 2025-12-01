# Mechanical Engineering Portfolio Website

A simple, static portfolio website to showcase mechanical engineering projects with interactive 3D model support.

## Features

- Clean, modern, and responsive design
- Interactive 3D model viewer using Google's `model-viewer` web component
- Easy to customize (no build tools required)
- Optimized for GitHub Pages hosting
- Beginner-friendly code structure

## File Structure

```
/
├── index.html          # Main landing page
├── projects.html       # Projects gallery page
├── about.html          # About page
├── contact.html        # Contact page
├── css/
│   └── style.css       # Main stylesheet
├── js/
│   └── main.js         # JavaScript for interactivity
├── images/             # Project images
└── models/             # 3D model files (glTF/GLB format)
```

## Getting Started

### 1. Customize Your Content

#### Update HTML Files
- **index.html**: Update the hero section with your name and title
- **projects.html**: Replace placeholder project information with your actual projects
- **about.html**: Add your background, education, skills, and interests
- **contact.html**: Update contact information and social media links

#### Add Project Images
1. Place your project images in the `images/` folder
2. Update image paths in the HTML files (replace `images/project-placeholder.jpg`)
3. Recommended image size: 1200x800px or similar aspect ratio
4. Supported formats: JPG, PNG, WebP

#### Add 3D Models
1. Convert your 3D models to **glTF** or **GLB** format
   - GLB is recommended (single file, easier to manage)
   - Tools for conversion:
     - [Blender](https://www.blender.org/) (free, open-source)
     - [Online converters](https://products.aspose.app/3d/conversion)
2. Place your model files in the `models/` folder
3. Update the `src` attribute in `<model-viewer>` tags in `projects.html`
   ```html
   <model-viewer
       src="models/your-model-name.glb"
       alt="Description of your model"
       ...
   >
   ```

### 2. Customize Styling

Edit `css/style.css` to change:
- Colors: Update CSS variables in `:root` section
- Fonts: Change the `font-family` in the `body` selector
- Layout: Adjust spacing, sizes, and grid layouts

### 3. Test Locally

1. Open `index.html` in your web browser
2. Navigate through all pages to ensure everything works
3. Test the 3D model viewer (if you've added models)
4. Test on mobile devices or use browser developer tools

## Deployment to GitHub Pages

### Option 1: Using GitHub Repository

1. **Create a GitHub repository**
   - Go to [GitHub](https://github.com) and create a new repository
   - Name it (e.g., `mechanical-engineering-portfolio`)

2. **Push your code**
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
   git push -u origin main
   ```

3. **Enable GitHub Pages**
   - Go to your repository on GitHub
   - Click **Settings** → **Pages**
   - Under "Source", select **main** branch and **/ (root)** folder
   - Click **Save**
   - Your site will be available at: `https://YOUR_USERNAME.github.io/YOUR_REPO_NAME/`

### Option 2: Using Netlify (Alternative)

1. Go to [Netlify](https://www.netlify.com/)
2. Sign up/login (free)
3. Drag and drop your project folder onto Netlify
4. Your site will be live instantly!

## 3D Model Format Requirements

- **Format**: glTF (.gltf) or GLB (.glb) - GLB is recommended
- **File Size**: Keep models under 10MB for best performance
- **Optimization**: Use tools like [glTF-Pipeline](https://github.com/CesiumGS/gltf-pipeline) to optimize large models

### Converting 3D Models to glTF/GLB

**From SolidWorks:**
1. Export as STL or STEP
2. Import into Blender
3. Export as glTF/GLB

**From Fusion 360:**
1. Export as STL or OBJ
2. Import into Blender
3. Export as glTF/GLB

**From Blender:**
1. File → Export → glTF 2.0
2. Choose GLB format for single file

## Customizing the Contact Form

The contact form is currently a template. To make it functional, you have several options:

1. **Formspree** (Easiest - No backend needed)
   - Sign up at [Formspree](https://formspree.io/)
   - Get your form endpoint
   - Update the form action in `contact.html`

2. **Netlify Forms** (If using Netlify)
   - Add `netlify` attribute to the form tag
   - Netlify will automatically handle submissions

3. **Backend Integration**
   - Set up a server (Node.js, Python, etc.)
   - Update the form action to point to your backend endpoint

## Browser Support

- Modern browsers (Chrome, Firefox, Safari, Edge)
- 3D model viewer requires WebGL support (available in all modern browsers)
- Mobile browsers are supported

## Tips for Best Results

1. **Optimize Images**: Compress images before uploading to reduce load times
2. **Optimize 3D Models**: Keep model file sizes reasonable (< 10MB)
3. **Test on Mobile**: Always test your site on mobile devices
4. **Update Regularly**: Keep your portfolio updated with new projects
5. **SEO**: Update meta descriptions in HTML `<head>` sections for better search visibility

## Troubleshooting

### 3D Models Not Loading
- Check that the file path is correct
- Ensure the file is in glTF or GLB format
- Check browser console for errors
- Verify the file size isn't too large

### Images Not Displaying
- Check file paths are correct
- Ensure image files exist in the `images/` folder
- Check file names match exactly (case-sensitive on some servers)

### GitHub Pages Not Updating
- Wait a few minutes after pushing changes
- Clear your browser cache
- Check GitHub Pages settings in repository settings

## License

This project is open source and available for personal use. Feel free to customize it for your own portfolio!

## Support

For issues or questions:
- Check the browser console for errors
- Verify all file paths are correct
- Ensure all required files are in the repository

---

**Happy showcasing!** 🚀

