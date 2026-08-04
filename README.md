# LabGenie: Project & Recruitment Website

Public website for the **LabGenie** project at Florida State University, School of Information. It explains the project and recruits participants for the UX testing sessions.

---

## Repo contents

```
index.html                          The entire site: HTML, CSS, and JS in one file
assets/labgenie-icon.png            Masthead and footer mark
assets/labgenie-wordmark.png        Masthead wordmark (dark, for light backgrounds)
assets/labgenie-wordmark-light.png  Footer wordmark (light, for the dark background)
assets/favicon.png                  Browser tab icon
README.md                           This file
```

No build step, no dependencies, no `npm install`.

---

## Making a change

1. Open `index.html` in a text editor
2. Find the section you want, each is marked with a comment banner
3. Edit, save
4. Open `index.html` in a browser to preview
5. Commit and push GitHub Pages redeploys in about a minute

Read the comment block at the very top of `index.html` first. It flags everything that shouldn't be changed without approval.

---

## Quick reference

| I want to change... | Where to look |
|---|---|
| Any wording | Inside `<body>`, find the `<section>` by its `id` |
| Colors or fonts | The `:root` block at the top of `<style>` |
| The sign-up link | Search `TODO` it appears in 4 places |
| Session details (length, format, gift card) | Section `WHAT'S INVOLVED`, in the `.spec` list |
| Eligibility criteria | Section `WHO CAN JOIN` |
| The example result card | Section `HERO` two views, `#view-portal` and `#view-genie` |
| Add/remove a team member | Section `TEAM`, copy an `<li>` block |
| Add/remove an FAQ | Section `QUESTIONS`, copy a `<details>` block |
| Add a nav link | `<header class="masthead">` add `<a href="#id">` and give the section that `id` |

---

## Accessibility

The audience is adults 65 and older, so a few things are deliberate:

- Body text is 1.15rem minimum with generous line height
- Sign-up buttons are at least 56px tall
- All motion is disabled if the visitor's OS has "reduce motion" enabled
- The FAQ uses native `<details>`/`<summary>` and works without JavaScript
- The result card toggle is a proper ARIA tablist with arrow-key support; with JavaScript off, the LabGenie view stays visible
- Keyboard focus outlines are visible, and a "skip to main content" link precedes the nav

Please keep these intact.

---

## Maintainer

**Dhruv Kale** Application Developer, School of Information, Florida State University