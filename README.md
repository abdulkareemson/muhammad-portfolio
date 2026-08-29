# Muhammad Nafiu Umar — Personal Portfolio

Personal portfolio website for Muhammad Nafiu Umar, B.Eng Computer Engineering student (Networking Option) at Ahmadu Bello University, Zaria. Built for **COEN 554 — Web Programming**, Question 1.

**Live site:** `https://muhammad-nafiu-portfolio.vercel.app/`

---

## Tech Stack

- HTML5 (semantic tags throughout)
- CSS3 (Grid, Flexbox, media queries, CSS-only interactivity — no JavaScript)
- JSON (`data/data.json` for structured Projects content)
- JSON-LD (`schema.org/Person`) embedded in every page's `<head>`

**No JavaScript is used anywhere in this project.** The mobile navigation menu is built with a pure-CSS checkbox toggle (`:checked` selector), and all hover/focus effects are plain CSS transitions.

---

## Folder Structure

```
portfolio-site/
├── index.html          Home
├── about.html          About Me
├── education.html      Educational Background
├── skills.html         Technical Skills
├── projects.html       Projects
├── hobbies.html        Hobbies and Interests
├── cv.html             CV (opens in a new tab from any nav link)
├── contact.html        Contact Me
├── assets/
│   ├── css/
│   │   └── style.css   Single stylesheet, all pages
│   └── images/         Profile photo + project screenshots
└── data/
    └── data.json       Structured data for the Projects page
```

---

## Pages

| Page                   | Purpose                                                                                  |
| ---------------------- | ---------------------------------------------------------------------------------------- |
| Home                   | Introduction, quick links to every section                                               |
| About Me               | Short bio + personal quote                                                               |
| Educational Background | B.Eng Computer Engineering, ABU Zaria                                                    |
| Technical Skills       | Networking, IoT, web development, technical operations                                   |
| Projects               | Smart Waste Detection & Sorting System (TinyML), Subnet & IP Address Calculator (Python) |
| Hobbies and Interests  | Pool, swimming, agribusiness                                                             |
| CV                     | Professional summary, experience, certifications, strengths                              |
| Contact Me             | Email, phone, location                                                                   |

---

## Running It Locally

No build step, no server required. Either:

- Double-click `index.html` to open it directly in a browser, **or**
- Serve it locally for a closer-to-production preview:
  ```
  cd portfolio-site
  python3 -m http.server 8000
  ```
  then visit `http://127.0.0.1:5500/`

---

## Deployment (Vercel)

1. Push this folder to a GitHub repository.
2. Go to [vercel.com](https://vercel.com), sign in, and click **Add New Project**.
3. Import the GitHub repository.
4. Framework Preset: **Other**. Leave Build Command and Output Directory blank — this is a static site with no build step.
5. Set the Root Directory to wherever `index.html` sits (the repo root, if you pushed the folder contents directly).
6. Click **Deploy**. Vercel returns a live URL within seconds.

Alternative, no GitHub needed:

```
npm install -g vercel
cd portfolio-site
vercel
```

---

## Updating Content Later

- **Projects:** edit both `data/data.json` and the matching card in `projects.html` (the JSON is the structured reference; the HTML is what actually renders, since no JavaScript is used to fetch it client-side).
- **Photo / screenshots:** drop new images into `assets/images/` and update the relevant `<img src="...">` path.
- **CV:** edit the content directly inside `cv.html`.

---

## Assignment Compliance Notes

- Semantic HTML5 tags (`header`, `nav`, `main` via page sections, `article`, `footer`) throughout.
- Fully responsive, mobile-first CSS with breakpoints.
- `data/data.json` models the Projects content as structured entities (`id`, `title`, `date`, `category`, `description`, `image_url`).
- JSON-LD `Person` schema in every page `<head>` for machine-readable identity metadata.
- Zero JavaScript, verified across all 8 pages.

---

© 2026 Muhammad Nafiu Umar. Built for COEN 554, Web Programming, Ahmadu Bello University, Zaria.
