

Gestione della posizione debitoria
==================================

Come previsto dalle Linee guida, tutte le tipologie di pagamento gestite dal Sistema pagoPA prevedono che l’Ente Creditore, per rendere realizzabile
un pagamento, registri nei propri archivi le informazioni necessarie per effettuare il pagamento e le metta a disposizione dell’utilizzatore finale.
Definiamo l’insieme di tali informazioni con il termine di “posizione debitoria”.

Nel Sistema pagoPA ogni pagamento presuppone la creazione propedeutica, nel sistema informativo dell’Ente Creditore, di una posizione debitoria.
All’Ente Creditore compete la gestione degli stati del ciclo di vita della posizione debitoria, che, in linea generale, corrispondono alle attività
di:

1. Creazione. La posizione debitoria viene creata dall’ Ente Creditore e posta nello stato di “Aperta”. Si sottolinea che, al fine della
   semplificazione tecnica del sistema, si definisce “posizione debitoria” sia la creazione che avviene su iniziativa dell’Ente Creditore (es.
   maturazione delle condizioni per il pagamento di una imposta) sia quella che avviene su iniziativa dell’utente (es. richiesta di un servizio),
   anche se in quest’ultimo caso l’utilizzatore finale non è effettivamente in debito con l’Ente Creditore fino a quando non acquista il servizio.

2. Aggiornamento. La posizione debitoria viene aggiornata dell’Ente Creditore ogni qualvolta intervengano eventi che modificano le informazioni
   associate a una posizione debitoria (es sanzioni per decorrenza dei termini). A valle di tale aggiornamento la posizione debitoria riamane in stato
   di aperta, ma l’Ente Creditore gestisce lo storico delle versioni.

3. Blocco. La posizione debitoria viene bloccata, a discrezione dell’Ente Creditore, nelle more del perfezionamento di un pagamento, onde evitare
   pagamenti ripetuti.

4. Trasferimento. La posizione debitoria è posta nello stato di trasferita nel caso in cui la competenza dell’incasso passi a un altro Ente Creditore
   (es. iscrizione in ruolo).

5. Chiusura. L’Ente Creditore pone la posizione debitoria nello stato “Chiusa” ogni qualvolta intervengano eventi che la rendano non più pagabile (es
   saldo del debito). Lo stato è reversibile nel caso in cui intervenga una revoca del pagamento che pone di nuovo la posizione debitoria in una nuova
   versione dello stato di “Aperta”.

Contestualmente alla creazione di una posizione debitoria, l’Ente Creditore, se ne ricorrono le condizioni, deve predisporre un avviso di pagamento,
in almeno una delle seguenti forme:

a) Analogico (sotto forma di avviso cartaceo o file stampabile), da recapitare all’utilizzatore finale o che stampa egli stesso effettuando, se
   previsto, il downloading dal sito web dell’Ente Creditore. Tutti i dettagli relativi all’avviso di pagamento analogico sono inclusi nel documento
   collegato *“Il nuovo avviso di pagamento analogico nel sistema pagoPA”* pubblicata sul sito dell’Agenzia per l’Italia Digitale.

b) Digitale, da inviare al NodSPC per essere recapitato al servizio di *repository* del Prestatore di Servizi di Pagamento scelto dall’utilizzatore
   finale.

L’avviso è lo strumento che rende possibile l’innesco del pagamento presso i Prestatori di Servizi di Pagamento, che l’Ente Creditore genera ogni
qualvolta le norme lo obbligano a notificare a un cittadino o a un’impresa l’insorgenza di una posizione debitoria aperta nei loro confronti. In
questo caso l’Ente creditore genera contestualmente anche un avviso in modalità digitale, che mantiene comunque un carattere bonario.

L’avviso di pagamento analogico, oltre al logotipo del Sistema pagoPA, contiene le informazioni indispensabili per l'esecuzione del pagamento, che
sono dettagliate nella sezione III.

