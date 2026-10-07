<div align="center">

# Abdhul Nasar Rishath Ahamed
### Software Engineering Graduate · Portfolio

An interactive 3D portfolio with a guide robot, voice narration and an AI assistant.
Built with plain HTML, CSS and JavaScript plus Three.js. No build step.

**[Live demo](https://itsrishath-lgtm.github.io/rishath-portfolio/)** · **[GitHub](https://github.com/itsrishath-lgtm)** · **[LinkedIn](https://linkedin.com/in/rishath-ahamed-a3199330a)** · **[Email](mailto:itsrishath@gmail.com)**

</div>

---

## About

I'm a Computing HND (Software Engineering) graduate from ESOFT Metro Campus, based in Batticaloa, Sri Lanka. This site is my personal portfolio: it introduces me, shows my education journey, projects, skills and AI tools, and lets visitors get in touch.

I'm looking for **internship, trainee and entry-level roles** in software development, QA and testing, IT support, web development and data/BI.

## Features

- **Hero stage** with a transparent portrait, gradient disc, outline headline, camera-frame corners and a light sheen that follows the silhouette of the portrait.
- **3D particle galaxy** background. The camera drifts through it as you scroll.
- **Guide robot** (Three.js) that flies between sections, follows the cursor with its head and eyes, waves, and explains each section in a speech bubble.
- **Voice narration** using the browser Web Speech API. Tap the speaker button in the navbar to switch it on.
- **AI assistant chat** that answers questions about my skills, projects and education. It uses a built-in knowledge base, so it works everywhere (see [AI chat](#ai-chat)).
- **Sections:** Home, About, Flight plan (education timeline), Services, Projects, Skills and tools, Contact.
- **Floating navbar** with an animated active-section indicator, scroll progress bar, and dark/light theme switch.
- **Responsive** for phones, tablets, laptops and large desktops. Tested at 360, 390, 768, 1000, 1366 and 1920 px widths.
- **Low-end device fallback.** On slow devices or when "reduced motion" is enabled, the heavy galaxy background is switched off, and the page stays fast.

## Tech stack

| Area | Technology |
| --- | --- |
| Markup and styling | HTML5, CSS3 (custom properties, grid, flexbox, 3D transforms) |
| Logic | Vanilla JavaScript (ES2020) |
| 3D | [Three.js r128](https://threejs.org/) loaded from cdnjs |
| Voice | Web Speech API (`speechSynthesis`) |
| Hosting | GitHub Pages (static) |

There is no framework, bundler or package install. The whole site is one `index.html` plus one image.

## Projects shown on the site

| Project | Stack | Repository |
| --- | --- | --- |
| Hospital / Doctor Appointment System | Java, OOP, linked-list Stack and Queue | [doctor-appointment-system](https://github.com/itsrishath-lgtm/doctor-appointment-system) |
| Dream Book Shop Data Analysis | Python, Pandas, Matplotlib | [dream-book-shop-data-analysis](https://github.com/itsrishath-lgtm/dream-book-shop-data-analysis) |
| Hotel Sales Dashboard | Power BI, Power Query, DAX, Excel | [Hotel-Sales-Dashboard](https://github.com/itsrishath-lgtm/Hotel-Sales-Dashboard) |

## Project structure

```
rishath-portfolio/
├── index.html          # the whole site (HTML, CSS and JS)
├── assets/
│   └── portrait.webp   # transparent portrait used in the hero
├── .nojekyll           # tells GitHub Pages to serve files as they are
└── README.md
```

## Run locally

No install is needed. Pick one:

```bash
# Option 1: just open the file
open index.html            # macOS
start index.html           # Windows

# Option 2: a local server (recommended)
python -m http.server 8000
# then visit http://localhost:8000
```

An internet connection is required for the first load, because Three.js is fetched from a CDN.

> Opening `index.html` directly from disk (`file://`) works, but the light sheen on the portrait is hidden there because browsers block image masks from local files. It works normally on a server or GitHub Pages.

## Deploy on GitHub Pages

1. Create a new public repository, for example `rishath-portfolio`.
2. Upload `index.html`, `assets/`, `.nojekyll` and `README.md` (drag and drop in the browser works).
3. Go to **Settings → Pages**.
4. Under **Build and deployment**, set **Source** to **Deploy from a branch**, choose **main** and **/(root)**, then **Save**.
5. After about a minute the site is live at `https://<your-username>.github.io/<repo-name>/`.

Every commit to `main` redeploys automatically.

## Customise

| What | Where in `index.html` |
| --- | --- |
| Name, intro text | Search for `Abdhul Nasar` and the `<p>` below the headline |
| Typing roles | The `W=[...]` array in the first `<script>` |
| Projects | The `id="projects"` section. Copy one `<div class="pj rv">` block and edit it |
| Skills and AI tools | The `id="skills"` section. Add or remove `<span class="chip">` items |
| Education timeline | The `id="journey"` section |
| Robot speech per section | The `const T={...}` object in the second `<script>` |
| Chat answers | The `KB=[...]` list and the `CTX` text in the last `<script>` |
| Colours | CSS variables at the top of the `<style>` block (`--ac`, `--ac2`) |
| Portrait | Replace `assets/portrait.webp` with your own transparent PNG or WebP (about 800 px wide works well) |

## AI chat

The chat widget has two modes:

- **Built-in answers (default on GitHub Pages).** A keyword knowledge base answers questions about skills, projects, education, contact details and AI tools. It needs no server or API key.
- **Live AI mode.** When the page is opened inside Claude (as a published artifact), the widget calls Claude with my CV facts as context for free-form answers. If that is unavailable, it falls back to the built-in answers automatically.

If you want live AI on your own hosting, you would need a small backend that holds an API key. Never put an API key in the front-end code.

## Browser support

Latest Chrome, Edge, Firefox and Safari, on desktop and Android/iOS. Voice depends on the browser and device voices. On phones, tap the speaker button once to allow audio.

## Performance notes

- The galaxy uses 4,500 points on desktop and fewer on phones.
- Devices with 3 or fewer CPU cores, or with "reduced motion" turned on, skip the galaxy renderer. The robot and the rest of the page still work.
- Animations use `transform` and `opacity` so they stay smooth.

## Contact

- Email: [itsrishath@gmail.com](mailto:itsrishath@gmail.com)
- LinkedIn: [rishath-ahamed](https://linkedin.com/in/rishath-ahamed-a3199330a)
- GitHub: [@itsrishath-lgtm](https://github.com/itsrishath-lgtm)
- Location: Batticaloa, Sri Lanka

## License and usage

The code is free to read and learn from. Please do not reuse my photo, name or personal content. If you build your own site from this, replace them with yours.

&copy; 2026 Abdhul Nasar Rishath Ahamed
