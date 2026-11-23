<h1 align="center">rails-longest-word-game</h1>

<p align="center"><b>Sessions, form round-trips, and the first call out to someone else’s API.</b></p>

<p align="center">
  <img alt="Ruby on Rails" src="https://img.shields.io/badge/Ruby%20on%20Rails-D30001?style=flat-square&logo=rubyonrails&logoColor=white">
  <img alt="Ruby" src="https://img.shields.io/badge/Ruby-CC342D?style=flat-square&logo=ruby&logoColor=white">
  <img alt="Le Wagon" src="https://img.shields.io/badge/Le%20Wagon-FF0000?style=flat-square">
</p>

<p align="center"><sub>🎓 Le Wagon full-stack bootcamp · 2021 · Week 6 · State and external APIs</sub></p>

---

## What this is

[Le Wagon](https://www.lewagon.com/) is a nine-week, full-time coding bootcamp — roughly 400 hours of Ruby, object-oriented design, SQL, front-end and Ruby on Rails, nine in the morning until seven at night, homework on top. ([programme](https://www.lewagon.com/web-development-course))

This repository is one step of that programme, kept exactly as it was written in 2021 — **before AI assistants, autocomplete or anything that writes code for you.** Every line here was typed by hand, every error read and understood. That is the point of keeping it.

## What is in it

A word game: the app deals a grid of letters, the player submits the longest word they can find, and the app scores it — which requires checking that the word is both *buildable from the grid* and *an actual English word*.

```ruby
get 'new',   to: 'games#new', as: :new
get 'score', to: 'games#score'
```

The grid has to survive the round trip between the two pages, and the dictionary check has to leave the application entirely.

## What it taught me

Two things that look simple and are not. **State:** HTTP forgets everything between requests, so the grid must be deliberately carried across — the first encounter with the session. **The network:** an external API can be slow, can be down, and can answer something you did not expect, so the response has to be parsed rather than trusted.

## Stack

`Ruby on Rails 6 · Ruby · sessions · external HTTP API`

---

<p align="center">
  <sub>Part of my 2021 Le Wagon apprenticeship — the full set is on <a href="https://github.com/LouisNeubauer">my profile</a>.<br>
  For what I build now, start there.</sub>
</p>
