# AI Studio Key And Spend Boundary

These prototypes were built around Google AI Studio style workflows.

## Current Boundary

AI Studio app links generally run behind Google sign-in and ask the visitor to select or attach their own API key before model calls execute.

That means the public AI Studio link is not the same thing as a Vercel or Netlify deployment using a private build-time key.

## The Footgun

Many Vite prototypes inject environment variables into browser code at build time. If one of these prototypes is deployed outside AI Studio with a private `GEMINI_API_KEY` in the build environment, that key can be bundled into public JavaScript.

## Safer Deployment Rule

Before deploying any prototype outside AI Studio:

1. Move model calls behind a server-side API route, or keep the visitor-key flow explicit.
2. Add rate limiting and budget controls.
3. Do not put private model keys in browser-visible build variables.
4. Add a clear demo note explaining who pays for API calls.

