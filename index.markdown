---
layout: default
title: The Web Development Benchmarks Game
---

# The Web Development Benchmarks Game

## (with apologies to the [Computer Language Benchmarks Game](http://benchmarksgame.alioth.debian.org/))

There are so many web frameworks around these days. Wouldn't it be
nice if there were a standard "benchmark" project, like cookbooks or
blog engines, that we could use to compare frameworks? Something small enough to write in an afternoon or two, but complex enough to illustrate how to handle real-world problems in a given framework?

From the [history](http://benchmarksgame.alioth.debian.org/dont-jump-to-conclusions.php#history) of the original Benchmarks Game:

> When I started this project, my goal was to compare all the major
> scripting languages. Then I started adding in some compiled languages
> for comparison ... and it's still growing with no end in sight. I'm
> doing it so that I can learn about new languages, compare them in
> various (possibly meaningless) ways, and most importantly, have some
> fun.

Unlike the original Benchmarks Game, our benchmarks are things like: lines of code, amount of time to build features, template language features, number of existing libraries, *et cetera*.

So far:

### Tic Tac Toe

A simple web-based version of Tic-Tac-Toe. Demonstrates:

- the framework's persistence layer, in particular relations between
  objects and custom queries
- unit tests
- built-in user system (if any)
- templates
- form handling

Features:

- a user can register, log in, log out
- a user can create games against other users
- a user can see the games in which it is their turn
- a user can make moves in games when it is their turn
- completed games display the winner or that the game tied

Implementations:

- [ttt_django15 (Django 1.5)](http://github.com/web-dev-benchmarks-game/ttt_django15). A
  pretty standard Django site, mostly contained in a "tictactoe"
  app. A separate "simplereg" app lets users register. Does some
  slickness in the "create game" page to reorder the user list to put
  the current user first.

- [ttt_yesod124 (Yesod
  1.2.4)](https://github.com/web-dev-benchmarks-game/ttt_yesod124).
  Yesod is one of the better-known Haskell web frameworks. Yesod comes
  with out-of-the-box support for authentication using Gmail. All
  parts of the website, including HTML/JS/CSS templates, are compiled
  to leverage the type system as much as possible.
