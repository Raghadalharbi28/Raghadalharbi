# Raghadalharbi
Cleaning company website
<!DOCTYPE html>
<html lang="de">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>AGG Gebäudereinigungs</title>
<style>
body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background-color: #f0f4f8;
    margin: 0;
    padding: 0;
    color: #333;
}
header {
    background-color: #ffffff;
    padding: 40px 20px;
    text-align: center;
    box-shadow: 0 2px 8px rgba(0,0,0,0.1);
}
header h1 span.a { color: #007acc; }
header h1 span.gg { color: #28a745; }
main {
    max-width: 900px;
    margin: 50px auto;
    background-color: #ffffff;
    padding: 30px 40px;
    border-radius: 10px;
    box-shadow: 0 4px 15px rgba(0,0,0,0.1);
}
h2 { color: #007acc; margin-top: 0; }
.contact h2 { color: #28a745; }
.contact p { margin: 8px 0; }
footer { text-align: center; margin-top: 60px; padding: 20px 0; background-color: #e6f2ff; color: #555; }
.lang-btn { cursor: pointer; color: #007acc; font-weight: bold; margin-left: 10px; }
.hidden { display: none; }
@media (max-width: 600px) { main { margin: 20px; padding: 20px; } header h1 { font-size: 1.8em; } }
</style>
</head>
<body>
<header>
    <h1><span class="a">A</span><span class="gg">GG</span> - Allgemeine Gebäudereinigungs GmbH & Co. KG</h1>
    <div>
        <span class="lang-btn" onclick="switchLang('de')">DE</span> |
        <span class="lang-btn" onclick="switchLang('en')">EN</span>
    </div>
</header>
<main>
    <div id="de">
        <h2>Über uns</h2>
        <p>Wir sind ein professionelles Reinigungsunternehmen in Berlin. Wir bieten hochwertige Reinigungsdienste für Büros, Gebäude und private Haushalte.</p>
        <div class="contact">
            <h2>Kontakt</h2>
            <p>Telefon: 030 7568020</p>
            <p>Adresse: Manteuffelstraße 65, 12103 Berlin</p>
            <p>Spezialisierung: Gebäudereinigung</p>
        </div>
    </div>
    <div id="en" class="hidden">
        <h2>About Us</h2>
        <p>We are a professional cleaning company in Berlin. We provide high-quality cleaning services for offices, buildings, and private households.</p>
        <div class="contact">
            <h2>Contact</h2>
            <p>Phone: 030 7568020</p>
            <p>Address: Manteuffelstraße 65, 12103 Berlin</p>
            <p>Specialization: Building Cleaning</p>
        </div>
    </div>
</main>
<footer>
    &copy; 2026 AGG Gebäudereinigungs. All rights reserved.
</footer>

<script>
function switchLang(lang) {
    document.getElementById('de').classList.add('hidden');
    document.getElementById('en').classList.add('hidden');
    document.getElementById(lang).classList.remove('hidden');
}
</script>
</body>
</html>
