# 🚀 Mike DiMaria Landing - Development Workflow Guide

## **🎯 Project Overview**
This guide establishes a reliable development workflow for Mike DiMaria's personal website - a static site hosted on GitHub Pages with comprehensive change tracking and user-controlled deployment.

## **🎯 Core Philosophy**
- **User-controlled development** - AI waits for explicit "let's go live" approval
- **Code synchronization** - Local = Git = Live Site always in sync
- **Comprehensive documentation** - Every change documented in changelog
- **Quality gates** - Test locally before any deployment

## **🚀 3-Phase Development Process**

### **Phase 1: Development & Testing**
1. Make changes locally
2. Test locally (with user approval)
3. Wait for user "let's go live" signal

### **Phase 2: GitHub Update**
4. Commit to git with descriptive message
5. Update CHANGELOG.md with:
   - Correct current date
   - Accurate summary of changes
   - Ask user questions if unclear about what to include
6. Push to GitHub

### **Phase 3: Live Deployment**
7. Deploy to live site after GitHub is updated

## **📝 Changelog Requirements**
- **Every commit must include changelog updates**
- Use correct current date for all entries
- Accurately summarize changes made in the commit
- Ask user questions if unclear about what to include
- Document all user-approved changes going live
- Maintain chronological order with newest entries at top

## **🔄 Code Synchronization Rules**
- **Local = Git = Live Site** must always be synchronized
- **No direct deployment** without git commit first
- **Proper version control** with meaningful commit messages
- **Clear deployment history** of what went live when

## **✅ Pre-Deployment Checklist**
1. All tests passing locally
2. Production build succeeds (if applicable)
3. No console errors in development
4. All new features tested locally
5. Linting passes (no errors)
6. Changelog updated with current date and accurate changes
7. User approval received for deployment

## **🔄 Development Workflow**

### **Local Development Setup**

#### **1. Local Server**
```bash
# Start local development server
python -m http.server 8000

# Alternative: Using Node.js (if available)
npx serve .

# Alternative: Using PHP (if available)
php -S localhost:8000
```

#### **2. Development Commands**
```bash
# Navigate to project directory
cd /Users/mikedimaria/mike-dimaria-landing

# Start local server
python -m http.server 8000

# Open in browser
open http://localhost:8000
```

#### **3. File Structure**
```
mike-dimaria-landing/
├── index.html          # Home page
├── about.html          # About page
├── approach.html       # Approach page
├── work.html           # Work page
├── styles.css          # Main stylesheet
├── styles-preview.css  # Preview-specific styles
├── profile-photo.jpg   # Profile image
├── favicon.ico         # Favicon
├── favicon.svg         # SVG favicon
├── create-favicon.js   # Favicon generator
├── favicon-generator.html # Favicon tool
├── preview.html        # Preview page
├── README.md           # Project documentation
├── DEVELOPMENT.md      # This workflow guide
└── LICENSE             # License file
```

### **Development Process**

#### **1. Feature Development**
- **Direct file editing**: Edit HTML/CSS/JS files directly
- **Immediate testing**: Refresh browser to see changes
- **No build process**: Static files work immediately
- **Version control**: Use Git for tracking changes

#### **2. Code Quality**
```bash
# Validate HTML
# Use browser developer tools or online validators

# Validate CSS
# Use browser developer tools or online validators

# Check for broken links
# Test all navigation links manually
```

#### **3. Testing Checklist**
- [ ] **Cross-browser testing**: Chrome, Firefox, Safari, Edge
- [ ] **Mobile responsiveness**: Test on actual devices
- [ ] **Performance**: Page load times under 3 seconds
- [ ] **Accessibility**: Screen reader compatibility
- [ ] **SEO**: Meta tags, alt text, semantic HTML
- [ ] **Links**: All navigation and external links work
- [ ] **Images**: All images load properly
- [ ] **Forms**: Contact forms function correctly

## **🚀 Deployment Process**

### **GitHub + Cloudflare Pages Setup**