Si attira l’attenzione sulla circostanza che l’importo dell’avviso di pagamento contenuto nell’avviso analogico è quello corrispondente al momento
della produzione di tale documento e quindi può essere soggetto a variazioni (in più o in meno) al momento in cui ne viene richiesto il pagamento da
parte dell’utilizzatore finale, nel caso sia intervenuto un aggiornamento della posizione debitoria, purché tale possibilità sia stata effettivamente
esplicitata in una avvertenza sull’avviso..

La peculiarità di alcune postazioni messe a disposizione dai Prestatori di Servizi di Pagamento rende necessario automatizzare l’acquisizione dei dati
presenti sull’avviso di pagamento. Per questo motivo tale documento è corredato, oltre che dati essenziali sopra citati, anche da un insieme di
elementi grafici facilmente leggibili e decodificabili da apposite apparecchiature.

I processi di creazione, aggiornamento, chiusura o annullamento di una posizione debitoria sono interni al sistema informativo dell’Ente Creditore.
Nei casi previsti tali operazioni scatenano l’invio di un avviso di pagamento con strumenti digitali (avvisatura digitale), il cui processo è
tracciato nel seguito.

Con l’avvisatura digitale l’Ente Creditore permette agli utenti di accedere allo stato corrente della propria posizione debitoria. Attraverso il
Sistema pagoPA è possibile gestire due tipologie di avvisatura digitale:

-  Avvisatura digitale *push*, ovvero su iniziativa dell’Ente Creditore

-  Avvisatura digitale *pull*, ovvero su iniziativa di un Prestatore di Servizi di Pagamento per soddisfare una richiesta dell’utilizzatore finale

I paragrafi che seguono descrivono i *workflow* gestiti da pagoPA nei due casi.

Avvisatura digitale *push* (su iniziativa dell’Ente Creditore)
--------------------------------------------------------------

La funzione di avvisatura digitale in modalità *push* è un servizio messo a disposizione dal Sistema pagoPA attraverso il NodoSPC che consente agli
utilizzatori finali di ricevere avvisi in formato elettronico, in modo che il correlato pagamento possa essere effettuato in modalità semplice e
sicura utilizzando il Sistema pagoPA. Salvo diverso avviso le notifiche digitali hanno un carattere bonario e quindi si affiancano a quelle
tradizionali, già previste dalla normativa, senza sostituirle. Tuttavia, per consentire ai propri clienti la più ampia possibilità di utilizzare tale
strumento innovativo, l’Ente Creditore è incentivato a utilizzarle anche nelle circostanze in cui la normativa non pone un obbligo formale di
notifica.

Per poter ricevere un avviso digitale l'utilizzatore finale dovrà dotarsi di un “cassetto digitale” che il NodoSPC utilizzerà per il recapito,
mediante la sottoscrizione di uno specifico contratto con un soggetto abilitato da AgID a erogare tale servizio. I Prestatori di Servizi di Pagamento
hanno la possibilità di integrare con essa ulteriori funzioni quali, a titolo di esempio, i servizi di pagamento offerti sul Sistema pagoPA, notifiche
sui dispositivi da essi gestiti, (*app* su PC, *tablet* e *smartphone*, servizio di *home* *banking*, ecc.), gestione delle scadenze, ecc.

Si puntualizza che l’utilizzatore finale, ossia il soggetto che riceve l’avvisatura da parte dell’Ente Creditore, è sempre il soggetto debitore
dell’Ente Creditore e che, in quanto l’utilizzatore finale è chiamato a procedere al relativo pagamento che materialmente potrà comunque essere
eseguito da un terzo soggetto (versante) in nome e per conto del debitore (pagatore).

L'adesione al servizio da parte dei Prestatori di Servizi di Pagamento è facoltativa, mentre gli Enti Creditori che generano un avviso analogico
pagabile presso i Prestatori di Servizi di Pagamento dovranno obbligatoriamente sviluppare tale funzionalità.

Il servizio in oggetto è monodirezionale in quanto prevede la distribuzione di avvisi digitali da parte degli Enti Creditori verso gli Utilizzatori
finali, ma non prevede una risposta da parte di questi ultimi.

L'iscrizione al servizio di avvisatura effettuata dall'utilizzatore finale presso il Prestatore di Servizi di Pagamento avrà efficacia per la
ricezione di avvisi da parte di tutti gli Enti Creditori aderenti al Sistema pagoPA.

