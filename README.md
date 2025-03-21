<!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hochzeitseinladung erstellen</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Erstellen Sie Ihre Hochzeitseinladung</h1>
    </header>
    <main>
        <!-- Schritt 1: Vorlage auswählen -->
        <section id="templateSelection">
            <h2>Wählen Sie eine Vorlage</h2>
            <div class="template-options">
                <div class="template" data-template="floral">
                    <img src="floral-template.jpg" alt="Floral Template">
                    <p>Floral Template</p>
                </div>
                <div class="template" data-template="mono">
                    <img src="mono-template.jpg" alt="Mono Template">
                    <p>Mono Template</p>
                </div>
                <div class="template" data-template="galleria">
                    <img src="galleria-template.jpg" alt="Galleria Template">
                    <p>Galleria Template</p>
                </div>
            </div>
        </section>

        <!-- Schritt 2: Informationen eingeben -->
        <section id="informationForm" class="hidden">
            <h2>Geben Sie Ihre Informationen ein</h2>
            <form id="weddingForm">
                <label for="brideName">Name der Braut:</label>
                <input type="text" id="brideName" name="brideName" required>

                <label for="groomName">Name des Bräutigams:</label>
                <input type="text" id="groomName" name="groomName" required>

                <label for="weddingDate">Hochzeitsdatum:</label>
                <input type="date" id="weddingDate" name="weddingDate" required>

                <label for="ceremonyLocation">Ort der Zeremonie:</label>
                <input type="text" id="ceremonyLocation" name="ceremonyLocation" required>

                <label for="partyLocation">Ort der Feier:</label>
                <input type="text" id="partyLocation" name="partyLocation">

                <label for="email">E-Mail-Adresse:</label>
                <input type="email" id="email" name="email" required>

                <label for="phone">Telefonnummer:</label>
                <input type="tel" id="phone" name="phone" required>

                <button type="submit">Einladung erstellen</button>
            </form>
        </section>

        <!-- Schritt 3: Einladung anzeigen -->
        <section id="invitationDisplay" class="hidden">
            <h2>Ihre Einladung</h2>
            <div id="invitationContent">
                <!-- Hier wird die Einladung dynamisch eingefügt -->
            </div>
            <button id="downloadButton">Einladung herunterladen</button>
        </section>
    </main>
    <footer>
        <p>&copy; 2025 Hochzeitseinladungsgenerator</p>
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
    padding: 20px;
    text-align: center;
}
main {
    padding: 20px;
    max-width: 800px;
    margin: 0 auto;
}
.template-options {
    display: flex;
    gap: 20px;
    justify-content: center;
}
.template {
    border: 1px solid #ddd;
    padding: 10px;
    text-align: center;
    cursor: pointer;
}
.template img {
    width: 150px;
    height: 200px;
    object-fit: cover;
}
.hidden {
    display: none;
}
form {
    display: flex;
    flex-direction: column;
}
label {
    margin-top: 10px;
}
input, button {
    margin-top: 5px;
    padding: 10px;
    font-size: 16px;
}
button {
    background-color: #333;
    color: #fff;
    border: none;
    cursor: pointer;
}
button:hover {
    background-color: #555;
}
#invitationDisplay {
    margin-top: 20px;
    padding: 20px;
    background-color: #fff;
    border: 1px solid #ddd;
}
let selectedTemplate = null;

// Vorlage auswählen
document.querySelectorAll('.template').forEach(template => {
    template.addEventListener('click', () => {
        selectedTemplate = template.getAttribute('data-template');
        document.getElementById('templateSelection').classList.add('hidden');
        document.getElementById('informationForm').classList.remove('hidden');
    });
});

// Formular abschicken
document.getElementById('weddingForm').addEventListener('submit', function(event) {
    event.preventDefault();

    const brideName = document.getElementById('brideName').value;
    const groomName = document.getElementById('groomName').value;
    const weddingDate = document.getElementById('weddingDate').value;
    const ceremonyLocation = document.getElementById('ceremonyLocation').value;
    const partyLocation = document.getElementById('partyLocation').value;

    // Einladung erstellen
    const invitationContent = `
        <h3>${brideName} & ${groomName}</h3>
        <p>Wir laden Sie herzlich zu unserer Hochzeit ein!</p>
        <p><strong>Datum:</strong> ${weddingDate}</p>
        <p><strong>Ort der Zeremonie:</strong> ${ceremonyLocation}</p>
        ${partyLocation ? `<p><strong>Ort der Feier:</strong> ${partyLocation}</p>` : ''}
    `;

    document.getElementById('invitationContent').innerHTML = invitationContent;
    document.getElementById('informationForm').classList.add('hidden');
    document.getElementById('invitationDisplay').classList.remove('hidden');
});

// Einladung herunterladen (Beispiel)
document.getElementById('downloadButton').addEventListener('click', () => {
    alert('Einladung wird heruntergeladen...');
    // Hier könnte der Download-Code hinzugefügt werden
});
