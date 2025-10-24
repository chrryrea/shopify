# Career Transition Theme

A Shopify theme designed for mid-career professionals seeking guidance through career transitions. Built on Shopify Dawn with custom sections for career coaching services.

## 🚀 Features

### Core Sections
- **Hero Section** - Engaging headline with clear call-to-action
- **Career Benefits** - Key value propositions with icons
- **Program Offerings** - Four-tiered service packages
- **Success Stories** - Social proof with testimonials
- **About Guide** - Credentials and approach
- **FAQ** - Common questions and concerns

### Technical Highlights
- **Responsive Design** - Mobile-first approach
- **Performance Optimized** - Fast loading times
- **Customizable** - Easy to update through theme editor
- **SEO Friendly** - Structured data and semantic HTML

## 🛠 Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/chrryrea/shopify.git
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Connect to your Shopify store**
   ```bash
   shopify theme dev --store your-store.myshopify.com
   ```

4. **Start development server**
   ```bash
   npm run dev
   ```

## 🎨 Theme Customization

### Theme Settings
- **Colors**: Update brand colors in `config/settings_schema.json`
- **Typography**: Customize fonts in `assets/theme.css`
- **Sections**: Reorder or disable sections via theme customizer

### Custom Sections
1. **Program Offerings**
   - Located in `sections/program-offerings.liquid`
   - Configure pricing, features, and CTAs

2. **Career Benefits**
   - Located in `sections/career-benefits.liquid`
   - Customize benefits and icons

3. **Success Stories**
   - Located in `sections/peer-success-stories.liquid`
   - Add/update testimonials

## 📱 Responsive Breakpoints
- Mobile: < 750px
- Tablet: 750px - 989px
- Desktop: 990px+

## 🧪 Testing

### Browser Support
- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

### Performance
- Lighthouse score: 95+
- Mobile-first responsive design
- Optimized images and assets

## 📝 Documentation

### Code Structure
```
themes/
├── assets/           # CSS, JS, and images
├── config/           # Theme settings
├── layout/           # Theme templates
├── sections/         # Custom sections
├── snippets/         # Reusable components
└── templates/        # Page templates
```

### Dependencies
- Shopify CLI
- Node.js 14+
- npm 6+

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Built on Shopify Dawn theme
- Icons from Font Awesome
- Inspired by career coaching best practices
