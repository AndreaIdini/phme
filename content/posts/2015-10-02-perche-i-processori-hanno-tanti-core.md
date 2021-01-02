---
title: Perchè i processori hanno tanti core
author: Andrea Idini
type: post
date: 2015-10-02T16:40:00+00:00
url: /blog/2015/10/02/perche-i-processori-hanno-tanti-core/
nkweb_code_in_head:
  - default
nkweb_Use_Custom_js:
  - default
nkweb_Use_Custom_Values:
  - default
nkweb_Use_Custom:
  - 'false'
categories:
  - Ph.ysics
tags:
  - Informatica
  - Tecnologia

---
<figure id="attachment_2020" aria-describedby="caption-attachment-2020" style="width: 300px" class="wp-caption alignleft"><a href="/wp-content/uploads/2015/10/insideintel.jpg" rel="lightbox[2019]"><img class="wp-image-2020 size-medium" src="/wp-content/uploads/2015/10/insideintel-300x150.jpg" alt="lo spaccato di un moderno processore" width="300" height="150" srcset="http://www.phme.it/wp-content/uploads/2015/10/insideintel-300x150.jpg 300w, http://www.phme.it/wp-content/uploads/2015/10/insideintel.jpg 570w" sizes="(max-width: 300px) 100vw, 300px" /></a><figcaption id="caption-attachment-2020" class="wp-caption-text">lo spaccato di un moderno processore, in cui si nota la memoria (cache), il processore grafico, e i 4 core.</figcaption></figure> 

Una volta erano una stravaganza riservata a supercomputer, poi hanno sempre più preso piede anche fra i processori più comuni, oggigiorno praticamente ogni sistema più potente di una calcolatrice tascabile frutta la potenza di calcolo di più core.

Perfino il **Chromecast**, che è una piccola chiavetta da 35€ da attaccare alla televisione per ricevere contenuti in streaming, è dotata di un **processore 1.2GHz doppio core**, e una scheda grafica con diversi core paralleli.

Ma perchè questa molteplicità di core si è diffusa così tanto?

<!--more-->

Innanzitutto le definizioni: **ogni sistema informatico**, dal più potente supercomputer ad un forno programmabile, **ha il suo fulcro di funzionamento nei processori**. Un processore è un sistema dedicato a **svolgere calcoli di diverso tipo**, tendenzialmente azioni su bit memorizzati che corrispondono ad elaborazioni aritmetiche. Una scheda grafica è molto simile in concetto, ma sono ottimizzati per svolgere specifiche operazioni, che solitamente corrispondono ad elaborazioni video, molto velocemente.

Il sebbene oggigiorno il confine fra processore e scheda grafica sia diventato un po' labile, integrando i due sistemi (e altri, come sensori di movimento e gestione reti cellulari) in un unico pacchetto chiamato "System on Chip", e permettendo alla scheda grafica di "alleggerire" o "accelerare" il carico sul processore, la differenza di intenti rimane molto marcata.

**Il core è un'unità di processamento**, di cui sono dotati sia processori che schede grafiche, ma nel caso di quest'ultime la parallelizzazione è molto più spinta (fino ad arrivare a migliaia per una singola scheda grafica).

Quando noi chiediamo a un sistema informatico di eseguire un'operazione semplice, il sistema attiverà un "processo" che verrà indirizzato in un core che lo esegui e svolga l'operazione. Gli Hz (o meglio, dato il momento, i GHz) di un processore sono "i cicli" che il processore è in grado di eseguire in un secondo: 1GHz è 1 miliardo di cicli al secondo. Un "ciclo" è un'operazione semplice (ad esempio il cambio di un bit, che corrisponde a una somma). Però non significa direttamente che i processori con più GHz siano necessariamente più veloci: potranno eseguire più cicli al secondo, ma sono tante le variabili da tenere in considerazione. In quanto tempo l'informazione viaggia dalla memoria, al processore, e la complicazione dell'operazione che il core riesce ad eseguire in un singolo ciclo sono oggi i margini di maggiore miglioramento che slegano quasi assolutamente il clock dalla velocità: esistono processori per portatili piuttosto veloci con 1.4GHz e processori da cellulare piuttosto lenti con più di 2GHz (è anche il motivo per cui i processori amd costano poco, nonostante gli alti clock).

**Il motivo principale che ha portato alla diffusione dei multicore, è che a parità di numero di elaborazioni consuma molto meno suddividere il carico su tanti core, piuttosto che alzare la frequenza.**

Il consumo di un processore incrementa (almeno) quadraticamente con la frequenza, ma (teoricamente) linearmente con il numero di core.

Ovvero, per fare un discorso illustrativo e didattico, se prendo un processore single core 2GHz e voglio raddoppiare il numero di elaborazioni al secondo, e' possibile adempiere letteralmente letteralmente alla richiesta, raddoppiando la frequenza a 4GHz, oppure raddoppiare il core tenendo fissa la frequenza a 2GHz.

