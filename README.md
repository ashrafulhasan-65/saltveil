
# SaltVeil — Smarter Water. Safer Tomorrow.

**SaltVeil is a prototype coastal-water information platform designed to help communities in Satkhira, Bangladesh decide where salinity testing should be prioritised.** It brings together location-based context, environmental information and clearly labelled data sources to support better-informed decisions.

> **Important:** SaltVeil does not directly measure water salinity and does not replace laboratory or field testing. Any weather-based risk score is experimental and has not been scientifically validated as a salinity prediction model. Use it only as a prioritisation aid—not as proof that a water source is safe or unsafe.

## The problem

Coastal communities can face seasonal changes in water salinity, while reliable, recent measurements may not be available for every local water source. People need understandable information about where to investigate first—and they need to know when a data point was measured, where it came from and what it actually represents.

## The proposed approach

SaltVeil is being developed to make water-risk information easier to explore and communicate. It combines a map-based interface with environmental context and source transparency, with the goal of helping communities and local organisations prioritise follow-up testing.

### Intended capabilities

- **Map-based exploration:** view geographic context for the locations represented in the app.
- **Environmental context:** use weather information to show relevant conditions, without treating weather as a direct measurement of salinity.
- **Source and date transparency:** distinguish measured observations from environmental data and experimental indicators wherever the interface provides those details.
- **Testing-first guidance:** encourage users to confirm potential concerns with an actual water test.
- **Web-first prototype:** designed to be accessible in a modern browser and suitable for deployment with GitHub Pages.

*Features depend on the files and data currently included in this repository. A displayed location or risk indicator should not be assumed to represent a recent water-quality measurement unless its source and measurement date are explicitly shown.*

## Why SaltVeil is different

SaltVeil focuses not only on displaying a risk indicator, but also on communicating **what the evidence can and cannot tell us**. Historical river-water measurements, groundwater or tubewell measurements, weather observations and experimental scores are different types of information. They must not be treated as interchangeable.

## Data sources and limitations

The following sources provide background material for the project. They do not automatically mean that every dataset is integrated into the current prototype.

- **Soil Resource Development Institute (SRDI), Satkhira — published report (2023–24):** [Open report (PDF)](https://objectstorage.ap-dcc-gazipur-1.oraclecloud15.com/n/axvjbnqprylg/b/V2Ministry/o/office-srdi-satkhira/2024/12/368452989878461f803f42d7d223de0b.pdf)
- **Bangladesh Water Development Board (BWDB) — salinity-data availability page:** [Check listed data availability](https://www.hydrology.bwdb.gov.bd/includes/salinity_data_available_print.php?dist=&river=)
- **Open-Meteo — weather API documentation:** [API documentation](https://open-meteo.com/en/docs)
- **Kaliganj groundwater study (2024), Heliyon:** [Research article](https://doi.org/10.1016/j.heliyon.2024.e27857)
- **Coastal river/soil salinity study (2025), Scientific Reports:** [Research article](https://doi.org/10.1038/s41598-025-30639-5)
- **Satkhira groundwater study (2025):** [Research article](https://doi.org/10.1007/s10661-025-14002-9)

### Data interpretation rules

1. **Always check the measurement date.** Historical data must be labelled historical; it must not be presented as a current reading.
2. **Check the water type and location.** A river measurement is not a tubewell measurement, and a nearby station does not prove the quality of a household's source.
3. **Keep units clear.** Electrical conductivity (EC), reported for example in dS/m or mS/cm, is not the same unit as salinity in parts per thousand (ppt). Values must not be silently converted or compared as though they were identical.
4. **Weather is not salinity.** Rainfall, temperature and other weather variables may provide context, but they do not establish a water source's salinity on their own.
5. **No unsupported “safe water” claims.** A source should not be declared safe or unsafe by SaltVeil without appropriate measurements and applicable health guidance.
6. **No unverified recent readings.** If a recent local measurement cannot be verified, the app should say so rather than estimate or invent a measurement.

## Technology

The web prototype uses HTML, CSS and JavaScript. The map interface uses [Leaflet](https://leafletjs.com/). Weather data may be requested from [Open-Meteo](https://open-meteo.com/), depending on the configuration in the app files.

## Run locally

1. Download or clone this repository.
2. Keep the project files in their existing folder structure.
3. Open `index.html` in a modern browser. If browser restrictions prevent a feature from working, serve the folder with a local static web server instead.

No build step is expected for a plain HTML/CSS/JavaScript version of the prototype. This may change if the project structure changes.

## Deploy with GitHub Pages

1. Ensure the main page is named `index.html` and is in the repository root (unless the Pages source is configured for a different folder).
2. Open **Settings → Pages** in the GitHub repository.
3. Under the build/deployment source, choose **Deploy from a branch**.
4. Select the `main` branch and `/ (root)`, then save.
5. Open the published URL shown by GitHub Pages and test the map, data labels and links on both mobile and desktop.

## Current status

SaltVeil is an early-stage prototype. Its purpose is to improve access to and interpretation of water-risk information and to help prioritise field testing. The project still requires validation against recent, location-specific field measurements before any predictive score could be considered scientifically reliable.

## Roadmap

- Add clear source, station/location, water-type, unit and observation-date labels to every measurement.
- Connect verified, location-specific monitoring data where access and reuse permissions allow.
- Test the interface with coastal residents and local water-testing practitioners.
- Evaluate any proposed risk score against real field measurements before making predictive claims.
- Improve accessibility, including plain-language and Bangla explanations.

## Project author

**Ashraful Hasan**  
Project: **SaltVeil — Salinity Risk Mapping for Satkhira, Bangladesh**

## Disclaimer

SaltVeil is an informational prototype, not a certified water-quality testing service or medical/public-health authority. Do not make drinking-water decisions solely from this website. Test the actual source using an appropriate method and follow guidance from qualified local authorities.

---

**Smarter Water. Safer Tomorrow.**
