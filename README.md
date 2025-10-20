# Password Generator

A small, responsive **Password Generator** (HTML / CSS / JavaScript).  
Generates random passwords with configurable length and character types, shows a strength meter, and lets users copy the result to clipboard.

---

## Demo
Replace the placeholder below with your live demo URL (GitHub Pages or other host):

**Live demo:** `https://password-generator-project-ali-khezri.netlify.app/`

---

## Features
- Select password length (6–24)
- Toggle character sets: Uppercase, Lowercase, Numbers, Symbols
- Generate random password with one click
- Copy password to clipboard (uses `navigator.clipboard`)
- Strength meter (Weak / Medium / Strong) with visual bar
- Responsive design and accessible UI
- No build step — pure static site (uses Google Fonts + Font Awesome CDN)

---

## Repo structure
```

.
├── index.html        # markup
├── style.css         # styling
├── script.js         # logic (generate, meter, clipboard)
├── README.md
└── (optional assets like icons/fonts)

````

---

## Quick start

### Option 1 — Open locally (fast)
Double-click `index.html` or open it in your browser.

> Note: `navigator.clipboard` works on pages served over `https` or `localhost` in some browsers. If copy fails when opening `file://`, use a local server (below).

### Option 2 — Run a local static server (recommended)
```bash
# With Python 3
python -m http.server 8000
# Open: http://localhost:8000

# Or using npm's serve (no install required):
npx serve .
````

### Option 3 — Use VS Code

Install the Live Server extension and click **Go Live**.

---

## How it works (brief)

* `script.js` builds a character pool depending on checkboxes.
* It picks `length` random characters to form a password.
* The strength meter scores the password on length and variety of character types.
* Clicking the copy icon writes the password to clipboard and shows a visual success briefly.

---

## Customization

* Change allowed characters in `script.js`:

  ```js
  const uppercaseLetters = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
  const lowercaseLetters = "abcdefghijklmnopqrstuvwxyz";
  const numberCharacters  = "0123456789";
  const symbolCharacters  = "!@#$%^&*()-_=+[]{}|;:,.<>?/";
  ```
* Adjust strength scoring logic in `updateStrengthMeter()` to match your policy (e.g., require at least one of each selected type).
* Replace Google Fonts / Font Awesome links in `index.html` if you prefer local assets.

---

## Author

**Ali Khezri** — [Github](https://github.com/ali-khezri) | [LinkedIn](https://www.linkedin.com/in/ali-khezri)

---