#### **1. Repository Management**
```bash
# Initialize Git (if not already done)
git init

# Add all files
git add .

# Commit changes
git commit -m "Update: [describe changes]"

# Push to GitHub
git push origin main
```

#### **2. Cloudflare Pages Configuration**
- **Build settings**: No build command needed
- **Build output directory**: `/` (root)
- **Environment variables**: None required
- **Custom domain**: Configure in Cloudflare DNS

#### **3. Deployment Commands**
```bash
# Deploy via Git push
git add .
git commit -m "Deploy: [feature description]"
git push origin main

# Cloudflare Pages will automatically deploy
# Check deployment status at: https://dash.cloudflare.com
```

### **Domain & DNS Management**

#### **1. Cloudflare DNS Settings**
- **A Record**: Point to Cloudflare Pages IP
- **CNAME**: www → your-domain.com
- **SSL/TLS**: Full (strict) encryption
- **Page Rules**: Configure as needed

#### **2. SSL Certificate**
- **Automatic**: Cloudflare provides free SSL
- **Always Use HTTPS**: Enable in Cloudflare settings
- **HSTS**: Enable for security headers

## **🧪 Testing Strategy**

### **Pre-Deployment Testing**

#### **1. Local Testing**
```bash
# Start local server
python -m http.server 8000

# Test in multiple browsers
open http://localhost:8000
# Test in Chrome, Firefox, Safari, Edge
```

#### **2. Mobile Testing**
- **Device testing**: Test on actual phones/tablets
- **Responsive design**: Check all breakpoints
- **Touch interactions**: Verify tap targets
- [ ] **Performance**: Test on slower connections

#### **3. Performance Testing**
- **PageSpeed Insights**: Google's tool
- **Lighthouse**: Chrome DevTools
- **WebPageTest**: Detailed performance analysis
- **GTmetrix**: Performance monitoring

### **Post-Deployment Testing**

#### **1. Live Site Validation**
- [ ] **Homepage loads**: All content displays correctly
- [ ] **Navigation works**: All pages accessible
- [ ] **Images load**: No broken image links
- [ ] **Contact forms**: Email functionality works
- [ ] **Mobile responsive**: Works on all devices
- [ ] **SSL certificate**: HTTPS works properly
- [ ] **Domain redirects**: www and non-www work

#### **2. Cross-Browser Testing**
- **Chrome**: Latest version
- **Firefox**: Latest version
- **Safari**: Latest version
- **Edge**: Latest version
- **Mobile browsers**: iOS Safari, Chrome Mobile

## **🔧 Key Differences from React Projects**

| Aspect | React (BFL) | Static Site (Personal Website) |
|--------|-------------|--------------------------------|
| **Local Dev** | `npm run dev` | `python -m http.server 8000` |
| **Build Process** | `npm run build` | No build needed |
| **File Changes** | Hot reload | Manual browser refresh |
| **Dependencies** | package.json | None (CDN for fonts) |
| **Deployment** | Firebase Hosting | Cloudflare Pages |
| **Testing** | Component testing | Browser testing |
| **Validation** | TypeScript compilation | HTML/CSS validation |
| **State Management** | React state | No state needed |
| **Routing** | React Router | Static HTML pages |

## **📋 Pre-Launch Checklist**

### **Technical Requirements**
- [ ] **HTML validation**: No errors or warnings
- [ ] **CSS validation**: All styles load correctly
- [ ] **JavaScript**: No console errors
- [ ] **Images optimized**: Compressed and web-ready
- [ ] **Favicon**: Multiple sizes and formats
- [ ] **Meta tags**: SEO and social media ready
- [ ] **Robots.txt**: Search engine crawling
- [ ] **Sitemap**: XML sitemap for SEO

### **Content Requirements**
- [ ] **Copy review**: All text is accurate and current
- [ ] **Image alt text**: Descriptive alt attributes
- [ ] **Contact information**: Email and links work
- [ ] **Professional photos**: High-quality images
- [ ] **Brand consistency**: Colors and fonts match
- [ ] **Legal pages**: Privacy policy if needed

