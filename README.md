# Showcase

Everything you watch, read, play and listen to, in one place, with the few
people whose taste you trust. This plugin brings Showcase into Claude.

## What you can do

- **Just say it.** "Add Severance, I'm on season 2", "Sam loved this one",
  "I finished Piranesi". Showcase files it on your shelves: Wishlist, On now
  and Showcase.
- **Pick together.** "What should Sam and I watch tonight?" gets an answer
  from both your lists and what the people you follow loved, not from an ad.
- **Keep your place.** "I'm on episode 4" is remembered, on your phone a
  moment later.
- `/next` asks what you're in the mood for, then picks from your list.
  `/watching` shows what you're partway through. `/import` helps bring in a
  Netflix, Letterboxd or Goodreads export.

Shows, films, books, games and podcasts. Everything here is the same list as
the Showcase app at [showcase.chat](https://showcase.chat).

## How it works, and what it sends

The plugin connects Claude to one remote server, Showcase's own:
`https://showcase.chat/api/mcp/showcase`. What you say about titles and the
people you follow is sent there, Showcase answers, and Claude repeats the
answer. Nothing is sent anywhere else, and the plugin runs no code on your
machine: it is the connection, the skills above, and a short description of
how Showcase thinks.

Signing in is OAuth, with the same Google or Apple account you use on
showcase.chat. There is nothing to paste. Showcase keeps what you say to it
in your own Showcase chat, so you can see it there; the
[privacy policy](https://showcase.chat/privacy) says what is kept and for how
long. For people 18 and over.

## Installing

From Claude's directory: find Showcase under Plugins and choose **Add**, then
sign in when Claude asks.

Claude Code or Cowork, from this repository:

```
claude plugin marketplace add keithguerin/showcase-plugin
claude plugin install showcase@showcase-plugin
```

## Support

[support@showcase.chat](mailto:support@showcase.chat) ·
[showcase.chat/support](https://showcase.chat/support) ·
[Terms](https://showcase.chat/terms) · [Privacy](https://showcase.chat/privacy)

Made by Block & Tackle LLC. MIT licensed.
