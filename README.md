1. Clone the repo:
   ```bash
   git clone https://github.com/Durgadevi3105/rail.git
   cd rail
   ```
2. Create `.env` from example:
   ```bash
   cp .env.example .env
   # Edit `.env` as needed
   ```
3. Build and run:
   ```bash
   docker-compose up --build
   ```
4. Visit [http://localhost:8000/items/](http://localhost:8000/items/) in your browser.

To stop the project:
```bash
docker-compose down
```
