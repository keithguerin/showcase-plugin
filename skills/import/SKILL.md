---
name: import
description: Bring someone's history from Netflix, Letterboxd or Goodreads into Showcase. Use when the user asks to import, bring over or copy their viewing history, watch history, films, shows, watchlist or books from one of those services into Showcase.
---

Showcase takes a whole history in one go at **Settings → Import**: it shows
where every title will go, adds them with one tap, and has Undo. Your job is
to get the export file into the person's Downloads and open that screen.
Don't add the titles one by one with the Showcase tools instead; that skips
the preview and the Undo.

## Netflix

1. If you can use the person's own browser (Claude in Chrome, or computer
   use), open `https://www.netflix.com/viewingactivity` there. Otherwise give
   them the steps in plain words: on netflix.com, Account, their profile,
   Viewing activity.
2. Each profile has its own history. If Netflix asks who is watching, ask the
   person which profile is theirs; don't pick one.
3. At the bottom of Viewing activity, click **Download all**. The browser
   saves `NetflixViewingHistory.csv` to Downloads.
4. Open `https://showcase.chat/settings?room=import&source=netflix`. Tell them
   to tap **Choose the file**, pick `NetflixViewingHistory.csv` from
   Downloads, look over where each title goes, and tap **Add**. A browser
   tool can't choose a file for them, so this tap is theirs.

## Letterboxd and Goodreads

Same idea, the same screen:

- Letterboxd: `https://letterboxd.com/settings/data/`, then **Export your
  data**; it downloads a zip. Then
  `https://showcase.chat/settings?room=import&source=letterboxd`.
- Goodreads: `https://www.goodreads.com/review/import`, then **Export
  Library**; when the link appears, click it to download the file. Then
  `https://showcase.chat/settings?room=import&source=goodreads`.

## Never

- Type or ask for anyone's password. If a site is signed out, ask the person
  to sign in themselves, then carry on.
- Open the downloaded file and paste its contents anywhere. It goes from
  Downloads straight into Showcase.

## What they'll see

Films go to Showcase. A show watched in the last 30 days goes to On now,
older ones to Showcase. Anything already on their shelves stays exactly where
it is, and titles Showcase can't find are listed, not guessed.
