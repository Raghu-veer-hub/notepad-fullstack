
# NotePad App (Django & React)

**NotePad** is a simple notepad application built with **Django** for the backend and **React.js** for the frontend. Users can create, edit, view, and delete notes.

## Features

- **Create Notes**: Add new notes.
- **Edit Notes**: Edit existing notes.
- **Delete Notes**: Delete notes.
- **View Notes**: View all saved notes.

## Tech Stack

- **Frontend**: React.js, Tailwind CSS, Vite
- **Backend**: Django
- **Database**: SQLite (Django's default)

## Project Structure

```
diginotes/
├── diginotes/                   # Main Django project folder
│   ├── __pycache__/             # Compiled Python files
│   ├── __init__.py              # Project initialization
│   ├── asgi.py                  # ASGI configuration
│   ├── settings.py              # Django settings
│   ├── urls.py                  # URL routing for the project
│   └── wsgi.py                  # WSGI configuration
├── notesapp/                    # Django app for managing notes
│   ├── __pycache__/             # Compiled Python files
│   ├── migrations/              # Database migrations
│   ├── __init__.py              # App initialization
│   ├── admin.py                 # Django admin configurations
│   ├── apps.py                  # App configuration
│   ├── models.py                # Database models for notes
│   ├── serializers.py           # Serializers to convert models to JSON
│   ├── tests.py                 # Unit tests
│   ├── urls.py                  # URL routing for the notes app
│   └── views.py                 # Views for handling requests
├── static/                      # Static files like images, CSS, JS
├── .DS_Store                    # System file (macOS)
├── db.sqlite3                   # SQLite database
├── manage.py                    # Django project manager
├── frontend/                    # React frontend
│   ├── dist/                    # Compiled CSS files
│   ├── public/                  # Public files
│   ├── src/                     # React source code
│   ├── .gitignore               # Git ignore file
│   ├── eslint.config.js         # ESLint configuration
│   ├── index.html               # Main HTML file for React
│   ├── package.json             # Node.js dependencies
│   ├── README.md                # Frontend README
│   ├── tailwind.config.js       # Tailwind CSS configuration
│   └── vite.config.js           # Vite configuration for bundling
└── .DS_Store                    # System file (macOS)
```

## Setup Instructions

### Requirements

- Python 3.x
- Node.js and npm

### Backend Setup (Django)

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/diginotes.git
    cd diginotes
    ```

2. Install the Python dependencies:
    ```bash
    cd diginotes
    pip install -r requirements.txt
    ```

3. Set up the database:
    ```bash
    python manage.py migrate
    ```

4. Run the Django server:
    ```bash
    python manage.py runserver
    ```

The backend server will run at `http://localhost:8000`.

### Frontend Setup (React.js)

1. Go to the `frontend` folder:
    ```bash
    cd frontend
    ```

2. Install the necessary frontend dependencies:
    ```bash
    npm install
    ```

3. Start the React app:
    ```bash
    npm run dev
    ```

The React frontend will be accessible at `http://localhost:5173/`.

### API Endpoints

The backend provides the following API endpoints:

- `POST /api/notes/` - Create a new note
- `GET /api/notes/` - Get all notes
- `PUT /api/notes/{id}/` - Edit a note
- `DELETE /api/notes/{id}/` - Delete a note

### How to Use the App

1. Open the React frontend app at `http://localhost:5173/`.
2. Use the interface to create, edit, and delete notes.
3. The backend handles the data storage and returns the notes as JSON.

## Project Files Overview

### React Files

- **App.jsx**: Main entry point for React app.
- **components/**: Contains reusable UI components like `NavBar`, `NoteCard`, and `Loader`.
- **layouts/MainLayout.jsx**: Layout for the main pages.
- **pages/**: Contains pages like `AddNotePage`, `HomePage`, `NoteDetailPage`, and `EditNotePage`.
- **tailwind.config.js**: Configuration for Tailwind CSS.

### Django Files

- **models.py**: Defines the structure of the notes in the database.
- **serializers.py**: Serializes the note model to JSON format for the frontend.
- **views.py**: Handles HTTP requests to perform CRUD operations on notes.
- **urls.py**: URL routing for the backend API endpoints.

## License

This project is open-source and available under the MIT License.