Raddoppiando la frequenza a 4GHz, il consumo aumenta a (più del) quadruplo (quadruplo nel caso di transistor ideale, nella pratica è molto peggio, almeno cubico), se raddoppio i core a 2GHz consuma doppio dato che, semplificando molto, si tratta di costruire un gemello e affiancarlo (in linea teorica perfino un filo meno, perché è possibile riutilizzare la mappa delle istruzioni).

Inizialmente, **per i primi processori commerciali, il limite non era di potenza erogata, era il costo stesso del transistor** e i limiti tecnologici di frequenza a limitarne la velocita'. Un 8086 (primo modello di CPU Intel per il mercato consumer) [consumava 1.8 Watt][1], perché fisicamente era difficile uscire dai limiti operativi in frequenza indipendentemente dalla potenza a disposizione. Mano a mano che i transistor sono diventati sempre più puri ed economici, **seguendo la [Legge di Moore][2], la potenza sia computazionale che elettrica dei processori ha continuato a incrementare esponenzialmente**, finchè in pochi anni [si superarono i 100W per i processori Pentium 4 superiori a 3GHz nel 2003][3]. Dal 2000 in poi la densità energetica di un processore era più alta di quella di una piastra da cucina, e continuando per quel passo [avrebbero superato la densità energetica di un reattore nucleare][4] prima del 2010!

Dato che mantenere la divisione in transistor non è possibile se il silicio si fonde, era impossibile incrementare la potenza dei processori con il banale incremento della frequenza oltre i 3.6GHz, e questo è il motivo per cui circa 10 anni fa si e' iniziati a migrare su sistemi multicore.

Inizialmente era un core virtuale: il furbo meccanismo Hyper Threading di Intel riesce a sfruttare i tempi morti fra un'operazione e l'altra per infilare un'altra operazione. L'Hyper Threading (HT) è ancora utilizzato nei processori di fascia più alta (generalmente Intel i7, con qualche eccezione). Poco dopo la generazione Pentium D ha introdotto i processori a doppio core, ed il resto è storia.

**Oggi i processori più comuni sono ben sotto i 100W** (per Desktop vanno dai 60 ai 80W, per Portatile dai 4.5 ai 45W, e per smartphone da circa 1.5 a 3W, e includono anche schede video!) e sono migliaia di volte più potenti di quei Pentium 4, e dimunendo i consumi (molto importanti per i portatili e i cellulari) e la temperatura di esercizio si garantisce una maggiore affidabilità.

Lo scotto da pagare è che **non tutto è (né può essere) parallelizzato alla perfezione**. Un "algoritmo", che è un procedimento fatto di istruzioni matematiche, può ad esempio essere ricorsivo, e richiedere come input, l'output di un calcolo precedente, iterandolo. Ad esempio consideriamo un algoritmo sciocco che "conti" sommando 1 tantissime volte. 0+1=1, 1+1=2, 2+1=3. In tal caso la parallelizzazione è impossibile.

Quindi **le performance di punta del singolo core, rimangono molto importanti**. Per ovviare a questa esigenza e per tenere il più possibile sotto controllo i consumi, le temperature e l'affidabilità, oggi le frequenze sono dinamiche: un processore ha diversi step, e nello stato a minimo consumo puo' far andare i core a 0.3GHz e "infilare il Turbo" (sì, si chiama Turbo :P) a 3GHz e oltre, gestendo in modo indipendente i diversi core consumando molto molto meno in situazioni statiche ma senza sacrificare le prestazioni massime. Difatti l'introduzione di nuovi step "verso il basso" è il vero motivo per cui i portatili molto moderni (per Intel dalla serie Haswell del 2013 in poi, indicata con numeri oltre il 4000) hanno durata di batteria di 8 ore e oltre. Se fossero stressati al massimo, avrebbero una durata delle solite 2/3 ore, ma dato che comunemente l'uso di un portatile è ben al di sotto della sua potenzialità massima il processore sta sempre dormicchiando e dendicandoci una frazione del suo potenziale, consumando quindi proporzionalmente poco.

&nbsp;

 [1]: http://www.cpu-world.com/CPUs/8086/Intel-D8086-2.html
 [2]: http://www.phme.it/blog/2015/03/13/apple-watch-nuovo-macbook-e-la-legge-di-moore/
 [3]: https://en.wikipedia.org/wiki/List_of_CPU_power_dissipation_figures#Pentium_4
 [4]: http://image.slidesharecdn.com/green-computing-bhagalpur-150730165430-lva1-app6892/95/green-commputing-paradigm-shift-in-computing-technology-ict-its-applications-socioeconomic-and-environmental-perspective-11-638.jpg?cb=1438310262