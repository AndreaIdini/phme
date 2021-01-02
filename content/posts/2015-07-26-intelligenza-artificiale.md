---
title: Le Intelligenze Artificiali
author: Andrea Idini
type: post
date: 2015-07-26T19:54:52+00:00
url: /blog/2015/07/26/intelligenza-artificiale/
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
  - Proprietà Emergenti
  - Società

---
L'intelligenza artificiale è uno dei più affascinanti argomenti messi in campo in questo periodo storico. Pochi quesiti toccano tante competenze e aspetti della cultura e società come la domanda "Può una macchina pensare?".

> "Se un computer possa pensare è una faccenda non più interessante di quella riguardante se un sottomarino possa nuotare" - E. W. Dijkstra

<!--more-->

  
Da un lato l'intelligenza artificiale è uno dei cosidetti "argomenti di confine" fra filosofia e scienza (citando Artigas quegli argomenti che permettono un ponte in quanto contatto bidirezionale fra le discipline): inquadrandosi nel generale inquadramento dell'antico problema filosofico "mente-cervello", lo studio e lo sviluppo della sua declinazione informatica ne permette studi e contaminazioni sotto diversi aspetti delle scienze dure, dalla teoria dell'informazione all'algoritmica, purgando le complicazioni neurologiche insite in uno studio _in vivo_.  
Dall'altro le conseguenze sociali della sempre maggiore indipendenza delle macchine, che si riflette attualmente in una forte crisi lavorativa del terziario a livello globale, già ora pongono quesiti politici sempre più pressanti e diversi scenari futuribili si profilano all'orizzonte.

Sarebbe assurdo se si parlasse di automobili senza sapere che esse hanno le ruote e funzionano con carburante, eppure si parla di I.A. considerando i possibili approcci e algoritmi come materia da tecnici che nulla hanno che vedere con le possibili implicazioni. Si discute della sua fattibilità filosofica o conseguenze sociologiche senza che sia ben chiaro da dove un eventuale _"io sintetico"_ possa praticamente derivare seguendo quali approcci, e le loro differenze e i limiti.

Fare un completo resoconto delle ricerche in atto nel campo è al di fuori dello scopo e dimensione di qualunque blogpost. Non esiste un approccio univoco e consolidato e data l'importanza dell'argomento le ricerche si espandono e moltiplicano proporzionalmente agli enormi fondi e numero di ricercatori coinvolti. Personalmente credo che le dozzine di diversi approcci, molti dei quali ibridi, siano divisibili in quattro diverse categorie di cui è importante apprezzare le differenze prima di poter imbastire una discussione a riguardo.

  1. Simulativo, o di neuroscienza computazionale
  2. Simbolico, o logico-cognitivo
  3. Statistico
  4. Fondamentale

L'approccio di **neuroscienza computazionale** cerca di simulare il cervello e la fisiologia di un organismo a livello fisico-chimico. Esattamente come altri sistemi fisici possono essere modellizzati computazionalmente, con le dovute approssimazioni, lo stesso può valere per la simulzione di un organismo biologico e di sue parti. La riproduzione dell'intero spettro di comportamenti di un organismo è lo scopo possibile con questo tipo di progetto: gli altri approcci creano qualcosa di unico che non ha corrispondente nel mondo biologico, mentre una simulazione, procedendo in modo analogico con la realtà, ha la possibilità di riprodurla e quindi di chiarire differenze specifiche fra un organismo e l'altro. I progressi sono garantiti [dalla legge di Moore][1] e la progressione della capacità computazionale, che permette sempre più sofisticate simulazioni di sistemi più complessi. E sulla strada per una "perfetta" simulazione, (ancora lontana dall'orizzonte per i mammiferi e uomo in particolare, dato che le simulazioni del più semplice organismo dotato di cervello, il verme _C. Elegans_, [di cui una opensource][2] non riescono ancora a riprodurre l'intero spettro di comportamenti di cui _C. Elegans_ è capace) molte cose si possono apprendere, come ad esempio dal [controverso][3] [Human Brain Project][4] europeo da 1 miliardo di euro sono state recentemente scoperte [sconosciuti sistemi di gestione dell'energia][5] all'interno del cervello umano.

Il **sistema simbolico** cerca di sviluppare sistemi astratti di elaborazione dell'informazione costruendo algoritmi con un linguaggio adeguato. Ovvero partendo dalle definizioni della logica che il sistema userà e fornendo regole per le relazioni fra enti in input (la parte cognitiva) è possibile programmare strutture elaborative automatiche che assolvono a diversi scopi. Ad esempio un sistema di cui vengono fornite regole del calcolo e opportune regole logiche quantitative potrà eseguire calcolo simbolico. Un sistema programmato con una logica più flessibile (ad esempio modale o paraconsistente) sarà un buon sistema per l'interpretazione del linguaggio. Nell'investigare possibili definizioni sintetiche di intelligenza [e' possibile riscontrare comportamenti spontaneanei][6], ovvero non preventivamente impostati ne' prevedibili, [soluzioni autonome di indovinelli][7] come "[test di autocoscienza][8]" inclusi.

