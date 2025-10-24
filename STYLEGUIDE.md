# Career Transition Theme - Style Guide

This document outlines the design system and coding standards for the Career Transition Shopify theme.

## Color Palette

### Primary Colors
- **Primary Blue**: `#667eea`
- **Primary Purple**: `#764ba2`
- **Gradient**: `linear-gradient(135deg, #667eea 0%, #764ba2 100%)`

### Text Colors
- **Dark**: `#2d3748` (Headings, Body text)
- **Medium**: `#4a5568` (Secondary text)
- **Light**: `#a0aec0` (Tertiary text)
- **White**: `#ffffff` (Text on dark backgrounds)

### UI Colors
- **Success**: `#48bb78`
- **Warning**: `#ecc94b`
- **Error**: `#f56565`
- **Info**: `#4299e1`

## Typography

### Font Family
- **Primary**: System UI, -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif
- **Headings**: Same as primary (system font stack for performance)

### Font Sizes (Desktop)
- **H1**: 2.5rem (40px)
- **H2**: 2rem (32px)
- **H3**: 1.5rem (24px)
- **H4**: 1.25rem (20px)
- **Body**: 1rem (16px)
- **Small**: 0.875rem (14px)

### Line Height
- **Headings**: 1.2
- **Body**: 1.6
- **Buttons**: 1.5

## Spacing System

### Base Unit: 1rem (16px)
- **XXS**: 0.25rem (4px)
- **XS**: 0.5rem (8px)
- **S**: 1rem (16px)
- **M**: 1.5rem (24px)
- **L**: 2rem (32px)
- **XL**: 3rem (48px)
- **XXL**: 4rem (64px)
- **XXXL**: 6rem (96px)

## Breakpoints

- **Mobile**: Up to 749px
- **Tablet**: 750px - 989px
- **Desktop**: 990px and up

## Buttons

### Primary Button
```css
.button-primary {
  background: #667eea;
  color: white;
  padding: 1rem 2rem;
  border-radius: 50px;
  font-weight: 600;
  text-decoration: none;
  display: inline-block;
  transition: all 0.3s ease;
  border: none;
  cursor: pointer;
}

.button-primary:hover {
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(0,0,0,0.15);
}
```

### Secondary Button
```css
.button-secondary {
  background: transparent;
  color: #667eea;
  padding: 1rem 2rem;
  border-radius: 50px;
  font-weight: 600;
  text-decoration: none;
  display: inline-block;
  transition: all 0.3s ease;
  border: 2px solid #667eea;
  cursor: pointer;
}

.button-secondary:hover {
  background: rgba(102, 126, 234, 0.1);
}
```

## Cards

### Default Card
```css
.card {
  background: white;
  border-radius: 12px;
  box-shadow: 0 4px 20px rgba(0,0,0,0.08);
  padding: 2rem;
  transition: all 0.3s ease;
}

.card:hover {
  transform: translateY(-5px);
  box-shadow: 0 10px 30px rgba(0,0,0,0.12);
}
```

### Glass Card
```css
.glass-card {
  background: rgba(255, 255, 255, 0.15);
  backdrop-filter: blur(10px);
  border: 1px solid rgba(255, 255, 255, 0.2);
  border-radius: 16px;
  padding: 2.5rem;
  transition: all 0.3s ease;
}

.glass-card:hover {
  background: rgba(255, 255, 255, 0.2);
  transform: translateY(-5px);
}
```

## Forms

### Text Input
```css
.input {
  width: 100%;
  padding: 0.75rem 1rem;
  border: 1px solid #e2e8f0;
  border-radius: 6px;
  font-size: 1rem;
  transition: border-color 0.2s ease;
}

.input:focus {
  outline: none;
  border-color: #667eea;
  box-shadow: 0 0 0 3px rgba(102, 126, 234, 0.2);
}
```

## Animations

### Fade In
```css
@keyframes fadeIn {
  from { opacity: 0; }
  to { opacity: 1; }
}

.fade-in {
  animation: fadeIn 0.5s ease-out;
}
```

### Slide Up
```css
@keyframes slideUp {
  from { 
    opacity: 0;
    transform: translateY(20px);
  }
  to { 
    opacity: 1;
    transform: translateY(0);
  }
}

.slide-up {
  animation: slideUp 0.6s cubic-bezier(0.4, 0, 0.2, 1);
}
```

## Best Practices

### Accessibility
- Use semantic HTML5 elements
- Ensure proper color contrast (minimum 4.5:1 for normal text)
- Add proper ARIA labels and roles
- Ensure keyboard navigability
- Test with screen readers

### Performance
- Optimize images (WebP format with fallbacks)
- Lazy load images and iframes
- Minimize CSS and JavaScript
- Use system fonts for better performance
- Implement proper caching

### Browser Support
- Chrome (latest 2 versions)
- Firefox (latest 2 versions)
- Safari (latest 2 versions)
- Edge (latest 2 versions)
- Mobile Safari (iOS 12+)
- Chrome for Android

## Component Library

### Program Card
```html
<div class="program-card">
  <div class="program-badge">FLAGSHIP</div>
  <h3>Program Title</h3>
  <div class="program-price">$497</div>
  <p>Program description goes here.</p>
  <ul class="program-features">
    <li>Feature 1</li>
    <li>Feature 2</li>
  </ul>
  <a href="#" class="button button-primary">Learn More</a>
</div>
```

### Testimonial Card
```html
<div class="testimonial-card">
  <div class="testimonial-content">
    "Testimonial quote goes here."
  </div>
  <div class="testimonial-author">
    <div class="author-name">John Doe</div>
    <div class="author-title">Job Title</div>
  </div>
</div>
```

## Contributing

1. Create a new branch for your feature: `git checkout -b feature/your-feature`
2. Follow the style guide and coding standards
3. Test your changes across different devices and browsers
4. Submit a pull request with a clear description of your changes

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