L'utente finale può iscriversi al servizio di avvisatura presso più Prestatori di Servizi di Pagamento: in questo caso, in fase di iscrizione presso
un altro Prestatore di Servizi di Pagamento dovrà ricevere una segnalazione di iscrizione "multipla" da parte del Prestatore di servizi di pagamento
che sta trattando l'operazione.

La revoca dell’iscrizione al servizio di avvisatura deve essere richiesta al Prestatore di Servizi di Pagamento, che ne stabilisce le modalità.

Nel processo di avvisatura *push* (Figura 4) sono coinvolti quattro soggetti:

-  utilizzatore finale

-  Ente Creditore

-  NodoSPC

-  Prestatore Servizi di Pagamento dell’Utilizzatore finale

|image5|

**Figura 4 – Il processo di gestione dell’avvisatura push**

Il processo di avvisatura *push* è iniziato dall’Ente Creditore quando genera una posizione debitoria (*Task* T1.1.1). Una volta generata la posizione
debitoria, l’Ente Creditore invia al NodoSPC gli avvisi digitali da recapitare (*Task* T1.1.2).

Il NodoSPC (*Task* T1.1.3) esegue azioni differenti a seconda che l’utilizzatore finale sia iscritto o meno al servizio presso un Prestatore Servizi
di Pagamento (*Gateway* G1.1.1):

-  Nel caso in cui l’utilizzatore finale sia iscritto tramite Prestatore Servizi di Pagamento, il NodoSPC invia l’avviso digitale al Prestatore
   Servizi di Pagamento (*Task* T1.1.3) che lo storicizza in un proprio database e ne dà notifica all’Utilizzatore finale (*Task* T1.1.4) in modo che
   sia a disposizione dello stesso (*Task* T1.1.5)

-  Negli altri casi, il NodoSPC non esegue alcuna azione.

Nel caso in cui l’Ente Creditore modifichi uno dei dati obbligatori dell’avviso (ad esempio: l’importo), dovrà inviare al NodoSPC una nuova copia
dell’avviso digitale con l’indicazione che si tratta di un aggiornamento.

Nel caso in cui l’Ente Creditore annulli un avviso digitale o tale avviso risulti pagato con modalità diverse dal Sistema pagoPA, dovrà inviare al
NodoSPC una nuova copia dell’avviso digitale con l’indicazione che si tratta di una cancellazione.

Il processo di aggiornamento e annullamento dell’avviso digitale è analogo a quello della generazione (Figura 5).

Avvisatura digitale *pull* (verifica della posizione debitoria)
---------------------------------------------------------------

L’avvisatura *pull* è una funzionalità messa a disposizione dell'utilizzatore finale che consente allo stesso di accedere alla propria posizione
debitoria.

Il Sistema pagoPA mette a disposizione tale funzione affinché la posizione debitoria di un utilizzatore finale possa essere interrogata attraverso
altre funzioni messe a disposizione dal Prestatori di Servizi di Pagamento presso il quale egli è titolare di un cassetto digitale, purché tale
Prestatore di Servizi di Pagamento risulti aderente all'iniziativa. Tale servizio viene erogato con un’interrogazione della base dati dell’Ente
Creditore di competenza, integrato con il “cassetto digitale”, e avviene secondo uno schema sincrono, attivato dall'utilizzatore finale stesso
attraverso le stesse modalità descritte nel paragrafo precedente.

Nel processo in oggetto (Figura 5) sono coinvolti quattro soggetti:

-  utilizzatore finale

-  Ente Creditore

-  NodoSPC

-  Prestatore Servizi di Pagamento dell’utilizzatore finale

|image6|


.. [1]
    Vedi http://www.indicepa.gov.it/

.. [2]
    Aggiornato con DM 20 marzo 2013, recante "Modifiche all'allegato A del decreto 8 luglio 2005 del Ministro per l'innovazione e le tecnologie,
   recante: «Requisiti tecnici e i diversi livelli per l'accessibilità agli strumenti informatici»" pubblicato in GU Serie Generale n.217 del
   16-9-2013

