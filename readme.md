# Router Login Website

A simple, automatic router detection and redirection website that helps users find and connect to their router's login page.

## Features

- **Auto-Detection**: Automatically scans common router IP addresses
- **Smart Prioritization**: Tests most common router IPs first
- **Manual Fallback**: Provides clickable options if auto-detection fails
- **Mobile Responsive**: Works on all devices and screen sizes
- **Modern UI**: Clean, professional interface with smooth animations
- **Comprehensive Help**: Built-in troubleshooting guidance

## How It Works

1. **Priority-Based Scanning**: Tests router IPs in order of probability
2. **Iframe Detection**: Uses hidden iframes to test router connectivity
3. **CORS Handling**: Treats cross-origin blocks as successful detections
4. **Automatic Redirect**: Immediately redirects to detected router
5. **Graceful Fallback**: Shows manual selection if no router found

## Supported Routers

The website detects routers from these manufacturers:
- Netgear, Linksys, D-Link, ASUS
- Belkin, SMC, Motorola, Buffalo
- Apple AirPort, Xfinity, Huawei
- AT&T, Thomson, Microsoft
- T-Mobile, Sprint, Verizon FiOS
- Netgear Orbi, Eero

## Files Included

- `index.html` - Main website file (complete, standalone)
- `robots.txt` - Search engine directives
- `llms.txt` - AI assistant directives
- `.htaccess` - Apache server configuration
- `sitemap.xml` - XML sitemap for search engines
- `apple-touch-icon.svg` - SVG icon for site icon
- `readme.md` - This documentation

## Installation

1. Upload all files to your web server
2. Ensure your domain points to the directory
3. Configure SSL certificate (recommended)
4. Update `.htaccess` if needed for your server setup
5. Update domain references in `robots.txt` and `sitemap.xml`

## Customization

### Adding More Router IPs
Edit the `commonRouterIPs` array in `index.html`:

```javascript
{ ip: '192.168.x.x', brands: 'Brand Names', priority: 1-4 }
```

### Changing Colors/Styling
Modify the CSS variables in the `<style>` section of `index.html`.

### Adjusting Detection Speed
Change these values in the JavaScript:
- `maxConcurrent`: Number of simultaneous tests (default: 4)
- Timeout values in `tryRouterIP` function (default: 3000ms)

## Browser Compatibility

- Chrome 60+
- Firefox 55+
- Safari 11+
- Edge 79+
- Mobile browsers (iOS Safari, Chrome Mobile)

## Security Features

- Content Security Policy headers
- XSS protection
- iFrame sandboxing
- No external dependencies
- HTTPS enforcement (when configured)

## Privacy Features

- No tracking, analytics, or logging

## SEO & Performance

- Optimized meta tags
- Gzip compression enabled
- Cache headers configured
- Mobile-friendly design
- Fast loading times
- XML sitemap included

## Troubleshooting

**Auto-detection not working?**
- Disable ad-blocker
- Check that users are on WiFi, not cellular
- Verify router is using standard IP ranges
- Test manually with browser dev tools

**Styling issues?**
- Ensure all CSS is properly closed
- Check for browser compatibility
- Validate HTML syntax

**Server errors?**
- Verify `.htaccess` compatibility with your host
- Check file permissions (644 for files, 755 for directories)
- Review server error logs

## License

This project is open source. Feel free to modify and distribute.

## Support

For issues or questions:
1. Check the troubleshooting section above
2. Test in multiple browsers
3. Verify network connectivity
4. Review browser console for errors