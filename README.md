![FoodScan AI App Banner](./path-to-image/banner.png)

FoodScan AI App
# Food Ingredient Safety Scanner

**AI-powered ingredient safety analysis at your fingertips. Make informed dietary decisions with trusted scientific insights.**

---

## Table of Contents

-   [About the App](#about-the-app)
-   [Key Features](#key-features)
-   [Technology Stack](#technology-stack)
-   [Getting Started](#getting-started)
    -   [Prerequisites](#prerequisites)
    -   [Installation](#installation)
    -   [Running the App](#running-the-app)
-   [Project Structure](#project-structure)
-   [Detailed Documentation](#detailed-documentation)
-   [Contributing](#contributing)
-   [License](#license)

---

## About the App

The Food Ingredient Safety Scanner is an AI-powered mobile application designed to empower users to make informed dietary decisions. By simply scanning food ingredient labels, users receive instant safety ratings and detailed information about each ingredient.

**Product Vision:** To create the most trusted and accessible food safety companion that helps users navigate complex ingredient lists with confidence, supporting both human and pet dietary needs.

**Core Value Proposition:** "Scan any food label and instantly know which ingredients are safe, concerning, or should be avoided based on your personal dietary needs and trusted scientific sources."

---

## Key Features

*   **Core Scanning Functionality**:
    *   Photo Capture & Upload of ingredient labels.
    *   OCR Processing to extract text from images.
    *   AI Analysis to identify, categorize, and rate ingredients.
    *   Safety Rating (Safe, Caution, Avoid) with source attribution.
*   **Personalized Dietary Profiles**:
    *   Preset dietary plans (e.g., Gluten-free, Vegan, Diabetic-friendly).
    *   Custom ingredient avoidance based on user-defined preferences.
    *   Dynamic rating adjustment based on selected profiles.
*   **Smart Recommendations**:
    *   Suggestions for alternative, healthier products.
    *   Recipe suggestions using safer ingredients.
*   **Educational Content**:
    *   Detailed explanations about each ingredient and its health impact.
    *   Links to trusted sources like FDA, EWG, and Open Food Facts.

---

## Technology Stack

This application is built using a modern and robust technology stack to ensure cross-platform compatibility, scalability, and powerful AI capabilities.

*   **Frontend**:
    *   **React Native / Expo**: For cross-platform mobile development (iOS, Android, Web).
    *   **Expo Router**: For navigation.
    *   **NativeWind**: For Tailwind CSS integration in React Native.
*   **Backend**:
    *   **Supabase**: Provides PostgreSQL database, authentication, and Edge Functions.
    *   **Supabase Edge Functions (Deno)**:
        *   **Google ML Kit / Tesseract (via Google Vision API)**: For OCR processing.
        *   **OpenAI GPT (gpt-4o-mini)**: For advanced AI ingredient analysis and safety rating.
*   **Data Sources**:
    *   Open Food Facts API
    *   EWG Food Scores Database
    *   FDA Additive Lists
    *   USDA Food Database

---

## Getting Started

Follow these instructions to get a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

*   Node.js (v18 or higher)
*   npm or Yarn
*   Expo CLI (`npm install -g expo-cli`)
*   A Supabase project with `OPENAI_API_KEY` and `GOOGLE_GEN_LANG_API_KEY` secrets configured.

### Installation

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/your-username/food-scanner-app.git
    cd food-scanner-app
    ```
2.  **Install dependencies:**
    ```bash
    npm install
    # or
    yarn install
    ```
3.  **Configure Supabase**:
    *   Ensure your Supabase project is set up and your `OPENAI_API_KEY` and `GOOGLE_GEN_LANG_API_KEY` secrets are added to your Supabase project's environment variables.
    *   The Supabase Edge Functions (`ocr-process` and `ai-analyze-ingredients`) should be deployed automatically when you link your local Supabase project to your remote one.

### Running the App

To run the application in development mode:

```bash
npm run dev
# or
yarn dev
This will start the Expo development server. You can then open the app on your mobile device using the Expo Go app, or in a web browser.

Project Structure
The project follows a standard Expo/React Native structure with additional directories for documentation and backend functions:


.
├── app/                  # Main application code (Expo Router)
├── assets/               # Static assets like images and fonts
├── Docs/                 # Comprehensive project documentation
├── hooks/                # Custom React hooks
├── services/             # Application services (OCR, Scan, Ingredient, Profile, AI)
├── supabase/             # Supabase Edge Functions
├── .npmrc                # npm configuration
├── app.json              # Expo configuration
├── package.json          # Project dependencies and scripts
├── README.md             # This file
└── tsconfig.json         # TypeScript configuration
Detailed Documentation
For more in-depth information about the project, its design, and implementation, please refer to the following documents located in the Docs/ directory:

Product Requirements Document (PRD)
Project Plan
Backend Operations
Database Schemas
API Documentation
Enhancements & Future Improvements
Changelog
Development Memory Bank
Marketing Plan
Contributing
We welcome contributions to the Food Ingredient Safety Scanner! If you'd like to contribute, please follow these steps:

Fork the repository.
Create a new branch (git checkout -b feature/your-feature-name).
Make your changes and commit them (git commit -m 'Add new feature').
Push to the branch (git push origin feature/your-feature-name).
Open a Pull Request.
Please ensure your code adheres to the project's coding standards and includes appropriate tests.
