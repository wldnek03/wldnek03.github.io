---
title: Joo Movie (Netflix Clone)
date: 2024-08-01
image:
  focal_point: 'top'
---

[🎬 Live Demo](https://joomovie.netlify.app/) ・ [🐙 GitHub Repository](https://github.com/wldnek03/jiwoo.github.io)

## Overview

A web application that clones Netflix's UI and features. Built with **React**, with a user interface modeled after Netflix. Created for learning purposes and deployed on **Netlify**.

## Features

- **Login**: Animated transitions between login and sign-up; on login, the header's login indicator changes to the email's first segment and a logout button; passwords are authenticated using the TMDB API
- **Home**: Banner displays a popular movie's poster, title, and description with Play / Details buttons; below the banner, lists of popular movies and TV shows; clicking a poster shows a heart icon and saves the title to the wishlist
- **Popular**: Grid view and list view of popular titles; grid view blocks scroll and uses pagination; list view uses infinite scroll; a Top button scrolls back to the top; clicking a poster saves it to the wishlist
- **Search**: Search movies and TV shows; click a poster to view details and trailer; recent searches are saved; sort by genre, rating, language, and various criteria; a Reset button restores the default popular-movies list
- **Detail Page**: Detailed info and trailer for each movie or TV show
- **Wishlist**: Displays posters saved from the home page and Popular page
- **Responsive Design**: Optimized UI across devices

## Homepage

🔗 [Joo Movie — joomovie.netlify.app](https://joomovie.netlify.app/)

## Tech Stack

- **Frontend**: React, JavaScript, HTML, CSS
- **State Management**: React Hooks (`useState`, `useEffect`)
- **Styling**: CSS
- **API**: TMDB API (movie data)
- **Deployment**: Netlify
<head>
    <style>
        p {
            text-align: justify;
        }
    </style>
</head>
