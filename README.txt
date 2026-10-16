Playhead — portfolio of Yevhen Tykva, ready for Netlify

Deploy: drag this whole folder onto your site's Deploys page on app.netlify.com (or app.netlify.com/drop).
Local preview needs a server (WebGL can't read images from file://):  npx serve .

What's inside
  index.html, about.html, contact.html   pages (minified)
  css/  js/                              minified, file names carry a content hash → cached for a year, new names on every change
  img/                                   every project screen in two widths: 800 px (phones) and 1600 px (desktop, tablets, retina);
                                         the page picks one by screen width × pixel ratio. Page snapshots (for the reel transitions) are single.
  _headers                               cache rules and two security headers
  netlify.toml                           /about and /contact also work without .html

Sound is synthesised in the browser (Web Audio): there are no audio files to load.
Libraries (three.js, GSAP) come from public CDNs, so a visitor who has them cached from other sites gets them for free.
