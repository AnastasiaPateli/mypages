<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Anastasia Anna Pateli - Architect</title>
    <link rel="stylesheet" href="styles.css">
    <style>
        body {
            margin: 0;
            font-family: Arial, sans-serif;
        }
        .hero {
            position: relative;
            width: 100%;
            height: 100vh;
            overflow: hidden;
            display: flex;
            justify-content: center;
            align-items: center;
        }
        .background-image {
            position: absolute;
            width: 100%;
            height: 100%;
            object-fit: cover;
            animation: zoom-in 10s infinite alternate;
        }
        @keyframes zoom-in {
            from {
                transform: scale(1);
            }
            to {
                transform: scale(1.1);
            }
        }
        .overlay {
            position: absolute;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.5);
        }
        .name {
            position: absolute;
            bottom: 20px;
            left: 20px;
            color: white;
            font-size: 24px;
        }
        .logo {
            position: absolute;
            top: 20px;
            left: 20px;
            width: 50px;
        }
        .menu-button {
            position: absolute;
            top: 20px;
            right: 20px;
            font-size: 24px;
            background: none;
            border: none;
            color: white;
            cursor: pointer;
        }
        .side-menu {
            position: fixed;
            top: 0;
            right: -250px;
            width: 250px;
            height: 100%;
            background: white;
            box-shadow: -2px 0 5px rgba(0, 0, 0, 0.5);
            transition: right 0.3s;
            padding: 20px;
        }
        .side-menu ul {
            list-style: none;
            padding: 0;
        }
        .side-menu li {
            margin: 20px 0;
            cursor: pointer;
        }
        .close-button {
            position: absolute;
            top: 10px;
            right: 10px;
            font-size: 24px;
            border: none;
            background: none;
            cursor: pointer;
        }
        .content {
            padding: 20px;
            text-align: center;
        }
    </style>
</head>
<body>
    <div class="hero">
        <img src="placeholder.jpg" alt="Background Image" class="background-image">
        <div class="overlay"></div>
        <h1 class="name">Anastasia Anna Pateli</h1>
        <img src="logo.png" alt="Logo" class="logo">
        <button class="menu-button" onclick="toggleMenu()">☰</button>
    </div>
    
    <div class="side-menu" id="sideMenu">
        <button class="close-button" onclick="toggleMenu()">&times;</button>
        <ul>
            <li onclick="showContent('about')">What you have to know about me</li>
            <li onclick="showContent('research')">Past Research Programs</li>
            <li onclick="showContent('distinctions')">Distinctions and praises</li>
        </ul>
    </div>
    
    <div class="content" id="content">
        <p>Select an option from the menu to see details.</p>
    </div>
    
    <script>
        function toggleMenu() {
            var menu = document.getElementById("sideMenu");
            if (menu.style.right === "0px") {
                menu.style.right = "-250px";
            } else {
                menu.style.right = "0px";
            }
        }
        function showContent(section) {
            var content = document.getElementById("content");
            if (section === "about") {
                content.innerHTML = "<h2>About Me</h2><p>Details about me...</p>";
            } else if (section === "research") {
                content.innerHTML = "<h2>Past Research Programs</h2><p>Details about research...</p>";
            } else if (section === "distinctions") {
                content.innerHTML = "<h2>Distinctions and Praises</h2><p>Details about distinctions...</p>";
            }
        }
    </script>
</body>
</html>
