# Rave Up Records website

Gli articoli si trovano nella cartella [`_posts`](https://github.com/raveup/raveup.github.io/tree/master/_posts).

### Modifica articolo

- Entra nella cartella [`_posts`](https://github.com/raveup/raveup.github.io/tree/master/_posts)
- Clicca sul file da modificare
- Premi il pulsante matita in alto a destra
- Modifica il testo
- Per salvare, premi il pulsante `Commit changes` in basso a sinistra.

### Aggiungi articolo

- Entra nella cartella [`_posts`](https://github.com/raveup/raveup.github.io/tree/master/_posts)
- Premi su `Add file > Create new file` in alto a destra
- Inserisci il nome del file nel formato `YYYY-MM-DD-nome-del-file.md` (ha estensione `.md` Markdown)
- Nel campo `Edit new file` inserisci i **metadati** e il testo dell'articolo
- Per salvare, premi il pulsante `Commit new file` in basso a sinistra.

### Metadati

Ogni articolo deve contenere in cima al file i metadati, preceduti e seguiti da 3 trattini `---`

Esempio:

```yml
---
# Metadati richiesti
layout: post
title: Nome della band
item: Titolo dell'articolo
# Supporto, può essere "lp", "7", "libro" eccetera
support: lp
# La categoria è il codice della label (file "_data/labels.yml")
category: rur
# Numero del volume
volume: 75
# Nome del file immagine senza estensione caricato in "assets/covers/<:: category ::>"
image: file_immagine

# Metadati opzionali
# Tag può essere "new" "few" oppure "soldout"
tag: new
# Aggiunge un testo in home page
focus:
  - title: text
  - description: text
# Aggiunge un video da youtube
youtube: youtube-url
# Aggiunge un video da caricare nella cartella "assets/video"
video: video-filename-senza-estensione
# Aggiunge un audio mp3 da caricare nella cartella "assets/mp3"
mp3: mp3-filename-senza-estensione
# Aggiunge metadati aggiuntivi per esempio tiratura, numero di pagine, etc.
metadata: [ "more", "info" ]
---
```

Il file immagine o copertina `image` va caricato nella cartella della corrispondente `category` (label) all'interno di [`assets/covers`](https://github.com/raveup/raveup.github.io/tree/master/assets/covers).

Ad esempio le copertine "BackStreet" nella cartella `assets/covers/bac` e quelle "Synthetic Shadows" in `assets/covers/ss`.

Consultare il file [`_data/labels.yml`](https://github.com/raveup/raveup.github.io/blob/master/_data/labels.yml) per le abbreviazioni.

### Home page

Ordine di visualizzazione degli articoli:

1. Blog posts (se attivati in [`_data/settings.yml`](https://github.com/raveup/raveup.github.io/blob/master/_data/settings.yml))
2. Articoli con `tag: new` oppure `focus: ...` raggruppati secondo la label (`category`)
3. Articoli con `tag: few` senza raggruppamento per label
4. Articoli rimanenti senza `tag`.

### Cartelle e files

- Le labels (`category` nei metadata) sono nel file [`_data/labels.yml`](https://github.com/raveup/raveup.github.io/blob/master/_data/labels.yml)
- [`_data/menu.yml`](https://github.com/raveup/raveup.github.io/blob/master/_data/menu.yml) contiene il navigation menù
- [`_blog`](https://github.com/raveup/raveup.github.io/tree/master/_blog) contiene i blog posts. Il numero di posts visualizzati è gestito nel file [`_data/settings.yml`](https://github.com/raveup/raveup.github.io/blob/master/_data/settings.yml)

### PayPal docs

- [paypal/JavaScriptButtons](https://github.com/paypal/JavaScriptButtons)
- [Instant Payment Notification (IPN) simulator](https://developer.paypal.com/webapps/developer/applications/ipn_simulator)
