# KeepNote - A Simple Note-Taking Web Application

A lightweight, web-based note-taking application built with FastAPI and MongoDB. KeepNote allows users to create, store, and manage their notes with a clean, responsive interface.

## 🚀 Features

- **Create Notes**: Add new notes with title and description
- **Mark Important**: Flag important notes for quick identification
- **Responsive Design**: Modern Bootstrap-based UI that works on all devices
- **Real-time Storage**: Notes are stored in MongoDB for persistence
- **Simple Interface**: Clean and intuitive user experience

## 🛠️ Tech Stack

- **Backend**: FastAPI (Python web framework)
- **Database**: MongoDB (NoSQL database)
- **Frontend**: HTML5, Bootstrap 5, CSS3
- **Template Engine**: Jinja2
- **Database Driver**: PyMongo

## 📋 Prerequisites

Before running this application, make sure you have:

- Python 3.7+ installed
- MongoDB Atlas account (or local MongoDB instance)
- pip (Python package installer)

## 🚀 Installation & Setup

### 1. Clone the Repository

```bash
git clone <your-repository-url>
cd KeepNote
```

### 2. Create Virtual Environment

```bash
python -m venv venv
```

**For Windows:**
```bash
venv\Scripts\activate
```

**For macOS/Linux:**
```bash
source venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Database Configuration

The application is configured to use MongoDB Atlas. Update the connection string in `config/db.py`:

```python
MONGO_URI = "your-mongodb-connection-string"
```

### 5. Run the Application

```bash
uvicorn index:app --reload
```

The application will be available at `http://localhost:8000`

## 📁 Project Structure

```
KeepNote/
├── config/
│   └── db.py              # Database configuration
├── models/
│   └── note.py            # Pydantic models
├── routes/
│   └── note.py            # API routes and handlers
├── schemas/
│   └── note.py            # Data serialization schemas
├── static/
│   └── style.css          # Static CSS files
├── templates/
│   └── index.html         # HTML templates
├── index.py               # Main application entry point
├── requirements.txt       # Python dependencies
└── README.md             # Project documentation
```

## 🎯 Usage

### Creating a Note

1. Navigate to the home page (`http://localhost:8000`)
2. Fill in the note title and description
3. Optionally check the "important" checkbox
4. Click "Submit" to save the note

### Viewing Notes

- All notes are displayed on the home page
- Important notes are marked for easy identification
- Notes are automatically loaded from the database

## 🔧 API Endpoints

- `GET /` - Display the main page with all notes
- `POST /` - Create a new note

## 🗄️ Database Schema

Each note document in MongoDB contains:
- `title` (string): The note title
- `desc` (string): The note description
- `important` (boolean): Whether the note is marked as important

## 🚀 Deployment

### Local Development

```bash
uvicorn index:app --reload --host 0.0.0.0 --port 8000
```

### Production Deployment

For production deployment, consider:
- Using a production WSGI server like Gunicorn
- Setting up proper environment variables
- Implementing security best practices
- Using a reverse proxy like Nginx

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

## 🙏 Acknowledgments

- FastAPI for the excellent web framework
- MongoDB for the database solution
- Bootstrap for the responsive UI components

---

**Note**: This is a simple note-taking application suitable for learning and personal use. For production applications, consider implementing additional features like user authentication, note editing, deletion, and search functionality.
