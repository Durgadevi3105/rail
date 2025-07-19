# RailS Dockerized Setup

This project is a Dockerized Django application based on [s2pl/Rail](https://github.com/s2pl/RailSathiBE), using PostgreSQL as the database. It supports fast setup via Docker Compose and is ready for local development and testing.

## 🚀 Setup Instructions

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Durgadevi3105/rail.git
   cd rail
   ```

2. **Create your `.env` file from the example:**
   ```bash
   cp .env.example .env
   # Edit `.env` as needed for DB name, user, password (these should match values in docker-compose.yml)
   ```

3. **Build and run the containers:**
   ```bash
   docker-compose up --build
   ```

   - This command will build the Docker image for Django, start the PostgreSQL container, run migrations, and start the development server.

4. **Access the application:**
   - Visit: [http://localhost:8000/items/](http://localhost:8000/items/) in your browser to verify the Django project is running.

5. **Stopping the containers:**
   ```bash
   docker-compose down
   ```

---

## ⚡️ API Usage

- Main endpoint: `/items/`
- Django admin: `/admin/` (if enabled)

---

## 🗒️ Assumptions & Notes

- Uses default PostgreSQL settings from `.env.example`
- Hot-reloading is enabled via Docker volume (so code changes reflect instantly during development)
- If there are issues with migrations or DB connection, check your `.env` and `settings.py` for correct values

---

## 🎁 Bonus Features (if added)

- **wait-for-it.sh:** Handles database startup timing for Django app
- **Django admin:** Superuser creation via Docker
- **Swagger docs:** Auto-generated API documentation

---

## 💡 Troubleshooting

- If the app doesn’t start, run `docker-compose logs web` and `docker-compose logs db` to check for errors.
- For DB issues, make sure your `.env` matches your Django `settings.py` and `docker-compose.yml`.
- If you change dependencies, rebuild with:
  ```bash
  docker-compose build
  ```

---

## 📬 Submission

- Repo link: `https://github.com/Durgadevi3105/rail`
- Screen recording: Upload to Google Drive as instructed and share the link.

---

Feel free to copy and use or further edit this README for clarity and completeness.  
If you need specific help with any file or want to add bonus features, just ask! 
