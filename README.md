# Login Panel — Dark Themed Login UI

A lightweight, dark-themed login panel built with plain HTML and CSS (Font Awesome icons). Designed as a small reusable component for portfolio pages and simple projects. Focuses on clean visuals, straightforward markup and easy customization.

## Features
- Dark, modern UI with subtle neon accent
- Inline Font Awesome icons inside inputs
- Responsive and simple layout
- Remember-me checkbox and Forgot Password link
- Smooth but slow background transition on the button (reduced risk of flashing)
- Keyboard accessible inputs and focus styles
- Easy to customize colors and spacing

## Demo / Preview
Open `beznicku.pl` in your browser to view the panel.

## Technologies
- HTML5
- CSS3
- Font Awesome (for icons)

## Installation / Run locally
1. Clone or download the repository.
2. Ensure `LoginPanel.html` is in your project folder (no server required).
3. Open the file in any modern browser:
   - double-click the file, 

## Usage
- The form is static (no backend). To integrate with a backend, set the `form` element `action` attribute and adapt `method`.
- Edit placeholders, labels and styles directly in `LoginPanel.html`.

## Customization
- Colors: change the accent (neon) by editing border and box-shadow colors (`#00e5ff`) inside the file.
- Button: dark gradient by default, hover uses accent. Adjust `.login-btn` / `.login-btn:hover`.
- Fonts: replace the system font-family if needed.

Example variables or CSS to change:
```css
/* change accent color */
.login-panel input,
.login-btn {
  border-color: #00e5ff; /* accent */
}
```

## Accessibility & Reduced Motion
To reduce flashing or rapid background color changes (for users sensitive to motion or light), the project includes slowed transitions. For stricter accessibility, add a `prefers-reduced-motion` rule to remove or fade animations:

```css
@media (prefers-reduced-motion: reduce) {
  .login-btn,
  .login-btn:hover {
    transition: none !important;
    transform: none !important;
    box-shadow: none !important;
    background-image: none !important;
    background-color: #16213e !important; /* stable fallback */
  }
}
```

Or, replace the color-changing hover with a subtle shadow-only hover:
```css
.login-btn:hover {
  background: linear-gradient(135deg, #1a1a2e 0%, #16213e 100%); /* no color swap */
  box-shadow: 0 0 40px rgba(0,229,255,0.15);
  transform: scale(1.02);
}
```

## File structure
- LoginPanel.html — main file containing HTML + CSS (inline) and Font Awesome link
- (Optional) Move styles to `styles.css` and icons to a shared assets folder for larger projects

## Contribution
- Issues and PRs welcome.
- Keep changes focused: either move styles to a separate file, add backend integration examples, or provide localization.

## License
MIT — free to use and modify. Include attribution if reusing in public projects.

## Author & Contact
- Created by bez_nicku.
- Contact: heyitsbeznicku@gmail.com 

---

