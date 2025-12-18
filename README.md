## Movie Reviews & News (Django)

Simple Django web application that lets you browse a list of movies with images and external links, and read a feed of news posts ordered by date. It is built as a learning project using Django 4 and Bootstrap.

### Features

- **Movie catalog**
  - List of movies with title, description and poster image.
  - Optional external URL for each movie (e.g. trailer or more info).
  - Search bar to filter movies by title (`?searchMovie=`).

- **News section**
  - `News` model with headline, body and date.
  - News page that shows all posts ordered by most recent first.

- **UI & layout**
  - Responsive layout using Bootstrap (navbar and footer in `base.html`).
  - Carousel section on the home page to highlight upcoming movies.

### Project structure (simplified)

- **`moviereviers/`** – main Django project (settings, URLs, templates base).
- **`movie/`** – movies app (`Movie` model, home & about views, `home.html`).
- **`news/`** – news app (`News` model, news view, `news.html`).
- **`media/movie/images/`** – sample movie poster images (used by `Movie.image`).

### Technology stack

- **Backend**: Python 3, Django 4.2
- **Database**: SQLite (default Django configuration)
- **Frontend**: HTML, Bootstrap 4/5 CDN

### Getting started (local development)

1. **Clone the repository**

   ```bash
   git clone <your-repo-url>
   cd TallerDjango2
   ```

2. **Create and activate a virtual environment (recommended)**

   ```bash
   python -m venv venv
   venv\Scripts\activate  # On Windows
   # source venv/bin/activate  # On macOS/Linux
   ```

3. **Install dependencies**

   This project mainly depends on Django 4.x:

   ```bash
   pip install "django>=4.2,<5.0"
   ```

4. **Apply migrations**

   ```bash
   python manage.py migrate
   ```

5. **Create a superuser (optional, for admin)**

   ```bash
   python manage.py createsuperuser
   ```

6. **Run the development server**

   ```bash
   python manage.py runserver
   ```

7. **Open the app in your browser**

   - Movies home: `http://127.0.0.1:8000/`
   - News page: check the URL configured in `moviereviers/urls.py` (commonly `/news/`).

### Media & static files

- Movie images are stored under `media/movie/images/` and served via the `Movie.image` field.
- Static assets use Bootstrap CDN; extra static configuration can be expanded in `moviereviers/settings.py`.

