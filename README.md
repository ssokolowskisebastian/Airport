#Setup – Docker (PostgreSQL)
docker compose up --build

#Setup – Local (SQLite)
python -m venv .venv
source .venv/bin/activate     # Linux/macOS
. .venv/Scripts/activate      # Windows PowerShell

pip install --upgrade pip
pip install -r requirements.txt

cp .env.example .env
python manage.py migrate
python manage.py createsuperuser
python manage.py loaddata fixtures/seed.json
python manage.py runserver