.. [3]
   In modo da gestire i casi in cui l’invio giornaliero superi la massima numerosità consentita, al momento prevista in 100 mila avvisi digitali.

.. [4]
   Attività da considerarsi solo nel caso di Revoca per Charge-Back

.. [5]
   Attività da considerarsi solo nel caso di Revoca per Charge-Back

.. [6]
   Per i dettagli del Tavolo Operativo si rimanda alla sezione IV.

.. |image0| image:: ..\output/media/image1.png
   :width: 3.93701in
   :height: 0.89306in
.. |image1| image:: ..\output/media/image2.png
   :width: 0.81568in
   :height: 0.4403in
.. |image2| image:: ..\output/media/image3.png
   :width: 3.39472in
   :height: 2.11312in
.. |image3| image:: ..\output/media/image4.png
   :width: 6.43198in
   :height: 0.93413in
.. |image4| image:: ..\output/media/image5.png
   :width: 4.08163in
   :height: 3.56195in
.. |image5| image:: ..\output/media/image6.png
   :width: 4.16697in
   :height: 3.89978in
.. |image6| image:: ..\output/media/image7.png
   :width: 4.37782in
   :height: 3.49935in
.. |image7| image:: ..\output/media/image8.png
   :width: 6.37446in
   :height: 0.87811in
.. |image8| image:: ..\output/media/image11.png
   :width: 11.40069in
   :height: 5.63403in
.. |image9| image:: ..\output/media/image12.png
   :width: 6.63533in
   :height: 0.91405in
.. |image10| image:: ..\output/media/image13.png
   :width: 12.68504in
   :height: 8.54545in
.. |image11| image:: ..\output/media/image14.png
   :width: 5.28056in
   :height: 5.63403in
.. |image12| image:: ..\output/media/image15.png
   :width: 4.95415in
   :height: 4.36631in
.. |image13| image:: ..\output/media/image16.png
   :width: 4.24028in
   :height: 4.04722in
.. |image14| image:: ..\output/media/image17.png
   :width: 5.51181in
   :height: 3.85849in
.. |C:\Users\mogi\AppData\Local\Microsoft\Windows\INetCache\Content.Outlook\2QI8WBLX\deploymentDiagram.png| image:: ..\output/media/image18.png
   :width: 5.36207in
   :height: 4.8097in
.. |C:\Users\mogi\AppData\Local\Microsoft\Windows\INetCache\Content.Outlook\2QI8WBLX\cd_interfacce.png| image:: ..\output/media/image19.png
   :width: 6.69272in
   :height: 2.02431in
.. |image17| image:: ..\output/media/image20.png
   :width: 0.85417in
   :height: 0.23958in
.. |image18| image:: ..\output/media/image20.png
   :width: 0.85417in
   :height: 0.23958in
.. |intro_errori_revoca_storno_riconciliazione| image:: ..\output/media/image21.png
   :width: 5.11181in
   :height: 3.68681in
.. |image20| image:: ..\output/media/image22.png
   :width: 3.17917in
   :height: 8.11181in
.. |image21| image:: ..\output/media/image2.png
   :width: 0.81568in
   :height: 0.4403in
.. |image22| image:: ..\output/media/image23.png
   :width: 5.75in
   :height: 3.125in
.. |image23| image:: ..\output/media/image24.png
   :width: 6.69306in
   :height: 3.02986in
.. |image24| image:: ..\output/media/image25.png
   :width: 5.125in
   :height: 2.65625in
.. |image25| image:: ..\output/media/image26.png
   :width: 2.98958in
   :height: 2.125in
.. |image26| image:: ..\output/media/image27.png
   :width: 3.46528in
   :height: 3.09375in
.. |image27| image:: ..\output/media/image28.png
   :width: 6.69306in
   :height: 2.12986in
.. |image28| image:: ..\output/media/image29.png
   :width: 1.27917in
   :height: 3.46181in
.. |image29| image:: ..\output/media/image30.png
   :width: 6.69306in
   :height: 1.56042in
.. |image30| image:: ..\output/media/image31.png
   :width: 6.69306in
   :height: 1.89868in
