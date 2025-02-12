<!DOCTYPE html>
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
        }
        .container {
            max-width: 800px;
            margin: 0 auto;
            background-color: #f9f9f9;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }
        header {
            text-align: center;
            padding: 20px;
            background-color: #4a90e2;
            color: white;
            border-radius: 5px;
            margin-bottom: 20px;
        }
        section {
            margin-bottom: 30px;
            padding: 20px;
            background-color: white;
            border-radius: 5px;
        }
        h1, h2 {
            color: #333;
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
            background-color: #4a90e2;
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
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>Anastasia Anna Pateli</h1>
            <p>Welcome to my personal page</p>
        </header>
        <section>
            <h2>About me</h2>
            <p>...</p>
        </section>
    </div>

    <div id="mySidebar" class="sidebar">
        <a href="javascript:void(0)" class="closebtn" onclick="closeNav()">&times;</a>
        <div class="center-content">
            <a href="#">Choice 1</a>
            <a href="#">Choice 2</a>
            <a href="#">Choice 3</a>
        </div>
    </div>

    <button class="openbtn" onclick="openNav()">☰ Open Sidebar</button>

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
        function closeNav() {
            document.getElementById("mySidebar").style.width = "0";
        }
    </script>
</body>
</html>
