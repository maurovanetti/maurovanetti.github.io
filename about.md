---
layout: page
shortcut: "?"
title: "Che cos'è questo sito?"
permalink: /about.html
---

Mauro Vanetti, Pavia, 29/9/1979.

Questo è il mio sgabuzzino. Non è un blog e non è molto interattivo, è un contenitore di roba che ho fatto, che mi riguarda e che mi interessa fatta con lo scopo di conservarla. Non è possibile avere un sito veramente eterno (sulle illusioni di eternità dei formati digitali suggerisco [questo stranissimo saggio seminarrativo](https://www.wumingfoundation.com/giap/2012/09/futuro-anteriore/) che ho contribuito a scrivere parecchi anni fa), ma mi ci vorrei avvicinare un filo di più. Sarebbe già molto avere tutto il materiale in un formato abbastanza comodo, fuori da uno specifico data base, e ben replicato e versionato.

Per questo motivo dopo 16 anni durante i quali ho usato [Drupal](https://drupal.org/), ho deciso che mi serve un sito statico, abbastanza duraturo, semplicissimo. Vorrei che il sito non rischiasse continuamente di rompersi e non richiedesse aggiornamenti per continuare a funzionare anche in mancanza di nuovi contenuti. Sarebbe poi molto meglio evitare ogni pericolo di hacking.

L'ho quindi rifatto tutto usando [Jekyll](https://jekyllrb.com/), un generatore di siti statici. Ha anche il vantaggio di permettermi di fare un sito un po' più "con le mie forze" senza essere inchiodati sempre alle convenzioni e alle idiosincrasie dei vari WordPress, Joomla, Drupal ecc. La struttura e i contenuti del sito vengono modificati su uno dei miei computer e le modifiche salvate in [un repository Git](https://github.com/maurovanetti/maurovanetti.github.io). Quando le modifiche vengono spinte sul cloud (GitHub) il sito viene automaticamente aggiornato sia su [GitHub Pages](https://maurovanetti.github.io/) sia finalmente [sul mio sito vero e proprio](https://maurovanetti.info/) attraverso dei [servizi di integrazione continua](https://github.com/maurovanetti/maurovanetti.github.io/actions/workflows/pages.yml) forniti da GitHub. Utilizzare un sistema di versionamento come Git significa tenere traccia di tutte le modifiche fatte sia ai contenuti sia al codice. Per come funziona Jekyll, i contenuti non sono salvati su un data base ma su dei file testuali.

I vecchi articoli e anche i commenti più interessanti del [vecchio sito](https://web.archive.org/web/20220512142813/http://maurovanetti.info/) sono stati migrati o lo saranno presto. Qualche contenuto potrebbe essere cambiato leggermente, ma è in buona sostanza lo stesso.

## Una nota sui commenti

Ho meditato a lungo su come permettere ai visitatori di lasciare dei commenti. Sul vecchio sito in [Drupal](https://drupal.org/) era possibile perché ovviamente venivano salvati nel DB, essendo un CMS per generare siti dinamici. Ma questo nuovo sgabuzzino è un sito statico basato su [Jekyll](https://jekyllrb.com/) quindi non si può "aggiungere" qualcosa dinamicamente. Ci sono servizi che esternalizzano la gestione dei commenti, come il banale Disqus e l'interessante ed elegante [Talkyard](https://talkyard.io/). Dopo averli sperimentati, ho optato per una decisione più drastica: **non voglio nessun sistema automatico per aggiungere commenti**.

Questo non significa che non si possono lasciare dei commenti: basta mandarmi un'email a [posta@maurovanetti.info](mailto:posta@maurovanetti.info) indicando l'articolo nell'oggetto dell'email. Mi occuperò io di pubblicare il commento ed eventualmente di rispondere, facendolo entrare a far parte integrante del sito.

Vantaggi:
- Moderazione perfetta
- Antispam perfetto
- Pulizia del risultato
- Caricamento velocissimo del sito
- Coerenza estetica e stilistica
- Maggiore riflessione nella scrittura dei commenti
- Andare controcorrente

I social esistono già, coi loro pregi e i loro moltissimi difetti. Voglio provare a fare una piccola cosa un po' diversa.