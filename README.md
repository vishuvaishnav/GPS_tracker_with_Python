# GPS Locator Using Python

## Overview

This project demonstrates how to obtain GPS coordinates using your IP address and display the location on a map. The map is generated using the Folium library and can be viewed in a web browser. This repository contains a Python script that automates the process of retrieving coordinates, generating a map, and displaying it in a browser.

## Prerequisites

- ![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white) Python 3.x
- ![requests](https://img.shields.io/badge/requests-3764AB?style=for-the-badge&logo=python&logoColor=white) `requests` library
- ![selenium](https://img.shields.io/badge/selenium-43B02A?style=for-the-badge&logo=selenium&logoColor=white) `selenium` library
- ![folium](https://img.shields.io/badge/folium-88B04B?style=for-the-badge&logo=python&logoColor=white) `folium` library
- ![Chrome WebDriver](https://img.shields.io/badge/Chrome_WebDriver-4285F4?style=for-the-badge&logo=google-chrome&logoColor=white) Chrome WebDriver (for Selenium)

## Installation

1. Clone the repository to your local machine:
    ```bash
    git clone https://github.com/VISHUVAISHNAV/gps-locator.git
    cd gps-locator
    ```

2. Install the required Python packages:
    ```bash
    pip install requests selenium folium
    ```

3. Download the Chrome WebDriver from [here](https://sites.google.com/a/chromium.org/chromedriver/) and ensure it is in your PATH or specify its location in the script.

## Usage

1. Ensure you have an active internet connection.
2. Run the script:
    ```bash
    python gps_locator.py
    ```
3. The script will:
    - Fetch your coordinates using your IP address.
    - Generate an HTML file with a map showing your location.
    - Open the HTML file in a Chrome browser.

## Script Details

### `locationCoordinates()`

This function fetches your current coordinates based on your IP address using the `ipinfo.io` API. It returns the latitude, longitude, city, and state.

### `gps_locator()`

This function uses the coordinates obtained from `locationCoordinates()` to create a map using the Folium library. It then saves the map as an HTML file and returns the file name.

### Main Execution

The main part of the script calls the `gps_locator()` function, opens the generated HTML file in a Chrome browser using Selenium, and keeps the browser open for 100 seconds before closing it.

## Example Output

- The script will print the following information to the console:
    ```
    ---------------GPS Using Python---------------
    You Are in [City], [State]
    Your latitude = [latitude] and longitude = [longitude]
    Opening File.............
    Browser Closed..............
    ```

- The generated HTML file will be saved in the specified folder and will display a map with a marker at your current location.

## Description

The **GPS Locator Using Python** project is designed to fetch and display the geographical location of a user based on their IP address. The project leverages multiple Python libraries, including `requests` for fetching data from an API, `folium` for creating interactive maps, and `selenium` for automating the web browser to display the map.

### Key Features

- **IP-Based Location Fetching**: Utilizes the `ipinfo.io` API to retrieve the user's geographical coordinates (latitude and longitude), city, and state based on their IP address.
- **Interactive Map Creation**: Uses the `folium` library to create an interactive map centered on the user's location, with a marker indicating the precise coordinates.
- **Automated Browser Display**: Employs the `selenium` library to automatically open the generated map in a web browser, providing a visual representation of the user's location.
- **Error Handling**: Includes error handling mechanisms to ensure the script terminates gracefully in case of connectivity issues or other errors.

### Project Workflow

1. **Fetch Location Data**: The `locationCoordinates()` function sends a request to the `ipinfo.io` API to get the user's location data. It processes the response to extract the latitude, longitude, city, and state.

2. **Generate Map**: The `gps_locator()` function uses the coordinates obtained from `locationCoordinates()` to create an interactive map with Folium. It places a marker on the map at the user's location and saves the map as an HTML file.

3. **Display Map**: The script's main execution flow calls `gps_locator()` to generate the map file, then uses Selenium to open this HTML file in a Chrome browser, allowing the user to view their location on an interactive map.

### Practical Applications

- **Geolocation Services**: This project can serve as a foundational component for services requiring geolocation data, such as delivery tracking, location-based services, or personalized content delivery.
- **Educational Tool**: It provides a practical example for learning how to use APIs, create interactive maps, and automate web browsers with Python.
- **Network and Security Tools**: Can be used in network diagnostics to verify the geographical location associated with an IP address, aiding in security and network management tasks.

### Future Enhancements

- **Multiple Browser Support**: Extend the browser automation to support multiple web browsers beyond Chrome.
- **Enhanced Error Handling**: Improve the error handling to cover more edge cases and provide detailed error messages.
- **Custom Markers and Layers**: Add features to customize map markers and include additional map layers for more detailed geographical information.
- **User Interface**: Develop a simple graphical user interface (GUI) to make the tool more user-friendly.

This project is an excellent demonstration of how to combine various Python libraries to create a useful application that provides real-world utility by displaying the user's geographical location on an interactive map.

## Author

**Vishu Vaishnav**
