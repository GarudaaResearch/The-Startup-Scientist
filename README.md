# Startup Scientist Guideline Portal

A comprehensive web portal for physics and biotechnology students to explore innovation opportunities, learn from inspirational personalities, and access real-time experiments.

## Features

- 🚀 Innovation opportunities in Physics & Biotechnology
- ⭐ Inspirational personalities with interactive profiles
- 🔬 Real-time experiments and learning resources
- 🌍 Global future opportunities
- 📱 Responsive design with modern UI

## Deployment on Render

### Prerequisites
- Render account (free tier available)
- Git repository

### Steps to Deploy

1. **Create a Git Repository**
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   ```

2. **Push to GitHub/GitLab**
   ```bash
   git remote add origin <your-repo-url>
   git push -u origin main
   ```

3. **Deploy on Render**
   - Go to [Render Dashboard](https://dashboard.render.com)
   - Click "New +" → "Static Site"
   - Connect your Git repository
   - Build Command: `echo "No build required"`
   - Publish Directory: `.`
   - Add Custom Domain (optional)

4. **Environment Variables** (if needed)
   - No environment variables required for this static site

### Project Structure
```
├── Startup_Scientist_Guideline_Portal.html  # Main HTML file
├── images/                                   # All images and assets
├── render.yaml                              # Render configuration
└── README.md                               # This file
```

### Custom Domain Setup
After deployment, you can add a custom domain:
1. Go to your Render service settings
2. Add custom domain
3. Update DNS records as instructed by Render

### Performance Optimization
- Images are optimized for web
- CSS is minified and embedded
- Font Awesome icons loaded from CDN
- Lazy loading implemented for better performance

## Technologies Used
- HTML5
- CSS3 with modern features
- Font Awesome for icons
- Responsive grid layouts
- JavaScript for interactivity

## Support
For any issues or questions, please contact the development team.
