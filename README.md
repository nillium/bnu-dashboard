# BNU Dashboard

A beautiful, modern web dashboard with integrated AI chat interface.

## Features

- 📊 **Clean Dashboard Layout** - Grid-based interface with smooth animations
- 💬 **AI Chat Integration** - Powered by n8n webhook integration
- 🎨 **Modern Design** - Gradient backgrounds, glassmorphism effects
- 📱 **Responsive** - Works on desktop, tablet, and mobile devices
- ⚡ **Fast & Lightweight** - Pure HTML/CSS/JS, no build tools required

## Screenshots

### Main Dashboard
Beautiful grid layout with 9 customizable quick-access tiles.

### AI Chat Interface
Integrated chat interface with n8n backend support.

## Quick Start

### Local Setup

1. Clone the repository:
```bash
git clone https://github.com/nillium/bnu-dashboard.git
cd bnu-dashboard
```

2. Serve the files:
```bash
# Python 3
python -m http.server 8080

# Node.js
npx serve

# PHP
php -S localhost:8080
```

3. Open in browser:
```
http://localhost:8080
```

### Configuration

#### Customize Dashboard Links

Edit `index.html` and modify the href attributes in the grid:

```html
<a href="YOUR_LINK_HERE" class="box">
    <div class="icon">📊</div>
    <div class="label">Your Label</div>
</a>
```

#### Configure AI Chat

Edit `chat.html` and set your n8n webhook URL:

```javascript
createChat({
    webhookUrl: 'http://your-n8n-instance:5678/webhook/your-webhook-id/chat',
    // ... other options
});
```

## File Structure

```
bnu-dashboard/
├── index.html          # Main dashboard page
├── chat.html           # AI chat interface
└── README.md          # This file
```

## Customization

### Colors

The dashboard uses a purple gradient theme. To change colors, edit the CSS variables:

```css
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
```

### Icons

The dashboard uses emoji icons by default. You can replace them with:
- Font Awesome icons
- Material Icons
- Custom SVG icons

### Grid Layout

The dashboard uses a 3-column grid. To change:

```css
.grid {
    grid-template-columns: repeat(3, 1fr); /* Change 3 to desired columns */
}
```

## Integration Options

### n8n Webhook
The chat interface is designed to work with n8n workflows. Set up a webhook trigger in n8n and configure the URL in `chat.html`.

### Home Assistant
Link to your Home Assistant instance by updating the href:

```html
<a href="http://your-ha-instance:8123" class="box">
    <div class="icon">🏠</div>
    <div class="label">Home Assistant</div>
</a>
```

### Nextcloud/File Server
Link to your file management system:

```html
<a href="https://your-nextcloud/files" class="box">
    <div class="icon">📁</div>
    <div class="label">Files</div>
</a>
```

## Browser Support

- ✅ Chrome/Edge (90+)
- ✅ Firefox (88+)
- ✅ Safari (14+)
- ✅ Mobile browsers

## Technologies Used

- **HTML5** - Semantic markup
- **CSS3** - Modern styling with flexbox/grid
- **JavaScript (ES6+)** - Module imports
- **n8n Chat Widget** - AI chat integration

## License

MIT License - feel free to use and modify for your projects.

## Contributing

Contributions welcome! Feel free to:
- Report bugs
- Suggest features
- Submit pull requests

## Support

For issues or questions, please open a GitHub issue.
