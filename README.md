# Plant Disease Detection

A small Flask web app that uses a PyTorch convolutional neural network to classify plant leaf images into disease categories. The project includes a pretrained model, a simple UI to upload images, and a supplements marketplace page with recommendations.

Key components
- `Flask Deployed App/` — Flask application, templates, and static assets.
- `Model/` — notebooks and notes used for training the PyTorch `CNN` model.
- `plant_disease_model_1_latest.pt` — pretrained model (place this at the repository root).

Features
- Upload a leaf image and receive a disease prediction with description and suggested supplements.
- Simple, responsive UI powered by Bootstrap.
- Example test images in `test_images/` for quick validation.

Quick start (Windows)

1. Create a virtual environment and activate it:

```powershell
python -m venv venv
.\venv\Scripts\Activate.ps1   # PowerShell
# or: .\venv\Scripts\activate  # cmd
```

2. Install dependencies:

```powershell
pip install -r "Flask Deployed App\requirements.txt"
```

3. Download the pretrained model and place it at the repository root (one level above `Flask Deployed App`). The app expects the model file named `plant_disease_model_1_latest.pt`.

4. Run the Flask app from the `Flask Deployed App` folder:

```powershell
cd "Flask Deployed App"
python app.py
```

5. Open a browser and visit `http://127.0.0.1:5000/`.

Using the app
- Home: overview and navigation.
- AI Engine (`/index`): upload a leaf image and submit for analysis.
- Results (`/submit`): shows predicted disease, description, prevention steps, and a supplement recommendation (if available).
- Market: browse supplements and buy links.

Development notes
- Model code is in `Flask Deployed App/CNN.py` and training notebooks are in the `Model/` folder.
- The Flask app serves static assets from `Flask Deployed App/static/`. Some example images are stored in `Flask Deployed App/templates/` and are exposed via a small `/images/<filename>` route.

Troubleshooting
- If CSS or layout appears broken:
  - Verify `/static/css/style.css` is reachable in the browser (open `http://127.0.0.1:5000/static/css/style.css`).
  - Clear browser cache or hard-refresh (Ctrl+F5).
  - Ensure the app was started from the `Flask Deployed App` folder.
- If the model file is not found, confirm `plant_disease_model_1_latest.pt` is at the repository root (one level above `Flask Deployed App`).

Contributing
- Contributions are welcome. Please fork the repo, make changes, and open a pull request with a clear description.

License & contact
- This project is provided as-is for learning and experimentation. For questions or collaboration, open an issue or reach out via the contact page in the app.

Screenshots
See the `demo_images/` folder for screenshots of the UI.
