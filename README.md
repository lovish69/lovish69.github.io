# Lovish Barber — The Engineering Observatory: Night Edition

A separate, redesigned portfolio in midnight navy, icy blue, and warm orange, featuring two independent interactive WebGL scenes and dimensional cards. Your existing live website has not been modified.

## Publish on your existing GitHub Pages site
1. Preview and approve this version first.
2. Back up your existing index.html, or use Git history to preserve it.
3. Upload index.html, favicon.svg, favicon.ico, apple-touch-icon.png, CNAME, .nojekyll, and the three license files from this folder to the ROOT of the same repository already serving deploywithlovish.tech. Replace files with matching names. Upload extracted files, not this ZIP.
4. Commit to the branch already configured under Settings → Pages, then wait for deployment to succeed.
5. Keep your existing custom domain and Enforce HTTPS setting unchanged. No DNS changes or new hosting are needed.
6. Open https://deploywithlovish.tech in a private window to check the new version. Browsers sometimes cache the old favicon.

The document title is exactly **Lovish Barber**. The included LB favicon matches the new cobalt-and-ivory palette.

## Interactive features
- Custom Three.js sculpture: seven layered decks, an central core, orbital bands, and clickable service satellites.
- Drag or keyboard-arrow rotation, pause/play, an unfold slider, wireframe mode, and reset.
- Project field-note dialogs with implementation details and links to the actual repositories.
- Category filtering for seven real projects.
- Interactive four-stage delivery lifecycle with keyboard-operable tabs.
- Ctrl/Cmd+K quick navigation, modal focus containment, and Escape dismissal.
- Public Credly credential links and embedded badge images.
- Email copy button with a visible fallback when clipboard access is unavailable.

The sculpture and architectural illustrations are conceptual, not live infrastructure or telemetry.

## Performance, accessibility, and fallbacks
The prebuilt index.html embeds the styles, fonts, badge images, application code, and Three.js bundle. There are no runtime CDN requests, remote fonts, paid APIs, or backend dependencies. Images/fonts/library account for most of the approximately 1.25 MB HTML document.

The renderer caps device pixel ratio and skips rendering while offscreen or while the document is hidden. Reduced-motion preferences disable automatic rotation. If WebGL initialization fails, a static fallback appears and all project content remains accessible. Without JavaScript, the seven project cards and repository links remain in the HTML.

## Editing and rebuilding
No installation or build step is required to publish the prebuilt index.html.

For further development:
```
npm ci
npm run build
```

Editable source:
- source/template.html — page structure and copy
- source/style.css — layout, colours, typography, responsive styles
- source/scene.js — custom Three.js model and interaction
- source/app.js — dialogs, filtering, lifecycle tabs, navigation
- source/projects.json — project descriptions and field notes
- source/credentials.json — credential content and embedded images
- source/fonts.css — embedded font declarations
- source/build.cjs — creates the self-contained index.html

Edit source files and rebuild rather than modifying both source and generated HTML separately. The original font and Three.js license notices must be retained.

## Content provenance
Project descriptions are based on the user's public repositories. Education and internship content come from the supplied résumé. The internship organization was not supplied and is not invented. No salary, employment, uptime, or performance-improvement claims were added.

Three earned certifications and an AWS Educate training badge appear on the public Credly profile:
https://www.credly.com/users/lovish-barber.1481ab50/badges/credly

Network+ via Udemy is labeled as coursework, not a CompTIA-issued certification. The cloud-todo application is identified as a team project, and its planned DynamoDB integration is not presented as complete. The original résumé PDF and phone number are not published. AI skills discussed as learning goals have not been represented as completed professional skills.

## Checks performed
- Chromium desktop 1440 px and responsive widths 320, 390, 768, and 1024 px: no horizontal overflow in tested layouts.
- No JavaScript page errors during the interaction test.
- Unfold slider, wireframe toggle, reset, project dialog, filtering, workflow tabs, keyboard workflow navigation, and command search tested.
- Reduced-motion preference pauses rotation.
- Simulated WebGL failure: fallback visible; project dialogs still work.
- JavaScript disabled: all seven static project cards and repository links remain accessible.

These are targeted browser checks, not a complete cross-browser accessibility or performance audit.


## Night Edition additions
- Complete dark theme across the hero, project cards, workflow, education, credentials, contact, dialogs, and favicon. Browser-tab title remains exactly Lovish Barber.
- Darker metallic hero materials, cool label plates, and a 3D star field.
- A second WebGL platform with four selectable stations: server infrastructure, container builds, Kubernetes pods, and a monitoring screen. The chart is illustrative, not live data.
- Station selection highlights and lifts the matching model, changes the explanatory readout, and synchronizes the lifecycle tabs below it.
- Isometric and top-view camera controls, drag/keyboard rotation, and pauseable data-flow particles.
- Perspective-following project cards, raised credential badges, and a layered about card on fine-pointer devices. Reduced-motion users do not get pointer tilt.
- A dimensional orbital motif in the contact section.

## Additional checks
Both canvases render in the tested Chromium environment. Station controls, workflow-tab synchronization, top-view toggle, pause controls, hero unfold/wireframe/reset, project briefs, category filters, command navigation, and credential tilt were tested. Layouts at 320, 390, 768, 1024, and 1440 px did not overflow horizontally. Both animations pause under reduced-motion preferences. Simulated WebGL failure preserves text alternatives, station selection, and project dialogs. No-JavaScript checks retain the project cards and both static scene alternatives. No JavaScript page errors appeared in these targeted checks.
