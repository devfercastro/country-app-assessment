# Country Info App - Assessment
This repository contains the code for a full-stack JavaScript engineer assessment. The project is split into two sections: a Backend using Node.js and a Frontend using Next.js. The goal is to create a country information app that provides data such as country details, borders, population trends, and more.

## Table of Contents
1. [Running the Project](#running-the-project)
2. [Assessment Details](#full-stack-js-engineer-test-assessment---the-country-info-app)
3. [Additional Notes](#additional-notes)

## Running the project
### Prerequisites
- Ensure that `pnpm` or `node` is installed globally on your machine.

### Instructions to Run

First, copy the `.env` file into both the `backend/` and `frontend/` directories.

### Backend
```bash
cd backend
pnpm install
pnpm start
```
### Frontend
```bash
cd frontend
pnpm install
pnpm build
pnpm start
```

# Full-Stack JS engineer test assessment - the Country Info App.
This documentation provides detailed instructions for completing the test assessment, which involves building two small applications to provide information about countries. The application includes a Backend (BE) built with Node.js (Nest or Express) and a Frontend (FE) built with React (Next.js is a plus).

## Project Overview
### Backend:
#### Tech Stack:
- Node.js (Nest.js or Express.js)
#### Tasks:
1. Endpoint: Get Available Countries
    - Create an API endpoint, using Date Nager API `https://date.nager.at/api/v3/AvailableCountries`
    - This endpoint should return a list of available countries
2. Endpoint: Get Country Info
    - Create an API endpoint to retrieve detailed information about a specific country
    - This endpoint should provide the following data:
    a. *List of Border Countries*: A list of countries that share a border with the selected country `https://date.nager.at/api/v3/CountryInfo/UA`
    b. *Population Data*: Historical population data for the country, suitable for plotting on a chart `https://countriesnow.space/api/v0.1/countries/population`
    c. *Flag URL*: A URL to the country’s flag image `https://countriesnow.space/api/v0.1/countries/flag/images`
### Frontend:
#### Tech Stack:
- React.js
- Next.js (preferred but not mandatory)
Tasks:
1. Country List Page
    - Display a list of countries fetched from the endpoint.
    - Each country name should be clickable and navigate the user to the Country Info Page.
2. Country Info Page
    - Display detailed information about the selected country, including:
        - Country Name: Displayed prominently at the top.
        - Country Flag: Displayed alongside the country name using the URL fetched from the backend.
    - Border Countries Widget:
        - Show a list of countries that border the selected country.
        - Each border country name should be clickable and navigate the user to the corresponding Country Info Page.
    - Population Chart:
        - Implement a chart that shows the country’s population over time.
        - The X-axis should represent years, and the Y-axis should represent the population.
### Additional Requirements
1. Styling:
    - You can use any CSS framework or custom styles to desing the components
    - Ensure that the UI is responsive and user-friendly.
2. Environment Variables:
    - Create a `.env` file to store sensitive data such as API keys and base URLs
    - Ensure that environment variables are loaded and used securely in the application
    - Add `.env` to the repository
3. Code Quality:
    - Set up ESLint and Prettier to ensure consistent code formatting and Quality
    - Ensure that all files are properly linted and formatted before submission
4. Documentation:
    - Include a `README.md` file that provides  instructions on how to install, run, and test the application.
    - Include any necessary setup steps, such as installing dependencies or configuring environment variables.
### API Documentation
- Country List API: [Nager.Date API Documentation](https://date.nager.at/swagger/index.html)
- Country Info API: [Postman Country Info API Documentation](https://documenter.getpostman.com/view/1134062/T1LJjU52)
### Additional Instructions
We will be testing your application locally. Please ensure the following:
- Separate Folders: Place the frontend (FE) and backend (BE) code in separate folders within the root directory. Do not create a monorepo structure.
- Parallel Execution: Ensure that both the frontend and backend can be run simultaneously on different ports. The frontend should be able to communicate with the backend without any issues.
- Instructions for Running: Provide clear instructions in the `README.md` file on how to start both the frontend and backend servers, including any necessary environment variables or configurations.
By following these instructions, we will be able to test your application smoothly and verify that both parts work together as expected.

## Additional Notes

- **Project Context**: The assessment was completed as part of a coding challenge but has not yet been reviewed or delivered to recruiters. All requirements were implemented based on the guidelines provided in the [assessment brief](https://develops.notion.site/Full-Stack-JS-engineer-test-assessment-the-Country-Info-App-5239484850be45d79702fd06773fc65a).

- **Tech Stack Choices**: Next.js was chosen for the frontend due to its server-side rendering capabilities, which enhance performance, particularly when fetching country data. Express.js was used for the backend to maintain simplicity and flexibility when integrating with third-party APIs.

- **API Integration**: The project heavily relies on third-party APIs for country data (Nager.Date and CountriesNow). Any changes or downtime in these APIs could affect the app’s functionality.

- **Styling**: Custom styles were applied using **tailwindcss** to ensure the UI is responsive. The application has been tested on mobile and desktop views.
