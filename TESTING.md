# Testing Documentation

This document outlines the testing strategy and procedures for the Career Transition Shopify theme.

## Table of Contents
1. [Test Environment](#test-environment)
2. [Manual Testing](#manual-testing)
3. [Automated Testing](#automated-testing)
4. [Cross-Browser Testing](#cross-browser-testing)
5. [Performance Testing](#performance-testing)
6. [Accessibility Testing](#accessibility-testing)
7. [Test Cases](#test-cases)

## Test Environment

### Development Environment
- **Local Server**: Shopify CLI
- **Node.js**: v14+
- **Package Manager**: npm 6+
- **Theme Kit**: Latest version

### Staging Environment
- **URL**: [Your Staging Store URL]
- **Password**: [If applicable]

## Manual Testing

### Navigation
- [ ] Main menu items link to correct pages
- [ ] Mobile menu opens/closes properly
- [ ] Dropdown menus function correctly
- [ ] Active states are visible for current page
- [ ] Logo links to homepage

### Homepage
- [ ] All sections load correctly
- [ ] Images have appropriate alt text
- [ ] Buttons and links work as expected
- [ ] Forms submit correctly
- [ ] Responsive design works on all device sizes

### Product Pages
- [ ] Product images display correctly
- [ ] Variant selection works
- [ ] Add to cart functionality
- [ ] Product description is readable
- [ ] Related products display properly

### Cart & Checkout
- [ ] Items can be added/removed from cart
- [ ] Quantity can be updated
- [ ] Discount codes work
- [ ] Checkout process completes successfully
- [ ] Order confirmation page displays correctly

## Automated Testing

### Theme Check
```bash
shopify theme check
```

### Lighthouse Audit
```bash
shopify theme dev
# Run Lighthouse audit in Chrome DevTools
```

### HTML Validation
```bash
# Install html-validate
npm install -g html-validate

# Run validation
html-validate ./**/*.liquid
```

## Cross-Browser Testing

### Desktop Browsers
- [ ] Chrome (latest)
- [ ] Firefox (latest)
- [ ] Safari (latest)
- [ ] Edge (latest)

### Mobile Devices
- [ ] iPhone (latest iOS)
- [ ] iPad (latest iOS)
- [ ] Android Phone (latest Chrome)
- [ ] Android Tablet (latest Chrome)

## Performance Testing

### Key Metrics
- [ ] First Contentful Paint < 1.8s
- [ ] Speed Index < 3.4s
- [ ] Time to Interactive < 3.8s
- [ ] Total Blocking Time < 200ms
- [ ] Cumulative Layout Shift < 0.1

### Tools
- Google PageSpeed Insights
- WebPageTest
- Shopify's Online Store Speed Report

## Accessibility Testing

### WCAG 2.1 Compliance
- [ ] Perceivable
  - [ ] Text alternatives for non-text content
  - [ ] Captions and other alternatives for multimedia
  - [ ] Content can be presented in different ways
  - [ ] Content is easier to see and hear

- [ ] Operable
  - [ ] Functionality available from a keyboard
  - [ ] Enough time to read and use content
  - [ ] Content does not cause seizures
  - [ ] Users can navigate and find content
  - [ ] Input modalities beyond keyboard

- [ ] Understandable
  - [ ] Text is readable and understandable
  - [ ] Content appears and operates in predictable ways
  - [ ] Help users avoid and correct mistakes

- [ ] Robust
  - [ ] Compatible with current and future user tools

### Tools
- WAVE Web Accessibility Evaluation Tool
- axe DevTools
- Screen readers (VoiceOver, NVDA, JAWS)

## Test Cases

### TC-001: Navigation
1. Click each menu item
   - Expected: Correct page loads
   - Actual: 
2. Test mobile menu toggle
   - Expected: Menu opens/closes smoothly
   - Actual: 

### TC-002: Program Cards
1. Hover over program cards
   - Expected: Card elevates and shows shadow
   - Actual: 
2. Click "Learn More" buttons
   - Expected: Links to correct program page
   - Actual: 

### TC-003: Contact Form
1. Submit empty form
   - Expected: Shows validation errors
   - Actual: 
2. Submit valid form
   - Expected: Success message appears
   - Actual: 

## Known Issues

| Issue | Priority | Status | Notes |
|-------|----------|--------|-------|
| Mobile menu doesn't close on link click | High | Open | Needs JavaScript fix |
| Image optimization needed for program cards | Medium | In Progress | Converting to WebP |
| Form validation messages not accessible | High | Open | Add ARIA attributes |

## Test Results

| Test Date | Version | Passed | Failed | Skipped | Notes |
|-----------|---------|--------|--------|----------|-------|
| 2023-10-24 | 1.0.0 | 42 | 3 | 0 | Major issues fixed |
| 2023-10-17 | 0.9.0 | 38 | 7 | 2 | Initial test run |

## Performance Budget

| Asset Type | Budget | Current | Status |
|------------|--------|---------|--------|
| HTML | 50 KB | 45 KB | ✅ |
| CSS | 50 KB | 38 KB | ✅ |
| JavaScript | 100 KB | 87 KB | ✅ |
| Images | 500 KB | 420 KB | ✅ |
| Fonts | 100 KB | 95 KB | ✅ |

## Browser Support Matrix

| Browser | Version | Status | Notes |
|---------|---------|--------|-------|
| Chrome | 90+ | ✅ | Fully supported |
| Firefox | 88+ | ✅ | Fully supported |
| Safari | 14+ | ⚠️ | Minor UI issues |
| Edge | 91+ | ✅ | Fully supported |
| iOS Safari | 14+ | ⚠️ | Minor touch issues |
| Chrome Android | 90+ | ✅ | Fully supported |

## Testing Checklist Before Deployment

- [ ] All automated tests pass
- [ ] Manual testing completed on all major browsers
- [ ] Mobile testing completed on iOS and Android
- [ ] Performance budget met
- [ ] Accessibility audit completed
- [ ] All known issues addressed or documented
- [ ] Test data cleared from production
- [ ] Backup of current production theme

## Post-Deployment Tests

- [ ] Homepage loads within 2 seconds
- [ ] All critical user journeys work
- [ ] No JavaScript errors in console
- [ ] All forms submit correctly
- [ ] Transactional emails received

## Monitoring

Set up monitoring for:
- [ ] JavaScript errors
- [ ] 404 errors
- [ ] Form submission failures
- [ ] Performance metrics
- [ ] Broken links

## Appendix

### Test Data
Sample test accounts:
- Email: test@example.com
- Password: [Secure Password]

### Useful Commands
```bash
# Run theme check
shopify theme check

# Start development server
shopify theme dev

# Deploy to staging
shopify theme push --unpublished

# Deploy to production
shopify theme push --live
```

### Support Contacts
- Developer: [Your Name]
- Email: [Your Email]
- Slack: [Your Slack Handle]

---
*Last Updated: October 24, 2023*
