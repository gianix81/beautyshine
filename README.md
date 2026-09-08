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

1. **`TUO-DOMINIO.it`** → il dominio reale. Compare 7 volte in `index.html`
   (canonical, og:url, og:image, JSON-LD) e in `robots.txt` / `sitemap.xml`.
   Comando rapido: `sed -i '' 's|TUO-DOMINIO.it|iltuodominio.it|g' index.html robots.txt sitemap.xml`
2. **P.IVA** — non inserita perché non disponibile. Va aggiunta nel footer e come
   `"vatID"` nel blocco JSON-LD (obbligo di legge per un sito aziendale).
3. **Email** — non inserita. Se ne avete una, aggiungerla nei contatti e in `"email"` nel JSON-LD.
4. **Coordinate GPS** — nel JSON-LD ci sono le coordinate approssimative di Arzano
   (40.9086, 14.2637). Per la SEO locale conviene mettere quelle esatte del salone
   (le trovi su Google Maps col tasto destro sul punto).
5. **Privacy policy / Cookie** — il sito carica Google Fonts e la mappa Google:
   serve una pagina privacy e, se aggiungete analytics, un banner cookie.

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
- Telefono/WhatsApp: 331 859 8620
- Orari: martedì–sabato 9:30–20:00
- Servizi: onicotecnica, semipermanente e nail art, epilazione laser, laminazione
  ciglia e sopracciglia, trucco sposa e cerimonia, make-up, trattamenti viso,
  candle massage, criolipolisi
- Instagram: @beautyshine_esteticaebenessere — TikTok: @beautyshine__

Fonti: bio e post Instagram/TikTok del profilo. Gli orari vengono dal post di
apertura del nuovo salone (maggio 2025): **da confermare**.

Nessuna recensione è stata inserita nel sito perché non ce ne sono di verificate
riferite a Beauty Shine.
