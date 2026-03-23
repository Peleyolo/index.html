# index.html
 Hurraa Pele Turkkiin
<!DOCTYPE html>
<html lang="fi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Reissulaskuri</title>
<style>
    body {
        font-family: Arial, sans-serif;
        text-align: center;
        background: linear-gradient(135deg, #00c6ff, #0072ff);
        color: white;
        padding: 30px;
    }
    h1 { font-size: 28px; }
    .countdown { font-size: 24px; margin: 20px 0; }
    .vitsi {
        margin-top: 30px;
        font-size: 20px;
        background: rgba(255,255,255,0.2);
        padding: 15px;
        border-radius: 12px;
    }
</style>
</head>
<body>

<h1>✈️ REISSULASKURI 🌴</h1>

<div class="countdown" id="countdown"></div>

<div class="vitsi" id="vitsi"></div>

<script>
const targetDate = new Date("2026-05-06T09:00:00");

// 45 vitsiä
const vitsit = [
"Aloitin pakkaamisen… avaamalla Netflixin",
"Matkalaukku on tyhjä… mutta pää täynnä lomaa",
"Tein pakkauslistan. Kadotin sen heti",
"Passi tallessa… jossain",
"Pakkaan kevyesti – 5 varavaatetta per päivä",
"Tarviiko 12 paitaa viikon reissulle",
"Lentokentälle lähden ajoissa… ehkä",
"Herätys 04:00 – en nuku",
"Kuka kantaa mun laukun",
"Minimalistisesti… kahdella laukulla",
"Missä syödään ensin",
"Budjetti tehty… ei käytetä",
"Sää checkattu 15 kertaa",
"Aurinkolasit ok… aurinko ei varma",
"Loma alkaa kun pääsen koneeseen",
"Kuukausi! Nyt paniikki",
"Tarviiko sukkia",
"Nukun koneessa… tai en",
"Powerbank > hammasharja",
"Toivottavasti en tarvitse vakuutusta",
"Pakkaan kevyesti… oikeasti tällä kertaa",
"Offline kartat ladattu… eksytään silti",
"Kuka on navigaattori",
"Tällä reissulla säästetään… joo",
"3 viikkoa! HYPE",
"Laukku kiinni… avaan sen 7 kertaa",
"Unohdan jotain varmasti",
"Käsimatkatavara = snacks",
"Lentokenttä = seikkailu",
"Pitäiskö pakata",
"2 viikkoa! Nyt säätö",
"Tarkistan passin päivittäin",
"Sää muuttui… pakkaan kaiken",
"Yksi laukku riittää… ehkä",
"Kohta mennään",
"Nyt oikea countdown",
"En voi keskittyä",
"Mitä ei saa unohtaa",
"VIIKKO!!!",
"Laukku melkein valmis",
"Viimeinen hetki pakata",
"Nukunko enää",
"Tämä on nyt todeksi",
"En pysy housuissa",
"HUOMENNA MENNÄÄN",
"SE ON NYT!!!"
];

function updateCountdown() {
    const now = new Date();
    const diff = targetDate - now;

    const days = Math.floor(diff / (1000 * 60 * 60 * 24));
    const hours = Math.floor((diff / (1000 * 60 * 60)) % 24);
    const minutes = Math.floor((diff / (1000 * 60)) % 60);
    const seconds = Math.floor((diff / 1000) % 60);

    document.getElementById("countdown").innerHTML =
        `${days} päivää ${hours}h ${minutes}m ${seconds}s`;

    // valitse päivän vitsi
    let index = 45 - days;
    if (index < 0) index = 0;
    if (index >= vitsit.length) index = vitsit.length - 1;

    document.getElementById("vitsi").innerHTML =
        "😂 " + vitsit[index];
}

setInterval(updateCountdown, 1000);
updateCountdown();
</script>

</body>
</html>
