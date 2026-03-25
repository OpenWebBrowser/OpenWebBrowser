# OpenWebBrowser Frontend Roadmap

## Scope
- This repo contains **only** the static frontend for GitHub Pages.
- All backend functionality (fetching, AI, search, scraping) lives in a separate repository.
- The frontend calls the backend via HTTPS API endpoints.

## File Structure (created)
- `apps/web/` — GitHub Pages site (static)
- `apps/web/public/` — public assets (index, icons)
- `apps/web/src/` — frontend source
- `scripts/` — automation and deployment helpers

## Milestones
1. **MVP scaffolding**
   - Static site skeleton with two modes: **AI** and **Web Search**.
   - Configuration for backend base URL (env or config file).

2. **Web Search mode**
   - UI for search input and results list.
   - Call backend `/search` and render results.
   - Link-out handling (open in new tab).

3. **AI mode**
   - UI for prompt input and streaming response display.
   - Call backend `/ai` (SSE or fetch streaming).
   - Basic error states and retries.

4. **Content view**
   - Readable view for fetched pages (using backend cleaned content).
   - Source attribution and metadata (title, URL, favicon).

5. **Deployment**
   - GitHub Pages build + deploy workflow.
   - Custom domain support (optional).

## Backend Contract Needed
- `/search` -> returns structured results
- `/ai` -> returns streaming or chunked responses
- `/fetch` -> returns cleaned content for display

## Next Decisions Needed
- Backend base URL
- Streaming protocol (SSE vs fetch streaming)
- UI design direction
