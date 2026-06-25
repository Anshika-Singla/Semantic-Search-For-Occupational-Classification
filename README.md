```markdown
# Semantic Search for Occupational Classification

A Flask web application designed for intelligent job matching and standardized occupational classification using semantic analysis. The system maps user-inputted job descriptions or natural language profiles to standardized occupational categories.

## Features

- **User Authentication**: Register and login securely
- **Occupational Search**: Search for occupations or roles using natural language descriptions
- **Semantic Matching**: Uses AI (Sentence Transformers) to find and classify relevant jobs based on semantic context rather than just exact keywords
- **Industry & Experience Filtering**: Filter jobs by industry sectors and experience level
- **Job Results & Analysis**: View, compare, and analyze job recommendations and taxonomy matches

## Tech Stack

- **Backend**: Flask, Flask-SQLAlchemy, Flask-Login, Flask-Bcrypt
- **Database**: SQLite
- **AI/ML**: Sentence Transformers, Scikit-learn
- **API**: RapidAPI Job Search
- **Translation**: Deep Translator
- **Data Processing**: Pandas

## Requirements

- Python 3.7+
- All dependencies in `requirements.txt`

## Installation

1. Clone the repository:
```bash
git clone [https://github.com/YOUR_USERNAME/Semantic-Search-Occupational-Classification.git](https://github.com/YOUR_USERNAME/Semantic-Search-Occupational-Classification.git)
cd Semantic-Search-Occupational-Classification

```

2. Create and activate a virtual environment:

```bash
# Windows
python -m venv venv
venv\Scripts\activate

# macOS/Linux
python3 -m venv venv
source venv/bin/activate

```

3. Install the required dependencies:

```bash
pip install -r requirements.txt

```

---

## ⚙️ Configuration

Create a `.env` file in the root directory of your project to store your configurations and API keys:

```env
FLASK_APP=run.py
FLASK_ENV=development
SECRET_KEY=your_super_secret_session_key
RAPIDAPI_KEY=your_rapidapi_job_search_key

```

---

## 🚀 Database Setup & Execution

1. Initialize the SQLite database:

```bash
python -c "from app import db, create_app; create_app().app_context().push(); db.create_all()"

```

2. Launch the Flask development server:

```bash
flask run

```

The application will now be running locally at `http://127.0.0.1:5000/`.

---

## 📂 Project Structure

```text
├── app/
│   ├── __init__.py       # App factory & extension initialization
│   ├── models.py         # SQLAlchemy Database models (User, Job, Taxonomy, etc.)
│   ├── routes.py         # Web routes & authentication logic
│   ├── templates/        # Jinja2 HTML templates
│   ├── static/           # CSS, JavaScript, and images
│   └── utils/
│       ├── semantic.py   # Sentence Transformer matching logic
│       └── api_handler.py# RapidAPI & translation fetching utils
├── instance/             # Local SQLite database file location
├── requirements.txt      # Project library dependencies
├── run.py                # Main application entry point
└── .env                  # Environment configuration (git ignored)

```

## 🛡️ License

This project is open-source and available under the [MIT License](https://www.google.com/search?q=LICENSE).


```

```
