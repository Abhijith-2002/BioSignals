# BioSignals - Video Anomaly Detection

## Project Description
BioSignals is a web application designed to detect unusual behavior in video streams. It provides an admin dashboard for uploading video files, which are then processed by a backend system using OpenCV to identify anomalies such as prolonged occupancy or too many entry/exit changes.

## Features
- **Admin Dashboard**: A user-friendly interface for uploading video files.
- **Video Analysis**: Backend processing of videos to detect unusual behavior.
- **Real-time Alerts**: (Future/Planned) Integration for displaying alerts based on detected anomalies.

## Technologies Used
- **Frontend**: HTML, CSS (adminstyles.css), JavaScript (adminScript.js)
- **Backend**: Python (Flask, OpenCV, imutils)

## Setup and Installation

### Prerequisites
- Python 3.x
- pip (Python package installer)
- npm (Node Package Manager) - if `server.js` is used for any frontend serving or build processes.

### Backend Setup

1.  **Clone the repository**:
    ```bash
    git clone <repository_url>
    cd BioSignals
    ```

2.  **Create a virtual environment (recommended)**:
    ```bash
    python3 -m venv venv
    source venv/bin/activate  # On Windows: `venv\Scripts\activate`
    ```

3.  **Install Python dependencies**:
    ```bash
    pip install -r requirements.txt
    # If requirements.txt is not present, install manually:
    pip install Flask opencv-python imutils python-dotenv
    ```

4.  **Environment Variables**:
    Create a `.env` file in the root directory with necessary environment variables.
    Example `.env`:
    ```
    # Add any environment variables required by your Flask app here
    # For example:
    # FLASK_APP=app.py
    # FLASK_ENV=development
    ```

### Frontend Setup (if applicable)

If there are Node.js dependencies or build steps for the frontend (indicated by `package.json` and `server.js`), follow these steps:

1.  **Install Node.js dependencies**:
    ```bash
    npm install
    ```

## Running the Application

### Start the Backend (Flask)

```bash
python app.py
```
The Flask application will typically run on `http://127.0.0.1:5000`.

### Start the Frontend Server (if applicable)

If `server.js` is used to serve static files or as a proxy:

```bash
npm start
```
Check `package.json` for the exact `start` script command.

## Usage

1.  Navigate to the admin dashboard in your web browser (e.g., `http://127.00.1:5000/`).
2.  Use the "Choose Video File" button to select a video from your local machine.
3.  Click "Upload and Analyze" to send the video to the server for processing.
4.  The backend will process the video, and any detected unusual behavior will be logged or indicated (depending on further UI implementation).

## Project Structure
- `app.py`: Main Flask application file, handles routes and video processing.
- `backend.py`: Contains the core video analysis logic using OpenCV.
- `templates/`: HTML templates for the web interface (e.g., `adminDashboard.html`).
- `static/`: Static assets like CSS (`adminstyles.css`) and JavaScript (`adminScript.js`).
- `uploads/`: Directory where uploaded video files are stored.
- `.env`: Environment variables for the application.
- `package.json`, `package-lock.json`, `server.js`: (If applicable) Node.js related files for frontend or server setup.

## Future Enhancements
- Display analysis results directly on the dashboard.
- Implement user authentication and authorization.
- Add a history of uploaded videos and their analysis reports.
- Improve video processing efficiency and add more sophisticated anomaly detection algorithms.
- Integrate real-time video stream analysis.
