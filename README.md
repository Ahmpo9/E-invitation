<!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Einladung erstellen</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Erstellen Sie Ihre Einladung</h1>
    </header>
    <main>
        <!-- Formular zur Erstellung der Einladung -->
        <form id="createInvitationForm">
            <label for="eventType">Art der Veranstaltung:</label>
            <select id="eventType" name="eventType" required>
                <option value="Hochzeit">Hochzeit</option>
                <option value="Geburtstag">Geburtstag</option>
                <option value="Party">Party</option>
                <option value="Andere">Andere</option>
            </select>

            <label for="eventDate">Datum:</label>
            <input type="date" id="eventDate" name="eventDate" required>

            <label for="eventLocation">Ort:</label>
            <input type="text" id="eventLocation" name="eventLocation" required>

            <label for="hostName1">Name des Gastgebers 1 (z. B. Braut):</label>
            <input type="text" id="hostName1" name="hostName1" required>

            <label for="hostName2">Name des Gastgebers 2 (z. B. Bräutigam):</label>
            <input type="text" id="hostName2" name="hostName2" required>

            <label for="maxGuests">Maximale Anzahl der Gäste:</label>
            <input type="number" id="maxGuests" name="maxGuests" required>

            <button type="submit">Einladung erstellen</button>
        </form>

        <!-- Link zur Einladung -->
        <div id="invitationLink" class="hidden">
            <h2>Ihr Einladungslink:</h2>
            <a id="generatedLink" target="_blank">Link zur Einladung</a>
        </div>
    </main>
    <footer>
        <p>&copy; 2025 Einladungsgenerator</p>
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
    max-width: 600px;
    margin: 0 auto;
}
form {
    display: flex;
    flex-direction: column;
}
label {
    margin-top: 10px;
}
input, select, textarea, button {
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
.hidden {
    display: none;
}
#invitationLink {
    margin-top: 20px;
    padding: 20px;
    background-color: #fff;
    border: 1px solid #ddd;
}
#generatedLink {
    color: #007BFF;
    text-decoration: none;
}
#generatedLink:hover {
    text-decoration: underline;
}
document.getElementById('createInvitationForm').addEventListener('submit', function(event) {
    event.preventDefault();

    // Daten aus dem Formular sammeln
    const eventType = document.getElementById('eventType').value;
    const eventDate = document.getElementById('eventDate').value;
    const eventLocation = document.getElementById('eventLocation').value;
    const hostName1 = document.getElementById('hostName1').value;
    const hostName2 = document.getElementById('hostName2').value;
    const maxGuests = document.getElementById('maxGuests').value;

    // Einladungslink erstellen (Beispiel: Einfache URL mit Parametern)
    const invitationData = {
        type: eventType,
        date: eventDate,
        location: eventLocation,
        host1: hostName1,
        host2: hostName2,
        guests: maxGuests
    };
    const baseUrl = window.location.href.split('?')[0]; // Aktuelle URL ohne Parameter
    const invitationLink = `${baseUrl}?invitation=${encodeURIComponent(JSON.stringify(invitationData))}`;

    // Link anzeigen
    document.getElementById('generatedLink').href = invitationLink;
    document.getElementById('generatedLink').textContent = invitationLink;
    document.getElementById('invitationLink').classList.remove('hidden');
});
