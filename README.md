# Little Kitchen Hub

A kid-friendly family kitchen dashboard hosted with GitHub Pages. The page is static; its weekly groceries, meal dates, and repair schedule are read from the Wix CMS collection **Kitchen Planner**.

## Update the kitchen plan

Open the [Kitchen Planner in Wix](https://manage.wix.com/dashboard/3f0926cf-6ae9-4c55-9bc8-87a284cf999d/wix-cms/data/kitchenPlanner) and add or edit rows. Use these **Category** values:

- `Grocery`
- `Main dish`
- `Dessert`
- `Repair`
- `Maintenance`

The live dashboard reads updates from Wix automatically; editing plan rows does not require changing or rebuilding the website.

## Hosting

GitHub Actions publishes the repository's static files to GitHub Pages whenever a change is pushed to `main`.

The Wix collection is public-read and admin-edit-only. Avoid putting private household details in it.

