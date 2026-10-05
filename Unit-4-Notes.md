## Step 0

- `vite.config.js` still does not contain the server proxy to `https://localhost:3001` in the exemplar.
- There is no .gitignore in the exemplar, `node_modules` may end up being committed.
- `server/config/` and its files from Unit 3 are completely missing and replaced by `db/db.js` with just a connection string instead of the config that was set up in previous labs. There is no mention of any switching to this format between labs. The example connection string holds sensitive data that would normally be in their `.env` which would not be committed, but here it is.
- `server/package.json` does not have the `start` and `reset` scripts set up as previous labs did.
- `server.js` is inconsistent with how it would be carried over from lab 3.
- `data/gifts.js` is missing. Inconsistent with previous labs where it's required for running `npm run reset`.
- `routes/gifts.js` not set up with the route for getting gift by ID as created in previous lab.
- `controllers/gifts.js` also missing function for getting gift by ID as created in previous lab.
- Exemplar did not include dotenv package, which is what students have been using for the past 3 labs. Even after running `npm i` in the server directory, they will get an error stating that the dotenv is not found.
- `client/src/App.jsx` has the fetch set for the url `http://localhost:3000/gifts` but that url is not valid if they are setting the backend up to hit `localhost:3001` like in previous labs. It should also reflect the work done in Lab 3 with using `await fetch("/gifts")`
- `client/src/pages/GiftDetails.jsx` has the `useEffect` hook set up differently to what was done in the previous lab.

## Step 1

- Instruction says to move the new css files in the `css` directory, but this lab does not have a `css` directory. The css files for each page were just stored in the same directory.

## General Comment

The exemplar files should not be differing drastically from how it was set up in the lab if it is going to be provided to students. Currently, the exemplar repos are set up as if only to be used for demonstration, rather than for downloading and starting with a "fresh" copy of the lab repo. The labs have set steps so the outcome is expected to always look the same, so the files provided as the fresh copy should match exactly what those steps look like, otherwise the students will waste a lot of time trying to fix the lab before they reach the implementation of important concepts.
