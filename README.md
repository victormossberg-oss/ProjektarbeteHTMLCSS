PROJEKTBESKRIVNING
------------------------
Strandhotellet BnB är en websida för ett fiktivt bed & breakfast i Visby.
Websidan består av 5 sidor:

* Startsida (index.html) - Hero-bild, kort presentation och aktiviteter.
* Rum & Priser (rum.html) - Information och bilder på bokningsbara rum.
* Matsalen (matsalen.html) - Middagsmeny med olika rätter.
* Boka (boka.html) - Bokningsformulär för bokningsförfrågan.
* Tack (tack.html) - Bekräftelse efter bokning.

Syftet är att visa upp hotellets erbjudanden på ett modernt, estetiskt och lättnavigerat sätt - både på mobil och desktop.

DESIGN
------------------------
Färgtema-
* --sand (#f6f3ec) – en varm, neutral bakgrund som ska påminna om Gotlands stränder.

* --hav (#5c7c89) – en lugn blågrå ton inspirerad av havet.

* --accent (#cfa77b) – detaljfärg som symboliserar solnedgång och värme.
Tillsammans ska dessa fäger ge ett lugnt och harmoniskt intryck.

Typografi-
Fontfamilj: Poppins, ett modernt och lättläst typsnitt

Layout-
* Flexbox används för att skapa responsiva rader och kolumner.
* Mycket "White space" för att ge fokus på bilderna.
* Bilderna är centrala för att ge användaren en känsla av platsen.
* background-image med mörk overlay (rgba) används i heron och matsalen för bättre kontrast mot text.

CSS-MÖNSTER
-----------------------
Funktion                          CSS-mönster
- Hamburgermeny                   input type="checkbox" + label + :checked för att toggla menyn utan JavaScript
- Hover-effekter på bilder        transform: scale() och opacity på .feature-overlay
- Responsiv layout                Flexbok och media queries (max-width: 600px och min-width: 600px)
- Hero-overlay                    ::before med rgba() för mörk toning ovanpå bakgrundsbild
- FAQ                             HTML5 "details" och "summary" – enkel inbyggd interaktivitet
- Formulärfokus                   :focus med accentfärg på inputfält för tydligare användarfeedback

KÄNDA BEGRÄNSNINGAR
----------------------
* Bokningsformuläret skickar ingen faktisk data utan bara en länk till tack.html

FÖRBÄTTRINGAR
---------------------
* Koppla formuläret till ett riktigt backend-script
* Göra dark mode-alternativ
* Lägga in fler bilder och recensioner från besökare

STILGUIDE
--------------------
Färgpalett -
Namn: Sand
Hex: #f6f3ec
Användning: Bakgrund & sektioner

Namn: Hav
Hex: #5c7c89
Användning: Rubriker, logotyp, länkar

Namn: Accent
Hex: #cfa77b
Användning: Knappar & detaljer

Namn: Text
Hex: #333333
Användning: Brödtext

--------------------

Typografi -
Rubriker: Poppins, semibold–bold

Brödtext: Poppins, regular

Storlekar: clamp(1rem, 2vw, 3rem) för anpassad skala.

Knappar - 
.button {
  background: var(--accent);
  color: white;
  border-radius: 0.5rem;
  padding: 0.8rem 2rem;
  transition: background 0.3s ease;
}
.button:hover {
  background: var(--hav);
}

Länkar -
a {
  color: var(--hav);
  text-decoration: none;
}
a:hover {
  border-bottom: 2px solid var(--accent);
}

Formulärfält -
input, select, textarea {
  border: 1px solid #ddd;
  border-radius: 0.5rem;
  padding: 0.7rem;
}
input:focus {
  border-color: var(--accent);
}


