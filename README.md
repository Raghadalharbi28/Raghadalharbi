<!DOCTYPE html>
<html lang="de">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>AGG Gebäudereinigungs</title>
<link href="https://cdn.jsdelivr.net/npm/aos@2.3.4/dist/aos.css" rel="stylesheet">
<style>
body {
    margin: 0; padding: 0; font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; background-color: #f0f4f8; color: #333;
}
header {
    background-color: #fff; padding: 60px 20px; text-align: center; box-shadow: 0 2px 8px rgba(0,0,0,0.1);
}
header h1 span.a { color: #007acc; }
header h1 span.gg { color: #28a745; }
.lang-btn { cursor: pointer; color: #007acc; font-weight: bold; margin-left: 10px; }
section { padding: 80px 20px; max-width: 1000px; margin: auto; }
h2 { color: #007acc; margin-top: 0; text-align: center; }
p { font-size: 1.1em; line-height: 1.7; }
.service { display: flex; flex-wrap: wrap; justify-content: center; margin-top: 50px; }
.service-item { width: 300px; margin: 20px; background: #fff; border-radius: 10px; box-shadow: 0 4px 15px rgba(0,0,0,0.1); overflow: hidden; }
.service-item img { width: 100%; display: block; }
.service-item h3 { margin: 15px; color: #28a745; }
.service-item p { margin: 0 15px 15px 15px; }
footer { background-color: #e6f2ff; color: #555; padding: 40px 20px; text-align: center; }
.map-container { margin-top: 40px; text-align: center; }
iframe { border:0; width:100%; height:400px; border-radius:10px; }
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

<section id="de">
    <h2 data-aos="fade-up">Über uns</h2>
    <p data-aos="fade-right">Wir sind ein professionelles Reinigungsunternehmen in Berlin. Wir bieten hochwertige Reinigungsdienste für Büros, Gebäude und private Haushalte.</p>

    <div class="service">
        <div class="service-item" data-aos="fade-left">
            <img src="https://source.unsplash.com/300x200/?cleaning,office" alt="Reinigung Büro">
            <h3>Büroreinigung</h3>
            <p>Professionelle Reinigung für Büros aller Größen.</p>
        </div>
        <div class="service-item" data-aos="fade-right">
            <img src="https://source.unsplash.com/300x200/?cleaning,building" alt="Gebäudereinigung">
            <h3>Gebäudereinigung</h3>
            <p>Wir reinigen Gebäude gründlich und zuverlässig.</p>
        </div>
        <div class="service-item" data-aos="fade-left">
            <img src="https://source.unsplash.com/300x200/?cleaning,house" alt="Privathaushalte">
            <h3>Privathaushalte</h3>
            <p>Sauberkeit in Ihrem Zuhause durch Profis.</p>
        </div>
    </div>
</section>

<section id="en" class="hidden">
    <h2 data-aos="fade-up">About Us</h2>
    <p data-aos="fade-right">We are a professional cleaning company in Berlin. We provide high-quality cleaning services for offices, buildings, and private households.</p>

    <div class="service">
        <div class="service-item" data-aos="fade-left">
            <img src="https://source.unsplash.com/300x200/?cleaning,office" alt="Office Cleaning">
            <h3>Office Cleaning</h3>
            <p>Professional cleaning for offices of all sizes.</p>
        </div>
        <div class="service-item" data-aos="fade-right">
            <img src="https://source.unsplash.com/300x200/?cleaning,building" alt="Building Cleaning">
            <h3>Building Cleaning</h3>
            <p>We clean buildings thoroughly and reliably.</p>
        </div>
        <div class="service-item" data-aos="fade-left">
            <img src="https://source.unsplash.com/300x200/?cleaning,house" alt="House Cleaning">
            <h3>Private Households</h3>
            <p>Professional home cleaning for your comfort.</p>
        </div>
    </div>
</section>

<footer>
    <p>📞 Telefon / Phone: 030 7568020</p>
    <div class="map-container">
        <iframe src="https://www.google.com/maps/embed/v1/place?key=YOUR_GOOGLE_MAPS_API_KEY&q=Manteuffelstraße+65,Berlin" allowfullscreen></iframe>
    </div>
</footer>

<script src="https://cdn.jsdelivr.net/npm/aos@2.3.4/dist/aos.js"></script>
<script>
AOS.init({ duration: 1000, once: true });

function switchLang(lang){
    document.getElementById('de').classList.add('hidden');
    document.getElementById('en').classList.add('hidden');
    document.getElementById(lang).classList.remove('hidden');
}
</script>
</body>
</html>
