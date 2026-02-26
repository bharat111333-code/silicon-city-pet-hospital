# Silicon City Pet Hospital - Website Template

A complete, professional veterinary hospital website template built with HTML, CSS, and JavaScript. Designed to be easily adapted for Wix or used as a standalone website.

## 📁 Project Structure

```
silicon-city-pet-hospital/
├── index.html          # Home page
├── services.html       # Services overview
├── about.html          # About the hospital
├── team.html           # Team members
├── contact.html        # Contact form & info
├── css/
│   └── style.css       # Complete styling
├── js/
│   └── script.js       # JavaScript functionality
└── WIX_VELO_CODE.js    # Wix-specific code
```

## ✨ Features

### General Features
- 🏥 Professional hospital branding
- 📱 Fully responsive design (mobile, tablet, desktop)
- 🎨 Modern UI with smooth animations
- ⏰ 24/7 emergency contact display
- 🔍 SEO-friendly structure
- ♿ Accessible navigation

### Functionality
- **Form Validation**: Contact form with real-time validation
- **Phone Formatting**: Auto-formats phone numbers as `(555) 123-4567`
- **Smooth Scrolling**: Navigation links scroll smoothly to sections
- **Scroll Animations**: Cards animate in when scrolled into view
- **Button Ripple Effect**: Interactive button animations
- **Mobile Menu**: Hamburger menu for small screens
- **Active Navigation**: Highlights current page in navigation
- **Scroll-to-Top Button**: Appears when scrolled down the page

## 🌐 Pages

### Home (index.html)
- Hero section with call-to-action
- Emergency services alert
- Why choose us section
- Services showcase
- Testimonials
- Call-to-action section

### Services (services.html)
- Detailed service descriptions
- 8 key services with features:
  - General Checkup & Wellness
  - Vaccinations & Immunizations
  - Dental Care
  - Surgery & Spaying/Neutering
  - Laboratory & Diagnostic Testing
  - Emergency & Critical Care
  - Digital Imaging
  - Pharmacy & Medications

### About (about.html)
- Hospital story
- Mission, vision, and values
- Why we're different
- Community involvement

### Team (team.html)
- 8 team member profiles
- Professional credentials
- Specialties
- Credentials & affiliations

### Contact (contact.html)
- Contact form with validation
- Business hours
- Multiple contact options
- Social media links
- Map placeholder

## 🛠️ Setup Instructions

### Option 1: Use Locally (Standalone Website)
1. Download all files
2. Open `index.html` in a web browser
3. All features work immediately

### Option 2: Use on Wix

#### Step 1: Create Forms
In your Wix Editor, create a contact form with these input field IDs:
- `nameInput` (Text input)
- `emailInput` (Email input)
- `phoneInput` (Phone input)
- `petNameInput` (Text input)
- `subjectInput` (Text input)
- `messageInput` (Text area)
- Add a text element for `validationMessage`

#### Step 2: Add Navigation
Create navigation links in the Wix editor with IDs:
- `navHome` → Link to Home
- `navServices` → Link to Services
- `navAbout` → Link to About
- `navTeam` → Link to Team
- `navContact` → Link to Contact

#### Step 3: Add JavaScript
1. Open your Wix site in **Dev Mode**
2. Go to **Code Files**
3. Copy code from `WIX_VELO_CODE.js`
4. Create a new `.jsw` file or add to your page code

#### Step 4: Connect Phone Formatting
In your phone input element:
1. Select the element
2. Go to **Events**
3. Add `onInput` event
4. Select `formatPhoneNumber` function from the dropdown

#### Step 5: Connect Form Submission
1. Select your submit button
2. Go to **Events**
3. Add `onClick` event
4. Select `contactFormSubmit_click` function

## 📱 Customization

### Change Colors
Edit the CSS variables in `style.css`:
```css
:root {
    --primary-color: #2E7D32;        /* Green */
    --secondary-color: #1976D2;      /* Blue */
    --accent-color: #FF6F00;         /* Orange */
    /* ... more colors ... */
}
```

### Update Contact Information
Replace placeholder info in:
- `index.html` - Emergency number
- `contact.html` - Address, phone, email
- `footer` (all pages) - Contact details

### Add Team Members
Duplicate team member cards in `team.html`:
```html
<div class="team-member">
    <div class="team-member-avatar">🧑‍⚕️</div>
    <h3>Dr. Name, Credentials</h3>
    <p class="team-role">Position</p>
    <p class="team-bio">Bio text...</p>
</div>
```

### Modify Services
Edit service cards in `services.html`:
```html
<div class="service-card">
    <div class="service-icon">🐕</div>
    <h3>Service Name</h3>
    <p>Description</p>
</div>
```

## 🔧 JavaScript Functions

### Form Validation
```javascript
// Validates name, email, subject, and message
// Shows alerts for invalid inputs
contactForm.addEventListener('submit', validateForm);
```

### Phone Formatting
```javascript
// Auto-formats: 5551234567 → (555) 123-4567
formatPhoneNumber(phoneInput);
```

### Smooth Scrolling
```javascript
// Smooth scroll to section when nav link clicked
document.querySelectorAll('a[href^="#"]').forEach(anchor => {
    anchor.addEventListener('click', scrollToTarget);
});
```

### Scroll Animations
```javascript
// Elements fade in and slide up when scrolled into view
observeElements();
```

### Mobile Menu
```javascript
// Toggle mobile menu on hamburger click
toggleMobileMenu();
```

## 📧 Form Submission

Currently, the form logs data to browser console. To store submissions:

### For Wix:
Use Wix Collections or Wix Backend functions:
```javascript
import { insertItem } from 'wix-data';

export async function submitForm(data) {
    await insertItem('ContactSubmissions', data);
}
```

### For Standalone:
Use a backend service like:
- Formspree
- EmailJS
- Firebase
- Your own backend

## 🎨 Design Highlights

- **Color Scheme**: Professional green (veterinary) + blue (trust)
- **Typography**: Clean, modern sans-serif fonts
- **Spacing**: Generous whitespace for readability
- **Shadows**: Subtle shadows for depth
- **Animations**: Smooth, not distraction
- **Responsive**: Mobile-first approach

## 📊 Performance

- Lightweight CSS (no frameworks)
- Minimal JavaScript (no dependencies)
- Optimized images (emoji icons reduce file size)
- Fast load times
- SEO-friendly structure

## 🔐 Security Notes

- Form validation on client-side (add server-side validation too)
- No sensitive data stored in JavaScript
- Consider HTTPS for production
- Validate all user inputs on backend

## 📋 Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Chrome Android)

## 🚀 Deployment

### For Wix
1. Import this template's design
2. Use WIX_VELO_CODE.js for functionality
3. Connect to Wix backend services
4. Test all forms and navigation
5. Publish site

### For Standalone Hosting
1. Upload all files to hosting service
2. Set `index.html` as home page
3. Keep directory structure intact
4. Test on different devices
5. Monitor console for errors

## 📞 Contact Information

**Silicon City Pet Hospital**
- 📍 2550 Tech Drive, Silicon Valley, CA 95051
- 📞 +1 (408) 555-7890 (Emergency 24/7)
- 📧 info@siliconpethospital.com

## 📄 License

This template is provided as-is for commercial use.

## 🤝 Support

For issues or questions:
1. Check browser console for errors
2. Verify all IDs match in HTML and JavaScript
3. Test on different browsers
4. Clear cache and reload

---

**Last Updated**: February 2026
**Version**: 1.0

