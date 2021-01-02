---
title: Il supercalcolo universitario (e la ricerca su macchine altrui)
author: Andrea Idini
type: post
date: 2016-03-31T23:30:50+00:00
url: /blog/2016/03/31/il-supercalcolo-universitario-e-la-ricerca-su-macchine-altrui/
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
  - Università

---
<figure id="attachment_2333" aria-describedby="caption-attachment-2333" style="width: 300px" class="wp-caption alignleft"><a href="/wp-content/uploads/2016/03/1024px-IBM_Blue_Gene_P_supercomputer.jpg" rel="lightbox[2298]"><img class="size-medium wp-image-2333" src="/wp-content/uploads/2016/03/1024px-IBM_Blue_Gene_P_supercomputer-300x199.jpg" alt="IBM Blue Gene Computer ad Argonne - fonte wikimedia" width="300" height="199" srcset="http://www.phme.it/wp-content/uploads/2016/03/1024px-IBM_Blue_Gene_P_supercomputer-300x199.jpg 300w, http://www.phme.it/wp-content/uploads/2016/03/1024px-IBM_Blue_Gene_P_supercomputer.jpg 1024w" sizes="(max-width: 300px) 100vw, 300px" /></a><figcaption id="caption-attachment-2333" class="wp-caption-text">IBM Blue Gene Computer ad Argonne - <a href="https://upload.wikimedia.org/wikipedia/commons/thumb/d/d3/IBM_Blue_Gene_P_supercomputer.jpg/1024px-IBM_Blue_Gene_P_supercomputer.jpg" rel="lightbox[2298]">fonte wikimedia</a></figcaption></figure> 

Da una domanda di _Gabriele Soranzo._

Il mondo informatico si [evolve rapidamente][1] per i consumatori. Ma nonostante questo determini prodotti sempre nuovi e con funzionalità differenti sugli scaffali dei negozi, non rende automaticamente obsoleto l'utilizzo tradizionale di sistemi di calcolo massivo. Al contrario il _"supercalcolo"_ svolto in sistemi appositamente costruiti per l'elaborazione di grandi dati [è sempre più usato][2] per le esigenze della ricerca e industria moderna.<!--more-->

Le istanze di calcolo [estremamente parallelizzate][3] che utilizzano migliaia di processori per giorni sono necessarie per simulare il [nucleo atomico][4] o [algoritmi di reti neurali][5], quindi parte fondamentale della vita di ricerca è l'utilizzo di tali macchine, e di converso la richiesta di accesso e usufrutto.

Il mondo del calcolo è tanto vario quanto è possibile immaginarlo, vengono utilizzati da cellulari a suddette macchine di supercalcolo, e di conseguenza una certa richiesta di potenza può venire soddisfatta sia da privati cittadini che mettono a disposizione i propri computer e smartphones (visitate [Boinc][6] per contribuire!), che industrie (ad esempio [amazon][7]), che centri statali e universitari appositamente dedicati al _supercalcolo_ (in Italia specialmente il [cineca][8]).

Limitandoci ai supercalcolatori, quando un ricercatore necessita di grande quantità di potenza, deve solitamente farne richiesta presso i centri affiliati alla sua università. Molti ricercatori hanno del denaro assegnato alla ricerca vinto attraverso bandi o assegnato con il contratto. Tuttavia questo fondo è solitamente destinato per comprare rivelatori e materiale di ricerca, e viaggi per collaborazioni e conferenze. Date le ristrette dei finanziamenti alla ricerca il mondo accademico vede con diffidenza l'acquisto di materiale che il sistema universitario (e affiliazioni) stesso può fornire.

Quindi sebbene in linea di principio i fondi di ricerca siano sufficienti per acquistare buone potenze di calcolo (i fondi di ricerca tipicamente variano tipicamente da poche migliaia a un milione di euro anno per una singola iniziativa scientifica/gruppo), non si riesce a fornire una giustificazione sufficiente per farlo in molte legislazioni (io non conosco nessuno che sia riuscito a farsela autorizzare).

Normalmente quindi si procede a scrivere un _Proposal,_ che è una richiesta ad un ente che è proprietaria di certe macchine particolari (siano esse [acceleratori di particelle][9] o [supercomputer][2]), per potere utilizzare una certa risorsa motivata da un obiettivo scientifico. Ad esempio è possibile presentare una richiesta per avere potenza di calcolo per uno studio teorico oppure giorni di acceleratore di particelle per uno studio sperimentale.

A quel punto una commissione vaglierà la richiesta e stabilirà _quanto_ e _come _essa verrà soddisfatta. Tipiche richieste variano da qualche giorno a qualche settimana di fascio di particelle, oppure da centinaia di migliaia a miliardi di ore di CPU.

A quel punto, nel caso di laboratori come per gli acceleratori di particelle, saranno stabilite le date a disposizione, e il gruppo viaggerà per eseguire l'esperimento al laboratorio prescelto, dividendosi i turni e spesso portando alcuni dei propri strumenti. Invece nel caso di centri calcolo le risorse sono spendibili comodamente collegandosi in remoto da casa (e rovinando l'immagine del cervellone di turno che corre verso il supercomputer con la chiavetta in mano), ma devono essere spese tutte entro una scadenza, solitamente annuale ma a volte più breve.

