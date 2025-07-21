# 📌 Tailwind Profile Card — Explanation (Task 5)

This HTML file creates a responsive **Profile Card** using **Tailwind CSS**, with smooth hover effects, dark mode support, and modern UI best practices. Below is a full breakdown of each part of the code and why it’s used.

---

## 🧠 Head Section

```html
<!DOCTYPE html>
➡️ Declares the document type. It ensures the browser renders the page in standards mode.

<html lang="en" class="bg-gray-100 dark:bg-gray-900">
➡️ Begins the HTML document and sets the default background for light mode using Tailwind (bg-gray-100) and for dark mode (dark:bg-gray-900) using the dark: variant.


<head>
  <meta charset="UTF-8">
➡️ Declares the character encoding as UTF-8 to support all characters.

  <meta name="viewport" content="width=device-width, initial-scale=1.0">
➡️ Ensures the layout scales properly on all screen sizes — essential for responsive design.


  <title>Tailwind Profile Card</title>
➡️ Sets the title shown in the browser tab.

  <script src="https://cdn.tailwindcss.com"></script>
➡️ Loads Tailwind CSS from CDN so we can use all utility classes without local setup.



  <script>
    tailwind.config = {
      darkMode: 'class',
    }
  </script>
➡️ Configures Tailwind to enable dark mode using a manual class toggle (dark), instead of relying on the user’s system preference.

🌙 Dark Mode Toggle Button

<button id="darkToggle" ...>Toggle Dark Mode</button>
➡️ A fixed-position button in the top-right that toggles dark mode on and off using JavaScript. Includes:

bg-white dark:bg-gray-700: changes color based on theme.

hover:scale-105 transition: animates on hover for visual feedback.

rounded shadow: gives a clean UI with a drop shadow.

👤 Profile Card Container

<div class="max-w-sm w-full ...">
➡️ A responsive card limited to a small max width (max-w-sm) but fills available width (w-full), with padding and hover effects:

bg-white dark:bg-gray-800: light/dark background

rounded-2xl: smooth corner radius

shadow-xl hover:shadow-2xl: animated elevation on hover

transform hover:scale-105 transition: gently enlarges the card on hover

🖼️ Profile Image Section

<img class="w-28 h-28 rounded-full ...">
➡️ Adds a circular profile picture with:

Fixed size (w-28 h-28)

Rounded corners (rounded-full)

border for visual contrast

transition-all: smooth animation when switching themes

🧾 Name & Description

<h2 class="...">Shibiraj R</h2>
<p class="...">Founder @ FSP ...</p>
➡️ Displays the user’s name and description:

Font styles (text-xl font-bold) for emphasis

text-gray-900 dark:text-white adapts color to light/dark mode

✉️ Contact Button

<a href="mailto:..." class="...">Contact</a>
➡️ A styled button that links to email. Uses:

Tailwind button styling (bg-blue-500, text-white, rounded-full)

hover:bg-blue-600 transition for interactivity

🧠 Skills Section

<div class="mt-6 text-sm text-gray-700 ...">
  <p><span class="font-medium">Stack:</span> ...</p>
</div>
➡️ A brief "About Me" or "Skills" section with clean typography. Tailwind provides:

Spacing (mt-6)

Readable font size (text-sm)

Light/dark adaptive text colors

💡 Dark Mode Toggle Script

const toggle = document.getElementById('darkToggle');
const html = document.documentElement;

toggle.addEventListener('click', () => {
  html.classList.toggle('dark');
});
➡️ JavaScript that:

Grabs the <html> element

Toggles the dark class on button click

Tailwind then applies all dark: utilities

📱 Responsive Behavior
The entire layout uses:

flex, items-center, justify-center: vertically and horizontally centers content

min-h-screen px-4: keeps the card centered even on tall screens and small devices

🌟 Summary of Concepts Used
Feature	Tailwind Utility Classes Used
Responsive UI	w-full, max-w-sm, min-h-screen
Hover Effects	hover:scale-105, hover:shadow-2xl
Transitions	transition, transition-all, ease-in-out
Dark Mode	dark: variants, JS class toggle
Typography	text-sm, font-medium, text-gray-*
Layout	flex, items-center, justify-center, p-*

💬 Why This Matters
This profile card demonstrates how you can build beautiful, animated, and theme-aware components using only Tailwind CSS and a sprinkle of JavaScript — no custom CSS required.

👨‍💻 Built with Tailwind CSS and love by Shibiraj R

