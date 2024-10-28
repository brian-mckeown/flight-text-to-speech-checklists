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

Enjoy using FlightDash!
