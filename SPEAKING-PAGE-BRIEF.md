# Speaking page brief: joeribillast.com/speaking

Checklist om aan te vullen voordat de pagina gebouwd wordt.
Zet de assets in `assets/` en de antwoorden onder elk punt in dit bestand.

---

## A. Beslissingen die ik niet voor jou kan nemen

### A1. Fee-aanpak
Toon je een fee range, "fees on request", of niets?
Aanbeveling: minstens een categorie (bijvoorbeeld "paid keynotes only, fees on request").
Dit filtert gratis-aanvragen weg.

Antwoord:

### A2. Reisbasis en beschikbaarheid
Waar vertrek je vanaf, en tot hoever reis je? Welk boekingsvenster hanteer je?
Voorbeeld: "Based in Lisbon. Speaks across Europe, MENA and North America. Typically booked 3 to 6 months ahead."

Antwoord:

### A3. Formats en duur
Welke formats bied je aan, met welke looptijd?
Bijvoorbeeld: keynote 30/45/60 min, workshop halve dag, panel moderation, live podcast, strategy circle.

Antwoord:

### A4. Waar je nee tegen zegt
Eén zin over het type event dat niet past. Selectiviteit is positionering.

Antwoord:

### A5. Bevestigde komende podia (2026 en 2027)
Toekomstige data verslaan een lijst met verleden. Als er iets vaststaat, noem het.

Antwoord:

### A6. Definitieve podialijst
Eén canonieke lijst. Nu spreken je twee sites elkaar tegen (DGT Innovation staat als Lisbon op webdrie en als Oeiras op joeribillast.com; NEXT Summit staat als 2026 en als Valletta zonder jaar).

Formaat: Event, Stad, Land, Jaar, rol (keynote / panel / moderator / fireside)

Antwoord:

### A7. Boekingsroute
Blijft het `myformflow.io/efficado/contact-joeri`, of wil je een apart speaking-formulier met velden voor datum, stad, publieksgrootte, format en budget?
Aanbeveling: apart formulier. Scheelt een e-mailronde en kwalificeert meteen.

Antwoord:

### A8. Reel-script of transcript
Plak hier de tekst die je in de speaker reel uitspreekt, of laat leeg dan schrijf ik een samenvatting op basis van de video.
Nodig omdat LLM's geen video bekijken.

Antwoord:

### A9. Betere testimonials
De huidige drie zeggen "insightful", "inspiring", "energetic". Vriendelijk maar inwisselbaar.
Vraag aan Akram Saad, Flavio Horta en Van Vo één zin over wat er ná de talk gebeurde.
Zeg het woord: ik schrijf de aanvraagmail als je wil.

Antwoord:

---

## B. Assets in de map `assets/`

Gebruik kebab-case zonder spaties. De bestaande bestanden met spaties in de naam werken wel,
maar worden in HTML als %20 geschreven en dat is fragiel.

- [ ] `speaker-reel-poster.jpg` — still uit de reel, 1600 px breed, onder 300 KB
- [ ] `stage-tedxchiado.jpg` — 1600 px breed, onder 300 KB
- [ ] `stage-marketing-plus-cairo.jpg` — de foto met Philip Kotler
- [ ] `stage-next-summit-valletta.jpg`
- [ ] `stage-dgt-innovation.jpg`
- [ ] `stage-bam-brussels.jpg` (optioneel)
- [ ] `joeri-headshot.jpg` — vierkant of portret, 1000 px
- [ ] `speaker-onesheet.pdf` — als je er al een hebt. Zo niet, zeg het, dan bouw ik er een.

Optioneel maar sterk: logo's van de events, alleen als je toestemming hebt.

Compressietip: `sips -Z 1600 bestand.jpg` op macOS schaalt snel.

---

## C. Technisch, kort antwoord volstaat

### C1. Hoe wordt joeribillast.com gedeployed?
Netlify, Vercel, GitHub Pages, of iets anders?
Ik moet weten hoe `/future-cmo` zonder `.html` werkt, zodat `/speaking` op dezelfde manier resolvet.

Antwoord:

### C2. Search Console
Wat haalt `webdrie.net/the-cmo-of-the-future-marketing-speaker-joeri-billast/` binnen aan
impressies, klikken en top-queries over de laatste 3 maanden?
Nodig om het risico van de 301 in te schatten.

Antwoord:

---

## D. Wat ik zonder verdere input doe

- Pagina bouwen volgens `CLAUDE.md`, tokens uit `colors_and_type.css`
- `.tedx-video` hernoemen naar `.video-embed` in index.html, CSS en JS, en documenteren in CLAUDE.md
- `VideoObject` schema voor de reel, plus koppeling aan de Person-entiteit via `subjectOf`
- FAQ-blok met speaking-specifieke vragen, voor AEO en GEO
- Bio in drie lengtes schrijven (50, 100 en 250 woorden) op basis van bestaand materiaal, jij keurt goed
- `youtube.com/embed` vervangen door `youtube-nocookie.com/embed`
- Canonical, meta, og:image en sitemap.xml bijwerken
