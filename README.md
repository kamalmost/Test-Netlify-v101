# Weather App

## Description
A simple web application that allows users to search for and display the current weather conditions for a specified city.

## Features
- Search for weather by city name.
- Display current temperature, weather condition, and wind speed.
- Show error messages for invalid city names or API issues.

## How to Use
1. Clone the repository.
2. Open `index.html` in a web browser.
3. Enter a city name in the input field and click "Search".

## Technologies Used
- HTML
- CSS
- JavaScript
- Open-Meteo Geocoding API (for city to coordinates)
- Open-Meteo Weather Forecast API (for weather data)

## API Credits
This project uses the free Open-Meteo API for weather data.

## Step-by-Step Guide to Replicate This Project

### 1. Setting up your Project on GitHub

This part will guide you through creating a place for your project on GitHub (a popular website for storing and sharing code). Think of Git as a tool to track changes in your code, and GitHub as a website to store your code projects and collaborate.

#### A. Initial Git Configuration (One-Time Setup)
Before you start using Git, it's a good idea to tell Git who you are. This information will be used in your commits. You only need to do this once on your computer.
Open your terminal or command prompt and type:

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```
Replace "Your Name" and "your.email@example.com" with your actual name and email address (ideally the one you use for GitHub).

*   **B. Create a GitHub Account:** If you don't have one, go to [https://github.com](https://github.com) and sign up. It's free!
*   **C. Create a New Repository on GitHub:**
    *   Once logged in, click the "+" icon in the top right corner and select "New repository".
    *   Give your repository a name (e.g., `my-weather-app`).
    *   You can add a short description (optional).
    *   Choose "Public" so others can see it (or "Private" if you prefer).
    *   You can skip adding a README, .gitignore, or license for now, as we'll create them manually or they are not strictly needed for this basic project.
    *   Click "Create repository".
*   **D. Option 1: Clone the Repository from GitHub (Easiest for existing projects):**
    *   On your new repository's page on GitHub, click the green "Code" button.
    *   Copy the HTTPS URL (it looks like `https://github.com/YOUR_USERNAME/YOUR_REPOSITORY_NAME.git`).
    *   Open a terminal or command prompt on your computer. If you're new to this, search for "Command Prompt" on Windows or "Terminal" on macOS/Linux.
    *   Navigate to where you want to store your project using the `cd` command (e.g., `cd Documents/Projects`).
    *   Type `git clone COPIED_URL_HERE` and press Enter. Replace `COPIED_URL_HERE` with the URL you copied. This downloads a copy of your GitHub repository to your computer. Cloning means creating a copy of the project from GitHub onto your own computer so you can work on it locally.
    *   You should now have a folder with your repository's name. Navigate into it: `cd YOUR_REPOSITORY_NAME`.

#### E. Option 2: Start a New Project Locally and then Push to GitHub

Sometimes, you might start working on a project on your computer *before* creating a repository on GitHub. Here's how to handle that:

1.  **Navigate to your project folder:** Open your terminal/command prompt and use the `cd` command to go into your project's main folder (e.g., `cd Documents/MyNewWeatherApp`).
2.  **Initialize a Git repository:** If you haven't already, turn this folder into a Git repository by typing:
    ```bash
    git init
    ```
    This creates a hidden `.git` folder inside your project directory, which Git uses to track changes.
3.  **Add your project files:** Create your `index.html`, `style.css`, and `script.js` files in this folder and add your code to them (as described in "### 2. Adding Your Project Files" below).
4.  **Add and Commit your files:**
    ```bash
    git add index.html style.css script.js 
    # Or use git add . to add all files in the current directory
    git commit -m "Initial project setup"
    ```
5.  **Create a New Repository on GitHub:** Go to GitHub (as described in "C. Create a New Repository on GitHub" above) and create an empty repository. **Do not** initialize it with a README, license, or .gitignore file, as you already have your project files locally.
6.  **Link your local repository to the GitHub repository:**
    On your GitHub repository page, find the "…or push an existing repository from the command line" section. You'll see commands similar to these. Copy the `git remote add origin` line (it will have your specific repository URL):
    ```bash
    git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPOSITORY_NAME.git
    ```
    Paste this into your terminal and press Enter. This tells your local Git repository where the "origin" (your GitHub repo) is.
