# Task Manager

A modern, responsive web application built with Flask for managing tasks. Features user authentication, task creation, editing, and status tracking with a beautiful UI.

## Features

- **User Authentication**: Register and login with username/password
- **Task Management**: Create, edit, and delete tasks
- **Status Tracking**: Update task status (Pending, In Progress, Completed)
- **Dashboard**: View all your tasks in an organized table
- **Responsive Design**: Works on desktop, tablet, and mobile devices
- **Modern UI**: Beautiful gradient design with smooth transitions and animations

## Tech Stack

- **Backend**: Flask (Python web framework)
- **Database**: SQLite with SQLAlchemy ORM
- **Authentication**: Flask-Login
- **Frontend**: HTML5, Jinja2 templates, CSS3
- **Styling**: Custom responsive CSS with modern gradients and effects

## Project Structure

```
Task-manager/
├── app.py                    # Main Flask application
├── config.py                 # Configuration file
├── README.md                 # This file
├── task_manager.db          # SQLite database (auto-created)
├── static/
│   └── css/
│       └── style.css        # Main stylesheet
└── templates/
    ├── base.html            # Base template with header
    ├── login.html           # Login page
    ├── register.html        # Registration page
    ├── dashboard.html       # Main task dashboard
    ├── add_task.html        # Add new task form
    └── edit_task.html       # Edit task form
```

## Installation

### Prerequisites
- Python 3.7 or higher
- pip (Python package manager)

### Setup Steps

1. **Clone the repository** (if applicable) or navigate to the project folder:
   ```bash
   cd "Task-manager"
   ```

2. **Create a virtual environment** (recommended):
   ```bash
   python -m venv venv
   ```

3. **Activate virtual environment**:
   - On Windows:
     ```bash
     venv\Scripts\activate
     ```
   - On macOS/Linux:
     ```bash
     source venv/bin/activate
     ```

4. **Install dependencies**:
   ```bash
   pip install flask, flask-sqlalchemy, flask-login, pymysql, cryptography
   ```

5. **Run the application**:
   ```bash
   python app.py
   ```

6. **Open in browser**:
   Navigate to `http://localhost:5000`

## Usage

### Getting Started

1. **Register**: Click on "Create Account" to create a new user account
2. **Login**: Enter your credentials to log in
3. **Dashboard**: View your tasks on the main dashboard

### Managing Tasks

- **Add Task**: Click "+ Add Task" button, enter task title, and submit
- **Edit Task**: Click "Edit" on any task to modify the title or status
- **Change Status**: Update status between Pending, In Progress, and Completed
- **Complete Task**: Click "Complete" to mark a task as completed
- **Delete Task**: Click "Delete" to remove a task (confirmation required)
- **Logout**: Click "Logout" to exit your account

## Database Models

### User Model
- `id`: Primary key
- `username`: Unique username (string, max 100 chars)
- `password`: User password (string, max 100 chars)

### Task Model
- `id`: Primary key
- `title`: Task title (string, max 200 chars)
- `status`: Task status - Pending, In Progress, Completed (default: Pending)
- `user_id`: Foreign key linking to User

## Features Details

### Status Badges
- **Pending**: Yellow badge - awaiting action
- **In Progress**: Blue badge - currently being worked on
- **Completed**: Green badge - finished tasks

### Security
- Login required for all task operations
- Session management with Flask-Login
- Task isolation - users can only see their own tasks

### Responsive Design
- Desktop: Full width with optimized layout
- Tablet: Adjusted spacing and button sizes
- Mobile: Single column layout with touch-friendly buttons

## Styling

The application uses a modern color scheme:
- **Primary Colors**: Purple/Blue gradient (#667eea to #764ba2)
- **Background**: White cards on gradient background
- **Accents**: Green (success), Red (danger), Blue (info)

## Future Enhancements

- Task priority levels
- Due dates and reminders
- Task categories/tags
- Task descriptions
- Collaborative task sharing
- Email notifications
- Dark mode

## Troubleshooting

### Database Issues
- Delete `task_manager.db` to reset the database (you'll lose all data)
- Database is recreated automatically on next run

### Login Issues
- Make sure you've registered before login
- Case-sensitive username and password

### CSS Not Loading
- Clear browser cache (Ctrl+Shift+Delete or Cmd+Shift+Delete)
- Make sure `static/css/style.css` exists in the project

## License

This project is open source and available for educational and personal use.

## Support

For issues or questions, please check the Flask and Flask-SQLAlchemy documentation:
- [Flask Documentation](https://flask.palletsprojects.com/)
- [Flask-SQLAlchemy](https://flask-sqlalchemy.palletsprojects.com/)
- [Flask-Login](https://flask-login.readthedocs.io/)

---

**Happy task managing!** 🚀
