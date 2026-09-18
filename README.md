# AI Study Planner

### Problem Statement (Problem 16)
Build a simple, modern, beginner-friendly **AI Study Planner** web application that helps a student add subjects, create study tasks under those subjects, assign a study date to each task, track whether a task is Pending or Completed, and view everything together as a study plan dashboard.

### Assigned Feature Set (Set A)
1. Add Study Subjects
2. Create Study Tasks
3. Set Study Dates
4. Track Task Completion
5. Display Study Plan

## Features Implemented

| # | Feature | Where in the app |
|---|---------|-------------------|
| 1 | Add / view / delete subjects | Sidebar (left panel) |
| 2 | Create a task with a title, linked to a subject | "Create a Study Task" card |
| 3 | Set a study date for each task | Date picker inside the task form |
| 4 | Mark tasks Pending / Completed | Checkbox on every task card |
| 5 | Display the full study plan | Dashboard stats bar + Pending/Completed columns |

Extra touches (still simple, but make the app feel complete):
- Deleting a subject also removes its tasks (no orphaned data).
- Duplicate subject names are blocked.
- Server-side **and** client-side input validation.
- Toast notifications instead of ugly `alert()` popups.
- Fully responsive layout (usable on mobile).

## Technologies Used

| Layer | Technology | Why |
|-------|-----------|-----|
| Frontend | HTML5, CSS3, Vanilla JavaScript (fetch API) | No framework needed to understand — easy to explain line by line |
| Backend | Node.js + Express.js | Minimal, widely taught, easy REST API syntax |
| Database | MongoDB + Mongoose | Document database that maps naturally to JS objects |
| Dev tool | Nodemon (optional) | Auto-restarts server while developing |

## Folder Structure

```
ai-study-planner/
├── backend/
│   ├── config/
│   │   └── db.js               # MongoDB connection logic
│   ├── controllers/
│   │   ├── subjectController.js
│   │   └── taskController.js
│   ├── models/
│   │   ├── Subject.js
│   │   └── Task.js
│   ├── routes/
│   │   ├── subjectRoutes.js
│   │   └── taskRoutes.js
│   ├── .env.example
│   ├── package.json
│   └── server.js                # Entry point
├── frontend/
│   ├── css/style.css
│   ├── js/script.js
│   └── index.html
└── README.md
```

## Instructions to Run the Project

**Prerequisites:** Node.js (v18+) and MongoDB (local install, or a free MongoDB Atlas cluster).

```bash
# 1. Go into the backend folder
cd ai-study-planner/backend

# 2. Install dependencies
npm install

# 3. Create your .env file
cp .env.example .env
# then edit MONGO_URI inside .env if needed

# 4. Start MongoDB (if running locally)
mongod

# 5. Start the server
npm start
# or, for auto-restart during development:
npm run dev
```

Open your browser at **http://localhost:5000** — the backend also serves the frontend, so this one URL runs the whole app.

## AI Tools Used
- **Claude (Anthropic)** — used as a learning and development assistant to help design the project architecture, generate a first working draft of the code, and explain Express/Mongoose/REST concepts.

## Important AI Prompts / AI Usage
This section documents how AI was used, as required for academic honesty.

1. *"Create a practice problem set going easiest to hardest... [later replaced with the actual assignment]: Build a complete working project based on Problem 16 – AI Study Planner, with feature set A (add subjects, create tasks, set dates, track completion, display plan), using HTML/CSS/JS + Node/Express + MongoDB, with proper folder structure, validation, error handling, and an explanation of every part of the code."*
2. Follow-up questions asked while reviewing the generated code, such as: *"Explain how populate() works in Mongoose"*, *"Why do we separate routes and controllers?"*, and *"What viva questions might my teacher ask about this project?"*

AI was used to **scaffold and explain** the project. The final code was reviewed, understood, and can be explained part-by-part by the student (see the "Viva Questions" section shared separately / in the assignment write-up).

## Screenshots
_Add screenshots here before submission:_
1. Dashboard with subjects, task form, and study plan visible
2. Adding a new subject
3. Creating a new task with subject + date selected
4. A task marked as Completed (checkbox ticked, moved to Completed column)
5. Empty states (no subjects / no tasks yet)
6. MongoDB Compass or terminal showing the `subjects` and `tasks` collections with data

