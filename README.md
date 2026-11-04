# The Department of Unfinished Things

A browser-only, compassionate case-file maker. No account, analytics, server-side storage, or AI service is used. Inputs and case state exist only in the current page's memory; refreshing or closing clears them. Downloads and printing happen locally.

## Run locally

Open `index.html` in a modern browser, or run `python3 -m http.server 8000` in this directory and visit http://localhost:8000. No dependencies or build step are required.

## Deploy to Cloudflare Workers

The checked-in `worker.js` serves the exact HTML embedded in it. After editing `index.html`, run `node build-worker.mjs` to regenerate the Worker. Deploy `worker.js` to the existing `the-department-of-unfinished-things` Worker with your preferred Cloudflare deployment workflow. The Worker serves no API and does not collect case contents.

## Sister department

When the actual URL is known, set `SISTER_DEPARTMENT_URL` near the top of the script in `index.html` to its full HTTPS address, then regenerate the Worker. Until then, the page clearly says the link is coming soon.
