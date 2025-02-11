# Password Generator

Questo progetto fornisce un semplice generatore di password casuali utilizzando HTML, jQuery e JavaScript.

## Funzionalità
- Generazione di una password casuale di 12 caratteri
- Include lettere maiuscole, minuscole, numeri e simboli speciali
- Interfaccia utente minimale con un pulsante per generare la password

## Tecnologie utilizzate
- **HTML** per la struttura
- **CSS** per lo stile (può essere aggiunto separatamente)
- **jQuery** per la gestione degli eventi e la manipolazione del DOM
- **JavaScript** per la generazione della password casuale

## Installazione e utilizzo
1. Scarica o clona il repository.
2. Apri il file `index.html` in un browser.
3. Clicca sul pulsante "Generate" per generare una nuova password casuale.

## Codice sorgente
```html
<div class="pass-gen" id="pass-gen">
    <a href="#" class="button" id="refresh">Generate</a>
    <span class="container" id="Container"></span>
</div>

<script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
<script>
  $(document).ready(function() {
    function randomStrings(length) {
        var strResult = "0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz!@#$%^&*()_-+=`~,.[]:|";
        return Array.from({ length }, () => strResult[Math.floor(Math.random() * strResult.length)]).join('');
    }

    $("#refresh").click(function() {
        $("#Container").html(randomStrings(12));      
        $(".container").show();
        return false;
    });
  });
</script>
```

## Contributi
Sentiti libero di proporre miglioramenti aprendo una pull request o segnalando problemi tramite issue.

## Licenza
Questo progetto è rilasciato sotto la licenza MIT.
