# 🏕️ Stafplanning Buitenzorg

Welkom bij de repository van de **Stafplanning Buitenzorg** tool! Dit is een interactieve, web-gebaseerde kalender ontworpen om het inplannen van vrijwillige kampstaf voor Scoutcentrum Buitenzorg makkelijker en overzichtelijker te maken.

## 🌟 Wat doet deze tool?
Deze applicatie leest het live iCal-bestand (uit Labelbooking) van het kampterrein uit en transformeert deze data naar een visueel aantrekkelijke grid-kalender. Stafleden kunnen in één oogopslag zien:
- Welke weekenden al voorzien zijn van staf.
- Welke weekenden en schoolvakanties nog **leeg** zijn (⚠️).
- Wanneer er grote evenementen of zomerkampen plaatsvinden.

Bovendien kunnen stafleden direct in de kalender dagen **aanvinken** waarop zij willen staffen. Met één druk op de knop wordt er een e-mail gegenereerd naar de HRM-planning met hun gekozen data!

## ✨ Features
* **Live Synchronisatie:** Geen dubbele administratie. De tool haalt altijd de meest actuele `.ics` kalenderdata op.
* **Slimme Overlap & Volledige Dagen:** Afspraken worden visueel als vloeiende balken over meerdere dagen getoond.
* **Schoolvakanties & Feestdagen:** Haalt automatisch de Nederlandse schoolvakanties (Noord, Midden, Zuid) en nationale feestdagen op via openbare iCal-feeds.
* **Interactieve E-mail Generator:** Vink dagen aan, vul je naam in, en de tool bouwt een perfect opgemaakte e-mail voor in je standaard mail-app.
* **Statistieken:** Een ingebouwd leaderboard (`Statistieken 📊` knop) dat toont hoeveel dagen elk staflid in het gekozen jaar al op de planning staat. Jouw eigen naam licht automatisch op in de lijst!
* **Mobielvriendelijk:** Voorzien van een responsive design met een slimme 'roteer'-waarschuwing voor mobiele gebruikers.
* **Robuust Proxy Systeem:** Bevat een *fallback-systeem* met meerdere CORS-proxy's om te garanderen dat de kalender altijd laadt, zelfs als een externe proxy tijdelijk onbereikbaar is.

## 🛠️ Techniek & Hosting
Dit project is gebouwd als een **Single Page Application (SPA)** en is 100% *client-side*. 
- **Talen:** HTML5, CSS3 (CSS Grid), en Vanilla JavaScript (ES6).
- **Geen database:** Alles wordt *on-the-fly* berekend en gerenderd in de browser van de gebruiker.
- **Hosting:** Wordt gehost via **GitHub Pages** en vereist geen backend server (zoals PHP of Node.js).

## ⚙️ Configuratie (Voor beheerders)
Wil je in de toekomst instellingen wijzigen? Open het `index.html` bestand en zoek naar de volgende variabelen in het `<script>` gedeelte:

* **iCal Link aanpassen:** Wijzig de variabele `targetUrl` als de link vanuit het reserveringssysteem verandert.
* **E-mailadres aanpassen:** Zoek in de functie `generateEmail()` naar de variabele `const emailTo = "HRM@buitenzorg.nl";` en wijzig deze.
* **Proxy's:** De lijst met `proxies` zorgt voor de CORS-omzeiling. Deze kunnen in de toekomst worden geüpdatet mochten ze offline gaan.

## 🤝 Bijdragen
Foutje gevonden of een coole nieuwe feature in gedachten? Voel je vrij om een *Pull Request* in te dienen of een *Issue* aan te maken in deze repository.

---
*Gemaakt met ❤️ voor de staf van Scoutcentrum Buitenzorg.*
