# Link of portfolio👇👇👇
https://princebhandari.netlify.app/
# Prince Bhandari — 3D Coding-Themed Portfolio

A single-file, cinematic 3D portfolio with a code-editor/terminal aesthetic (JetBrains Mono, VS Code Dark+
palette, terminal window chrome) — built with Three.js + GSAP/ScrollTrigger + Lenis smooth scroll. The
contact form is wired to EmailJS instead of a custom backend.

## Run it
Just open `index.html` in a browser — no build step, no server required.

## Enable the contact form (EmailJS)
1. Create a free account at https://www.emailjs.com
2. Add an **Email Service** (e.g. connect your Gmail) → copy its **Service ID**
3. Create an **Email Template** with these variables in the body: `{{name}}`, `{{email}}`, `{{subject}}`, `{{message}}` → copy its **Template ID**
4. Go to **Account → General** and copy your **Public Key**
5. Open `index.html`, find this block near the bottom `<script>` section, and paste your three values in:

```js
const EMAILJS_SERVICE_ID  = 'YOUR_SERVICE_ID';
const EMAILJS_TEMPLATE_ID = 'YOUR_TEMPLATE_ID';
const EMAILJS_PUBLIC_KEY  = 'YOUR_PUBLIC_KEY';
```

That's it — messages submitted through the contact form will land directly in your inbox via EmailJS's
free tier (200 emails/month), no server or database needed.

## Sections
- Hero — terminal window frame with a Three.js particle field + wireframe icosahedron background, typing tagline
- About — rotating 3D wireframe object, resume-accurate bio and stats
- Education — pinned horizontal 3D scroll timeline (BCA → MCA) with a Three.js fly-through camera
- Projects — Society Maintenance Tracker, CourseHub, Streamflix, each with a live link and a cinematic detail modal
- GitHub — a repo grid pulled from github.com/princebhandarii, styled like a file listing
- Skills — animated bars + orbiting 3D spheres
- Contact — terminal-styled glassmorphic form (EmailJS)

## Customizing content
Project data lives in the `PROJECTS` array, education in `EDUCATION`, GitHub repos in `GH_REPOS`, and
skills in `SKILLS` — all inline in the script for easy editing without a build step. If you push new
repos, just add an entry to `GH_REPOS` with the repo name, description, primary language, and star count.

