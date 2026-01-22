# artifacts-mmo-controller

A monorepo for the GeekZoo Artifacts MMO controller

# Overview
This is a controller for the game Artifacts MMO. The goal of this is to allow the player to automate as many actions as possible. 

The backend is written in Go leveraging the Encore framework. We use a postgresql database to store the game state data since much of it does not change. We also leverage caching for game images to reduce the calls we need to make. This means on first app startup there is some initialization that happens which takes some time. Future starts will be much faster.

# What can I do?
For now it will serve as a basic controller allowing you to do the following:

1. Control all player characters - up to 5
2. Gather a specific resource in a loop until a condition is met
3. Fight a specific monster in a loop until a condition is met
4. Craft an item

# What will the UI show me?
The UI will allow us to do the following:

1. A dashboard will show you some basic information about all your characters at once
2. Selecting a character will allow you to control that character and get more detailed information
3. The monsters page will allow you to see all the monsters in a card view with an iimage of the monster as well as its stats. We will also show the mob drops so you can filter by thos
4. Show you all the resources that you might want to gather in a card format with an image.
5. Show you all the avaliable weapons with images, stats, and what is needed to craft them
6. Select a gather, fight or crafting loop to run with a specific end condition

# Backend - Go, Encore and PostgreSQL
For the backend we are using Go and the encore framework. This allows us to create the Artifacts API integrations and the game engine automations in a highly performant way. We use our PostgreSQL database to store game state.

# Frontend - SvelteKit, TailwindCSS, BitsUI
We are leveraging Svelte 5 and SvelteKit for the frontend UI because of its built in reactivity. We ensure we use a Svelte 5 / runes first approach limiting $effects to help with debugging.