**L'approccio statistico** è quello più utilizzato attualmente per sviluppare algoritmi flessibili operativi. Prendendo sistemi biologici e logici a ispirazione si costruiscono algoritmi adattativi, che cioè abbiano dei criteri fondamentali per stabilire se un'azione si muove nella direzione desiderata e che poi costruiscano una rete di relazioni fra le azioni, definita rete neurale, in modo autonomo o solo parzialmente assistito. Esplorino insomma la causalità dello spazio in cui si trovano ad operare, in funzione di un obiettivo. Un ottimo esempio, sufficientemente semplice per essere seguito e compreso, con relativa spiegazione, è come [questo algoritmo "impari" a giocare a Super Mario][9] dopo poche modifiche. Come si nota nel video, inizialmente la rete neurale non sa di dover schiacciare il pulsante destro, e rimane fermo. Modifiche casuali della rete neurale implicano che l'algoritmo schiacci il tasto destro (e solo quello) fino alla sua morte ma questo già comporta che questa specifica rete neurale viene selezionata, poichè schiacciare il tasto destro fa progredire nel livello più che stare fermi o saltare sul posto. Modifiche successive fanno realizzare che è necessario saltare in certe condizioni per schivare i nemici o evitare di cadere, finchè la rete neurale non diventa sufficientemente sofisticata da finire il livello. Reti neurali più sofisticate, come [DeepMind realizzata dai ricercatori Google][9] sono sufficientemente flessibili da poter efficacemente giocare a una serie di 49 giochi classici, senza che il programmatore insegni alcuna strategia, ma lasciandola imparare da se lasciando il computer "allenarsi", premiando esclusivamente il punteggio. Ovviamente le applicazioni delle reti neurali e, più in generale, dell'approccio statistico all'I.A. non si limitano alla teoria dei giochi. Al contrario sono le tipologie di algoritmi più versatili e utilizzati, che letteralmente ci circondano e migliorano la nostra vita. Riconoscimento, interpretazione e traduzione linguistica e vocale (da [Google Translate][10] a Siri), dalle alle [auto a guida autonoma][11] ai filtri per lo spam.

Un approccio ibrido fra quello _statistico_ e quello _simbolico_ ottiene i risultati più interessanti, in termini applicativi, come Wolfram Language (Mathematica e [Wolfram Alpha][12]) ed il versatilissimo assistente professionale [Watson di IBM][13] che sta avendo successo [sia come medico][14] che [come chef][15].

In ultima analisi è anche possibile ripensare la costruzione di una intelligenza artificiale in modo **costruttivista,** cioè basandosi sulla configurazione fisica delle strutture che danno origine ad intelligenza e coscienza. Questo metodo spesso cerca di trascendere i limiti imposti da transistor ed elettronica digitale, costituzionalmente inscindibile da una logica binaria e difficilmente impletabile in modo _consistentemente retroazionato. _Ovvero le approssimazione pratiche necessarie alla scrittura delle metodologie _simboliche_ e _simulative_, non permetterebbero progressi sostanziali, e quindi l'intero hardware di una intelligenza artificiale dovrebbe essere costruito per funzionare in modo altamente connesso e non limitato alla rappresentazione binaria dell'era digitale e la sua relativa programmazione.

_"Può una macchina pensare"_, quindi?  
La risposta, a questo punto, dovrebbe essere ovvia: _"Quale macchina?"_

 [1]: http://www.phme.it/blog/2015/03/13/apple-watch-nuovo-macbook-e-la-legge-di-moore/
 [2]: http://www.openworm.org/
 [3]: http://www.nature.com/news/human-brain-project-votes-for-leadership-change-1.17060
 [4]: https://www.humanbrainproject.eu/
 [5]: http://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1004036
 [6]: http://www.ted.com/talks/alex_wissner_gross_a_new_equation_for_intelligence?embed=true&language=es
 [7]: https://www.youtube.com/watch?v=MceJYhVD_xY
 [8]: http://kryten.mm.rpi.edu/SBringsjord_etal_self-con_robots_kg4_0601151615NY.pdf
 [9]: https://www.youtube.com/watch?v=qv6UVOQ0F44
 [10]: https://translate.google.it/
 [11]: https://www.youtube.com/watch?v=nlMjSWnvglU
 [12]: https://www.wolframalpha.com/
 [13]: https://www.youtube.com/watch?v=_Xcmh1LQB9I
 [14]: http://www.businessinsider.com/ibms-watson-may-soon-be-the-best-doctor-in-the-world-2014-4?IR=T
 [15]: https://www.ibmchefwatson.com/