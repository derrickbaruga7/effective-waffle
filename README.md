# Incident JSON Builder & Viewer

A simple, self-contained web application that parses tab-delimited incident data into a structured JSON format. Features include filtering, searching, and exporting functionality.

## Features

- **Data Parsing**: Converts tab-delimited incident data into structured JSON
- **Search & Filter**: Filter by department, incident type, and PPE usage
- **JSON Export**: Download filtered results as JSON
- **Responsive Design**: Works on desktop and mobile devices
- **Interactive UI**: View detailed JSON for each incident

## Deployment to GitHub Pages

### Option 1: Using GitHub Web Interface

1. Create a new repository on GitHub
2. Upload the `index.html` file to the repository
3. Go to repository Settings → Pages
4. Under "Source", select the branch (usually `main` or `master`)
5. Click Save
6. Your site will be available at `https://yourusername.github.io/repository-name/`

### Option 2: Using Git Command Line

```bash
# Initialize git repository
git init

# Add the index.html file
git add index.html README.md

# Commit the changes
git commit -m "Initial commit - Incident JSON Builder"

# Add your GitHub repository as remote
git remote add origin https://github.com/yourusername/repository-name.git

# Push to GitHub
git push -u origin main

# Enable GitHub Pages in your repository settings
```

### Option 3: Quick Deploy Script

```bash
# Create a new repository on GitHub first, then run:
git init
git add .
git commit -m "Deploy Incident JSON Builder to GitHub Pages"
git branch -M main
git remote add origin https://github.com/yourusername/your-repo-name.git
git push -u origin main
```

Then go to your repository settings and enable GitHub Pages from the main branch.

## Local Development

To run locally, simply open `index.html` in a web browser. No build process or server required!

```bash
# Open in default browser (macOS)
open index.html

# Open in default browser (Linux)
xdg-open index.html

# Open in default browser (Windows)
start index.html
```

Or use a local server:

```bash
# Using Python 3
python -m http.server 8000

# Using Node.js (with http-server)
npx http-server

# Using PHP
php -S localhost:8000
```

Then visit `http://localhost:8000` in your browser.

## Technology Stack

- **React 18** (via CDN)
- **Tailwind CSS** (via CDN)
- **Babel Standalone** (for JSX transformation)
- Pure JavaScript - no build process required

## Data Structure

Each incident is parsed into the following JSON structure:

```json
{
  "incident_data": {
    "date": "3/28/2023",
    "summary": "Description of incident...",
    "injury_incident_type": "Foreign Body",
    "department": "Fabrication",
    "ppe_used": "yes",
    "object_involved": "Body"
  },
  "safety_manual_reference": {
    "section": "4.1 PPE Requirements - Welding Operations",
    "requirement": "Workers must wear safety glasses..."
  },
  "causal_factor_definitions": {
    "people_factors": [...],
    "process_factors": [...]
  },
  "analysis": {
    "identified_people_factors": [],
    "identified_process_factors": [],
    "reasoning": ""
  }
}
```

## Customization

To customize the data:

1. Open `index.html`
2. Find the `RAW` constant (around line 14)
3. Replace with your tab-delimited data
4. Ensure the header row matches the expected format

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## License

MIT License - feel free to use and modify as needed.

## Demo

Once deployed to GitHub Pages, your site will be live and accessible worldwide!
