# LabGenie: Project & Recruitment Website

Public website for the **LabGenie** project at Florida State University, School of Information. It explains the project and recruits participants for the UX testing sessions.

**Live site:** https://TODO.github.io

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

## Before it goes live

Three things are unresolved and the site should not be published until they are.

**1. IRB approval.** UX Testing Protocol V4.0 was submitted 23 July 2026; the FSU IRB meeting date is 12 August 2026. This page is a recruitment material and needs approval covering *this* protocol before going public. `STUDY00004785` covers the previous protocol (2-hour in-person workshops), not this one.

The IRB line in the footer is deliberately commented out. Uncomment it only once approval is granted, and use the study ID that covers V4.

**2. Compensation amount.** Protocol V4 doesn't state one. The 2025 flyer said a $50 Amazon gift card. The site currently says "Gift card" as a placeholder in two spots.

Search `index.html` for `TODO` to find all of these.

---

## Source of truth

All study details come from **LabGenie UX Testing Protocol V4.0 (21 July 2026)**.

Do **not** use the 2025 recruitment flyer as a reference. It describes the previous protocol and conflicts with the current one on almost every detail:

| | 2025 flyer | Protocol V4 |
|---|---|---|
| Format | In person at FSU | Remote, one-on-one, Zoom |
| Duration | Up to 2 hours | 60 minutes |
| Eligibility | 65+, normal vision, English | 65+, **two or more** listed chronic conditions, recent lab test, device with camera and mic, English |
| Exclusions | Terminal illness, severe motor impairment | Works in healthcare, already in another health-tech study, diagnosed cognitive impairment |

**Clear with Dr. He before changing:** eligibility criteria, session details, compensation, IRB wording, team names and titles, and the FAQ answers. Those answers make public commitments about what participants will and won't be asked to do, and each needs to match the approved protocol and consent form.

---

## Two open questions for the team

1. **Recruitment channel.** Protocol V4 lists Prolific as the primary channel and senior center contact lists as secondary. If this site and the tabling events are becoming the main source, that's a change from the written protocol.
2. **In-person sessions.** V4 scopes the in-person option to senior centers in **New York** via Pace University. If Tallahassee tabling is meant to feed in-person Tallahassee sessions, that isn't what the protocol describes.

---

## For tabling events

The site is built for someone scanning a QR code and browsing on their own phone:

- Sign-up buttons appear four times down the page (header, hero, mid-page band, footer), so one is never far away
- The four facts people ask first (one hour, online, one-on-one, gift card) sit at the top, above the fold
- The result card in the hero has a **Your portal / LabGenie** toggle a quick, tappable way to show what the tool actually does

There is deliberately **no fixed/sticky bar on mobile**. A `position:fixed` element fights the browser's collapsing address bar on every scroll, which makes the page stutter. Please don't add one back.

Generate the QR code once the final URL is live.

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