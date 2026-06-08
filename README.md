#  Valentine — Will You Be My Valentine?

> An interactive Valentine's Day web experience built with pure HTML, CSS, and JavaScript — my first deployed project as a first-year CS student.

[![Live Demo](https://img.shields.io/badge/🌐%20Live%20Demo-Visit%20Site-ff4d79?style=for-the-badge)](https://shawshank1307.github.io/Valentine-Repo/)
[![GitHub Repo](https://img.shields.io/badge/GitHub-Valentine--Repo-181717?style=for-the-badge&logo=github)](https://github.com/shawshank1307/Valentine-Repo)
[![Made with HTML](https://img.shields.io/badge/HTML-96.5%25-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://github.com/shawshank1307/Valentine-Repo)
[![Made with CSS](https://img.shields.io/badge/CSS-1.8%25-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://github.com/shawshank1307/Valentine-Repo)
[![Made with JS](https://img.shields.io/badge/JavaScript-1.7%25-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://github.com/shawshank1307/Valentine-Repo)

---

##  Preview

> A soft pink-themed page asking **"Will you be my Valentine Girl? ❤️"** — with a Yes button that rewards you and a No button that literally runs away from your cursor.

---

##  Live Site

👉 **[https://shawshank1307.github.io/Valentine-Repo/](https://shawshank1307.github.io/Valentine-Repo/)**

Deployed via **GitHub Pages** — live, free, and publicly accessible directly from the repository.

---

## 💡 What This Project Does

This is a fun, interactive Valentine's Day webpage where:

- The user is presented with the question **"Will you be my Valentine Girl? ❤️"**
- If they click **Yes** → a celebration GIF appears with the message *"You really made me Happy Gurlll 😂💖"*
- If they try to click **No** → the button **runs away** from the cursor using randomised screen coordinates, making it impossible to click
- The experience is fully responsive and works on both desktop and mobile

---

##  How I Thought Through This

I built this project entirely in my **first year of computer science** — before I had formal training in DOM manipulation or event handling. Here's the thought process behind each piece:

### The Core Idea
I wanted to make something personal and fun — not just a static webpage. The challenge was: *how do I make a "No" button feel alive?* That's when I thought about using JavaScript to change the button's position dynamically whenever someone's mouse gets close.

### The "Runaway" Button Logic
The key insight was using `mouseover` on the `#no` button and reassigning its `style.left` and `style.top` to random values within the viewport bounds every time the user's cursor approaches. I set the button's `position` to `absolute` in CSS so it could be freely repositioned on the page — no layout interference.

```javascript
noButton.addEventListener("mouseover", () => {
  const x = Math.random() * (window.innerWidth - 100);
  const y = Math.random() * (window.innerHeight - 50);
  noButton.style.left = x + "px";
  noButton.style.top = y + "px";
});
```

The `-100` and `-50` offsets prevent the button from jumping off-screen — I figured that out through trial and error.

### The Yes Celebration
For the `Yes` button, I used a simple `click` event listener to toggle the hidden GIF div from `display: none` to `display: block`. I pulled a fun GIF from Giphy to make the moment feel rewarding and personal.

### The Layout
I used **Flexbox** (`display: flex; justify-content: center; align-items: center; height: 100vh`) to center everything perfectly on screen — a pattern I'd just learned and wanted to apply in a real project.

### Deployment
After getting the HTML working locally, I deployed it using **GitHub Pages** by enabling it in the repository settings. This was my first time deploying anything to the live internet — figuring out the `.github/workflows` pipeline was a learning moment in itself.

---

##  Project Structure

```
Valentine-Repo/
│
├── index.html          # Main page — structure, embedded styles, and JS logic
├── style.css           # External stylesheet (linked from index.html)
├── script.js           # External JavaScript file
├── .github/
│   └── workflows/      # GitHub Actions / Pages deployment config
└── README.md           # This file
```

> **Note:** The core logic (HTML structure, CSS styles, and JavaScript) is all embedded within `index.html`. The external `style.css` and `script.js` files are linked for separation of concerns.

---

##  Tech Stack

| Technology | Usage |
|---|---|
| **HTML5** | Page structure, semantic layout |
| **CSS3** | Flexbox layout, button styling, color theming, absolute positioning |
| **Vanilla JavaScript** | DOM event handling (`mouseover`, `click`), dynamic style manipulation |
| **GitHub Pages** | Free static site hosting with CI/CD via GitHub Actions |

No frameworks. No libraries. No build tools. Just the raw web fundamentals.

---

## ✨ Features

- 💘 **Interactive Valentine's proposal** — personalized and fun
- 🏃 **Runaway "No" button** — randomised positioning on hover makes it nearly impossible to click
- 🎉 **GIF celebration on "Yes"** — cheerful animated response on acceptance
- 🎨 **Soft pink UI** — warm `#ffe6eb` background, rounded buttons, clean typography
- 📱 **Responsive layout** — Flexbox centering works across screen sizes
- 🌐 **Deployed live** — accessible to anyone with the link, no setup needed

---

##  Running Locally

No installation or setup required.

```bash
# Clone the repository
git clone https://github.com/shawshank1307/Valentine-Repo.git

# Navigate into the folder
cd Valentine-Repo

# Open in browser
open index.html
# or just double-click index.html in your file explorer
```

---

##  What I Learned

This project was my hands-on introduction to several core web development concepts:

- **DOM manipulation** — selecting elements with `getElementById` and changing their properties at runtime
- **Event listeners** — understanding `mouseover` vs `click` and when to use each
- **CSS positioning** — the difference between `static`, `relative`, and `absolute`, and why `absolute` was essential for the runaway button
- **Flexbox** — centering content vertically and horizontally in a viewport
- **GitHub Pages deployment** — publishing a live website from a repository, configuring the `main` branch as the source
- **Viewport-aware randomness** — using `window.innerWidth` and `window.innerHeight` with offsets to keep elements on-screen

---

## 🌱 About Me

Hi, I'm **Shashank** — a first-year Computer Science student. This project was one of my earliest attempts at building something real with web technologies. I wanted to go beyond textbook exercises and create something that actually *does* something fun and interactive.

I'm learning the fundamentals of HTML, CSS, and JavaScript, and this project represents my process of applying what I study in class to something I actually care about building.

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).  
Feel free to fork it, personalise it, and send it to your special someone 💌

---

<p align="center">Made with ❤️ and a little JavaScript magic</p>
