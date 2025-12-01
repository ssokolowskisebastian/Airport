Docker (PostgreSQL)
# start (build images and run containers)
docker compose up --build
# stop
docker compose down



Setup (local, SQLite)
python -m venv .venv
. .venv/Scripts/activate  # Windows PowerShell
source .venv/bin/activate  # macOS/Linux

pip install --upgrade pip
pip install -r requirements.txt

cp .env.example .env
# By default SQLite will be used (no extra steps needed)

python manage.py migrate
python manage.py createsuperuser
python manage.py loaddata fixtures/seed.json
python manage.py runserver


Here are some screenshots of the application:

<table>
  <tr>
    <td>
      <img src="1" alt="Screenshot 1" width="300"/>
      <p align="center"><em>Screenshot 1: Home Page</em></p>
    </td>
    <td>
      <img src="2.png" alt="Screenshot 2" width="300"/>
      <p align="center"><em>Screenshot 2: Dashboard</em></p>
    </td>
  </tr>
  <tr>
    <td>
      <img src="3.png" alt="Screenshot 3" width="300"/>
      <p align="center"><em>Screenshot 3: Feature View</em></p>
    </td>
    <td>
      <img src="4.png" alt="Screenshot 4" width="300"/>
      <p align="center"><em>Screenshot 4: Settings</em></p>
    </td>
  </tr>
</table>
