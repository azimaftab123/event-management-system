# EventHub — Event Management Portal

A complete full stack web app for creating, browsing, and registering for events.

## Tech stack (maps to 4 core subjects)
1. **Frontend** — HTML5, CSS3, vanilla JavaScript (`frontend/`)
2. **Backend / Server** — Node.js + Express REST API (`backend/server.js`)
3. **Database** — JSON file-based data store (`backend/data/db.json`), storing users, events, and registrations
4. **Authentication & Security** — JWT tokens + bcrypt password hashing

## How to run

### 1. Backend
```
cd backend
npm install
npm start
```
Runs on `http://localhost:5000`

### 2. Frontend
Open `frontend/index.html` in your browser
(or serve it with `npx serve frontend`)

### 3. Login
Use the pre-filled demo account:
- Email: `demo@eventhub.com`
- Password: `demo1234`

Or register a new account from the Register tab.

## Features
- User registration & login (JWT-based auth, bcrypt password hashing)
- Browse all upcoming events with live capacity tracking
- Create new events (become the organizer)
- Register / cancel RSVP for events
- "My Events" — see events you're organizing, with delete option
- "My Registrations" — see events you've RSVP'd to
- Capacity limits — events show as "Full" once max capacity is reached
- Only the event organizer can edit/delete their own events

## Project structure
```
eventhub/
├── backend/
│   ├── server.js       # Express app: auth, events CRUD, registrations
│   ├── db.js            # simple JSON-file DB helper
│   ├── package.json
│   └── data/db.json      # "database" — users, events, registrations
└── frontend/
    ├── index.html
    ├── style.css
    └── app.js            # calls the API with fetch()
```

## Notes for submission
- Push this whole folder to a GitHub repo and submit that repo link.
- For a live demo link: deploy the backend on Render/Railway and the frontend on Vercel/Netlify (update `API_URL` in `app.js` to the deployed backend URL).
- This demonstrates: frontend, backend, database, and authentication with real-world CRUD + relational data (events ↔ registrations ↔ users).