.. |C:\Users\mogi\AppData\Local\Microsoft\Windows\INetCache\Content.Outlook\2QI8WBLX\cd_ES.png| image:: ..\output/media/image32.png
   :width: 6.69306in
   :height: 1.69857in
.. |image32| image:: ..\output/media/image33.png
   :width: 6.69306in
   :height: 2.61481in
.. |https://www.plantuml.com/plantuml/img/LOv12eDG34JtEONxN49gwGKyGV2d4eZvaiHLyUxQebXdDJnumxIHvBbC2di6fOZcJOlcWycQ3w0Km1_eQk6ZzkbY8s3X65pcb6g0mIwaWDLb52DzNT8DdV89dtyZw_T4orRsFni0| image:: ..\output/media/image34.png
   :width: 1.54653in
   :height: 1.75in
.. |image34| image:: ..\output/media/image35.png
.. |image35| image:: ..\output/media/image36.png
   :width: 5.4875in
   :height: 5.29221in
.. |image36| image:: ..\output/media/image37.png
.. |SD_PRENOTAZIONE_RIFIUTATA| image:: ..\output/media/image38.png
   :width: 6.6875in
   :height: 3.30208in
.. |image38| image:: ..\output/media/image39.png
   :width: 6.68889in
   :height: 2.4625in
.. |SD_ERR_PAGAMENTO_NON_CONTABILIZZATO| image:: ..\output/media/image40.png
   :width: 6.6875in
   :height: 5.97917in
.. |SD_RT_RIFIUTATA_NODO| image:: ..\output/media/image41.png
   :width: 4.11458in
   :height: 2.25in
.. |sd_RT_RIUTATA_EC| image:: ..\output/media/image42.png
   :width: 5.72917in
   :height: 2.79167in
.. |SD_RT_TIMEOUT_CONTROPARTIpng| image:: ..\output/media/image43.png
   :width: 6.6875in
   :height: 3.95833in
.. |image43| image:: ..\output/media/image44.png
   :width: 6.69306in
   :height: 8.28403in
.. |image44| image:: ..\output/media/image45.png
   :width: 6.19514in
   :height: 9.92153in
.. |image45| image:: ..\output/media/image2.png
   :width: 0.81568in
   :height: 0.4403in
.. |image46| image:: ..\output/media/image46.png
   :width: 6.23958in
   :height: 3.44792in
.. |image47| image:: ..\output/media/image47.png
   :width: 6.69306in
   :height: 4.37917in
.. |image48| image:: ..\output/media/image48.png
   :width: 4.07292in
   :height: 4.47917in
.. |image49| image:: ..\output/media/image49.png
   :width: 6.125in
   :height: 7.71875in
.. |image50| image:: ..\output/media/image2.png
   :width: 0.81568in
   :height: 0.4403in
.. |image51| image:: ..\output/media/image50.png
   :width: 6.69306in
   :height: 1.96875in
.. |image52| image:: ..\output/media/image51.png
   :width: 6.69306in
   :height: 4.79722in
.. |image53| image:: ..\output/media/image52.png
   :width: 6.69306in
   :height: 6.58542in
.. |image54| image:: ..\output/media/image53.png
   :width: 6.69306in
   :height: 2.64722in
.. |image55| image:: ..\output/media/image54.png
   :width: 6.03125in
   :height: 3.25in
.. |image56| image:: ..\output/media/image55.png
   :width: 6.69306in
   :height: 6.47917in
.. |image57| image:: ..\output/media/image56.png
   :width: 5.16667in
   :height: 2.76042in
.. |image58| image:: ..\output/media/image57.png
   :width: 6.25in
   :height: 3.63542in
.. |image59| image:: ..\output/media/image58.png
   :width: 6.69306in
   :height: 5.15556in
.. |info| image:: ..\output/media/image59.png
   :width: 6.67847in
   :height: 2.52153in
.. |C:\Users\mogi\AppData\Local\Microsoft\Windows\INetCache\Content.Outlook\2QI8WBLX\SD_Annullo_Tecnico.png| image:: ..\output/media/image60.png
   :width: 6.69306in
   :height: 3.82492in
