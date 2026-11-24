# FitTrack - Gym Management System

A full-stack web app for running a gym: admins manage members, trainers and the exercise library; trainers build workout plans for their members; members follow plans and track their progress over time.

Built as a single-page application in vanilla JavaScript with a Node.js/Express REST API and SQLite storage - no frontend framework, which meant building the routing, state handling and data visualization from scratch.

## Features

- Role-based access for Administrators, Trainers and Members
- Trainers create workout plans from a shared exercise library and assign them to members
- Members log weight and body-fat daily and see trends on interactive charts (Chart.js)
- Billing and payment history per member
- Real-time data sync across devices connected to the server

## Tech Stack

- Frontend: HTML5, vanilla JavaScript (ES6+), CSS3 with CSS variables, Chart.js
- Backend: Node.js, Express (REST API)
- Database: SQLite (better-sqlite3)

## Run It Locally

Requires Node.js 18+.

```bash
npm install
npm start
# open http://localhost:3000
```

## Project Structure

```
├── package.json      # Node dependencies and scripts
├── server.js         # Express API routes and server config
├── database.js       # SQLite schema and connection setup
├── db/               # SQLite database files
└── web/              # Static frontend
    ├── index.html    # SPA shell
    ├── styles.css    # Theme and layout
    ├── app.js        # UI router and controller
    └── db.js         # DataService wrapper for API calls
```

## What I Learned

- Designing a relational schema and writing the API layer around it (users, members, trainers, plans, exercises, billing)
- Building an SPA without a framework: client-side routing, async fetch wrappers, DOM rendering
- Structuring a project so the frontend, API and database layers stay separate
