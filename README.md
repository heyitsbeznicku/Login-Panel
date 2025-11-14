# Login Panel — Dark Themed Login UI

A lightweight, dark-themed login panel built with plain HTML and CSS (Font Awesome icons). Designed as a small reusable component for portfolio pages and simple projects. Focuses on clean visuals, straightforward markup and easy customization.

## Features
- Dark, modern UI with subtle neon accent
- Inline Font Awesome icons inside inputs
- Fully responsive design (desktop, tablet, mobile)
- Remember-me checkbox and Forgot Password link
- Smooth transitions with accessibility in mind
- Keyboard accessible inputs and focus styles
- Easy to customize colors and spacing

## Demo / Preview
Open `LoginPanel.html` in your browser to view the panel. Visit [beznicku.pl](https://beznicku.pl) to see it in action.

## Technologies
- HTML5
- CSS3
- Font Awesome 6.4.0 (for icons)

## Installation / Run locally
1. Clone or download the repository.
2. Ensure `LoginPanel.html` is in your project folder (no server required).
3. Open the file in any modern browser:
   - Double-click the file, or
   - Right-click → "Open with" → your preferred browser

## Usage
- The form is static (no backend). To integrate with a backend, set the `form` element `action` attribute and adapt `method`.
- Edit placeholders, labels and styles directly in `LoginPanel.html`.
- Customize username/password field names as needed.

## Customization
- **Colors**: Change the accent (neon) by editing border and box-shadow colors (`#00e5ff`) inside the file.
- **Button**: Dark gradient by default, hover uses accent. Adjust `.login-btn` / `.login-btn:hover`.
- **Fonts**: Replace the system font-family if needed.
- **Panel size**: Adjust `.login-panel` width and padding for different layouts.

Example color change:
```css
/* change accent color from cyan to purple */
.login-panel input,
.login-btn,
.input-wrapper i {
  border-color: #b026ff; /* new accent */
  color: #b026ff;
}

.login-panel input:hover,
.login-panel input:focus {
  box-shadow: 0 0 40px rgba(176, 38, 255, 0.25); /* updated shadow */
}
```

## Responsive Design
The panel includes media queries for tablets and mobile devices:
- **Desktop** (768px+): Full-width panel at center
- **Tablet** (480px - 768px): 90% width, stacked form options
- **Mobile** (< 480px): 95% width, optimized spacing and font sizes

## Accessibility & Reduced Motion
To reduce flashing or rapid background color changes (for users sensitive to motion or light), add this rule:

```css
@media (prefers-reduced-motion: reduce) {
  .login-btn,
  .login-btn:hover,
  .remember-me span,
  .forgot-password {
    transition: none !important;
    transform: none !important;
  }

  .login-btn:hover {
    background: linear-gradient(135deg, #1a1a2e 0%, #16213e 100%); /* no color swap */
    box-shadow: 0 0 20px rgba(0, 229, 255, 0.1);
  }
}
```

## Contribution
- Issues and PRs welcome.
- Keep changes focused: either move styles to a separate file, add backend integration examples, or provide localization.

## License
MIT — free to use and modify. Include attribution if reusing in public projects.

## Author & Contact
- Created by **bez_nicku**
- Email: heyitsbeznicku@gmail.com
- Website: [beznicku.pl](https://beznicku.pl)
- Discord: bez_nicku

---
