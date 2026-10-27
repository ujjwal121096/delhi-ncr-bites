# Delhi NCR Bites — website starter

A responsive React + Vite prototype for a Delhi NCR restaurant discovery website.

## What works in this prototype
- Responsive homepage and restaurant cards
- Search by restaurant, locality, city or cuisine
- Cuisine, area, rating and price filters
- Sort by recommended, rating or review-count label
- Save/favourite restaurants in the current page session
- Restaurant detail modal
- Demo Google sign-in and API buttons that clearly explain they are placeholders

## Important demo limitations
- Restaurant information, ratings, counts and review snippets are illustrative sample content. They are **not live Google data** and should not be published as factual ratings/reviews.
- Google login is not connected yet.
- Google Places API is not connected yet.
- Saved places are held in React state and are not persistent.
- Images are loaded from Unsplash URLs, so an internet connection is needed for those images.

## Run locally (Windows / Mac)
1. Install Node.js LTS from https://nodejs.org/.
2. Extract this folder.
3. Open a terminal inside the `delhi-ncr-bites` folder.
4. Run:

   ```bash
   npm install
   npm run dev
   ```

5. Open the local URL Vite prints, usually `http://localhost:5173`.

## Next steps for real launch
1. Create a Supabase project and configure Google OAuth in Supabase and Google Cloud Console.
2. Add a Supabase client using `.env.local` (copy `.env.example` and fill in your project URL and publishable key).
3. Deploy server-side Supabase Edge Functions for Places API calls. Keep the Google API key and Supabase service-role key out of frontend code.
4. Add server-side admin authorization, request throttling, quotas and budget alerts before discovery automation.
5. Implement the Google Places API policies: only store permitted data; Place IDs can be stored, but do not bulk-copy Google reviews; display Google and reviewer attributions as required and link to Google Maps.
6. Replace all demo data with live API results and add privacy/terms pages.

## Build for deployment

```bash
npm run build
```

The production output is generated in `dist/`. You can deploy the Vite app to a supported static host. Configure the real environment variables in the hosting dashboard, not in committed source files.
