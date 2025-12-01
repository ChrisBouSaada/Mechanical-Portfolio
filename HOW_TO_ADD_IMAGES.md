# How to Add Images to Your Portfolio

## Step-by-Step Guide

### Step 1: Prepare Your Images

1. **Find your project images** (photos, screenshots, CAD renders, etc.)
2. **Recommended formats**: JPG, PNG, or WebP
3. **Recommended size**: 
   - Width: 1200-1600 pixels
   - Height: 800-1000 pixels (or similar aspect ratio)
   - File size: Under 500KB per image (for faster loading)

**Tip**: You can resize images using:
- Online tools: [TinyPNG](https://tinypng.com/) or [Squoosh](https://squoosh.app/)
- Mac: Preview app → Tools → Adjust Size
- Windows: Paint or Photos app

### Step 2: Add Images to the Images Folder

1. **Copy your image files** to the `images/` folder in your project
2. **Name your files** clearly (use lowercase, no spaces):
   - Good: `robot-arm-project.jpg`
   - Good: `project1-main.png`
   - Avoid: `My Project Image!.jpg` (spaces and special characters can cause issues)

**Example folder structure:**
```
images/
  ├── robot-arm-project.jpg
  ├── gear-system.png
  ├── project-3-main.jpg
  └── model-poster-1.jpg
```

### Step 3: Update the HTML Files

You need to replace `images/project-placeholder.jpg` with your actual image file names.

#### For the Homepage (index.html)

Find lines like this:
```html
<img src="images/project-placeholder.jpg" alt="Project 1">
```

Replace with:
```html
<img src="images/your-image-name.jpg" alt="Project 1">
```

**Example:**
- If your image is named `robot-arm.jpg`, change it to:
  ```html
  <img src="images/robot-arm.jpg" alt="Robot Arm Project">
  ```

#### For the Projects Page (projects.html)

Same process - find the placeholder image references and replace them.

**Locations to update:**
1. **Project thumbnail images** (around line 47, 88, 129)
2. **3D model poster images** (optional, around line 75, 116, 157)

### Step 4: Update the Alt Text

Always update the `alt` attribute to describe your image. This helps with accessibility and SEO.

**Example:**
```html
<img src="images/robot-arm.jpg" alt="3D rendered view of robotic arm assembly">
```

## Quick Example

Let's say you have an image called `my-robot-project.jpg`:

1. **Copy the file** to: `images/my-robot-project.jpg`

2. **In index.html**, find:
   ```html
   <img src="images/project-placeholder.jpg" alt="Project 1">
   ```

3. **Replace with:**
   ```html
   <img src="images/my-robot-project.jpg" alt="Robotic Arm Assembly">
   ```

4. **Save the file** and refresh your browser!

## Common Issues & Solutions

### Image Not Showing?

1. **Check the file name** - Make sure it matches exactly (case-sensitive on some servers)
2. **Check the file path** - Should be `images/your-file.jpg` (not `/images/` or `./images/`)
3. **Check the file exists** - Make sure the file is actually in the `images/` folder
4. **Check the file extension** - `.jpg` vs `.jpeg` vs `.JPG` - they must match exactly

### Image Too Large/Slow Loading?

1. **Compress the image** using [TinyPNG](https://tinypng.com/)
2. **Resize the image** to around 1200px width
3. **Use WebP format** for better compression (if your images support it)

### Want Multiple Images Per Project?

You can add more images in the project details section on `projects.html`:

```html
<div class="project-image">
    <img src="images/project-main.jpg" alt="Main view">
</div>
<div class="project-image">
    <img src="images/project-detail.jpg" alt="Detail view">
</div>
```

## File Naming Best Practices

✅ **Good names:**
- `robot-arm-project.jpg`
- `project-1-main.png`
- `gear-assembly-front.jpg`

❌ **Avoid:**
- `My Project!.jpg` (spaces and special characters)
- `project image.jpg` (spaces)
- `PROJECT.JPG` (all caps - harder to read)

## Testing

After adding images:
1. Open `index.html` in your web browser
2. Check that images display correctly
3. Test on mobile if possible
4. If deploying to GitHub Pages, push your changes and wait a few minutes

---

**Need help?** Check the browser's developer console (F12) for any error messages about missing images.

