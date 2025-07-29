# SubjectPhoto - Professional Photography Website

A modern, responsive photography portfolio website built with HTML, CSS (Tailwind), and JavaScript. Features a complete admin panel for managing images and categories.

## 🌟 Features

### Frontend Features
- **Responsive Design**: Mobile-first approach with Tailwind CSS
- **Modern UI**: Clean, professional design with smooth animations
- **Image Gallery**: Dynamic gallery with filtering and search functionality
- **SEO Optimized**: Meta tags, structured data, and semantic HTML
- **Accessibility**: ARIA labels, keyboard navigation, and screen reader support
- **PWA Ready**: Service worker, manifest file, and offline support
- **Social Sharing**: Integrated sharing for major social platforms

### Admin Panel Features
- **Image Management**: Upload, delete, and organize images
- **Category Management**: Create and manage custom categories
- **Bulk Operations**: Select multiple images for batch operations
- **Data Export/Import**: Backup and restore functionality
- **File Validation**: Type and size validation for uploads
- **Real-time Updates**: Dynamic content updates without page refresh

### Technical Features
- **Client-side Storage**: Uses localStorage for data persistence
- **Image Optimization**: Lazy loading and responsive images
- **Error Handling**: Comprehensive error messages and validation
- **Performance**: Optimized loading and caching strategies

## 🚀 Quick Start

### Prerequisites
- A modern web browser
- A local web server (for development)

### Installation

1. **Clone or download** the project files
2. **Start a local server** in the project directory:

```bash
# Using Python 3
python -m http.server 8000

# Using Node.js (if you have http-server installed)
npx http-server

# Using PHP
php -S localhost:8000
```

3. **Open your browser** and navigate to `http://localhost:8000`

## 📁 File Structure

```
SubjectPhoto/
├── index.html              # Home page
├── gallery.html            # Image gallery
├── about.html              # About page
├── booking.html            # Booking system
├── secure-access.html      # Secure admin login
├── management-portal.html  # Admin dashboard
├── admin.html              # Legacy admin (redirects)
├── login.html              # Legacy login (redirects)
├── manifest.json           # PWA manifest
├── sw.js                  # Service worker
├── robots.txt             # Search engine protection
├── SECURITY.md            # Security documentation
├── README.md              # This file
└── DEPLOYMENT.md          # Deployment guide
```

## 🔐 Admin Access

### Secure Admin Panel

The website includes a comprehensive admin panel with enhanced security:

- **Gallery Management**: Upload, organize, and manage photos
- **About Page Editor**: Edit photographer information and social links
- **Booking Management**: View and manage booking requests
- **Data Export/Import**: Backup and restore website data
- **Availability Management**: Mark dates as unavailable

### Security Features

- **Obscure URLs**: Admin pages use non-obvious URLs
- **Session Management**: 30-minute timeout with auto-logout
- **Login Protection**: 5 failed attempts = 15-minute lockout
- **Search Engine Blocking**: Admin pages blocked from search engines
- **Hidden Navigation**: Admin links removed from public pages

### Access Instructions

1. Navigate directly to `/secure-access.html`
2. Use the provided credentials:
   - Username: `admin`
   - Password: `subjectphoto2024`
3. Monitor the session timer in the top-right corner
4. Use the logout button or wait for auto-logout

**Important**: Change the default credentials immediately for production use.

For detailed security information, see `SECURITY.md`.

## 🔧 Configuration

### Customizing Colors
The website uses a blue color scheme. To change colors, update the Tailwind configuration in each HTML file:

```javascript
tailwind.config = {
    theme: {
        extend: {
            colors: {
                'accent-blue': '#3b82f6',    // Primary blue
                'hover-blue': '#2563eb',     // Darker blue for hover
                'cool-white': '#f0f9ff',     // Light blue background
                // ... other colors
            }
        }
    }
}
```

### Adding Custom Categories
1. Log into the admin panel
2. Upload images and select "Custom Category"
3. Enter your category name
4. The category will be automatically added to the system

### SEO Configuration
Update the meta tags in each HTML file:

```html
<meta name="description" content="Your description here">
<meta property="og:title" content="Your title here">
<meta property="og:description" content="Your description here">
```

## 🎨 Customization

### Adding New Pages
1. Create a new HTML file
2. Copy the navigation structure from existing pages
3. Update the Tailwind configuration
4. Add the page to the service worker cache list

### Modifying Styles
The website uses Tailwind CSS classes. You can:
- Modify existing classes in the HTML
- Add custom CSS in `<style>` tags
- Override Tailwind utilities with custom classes

### Adding Features
The modular JavaScript structure makes it easy to add new features:
- Image editing capabilities
- Advanced filtering options
- User authentication
- Database integration

## 🔒 Security Considerations

### Current Implementation
- Client-side authentication (for demo purposes)
- localStorage for data storage
- No server-side validation

### Production Recommendations
- Implement server-side authentication
- Use a proper database (MySQL, PostgreSQL, MongoDB)
- Add CSRF protection
- Implement rate limiting
- Use HTTPS
- Add input sanitization

## 📱 PWA Features

The website includes Progressive Web App features:
- **Installable**: Can be added to home screen
- **Offline Support**: Basic offline functionality
- **App-like Experience**: Full-screen mode
- **Fast Loading**: Cached resources

## 🚀 Deployment

### GitHub Pages
1. Push code to GitHub repository
2. Enable GitHub Pages in repository settings
3. Select source branch (usually `main`)
4. Your site will be available at `https://username.github.io/repository-name`

### Traditional Hosting
1. Upload all files to your web server
2. Ensure the server supports HTML files
3. Update any absolute paths if needed
4. Test all functionality

### Vercel/Netlify
1. Connect your GitHub repository
2. Deploy automatically on push
3. Configure custom domain if needed

## 🐛 Troubleshooting

### Common Issues

**Images not loading**
- Check file paths
- Ensure images are in the correct format
- Verify file permissions

**Admin panel not working**
- Clear browser cache
- Check localStorage availability
- Verify JavaScript is enabled

**Mobile responsiveness issues**
- Test on different devices
- Check viewport meta tag
- Verify Tailwind responsive classes

### Browser Compatibility
- Chrome 60+
- Firefox 55+
- Safari 12+
- Edge 79+

## 📈 Performance Optimization

### Current Optimizations
- Lazy loading images
- Minified CSS (Tailwind)
- Optimized images
- Service worker caching

### Additional Recommendations
- Use WebP image format
- Implement image compression
- Add CDN for static assets
- Enable Gzip compression

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 🆘 Support

For support and questions:
- Check the troubleshooting section
- Review the code comments
- Open an issue on GitHub

## 🔄 Version History

### v1.0.0
- Initial release
- Complete admin panel
- Responsive design
- PWA features
- SEO optimization

---

**Built with ❤️ using HTML, CSS, and JavaScript** 