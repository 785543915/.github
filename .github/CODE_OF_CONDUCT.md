<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Application Thème Sombre</title>
    <style>
        body {
            background-color: #121212;
            color: #ffffff;
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            transition: background-color 0.3s, color 0.3s;
        }
        .navbar {
            background-color: #1e1e1e;
            padding: 10px;
            display: flex;
            justify-content: space-around;
        }
        .navbar a {
            color: #ffffff;
            text-decoration: none;
            padding: 10px;
        }
        .navbar a:hover {
            background-color: #333333;
        }
        .content {
            padding: 20px;
        }
        .button {
            background-color: #6200ea;
            color: white;
            border: none;
            padding: 10px 20px;
            cursor: pointer;
            border-radius: 5px;
            transition: background-color 0.3s;
        }
        .button:hover {
            background-color: #3700b3;
        }
        .accessibility-settings {
            margin-top: 20px;
        }
        .reading-mode {
            background-color: #ffffff;
            color: #000000;
        }
    </style>
</head>
<body>
    <div class="navbar">
        <a href="#home">Accueil</a>
        <a href="#settings">Paramètres</a>
    </div>
    <div class="content">
        <h1>Bienvenue dans l'application</h1>
        <p>Ceci est un exemple d'application avec un thème sombre et des fonctionnalités d'accessibilité.</p>
        <button class="button" onclick="toggleReadingMode()">Mode de Lecture</button>
        <div class="accessibility-settings">
            <h2>Paramètres d'Accessibilité</h2>
            <label for="fontSize">Taille de la police :</label>
            <select id="fontSize" onchange="changeFontSize(this.value)">
                <option value="16px">Normal</option>
                <option value="20px">Grande</option>
                <option value="24px">Très Grande</option>
            </select>
        </div>
    </div>
    <script>
        function changeFontSize(size) {
            document.body.style.fontSize = size;
        }
        function toggleReadingMode() {
            document.body.classList.toggle('reading-mode');
            if (document.body.classList.contains('reading-mode')) {
                document.body.style.backgroundColor = '#ffffff';
                document.body.style.color = '#000000';
            } else {
                document.body.style.backgroundColor = '#121212';
                document.body.style.color = '#ffffff';
            }
        }
    </script>
</body>
</html>
