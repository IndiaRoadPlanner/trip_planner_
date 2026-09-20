# India Road Planner Premium

A fresh responsive multi-page travel planner starter built with HTML, CSS and vanilla JavaScript modules.

## Run locally
Because the project uses JavaScript ES modules, serve the folder using a local web server rather than opening `index.html` as a `file://` URL. For example, with Python installed:
```bash
python -m http.server 8000
```
Then visit `http://localhost:8000`.

## Publish
Upload the extracted project contents to a GitHub repository. For GitHub Pages, select the branch and root folder in **Settings → Pages**. Keep the folder structure intact.

## Pages
- `index.html` — homepage
- `pages/road-trip.html` — Google Maps route calculation, map display, fuel estimate and nearby attraction search
- `pages/destinations.html` — searchable starter destination list
- `pages/flights.html` — flight search handoff
- `pages/trains.html` — railway search/official-service links
- `pages/transport.html` — transport modes and provider links
- `pages/stays.html` — nearby stays/rest-stop search handoff
- `pages/ai-assistant.html` — AI prompt builder (local template, no AI API call)
- `pages/my-trip.html` — local trip notes and browser-only reminder saving
- `pages/integrations.html`, `pages/about.html`, `pages/privacy.html`

## Important integration notes
This is a functional front-end starter, not a production-connected booking platform.
- **Google Maps:** Road Trip uses the Maps JavaScript Directions service to obtain route distance and estimated duration, then calculates fuel from distance ÷ efficiency × entered fuel price. Nearby attractions are retrieved through Places. Set a browser key in the script URL in `pages/road-trip.html`, restrict it by HTTP referrer, enable Maps JavaScript API and Places API, configure billing/quotas, and do not commit an unrestricted key. Duration is a route estimate, not a guarantee; traffic and road conditions can change. Google Maps route data depends on API availability and supported modes.
- **Flights:** Skyscanner links are a handoff/search entry point. Affiliate tracking, deep links and API access depend on the relevant partner programme and approval. Confirm current partner terms before launch.
- **Railways:** links lead to official or established railway resources. IRCTC booking automation/API access is not included; use only officially authorized access and comply with terms.
- **AI:** the page creates a prompt that can be copied into an AI service. A production AI assistant needs a backend endpoint and securely stored API credentials.
- **SMS/location alerts:** this starter only saves a reminder in browser local storage. Real SMS needs a backend, consent, an SMS provider, verified sender/recipient setup and destination-arrival detection. Background location tracking requires explicit user permission and platform support.
- **Hotels and points of interest:** nearby search is handed off to Google Maps. Live inventory, prices and booking need a provider integration and partner access.

No API secrets are included. Check provider terms, privacy obligations, local rules and security before launching.
