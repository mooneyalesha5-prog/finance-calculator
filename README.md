# finance-calculator
Ashley value city
{
  "name": "Alesha Furniture Sales Calculator",
  "short_name": "Furniture Calc",
  "start_url": ".",
  "display": "standalone",
  "background_color": "#f5f7fb",
  "theme_color": "#0b4f9c",
  "description": "Furniture sales and financing calculator",
  "icons": [
    {
      "src": "data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 192 192'><rect fill='%230b4f9c' width='192' height='192'/><text x='50%' y='50%' font-size='100' font-weight='bold' fill='white' text-anchor='middle' dominant-baseline='middle'>FC</text></svg>",
      "sizes": "192x192",
      "type": "image/svg+xml",
      "purpose": "any maskable"
    }
  ]
}
.install-prompt { position: fixed; bottom: 20px; left: 14px; right: 14px; background: var(--blue); color: white; padding: 14px; border-radius: 12px; box-shadow: var(--shadow); z-index: 100; display: none; } .install-prompt button { width: 100%; border: 0; padding: 10px 14px; border-radius: 8px; font-weight: 800; cursor: pointer; }
self.addEventListener('install', (event) => {
  self.skipWaiting();
});

self.addEventListener('activate', (event) => {
  event.waitUntil(self.clients.claim());
});

self.addEventListener('fetch', (event) => {
  event.respondWith(
    fetch(event.request).catch(() => caches.match(event.request))
  );
});