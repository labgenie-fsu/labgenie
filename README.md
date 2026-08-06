# LabGenie Volunteer Registry: Website

Public recruitment website for the **LabGenie** project at Florida State University, School of Information.

The site introduces LabGenie, explains what taking part in research involves, and guides visitors toward one action: **joining the LabGenie Volunteer Registry**.

It is deliberately *not* about any single study. Individual studies are described when we contact a volunteer, not on this site. 

---

## Repo contents

```
index.html                            Home page
faq.html                              Full FAQ page
assets/style.css                      Shared stylesheet for both pages
assets/labgenie-icon.png              Masthead and footer mark
assets/labgenie-wordmark.png          Masthead wordmark (dark, for light backgrounds)
assets/labgenie-wordmark-light.png    Footer wordmark (light, for the dark footer)
assets/favicon.png                    Browser tab icon
registry-form/                        Registry form documents (not part of the site)
README.md                             This file
```

No build step, no dependencies, no `npm install`. Edit, save, refresh.

---

## Making a change

1. Open the file in a text editor
2. Find the section you want, each is marked with a comment banner
3. Edit, save
4. Open the page in a browser to preview
5. Commit and push. GitHub Pages redeploys in about a minute

Read the comment block at the top of `index.html` first. It flags what shouldn't change without approval.

**Styling lives in `assets/style.css`, shared by both pages.** Edit it once and both update. There is no `<style>` block in the HTML any more.

---

## Quick reference

| I want to change... | Where to look |
|---|---|
| Wording on the home page | `index.html`, find the `<section>` by its `id` |
| Wording on the FAQ page | `faq.html`, find the `<details>` block |
| Colours or fonts | The `:root` block at the top of `assets/style.css` |
| The registry link | Search for `qualtrics.com` **5 places**: 3 in `index.html`, 2 in `faq.html` |
| Ways to take part (activity/time table) | `index.html`, section `WAYS YOU CAN PARTICIPATE` |
| The four-step "what happens next" | `index.html`, section `WHAT HAPPENS AFTER I SIGN UP` |
| The four quick questions | `index.html`, section `QUICK QUESTIONS` |
| The example result card | `index.html`, section `ABOUT LABGENIE` two views, `#view-portal` and `#view-genie` |
| Add or remove a full FAQ | `faq.html`, copy a `<details>` block inside the right `.faqgroup` |
| Add a nav link | `<header class="masthead">` on **both** pages they're duplicated |

Nav and footer are duplicated across the two pages. If you change one, change the other.

---

## Accessibility

The audience is adults 60 and over, so several things are deliberate:

- Body text is 1.15rem minimum, with generous line height
- Buttons are at least 56px tall
- All motion is disabled if the visitor's OS has "reduce motion" enabled
- The FAQ uses native `<details>`/`<summary>` and works without JavaScript
- The result card toggle is a proper ARIA tablist with arrow-key support; with JavaScript off, the explained view stays visible
- Choice layouts are vertical, which is easier to hit accurately on a phone
- Keyboard focus outlines are visible, and a "skip to main content" link precedes the nav

Please keep these intact.

---

## Maintainer

**Dhruv Kale** Application Developer, School of Information, Florida State University
