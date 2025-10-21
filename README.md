# 🎉 Hacktoberfest 2025 — Weather App 🌦️

**Real-Time Weather Visualization with Dynamic Sky Animations**

---

## 🌍 About the Project

The **Weather App** is an interactive web project that brings weather data to life.
It fetches **live weather information** from an external API (like OpenWeatherMap or WeatherAPI) and displays it using beautiful **animated visuals** — including sun, clouds, rain, snow, and dynamic lighting based on the time of day.

The project is ideal for learning about **API integration**, **JavaScript DOM manipulation**, and **responsive web design** while creating something visually impressive.

---

## 🧠 Key Features

✅ Fetches **real-time weather** data for any city or your current location
✅ Displays **temperature**, **humidity**, **wind speed**, and **forecast conditions**
✅ Dynamic **sky animations** (sun, moon, clouds, rain, snow)
✅ Auto-detects **user’s location** with browser geolocation
✅ Supports **manual city search**
✅ **Responsive** on mobile and desktop
✅ Built for **Hacktoberfest 2025** — open for collaboration and learning

---

## 🏗️ Project Structure

```plaintext
/
├── index.html                 # Main webpage  
├── styles/                    # All styling files  
│   ├── main.css               # Core styles and animations  
│   └── responsive.css         # Media queries for mobile view  
├── scripts/                   # JavaScript logic for data and UI  
│   ├── weatherFetch.js        # Fetches live weather data from API  
│   ├── skyRenderer.js         # Handles animations for weather visualization  
│   ├── locationDetect.js      # Auto-detects user location via Geolocation API  
│   └── uiController.js        # Updates DOM and manages user interactions  
├── assets/                    # Images, icons, and background elements  
│   ├── icons/                 # Weather icons (sun, clouds, rain, etc.)  
│   └── images/                # Static backgrounds or visual overlays  
├── data/                      # (Optional) Sample JSON data for offline testing  
│   └── sampleWeather.json  
├── LICENSE                    # MIT License file  
└── README.md                  # This documentation  
```

### 📂 Folder Breakdown

* **styles/** → Manages UI theme, animations, layout responsiveness.
* **scripts/** → Contains JavaScript modules for fetching and rendering weather data.
* **assets/** → Static visual content like icons or background textures.
* **data/** → Sample files to test without API calls.

---

## 📊 Data Flow & System Design

### Step 1: Detect User Location

* Uses **Geolocation API** to retrieve latitude & longitude.
* Falls back to manual city input if location access is denied.

### Step 2: Fetch Weather Data

* Sends a request to the chosen API (e.g., OpenWeatherMap) using your **API key**.
* Receives data in JSON format containing:

  ```json
  {
    "main": { "temp": 29, "humidity": 75 },
    "weather": [{ "description": "clear sky", "icon": "01d" }],
    "wind": { "speed": 4.2 }
  }
  ```

### Step 3: Render Data & Animation

* The `skyRenderer.js` script analyses weather conditions and time (day/night).
* It displays appropriate animations:

  * ☀️ Clear sky → sun animation
  * 🌧️ Rain → falling droplets
  * 🌨️ Snow → drifting flakes
  * ⛅ Clouds → floating cloud layers

### Step 4: Update UI

* DOM elements (temperature, humidity, icons) are dynamically updated every few minutes.
* Background transitions smoothly between day/night gradients.

---

## 🛠️ Built With

| Technology                             | Purpose                             |
| -------------------------------------- | ----------------------------------- |
| **HTML5**                              | App structure & layout              |
| **CSS3 / SCSS**                        | Styling, animations, responsiveness |
| **JavaScript (ES6)**                   | Logic, data fetching, rendering     |
| **Weather API (e.g., OpenWeatherMap)** | Real-time weather data              |
| **Geolocation API**                    | Detects user location               |
| **Canvas / SVG**                       | Visual weather animations           |

---

## 🚀 Getting Started

### Prerequisites

* A **modern browser** (Chrome, Edge, Firefox, Safari)
* A **free API key** from [OpenWeatherMap](https://openweathermap.org/api)

### Installation

```bash
# Clone this repository
git clone https://github.com/Marcozkiller666/weather.git

# Navigate into the project directory
cd weather
```

Then, open **index.html** directly in your browser,
or use a local server for smoother development (e.g., Live Server in VS Code).

---

## ⚙️ Configuration

Create a file called `config.js` in the `scripts/` folder and add your API key:

```javascript
// config.js
const API_KEY = "your_api_key_here";
```

This will be imported by `weatherFetch.js` when making API requests.

---

## 💻 Usage

1. **Allow location access** when prompted, or manually type your city name.
2. Watch the dynamic background update to match current weather conditions.
3. Hover or tap the display to view details like temperature, humidity, wind speed, etc.
4. Use mobile or desktop — the layout adjusts automatically.

---

## 📸 Screenshots

| Clear Sky                                | Rainy Day                            | Snow Night                          |
| ---------------------------------------- | ------------------------------------ | ----------------------------------- |
| ☀️ ![clear](assets/images/clear-sky.png) | 🌧️ ![rain](assets/images/rainy.png) | ❄️ ![snow](assets/images/snowy.png) |

---

## 🤝 Contributing (Hacktoberfest 2025)

We welcome all contributions during **Hacktoberfest 2025**!
Join the fun, learn new skills, and make this weather app even better 🌈

### Steps to Contribute:

1. **Fork** the repository.
2. **Create a branch** for your feature or fix:

   ```bash
   git checkout -b feature/add-dark-mode
   ```
3. **Commit** your changes with a clear message:

   ```bash
   git commit -m "Added dark mode feature"
   ```
4. **Push** your branch and open a **Pull Request**.

---

### 💡 Ideas for Contribution

* Add **Dark/Light Mode** toggle
* Introduce **hourly forecast** display
* Improve **animations** for smoother performance
* Add **unit conversion** (°C ↔ °F)
* Enhance **UI accessibility** (color contrast, ARIA labels)
* Include **offline mode** using cached data

---

## 🧰 Testing

To test your changes:

* Use browser dev tools to simulate various geolocations and weather conditions.
* Verify animation and UI responsiveness.
* Check console for API or JavaScript errors.

---

## 📬 Contact

**Author:** [Marco Ziller](https://github.com/Marcozkiller666)
**Repository:** [github.com/Marcozkiller666/weather](https://github.com/Marcozkiller666/weather)
**Email:** [marcoz.developer@example.com](mailto:marcoz.developer@example.com) *(replace with actual contact if public)*

---

## 📝 License

This project is licensed under the **MIT License**.
You are free to use, modify, and distribute this code with attribution.
See the [LICENSE](LICENSE) file for full details.

---

## 🙏 Acknowledgements

* Thanks to **OpenWeatherMap** (or your chosen API provider) for real-time data.
* Inspired by developers who blend technology with creativity.
* Thanks to all **Hacktoberfest 2025** participants for contributing and learning together.

---

### 🌈 Final Note

> “Code can predict storms, paint sunsets, and make the world a bit brighter.”

Built with ☀️ + ❤️ by **Marco Ziller** — Happy Hacktoberfest 2025! 🎃

