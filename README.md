<!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Meine Erweiterte Website</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Willkommen auf meiner erweiterten Website</h1>
    </header>
    <main>
        <p>Dies ist eine erweiterte Beispielwebsite.</p>
        <button id="clickMe">Klick mich!</button>
    </main>
    <footer>
        <p>&copy; 2023 Mein Name</p>
    </footer>
    <script src="script.js"></script>
</body>
</html>
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f4f4f4;
    color: #333;
}
header {
    background-color: #333;
    color: #fff;
    padding: 10px 0;
    text-align: center;
}
main {
    padding: 20px;
}
footer {
    background-color: #333;
    color: #fff;
    text-align: center;
    padding: 10px 0;
    position: fixed;
    width: 100%;
    bottom: 0;
}
button {
    padding: 10px 20px;
    font-size: 16px;
    cursor: pointer;
}
document.getElementById('clickMe').addEventListener('click', function() {
    alert('Danke für den Klick!');
});
