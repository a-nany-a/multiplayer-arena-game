## Files and what they do

`main.py`: Entry point of the backend; initializes FastAPI, builds face encoding cache at startup, and manages WebSocket connections.


`database/sql.py` – Manages MySQL operations such as user storage, status updates, and Elo ratings.

`database/mongo.py` – Handles MongoDB operations for storing and retrieving profile images.


`utils/face_auth.py` – Connects login requests to the facial recognition system using cached encodings.

`utils/facial_recognition_module.py` – BlacUSE my_app_db;
k-box module that detects faces and computes/compares encodings.

`utils/cache.py` – Stores the in-memory face encoding cache shared across the backend.

`utils/scraper.py` – Scrapes profile images from student websites and stores them in databases.


`public/login.html` – Login page that captures webcam input for facial authentication.

`index.html` – Main frontend page (likely lobby/game UI entry point).

`js/login.js` – Handles webcam capture and sends login requests to backend.

`css/styles.css` – Styles for the frontend UI.

<br><br>
Screenshots of our AI chats

This part is mostly on how we got started

![alt text](image.png)

![alt text](image-1.png)

![alt text](image-2.png)

![alt text](image-3.png)

![alt text](image-4.png)<br>

This part is mostly for backend and integrating it with frontend + websockets(chat links have been put up here)

https://chatgpt.com/share/69e64cfd-2664-83e8-b580-a23e81d6dde8<br>
https://chatgpt.com/share/69e64da5-5d04-83e8-887b-218a399759f0<br>
https://chatgpt.com/share/69e64e42-f6fc-83e8-92e1-06ea827bfe8b<br>
https://chatgpt.com/share/69e64ed8-7aec-83e8-bd67-b722f3dbd5f5<br>

<br>
To start the backend run - uv run uvicorn main:app --host 0.0.0.0 --port 8000
To start thr frontend server run - python -m http.server 5500
To get to the login page http://<IP address>:5500/public/login.html