# Tableau de Suivi — Engagements & KPI

A client-side web application for tracking contractual commitments and evaluating their Key Performance Indicators (KPIs).

## Features

- **Load JSON Data**: Import engagement data from JSON files
- **Visual Dashboard**: View all engagements with completion status indicators
- **KPI Evaluation**: Rate each KPI's confidence (Oui/Non/Probablement) and importance (Haute/Moyenne/Faible)
- **Auto-Save**: Selections are automatically saved to browser localStorage
- **Filtering**: Search and filter by domain, KPI name, or completion status
- **Excel Export**: Download your evaluations as an Excel file

## Live Demo

Visit: `https://<your-username>.github.io/<repo-name>/`

## Quick Start

### Option 1: Open Locally
1. Download or clone this repository
2. Open `index.html` in your browser
3. Load your JSON data file

### Option 2: GitHub Pages
1. Fork this repository
2. Go to Settings > Pages
3. Select "Deploy from a branch" and choose `main`
4. Access at `https://<username>.github.io/<repo>/`

## JSON Data Format

Your JSON file must be an array of engagement objects:

```json
[
  {
    "Domaine": "Category Name",
    "Référence contractuelle": "4.1",
    "Engagement": "Description of the commitment...",
    "Points détaillés de l'engagement": [
      "Detail point 1",
      "Detail point 2"
    ],
    "Indicateurs & KPI": [
      {
        "Nom_KPI": "KPI Name",
        "Définition": "What this KPI measures",
        "Unité": "unit (e.g., %, oui/non)",
        "Périodicité": "Frequency",
        "Méthode_de_calcul": "Calculation method",
        "Source_donnée": "Data source"
      }
    ]
  }
]
```

See [sample-data.json](sample-data.json) for a complete example.

## Usage Guide

### 1. Load Data
Click "Choose File" and select your JSON file. The engagements will appear as cards.

### 2. Filter & Search
- Use the search bar to find specific engagements or KPIs
- Filter by domain, KPI name, or completion status

### 3. Evaluate KPIs
- Click on an engagement card to open the KPI panel
- For each KPI, select:
  - **Confiance**: Oui / Non / Probablement
  - **Importance**: Haute / Moyenne / Faible
- Selections are saved automatically

### 4. Track Progress
Cards show completion status:
- **Gray**: Not started (no KPIs rated)
- **Blue**: Partially complete (some KPIs rated)
- **Green**: Complete (all KPIs rated)

### 5. Export Results
Click "Exporter Excel" to download your evaluations as an Excel file.

## Data Persistence

- Data is saved in your browser's localStorage
- Selections persist across sessions on the same browser/device
- **Warning**: Clearing browser data will erase all selections

## Browser Support

- Chrome 90+
- Firefox 88+
- Edge 90+
- Safari 14+

## Technology Stack

- Vanilla JavaScript (ES6+)
- Bootstrap 5.3.2
- SheetJS (xlsx) for Excel export

## License

MIT License

## Author

Made by Youssef Chigane
