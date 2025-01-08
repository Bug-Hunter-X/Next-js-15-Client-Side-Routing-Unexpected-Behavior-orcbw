# Next.js 15 Client-Side Routing Issue

This repository demonstrates an unexpected behavior in Next.js 15's client-side routing.  When navigating to the '/about' page, the page appears to render before the actual rendering process completes (as evidenced by a setTimeout console log).  This might lead to inconsistent UI behaviour and data fetching issues in larger applications.

## Steps to Reproduce

1. Clone this repository.
2. Run `npm install`.
3. Run `npm run dev`.
4. Navigate to the '/about' page.
5. Observe that the About page content is displayed before the console log in `about.js` appears, indicating that the page's components haven't fully rendered.

## Expected Behavior

The About page should render completely *after* the `console.log` in `about.js` indicates successful rendering.

## Actual Behavior

The About page content displays before the `console.log` executes, which is inconsistent with the expected rendering process.