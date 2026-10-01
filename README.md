# Rishath 3D Portfolio
React Three Fiber + drei + GSAP ScrollTrigger + Framer Motion + Tailwind v4 (Vite).
## Run
npm install && npm run dev   (open the printed localhost link)
Test the low-end 2D fallback: add `?lite=1` to the URL.
## Photo
Put your photo at `public/me.jpg` (already included). If missing, the About card shows an upload box.
## Deploy on Vercel
1. Push this folder to a new GitHub repo.
2. vercel.com > Add New > Project > import the repo.
3. Framework: Vite (auto-detected). Build: `npm run build`. Output: `dist`. Click Deploy.
4. Every `git push` redeploys. Add a custom domain under Project > Settings > Domains.
## Add a project
Add one line to the `PROJECTS` array in `src/App.jsx`.
