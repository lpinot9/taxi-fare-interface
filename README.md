# NY Taxi Fare Prediction Interface

A web interface for predicting taxi fares in New York City using machine learning.

## Features

- Interactive map powered by Mapbox
- Location autocomplete for pickup and dropoff
- Real-time fare prediction
- Visual route display on the map

## Setup Instructions

### Configuring the Mapbox Token

This application uses Mapbox for mapping functionality. To keep the Mapbox access token secure, it needs to be configured as a GitHub Secret.

#### Steps to Configure:

1. **Get a Mapbox Access Token**
   - Sign up or log in at [Mapbox](https://www.mapbox.com/)
   - Navigate to your [Account page](https://account.mapbox.com/)
   - Copy your public access token (starts with `pk.`)

2. **Add the Token to GitHub Secrets**
   - Go to your GitHub repository
   - Click on **Settings** → **Secrets and variables** → **Actions**
   - Click **New repository secret**
   - Name: `PUBLIC_TOKEN`
   - Value: Paste your Mapbox access token
   - Click **Add secret**

3. **Deploy**
   - Once the secret is configured, push changes to the `master` branch
   - GitHub Actions will automatically deploy the site to GitHub Pages
   - The workflow will inject the token during deployment
   - The site will be available on the `gh-pages` branch

## Deployment

The site is automatically deployed to GitHub Pages when changes are pushed to the `master` branch. The deployment workflow:

1. Checks out the code
2. Injects the Mapbox token from GitHub Secrets
3. Deploys to the `gh-pages` branch

## Development

To run this locally for development:

1. Clone the repository
2. Create a local copy of `script.js` (e.g., `script.local.js`) and replace `${PUBLIC_TOKEN}` with your own Mapbox token
3. Update the script reference in `index.html` to point to your local file
4. Open `index.html` in a web browser
5. **Important:** Make sure `script.local.js` is not tracked by git (add it to `.gitignore` if needed)

Alternatively, you can use a local web server and inject the token via environment variables.

## Technologies Used

- HTML/CSS/JavaScript
- [Mapbox GL JS](https://docs.mapbox.com/mapbox-gl-js/) - Interactive maps
- [Mapbox Geocoder](https://github.com/mapbox/mapbox-gl-geocoder) - Location search
- [Bootstrap](https://getbootstrap.com/) - UI framework
- [Flatpickr](https://flatpickr.js.org/) - Date/time picker

## License

This project was created as part of [Le Wagon](https://www.lewagon.com/) coding bootcamp.
