# Om Patel — Portfolio Website

A single-file, production-ready portfolio (`index.html`) built entirely from the content in `Om_Patel_Resume.pdf`. No skills, projects, or experience were invented — everything you see traces back to the resume.

## What's inside
- Dark theme by default with a light-mode toggle (persisted via `localStorage`)
- Animated hero with a typing effect cycling through your actual roles, a canvas particle network background, magnetic/ripple buttons, and a custom cursor
- About section with a real timeline (internships, education) and animated stats (CGPA, internship count, etc.)
- Skills grouped exactly as on the resume: Programming Languages, Frontend, Backend, Frameworks, Data Science Toolkit, Tools & Core Competencies, Soft Skills
- Experience timeline for both internships (Thiranex, Unified Mentor) with real responsibilities and tech tags
- Projects section with "Trendy Threads" (from your resume) plus all 6 of your public GitHub repos (github.com/om773): "Bluesky" (weather forecasting), "Jarvis Voice Assistant", "Advance Jarvis Website", "Crazy Racing Game (HTML5)", "Crop Residue Management for Energy Generation", and "AIToolGalaxy" — with filtering + search
- Education, Freelance Services, Why Hire Me, Testimonials (placeholders, as requested), Blog (placeholder, as requested), and a Contact section with a working `mailto:` fallback
- Scroll progress bar, back-to-top button, WhatsApp button, sticky Hire Me CTA, section reveal animations (GSAP + ScrollTrigger), reduced-motion support, skip link, and visible focus states
- SEO: title, meta description, keywords, Open Graph, Twitter Card, and JSON-LD Person schema — all populated with your real details

## A few honest notes
- **GitHub projects**: descriptions for Bluesky, Jarvis Voice Assistant, Crazy Racing Game, Crop Residue Management, and AIToolGalaxy are taken from what's on their GitHub repo pages (name, description, primary language) — not from reading each repo's full README, since only the profile overview was accessible. "Advance Jarvis Website" has no description on GitHub yet, so its card says so plainly. Feel free to send me each repo's README (or a short description) and I'll flesh out the Features/Challenges sections like Trendy Threads has.
- **Skill bars**: your resume doesn't list proficiency percentages, so the bar widths are illustrative (not a precise claim about skill level). Feel free to adjust the `data-fill` values in the Skills section to match how you'd actually rate yourself.
- **Services pricing**: shown as "Contact for pricing" rather than invented numbers — add real starting prices once you've decided on them.
- **Photo**: the hero uses your initials as a placeholder avatar. Swap in a real photo by replacing the `.hero-photo` div content with an `<img>` tag.
- **Contact form**: wired to send submissions to **nriomp25@yahoo.com** using [EmailJS](https://www.emailjs.com/) (free tier, ~200 emails/month). To activate it: create an EmailJS account, add an Email Service with `nriomp25@yahoo.com` as the recipient, create an Email Template using the `from_name`, `from_email`, `subject`, `message` variables, then paste your **Public Key**, **Service ID**, and **Template ID** into the `EMAILJS_PUBLIC_KEY` / `EMAILJS_SERVICE_ID` / `EMAILJS_TEMPLATE_ID` constants near the bottom of `index.html`. Until those are filled in, the form falls back to opening the visitor's email client with a message pre-addressed to `nriomp25@yahoo.com`.
- **Book a Meeting / Live Demo / Verify buttons**: linked as placeholders — swap in your Calendly link, deployed project URL, etc. once available.

## Tech used
Plain HTML/CSS/JS (no build step required) with:
- Tailwind-free custom CSS using your requested color palette and CSS variables for theming
- GSAP + ScrollTrigger (CDN) for scroll reveals and counters
- Lucide Icons (CDN)
- Canvas 2D for the particle network background (lightweight alternative to a full Three.js scene)

## Running locally
Just open `index.html` in a browser — no build step needed.

## Deploying to Vercel
1. Create a new GitHub repo and push `index.html`, `Om_Patel_Resume.pdf`, and this `README.md`.
2. Go to [vercel.com/new](https://vercel.com/new), import the repo.
3. Framework preset: **Other** (static site) — no build command needed, output directory is the repo root.
4. Deploy. Vercel will give you a live URL (e.g. `om-patel.vercel.app`) — update the `og:url`/`canonical` tags in `index.html` to match once you have it.

### Optional next steps
- Wire up the contact form to Formspree, EmailJS, or a serverless function.
- Add a real headshot and Open Graph cover image.
- If you'd like this rebuilt as a full Next.js + TypeScript + Framer Motion project (with routing, a proper `/api` contact route, and componentized files) instead of a single HTML file, just ask — happy to scaffold that version too.