.. |C:\Users\mogi\AppData\Local\Microsoft\Windows\INetCache\Content.Outlook\2QI8WBLX\SD_ChargeBack.png| image:: ..\output/media/image61.png
   :width: 6.69306in
   :height: 4.01233in
.. |image63| image:: ..\output/media/image62.png
   :width: 5in
   :height: 2.8125in
.. |image64| image:: ..\output/media/image63.png
   :width: 6.69306in
   :height: 5.31944in
.. |SD_ERR_nodoInviaRichiestaRevoca| image:: ..\output/media/image64.png
   :width: 5.11458in
   :height: 2.46875in
.. |C:\Users\gianni.papetti\AppData\Local\Microsoft\Windows\INetCache\Content.Word\SD_ERR_paaInviaRichiestaRevoca.png| image:: ..\output/media/image65.png
   :width: 5.7381in
   :height: 2.67361in
.. |SD_ERR_nodoInviaRispostaRevoca| image:: ..\output/media/image66.png
   :width: 4.98264in
   :height: 3.13889in
.. |SD_ERR_nodoInviaRispostaRevoca_ERR_PSP| image:: ..\output/media/image67.png
   :width: 5.09583in
   :height: 2.66944in
.. |image69| image:: ..\output/media/image68.png
   :width: 5in
   :height: 2.66667in
.. |SD_ERR_RICHIESTA_STORNO_KO_PSP| image:: ..\output/media/image69.png
   :width: 6.68681in
   :height: 2.77361in
.. |SD_ERR_ESITO_STORNO_KO_NODO| image:: ..\output/media/image70.png
   :width: 5.60903in
   :height: 3.17361in
.. |SD_ERR_ESITO_STORNO_KO_EC| image:: ..\output/media/image71.png
   :width: 6.69583in
   :height: 3.26944in
.. |SD_ERR_ESITO_STORNO_TIMEOUT| image:: ..\output/media/image72.png
   :width: 6.68681in
   :height: 4.94792in
.. |SD_ERR_FLUSSO_KO_NODO| image:: ..\output/media/image73.png
   :width: 6.69583in
   :height: 4.24375in
.. |image75| image:: ..\output/media/image74.png
   :width: 5in
   :height: 2.98958in
.. |SD_ERR_RICHIESTA_FLUSSI_KO| image:: ..\output/media/image75.png
   :width: 5.97361in
   :height: 2.00903in
.. |SD_ERR_RICHIESTA_FLUSSO_KO| image:: ..\output/media/image76.png
   :width: 6.01736in
   :height: 2.32153in
.. |Intro| image:: ..\output/media/image77.png
   :width: 6.68681in
   :height: 3.60903in
.. |nodoChiediCopiaRT| image:: ..\output/media/image78.png
   :width: 4.44375in
   :height: 3.24375in
.. |nodoChiediRPTPendenti| image:: ..\output/media/image79.png
   :width: 6.55625in
   :height: 2.63472in
.. |nodoChiediStatoRPT| image:: ..\output/media/image80.png
   :width: 5.56528in
   :height: 2.94792in
.. |SD_nodoChiediInformativaPSP| image:: ..\output/media/image81.png
   :width: 5.37361in
   :height: 4.30417in
.. |SD_nodoChiediCatalogoServizi| image:: ..\output/media/image82.png
   :width: 4.90417in
   :height: 2.63472in
.. |SD_nodoChiediTemplateInformativaPSP| image:: ..\output/media/image83.png
   :width: 6.43472in
   :height: 3.21736in
.. |SD_nodoChiediInformativaPA| image:: ..\output/media/image84.png
   :width: 5.53889in
   :height: 2.47847in
.. |sd_nodoChiediStatoElaborazioneFlussoRendicontazione| image:: ..\output/media/image85.png
   :width: 6.69583in
   :height: 2.54792in
.. |pspChiediAvanzamentoRPT| image:: ..\output/media/image86.png
   :width: 5.91319in
   :height: 2.98264in
.. |pspChiediAvanzamentoRT| image:: ..\output/media/image87.png
   :width: 5.74792in
   :height: 2.98264in
