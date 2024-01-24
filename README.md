# EMIT - Earth Surface Mineral Dust Source Investigation

![EMIT Logo](https://media.discordapp.net/attachments/821655672536956942/1160247599757017120/image_3.png?ex=6533f7c8&is=652182c8&hm=19ea0cc3ca9834df934a0995f01ab47d401a15501dbcb78b9d6ee9d89812c528&=&width=266&height=110)

## Introduction

EMIT (Earth Surface Mineral Dust Source Investigation) is a NASA Earth Ventures-Instrument (EVI-4) Mission designed to map the mineral composition of arid dust source regions using imaging spectroscopy in the visible and short-wave infrared range. The mission aims to model the role of mineral dust in the radiative forcing (warming or cooling) of the atmosphere.

## Mission Details

- Developed at NASA’s Jet Propulsion Laboratory.
- Launched on July 14, 2022.
- Observes Earth from outside the International Space Station.
- Data is delivered to the NASA Land Processes Distributed Active Archive Center (DAAC) for use by researchers and the public.

## About Methane Gas Detection

EMIT is equipped to detect methane gas emissions. Methane is a significant greenhouse gas, and EMIT helps in pinpointing locations of large methane releases. The information provided by EMIT contributes to understanding and addressing the impact of methane on global climate change.

## How to Deal with Methane Gas

Reducing methane emissions is crucial for limiting global warming. Here are some steps that can be taken:

- **Upgrade Infrastructure:** Prevent and contain or seal methane leaks from sources that use fossil fuels, oil, or gas.
- **Transition to Renewable Energy:** Increase the use of renewable energy sources to reduce reliance on fossil fuels.
- **Manage Organic Waste:** Reduce the amount of organic waste in landfills, as it contributes to methane emissions.
- **Improve Wastewater Treatment:** Implement better wastewater treatment systems to minimize methane release.
- **International Cooperation:** Establish procedures for managing, monitoring, and controlling methane release into the atmosphere.

## Explore EMIT Data

Visit the [EMIT Data Portal](https://earth.jpl.nasa.gov/emit/data/data-portal/coverage-and-forecasts/) to explore data on methane emissions and dust quantity collected by the EMIT satellite.

## Additional Resources

- [About EMIT Mission](https://earth.jpl.nasa.gov/emit/mission/about/)
- [EMIT First Data](https://earth.jpl.nasa.gov/emit/resources/101/emit-first-data/)
- [Methane Super Emitters Mapped](https://earth.jpl.nasa.gov/emit/news/23/methane-super-emitters-mapped-by-nasas-new-earth-space-mission/)

## Methane Emissions Map

Check out the interactive [Methane Emissions Map](#) to see the locations detected by EMIT.

## Dust Quantity Information

Explore the [Dust Quantity](DustQuantity.html) section to learn more about the mineral dust quantity collected by EMIT.

## Methane Gas Details

Learn about Methane Gas and its impact by visiting the [Methane Gas](MethaneGas.html) section.

## Explore EMIT Data

Visit the [EMIT Data Portal](https://earth.jpl.nasa.gov/emit/data/data-portal/coverage-and-forecasts/) to explore data on methane emissions and dust quantity collected by the EMIT satellite.

## EMIT Website

Visit the [EMIT Website](#) for a detailed interactive experience, including the latest information on the mission, methane gas detection, and more.

## JavaScript Code for Data Fetching

The following JavaScript code is responsible for fetching GeoJSON data from the server and displaying it on the interactive map:

```javascript
// Create a Leaflet map centered at a specific latitude and longitude
var map = L.map('map').setView([51.505, -0.09], 13);

// Add a base layer (e.g., OpenStreetMap)
L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
    attribution: '&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors'
}).addTo(map);

// Load GeoJSON data ("Methane Metadata.json") and add it to the map
fetch('Methane_Metadata.json')
    .then(function (response) {
        return response.json();
    })
    .then(function (data) {
        L.geoJSON(data).addTo(map);
    })
    .catch(function (error) {
        console.error('Error loading GeoJSON:', error);
});
```

## License

This project is licensed under the [Nasean License](LICENSE).

---

&copy; 2023 Nasean. All Rights Reserved.
