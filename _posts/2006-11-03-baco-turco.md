---
layout: post
title: Ci sarà sempre un baco turco
tags: geek
slug: baco-turco
ref: baco-turco
---
Programmare può sembrare un lavoro molto arido, e in parte lo è. Eppure, ogni tanto dà occasione di fare un po' di filosofia.\
Racconto una storia che riguarda il mio precedente posto di lavoro, sperando che rivelare questi importanti segreti industriali non li spinga a portarmi in tribunale…

Una delle cose che si impara subito programmando è che non è possibile fare il programma perfetto, che funziona correttamente in tutte le condizioni possibili. C'è sempre qualcosa a cui non avevamo pensato, l'unico programma perfetto è un programma che viene continuamente riprogrammato: un software o evolve o è morto. Nel caso migliore deve evolvere per tener dietro ai cambiamenti del contesto in cui opera (inclusi i cambiamenti delle esigenze degli utenti), nel caso peggiore si tratta semplicemente di rendersi conto di errori (*bug* o *bachi*) sottili commessi dagli sviluppatori, errori che manifestano la loro nocività solo con l'uso concreto dell'applicazione.

Un giorno, nella grande multinazionale dove lavoravo prima, qualcuno si accorge che una parte dell'applicazione su cui decine e decine di persone stavano lavorando da lustri, e che aveva ormai raggiunto la settima o l'ottava versione, *non funzionava in **Turchia***. Non voglio dire che funzionasse male, proprio non partiva.

Chi se ne accorge manda un messaggio allarmato nella mailing list interna. Uno che pensava di saperla lunga risponde: *"Figuriamoci, è impossibile, controlla meglio, avrai sbagliato qualcosa"*. Mezz'ora dopo, la stessa persona scrive: *"Ho provato a cambiare la configurazione del computer mettendo come se fossi in Turchia. È vero, non parte!"*. Ma che diamine…?!

Cos'ha di speciale la Turchia?

Passa un'ora, altra email: *"Abbiamo scoperto che nella fase di avvio fallisce un controllo banale sul confronto tra due stringhe, sembra che in Turchia non funzioni bene **toLowerCase()**"*. Il metodo *toLowerCase()*, in Java, come spiega la sua [documentazione](http://java.sun.com/j2se/1.3/docs/api/java/lang/String.html#toLowerCase()), converte del testo nella sua versione in minuscolo. Perché mai non dovrebbe funzionare bene in Turchia? Tanto più che in Turchia si usa l'alfabeto latino, da quando ci furono le riforme modernizzatrici e filo-occidentali di Mustafa Kemal Atatürk.

**Eureka!** Anche se in quell'azienda non contavo un tubo, non ho resistito alla tentazione di mandare un'email in cui spiegavo l'arcano. La Turchia ha eccome qualcosa di speciale: è l'unico Paese al mondo, per quel che ne so, dove la versione minuscola della lettera *I* non è la lettera *i*. Nell'alfabeto turco esistono infatti due lettere molto simili: una è la *I*, senza puntino, che al minuscolo fa *ı*, l'altra è la *İ*, con puntino, che al minuscolo fa *i*.

All'avvio, quel programma applicava su una frase che conteneva una *I* il metodo *toLowerCase*, e la confrontava con una certa stringa costante, che conteneva una *i*. Il confronto in Turchia falliva, perché in Java quel metodo è *localizzato*, cioè realizza la conversione al minuscolo in un modo che dipende dalla lingua e dalle altre "impostazioni regionali" del sistema su cui viene eseguito.

Bisogna stare attenti a mettere i puntini sulle *i*, perché il baco turco è sempre in agguato.