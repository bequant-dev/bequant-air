# BeQuant Discourse Theme

A modern, clean Discourse theme customized for BeQuant with Material Design colors and enhanced user experience.

## Features

### 🎨 **Material Design 3 Color Palette**
- **Light Mode**: Clean, professional light theme with Material Blue accents
- **Dark Mode**: Elegant dark theme with proper contrast and readability
- **Consistent Branding**: BeQuant colors throughout the interface

### 🌓 **Theme Toggle**
- **Floating Toggle Button**: Easy access theme switcher in the top-right corner
- **Smooth Transitions**: Beautiful animations between light and dark modes
- **Persistent Settings**: Remembers user's theme preference

### 🎯 **Enhanced User Experience**
- **Modern Styling**: Rounded corners, subtle shadows, and smooth animations
- **Better Typography**: Improved readability and visual hierarchy
- **Responsive Design**: Works perfectly on all device sizes
- **Accessibility**: WCAG compliant color contrasts

### 🔧 **Built-in Components**
- **Dark/Light Scheme Toggle**: Seamless theme switching
- **Clickable Topics**: Enhanced topic interaction
- **Discourse Loading Slider**: Smooth loading animations
- **Discourse Search Banner**: Modern search experience
- **Modern Category + Group Boxes**: Beautiful category organization

## Installation

### Method 1: GitHub Repository (Recommended)

1. **Fork this repository** to your GitHub account
2. **Update the repository URL** in `about.json` to point to your fork
3. **In your Discourse admin panel**:
   - Go to **Admin** → **Customize** → **Themes**
   - Click **Install** → **From a git repository**
   - Enter your repository URL: `https://github.com/your-username/bequant-air`
   - Click **Install**

### Method 2: Manual Installation

1. **Download the theme files**
2. **Upload to your Discourse server** in the `themes/` directory
3. **Enable the theme** in your admin panel

## Configuration

### Color Schemes

The theme includes two color schemes:

#### BeQuant Light
- **Primary**: Material Grey 900 (`#212121`)
- **Secondary**: Material Grey 50 (`#fafafa`)
- **Tertiary**: Material Blue 700 (`#1976d2`)
- **Header**: Clean white background with blue accents

#### BeQuant Dark
- **Primary**: Material Grey 50 (`#f9fafb`)
- **Secondary**: Material Grey 950 (`#0f172a`)
- **Tertiary**: Material Teal 400 (`#38bdf8`)
- **Header**: Dark slate background with teal accents

### Required Settings

1. **Enable Color Schemes**: 
   - Go to **Admin** → **Customize** → **Colors**
   - Enable both "BeQuant Light" and "BeQuant Dark"
   - Check "Color scheme can be selected by users" for both

2. **Theme Components**:
   - The theme automatically includes modern category boxes
   - Search banner component is pre-configured
   - Clickable topics are enabled by default

## Customization

### Adding Your Own Colors

To customize the colors further, edit the `about.json` file:

```json
"color_schemes": {
  "bequant-light": {
    "primary": "your-primary-color",
    "secondary": "your-secondary-color",
    "tertiary": "your-accent-color"
  }
}
```

### Modifying the Theme Toggle

The theme toggle is located in `common/header.html`. You can:
- Change the position by modifying the CSS in `common/common.scss`
- Update the icons by replacing the SVG elements
- Modify the animation behavior in the JavaScript section

### Styling Enhancements

All custom styling is in `common/common.scss`. Key sections:
- **Theme Toggle**: Lines 645-700
- **BeQuant Branding**: Lines 702-710
- **Material Design Buttons**: Lines 712-730
- **Enhanced Forms**: Lines 732-740
- **Card Styling**: Lines 742-750

## Browser Support

- **Chrome**: 90+
- **Firefox**: 88+
- **Safari**: 14+
- **Edge**: 90+

## Development

### Prerequisites
- Node.js 16+
- Ruby 2.7+
- Discourse development environment

### Setup
```bash
# Clone the repository
git clone https://github.com/your-username/bequant-air.git
cd bequant-air

# Install dependencies
npm install

# Build the theme
npm run build
```

### Making Changes
1. **SCSS Changes**: Edit files in `scss/` and `common/`
2. **JavaScript**: Modify the script in `common/header.html`
3. **Colors**: Update `about.json` color schemes
4. **Test**: Use Discourse's theme development tools

## Troubleshooting

### Theme Not Loading
- Check that all files are properly uploaded
- Verify the repository URL in admin panel
- Check Discourse logs for errors

### Theme Toggle Not Working
- Ensure both color schemes are enabled
- Check browser console for JavaScript errors
- Verify localStorage is enabled

### Styling Issues
- Clear browser cache
- Check for CSS conflicts with other themes
- Verify SCSS compilation

## Contributing

1. **Fork the repository**
2. **Create a feature branch**: `git checkout -b feature/amazing-feature`
3. **Commit your changes**: `git commit -m 'Add amazing feature'`
4. **Push to the branch**: `git push origin feature/amazing-feature`
5. **Open a Pull Request**

## License

This theme is based on the [discourse-air theme](https://github.com/discourse/discourse-air) and is licensed under the GPL-2.0 license.

## Support

For support and questions:
- **GitHub Issues**: Create an issue in this repository
- **BeQuant Support**: Contact support@bequant.dev
- **Discourse Community**: Ask in the [Discourse Meta](https://meta.discourse.org/) community

## Credits

- **Original Theme**: [discourse-air](https://github.com/discourse/discourse-air) by Jordan Vidrine
- **Material Design**: Google's Material Design 3 system
- **Icons**: Feather Icons
- **Customization**: BeQuant Team

---

**Made with ❤️ for the BeQuant community** 