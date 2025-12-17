# NY Taxi Fare Prediction Interface

A web interface for predicting taxi fares in New York City using machine learning.

## Features

- Interactive map powered by Mapbox
- Location autocomplete for pickup and dropoff
- Real-time fare prediction
- Visual route display on the map



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
