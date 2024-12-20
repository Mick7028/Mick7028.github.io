---
layout: default
title: Home
---

<!-- Dark Mode Toggle -->
<div class="theme-toggle">
  <button id="toggleTheme" onclick="toggleTheme()">🌙</button>
</div>

# Portfolio

---

## Navigation

- [Senior Project](#senior-project)
- [Programming Projects](#programming-projects)
- [Lab Projects](#lab-projects)
- [Ethics Papers](#ethics-papers)
- [Presentations](#presentations)
- [Contact for Private Repositories](#contact-for-private-repositories)

---

## <a href="https://github.com/Mick7028/CSU-Senior-Project/blob/master/docs/Defense_Documentation.md" target="_blank">Senior Project</a>

<a href="https://github.com/Mick7028/CSU-Senior-Project/blob/master/docs/Defense_Documentation.md" target="_blank">
  ![VR Language Immersion Activity](images/Hover_Name.jpg)
</a>

## Programming Projects

---

### [Calculating Average Score and Winner | CSCI 301](project1)

[![Score Ranking](images/ScoreRanking.jpg)](project1)

### [Mean, Median, and Mode Calculator | CSCI 325](project2)

[![Menu of project2](images/project_2_images/All.png)](project2)

### [Ruby on Rails Tutorial: Ch. 1 - 5 | CSCI 334](project3)

[![Project 3 Thumbnail Name](images/RubyOnRails.png)](project3)

## Lab Projects

---

### [SQL Injection Attack | CSCI 452](project4)

[![Project 4 Thumbnail Name](images/SQLInjection.png)](project4)

### [Meltdown Attack Lab | CSCI 452](project5)

[![Project 5 Thumbnail Name](images/Meltdown.png)](project5)

## Ethics Papers
-------------

### [Think Ethically](/pdf/Ethics Paper 1.pdf)

-   **Class: CSCI 332**  
-   **Grade: A**

### [Ethics & Computing](/pdf/Ethics Paper 2.pdf)

-   **Class: CSCI 301** 
-   **Grade: A**

### [Can Hacking Be Ethical?](/pdf/Ethics Paper 3.pdf)

-   **Class: CSCI 235** 
-   **Grade: A**

---

## Presentations

### [Ransomware Attacks](/pdf/Security Presentation.pdf)

- **Class: CSCI 301**  
- **Grade: A**

### [SQL Injections](/pdf/SQL Injection.pdf)

- **Class: CSCI 352**  
- **Grade: A**

---

## Contact for Private Repositories

*For access to my private project repositories, please [email me](mailto:michaelson1999@gmail.com?subject=GitHub%20Access) with the subject line, GitHub Access.*

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
    --list-item-color: #000000; /* Default list item color */
  }

  body.dark-mode {
    --background-color: #121212;
    --text-color: #e0e0e0;
    --link-color: #bb86fc;
    --heading-color: #ffffff; /* Light heading color for dark mode */
    --list-item-color: #e0e0e0; /* Light list item color for dark mode */
  }

  body {
    background-color: var(--background-color);
    color: var(--text-color);
  }

  h1, h2, h3, h4, h5, h6 {
    color: var(--heading-color);
  }

  a {
    color: var(--link-color);
  }

  /* Ensure lists and bullet points inherit the correct color */
  ul, ol, li, li span {
    color: var(--list-item-color);
  }

  /* Specific styles for list items with inline spans */
  li > span {
    display: inline-block;
    color: var(--list-item-color);
  }

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
