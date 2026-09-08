# Come pubblicare su GitHub + Vercel

Il sito è statico: nessuna build, nessuna dipendenza. Vercel lo serve così com'è.

## 1. Repo GitHub

Dalla cartella `beautyshine`:

```bash
git init
git add .
git commit -m "Sito Beauty Shine Arzano"
git branch -M main
git remote add origin https://github.com/TUO-UTENTE/beautyshine.git
git push -u origin main
```

**Fai il repo privato** se non vuoi che il materiale del centro sia pubblico.
Il `.gitignore` esclude già `brand/frames-estetista/` (i fermo immagine del volto
della titolare): non servono al sito e su un repo pubblico sarebbero indicizzabili.
Se li vuoi comunque nel repo, togli quella riga.

## 2. Vercel

1. vercel.com → **Add New… → Project** → importa il repo
2. Framework Preset: **Other** — lascia vuoti Build Command e Output Directory
   (il sito è alla radice del repo)
3. Deploy

Esce un URL tipo `beautyshine.vercel.app`, online in meno di un minuto.

`vercel.json` è già incluso: mette cache lunga sugli asset (video e foto non cambiano)
e nessuna cache su `index.html`, così ogni modifica va online subito.

## 3. Dominio

In Vercel: **Settings → Domains → Add**. Poi dal pannello del registrar
(Aruba, Register, GoDaddy…) punta i DNS come indicato da Vercel.

Appena il dominio è attivo, sostituisci il segnaposto ovunque:

```bash
sed -i '' 's|TUO-DOMINIO.it|iltuodominio.it|g' index.html robots.txt sitemap.xml
```

(su Linux: `sed -i` senza `''`). Compare 7 volte in `index.html` — canonical,
Open Graph e JSON-LD — più robots e sitemap.

## 4. Dopo il deploy

- Google Search Console: aggiungi la proprietà, invia `sitemap.xml`, chiedi l'indicizzazione
- Apri la scheda Google Business del centro e mettici l'URL
- Link in bio su Instagram e TikTok

## Nota sul video

`assets/master.mp4` pesa 10 MB. È sotto il limite dei 100 MB per file di GitHub,
quindi non serve Git LFS. Su Vercel viene servito da CDN con la cache di `vercel.json`.
