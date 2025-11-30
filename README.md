# High-Fidelity GIS & Plant Management (Vite)

Simple Vite + React starter with Mapbox (optional) and Leaflet fallback.

## Quick start

1. Install dependencies:

```bash
npm install
```

2. Start dev server:

```bash
npm run dev
```

3. To enable Mapbox, set an environment variable before starting or set window.MAPBOX_TOKEN in the browser console.

- Create a `.env` file with `VITE_MAPBOX_TOKEN=your_token` (optional). The app also reads `window.MAPBOX_TOKEN` at runtime.

## Notes
- This project is JavaScript (no TypeScript).
- TailwindCSS is configured. You may need to run the dev server so Tailwind classes are processed.


## Docker (build and run)

### Build image and run locally

```
# build Docker image
docker build -t high-fidelity-gis:latest .
# run container
docker run -p 5173:80 --name high-fidelity-gis -e VITE_MAPBOX_TOKEN=your_token -d high-fidelity-gis:latest
```

Or with docker-compose:

```
# using docker compose
docker-compose up --build -d
```

Open http://localhost:5173

## Push to GitHub (from your machine)

```
git init
git add .
git commit -m "Initial commit: Vite app + Docker"
# create repo on GitHub, then:
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO.git
git branch -M main
git push -u origin main
```

If you want I can prepare a push script or open a PR — you'll need to create the GitHub repo and provide access token if you want me to push it for you.