### **Performance Requirements**
- [ ] **Page load time**: Under 3 seconds
- [ ] **Image optimization**: WebP format where possible
- [ ] **Minification**: CSS and JS minified
- [ ] **Caching**: Browser caching configured
- [ ] **CDN**: Cloudflare CDN enabled
- [ ] **Compression**: Gzip compression enabled

## **🚨 Common Issues & Solutions**

### **Local Development Issues**
```bash
# Port already in use
python -m http.server 8001

# Permission denied
sudo python -m http.server 8000

# File not found
# Check file paths and case sensitivity
```

### **Deployment Issues**
- **Build failures**: Not applicable (no build process)
- **Domain issues**: Check Cloudflare DNS settings
- **SSL issues**: Verify Cloudflare SSL settings
- **Cache issues**: Clear Cloudflare cache

### **Performance Issues**
- **Slow loading**: Optimize images and minify CSS
- **Mobile issues**: Test responsive breakpoints
- **Browser compatibility**: Test in multiple browsers

## **📊 Monitoring & Maintenance**

### **Regular Checks**
- **Weekly**: Test all pages and forms
- **Monthly**: Check performance metrics
- **Quarterly**: Update content and images
- **Annually**: Review and refresh design

### **Analytics Setup**
- **Google Analytics**: Track visitor behavior
- **Cloudflare Analytics**: Performance monitoring
- **Search Console**: SEO performance

## **🎯 Success Metrics**

### **Performance Targets**
- **Page load time**: < 3 seconds
- **Mobile performance**: 90+ Lighthouse score
- **Accessibility**: WCAG 2.1 AA compliance
- **SEO**: 90+ Lighthouse SEO score

### **User Experience**
- **Navigation**: All pages accessible in 2 clicks
- **Contact**: Email links work immediately
- **Mobile**: Perfect experience on all devices
- **Cross-browser**: Consistent experience

## **🔄 Workflow Summary**

### **Daily Development**
1. **Start local server**: `python -m http.server 8000`
2. **Edit files**: HTML, CSS, JS as needed
3. **Test changes**: Refresh browser to verify
4. **Commit changes**: `git add . && git commit -m "Update: description"`
5. **Push to GitHub**: `git push origin main`

### **Feature Completion**
1. **Local testing**: Test all functionality
2. **Cross-browser testing**: Verify in all browsers
3. **Mobile testing**: Test on actual devices
4. **Performance check**: Run Lighthouse audit
5. **Deploy**: Push to GitHub (auto-deploys to Cloudflare)
6. **Live testing**: Verify on production site

### **Pre-Launch Process**
1. **Complete checklist**: All items checked off
2. **Final testing**: Comprehensive testing suite
3. **Performance audit**: Optimize if needed
4. **Content review**: Final content approval
5. **Launch**: Deploy to production
6. **Post-launch**: Monitor and address any issues

---

## **📞 Support & Resources**

### **Useful Commands**
```bash
# Quick local development
cd /Users/mikedimaria/mike-dimaria-landing && python -m http.server 8000

# Git workflow
git status
git add .
git commit -m "Update: [description]"
git push origin main

# File validation
# Use browser developer tools for HTML/CSS validation
```

### **Important URLs**
- **Local development**: http://localhost:8000
- **GitHub repository**: [Your GitHub repo URL]
- **Cloudflare dashboard**: https://dash.cloudflare.com
- **Live site**: [Your domain URL]

### **Tools & Resources**
- **HTML Validator**: https://validator.w3.org
- **CSS Validator**: https://jigsaw.w3.org/css-validator
- **PageSpeed Insights**: https://pagespeed.web.dev
- **Lighthouse**: Chrome DevTools
- **GTmetrix**: https://gtmetrix.com

---

**Last Updated**: January 2025  
**Version**: 1.0  
**Maintainer**: Mike DiMaria  
**Project**: Personal Website - Cloudflare Pages