7.  **Verify the remote (optional):**
    ```bash
    git remote -v
    ```
    This should show you the `origin` URL for fetch and push.
8.  **Push your local commits to GitHub:**
    If your main branch on GitHub is named `main` (common for new repositories):
    ```bash
    git push -u origin main
    ```
    If your main branch on GitHub is named `master` (older default):
    ```bash
    git push -u origin master
    ```
    The `-u` flag sets up the upstream tracking relationship, so in the future, you can just type `git push`.

### 2. Adding Your Project Files

Now, let's add the HTML, CSS, and JavaScript files that make the weather app work.

*   **Create the Files:** Inside your project folder (e.g., `my-weather-app`), create the following three files. You can do this with a code editor. We recommend Visual Studio Code (VS Code) which is free and very popular; you can download it from [https://code.visualstudio.com/](https://code.visualstudio.com/). However, other editors like Sublime Text or even basic text editors like Notepad (Windows) or TextEdit (Mac) will work.
    *   `index.html`
    *   `style.css`
    *   `script.js`
*   **Copy the Code:**
    *   Copy the HTML code from the original project's `index.html` and paste it into your `index.html` file.
    *   Copy the CSS code from the original project's `style.css` and paste it into your `style.css` file.
    *   Copy the JavaScript code from the original project's `script.js` and paste it into your `script.js` file.
    *   (You can find the original code in the initial sections of this README or by browsing the original repository if you cloned it directly).

### 3. Committing and Pushing Your Code to GitHub

This means saving your changes and sending them up to your GitHub repository.

*   **Check Status (Optional but good practice):** In your terminal (make sure you're in your project folder), type `git status`. This shows you which files are new or changed.
*   **Add Files to Staging:** Type `git add index.html style.css script.js` and press Enter. This prepares your files to be saved. You can also use `git add .` to add all new/changed files in the current directory (the `.` stands for the current directory).
*   **Commit Your Changes (Saving a snapshot):** Type `git commit -m "Add initial project files for weather app"` and press Enter. The message in quotes should be a brief description of what you did.
*   **Push Your Code to GitHub (Uploading):** Type `git push origin main` (or `git push origin master` if your main branch is called master) and press Enter. GitHub now uses `main` as the default name for the primary branch in new repositories, but many older projects use `master`. This uploads your committed files to your GitHub repository. You might be asked for your GitHub username and password.

### 4. Deploying Your Weather App with Netlify

Netlify is a service that makes it easy to publish websites from your GitHub repositories.

*   **Create a Netlify Account:**
    *   Go to [https://www.netlify.com](https://www.netlify.com) and sign up. You can usually sign up using your GitHub account, which makes things easier.
*   **Deploy Your Site:**
    *   Once logged in to Netlify, you should see a button like "Add new site" or "Import an existing project". Click it.
    *   Choose "Import an existing project" and then select "Deploy with GitHub" (or your Git provider if different, but we used GitHub).
    *   Authorize Netlify to access your GitHub account if prompted.
    *   Netlify will show you a list of your GitHub repositories. Select the repository you created for your weather app (e.g., `my-weather-app`).
    *   **Deployment Settings:**
        *   **Branch to deploy:** Ensure it's set to `main` (or `master`, whichever you pushed to).
        *   **Build command:** You can leave this blank for this project, as it's just static HTML, CSS, and JS.
        *   **Publish directory:** This should be the root of your project where `index.html` is located. For this specific project, since `index.html` is in the root folder, leaving this blank or using the default setting provided by Netlify will work correctly.
    *   Click "Deploy site".
*   **Your Site is Live!**
    *   Netlify will build and deploy your site. It usually takes less than a minute.
    *   Once done, Netlify will provide you with a unique URL (like `random-name-12345.netlify.app`). You can click this link to see your live weather app!
    *   You can customize the site name in Netlify's settings if you want a more memorable URL.

### 5. Automatic Redeployments

One of the great things about Netlify is that whenever you push updates to your GitHub repository (e.g., `git push origin main`), Netlify will automatically detect the changes and redeploy your site with the latest version!

---
That's it! You've successfully replicated and deployed the weather app. Happy coding!
