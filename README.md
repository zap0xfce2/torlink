<p align="center">
  <img src="preview/splash.svg" alt="delugefinder, curated torrents straight from your terminal" style="max-width: 832px; width: 100%; height: auto;">
</p>

Finding a torrent these days sucks. One site is a minefield of fake download buttons. Another hides the real link under a popup that spawns two more tabs. And after all that, half the results are dead, zero seeders.

DelugeFinder is a torrent finder that lives in your terminal. One search checks a short list of reputable sources at once, and whatever you pick gets sent straight to your own [Deluge](https://deluge-torrent.org) instance over its Web UI — delugefinder itself never downloads anything.

## Get started

1. **Install Node** (from [nodejs.org](https://nodejs.org)) and have a Deluge Web UI reachable (local or remote).
2. **Open your terminal.**
3. **Start it:**

   ```sh
   npx dlfi
   ```

delugefinder opens straight to a search bar: search for what you want, paste in a magnet link or a bare infohash, or just press Enter on an empty box to browse the curated library. Press `o` once to point it at your Deluge Web UI (address + password); it's saved locally after that. From there it's all keypresses, nothing to memorize, and `?` brings up the full list anytime.

## Finding something

Type what you're looking for and press Enter. Results stream in from every source as they answer, tagged with size and how many people are sharing each one, so you can see what'll come down fast. Arrow to what you want and press `d` to send it to Deluge, or `y` to just copy the magnet link instead.

<p align="center">
  <img src="preview/browse.svg" alt="delugefinder's browse view: the sidebar, the search bar, and merged results from every source" style="max-width: 832px; width: 100%; height: auto;">
</p>

## What it searches

Type `p`

## Contributing

To run or work on DelugeFinder locally:

1. Clone the repository and open the folder.
2. Install dependencies:
   ```sh
   npm install
   ```
3. Run the development version:
   ```sh
   npm run dev
   ```
   Or build it and run the bundled version:
   ```sh
   npm run build
   npx dlfi
   ```

## Privacy

delugefinder itself never opens a connection to the torrent network — it only searches, then hands the chosen magnet link to your own Deluge instance over its Web UI. Everything after that (downloading, seeding, where files land) is Deluge's territory, configured however you already run it.
