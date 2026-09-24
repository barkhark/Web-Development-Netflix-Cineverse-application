# CineVerse

CineVerse is a full-stack movie and series application made using React and Django. It allows users to browse movies, search and filter them, and also add, edit and delete movies.

## Technologies Used

* React
* Vite
* Django
* Django REST Framework
* SQLite
* HTML and CSS
* JavaScript

## Project Structure

```text
Cineverse Application/
├── backend/
└── frontend/
```

### Backend

The backend is developed using Django and Django REST Framework.

It handles:

* Movie data
* Add movie
* Edit movie
* Delete movie
* API requests
* Database operations

SQLite is used as the database.

### Frontend

The frontend is developed using React and Vite.

It contains:

* Movie cards
* Search
* Movie and series filter
* Sorting
* Movie details
* Favourite movies
* Add movie
* Edit movie
* Delete movie

## How React and Django are Connected

React frontend sends requests to the Django REST API using HTTP and JSON.

```text
React
  ↓
Django REST API
  ↓
Django
  ↓
SQLite
```

The React frontend does not directly access the SQLite database. It gets the movie data from the Django API.

## API Endpoints

| Method | URL                 | Work                 |
| ------ | ------------------- | -------------------- |
| GET    | `/api/movies/`      | Get all movies       |
| POST   | `/api/movies/`      | Add movie            |
| GET    | `/api/movies/<id>/` | Get one movie        |
| PUT    | `/api/movies/<id>/` | Update movie         |
| PATCH  | `/api/movies/<id>/` | Update part of movie |
| DELETE | `/api/movies/<id>/` | Delete movie         |

## How to Run the Project

### Backend

Open a terminal and go to the backend folder:

```bash
cd backend
```

Activate the virtual environment if required and install the packages:

```bash
pip install django djangorestframework django-cors-headers
```

Run migrations:

```bash
python manage.py migrate
```

Start Django:

```bash
python manage.py runserver
```

Backend will run on:

```text
http://127.0.0.1:8000/
```

API:

```text
http://127.0.0.1:8000/api/movies/
```

### Frontend

Open another terminal:

```bash
cd frontend
```

Install the packages:

```bash
npm install
```

Start React:

```bash
npm run dev
```

Frontend will run on:

```text
http://localhost:5173/
```

## CRUD Operations

In this project I implemented CRUD operations for movies.

* **Create** – Add a new movie
* **Read** – View movies from the database
* **Update** – Edit movie details
* **Delete** – Delete a movie

The data is stored in the SQLite database through Django.

## Main Features

* Browse movies and series
* Search movies
* Filter movies and series
* Sort movies
* Add movie
* Edit movie
* Delete movie
* Favourite movies
* Movie details
* YouTube trailer
* Django Admin

## Conclusion

This project helped me understand how a React frontend can communicate with a Django backend using REST API. I also learned how CRUD operations work and how data is stored in a database.

The basic flow of the project is:

```text
User
 ↓
React + Vite
 ↓
HTTP + JSON
 ↓
Django REST Framework
 ↓
SQLite Database
```
