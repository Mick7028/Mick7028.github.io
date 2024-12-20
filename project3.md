---
layout: default
title: Project 3
---

<!-- Dark Mode Toggle -->
<div class="theme-toggle">
  <button id="toggleTheme" onclick="toggleTheme()">🌙</button>
</div>

[Back to Portfolio](./)

Ruby on Rails Tutorial: Sample App
===============

-   **Class: CSCI 452** 
-   **Grade: A**
-   **Language(s): Ruby, HTML, CSS, JavaScript**
-   **Source Code Repository:** [ Mick7028 / Sample_App](https://github.com/Mick7028/sample_app)  
    (Please [email me](mailto:example@csustudent.net?subject=GitHub%20Access) to request access.)
-   **Website Server:** [Sample_App](https://throbbing-pond-4766.fly.dev/)

## Project description
 
 In this project, we go over chapters 1-5 in the Ruby on Rails tutorial. This tutorial introduces the use of web development using the Ruby on Rails framework with the creation of a sign-up webpage that creates an account for the user.

## How to compile / run the program

How to compile (if applicable) and run the project: N/A

## UI Design

The user interface of this program is a website.

![screenshot](images/project_3_images/Home_Page.png)
**Fig 1. Home Page**

![screenshot](images/project_3_images/Signup_Page.png)
**Fig 2. Signup Page**

![screenshot](images/project_3_images/About_Page.png)
**Fig 3. About Page**

![screenshot](images/project_3_images/Help_Page.png)
**Fig 4. Help Page**

![screenshot](images/project_3_images/Contact_Page.png)
**Fig 5. Contact Page**

[Back to Portfolio](./)

<script>
  // Function to toggle theme and update button icon
  function toggleTheme() {
    const body = document.body;
    const button = document.getElementById("toggleTheme");

    if (body.classList.contains("dark-mode")) {
      body.classList.remove("dark-mode");
      localStorage.setItem("theme", "light");
      button.textContent = "☀️"; // Show sun for day mode
    } else {
      body.classList.add("dark-mode");
      localStorage.setItem("theme", "dark");
      button.textContent = "🌙"; // Show moon for night mode
    }
  }

  // Set default theme on page load and update button icon
  document.addEventListener("DOMContentLoaded", () => {
    const body = document.body;
    const button = document.getElementById("toggleTheme");
    const savedTheme = localStorage.getItem("theme");

    if (savedTheme === "dark") {
      body.classList.add("dark-mode");
      button.textContent = "🌙"; // Show moon for night mode
    } else {
      body.classList.remove("dark-mode");
      button.textContent = "☀️"; // Show sun for day mode
    }
  });
</script>

<style>
  :root {
    --background-color: #ffffff;
    --text-color: #000000;
    --link-color: #1a73e8;
    --heading-color: #000000; /* Default heading color */
  }

  body.dark-mode {
    --background-color: #121212;
    --text-color: #e0e0e0;
    --link-color: #bb86fc;
    --heading-color: #ffffff; /* Light heading color for dark mode */
  }

  /* Apply background and text colors globally */
  body {
    background-color: var(--background-color);
    color: var(--text-color);
  }

  /* Ensure headings inherit colors */
  h1, h2, h3, h4, h5, h6 {
    color: var(--heading-color);
  }

  /* Ensure links adapt */
  a {
    color: var(--link-color);
  }

  /* Ensure list items and nested elements inherit text color */
  ul, ol, li, p, span, div, strong, em, b, i {
    color: var(--text-color) !important;
  }

  /* Add a small margin for better list readability */
  ul > li, ol > li {
    margin-bottom: 0.5rem;
  }

  /* Toggle button styling */
  .theme-toggle {
    position: fixed;
    top: 10px;
    right: 10px;
    z-index: 1000;
  }

  #toggleTheme {
    background: none;
    border: none;
    font-size: 1.5rem;
    cursor: pointer;
  }
</style>

