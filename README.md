# FlightDash.io Web App (For Local Use)

Welcome to the FlightDash Web App! Since FlightDash.io is no longer hosted on the web, this guide will walk you through setting up and running the app locally on your machine. Follow each section carefully to install prerequisites, configure the environment, and start the application.

---

## Prerequisites

Before starting, make sure you have the following tools installed on your system:

### 1. Install Java (Java 17 or later)

1. **Check if Java is already installed**:
   - **Windows PowerShell**:
     ```powershell
     java -version
     ```
   - **Mac Terminal**:
     ```bash
     java -version
     ```
   If Java is not installed or the version is older than 17, proceed to download and install Java.

2. **Download Java 17 or later**:
   - [Oracle JDK](https://www.oracle.com/java/technologies/javase-jdk17-downloads.html)
   - [OpenJDK](https://openjdk.java.net/)

3. **Verify Installation**:
   - **Windows PowerShell**:
     ```powershell
     java -version
     ```
   - **Mac Terminal**:
     ```bash
     java -version
     ```
   The command should display Java 17 or later.

### 2. Install Maven

1. **Check if Maven is already installed**:
   - **Windows PowerShell**:
     ```powershell
     mvn -version
     ```
   - **Mac Terminal**:
     ```bash
     mvn -version
     ```
   If Maven is not installed, follow the installation instructions for your OS.

2. **Download Maven**: [Apache Maven](https://maven.apache.org/download.cgi)

3. **Verify Installation**:
   - **Windows PowerShell**:
     ```powershell
     mvn -version
     ```
   - **Mac Terminal**:
     ```bash
     mvn -version
     ```

### 3. Install Git (for cloning the repository)

If Git is not installed, download it from [Git's official site](https://git-scm.com/), and follow the installation instructions for your operating system.

---
## Installation

Follow the below steps to install the repository. 

### Step 1: Clone the Repository

First, locate a folder/directory on your machine where you want to clone the project and ```cd``` to that location using Windows Powershell or Mac Terminal.

1. **Open a Terminal**:
   - **Windows**: Open PowerShell.
   - **Mac**: Open Terminal.

2. **Clone the Repository from GitHub**:
   - **PowerShell** and **Terminal**:
     ```bash
     git clone https://github.com/brian-mckeown/flightdash.git
     ```
   This command will create a folder named `flightdash` containing the project files.

3. **Navigate to the Project Directory**:
   - **Windows PowerShell**:
     ```powershell
     cd .\flightdash\
     ```
   - **Mac Terminal**:
     ```bash
     cd flightdash
     ```

---

## Step 2: Set Up Environment Variables

This application requires two API tokens for the Airport and Weather data services.

1. **Get API Tokens**:
   - [AirportDB API Token](https://airportdb.io/)
   - [WeatherAPI Token](https://api.weatherapi.com/)

2. **Create a `.env` file in the project directory**:
   - **Windows PowerShell**:
     ```powershell
     New-Item -Path . -Name ".env" -ItemType "file"
     ```
   - **Mac Terminal**:
     ```bash
     touch .env
     ```

3. **Edit the `.env` file**:
   Open the `.env` file in a text editor of your choice and add the following lines. Replace `<your_token_here>` with your actual API tokens:

   ```plaintext
   AIRPORTDB_API_TOKEN=<your_airportdb_token_here>
   WEATHER_API_TOKEN=<your_weatherapi_token_here>

   ## Step 3: Build and Run the Application

1. **Build the Application**:
   - **PowerShell** and **Terminal**:
     ```bash
     mvn clean install
     ```
   This command compiles the application and installs necessary dependencies.

2. **Run the Application**:
   Start the Spring Boot app on port 8080:
   - **PowerShell** and **Terminal**:
     ```bash
     mvn spring-boot:run
     ```

3. **Access the Application**:
   Once the application is running, open your web browser and go to [http://localhost:8080](http://localhost:8080) to view it.

---

## Troubleshooting

### Common Issues

- **Java or Maven Commands Not Recognized**:
  Ensure Java and Maven are installed correctly and added to your system PATH.

- **Environment Variables Not Set**:
  Double-check the `.env` file to ensure that the API tokens are correctly set.

---

## License

This project is licensed under the Creative Commonons License. See the [LICENSE](./LICENSE) file for more information.

---

# User Guide

This User Guide provides step-by-step instructions and helpful information on using FlightDash.io. Find detailed guidance for setup, features, and functionalities organized into categories.

---

## Getting Started

### Initial Configuration

1. Navigate to [http://localhost:8080](http://localhost:8080)

2. Open the **FlightDash App**.

3. Agree to the **Terms of Use** and **Privacy Policy**.

4. Click **Settings** in the top-right corner.

5. Choose a **METAR Source**.

6. Enter your **Simbrief Pilot ID** (optional).

   **Important**: Many of FlightDash.io's automations are built around Simbrief. While it's not required to use all features of FlightDash.io, it is highly recommended for the best experience.

   - **Where to find my Simbrief Pilot ID?**  
     Navigate back to the main User Guide and refer to our guide on finding your Simbrief Pilot ID.

7. Choose a **default checklist** (optional).

   - **Checklists**: For more details on checklists, see our guides in the Checklists section of the main User Guide.

8. Click **Save and Close**.


### Using FlightDash.io with MSFS2020 on Xbox

# Introduction

FlightDash.io is a web application that must be run in a web browser. To ensure the best experience, we recommend using FlightDash.io on a separate device, like a laptop or tablet, when flying in MSFS2020 on Xbox. Note that **not all features are compatible with Xbox**; refer to the compatibility matrix below to see what features work on each platform.

**Note**: FlightDash.io will not function directly in-game with MSFS2020. It is intended as an external tool to assist with your flight simulations.

## Compatibility Matrix

| Feature                                | Xbox                  | PC                          |
|----------------------------------------|-----------------------|-----------------------------|
| Vat Track Map                          | ❌                    | ✅                           |
| Checklists                             | ✅🔈                 | ✅                           |
| Airport General Data                   | ✅                    | ✅                           |
| Airport Weather Information            | ✅                    | ✅                           |
| Airport Frequency Information          | ✅                    | ✅                           |
| Runway Information with Suggested Runways (live wind data) | ✅ | ✅ |
| Airport Vatsim Controllers, Inbound & Outbound Flights | ❌ | ✅ |
| Simbrief Flight Plan Import            | ✅ (w/ Simbrief)      | ✅ (w/ Simbrief)             |
| Custom Cabin Crew Configuration        | ✅                    | ✅                           |
| AviationAPI.com Charts                 | ✅                    | ✅                           |
| Manual Flight Status Tracking          | ✅                    | ✅                           |
| Live Passenger Manifest                | ✅                    | ✅                           |
| Flight Stats Banner                    | ✅                    | ✅                           |
| Vatsim Flight Stats Banner             | ❌                    | ✅ (w/ Vatsim)               |
| Vatsim Group Flight Tracking           | ❌                    | ✅ (w/ Vatsim)               |
| Vatsim Flight Proximity Tracking       | ❌                    | ✅ (w/ Vatsim)               |
| AI Cabin Crew Announcements Web Player | ✅🔈                 | ✅ (w/ OpenAI API Key)       |
| AI Cabin Crew Announcements Fenix Soundpack Generator | ❌ | ✅ (w/ OpenAI API Key) |
| Announcement Autopilot (Vatsim only)   | ❌                    | ✅ (w/ Vatsim)               |
| Post Flight Report                     | ✅                    | ✅                           |

**🔊 Xbox Features that Require Audio**  
The following features require audio output on Xbox:

- Checklists (Voice Recognition and Readout)
- AI Cabin Crew Announcements (Web Player)

## Options for Audio Output on Xbox

To use the above audio-reliant features with Xbox, consider one of the following options:

### 1. Use the Audio Output from the External Device

Simply play the audio directly from your external device (laptop or tablet) through built-in speakers, connected headphones, or external speakers.

### 2. Audio Receiver

Use an audio receiver that can output audio from multiple sources simultaneously.

- Open **FlightDash.io** on a computer, laptop, or tablet.
- Connect the device to the audio system receiver via wire or Bluetooth.
- Connect the Xbox HDMI cable to the receiver.
- If the audio receiver allows playing both sources at once, you should be ready to go.

### 3. Capture Card (e.g., Elgato Capture Card)

1. Connect the Xbox to the capture card.
2. Connect the capture card outputs to both a laptop and your TV/monitor.
3. Use software like OBS to route the audio from both the capture card and your computer’s browser (FlightDash.io) to your audio system, speakers, or headphones.

For more detailed guidance, refer to other sections of the User Guide available at [http://localhost:8080](http://localhost:8080).


---

## Streaming with OBS Studio

The following video provides a walkthrough on how to display FlightDash.io during streaming using OBS Studio:

[![FlightDash.io OBS Studio Setup](https://img.youtube.com/vi/nE9nQ00y214/0.jpg)](https://youtu.be/nE9nQ00y214?si=nFMcCgNAI5HA6Ihs)

Click on the thumbnail above to watch the video on YouTube.

---

## AI Announcements

### AI Cabin Crew Announcements Fenix Soundpack Generator

Learn how to generate a custom cabin crew announcement soundpack for the Fenix A320 (version 2 block 2), tailored to your flight plan. Watch the video below for a step-by-step guide:

[![Custom Cabin Crew Soundpack for Fenix A320](https://img.youtube.com/vi/KESKoellxRo/0.jpg)](https://youtu.be/KESKoellxRo?si=i5idnnReVBk1Hlui)

Click on the thumbnail above to watch the video on YouTube.

### AI Cabin Crew Announcements Web Player

Learn how to use the AI Cabin Crew Announcements feature through the Web Player by watching the video below:

[![AI Cabin Crew Announcements Web Player](https://img.youtube.com/vi/UI70MJKVB9c/0.jpg)](https://youtu.be/UI70MJKVB9c?si=4UTJsYE8luitjIxE)

Click on the thumbnail above to watch the video on YouTube.

### How to configure an OpenAI Payment Method and Set Limits

## How to Configure an OpenAI Payment Method and Set Limits

1. Navigate to [https://auth0.openai.com/u/login/](https://auth0.openai.com/u/login/)

2. Log in to your account.

3. In the left navigation bar, click **Settings**.

4. Select **Billing**.

5. Click the **Payment Methods** tab.

6. Click **Add payment method**.

7. Complete your billing details and click **Add payment method**.

8. Next, in the left navigation bar, select **Limits** under **Settings**.

9. In the text input for **Set a monthly budget**, enter the amount you want to allow to be charged per month.

   **Note**: FlightDash.io will not notify you if you exceed this limit. If your monthly budget/limit is exceeded, you may notice that announcements stop working as expected in FlightDash.io.

10. Click **Save** to confirm your settings.


### How to Create an API Key for OpenAI Integration

1. Navigate to [OpenAI](https://platform.openai.com/).

2. Click **Menu**.

3. Click **Log in**.

4. Create an account or log in with your existing credentials.

5. Select **API** from the main dashboard.

6. In the left navigation bar, click **API Keys**.

7. Click **Create a new secret key**.

8. Enter a name for your key.

9. Click **Create secret key**.

10. Copy the API Key.

    **Important**: Make sure to copy the API Key to a safe place. Once you click **Done**, you will not be able to view the key again.

11. Click **Done** to finish.


---

## EFB App (Electronic Flight Bag)

### Importing SimBrief Flight Plan

1. Navigate to [http://localhost:8080/app](http://localhost:8080/app).

2. Click the **Flight Plan** icon in the left navigation bar (icon resembles a piece of paper with lines of writing).

3. Click the **Load Flight Plan** button.

   **Note**: Ensure your Simbrief ID is entered in **Settings**, and you have a flight plan generated in Simbrief.

4. Once loaded, your **OFP** (Operational Flight Plan) will be displayed below the buttons.

5. In the **Flight Data** section (click the pencil & paper icon in the left navigation bar), you’ll see that most of the Flight Data fields have been prefilled for you.

   **Note**: To use the **AI Cabin Crew Announcements**, be sure to enter your airline name and click the **Generate Flight Crew** button. These fields are not automatically completed when importing from Simbrief.


### How to Manually Enter Flight Data

1. Navigate to [http://localhost:8080/app](http://localhost:8080/app).

2. Click the **Flight Data Edit** icon (pencil and paper icon) in the left navigation bar.

3. Complete all of the fields as follows:
   - **Aircraft**
   - **Call Sign**
   - **Departure ICAO**
   - **Arrival ICAO**
   - **Scheduled Boarding** (local time of the user)
   - **Scheduled Departure** (local time of the user)
   - **Estimated Departure** (local time of the user)
   - **Estimated Arrival** (local time of the user)
   - **Passengers** (count)
   - **Airline**

4. Click **Generate Flight Crew**.

5. Edit your flight crew details as desired.

   **Note**: All fields must be completed, including clicking the **Generate Flight Crew** button, for the **AI Cabin Crew Announcements**, **Passenger/Baggage Manifest**, and **Live Flight Status** features to function correctly.


### How to Access Charts

Watch the following video to learn how to access free charts, powered by AviationAPI.com:

[![Accessing Free Charts with AviationAPI.com](https://img.youtube.com/vi/XoFhBEtlTsI/0.jpg)](https://youtu.be/XoFhBEtlTsI?si=jMAANT1-vWvC_bpY)

**Note**: Only charts available from AviationAPI.com will work. Most charts in the US have been confirmed to work, but charts from other countries may not be available.


### How to use Flight Plans

View the following video to learn more about how to use flight plans:

[![Using Flight Plans](https://img.youtube.com/vi/2BB_hPundjY/0.jpg)](https://youtu.be/2BB_hPundjY?si=E2Iv2v2zt2uvVxnK)


### Viewing VATSIM Data in the Airport Details

View live ATC Controllers, ATIS, Departures, and Arrivals on the VATSIM network for specific airports. Learn more in the following video:

[![Viewing VATSIM Data in Airport Details](https://img.youtube.com/vi/Dv1KE7Y-l2g/0.jpg)](https://youtu.be/Dv1KE7Y-l2g?si=pNL9fssrsq1_al-V)


### How to Request Weather Information

Watch the following video to learn how to request live weather information:

[![Requesting Live Weather Information](https://img.youtube.com/vi/cpNZAvV4w9M/0.jpg)](https://youtu.be/cpNZAvV4w9M?si=oB9d-OLRnX8-2pVE)


### How to Look Up an ICAO Code

1. Navigate to [http://localhost:8080/app](http://localhost:8080/app).

2. In the left navigation bar, click the **Airport** icon (the icon resembles an airplane landing).

3. Click the link for **ourairports.com**.

4. In the **Look up an airport** field, enter the city or location name, then click **Search**.

5. Click on the appropriate airport from the search results.

6. In the **Facility Data** section on the right side of the page, look for the **GPS Code**. This field contains your ICAO Code.

7. Copy the ICAO Code from the **GPS Code** field.

8. Navigate back to the FlightDash.io web app (click the Airport icon if you are not already there).

9. Paste your ICAO Code into the text field and click **Request**.

### How to retrieve Airport and Runway Info

Watch the following video to learn how to look up current airport data, frequencies, and runway information:

[![Retrieving Airport and Runway Information](https://img.youtube.com/vi/uUI9kjP0n9M/0.jpg)](https://youtu.be/uUI9kjP0n9M?si=NQ2lMcIt_72s_Vs0)


### Using Checklists

To learn about configuring and using checklists, please watch the following video:

[![Using Checklists](https://img.youtube.com/vi/JNDOho6CG_E/0.jpg)](https://youtu.be/JNDOho6CG_E?si=7pYfkZpBRJwKGeIT)


### How to Save a Config File

Please review the following video to learn how to save a config file:

[![Saving a Config File](https://img.youtube.com/vi/7af8Dl1p70Y/0.jpg)](https://youtu.be/7af8Dl1p70Y?si=ON3xRr7d8Pt5miU1)


### How to Access Simbrief Pilot ID

1. Navigate to [SimBrief.com - Virtual Flight Planning Solutions](https://www.simbrief.com/) and log in.

2. Click **Dispatch**.

3. In the left navigation bar, click **Account Settings**.

4. Copy your **Pilot ID**.

### Passenger & Baggage Manifest

Learn how to use the Passenger & Baggage Manifest feature by watching the video below:

[![Passenger & Baggage Manifest](https://img.youtube.com/vi/iZFOjmfmwpk/0.jpg)](https://youtu.be/iZFOjmfmwpk?si=zFqlLAWodYzQtjsM)

### Live Flight Status Tracking

Watch the following video to learn how to use the Flight Status Tracking feature:

[![Live Flight Status Tracking](https://img.youtube.com/vi/txuKL20e9Ak/0.jpg)](https://youtu.be/txuKL20e9Ak?si=Dnm_RtIT__JZJyoi)

### Post Flight Reports

Learn how to use the Post Flight Reports feature in the video below:

[![Post Flight Reports](https://img.youtube.com/vi/zQcNaCmx2Bg/0.jpg)](https://youtu.be/zQcNaCmx2Bg?si=msE90p-jyxNzrL5g)


---

This User Guide is designed to help you make the most of FlightDash.io. Follow each section to find the specific details and instructions for using each feature.
