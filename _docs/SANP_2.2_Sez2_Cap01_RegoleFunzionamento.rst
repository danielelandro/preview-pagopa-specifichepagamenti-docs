
+--------------------------------------------------+
| SEZIONE II – REGOLE DI FUNZIONAMENTO DEL SISTEMA |
+--------------------------------------------------+

================================================
SEZIONE II – Regole di funzionamento del sistema
================================================

I due diversi *workflow* gestiti sul Sistema pagoPA si differenziano principalmente in base al soggetto che innesca il pagamento. Avremo quindi un
processo diverso se l’utilizzatore finale accede al servizio di pagamento attraverso tecnologie e funzioni messe a disposizione da un Ente Creditore
ovvero attraverso tecnologie e funzioni messe a disposizione da un Prestatore di Servizi di Pagamento

Nella presente sezione è modellato il processo di scambio dati tra i sistemi informativi dei tre soggetti che partecipano a ogni processo di pagamento
mediati dal NodoSPC.

La modellazione risultante descrive quindi, da una parte, le specifiche che definiscono il comportamento progettato del NodoSPC, riportando un set di
informazioni certe e conosciute (le primitive rese disponibili dai Web Services, i dati di configurazione, etc.) e, in un’altra parte, il
comportamento atteso dei sistemi intermediati riportando l’insieme di informazioni minime indispensabili alle funzioni informatiche effettivamente
sviluppate dai soggetti aderenti in qualità di Enti Creditori o Prestatori di Servizi di Pagamento.

I dettagli delle primitive utilizzate in ciascun *workflow*, i tracciati, gli errori e tutte le informazioni tecniche necessarie per integrare servizi
di Enti Creditori e Prestatori di Servizi di Pagamento con il NodoSPC sono descritti nella sezione III.

La modellazione segue le notazioni dello standard *Business Process Model and Notation* (BPMN) versione 2.0, di cui si riporta, in Figura 3, i simboli
utilizzati e il loro significato.

|image4|

**Figura 3 – Notazioni BPMN 2.0 utilizzate**




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
