# Family Kitchen Hub

A friendly family kitchen dashboard. The site is hosted in two places: the live Wix Headless site and GitHub Pages. The repository's `index.html` is the source file for both. Both versions read and write the same Wix CMS collection, so changes made on either site appear on both.

## Shared kitchen plan

Planner items are stored in the Wix CMS collection **Family Kitchen Planner** (`kitchenPlanner`) on the Wix site. The collection contains groceries, main dishes, desserts, repairs, and maintenance. Every visitor can read, add, edit, check off, and remove items; changes are stored centrally and refresh on other open pages.

The website validates names, categories, and dates before saving, escapes saved text before displaying it, and ignores planner rows with an unsupported category or missing title. Do not put private household details in this public collection.

## Deploy

GitHub Actions publishes the repository to GitHub Pages when `main` changes. The Wix Headless site is a separate deployment and must also receive the updated `index.html` to update the Wix-hosted version. Both deployments use the same public Wix OAuth client ID and central CMS data. The client ID is a public identifier; never add a client secret or privileged API key to the page.

## Wix CMS structure

Collection ID: `kitchenPlanner`

- `title`: item name
- `category`: `Grocery`, `Main dish`, `Dessert`, `Repair`, or `Maintenance`
- `scheduledDate`: optional date in `YYYY-MM-DD` form
- `details`: optional note
- `completed`: checkbox state

The collection is public-read and public-write to match the site's public editing behavior. Wix collection field types describe the stored data but are not server-side schema validation; the page validates submitted values before sending them. Keep this board limited to ordinary, non-sensitive kitchen planning.
