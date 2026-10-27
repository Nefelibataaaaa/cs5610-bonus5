# Bonus 5: Svelte Grid

A 2x2 grid built with Svelte 5 and Vite for the bonus assignment. Clicking a cell
toggles it between white and black, and the counter above the grid tracks how many
cells are currently on.

## Running

```sh
npm install
npm run dev
```

Vite prints the local URL (usually http://localhost:5173).

To build for production, run `npm run build` and then `npm run preview`.

## Files

- `src/App.svelte` holds the four cell states and renders the grid
- `src/Cell.svelte` is the button for a single cell
- `src/main.js` mounts the app
