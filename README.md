# Plate Ledger

A single-file, no-build food tracker for people who eat the same handful of things every day. Track calories and macros by logging foods into scheduled meals, in grams or portions.

Everything lives in one `index.html`. There is no backend, no account, and no dependencies. The only external request is an optional Google Font, which falls back to system fonts.

## Features

- **Foods:** Enter calories, protein, carbs and fat per 100 g. Leave calories blank to calculate them (4/4/9). Add an optional portion size in grams to log "1 portion".
- **Meals:** Schedule meals by name, time and repeat days, such as Breakfast at 8:00 every day or a Morning snack on weekdays. Each day shows its meals in time order.
- **Recipes:** Combine foods into a batch, such as a large pan. Log `1`, `1/2` or `1 1/2` of it without weighing a portion. Tap an entry to see the ingredient amounts to plate.
- **Planned vs eaten:** Plan ahead and mark entries eaten, with the actual grams or portions. Totals count only what you ate, and planned items show as "projected".
- **Targets:** Set a daily or a weekly calorie target (one or the other), with progress and remaining.
- **Week view:** Averages, totals, and a bar per day.
- **Copy:** Copy an entry to any date, or copy a whole day into another. Copies to a future date become planned.
- **Backup:** Export and import everything as JSON.

## Use it

1. Host `index.html` on any static host (GitHub Pages, Netlify), or open it from a normal web address.
2. On a phone, use your browser's "Add to Home screen" to run it like an app.
3. Go to **Settings → Foods** and add your foods.
4. Go to **Settings → Meals** and set your schedule.
5. Log food from the **Today** tab.

## Your data

Data is stored in your browser's `localStorage`, on one device and one browser.

- It does not sync between devices.
- Clearing site data erases it. Use **Settings → General → Export backup** regularly.
- Opening the file straight from local storage (for example `file://` on Android) often doesn't persist data. The app shows a warning when saving is unavailable, so serve it from a web address instead.

## How the numbers work

- Macros are stored per 100 g. An entry's macros are grams ÷ 100 × the food's values.
- A recipe's per-gram values come from the total weight of its ingredients. `1` portion of a recipe is the whole thing, so weigh ingredients as you put them in.
- Recipe entries keep their logged grams. If you edit a recipe later, past entries aren't re-scaled.

## Limitations

- No cloud sync or multi-user support.
- No barcode scanning or food database. Foods are entered by hand.
- The Week view totals whole days, not individual meals.

## License

MIT
