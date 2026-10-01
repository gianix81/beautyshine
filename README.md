# Beauty Shine — sito web

Sito one-page scroll-driven per **Beauty Shine — Estetica e Benessere**, Arzano (NA).

## File

```
index.html          il sito (CSS e JS inline, nessuna dipendenza)
robots.txt
sitemap.xml
assets/
  master.mp4          video girato nel salone (10 s, 7,7 MB) — scrubbing legato allo scroll
  poster.jpg          primo frame, usato dal preloader e come og:image
  hero-01..03.jpg     i 3 fermo immagine dello scroll, 16:9 (fallback desktop)
  hero-01..03-v.jpg   gli stessi in 9:16, usati su mobile
  scene-01..06.jpg    le 6 zone del salone, usate nella galleria
```

Si pubblica caricando l'intera cartella su un hosting statico (Hostinger, Netlify, Vercel).
Funziona anche aprendo `index.html` in locale.

## DA SOSTITUIRE prima di pubblicare

1. **`TUO-DOMINIO.it`** → il dominio reale. Compare in `index.html`, `privacy.html`,
   `cookie.html`, `robots.txt` e `sitemap.xml`.
   Comando rapido: `sed -i '' 's|TUO-DOMINIO.it|iltuodominio.it|g' index.html privacy.html cookie.html robots.txt sitemap.xml`
2. **`DA COMPILARE`** → i dati legali. Compaiono evidenziati in giallo nel footer di tutte
   le pagine e dentro `privacy.html` / `cookie.html`. Servono:
   - denominazione o ragione sociale del titolare del trattamento;
   - P.IVA / codice fiscale (va messa anche come `"vatID"` nel JSON-LD di `index.html`);
   - un indirizzo e-mail per le richieste privacy (artt. 15–22 GDPR).
   Finché restano i segnaposto il sito **non è a norma**: vanno sostituiti prima di pubblicare.
   Comando rapido, una volta noti i dati:
   `sed -i '' 's|<span class="da-compilare">DA COMPILARE</span>|Ragione Sociale|g' privacy.html cookie.html index.html`
   (meglio farlo campo per campo: i tre segnaposto hanno contenuti diversi).
3. **Coordinate GPS** — nel JSON-LD ci sono le coordinate approssimative di Arzano
   (40.9086, 14.2637). Per la SEO locale conviene mettere quelle esatte del salone
   (le trovi su Google Maps col tasto destro sul punto).

## Privacy e GDPR

- `privacy.html` — informativa artt. 13–14 GDPR, da far verificare a un consulente.
- `cookie.html` — cookie policy secondo le linee guida del Garante del 10/06/2021.
- **Il sito non installa cookie** e non usa local storage: per questo non c'è il banner,
  che il Garante non richiede quando non ci sono cookie da autorizzare.
- I **font sono ospitati in `assets/fonts/`**, non su Google Fonts: nessuna chiamata a
  server terzi al caricamento delle pagine (evita il problema del trasferimento dell'IP).
- La **mappa Google è spenta** e si carica solo premendo «Carica la mappa»: finché non
  si clicca, Google non riceve nulla.
- **Attenzione:** se in futuro si aggiunge Google Analytics, il pixel di Meta o qualsiasi
  strumento di tracciamento, diventa obbligatorio un banner cookie con consenso preventivo
  e va aggiornata `cookie.html`.

## Immagini

Lo scroll usa il **video girato nel salone** (10 s): la titolare davanti alla parete teal
con l'insegna, poi il passaggio ai prodotti. Le foto della galleria vengono dai **video
ufficiali TikTok** del centro — reception, Nails Space, pedicure, make-up, cabina laser,
area relax — con sottotitoli e watermark rimossi. Nessuna immagine è inventata.

Se in futuro avete foto professionali del salone, basta sostituire i file mantenendo
nomi e proporzioni: `scene-0X.jpg` in 16:9 e `scene-0X-v.jpg` in 9:16.

## Palette del sito

Presa dai video, non inventata: bianco panna `#F7F4EF`, oro champagne `#C9A961`,
teal `#0F6B78` (le pareti del salone), con smeraldo, ocra e il magenta dell'area
massaggi come accenti. I pannelli e le card riprendono la forma ad **arco** delle
nicchie retroilluminate. Il simbolo **ginkgo** del logo compare nel marchio in alto.

## Da fare per farsi trovare su Google

1. **Aprire la scheda Google Business** — è la cosa che pesa di più per un centro
   estetico locale, più del sito stesso. Beauty Shine oggi non ce l'ha.
   Attenzione: su Maps esiste già "Shine" in Via Sanremo 22 — è **un'altra attività**,
   non rivendicarla.
2. **Google Search Console**: aggiungere la proprietà, inviare `sitemap.xml`,
   chiedere l'indicizzazione della home.
3. Mettere il link del sito nella bio Instagram e TikTok.
4. Nome-indirizzo-telefono identici ovunque (sito, Google, Instagram, TikTok, directory).

Indicizzazione: 2-7 giorni. Posizionamento locale: 3-6 settimane.

## Dati usati nel sito

- Indirizzo: Via Palmiro Togliatti 21/23, angolo Via Sanremo — 80022 Arzano (NA)
- Telefono: 331 859 8620 (prenotazioni solo telefoniche o in salone)
- Orari: martedì–sabato 9:30–20:00
- Servizi: onicotecnica, semipermanente e nail art, epilazione laser, laminazione
  ciglia e sopracciglia, trucco sposa e cerimonia, make-up, trattamenti viso,
  candle massage, criolipolisi
- Instagram: @beautyshine_esteticaebenessere — TikTok: @beautyshine__

Fonti: bio e post Instagram/TikTok del profilo. Gli orari vengono dal post di
apertura del nuovo salone (maggio 2025): **da confermare**.

Nessuna recensione è stata inserita nel sito perché non ce ne sono di verificate
riferite a Beauty Shine.
