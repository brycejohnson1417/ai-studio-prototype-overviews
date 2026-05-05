# Production Readiness Checklist

Use this checklist before any prototype becomes a public standalone app outside AI Studio.

## API Boundary

- Model calls are server-side or visitor-key based.
- No private key is bundled into browser JavaScript.
- Rate limits exist.
- Budget alerts exist.
- Abuse handling exists.

## Data Boundary

- No private uploads are retained without clear disclosure.
- Synthetic examples are used for public screenshots.
- Sensitive inputs are not logged by default.
- Export and sharing behavior is explicit.

## Product Boundary

- README explains what the prototype does and does not do.
- Failure modes are documented.
- The prototype has a status label: active concept, visual prototype, playful prototype, or unfeatured experiment.
- Any consent-sensitive workflow has clear acceptable-use language.

