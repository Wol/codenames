Client
- Angular (JS?)

Server
- PHP Backend
-- Laravel driven interface

- Websocket
-- NodeJS script
--- Faye.JS - Communication between the client and nodejs app. Also allows other clients to get an update


- Database
-- MySQL


-- The Gist ---
The main PHP app will handle the request to open up a game based on session id / user ID. 

Select 25 random word cards. Assign their teams against the game.


Determine which mode game is being played (1 + spymaster, 1 vs 1 + spymaster, or team vs team)

There's always a 'team' assigned, this way it handles the single vs multiple user case.

Spymasters don't need to belong to teams (e.g. in the 1vs1 + spymaster case), but they can do (in the team vs team case)

Need a log of clues (+ number). Can also save the cards which were intended to be answered by this clue (not shown until end), and a count of how many the answering team thinks that theyve handled from it.

Need a lot of guesses, by which person / which team, and can also mark down here which clue they think the guess was for. This should show up any 'accidental' answers.