Il ricercatore avrà quindi realizzato un programma, e utilizzerà il suo monte ore per simulare un evento fisico. A seconda delle sue necessità di calcolo avrà chiesto risorse adeguate, tuttavia non è così tanto semplice. Infatti un algoritmo andrà [parallelizzato][3] efficientemente, per disporre delle grandi risorse.

Un supercomputer è un sistema di diversi computer, detti _nodi_, ognuno dei quali contenenti molti processori, quindi un po' più potente del desktop o laptop che avete a casa che verosimilmente contiene un singolo processore (anche se con [molti core][3]).<figure id="attachment_2334" aria-describedby="caption-attachment-2334" style="width: 300px" class="wp-caption alignright">

<a href="/wp-content/uploads/2016/03/12-950iap10.jpg" rel="lightbox[2298]"><img class="wp-image-2334 size-medium" src="/wp-content/uploads/2016/03/12-950iap10-300x255.jpg" alt="In questa figura uno schema semplificato. Un compito viene suddiviso fra 4 istanze MPI e ognuna di queste viene suddivisa in 3 thread openMP." width="300" height="255" srcset="http://www.phme.it/wp-content/uploads/2016/03/12-950iap10-300x255.jpg 300w, http://www.phme.it/wp-content/uploads/2016/03/12-950iap10.jpg 320w" sizes="(max-width: 300px) 100vw, 300px" /></a><figcaption id="caption-attachment-2334" class="wp-caption-text">In questa figura uno schema semplificato: un compito viene suddiviso fra 4 istanze MPI (ad esempio i processori all'interno di un _nodo_) e ognuna di queste viene suddivisa in 3 thread (ovvero il carico fra i vari core di un singolo processore) openMP.</figcaption></figure> 

Quando si esegue un programma _"massivamente parallelo",_ esso funziona su diversi nodi per volta ognuno dei quali dotato (solitamente) 4 processori (ed eventualmente acceleratori grafici). Le comunicazioni si fanno molto intricate: la comunicazione all'interno dello stesso core è più veloce che fra due core dello stesso processore che è più veloce che fra due processori dello stesso nodo che è più veloce che fra due nodi diversi. Di conseguenza la progettazione di un algoritmo che efficientemente scali su grandi parallelizzazioni, con diversi gradini di velocità e complicazione, non è sempre banale né fattibile.<figure id="attachment_2335" aria-describedby="caption-attachment-2335" style="width: 300px" class="wp-caption alignleft">

<a href="/wp-content/uploads/2016/03/image_preview.jpg" rel="lightbox[2298]"><img class="size-medium wp-image-2335" src="/wp-content/uploads/2016/03/image_preview-300x300.jpg" alt="Simulazione di collasso di supernova" width="300" height="300" srcset="http://www.phme.it/wp-content/uploads/2016/03/image_preview-300x300.jpg 300w, http://www.phme.it/wp-content/uploads/2016/03/image_preview-150x150.jpg 150w, http://www.phme.it/wp-content/uploads/2016/03/image_preview.jpg 336w" sizes="(max-width: 300px) 100vw, 300px" /></a><figcaption id="caption-attachment-2335" class="wp-caption-text">[Simulazione di collasso di supernova del gruppo di Monaco][10]</figcaption></figure> 

Le citate _ore _che il ricercatore ottiene sono le ore per ogni singolo processo (core). Ad esempio si può fare richiesta scrivendo un progetto (che porta via qualche giorno di lavoro a qualche persona), si ottengono 5 milioni di ore sul cluster [Dirac Complexity][11] che possono essere usate come 2 mila 500 ore su 128 nodi (circa metà di tutto il centro).

Il risultato può essere una simulazione spettacolare come [questa][10], oppure qualcosa di molto meno spettacolare ma altrettanto interessante scientificamente come le tante che spesso descrivo da queste parti!

 [1]: http://www.phme.it/blog/2015/03/13/apple-watch-nuovo-macbook-e-la-legge-di-moore/
 [2]: http://www.phme.it/blog/2010/11/20/la-nuova-guerra-fredda-from-tons-to-flops/
 [3]: http://www.phme.it/blog/2015/10/02/perche-i-processori-hanno-tanti-core/
 [4]: http://www.phme.it/blog/2015/09/25/phringe-limportanza-di-fare-scale-in-fisica-nucleare/
 [5]: http://www.phme.it/blog/2015/07/26/intelligenza-artificiale/
 [6]: https://boinc.berkeley.edu/
 [7]: http://aws.amazon.com
 [8]: http://www.cineca.it/it/content/supercalcolo
 [9]: http://www.phme.it/blog/2010/02/04/perche-usiamo-gli-acceleratori/
 [10]: https://www.youtube.com/watch?v=2RxIwtxdEnQ
 [11]: http://www2.le.ac.uk/offices/itservices/ithelp/services/hpc/dirac/architecture