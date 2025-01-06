# WeatherPy and VacationPy Analysis

## Overview of the Analysis

The goal of this project was to analyze weather data for over 500 cities around the world and visualize the relationships between weather variables and geographic latitude. Additionally, I used this data to identify ideal vacation locations and find nearby hotels for those locations. The analysis was split into two parts:

- **WeatherPy**: Focused on visualizing weather trends using scatter plots and linear regression.
- **VacationPy**: Used weather data to narrow down cities based on ideal weather conditions and locate hotels using the Geoapify API.

---

## WeatherPy Analysis

### Data and Methodology:
- **Weather Data Source**: OpenWeatherMap API
- **Number of Cities Analyzed**: Over 500 cities, selected randomly based on geographic coordinates.
- **Weather Variables Examined**:
  - Maximum Temperature
  - Humidity
  - Cloudiness
  - Wind Speed
- **Geographic Focus**: Data was separated into Northern Hemisphere (Latitude >= 0) and Southern Hemisphere (Latitude < 0).

### Process:
1. **Data Collection**:
   - Used the `citipy` library to find cities near randomly generated geographic coordinates.
   - Retrieved weather data for each city using the OpenWeatherMap API.
2. **Scatter Plots**:
   - Plotted relationships between latitude and weather variables (e.g., Temperature vs. Latitude).
3. **Linear Regression**:
   - Conducted linear regression for each weather variable against latitude, separately for the Northern and Southern Hemispheres.
4. **Discussion of Trends**:
   - Interpreted relationships (or lack thereof) between latitude and each weather variable.

### Key Findings:
1. **Temperature vs. Latitude**:
   - **Northern Hemisphere**: Strong negative correlation; temperatures decrease as latitude increases.
   - **Southern Hemisphere**: Positive correlation; temperatures increase closer to the equator.
2. **Humidity vs. Latitude**:
   - No significant correlation in either hemisphere.
3. **Cloudiness vs. Latitude**:
   - No strong patterns observed in either hemisphere.
4. **Wind Speed vs. Latitude**:
   - Wind speeds showed no clear relationship with latitude in either hemisphere.

---

## VacationPy Analysis

### Data and Methodology:
- **Objective**: Identify vacation destinations with ideal weather conditions and locate nearby hotels.
- **Ideal Weather Criteria**:
  - Temperature between 21°C and 27°C
  - Wind Speed less than 4.5 m/s
  - Clear skies (0% cloudiness)
- **Hotel Search**: Used the Geoapify API to find hotels within 10,000 meters of selected city coordinates.

### Process:
1. **Filter Cities**:
   - Narrowed down cities that matched the ideal weather conditions.
2. **Locate Hotels**:
   - Used the Geoapify API to search for hotels near these cities.
3. **Visualization**:
   - Created an interactive map displaying the ideal cities and their nearby hotels.

### Key Findings:
- Several cities met the ideal weather criteria, and hotels were successfully identified for most locations.
- Interactive maps provided an easy way to visualize potential vacation spots.

---

## Summary

This analysis combined weather data with geographic data to:
1. Identify global weather trends based on latitude.
2. Select ideal vacation locations based on specific weather criteria.
3. Locate nearby hotels for selected cities.

The findings show clear trends between temperature and latitude, while other weather variables, such as humidity and wind speed, displayed no strong correlations. This project demonstrates the power of combining APIs and geographic data for real-world applications like travel planning.
