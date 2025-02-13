<!DOCTYPE html>
<html lang="el">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Βιογραφικό Αρχιτέκτονα</title>
    <link rel="stylesheet" href="styles.css">
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
            color: #333;
        }
        header {
            background: #06fbef;
            color: white;
            text-align: center;
            padding: 20px;
        }
        #about {
            text-align: center;
            padding: 50px;
        }
        #about img {
            max-width: 200px;
            border-radius: 50%;
        }
        .gallery {
            display: flex;
            justify-content: center;
            gap: 20px;
            padding: 50px;
        }
        .project {
            background: white;
            padding: 10px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        .project img {
            max-width: 100%;
            border-radius: 10px;
        }
        form {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 10px;
            padding: 20px;
        }
        input, textarea {
            width: 80%;
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        button {
            background: #222;
            color: white;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <header>
        <h1>Όνομα Αρχιτέκτονα</h1>
        <p>Σύγχρονη Αρχιτεκτονική & Καινοτόμος Σχεδιασμός</p>
    </header>
    <section id="about">
        <img src="architect.jpg" alt="Αρχιτέκτονας">
        <p>Είμαι ένας παθιασμένος αρχιτέκτονας με εμπειρία στον μοντέρνο και βιώσιμο σχεδιασμό.</p>
    </section>
    <section id="projects">
        <h2>Έργα</h2>
        <div class="gallery">
            <div class="project">
                <img src="project1.jpg" alt="Project 1">
                <p>Σύγχρονη κατοικία με minimal γραμμές.</p>
            </div>
            <div class="project">
                <img src="project2.jpg" alt="Project 2">
                <p>Επαγγελματικός χώρος με βιώσιμα υλικά.</p>
            </div>
        </div>
    </section>
    <section id="contact">
        <h2>Επικοινωνία</h2>
        <form id="contact-form">
            <input type="text" id="name" placeholder="Όνομα" required>
            <input type="email" id="email" placeholder="Email" required>
            <textarea id="message" placeholder="Μήνυμα" required></textarea>
            <button type="submit">Αποστολή</button>
        </form>
        <p id="response-message" style="text-align: center; color: green; display: none;">Το μήνυμά σας εστάλη!</p>
    </section>
    <script>
        document.getElementById('contact-form').addEventListener('submit', function(event) {
            event.preventDefault();
            document.getElementById('response-message').style.display = 'block';
            setTimeout(() => {
                document.getElementById('response-message').style.display = 'none';
                document.getElementById('contact-form').reset();
            }, 3000);
        });
    </script>
</body>
</html>
