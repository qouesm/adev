# adev

## A personal landing page for me, Andrew Avella

## [andrewavella.dev](https://andrewavella.dev)

# TODO

- Add headshot
- Add logo/favicon

### Info

This project was made as a landing page for any potential future employers (Hello if you're reading this!) so that I can link together my resume with my various links and contact info.
It's built with [Svelte](https://svelte.dev/) ([SvelteKit](https://kit.svelte.dev/)) and [TailwindCSS](https://tailwindcss.com/) to be very simple but extensible when I need it to be.

### Development

Clone the repo
```
git clone git@github.com:qouesm/adev.git
```

Navigate to the repo
```
cd adev
```

To serve the page locally one time
```
npm run build
npm run preview
```

To reload the app when changes are made
```
npm run dev
```

Prettier and ESLint are included for project formatting and linting respectively
```
npm run format
npm run lint
```

### Deployment

This project is intended to be deployed in a Docker container so that it may be hosted from my Raspberry Pi.

Assuming you have cloned and navigated to the repo:

First build the image
```
docker build . -t adev
```

Then run it
```
docker run -p 3000:3000 --name adev adev
```

The website will be available on http://localhost:3000.
At this point I set up a Cloudflare tunnel to serve the page publicly.
