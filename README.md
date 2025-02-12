<html lang="el">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Personal Page</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            margin: 0;
            padding: 20px;
            overflow: hidden;
            color: white; /* Set all text to white */
        }

        .zoom-background {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-image: url('final%20decision.png'); /* Change background image */
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
            z-index: -1;
            animation: zoom-in 10s infinite alternate;
        }

        @keyframes zoom-in {
            0% {
                transform: scale(1);
            }
            100% {
                transform: scale(1.1);
            }
        }

        .header-text {
            color: white;
            position: fixed;
            bottom: 20px;
            left: 20px;
        }
        h1, h2 {
            color: white;
        }
        .contact-info {
            background-color: #e8f4f8;
            padding: 15px;
            border-radius: 5px;
        }
        /* Sidebar styles */
        .sidebar {
            height: 100%;
            width: 0;
            position: fixed;
            z-index: 1;
            top: 0;
            right: 0;
            background-color: #111;
            overflow-x: hidden;
            transition: 0.5s;
            padding-top: 60px;
            display: flex;
            justify-content: center;
            align-items: center;
        }
        .sidebar a {
            padding: 8px 8px 8px 32px;
            text-decoration: none;
            font-size: 25px;
            color: #818181;
            display: block;
            transition: 0.3s;
        }
        .sidebar a:hover {
            color: #f1f1f1;
        }
        .sidebar .closebtn {
            position: absolute;
            top: 0;
            right: 25px;
            font-size: 36px;
        }
        .openbtn {
            position: fixed;
            top: 20px;
            right: 20px;
            background-color: black; /* Set button to black */
            color: white;
            padding: 10px 15px;
            border: none;
            cursor: pointer;
            border-radius: 5px;
        }
        .openbtn:hover {
            background-color: #3a78c2;
        }
        .center-content {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100%;
            flex-direction: column;
        }
        a[href="#my-pages"] {
            color: white; /* Set 'my pages' to white */
        }
    </style>
</head>
<body>
    <div class="zoom-background"></div>
    <div class="header-text">
        <h1>Anastasia Anna Pateli</h1>
    </div>

    <div id="mySidebar" class="sidebar">
        <a href="javascript:void(0)" class="closebtn" onclick="closeNav()">&times;</a>
        <div class="center-content">
            <a href="about-me.html">What you have to know about me</a>
            <a href="research-programs.html">Research Programs</a>
            <a href="distinctions-praises.html">Distinctions and Praises</a>
        </div>
    </div>

    <button class="openbtn" onclick="openNav()">☰</button>

    <script>
        function openNav() {
            document.getElementById("mySidebar").style.width = "100%";
        }

        function closeNav() {
            document.getElementById("mySidebar").style.width = "0";
        }
    </script>
</body>
</html>
