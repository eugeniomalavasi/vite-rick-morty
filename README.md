# Vue Rick and Morty Characters Project

This Vue.js project fetches and displays character data from the Rick and Morty API. It features components for the header, search, and card display of characters, with filtering capabilities.

## Table of Contents

1. [Overview](#overview)
2. [Installation](#installation)
3. [API Usage](#api-usage)
4. [Project Structure](#project-structure)
5. [Components](#components)
6. [Store](#store)
7. [Usage](#usage)
8. [License](#license)

## Overview

This project retrieves character data from the Rick and Morty API and displays it in a card format. Users can filter characters by status using a dropdown menu.
<img width="985" alt="Immagine 2024-07-20 082310" src="https://github.com/user-attachments/assets/174adf38-df89-4ff9-b016-26fd08c064e0">

## Installation

1. **Clone the repository**:
    ```bash
    git clone <repository-url>
    cd <repository-directory>
    ```

2. **Install dependencies**:
    ```bash
    npm install
    ```

3. **Run the development server**:
    ```bash
    npm run serve
    ```

## API Usage

The project uses the [Rick and Morty API](https://rickandmortyapi.com/api/character) to fetch character data. 

## Project Structure

- **`src/components`**: Contains all Vue components
- **`src/store.js`**: Contains the Vuex store for managing state

## Components

### AppHeader.vue
Displays the header of the application.

### CardsContainer.vue
Displays the character cards. It shows a loading message until the data is fetched.

### AppSearch.vue
Contains the search functionality with a dropdown to filter characters by their status.

### CharacterCard.vue
Displays individual character details.

### SearchTotal.vue
Shows the total number of characters matching the current filter.

## Store

The store is defined in `store.js` and manages the state of the application, including the list of characters and the selected filter status.

##Usage
Fetching and Displaying Data
The main Vue instance fetches character data from the API when created and stores it in the reactive store object.

