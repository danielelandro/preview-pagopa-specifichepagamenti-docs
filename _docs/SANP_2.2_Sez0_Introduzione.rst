+----------+
| |image0| |
+----------+

+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| **Specifiche Attuative del Nodo dei Pagamenti-SPC**                                                                                                 |
|                                                                                                                                                     |
|    *Allegato B alle "Linee guida per l'effettuazione dei pagamenti elettronici a favore delle pubbliche amministrazioni e dei gestori di pubblici   |
|    servizi"*                                                                                                                                        |
|                                                                                                                                                     |
| **Versione** **2.2-** **gennaio 2019**                                                                                                              |
+-----------------------------------------------------------------------------------------------------------------------------------------------------+

Indice dei contenuti

`Indice dei contenuti 2 <#_Toc534291592>`__

`Definizioni e Acronimi 12 <#definizioni-e-acronimi>`__

`Introduzione alla versione 2.2 16 <#introduzione-alla-versione-2.2>`__

`SEZIONE I – FUNZIONAMENTO GENERALE DEL SISTEMA 18 <#_Toc311040588>`__

`1.1 Il ciclo di vita del pagamento gestito sul Sistema pagoPA 20 <#il-ciclo-di-vita-del-pagamento-gestito-sul-sistema-pagopa>`__

`1.2 L’adesione al Sistema pagoPA 21 <#ladesione-al-sistema-pagopa>`__

`1.3 Governance del sistema 22 <#governance-del-sistema>`__

`1.4 Gli oggetti scambiati 22 <#gli-oggetti-scambiati>`__

`1.5 Obblighi degli Enti Creditori 23 <#obblighi-degli-enti-creditori>`__

`1.6 Trasparenza nei confronti degli utilizzatori finali 24 <#trasparenza-nei-confronti-degli-utilizzatori-finali>`__

`1.7 Funzioni accessorie di controllo 24 <#funzioni-accessorie-di-controllo>`__

`1.8 Sicurezza e conservazione 25 <#sicurezza-e-conservazione>`__

`1.9 Software Development KIT per applicazioni “mobile” 25 <#software-development-kit-per-applicazioni-mobile>`__

`SEZIONE II – REGOLE DI FUNZIONAMENTO DEL SISTEMA 26 <#_Toc311040648>`__

`2. Gestione della posizione debitoria 27 <#gestione-della-posizione-debitoria>`__

`2.1 Avvisatura digitale push (su iniziativa dell’Ente Creditore) 28 <#avvisatura-digitale-push-su-iniziativa-dellente-creditore>`__

`2.2 Avvisatura digitale pull (verifica della posizione debitoria) 30 <#avvisatura-digitale-pull-verifica-della-posizione-debitoria>`__

`3. Il Processo di pagamento attivato presso l’Ente Creditore 32 <#il-processo-di-pagamento-attivato-presso-lente-creditore>`__

`4. Processo di pagamento attivato presso il Prestatore di Servizi di Pagamento 37 <#_Toc535250101>`__

`4.1 Avvio del pagamento 40 <#avvio-del-pagamento>`__

`4.2 Generazione posizione debitoria 40 <#generazione-posizione-debitoria>`__

`4.3 Verifica posizione debitoria e attivazione richiesta di pagamento telematica
40 <#verifica-posizione-debitoria-e-attivazione-richiesta-di-pagamento-telematica>`__

`4.4 Trasmissione dati di accredito e rendicontazione 41 <#trasmissione-dati-di-accredito-e-rendicontazione>`__

`4.5 Attivazione della richiesta di pagamento 42 <#attivazione-della-richiesta-di-pagamento>`__

`5. Funzioni accessorie 43 <#funzioni-accessorie>`__

`5.1 Revoca della Ricevuta Telematica 43 <#revoca-della-ricevuta-telematica>`__

`5.2 Annullo tecnico 44 <#annullo-tecnico>`__

`5.3 Storno del pagamento 45 <#storno-del-pagamento>`__

`5.4 Attestazione del pagamento 46 <#attestazione-del-pagamento>`__

`5.5 Riconciliazione dei pagamenti 47 <#riconciliazione-dei-pagamenti>`__

`5.6 Altre funzioni accessorie 48 <#altre-funzioni-accessorie>`__

`6. componenti tecniche del NodoSPC 49 <#componenti-tecniche-del-nodospc>`__

`6.1 Gestore del Workflow Applicativo 50 <#_Toc535250115>`__

`6.2 Gestore della Connessione 50 <#gestore-della-connessione>`__

`6.3 Gestore della Porta di Dominio 50 <#gestore-della-porta-di-dominio>`__

`6.4 Interfaccia di Canale 51 <#interfaccia-di-canale>`__

`6.5 Repository ricevute telematiche 51 <#repository-ricevute-telematiche>`__

`6.6 Componente Web-FESP 51 <#componente-web-fesp>`__

`6.7 Componente WISP 52 <#componente-wisp>`__

`6.8 Componente Wrapper MyBank 52 <#componente-wrapper-mybank>`__

`6.9 Componente per la gestione dell'avvisatura digitale in modalità push 52 <#componente-per-la-gestione-dellavvisatura-digitale-in-modalità-push>`__

`6.10 File Transfer sicuro 52 <#file-transfer-sicuro>`__

`6.11 Giornale degli Eventi 53 <#giornale-degli-eventi>`__

`6.12 Componenti di utilità 53 <#componenti-di-utilità>`__

`6.13 Sistema di monitoring 53 <#sistema-di-monitoring>`__

`6.14 Sistema di Gestione del Tavolo Operativo 54 <#sistema-di-gestione-del-tavolo-operativo>`__

`6.15 Controlli 54 <#controlli>`__

`6.16 Servizi applicativi opzionali 54 <#servizi-applicativi-opzionali>`__

`6.16.1 Totali di traffico 54 <#totali-di-traffico>`__

`SEZIONE III – SPECIFICHE TECNICHE 55 <#_Toc534291641>`__

`7. Introduzione 55 <#introduzione>`__

`7.1 Interfacce/Protocolli 57 <#interfacceprotocolli>`__

`7.2 Architettura Funzionale 57 <#architettura-funzionale>`__

`7.3 Stato del Pagamento 60 <#stato-del-pagamento>`__

`8. Modello dei dati 69 <#modello-dei-dati>`__

`8.1 Avvisatura digitale 69 <#avvisatura-digitale>`__

`8.1.1 Avviso digitale 69 <#avviso-digitale>`__

`8.1.2 Esito Inoltro Avvisatura 71 <#esito-inoltro-avvisatura>`__

`8.1.3 Iscrizione al servizio 71 <#iscrizione-al-servizio>`__

`8.2 Pagamenti 72 <#pagamenti>`__

`8.2.1 Richiesta di Pagamento Telematica (RPT) 74 <#richiesta-di-pagamento-telematica-rpt>`__

`8.2.2 Richiesta di acquisto Marca da Bollo Digitale 76 <#richiesta-di-acquisto-marca-da-bollo-digitale>`__

`8.2.3 Ricevuta Telematica (RT) 76 <#ricevuta-telematica-rt>`__

`8.2.4 Richiesta di revoca (RR) 77 <#richiesta-di-revoca-rr>`__

`8.2.5 Esito Della Revoca (ER) 78 <#esito-della-revoca-er>`__

`8.2.6 Flusso di rendicontazione (FR) 79 <#flusso-di-rendicontazione-fr>`__

`8.3 Giornale degli eventi 80 <#giornale-degli-eventi-1>`__

`8.4 Messaggi di errore 82 <#messaggi-di-errore>`__

`8.5 Configurazione 86 <#configurazione>`__

`8.5.1 Ente Creditore 86 <#ente-creditore>`__

`8.5.2 PSP 87 <#psp>`__

`9. Pagamento presso l’Ente Creditore 91 <#pagamento-presso-lente-creditore>`__

`9.1 Attori e casi d’uso 91 <#attori-e-casi-duso>`__

`9.2 Pagamento online con guida interattiva di selezione del PSP (WISP) 91 <#pagamento-online-con-guida-interattiva-di-selezione-del-psp-wisp>`__

`9.3 Prenotazione Rifiutata 96 <#prenotazione-rifiutata>`__

`9.4 Gestione degli errori 97 <#gestione-degli-errori>`__

`10. Pagamento presso il PSP 104 <#pagamento-presso-il-psp>`__

`10.1 Attori e casi d’uso 104 <#attori-e-casi-duso-1>`__

`10.2 Pagamento mediante Avviso (scenario principale) 105 <#pagamento-mediante-avviso-scenario-principale>`__

`10.3 Pagamento mediante Avviso (scenario alternativo) DEPRECATO 108 <#pagamento-mediante-avviso-scenario-alternativo-deprecato>`__

`10.4 Pagamento spontaneo 113 <#pagamento-spontaneo>`__

`10.5 Gestione degli errori 114 <#gestione-degli-errori-1>`__

`11. Avvisatura 122 <#avvisatura>`__

`11.1 Scenari e casi d’uso 122 <#scenari-e-casi-duso>`__

`11.2 Iscrizione avvisatura 122 <#iscrizione-avvisatura>`__

`11.3 Invio sincrono avviso digitale 123 <#invio-sincrono-avviso-digitale>`__

`11.4 Invio massivo avvisi digitali 125 <#invio-massivo-avvisi-digitali>`__

`11.5 Avvisatura pull 127 <#avvisatura-pull>`__

`11.6 Gestione degli errori 129 <#gestione-degli-errori-2>`__

`12. Back-office 136 <#back-office>`__

`12.1 Revoca e storno 136 <#revoca-e-storno>`__

`12.1.1 Processo di Revoca per Annullo Tecnico 137 <#processo-di-revoca-per-annullo-tecnico>`__

`12.1.2 Processo di Revoca di una Ricevuta Telematica per charge-back 139 <#processo-di-revoca-di-una-ricevuta-telematica-per-charge-back>`__

`12.1.3 Processo di Storno di un pagamento 141 <#processo-di-storno-di-un-pagamento>`__

`12.2 Riconciliazione 142 <#riconciliazione>`__

`12.2.1 Attori del processo di Riconciliazione Contabile e casi d’uso 142 <#attori-del-processo-di-riconciliazione-contabile-e-casi-duso>`__

`12.2.2 Worflow di Riconciliazione 142 <#worflow-di-riconciliazione>`__

`12.3 Gestione degli errori 145 <#gestione-degli-errori-3>`__

`12.3.1 Gestione degli errori di revoca 145 <#gestione-degli-errori-di-revoca>`__

`12.3.2 Gestione degli errori di storno 150 <#gestione-degli-errori-di-storno>`__

`12.3.3 Gestione degli errori di riconciliazione 156 <#gestione-degli-errori-di-riconciliazione>`__

`13. Ausiliarie 163 <#ausiliarie>`__

`13.1 Scenari, casi d’uso e attori 163 <#scenari-casi-duso-e-attori>`__

`13.1.1 Funzioni Ausiliarie per L’Ente Creditore 164 <#funzioni-ausiliarie-per-lente-creditore>`__

`13.1.2 Funzioni ausiliarie per il PSP 169 <#funzioni-ausiliarie-per-il-psp>`__

`13.1.3 Funzioni Ausiliarie per il NodoSPC 172 <#funzioni-ausiliarie-per-il-nodospc>`__

`Sezione IV – Processo di adesione ed Esercizio 175 <#_Toc355876994>`__

`14. Adesione al sistema pagoPA 175 <#adesione-al-sistema-pagopa>`__

`14.1 Adesione di un Ente Creditore. 176 <#adesione-di-un-ente-creditore.>`__

`14.2 Adesione di un Prestatore di Servizi di Pagamento 176 <#adesione-di-un-prestatore-di-servizi-di-pagamento>`__

`14.3 Intermediari e Partner tecnologici nel sistema pagoPA 177 <#intermediari-e-partner-tecnologici-nel-sistema-pagopa>`__

`15. Attivazione sul sistema pagoPA 177 <#attivazione-sul-sistema-pagopa>`__

`16. Attivazione di un EC direttamente connesso 178 <#attivazione-di-un-ec-direttamente-connesso>`__

`16.1 Processo di avvio in Esercizio 179 <#processo-di-avvio-in-esercizio>`__

`17. Attivazione di un EC intermediato 181 <#attivazione-di-un-ec-intermediato>`__

`17.1 Attivazione di un EC con un Intermediario Tecnologico 181 <#attivazione-di-un-ec-con-un-intermediario-tecnologico>`__

`17.2 Attivazione di un EC con un Partner Tecnologico 181 <#attivazione-di-un-ec-con-un-partner-tecnologico>`__

`17.2.1 Attivazione di Ente Creditore “pilota” 182 <#attivazione-di-ente-creditore-pilota>`__

`17.2.2 Attivazione di Ente Creditore “non pilota” 182 <#attivazione-di-ente-creditore-non-pilota>`__

`18. Attivazione di un PSP sul sistema pagoPA 182 <#attivazione-di-un-psp-sul-sistema-pagopa>`__

`18.1 Attivazione di un PSP che si collega direttamente al Nodo 183 <#attivazione-di-un-psp-che-si-collega-direttamente-al-nodo>`__

`18.2 Attivazione di un PSP che svolge il ruolo di Acquirer 184 <#attivazione-di-un-psp-che-svolge-il-ruolo-di-acquirer>`__

`18.3 Attivazione di un PSP che offre il servizio MyBank 184 <#attivazione-di-un-psp-che-offre-il-servizio-mybank>`__

`18.3.1 PSP che intendono svolgere il ruolo di Banca Buyer 184 <#psp-che-intendono-svolgere-il-ruolo-di-banca-buyer>`__

`18.3.2 PSP che intendono svolgere il ruolo di Banca Seller 184 <#psp-che-intendono-svolgere-il-ruolo-di-banca-seller>`__

`18.4 Attivazione di un PSP che offre il servizio CBILL 185 <#attivazione-di-un-psp-che-offre-il-servizio-cbill>`__

`18.5 Attivazione di un PSP intermediato 185 <#attivazione-di-un-psp-intermediato>`__

`19. Adempimenti durante l’erogazione del servizio 185 <#adempimenti-durante-lerogazione-del-servizio>`__

`19.1 Adempimenti dei soggetti direttamente collegati al Nodo-SPC 185 <#adempimenti-dei-soggetti-direttamente-collegati-al-nodo-spc>`__

`19.1.1 Tavoli operativi 186 <#tavoli-operativi>`__

`19.1.2 Monitoraggio e controllo 186 <#monitoraggio-e-controllo>`__

`19.1.3 Business continuity e Disaster Recovery 186 <#business-continuity-e-disaster-recovery>`__

`19.1.4 Archiviazione dei dati 186 <#archiviazione-dei-dati>`__

`19.1.5 Ulteriori adempimenti 186 <#ulteriori-adempimenti>`__

`19.2 Adempimenti dei soggetti non direttamente collegati al Nodo-SPC 187 <#adempimenti-dei-soggetti-non-direttamente-collegati-al-nodo-spc>`__

`20. Utilizzo del marchio pagoPA 188 <#utilizzo-del-marchio-pagopa>`__

`21. Disponibilità dei Servizi 189 <#disponibilità-dei-servizi>`__

`21.1 Nodo-SPC 189 <#nodo-spc>`__

`21.2 Enti Creditori 189 <#enti-creditori>`__

`21.3 Prestatori di servizi di pagamento aderenti 189 <#prestatori-di-servizi-di-pagamento-aderenti>`__

`22. Livelli di Servizio 189 <#livelli-di-servizio>`__

`22.1 Indicatori di qualità del Nodo-SPC 189 <#indicatori-di-qualità-del-nodo-spc>`__

`23. Responsabilità dei soggetti aderenti 189 <#responsabilità-dei-soggetti-aderenti>`__

`23.1 Responsabilità dell’Ente Creditore 190 <#responsabilità-dellente-creditore>`__

`23.2 Responsabilità del Prestatore di Servizi di Pagamento 190 <#responsabilità-del-prestatore-di-servizi-di-pagamento>`__

`APPENDICE I – APPROFONDIMENTI (ENTI CREDITORI) 191 <#_Toc534291745>`__

`Integrità e non ripudiabilità della Ricevuta Telematica 191 <#integrità-e-non-ripudiabilità-della-ricevuta-telematica>`__

`Acquisto della marca da bollo digitale 191 <#acquisto-della-marca-da-bollo-digitale>`__

`APPENDICE II – APPROFONDIMENTI (PRESTATORI DI SERVIZI DI PAGAMENTO) 192 <#_Toc534291748>`__

`Il servizio MyBank 192 <#il-servizio-mybank>`__

`Indice dei contenuti 1 <#_Toc534291592>`__

`Definizioni e Acronimi 1 <#definizioni-e-acronimi>`__

`Introduzione alla versione 3.0 1 <#introduzione-alla-versione-2.2>`__

`SEZIONE I – FUNZIONAMENTO GENERALE DEL SISTEMA 1 <#_Toc311040588>`__

`1.1 Il ciclo di vita del pagamento gestito sul Sistema pagoPA 1 <#il-ciclo-di-vita-del-pagamento-gestito-sul-sistema-pagopa>`__

`1.2 L’adesione al Sistema pagoPA 1 <#ladesione-al-sistema-pagopa>`__

`1.3 Governance del sistema 1 <#governance-del-sistema>`__

`1.4 Gli oggetti scambiati 1 <#gli-oggetti-scambiati>`__

`1.5 Obblighi degli Enti Creditori 1 <#obblighi-degli-enti-creditori>`__

`1.6 Trasparenza nei confronti degli utilizzatori finali 1 <#trasparenza-nei-confronti-degli-utilizzatori-finali>`__

`1.7 Funzioni accessorie di controllo 1 <#funzioni-accessorie-di-controllo>`__

`1.8 Sicurezza e conservazione 1 <#sicurezza-e-conservazione>`__

`1.9 Software Development KIT per applicazioni “mobile” 1 <#software-development-kit-per-applicazioni-mobile>`__

`SEZIONE II – REGOLE DI FUNZIONAMENTO DEL SISTEMA 1 <#_Toc311040648>`__

`2. Gestione della posizione debitoria 1 <#gestione-della-posizione-debitoria>`__

`2.1 Avvisatura digitale push (su iniziativa dell’Ente Creditore) 1 <#avvisatura-digitale-push-su-iniziativa-dellente-creditore>`__

`2.2 Avvisatura digitale pull (verifica della posizione debitoria) 1 <#avvisatura-digitale-pull-verifica-della-posizione-debitoria>`__

`3. Il Processo di pagamento attivato presso l’Ente Creditore 1 <#il-processo-di-pagamento-attivato-presso-lente-creditore>`__

`4. Processo di pagamento attivato presso il Prestatore di Servizi di Pagamento 1 <#_Toc534291610>`__

`4.1 Avvio del pagamento 1 <#avvio-del-pagamento>`__

`4.2 Generazione posizione debitoria 1 <#generazione-posizione-debitoria>`__

`4.3 Verifica posizione debitoria e attivazione richiesta di pagamento telematica
1 <#verifica-posizione-debitoria-e-attivazione-richiesta-di-pagamento-telematica>`__

`4.4 Trasmissione dati di accredito e rendicontazione 1 <#trasmissione-dati-di-accredito-e-rendicontazione>`__

`4.5 Attivazione della richiesta di pagamento 1 <#attivazione-della-richiesta-di-pagamento>`__

`5. Funzioni accessorie 1 <#funzioni-accessorie>`__

`5.1 Revoca della Ricevuta Telematica 1 <#revoca-della-ricevuta-telematica>`__

`5.2 Annullo tecnico 1 <#annullo-tecnico>`__

`5.3 Storno del pagamento 1 <#storno-del-pagamento>`__

`5.4 Attestazione del pagamento 1 <#attestazione-del-pagamento>`__

`5.5 Riconciliazione dei pagamenti 1 <#riconciliazione-dei-pagamenti>`__

`5.6 Altre funzioni accessorie 1 <#altre-funzioni-accessorie>`__

`6. componenti tecniche del NodoSPC 1 <#componenti-tecniche-del-nodospc>`__

`6.1 Gestore del Workflow Applicativo 1 <#_Toc534291624>`__

`6.2 Gestore della Connessione 1 <#gestore-della-connessione>`__

`6.3 Gestore della Porta di Dominio 1 <#gestore-della-porta-di-dominio>`__

`6.4 Interfaccia di Canale 1 <#interfaccia-di-canale>`__

`6.5 Repository ricevute telematiche 1 <#repository-ricevute-telematiche>`__

`6.6 Componente Web-FESP 1 <#componente-web-fesp>`__

`6.7 Componente WISP 1 <#componente-wisp>`__

`6.8 Componente Wrapper MyBank 1 <#componente-wrapper-mybank>`__

`6.9 Componente per la gestione dell'avvisatura digitale in modalità push 1 <#componente-per-la-gestione-dellavvisatura-digitale-in-modalità-push>`__

`6.10 File Transfer sicuro 1 <#file-transfer-sicuro>`__

`6.11 Giornale degli Eventi 1 <#giornale-degli-eventi>`__

`6.12 Componenti di utilità 1 <#componenti-di-utilità>`__

`6.13 Sistema di monitoring 1 <#sistema-di-monitoring>`__

`6.14 Sistema di Gestione del Tavolo Operativo 1 <#sistema-di-gestione-del-tavolo-operativo>`__

`6.15 Controlli 1 <#controlli>`__

`6.16 Servizi applicativi opzionali 1 <#servizi-applicativi-opzionali>`__

`6.16.1 Totali di traffico 1 <#totali-di-traffico>`__

`SEZIONE III – SPECIFICHE TECNICHE 1 <#_Toc534291641>`__

`7. Introduzione 1 <#introduzione>`__

`7.1 Interfacce/Protocolli 1 <#interfacceprotocolli>`__

`7.2 Architettura Funzionale 1 <#architettura-funzionale>`__

`7.3 Stato del Pagamento 1 <#stato-del-pagamento>`__

`8. Modello dei dati 1 <#modello-dei-dati>`__

`8.1 Avvisatura digitale 1 <#avvisatura-digitale>`__

`8.1.1 Avviso digitale 1 <#avviso-digitale>`__

`8.1.2 Esito Inoltro Avvisatura 1 <#esito-inoltro-avvisatura>`__

`8.1.3 Iscrizione al servizio 1 <#iscrizione-al-servizio>`__

`8.2 Pagamenti 1 <#pagamenti>`__

`8.2.1 Richiesta di Pagamento Telematica 1 <#richiesta-di-pagamento-telematica-rpt>`__

`8.2.2 Marca da Bollo Digitale 1 <#richiesta-di-acquisto-marca-da-bollo-digitale>`__

`8.2.3 Ricevuta Telematica (RT) 1 <#ricevuta-telematica-rt>`__

`8.2.4 Richiesta di revoca (RR) 1 <#richiesta-di-revoca-rr>`__

`8.2.5 Esito Della Revoca (ER) 1 <#esito-della-revoca-er>`__

`8.2.6 Flusso di rendicontazione (FR) 1 <#flusso-di-rendicontazione-fr>`__

`8.3 Giornale degli eventi 1 <#giornale-degli-eventi-1>`__

`8.4 Messaggi di errore 1 <#messaggi-di-errore>`__

`8.5 Configurazione 1 <#_Toc534291660>`__

`8.5.1 Ente Creditore 1 <#ente-creditore>`__

`8.5.2 PSP 1 <#psp>`__

`8.5.3 Pubblicazione 1 <#_Toc534291663>`__

`8.5.4 Canale 1 <#canale>`__

`8.5.5 Servizio 1 <#servizio>`__

`8.5.6 Informazioni dettaglio Servizio 1 <#informazioni-dettaglio-servizio>`__

`8.5.7 Plugin 1 <#plugin>`__

`8.5.8 Costi 1 <#costi>`__

`8.5.9 Acquirer 1 <#acquirer>`__

`9. Pagamento presso l’Ente Creditore 1 <#pagamento-presso-lente-creditore>`__

`9.1.1 Attori e casi d’uso 1 <#attori-e-casi-duso>`__

`9.1.2 Pagamento online con guida interattiva di selezione del PSP (WISP) 1 <#pagamento-online-con-guida-interattiva-di-selezione-del-psp-wisp>`__

`9.1.2.1 Caso Marca da bollo digitale 1 <#caso-acquisto-marca-da-bollo-digitale>`__

`9.1.2.2 Caso autorizzazione gestita dal PSP 1 <#_Toc534291674>`__

`9.1.3 Gestione degli errori 1 <#gestione-degli-errori>`__

`10. Pagamento presso il PSP 1 <#_Toc534291676>`__

`10.1.1 Attori e casi d’uso 1 <#_Toc534291677>`__

`10.1.2 Pagamento mediante Avviso (scenario principale): 1 <#_Toc534291678>`__

`10.1.3 Pagamento PSP con avviso di pagamento alternativo 1 <#_Toc534291679>`__

`10.1.4 Pagamento spontaneo 1 <#_Toc534291680>`__

`10.1.5 Gestione degli errori 1 <#_Toc534291681>`__

`11. Avvisatura 1 <#pagamento-presso-il-psp>`__

`11.1.1 Scenari e casi d’uso 1 <#scenari-e-casi-duso>`__

`11.1.2 Iscrizione avvisatura 1 <#iscrizione-avvisatura>`__

`11.1.3 Invio sincrono avviso digitale 1 <#invio-sincrono-avviso-digitale>`__

`11.1.4 Invio massivo avvisi digitali 1 <#invio-massivo-avvisi-digitali>`__

`11.1.5 Avvisatura pull 1 <#avvisatura-pull>`__

`11.1.6 Gestione degli errori 1 <#gestione-degli-errori-2>`__

`12. Backoffice 1 <#back-office>`__

`12.1 Revoca e storno 1 <#_Toc534291690>`__

`12.1.1 Processo di Revoca per Annullo Tecnico 1 <#_Toc534291691>`__

`12.1.2 Processo di Revoca di una Ricevuta Telematica per Charge-Back 1 <#_Toc534291692>`__

`12.1.3 Processo di Storno di un pagamento 1 <#_Toc534291693>`__

`12.2 Riconciliazione 1 <#_Toc534291694>`__

`12.2.1 Attori del processo di Riconciliazione Contabile e casi d’uso 1 <#_Toc534291695>`__

`12.2.2 Worflow di Riconciliazione 1 <#_Toc534291696>`__

`12.3 Gestione degli errori 1 <#_Toc534291697>`__

`12.3.1 Gestione degli errori di revoca 1 <#_Toc534291698>`__

`12.3.2 Gestione degli errori di storno 1 <#_Toc534291699>`__

`12.3.3 Gestione degli errori di riconciliazione 1 <#_Toc534291700>`__

`13. Ausiliarie 1 <#ausiliarie>`__

`13.1 Scenari, casi d’uso e attori 1 <#scenari-casi-duso-e-attori>`__

`13.1.1 Funzioni Ausiliarie per L’Ente Creditore 1 <#funzioni-ausiliarie-per-lente-creditore>`__

`13.1.2 Funzioni ausiliarie per il PSP 1 <#funzioni-ausiliarie-per-il-psp>`__

`13.1.3 Funzioni Ausiliarie per il NodoSPC 1 <#funzioni-ausiliarie-per-il-nodospc>`__

`Sezione IV – Processo di adesione ed Esercizio 1 <#_Toc355876994>`__

`14. Adesione al sistema pagoPA 1 <#adesione-al-sistema-pagopa>`__

`14.1 Adesione di un Ente Creditore. 1 <#adesione-di-un-ente-creditore.>`__

`14.2 Adesione di un Prestatore di Servizi di Pagamento 1 <#adesione-di-un-prestatore-di-servizi-di-pagamento>`__

`14.3 Intermediari e Partner tecnologici nel sistema pagoPA 1 <#intermediari-e-partner-tecnologici-nel-sistema-pagopa>`__

`15. Attivazione sul sistema pagoPA 1 <#attivazione-sul-sistema-pagopa>`__

`16. Attivazione di un EC direttamente connesso 1 <#attivazione-di-un-ec-direttamente-connesso>`__

`16.1 Processo di avvio in Esercizio 1 <#processo-di-avvio-in-esercizio>`__

`17. Attivazione di un EC intermediato 1 <#attivazione-di-un-ec-intermediato>`__

`17.1 Attivazione di un EC con un Intermediario Tecnologico 1 <#attivazione-di-un-ec-con-un-intermediario-tecnologico>`__

`17.2 Attivazione di un EC con un Partner Tecnologico 1 <#attivazione-di-un-ec-con-un-partner-tecnologico>`__

`17.2.1 Attivazione di Ente Creditore “pilota” 1 <#attivazione-di-ente-creditore-pilota>`__

`17.2.2 Attivazione di Ente Creditore “non pilota” 1 <#attivazione-di-ente-creditore-non-pilota>`__

`18. Attivazione di un PSP sul sistema pagoPA 1 <#attivazione-di-un-psp-sul-sistema-pagopa>`__

`18.1 Attivazione di un PSP che si collega direttamente al Nodo 1 <#attivazione-di-un-psp-che-si-collega-direttamente-al-nodo>`__

`18.2 Attivazione di un PSP che svolge il ruolo di Acquirer 1 <#attivazione-di-un-psp-che-svolge-il-ruolo-di-acquirer>`__

`18.3 Attivazione di un PSP che offre il servizio MyBank 1 <#attivazione-di-un-psp-che-offre-il-servizio-mybank>`__

`18.3.1 PSP che intendono svolgere il ruolo di Banca Buyer 1 <#psp-che-intendono-svolgere-il-ruolo-di-banca-buyer>`__

`18.3.2 PSP che intendono svolgere il ruolo di Banca Seller 1 <#psp-che-intendono-svolgere-il-ruolo-di-banca-seller>`__

`18.4 Attivazione di un PSP che offre il servizio CBILL 1 <#attivazione-di-un-psp-che-offre-il-servizio-cbill>`__

`18.5 Attivazione di un PSP intermediato 1 <#attivazione-di-un-psp-intermediato>`__

`19. Adempimenti durante l’erogazione del servizio 1 <#adempimenti-durante-lerogazione-del-servizio>`__

`19.1 Adempimenti dei soggetti direttamente collegati al Nodo-SPC 1 <#adempimenti-dei-soggetti-direttamente-collegati-al-nodo-spc>`__

`19.1.1 Tavoli operativi 1 <#tavoli-operativi>`__

`19.1.2 Monitoraggio e controllo 1 <#monitoraggio-e-controllo>`__

`19.1.3 Business continuity e Disaster Recovery 1 <#business-continuity-e-disaster-recovery>`__

`19.1.4 Archiviazione dei dati 1 <#archiviazione-dei-dati>`__

`19.1.5 Ulteriori adempimenti 1 <#ulteriori-adempimenti>`__

`19.2 Adempimenti dei soggetti non direttamente collegati al Nodo-SPC 1 <#adempimenti-dei-soggetti-non-direttamente-collegati-al-nodo-spc>`__

`20. Utilizzo del marchio pagoPA 1 <#utilizzo-del-marchio-pagopa>`__

`21. Disponibilità dei Servizi 1 <#disponibilità-dei-servizi>`__

`21.1 Nodo-SPC 1 <#nodo-spc>`__

`21.2 Enti Creditori 1 <#enti-creditori>`__

`21.3 Prestatori di servizi di pagamento aderenti 1 <#prestatori-di-servizi-di-pagamento-aderenti>`__

`22. Livelli di Servizio 1 <#livelli-di-servizio>`__

`22.1 Indicatori di qualità del Nodo-SPC 1 <#indicatori-di-qualità-del-nodo-spc>`__

`23. Responsabilità dei soggetti aderenti 1 <#responsabilità-dei-soggetti-aderenti>`__

`23.1 Responsabilità dell’Ente Creditore 1 <#responsabilità-dellente-creditore>`__

`23.2 Responsabilità del Prestatore di Servizi di Pagamento 1 <#responsabilità-del-prestatore-di-servizi-di-pagamento>`__

`APPENDICE I – APPROFONDIMENTI (ENTI CREDITORI) 1 <#_Toc534291745>`__

`Integrità e non ripudiabilità della Ricevuta Telematica 1 <#integrità-e-non-ripudiabilità-della-ricevuta-telematica>`__

`Acquisto della marca da bollo digitale 1 <#acquisto-della-marca-da-bollo-digitale>`__

`APPENDICE II – APPROFONDIMENTI (PRESTATORI DI SERVIZI DI PAGAMENTO) 1 <#_Toc534291748>`__

`Il servizio MyBank 1 <#il-servizio-mybank>`__

Definizioni e Acronimi
======================

+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| **Acronimo**                                                             | **Descrizione**                                                          |
|                                                                          |                                                                          |
| **Definizione**                                                          |                                                                          |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
|    AgID                                                                  |    Ente istituito ai sensi del decreto legge n. 83 del 22 giugno 2012    |
|                                                                          |    convertito con legge n. 134 del 7 agosto 2012 (già DigitPA).          |
|    Agenzia per l’Italia Digitale                                         |                                                                          |
|                                                                          |    Gestore del Nodo dei Pagamenti-SPC.                                   |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
|    Allegato A                                                            |    Il documento allegato alle Linee guida.                               |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
|    Buyer Bank                                                            |    Nell’ambito del servizio MyBank è la banca dell’utilizzatore finale.  |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
|    CAD                                                                   |    Codice dell'amministrazione digitale: decreto legislativo 7 marzo     |
|                                                                          |    2005, n. 82 aggiornato con le modifiche e integrazioni                |
|                                                                          |    successivamente introdotte.                                           |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
|    CCP                                                                   |    Codice Contesto di Pagamento.                                         |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
|    Certificato digitale                                                  |    Nella crittografia asimmetrica è un documento elettronico che attesta |
|                                                                          |    l'associazione univoca tra una chiave pubblica e l'identità di un     |
|                                                                          |    soggetto (una persona, una società, un computer, ecc.) che dichiara   |
|                                                                          |    di utilizzarla nell'ambito delle procedure di cifratura asimmetrica   |
|                                                                          |    e/o autenticazione tramite firma digitale.                            |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
|    Comitato di coordinamento SIPA                                        |    Comitato composto da Ragioneria Generale dello Stato, Corte dei       |
|                                                                          |    Conti, Agenzia per l’Italia Digitale e Banca d’Italia, che            |
|                                                                          |    sovraintende alla gestione del “Sistema Informatizzato dei Pagamenti  |
|                                                                          |    della Pubblica Amministrazione” applicabile all’Ente Creditore        |
|                                                                          |    Centrale.                                                             |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
|    Dominio                                                               |    Rappresenta il sistema complessivo che si riferisce sia alla comunità |
|                                                                          |    di Pubbliche Amministrazioni, Enti Creditori e prestatori di servizio |
|                                                                          |    aderenti che possono accedere ed utilizzare il Servizio, sia alle     |
|                                                                          |    componenti tecnico-organizzative dello stesso.                        |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
|    EC                                                                    |    Ente Creditore.                                                       |
|                                                                          |                                                                          |
|    Ente Creditore                                                        |    Nel contesto di pagoPA comprende le pubbliche amministrazioni, le     |
|                                                                          |    società a controllo pubblico, come definite nel decreto legislativo   |
|                                                                          |    adottato in attuazione dell’articolo 18 della legge n. 124 del 2015,  |
|                                                                          |    escluse le società quotate, ed i gestori di pubblici servizi. A       |
|                                                                          |    prescindere dalla natura giuridica dell’ente, è il soggetto aderente  |
|                                                                          |    a pagoPA indicato nell’elemento enteBeneficiario nella richiesta di   |
|                                                                          |    pagamento telematico.                                                 |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
|    Ente Aggregatore                                                      |    Soggetto SPCoop che mette a disposizione di altre Pubbliche           |
|                                                                          |    Amministrazioni una Porta di Dominio per consentire la cooperazione   |
|                                                                          |    applicativa con altri soggetti SPCoop.                                |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
|    ER                                                                    |    Esito Revoca                                                          |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
|    FESP                                                                  |    Front-End del Sistema dei Pagamenti. Componente del Nodo              |
|                                                                          |    Pagamenti-SPC che gestisce lo scambio di richieste di pagamento       |
|                                                                          |    telematico ed ricevute telematiche tra Ente Creditore e Prestatore di |
|                                                                          |    Servizi di Pagamento.                                                 |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
|    Flusso                                                                |    Serie di dati attinenti ad un Servizio di Nodo, oggetto o di          |
|                                                                          |    trasmissione o di un processo elaborativo e di trattamento            |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
|    Gestori di pubblici servizi                                           |    Le aziende e gli enti organizzati in forma societaria che gestiscono  |
|                                                                          |    servizi pubblici quali, ad esempio, Enel, Uffici postali (per quanto  |
|                                                                          |    riguarda il “servizio postale”), Italgas, Trenitalia, ecc., così      |
|                                                                          |    come, in ambito locale, le aziende che gestiscono l’erogazione di     |
|                                                                          |    acqua e gas o quelle che provvedono al trasporto urbano e alla        |
|                                                                          |    gestione degli edifici comunali, ecc.                                 |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
|    Initiating Party                                                      |    Componente tecnica offerta dalla Seller Bank che consente di mettere  |
|                                                                          |    in comunicazione il Nodo dei Pagamenti-SPC con il Routing Service     |
|                                                                          |    della Seller Bank per l’erogazione del servizio MyBank.               |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
|    Intermediario tecnologico                                             |    PA o Prestatore di Servizi di Pagamento aderente a pagoPA che         |
|                                                                          |    gestisce le attività di interconnessione al NodoSPC per conto di      |
|                                                                          |    altri soggetti aderenti a pagoPA (PA o Prestatore di Servizi di       |
|                                                                          |    Pagamento), ai sensi del § 8.3.3 delle Linee guida.                   |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
|    Istituto tesoriere                                                    |    Soggetto finanziario affidatario del servizio di tesoreria o di cassa |
|                                                                          |    della singola amministrazione, ivi compresa la Banca d’Italia, o del  |
|                                                                          |    gestore di pubblici servizi                                           |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
|    IUV                                                                   |    Identificativo Univoco Versamento                                     |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
|    Linee guida                                                           |    Il documento di cui le presenti specifiche attuative rappresentano    |
|                                                                          |    l’Allegato B.                                                         |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
|    MEF                                                                   |    Ministero dell’Economia e delle Finanze                               |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
|    MyBank                                                                |    Servizio che consente ai consumatori di effettuare in modo sicuro     |
|                                                                          |    pagamenti online usando il servizio di online banking delle propria   |
|                                                                          |    banca o un’app da smartphone o tablet.                                |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
|    NodoSPC                                                               |    Piattaforma tecnologica per l’interconnessione e l’interoperabilità   |
|                                                                          |    tra le Pubbliche Amministrazioni e i Prestatori di Servizi di         |
|    Nodo dei Pagamenti-SPC                                                |    Pagamento di cui all’art. 5, comma 2 del CAD                          |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
|    OBeP                                                                  |    Pagamento “istantaneo on-line” effettuato attraverso le               |
|                                                                          |    infrastrutture di home/remote banking di un Prestatore di Servizi di  |
|    On-line Banking ePayment                                              |    Pagamento contestualmente al perfezionamento di un acquisto di beni o |
|                                                                          |    servizi nel web.                                                      |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
|    PA                                                                    |    Pubblica Amministrazione (Centrale e Locale).                         |
|                                                                          |                                                                          |
|                                                                          |    Per la nozione di pubblica amministrazione, si rinvia a quanto già    |
|                                                                          |    ampiamente dettagliato dal Ministero dell’Economia e delle Finanze e  |
|                                                                          |    della Presidenza del Consiglio dei Ministri con la circolare          |
|                                                                          |    interpretativa n. 1 del 9 marzo 2015.                                 |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
|    pagoPA                                                                |    Il sistema dei pagamenti a favore delle pubbliche amministrazioni e   |
|                                                                          |    dei gestori di pubblici servizi.                                      |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
|    Partner tecnologico                                                   |    Soggetto che gestisce le attività di interconnessione al NodoSPC per  |
|                                                                          |    conto di una Pubblica Amministrazione, nel rispetto delle specifiche  |
|                                                                          |    tecniche contenute nelle Linee guida.                                 |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
|    PdD                                                                   |    Porta di Dominio SPCoop.                                              |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
|    Portale delle Adesioni                                                |    Sito web predisposto dall’Agenzia per l’Italia Digitale per           |
|                                                                          |    dematerializzare il processo di adesione dell'Ente Creditore e        |
|                                                                          |    automatizzare le attività gestionali degli enti aderenti.             |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
|    Provvedimento                                                         |    Provvedimento del Direttore dell’Agenzia delle Entrate del 19         |
|                                                                          |    settembre 2014 recante “Modalità di pagamento in via telematica       |
|    Bollo Digitale                                                        |    dell'imposta di bollo dovuta per le istanze e per i relativi atti e   |
|                                                                          |    provvedimenti trasmessi in via telematica ai sensi dell’art. 1, comma |
|                                                                          |    596, della legge 27 dicembre 2013, n. 147 - servizio @e.bollo”.       |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
|    Prestatore di Servizi di Pagamento                                    |    Prestatore di Servizi di Pagamento.                                   |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
|    Prestatore di Servizi di Pagamento dell’Ente Creditore                |    Il Prestatore di Servizi di Pagamento che l’Ente Creditore ha         |
|                                                                          |    indicato nella Richiesta di Pagamento Telematico in quanto titolare   |
|                                                                          |    del c/c da accreditare.                                               |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
|    Routing Service                                                       |    Componente che, nell’ambito del servizio MyBank, consente             |
|                                                                          |    l’autenticazione del soggetto creditore e l’inoltro della richiesta   |
|                                                                          |    di pagamento alla componente denominata Validation Service.           |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
|    RPT                                                                   |    Oggetto informatico inviato dall’Ente Creditore al Prestatore di      |
|                                                                          |    Servizi di Pagamento attraverso il Nodo dei Pagamenti-SPC al fine di  |
|    Richiesta di Pagamento Telematico                                     |    richiedere l’esecuzione di un pagamento.                              |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
|    RR                                                                    |    Richiesta Revoca                                                      |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
|    RT                                                                    |    Oggetto informatico inviato dal Prestatore di Servizi di Pagamento    |
|                                                                          |    all’Ente Creditore attraverso il Nodo dei Pagamenti-SPC in risposta   |
|    Ricevuta Telematica                                                   |    ad una Richiesta di Pagamento Telematico effettuata da un Ente        |
|                                                                          |    Creditore.                                                            |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
|    SACI                                                                  |    Specifiche attuative dei codici identificativi di versamento,         |
|                                                                          |    riversamento e rendicontazione, Allegato A alle Linee guida.          |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
|    SANP                                                                  |    Specifiche attuative del Nodo dei Pagamenti-SPC, Allegato B alle      |
|                                                                          |    Linee guida.                                                          |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
|    Seller Bank                                                           |    Nell’ambito del servizio MyBank è la banca dell’Ente Creditore.       |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
|    SEPA                                                                  |    Single Euro Payments Area (Area unica dei pagamenti in euro), ovvero  |
|                                                                          |    un'area nella quale gli utilizzatori degli strumenti di pagamento - i |
|                                                                          |    cittadini, imprese, pubbliche amministrazioni e gli altri operatori   |
|                                                                          |    economici - indipendentemente dalla loro residenza, possono           |
|                                                                          |    effettuare e ricevere pagamenti in euro non in contanti sia           |
|                                                                          |    all'interno dei confini nazionali che fra paesi diversi, alle stesse  |
|                                                                          |    condizioni e con gli stessi diritti e obblighi. La SEPA riguarda 32   |
|                                                                          |    paesi (tutti i paesi dell'Unione Europea più l'Islanda, la Norvegia,  |
|                                                                          |    il Liechtenstein, la Svizzera e il Principato di Monaco).             |
|                                                                          |                                                                          |
|                                                                          |    Il progetto SEPA, avviato oltre 10 anni fa - su impulso delle         |
|                                                                          |    autorità europee - dall'industria bancaria e dei pagamenti europea,   |
|                                                                          |    prevede la definizione di standard comuni per bonifici e addebiti     |
|                                                                          |    diretti, i due principali servizi di pagamento al dettaglio in euro   |
|                                                                          |    diversi dal contante. Ai sensi del Regolamento UE 260/2012, la        |
|                                                                          |    migrazione ai nuovi strumenti europei dovrà completarsi entro il 1°   |
|                                                                          |    febbraio 2014.                                                        |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
|    Servizi di Nodo                                                       |    Funzionalità rese disponibili dal Nodo dei Pagamenti-SPC ai soggetti  |
|                                                                          |    appartenenti al Dominio.                                              |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
|    Servizio                                                              |    L’insieme delle funzione e delle strutture tecniche, organizzative e  |
|                                                                          |    di governo finalizzate all’interconnessione e all’interoperabilità    |
|                                                                          |    tra gli Enti Creditori ed i Prestatori di Servizi di Pagamento        |
|                                                                          |    aderenti, ai sensi dell’articolo 81, comma 2-bis, del CAD.            |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
|    SIPA                                                                  |    Nel dicembre 2000 la Ragioneria generale dello Stato, l’AIPA (oggi    |
|                                                                          |    Agenzia per l’Italia Digitale), la Banca d’Italia e la Corte dei      |
|                                                                          |    conti hanno sottoscritto il "Protocollo d’intesa per lo sviluppo del  |
|                                                                          |    Sistema Informatizzato dei Pagamenti della Pubblica Amministrazione – |
|                                                                          |    SIPA".                                                                |
|                                                                          |                                                                          |
|                                                                          |    Gli obiettivi del SIPA erano la completa attuazione della Legge       |
|                                                                          |    367/94 che prevedeva la diffusione dei sistemi telematici nelle       |
|                                                                          |    procedure di spesa dell’Amministrazione Centrale.                     |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
|    SPC                                                                   |    Sistema Pubblico di Connettività.                                     |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
|    SPCoop                                                                |    Sistema Pubblico di Connettività e cooperazione.                      |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
|    Standard di Servizio                                                  |    Specifiche attuative del servizio di cui alle Sezioni II e III        |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
|    Utente                                                                |    Persona fisica o giuridica che effettua un pagamento elettronico in   |
|                                                                          |    favore di un Ente creditore attraverso pagoPA.                        |
|    Utilizzatore finale                                                   |                                                                          |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
|    Validation Service                                                    |    Componente che, nell’ambito del servizio MyBank, deve comunicare con  |
|                                                                          |    l’applicazione di *Home banking* dell’utilizzatore finale per         |
|                                                                          |    autenticarlo, secondo le modalità previste dal Prestatore di Servizi  |
|                                                                          |    di Pagamento, e completare l’acquisto.                                |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
|    Web Service                                                           |    È un sistema software progettato per supportare l'interoperabilità    |
|                                                                          |    tra diversi elaboratori su di una medesima rete ovvero in un contesto |
|                                                                          |    distribuito (definizione da W3C, World Wide Web Consortium).          |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
|    Web-FESP                                                              |    Componente del Nodo Pagamenti-SPC che permette di effettuare il       |
|                                                                          |    pagamento attraverso i portali o i canali messi a disposizione dal    |
|                                                                          |    Prestatore di Servizi di Pagamento nei confronti dell’utilizzatore    |
|                                                                          |    finale.                                                               |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
|    WISP                                                                  |    Wizard Interattivo di Scelta del Prestatore di Servizi di Pagamento.  |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
|    Wrapper MyBank                                                        |    Componente del Nodo dei Pagamenti-SPC che si occupa di effettuare le  |
|                                                                          |    necessarie conversioni di tracciati e gestire il colloquio tra il     |
|                                                                          |    Nodo stesso e la componente Initiating Party messa a disposizione     |
|                                                                          |    dalla Seller Bank.                                                    |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
|    WSDL                                                                  |    *Web service* Description Language.                                   |
|                                                                          |                                                                          |
|                                                                          |    È un linguaggio formale utilizzato per la creazione di "documenti"    |
|                                                                          |    che definiscono il “Web Service”.                                     |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+

Introduzione alla versione 2.2
==============================

Il sistema dei pagamenti elettronici a favore della Pubblica Amministrazione, il Sistema pagoPA, garantisce agli Utilizzatori finali (cittadini e
imprese) di effettuare pagamenti elettronici alla Pubblica Amministrazione in modo sicuro e affidabile, semplice, in totale trasparenza nei costi di
commissione e in funzione delle proprie esigenze.

L’introduzione del Sistema pagoPA porta benefici per i cittadini, la Pubblica Amministrazione e l’intero sistema Paese:

-  Benefici per i Cittadini

-  trasparenza e minori costi

-  possibilità di usufruire dei servizi pubblici in maniera più immediata

-  semplificazione del processo di pagamento che consente di usufruire del maggior numero di canali e servizi possibili

-  standardizzazione dell’esperienza utente per i pagamenti verso la Pubblica Amministrazione

-  standardizzazione delle comunicazioni di avviso di pagamento, riconoscibile su tutto il territorio nazionale

-  Benefici per la Pubblica Amministrazione:

   -  riduzione dei tempi di incasso attraverso l’accredito delle somme direttamente sui conti dell’Ente Beneficiario entro il giorno successivo al
      pagamento

-  riduzione dei costi di gestione del contante

-  miglioramento dell’efficienza della gestione degli incassi attraverso la riconciliazione automatica

-  superamento della necessità bandire gare per l’acquisizione di servizi di incasso, con conseguenti riduzioni di inefficienze e costi di commissione
   fuori mercato

-  riduzione dei costi e tempi di sviluppo delle applicazioni online (riuso soluzioni)

-  eliminazione della necessità di molteplici accordi di riscossione

-  maggiori controlli automatici per evitare i doppi pagamenti e le conseguenti procedure di rimborso

-  Benefici per i Prestatori di Servizi di Pagamento:

-  Eliminazione necessità molteplici accordi con le PA

-  Riduzione dei costi di gestione del contante

-  Miglioramento dei servizi resi

-  Fidelizzazione della clientela

-  Benefici per il Sistema Paese:

-  completa aderenza agli standard della PSD2

-  incentivazione dell’utilizzo dei pagamenti elettronici a livello nazionale attraverso l’utilizzo con le transazioni verso la Pubblica
   Amministrazione, che consente di stimolare il mercato e favorire, a tendere, una maggiore concorrenza nel mercato dei servizi di pagamento ed un
   livellamento delle commissioni

Il Sistema pagoPA è stato realizzato dall’Agenzia per l’Italia Digitale (AgID) in attuazione dell’art. 5 del CAD , il quale precisa che “Al fine di
dare attuazione a quanto disposto dall'articolo 5, l’Agenzia per l’Italia Digitale (già DigitPA) mette a disposizione, attraverso il Sistema pubblico
di connettività, una piattaforma tecnologica per l'interconnessione e l’interoperabilità tra le pubbliche amministrazioni e i prestatori di servizi di
pagamento abilitati, al fine di assicurare, attraverso strumenti condivisi di riconoscimento unificati, l'autenticazione certa dei soggetti
interessati all'operazione in tutta la gestione del processo di pagamento”.

IL CAD inoltre ha affidato all’Agenzia per l’Italia Digitale, sentita la Banca d'Italia, il compito di definire le Linee guida per la specifica delle
modalità tecniche e operative per l’esecuzione dei pagamenti elettronici ed introdotto all’articolo 15, comma 5 bis, del D.L. n. 179/2012,
l’obbligatorietà dell’uso di una piattaforma tecnologica messa a disposizione dall’Agenzia per l’Italia Digitale per le Pubbliche Amministrazioni e i
Gestori di Pubblico Servizio.

Il presente documento denominato “\ *Specifiche Attuative del Nodo dei Pagamenti-SPC*\ ” rappresenta l’\ **Allegato B** alle *“Linee guida per
l'effettuazione dei pagamenti a favore delle pubbliche amministrazioni e dei gestori di pubblici servizi”* (di seguito, Linee guida) e deve essere
utilizzato in combinazione con il documento *"Specifiche attuative dei codici identificativi di versamento, riversamento e rendicontazione"*
(**Allegato A)**, nonché con le stesse Linee guida; documenti ai quali si rimanda per tutte le voci e gli argomenti non specificatamente qui indicati.

La presente versione delle Specifiche Attuative del Nodo dei Pagamenti-SPC (di seguito, NodoSPC) è il frutto di una diversa scelta editoriale per la
presentazione dei contenuti. Le modifiche apportate al presente documento riguardano una riorganizzazione del testo, al fine di migliorarne la
leggibilità e l’utilizzo come documento tecnico per diverse tipologie di lettori.

A tal fine il documento è suddiviso nelle seguenti quattro sezioni:

-  Sezione I – Modello Generale del Sistema, in cui si fornisce una visione d’insieme e di alto livello del Sistema pagoPA, con un linguaggio ed un
   livello di dettaglio fruibile anche ai non addetti ai lavori

-  Sezione II – Regole di funzionamento del Sistema, in cui sono dettagliati i diversi processi gestiti dal Sistema pagoPA. Lo scopo è quello di
   esplicitare ai diversi soggetti coinvolti le responsabilità connesse al loro ruolo. Nella Sezione II sono altresì dettagliati, in maniera
   descrittiva, i controlli funzionali effettuati dal NodoSPC e le possibili eccezioni

-  Sezione III – Specifiche funzionali e tecniche del Sistema, in cui sono dettagliati gli oggetti, i messaggi, i flussi informativi, gli stati del
   pagamento e gli errori gestiti sul NodoSPC. Tale sezione include anche i casi di test da eseguire per l’autovalutazione del proprio software.

-  Sezione IV – Procedure di adesione ed esercizio, in cui sono dettagliare le procedure tecniche e amministrative da seguire per aderire al Sistema
   pagoPA, per attivare i servizi e per gestire gli adempimenti richiesti all’esercizio del sistema e per accedere ai servizi di assistenza e
   supporto.

N.B. Si fa presente che i paragrafi per i quali è prevista una proposta evolutiva per la versione 3.0 delle Specifiche Attuative di prossima
pubblicazione, saranno contrassegnati dalla seguente dicitura:

+----------+-----------------------------------------------+
| |image1| | **Paragrafo soggetto a proposta di modifica** |
+----------+-----------------------------------------------+

+------------------------------------------------+
| SEZIONE I – FUNZIONAMENTO GENERALE DEL SISTEMA |
+------------------------------------------------+

Obiettivo strategico del Sistema pagoPA è quello di facilitare e diffondere gli strumenti di pagamento elettronici, in particolare, quelli riferiti
agli incassi della Pubblica Amministrazione, che da un lato associno, nel rispetto delle situazioni già in essere, benefici ai fini della gestione dei
servizi di tesoreria, dall’altro consentano alla Pubblica Amministrazione di dotarsi di nuove modalità di rapporto con i cittadini e le imprese per
tutte le problematiche di incasso, assicurando nel contempo un coordinamento a livello nazionale della concreta attuazione ed evoluzione nel tempo del
sistema.

Ciò consente alla Pubblica Amministrazione di eliminare gli onerosi processi di gestione del back office, attraverso processi automatizzati di
riconciliazione. Identico beneficio è atteso per ogni operatore del settore dei pagamenti che aderisca all’iniziativa che si inquadra, da un lato,
nella più ampia regolamentazione europea in materia di servizi di pagamento introdotto con il progetto SEPA, dall’altro, nell’attuazione delle norme
introdotte dal nuovo articolo 5 del CAD in tema di pagamenti informatici a favore della Pubblica Amministrazione.

Le suddette norme trovano una concreta attuazione tramite l’infrastruttura abilitante, denominata Nodo dei Pagamenti-SPC (NodoSPC). Tale
infrastruttura si configura come una componente del Sistema Pubblico di Connettività che regola - a livello nazionale - le modalità organizzative e
tecnico-infrastrutturali di funzionamento dei pagamenti verso la Pubblica Amministrazione, senza alterare i rapporti commerciali tra i diversi attori
del processo, ma introducendo più semplici modalità di interazione.

In questo contesto l’impianto si configura come un sistema di livello nazionale definito anche come “Dominio dei Pagamenti della Pubblica
Amministrazione” (Dominio), che ha assunto a partire dalla fine dell'anno 2014, con la registrazione del correlato marchio, la denominazione di
Sistema pagoPA.

Il modello di funzionamento del Sistema fa riferimento ai principi del *Four Corners* *model* definito dall’European Payment Council ed è riportato
nel diagramma di Figura 1, nel quale l’infrastruttura costituita dal NodoSPC si pone quale facilitatore del colloquio i vari soggetti coinvolti:

+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| **Utilizzatore finale**                                                  | Rappresenta il privato cittadino, professionista, impresa, che effettua  |
|                                                                          | pagamenti a favore della Pubblica Amministrazione con modalità           |
| **(Debtor)**                                                             | informatiche. L’identità dell’utilizzatore finale può essere determinata |
|                                                                          | con modalità informatiche (tipicamente SPID) per accedere ai servizi     |
|                                                                          | informatici dell’Ente Creditore.                                         |
|                                                                          |                                                                          |
|                                                                          | Nell’ambito del processo di pagamento si distingue il ruolo del          |
|                                                                          | **soggetto debitore**, cioè colui che ha contratto un debito a favore    |
|                                                                          | dell’Ente Creditore, ovvero effettua un pagamento di sua iniziativa per  |
|                                                                          | ottenere a un servizio o una certificazione. Nel rapporto con Ente       |
|                                                                          | Creditore si può presumere che l’utilizzatore finale sia il soggetto     |
|                                                                          | debitore                                                                 |
|                                                                          |                                                                          |
|                                                                          | Si distingue infine il **soggetto versante**, ovvero come colui accede   |
|                                                                          | ai servizi informatici dal Prestatore dei Servizi di Pagamento, e        |
|                                                                          | dispone il pagamento a favore dell’Ente Creditore.                       |
+==========================================================================+==========================================================================+
| **Ente Creditore**                                                       | Soggetto a cui l’utilizzatore finale richiede il servizio e che nei      |
|                                                                          | confronti del quali si configura come “creditore” per le somme a vario   |
| **(Creditor)**                                                           | titolo da questi dovute.                                                 |
|                                                                          |                                                                          |
|                                                                          | L’Ente Creditore, che identifica il soggetto pagatore e la causale del   |
|                                                                          | pagamento, offre il servizio tramite il NodoSPC a cui accede             |
|                                                                          | direttamente o tramite un soggetto pubblico o privato, quale             |
|                                                                          | intermediario tecnologico nei confronti dell’Ente Creditore .            |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| **Prestatore di Servizi di Pagamento**                                   | È il soggetto, abilitato dalle norme vigenti in materia, ad eseguire le  |
|                                                                          | richieste di pagamento in via elettronica ed a restituire la ricevuta    |
| **(Debtor e Creditor Bank)**                                             | elettronica di avvenuto pagamento/incasso.                               |
|                                                                          |                                                                          |
|                                                                          | Il Prestatore di Servizi di Pagamento offre i propri servizi di          |
|                                                                          | pagamento mettendo a disposizione direttamente o tramite terze parti     |
|                                                                          | (intermediari) i canali di pagamento, fisici e telematici, su cui        |
|                                                                          | l’utilizzatore finale può effettuare l’operazione.                       |
|                                                                          |                                                                          |
|                                                                          | In questo contesto il Prestatore di Servizi di Pagamento può svolgere    |
|                                                                          | anche, sulla base di appositi accordi con l’ente, funzioni di “Incasso”  |
|                                                                          | per conto dello stesso e provvedere, laddove richiesto, al successivo    |
|                                                                          | riversamento delle somme percepite sui conti di tesoreria che l’Ente     |
|                                                                          | Creditore detiene presso il Prestatore di Servizi di Pagamento dell’Ente |
|                                                                          | Creditore.                                                               |
|                                                                          |                                                                          |
|                                                                          | È il Prestatore di Servizi di Pagamento che, nel rispetto delle          |
|                                                                          | normative vigenti, svolge le proprie funzioni di Tesoreria o di Cassa    |
|                                                                          | nei confronti dell’Ente Creditore e può non coincidere con il Prestatore |
|                                                                          | di Servizi di Pagamento dell’Ente Creditore stesso.                      |
|                                                                          |                                                                          |
|                                                                          | L’utilizzo dell’infrastruttura del NodoSPC non altera in alcun modo i    |
|                                                                          | rapporti esistenti tra l’Ente Creditore ed il proprio istituto           |
|                                                                          | tesoriere.                                                               |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+

|image2|

**Figura 1 – EPC Four Corners model**

Il perfezionamento delle operazioni tra banche avviene attraverso il sistema di regolamento e compensazione (CSM) utilizzando le regole SEPA.

Il sistema supporta anche altri tipi di operazioni di pagamento che risultano dal collegamento tra più servizi di pagamento o tra servizi di pagamento
e altre operazioni ad essi contigue, così come definito dal Provvedimento Banca d’Italia del 5 luglio 2011 in materia di diritti e obblighi delle
parti nei servizi di pagamento.

Dal punto di vista organizzativo, la partecipazione al sistema si configura attraverso la sottoscrizione di accordi di servizio tra l’Agenzia per
l’Italia Digitale, i Prestatori di Servizi di Pagamento, le Pubbliche Amministrazioni ed eventualmente i gestori di pubblici servizi: ciò consente di
stabilire un rapporto di collaborazione “molti a molti”, accelerando il processo di attuazione del sistema.

La struttura del sistema prevede inoltre la possibilità che le attività legate all’effettuazione dei pagamenti siano eseguite, in tutto od in parte,
da Intermediari tecnologici (soggetti pubblici e/o privati) per conto sia delle Pubbliche Amministrazioni che dei Prestatori di servizi di pagamento:

-  Un Intermediario tecnologico è un soggetto aderente al NodoSPC come Ente Creditore (ad esempio: Regione), che quindi ha già accettato e si è
   obbligato al rispetto delle Linee Guida e dei relativi allegati e che risulta, altresì, responsabile, nei confronti dell’Agenzia per l’Italia
   Digitale, delle attività tecniche per l’interfacciamento con il NodoSPC.

-  Viceversa, il Partner tecnologico è un mero fornitore dell’Ente Creditore utilizzato in via strumentale per l’esecuzione delle attività tecniche
   per l’interfacciamento con il NodoSPC, ferma restando la responsabilità nei confronti di AgID in capo all’Ente Creditore. Si precisa che l’Agenzia
   per l’Italia Digitale esclude l’adesione al NodoSPC da parte del Partner tecnologico in quanto tale.

Si precisa che l’utilizzo di un particolare Intermediario tecnologico o Partner tecnologico può essere limitato ad una parte delle attività dell’Ente
Creditore, mentre le rimanenti attività possono essere gestiste da un altro soggetto Intermediario e/o Partner oppure in proprio dall’ente stesso:
possono cioè coesistere situazioni miste, nelle quali i servizi sono erogati da una molteplicità di soggetti, compreso l’Ente Creditore, sempre nel
rispetto delle Linee guida.

Anche i Prestatori di Servizi di Pagamento possono utilizzare degli intermediari per connettersi al NodoSPC o per offrire i propri servizi di
pagamento; tali soggetti possono essere rappresentati da altri prestatori di servizi di pagamento ovvero da circuiti o consorzi costituiti in ambito
finanziario.

Rimangono, comunque, inalterate le responsabilità di Ente Creditore e Prestatori di Servizi di Pagamento nei confronti delle proprie controparti
diverse dall’Agenzia per l’Italia Digitale e, in particolare, degli utilizzatori finali.

Il sistema è corredato da un ambiente di sperimentazione da utilizzare dai nuovi aderenti al sistema e per effettuare collaudi su eventuali modifiche
apportate alle presenti Specifiche attuative a seguito di variazioni conseguenti a modificazioni della normativa, alle mutate esigenze delle pubbliche
amministrazioni e degli utenti, all’evoluzione del contesto tecnologico.

Il ciclo di vita del pagamento gestito sul Sistema pagoPA
---------------------------------------------------------

Nell’ambito delle relazioni tra l’utilizzatore finale e gli Enti Creditori, la necessità di effettuare pagamenti a favore di questi ultimi è sempre
associata a procedimenti amministrativi che prevedono il rispetto di regole per il loro corretto svolgimento (ad esempio: la verifica di prerequisiti)
e seguono un preordinato “Ciclo di vita” che può essere schematizzato nella Figura 2.

|image3|

**Figura 2 - Ciclo di vita del pagamento**

1. L’esigenza del pagamento può nascere in due modi che innescano processi di business differenti:

-  sulla base di un bisogno dell’Utilizzatore finale che necessita, ad esempio, di un servizio da parte dell’ente

-  quando quest’ultimo deve richiedere all’Utilizzatore finale l’estinzione di un debito creatosi nei suoi confronti: ad esempio il pagamento di una
   multa o di un’ammenda.

2. L’esigenza di pagamento si concretizza attraverso la generazione di una **posizione debitoria**, cioè l’insieme di informazioni che l’Ente
   Creditore deve memorizzare in appositi archivi per consentire il pagamento e la successiva fase di riconciliazione.

3. L’utilizzatore finale sceglie il Prestatore di Servizi di Pagamento e effettua il pagamento. Il Prestatore di Servizi di Pagamento del pagatore
   incamera i fondi da destinare all’Ente Creditore.

4. Il Prestatore di Servizi di Pagamento del pagatore esegue il regolamento contabile dell’operazione accreditando il conto indicato dall’Ente
   Creditore con un SEPA Credit Transfer, salvo le eccezioni previste dalla vigente normativa di settore.

5. L’Ente Creditore esegue la fase di riconciliazione contabile del pagamento

6. L’Ente Creditore rilascia - se previsto – la relativa quietanza.

L’esecuzione di pagamenti telematici prevede l’interazione (realizzata tramite tecnologia *Web service*) tra i sistemi informativi dei vari attori
aderenti al Dominio. Il NodoSPC è il centro stella del sistema che assicura l’interoperabilità dei sistemi dei soggetti aderenti rendendo disponibili
primitive e metodi per l’interscambio dei flussi di dati, nonché l’interfaccia per la selezione del Prestatore di Servizi di Pagamento del pagatore.
Tutte le funzionalità per la definizione e la gestione dei pagamenti dovranno essere rese disponibili dai partecipanti al Dominio, ognuno secondo il
proprio ruolo.

A tal fine il NodoSPC gestisce diversi *workflow* applicativi che prevedono lo scambio di oggetti contenenti le informazioni necessarie a garantire la
corretta gestione dei processi. Tali *workflow* sono descritti nel dettaglio nella sezione III

L’adesione al Sistema pagoPA
----------------------------

Il sistema complessivo - formato dalla comunità di Enti Creditori, Prestatori di Servizi di Pagamento ed eventuali gestori di pubblici servizi
aderenti e dai loro intermediari tecnologici, che possono accedere ed utilizzare il Servizio – costituisce, come detto sopra il “Dominio dei Pagamenti
delle Pubbliche Amministrazioni”, altrimenti denominato “Dominio dei Pagamenti dell’Ente Creditore” (o più brevemente Dominio). Implicitamente con il
termine di Dominio ci si riferisce anche alle componenti tecnico-organizzative di tali attori.

L’utilizzo dei servizi messi a disposizione dal NodoSPC è attivato attraverso apposite procedure rese disponibili sul sito dell’Agenzia per l’Italia
Digitale. In particolare:

-  le Pubbliche Amministrazioni e i gestori di pubblici servizi sottoscrivono con l’Agenzia per l’Italia Digitale specifiche lettere di adesione;

-  i prestatori di servizi di pagamento sottoscrivono con l’Agenzia per l’Italia Digitale, su base volontaria, appositi Accordi di Servizio.

Nella Sezione IV sono descritte le procedure di accreditamento degli Enti Creditori e dei Prestatori di Servizi di Pagamento.

Ogni Ente Creditore e Prestatore di Servizi di Pagamento aderente può, per lo svolgimento delle attività tecniche, utilizzare intermediari rimanendo
comunque responsabile in quanto mittente o destinatario logico dei flussi.

Tutto ciò è subordinato alla preventiva comunicazione all’Agenzia per l’Italia Digitale che dovrà provvedere alla necessaria configurazione del
NodoSPC.

Nel Dominio, le attività di pertinenza di ogni soggetto sono effettuate conformemente ai requisiti di riservatezza e di protezione da accessi non
autorizzati. A Tal fine l’Agenzia per l’Italia Digitale rende disponibile SPID (Sistema Pubblico di Identità Digitale). Inoltre gli indirizzi internet
dei servizi dedicati ai pagamenti devono essere inoltre pubblicati sull'Indice delle Pubbliche Amministrazioni (IPA [1]_) istituito con il DPCM del 31
ottobre 2000 recante le regole tecniche per il protocollo informatico.

Si ricorda, altresì, che i siti Web di cui all'art. 3, comma 1, della Legge 9 gennaio 2004, n. 4 devono rispettare i requisiti di accessibilità
previsti dall'Allegato A del DM 8 luglio 2005 [2]_, rispettando, tra l'altro, il punto 3 dei criteri di conformità (Processi completi: quando un
servizio è erogato mediante un processo che si sviluppa su più pagine web allora tutte le pagine web ad esso relative devono essere conformi, anche
quando tali pagine si trovino su siti diversi). Per ulteriori riferimenti, consultare la sezione accessibilità del sito dell’Agenzia per l'Italia
Digitale.

Gli utilizzatori finali non sono membri del Dominio: pertanto il loro riconoscimento e l’abilitazione ad effettuare attività che determineranno
l’invocazione dei Servizi di Nodo è a cura dei soggetti aderenti (Ente Creditore, Prestatori di Servizi di Pagamento e/o intermediari da questi
utilizzati) che erogano i servizi applicativi.

*Governance* del sistema
------------------------

Stante la valenza infrastrutturale dell’iniziativa, la guida ed il controllo del sistema (*governance*) è affidata all’\ **Agenzia per l’Italia
Digitale**, che assicura la gestione del sistema attraverso la definizione di regole e standard, definisce l’elenco delle Pubbliche Amministrazioni e
dei Prestatori di Servizi di Pagamento partecipanti al sistema, provvede alla gestione ed al monitoraggio dell’infrastruttura;

Gli oggetti scambiati
---------------------

Nei *workflow* applicativi gestiti dal NodoSPC è previsto lo scambio di oggetti applicativi costituiti da documenti informatici. Le funzioni primarie
sono assicurate dallo scambio dei seguenti oggetti e informazioni:

-  *Richiesta Pagamento Telematico* (RPT). Emessa dall’Ente Creditore definisce tutti gli elementi caratterizzanti il pagamento nonché i parametri
      necessari all’esecuzione;

-  *Ricevuta Telematica* (RT). Emessa da un Prestatore di Servizi di Pagamento a valle di un pagamento innescato da una richiesta di pagamento
   telematico, definisce gli elementi necessari a qualificare l’esito dell’operazione;

-  *Richiesta Revoca* (RR). Emessa da un Ente aderente per richiedere alla controparte la revoca di una ricevuta telematica o lo storno di un
   pagamento;

-  *Esito Revoca* (ER). Oggetto emessa per fornire alla controparte l’esito di una RR.

-  *Codice Contesto Pagamento* (CCP). È un codice utilizzato in caso di pagamenti da Prestatore servizi di Pagamento, che supporta la rilavorazione
   dei pagamenti non andati a buon fine

-  *Identificativo Univoco Versamento* (IUV) assegnato dall’Ente Creditore attraverso le regole di generazione previste nella Sezione I del documento
   "Specifiche attuative dei codici identificativi di versamento, riversamento e rendicontazione" allegato A alle “Linee guida per l'effettuazione dei
   pagamenti a favore delle pubbliche amministrazioni e dei gestori di pubblici servizi”. Ogni coppia di oggetti precedentemente definiti (RPT, RT,
   RR, ER, CCP), sono identificati a livello nazionale dalla seguente coppia di informazioni:

   -  ID dell’Ente Creditore,

   -  codice identificativo univoco versamento (IUV).

-  *Flusso di Rendicontazione* (FR). è il documento informatico inviato dal PSP agli EC tramite il NodoSPC che raccoglie i dettagli dei versamenti
   eseguiti presso i conti correnti delle pubbliche amministrazioni relativamente alle richieste telematiche di pagamento ricevute. Per maggiori
   dettagli consultare l’allegato A delle Linee Guida

Gli Enti Creditori (e i loro intermediari) si avvalgono della piattaforma tecnologica del NodoSPC solo per scambiare con i Prestatore di Servizi di
Pagamento (e i loro intermediari) i flussi informativi costituiti dalle strutture dati standardizzate (RPT e RT) necessarie all’istradamento del
pagamento informatico:

-  L’utilizzatore finale dispone il pagamento per mezzo di una richiesta di pagamento telematico, tramite sportelli fisici o telematici messi a
   disposizione dall’Ente Creditore, da eventuali intermediari dallo stesso o direttamente da un Prestatore di Servizi di Pagamento (o dai suoi
   intermediari).

-  Indipendentemente dal canale utilizzato, l’esecutore del pagamento è un Prestatore di Servizi di Pagamento scelto direttamente dall’utilizzatore
   finale: il Prestatore di Servizi di Pagamento entra in possesso della richiesta di pagamento telematico messa a disposizione dall’Ente Creditore (o
   dal suo intermediario) attraverso il NodoSPC, esegue il pagamento richiesto ed emette una ricevuta telematica, che certifica l’esito del pagamento.

-  La ricevuta telematica è veicolata attraverso il NodoSPC e consegnata all’Ente Creditore (o al suo intermediario) ed è rilasciata all’utilizzatore
   finale.

L’effettiva esecuzione dei pagamenti, instradati da tale scambio informativo, è gestita utilizzando i circuiti di pagamento esistenti, esterni al
NodoSPC.

Nell’ambito delle funzionalità esposte dal NodoSPC è previsto lo scambio di ulteriori oggetti applicativi e servizi applicativi opzionali che verranno
dettagliati nella Sezione III.

Obblighi degli Enti Creditori
-----------------------------

Al fine di gestire nel modo migliore l’iter del processo di pagamento gli Enti Creditori hanno l’obbligo di rendere disponibili direttamente
all’utilizzatore finale, attraverso opportuni servizi informatici offerti direttamente o tramite intermediari:

-  le modalità per effettuare i pagamenti informatici e il trasferimento di ogni altra informazione che abbia il fine di agevolarne l’esecuzione;

-  l’accesso all’archivio delle ricevute telematica relative ad ogni pagamento da questi disposto. Fino a prescrizione, è fatto obbligo all’Ente
   Creditore di conservare le informazioni di ogni ricevuta telematica in modo da poterla riprodurre a richiesta anche su supporti cartaceo;

-  le modalità di gestione, nel rispetto della normativa vigente, di possibili flussi secondari (reclami, rimborsi, storni), anche usufruendo delle
   funzionalità accessorie messe a disposizione dalla piattaforma.

Si sottolinea inoltre che l’Ente Creditore dovrà mettere a disposizione dell’Utilizzatore finale un servizio di *help desk* disponibile h24 7/7
unitamente a un tavolo operativo.

Trasparenza nei confronti degli utilizzatori finali 
----------------------------------------------------

La trasparenza dell’operazione di pagamento deve essere garantita nei confronti dell’utilizzatore finale. A tal fine il NodoSPC mette a disposizione
apposite funzioni che consentono ai Prestatori di Servizi di Pagamento di esporre i costi del servizio, differenziati per strumento e/o canale di
pagamento in modo che gli utilizzatori finali possano scegliere il servizio che più si addice alle proprie esigenze.

In merito a quest'ultimo punto, si fa presente che il NodoSPC mette a disposizione degli Enti Creditori una funzione centralizzata che dà agli
utilizzatori finali la possibilità di sperimentare, nella scelta del servizio di pagamento, la stessa *user experience* in modalità unificata a
livello nazionale. Tale funzione mantiene inalterata la facoltà in capo al Prestatore di Servizi di Pagamento di stabilire commissioni specifiche e/o
di maggior favore per il singolo utilizzatore finale. In merito, si precisa che resta in capo al Prestatore di Servizi di Pagamento l’onere di
promuovere e pubblicizzare alla propria clientela e attraverso i propri canali ogni attività di *pricing* differente da quella esposta a livello
nazionale dalla funzione centralizzata del NodoSPC.

A tale proposito, si ricorda che è altresì onere del Prestatore di Servizi di Pagamento individuare, se del caso, le modalità con cui indicare
all’utilizzatore finale l’importo della commissione specifica e/o di maggior favore praticata all’atto dell’esecuzione del singolo pagamento.

Funzioni accessorie di controllo 
---------------------------------

Il Sistema prevede modalità di controllo focalizzate sulla verifica della corretta applicazione degli Standard di Servizio (p.e. norme di
comportamento, livelli di Servizio garantiti, ecc.) e dei processi che da questi derivano.

A supporto di tali funzioni, ogni soggetto (Enti Creditori e Prestatori di Servizi di Pagamento aderenti, NodoSPC) deve registrare all’interno del
proprio sistema (dominio del soggetto) ogni singolo evento significativo dal punto di vista applicativo al fine di tenerne traccia.

L’insieme di tali registrazioni, indipendentemente dalle peculiarità tecniche delle soluzioni adottate da ciascun soggetto che definisce in autonomia
tali aspetti, costituisce il “Giornale degli Eventi” che riporta gli estremi di tutte le situazioni verificatesi nell’esecuzione dell’operazione di
pagamento nelle varie tratte coinvolte (tra Enti Creditori e NodoSPC, nel NodoSPC, tra NodoSPC e Prestatori di Servizi di Pagamento).

Tali informazioni devono essere fornite ai soggetti interessati sul supporto definito dal soggetto che registra tali informazioni. Il NodoSPC fornisce
tali informazioni su supporto cartaceo e file XML (i dettagli relativi ai formati sono riportati in Sezione III).

Sicurezza e conservazione
-------------------------

Tutte le informazioni trattate nell’ambito del Sistema saranno gestite dai diversi attori che interagiscono con il NodoSPC, ciascuno nell’ambito della
propria competenza e responsabilità, nel rispetto delle regole definite dal CAD in materia di conservazione dei documenti informatici e di sicurezza
dei dati.

In merito, si rammenta che la conservazione è finalizzata a proteggere nel tempo i documenti informatici e i dati ivi contenuti, assicurandone, tra
l’altro, la sicurezza, l'integrità e la non modificabilità, al fine di preservare il valore probatorio del documento informatico e, nel caso specifico
del Sistema pagoPA, della transazione di pagamento.

Considerato che la quietanza, fornita dall’Ente Creditore all’utilizzatore finale, è formata sulla base degli oggetti scambiati attraverso il NodoSPC,
si ritiene che, al fine di conservare traccia dell’intera transazione di pagamento, sia opportuno conservare a norma sia la Ricevuta Telematica, sia
la Richiesta di Pagamento Telematico e non anche il Flusso di Rendicontazione.

*Software Development KIT* per applicazioni “mobile”
----------------------------------------------------

Per supportare lo sviluppo di App *mobile* rilasciate dagli Enti Creditori, che includano funzionalità di pagamento, l’Agenzia per l’Italia Digitale
rende disponibile un SDK (Software Development Kit) che consente una rapida integrazione delle funzioni del NodoSPC.

Lo SDK è disponibile in download, previa sottoscrizione di un apposito *disclaimer*, fra gli strumenti GitHub del sito https://developers.italia.it/ e
fornito in modalità nativa per le due principali tecnologie presenti sul mercato: IOS e Android.

SEZIONE II – REGOLE DI FUNZIONAMENTO DEL SISTEMA

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

**Figura 5 – Il processo di gestione dell’avvisatura pull**

Il processo segue i seguenti passi:

-  L’utilizzatore finale accede ad una degli strumenti messi a disposizione dal Prestatore di Servizi di Pagamento richiedendo di conoscere la sua
   (*Task* T1.3.1) posizione debitoria

-  Il Prestatore di servizi di Pagamento inoltra la richiesta all’Ente Creditore attraverso il NodoSPC (*Task* T1.3.2 e T1.3.3)

-  L’Ente Creditore predispone la lista delle Posizione Debitorie relative all’utilizzatore finale (Task T1.3.4) e le inoltra al Prestatore di Servizi
   di Pagamento attraverso il NodoSPC (Task T1.3.5).

-  Il Prestatore di servizi di Pagamento riceve la posizione debitoria dell’Utilizzatore finale e può informarlo (*Task* T1.3.6)

-  L’utilizzatore finale a questo punto ha a disposizione la propria posizione debitoria (*Task* T1.3.7)

Al fine di prevenire utilizzi non consoni, il NodoSPC si riserva la possibilità di applicare apposite regole di *throttling* (limitazioni
nell'utilizzo). Le eventuali regole di *throttling* sono indicate nel documento “\ *Indicatori di qualità per i Soggetti Aderenti*\ ” pubblicato sul
sito istituzionale dell’Agenzia per l’Italia Digitale.

Il Processo di pagamento attivato presso l’Ente Creditore
=========================================================

Rientrano in questa categoria di pagamenti quelli richiesti dall’utilizzatore finale attraverso i siti web o *mobile app* o altri strumenti
tecnologici messi a disposizione dagli Enti Creditori per i pagamenti elettronici. Il processo di pagamento attivato presso l’Ente Creditore consente
di gestire le modalità di incasso sia nel caso in cui l’utilizzatore finale abbia ricevuto un avviso di pagamento, sia nel caso opposto (pagamenti
spontanei)

Le attività a carico degli Enti Creditori per gestire il processo sono rappresentate dalla realizzazione delle procedure di pagamento (sia in termini
organizzativi, che informatici); le procedure di pagamento potranno essere più o meno strettamente integrate con i servizi cui fanno riferimento.

Il diagramma di Figura 8 descrive il processo di pagamento attraverso l’Ente Creditore. Al fine di rendere tale diagramma immediatamente leggibile la
descrizione del *workflow* è stata aggregata in sottoparagrafi secondo lo schema logico che segue (Figura 6).

|image7|

**Figura 6 – Schema logico del processo di business del pagamento presso l’Ente Creditore**

Nel processo in oggetto (Figura 7) sono coinvolti quattro soggetti:

-  utilizzatore finale

-  Ente Creditore

-  NodoSPC

-  Prestatore Servizi di Pagamento dell’utilizzatore finale

|image8|

**Figura 7 – Il processo del pagamento da Ente Creditore**

**Avvio del pagamento**

Come descritto nei paragrafi precedenti, l’utilizzatore finale può eseguire un pagamento per ragioni diverse che generano due diramazioni distinte
(gateway G2.1.1) nel caso abbia disponibile o meno un avviso di pagamento (digitale e analogico).

**Generazione posizione debitoria**

La generazione della posizione debitoria è l’evento che costituisce la premessa al pagamento sul Sistema pagoPA.

In determinate circostanze, previste nello specifico dalla vigente normativa, un soggetto matura un debito in favore di una Pubblica Amministrazione
(centrale o locale). In questo caso lo stesso Ente Creditore assume l’iniziativa di generare una posizione debitoria e provvede a notificare l’avviso
di pagamento al soggetto pagatore. L’EC è altresì tenuto ad accompagnare la notifica con avviso analogico, anche con l’invio al NodoSPC di un avviso
digitale *push*. Questa attività è parte del processo di avvisatura digitale.

Nel caso non sussistano le circostanze sopra indicate per il pagamento dovuto, ovvero l’utilizzatore finale non sia in possesso di un avviso digitale,
lo stesso utilizzatore può assumere l’iniziativa di avviare il pagamento (pagamento spontaneo). In questo caso, se l’utilizzatore finale accede a
portali messi a disposizione dall’Ente Creditore, la posizione debitoria è generata (*Task* T2.1.1). È facoltà dell’EC esporre delle funzioni che
consentono al soggetto pagatore di riceve un avviso digitale (nel caso abbia aderito al servizio) ovvero provveda alla stampa di un avviso analogico,
da utilizzare per disporre il pagamento presso i Prestatori di Servizi di Pagamento che offrono tale opzione.

**Scelta canale di pagamento**

L’utilizzatore finale accede ai sistemi dell’EC per pagare uno o più avvisi che gli sono stati recapitati e/o uno o più pagamenti spontanei e l’Ente
Creditore genera il carrello di richieste di pagamento telematico reindirizzando l’utilizzatore finale sul portale WISP (*Task* T2.1.2).

Il NodoSPC prende in carico il carrello delle richieste di pagamento telematico (*Task* T2.1.3) mentre l’Utilizzatore finale sceglie il Prestatore di
Servizi di Pagamento e il canale di pagamento.

Per gli utilizzatori finali che scelgono di registrarsi al Sistema pagoPA sono a disposizione funzioni di supporto che consentono di memorizzare le
scelte di pagamento effettuate per poterle richiamare e riutilizzare nelle successive occasioni. In questo caso è possibile eleggere una delle scelte
come predefinita così da avere un’esperienza quanto più possibile simile alla modalità *one-click* tipica dei siti di *e-commerce*.

I dati personali raccolti saranno trattati, nel rispetto della normativa vigente, solo per consentire l’erogazione dei servizi richiesti.

Pertanto, detti dati saranno trattati esclusivamente per consentire agli utenti delle pubbliche amministrazioni e degli altri soggetti aderenti al
Sistema pagoPA di richiedere e ottenere i servizi di pagamento erogati dai Prestatori di Servizi di Pagamento abilitati sul Sistema pagoPA, nonché per
richiedere e ottenere parimenti i servizi di identificazione e memorizzazione erogati da AgID sul Sistema pagoPA.

Il conferimento dei dati ed il trattamento degli stessi da parte di AgID per tali finalità è dunque obbligatorio e non richiede un esplicito consenso,
pena l’impossibilità per l’AgID di erogare i servizi sopra citati.

**Autorizzazione del pagamento**

L’autorizzazione del pagamento viene effettuata in maniera differente a seconda del servizio scelto dall’utilizzatore finale:

-  In caso di pagamento con carta di credito o di debito (*Gateway* G2.1.2), l’Utilizzatore finale immette (o recupera nel caso li abbia
   precedentemente memorizzati) i dati della carta (*Task* T2.1.4) e gli viene proposto il pagamento in una *check out page* gestita dal NodoSPC.

..

   Questa tipologia di pagamento prevede che l’autorizzazione del pagamento da parte dell’utilizzatore finale sia inizializzata dal NodoSPC,
   attraverso un proprio POS virtuale. Nel caso che la carta utilizzata sia stata emessa da un Prestatore di servizi di Pagamento aderente al Sistema
   pagoPA, il relativo gestore dell’operazione sarà proposto automaticamente all’utilizzatore finale. Questa casistica è denominata pagamento “on us”.
   Nel caso in cui l’utilizzatore finale non confermi tale scelta ovvero il Prestatore di Servizi di Pagamento emittente della carta non aderisca al
   Sistema pagoPA, l’utilizzatore finale dovrà scegliere il gestore dell’operazione da una lista di Prestatori di servizi di pagamento che mostri i
   costi della commissione richiesta per il servizio. In questo caso si realizza un pagamento “not on us”.

   I Prestatori di Servizi di Pagamento che offrono il servizio di pagamento con carta devono:

-  indicare al NodoSPC le commissioni richiesta per i pagamenti “on us” e i pagamenti “not on us”;

-  Configurare sul NodoSPC le informazioni necessarie a configurare il dialogo tecnico con il POS virtuale con il NodoSPC.

..

   I dettagli delle procedure da seguire sono riportati nella sezione IV.

   Sul portale dell’Ente Creditore devono essere messe a disposizione le funzioni che permettono all’utilizzatore finale di interrogare lo stato della
   sua richiesta di pagamento, scaricare una copia di ricevuta o quietanza di pagamento, scaricare copia analogica e/o duplicato del documento
   informatico Ricevuta Telematica.

-  In caso di pagamento con autorizzazione gestita dal Prestatore Servizi di Pagamento (a cui si assimila anche il pagamento attraverso il circuito
   MyBank, purché sia previsto un pagamento singolo) (*Gateway* G2.1.3), il NodoSPC inoltra in *back-end* il carrello al Prestatore di Servizi di
   Pagamento (o al Wrapper Mybank) (*Task* T2.1.5). Se il canale di pagamento del Prestatore di Servizi di Pagamento lo prevede, l’esperienza utente
   del processo di pagamento può proseguire in un *front-end* gestito dal Prestatore di Servizi di Pagamento (quindi esterno al NodoSPC), prevedendo
   l’identificazione del soggetto versante che autorizza il pagamento (*Task* T2.1.8). In ogni caso, a valle della autorizzazione, l’utilizzatore
   finale viene reindirizzato al *front-end* dell’Ente Creditore da cui aveva avviato il pagamento (*Task* T2.1.9).

..

   Queste tipologie di pagamento prevedono che l’autorizzazione del pagamento da parte dell’utilizzatore finale avvenga mediante l’interazione con
   strumenti messi a disposizione dal Prestatore di Servizi di Pagamento. L’esecuzione del pagamento ed il rilascio della relativa attestazione (RT)
   avvengono in funzione delle modalità di autorizzazione del pagamento adottate dal Prestatore di Servizi di Pagamento. Si distingue quindi
   l’autorizzazione:

-  contestuale alla richiesta effettuata, in funzione dei livelli di servizio pattuiti con il Prestatore di Servizi di Pagamento, se l’utilizzatore
   finale ha pre-autorizzato il pagamento (ad esempio: lettera di manleva o altro strumento contrattuale);

-  non contestuale, se l’autorizzazione viene rilasciata successivamente alla ricezione della richiesta di pagamento telematico da parte del
   Prestatore di Servizi di Pagamento, attraverso canali da questo messi a disposizione (ad esempio: home banking, notifica su app per smartphone o
   tablet, ecc.).

..

   In ogni caso il Prestatore di Servizi di Pagamento deve restituire la ricevuta telematica nei tempi stabiliti secondo quanto previsto nel documento
   “Indicatori di qualità per i soggetti aderenti” pubblicato sul sito istituzionale dell’AgID, in modo da consentire all’utilizzatore finale di
   usufruire dei servizi per cui ha pagato.

   Nel caso di pre-autorizzazione del pagamento, resta salva la possibilità per l’utilizzatore finale di revocare il consenso rilasciato al Prestatore
   di Servizi di Pagamento ad eseguire un’operazione di pagamento, in presenza delle condizioni previste all’articolo 17 del Decreto legislativo n.
   11/2010.

A questo punto, nei casi diversi dall’autorizzazione presso il Prestatore di Servizi di Pagamento, per il quale l’autorizzazione avviene al di fuori
del NodoSPC, l’Utilizzatore finale decide se autorizzare (*Task* T2.1.11):

-  In caso negativo, se il metodo di pagamento scelto era carta di credito (*Gateway* G2.1.7) il NodoSPC genera una ricevuta telematica negativa
   (*Task* T2.1.14), altrimenti è il Prestatore di Servizi di Pagamento che genera la ricevuta telematica negativa (*Task* T2.1.15)

-  In caso positivo, se l’Utilizzatore effettua il pagamento con carta (*Gateway* G2.1.6) il NodoSPC inoltra la richiesta di pagamento telematico al
   Prestatore Servizi di Pagamento (*Task* T2.1.12), altrimenti il Prestatore Servizi di Pagamento incassa il pagamento (*Task* T2.1.12)

Una volta effettuato l’incasso il Prestatore Servizi di Pagamento genera la ricevuta telematica, redirezionando sul sito dell’Ente Creditore in caso
di carta di credito, (*Task* 2.1.16) e la trasmette al NodoSPC (*Task* T2.17).

Il NodoSPC mette la ricevuta telematica a disposizione del’Ente Creditore (*Task* 2.1.17) che a sua volta può mettere a disposizione dell’Utilizzatore
finale una ricevuta (*Task* T2.18).

L’Utilizzatore finale a questo punto può ottenere la ricevuta (Task T2.1.19) e terminare il processo.

**Accredito e rendiconto**

Dopo aver effettuato il pagamento, il Prestatore Servizi di Pagamento lo accredita sul conto dell’Ente Creditore (*Task* T2.1.20).

Il Prestatore Servizi di Pagamento invia i dati relativi alla rendicontazione al NodoSPC (*Task* T2.1.21).

Il NodoSPC trasmette i dati di rendicontazione all’Ente Creditore (*Task* T2.1.22), che li riceve (*Task* T2.1.23).

Processo di pagamento attivato presso il Prestatore di Servizi di Pagamento
===========================================================================

Questo processo prevede che l’esecuzione del pagamento avvenga presso le infrastrutture messe a disposizione dal Prestatore di Servizi di Pagamento
quali, ad esempio, sportelli ATM, applicazioni di *Home banking* e *mobile* *payment*, uffici postali, punti della rete di vendita dei generi di
Monopolio (Tabaccai), SISAL e Lottomatica, casse predisposte presso la Grande Distribuzione Organizzata, ecc.

L’Ente Creditore che consente il pagamento deve mettere a disposizione dei Prestatori di Servizi di Pagamento, attraverso il NodoSPC, un archivio nel
quale siano già stati memorizzati i pagamenti predisposti dall’ente (Archivio Pagamenti in Attesa).

Per rendere possibile il pagamento l’Ente Creditore ha l’obbligo di recapitare all’utilizzatore finale un avviso con gli estremi del pagamento da
effettuare. Tale recapito deve obbligatoriamente avvenire sia in modalità analogica (tramite servizi postali), che digitale. L’Ente Creditore può
inoltre adottare ulteriori misure per la diffusione degli avvisi di pagamento, per esempio rendere disponibili funzioni di stampa on line tramite il
proprio sito.

Il processo di pagamento descritto di seguito, supporta principalmente la modalità di incasso su iniziativa dell’Ente Creditore, ma può essere
utilizzato anche per gestire la modalità di incasso su iniziativa del debitore, atteso che, sul proprio portale, l’Ente Creditore metta a disposizione
dell’utilizzatore finale la possibilità di eseguire pagamenti presso gli sportelli dei Prestatori di Servizi di Pagamento generando a richiesta del
debitore, un avviso di pagamento utilizzabile all’uopo.

Anche il modello di pagamento in esame può essere utilizzato dall’utente per tutti quei servizi per i quali non è necessario disporre in via immediata
dell’attestazione di pagamento, che può essere esibita in un momento successivo.

Nello schema di Figura 10 è trattato il caso in cui l’utilizzatore finale, già in possesso dell’avviso di pagamento analogico fornito dall’Ente, si
rechi presso le strutture del Prestatore di Servizi di Pagamento e comunichi il codice dell'avviso di pagamento. Si tenga presente che il caso d’uso
descritto non dipende dalla concreta modalità in cui tale dato entra in possesso del Prestatore di Servizi di Pagamento: il codice potrebbe essere
comunicato a un operatore di sportello, letto automaticamente tramite dispositivi ottici, inserito manualmente dal soggetto versante su interfacce
messe a disposizione dai Prestatori di Servizi di Pagamento (un terminale ATM, una pagina WEB, ecc.), ovvero, da ultimo, comunicato tramite avviso
digitale.

Il diagramma di Figura 10 descrive il processo pagamento operato presso il Prestatore di Servizi di Pagamento. Al fine di rendere tale diagramma
immediatamente leggibile la descrizione del *workflow* è stata aggregata in paragrafi secondo lo schema logico che segue (Figura 8).

|image9|

**Figura 8 – Schema logico del processo di business del pagamento presso il Prestatore di Servizi di Pagamento**

Nel processo in oggetto (Figura 9) sono coinvolti quattro soggetti:

-  Utilizzatore finale

-  Ente Creditore

-  NodoSPC

-  Prestatore Servizi di Pagamento dell’Utilizzatore finale

|image10|

**Figura 9 – Il processo del pagamento attivato presso il Prestatore di Servizi di Pagamento**

Avvio del pagamento
-------------------

Come descritto nei paragrafi precedenti, l’Utilizzatore finale può eseguire un pagamento per ragioni diverse, che generano due diramazioni distinte
(gateway G2.2.1), nel caso che abbia disponibile o meno un avviso di pagamento (digitale e analogico).

Generazione posizione debitoria
-------------------------------

La generazione della posizione debitoria è l’evento che costituisce la premessa al pagamento sul Sistema pagoPA.

In determinate circostanze, previste nello specifico dalla vigente normativa, un soggetto matura un debito in favore di una Pubblica Amministrazione
(centrale o locale). In questo caso lo stesso Ente Creditore assume l’iniziativa di genera una posizione debitoria e provvede a notificare l’avviso di
pagamento al soggetto pagatore. L’EC è altresì tenuto ad accompagnare la notifica con avviso analogico, anche con l’invio al NodoSPC di un avviso
digitale *push*. Questa attività è parte del processo di avvisatura digitale.

Nel caso in cui non sussistano le circostanze sopra indicate per il pagamento dovuto, ovvero l’Utilizzatore finale non sia in possesso di un avviso
digitale, l’Utilizzatore stesso può assumere l’iniziativa di avviare il pagamento (pagamento spontaneo), purché sia disponibile la relativa funzione.
In questo caso l’Utilizzatore finale accede a portali messi a disposizione dal Prestatore di Servizi di Pagamento e quest’ultimo richiede all’Ente
Creditore la generazione della posizione debitoria (*Task* T2.2.1). L’Ente Creditore risponde con l’invio al Prestatore Servizi di Pagamento di un
numero avviso (*Task* T2.2.2) che può essere consegnato all’Utilizzatore (Task T2.2.3) che dunque può decidere se autorizzare (*Task* T2.2.8).

Verifica posizione debitoria e attivazione richiesta di pagamento telematica
----------------------------------------------------------------------------

Nel caso in cui l’Utilizzatore finale abbia ricevuto un avviso di pagamento e abbia deciso di pagare tramite un Prestatore Servizi di Pagamento,
quest’ultimo, prima di effettuare il pagamento, può verificare la posizione debitoria utilizzando la specifica funzione, per accertarsi che il
pagamento non sia stato saldato e/o i termini siano rimasti invariati (per esempio potrebbe essere variato l’importo a causa di interessi di mora)

Allorché il Prestatore Servizi di Pagamento chiede la verifica della posizione debitoria (*Gateway* G2.2.3), l’Ente Creditore risponde (Task T2.2.5)
con i dati previsti riguardo lo stato della posizione debitoria, nonché le possibili variazioni dell'importo dovute ad eventi successivi all'invio
dell'Avviso analogico, ad esempio il superamento della data di scadenza del pagamento). L’invocazione della funzione di verifica non ha effetti sullo
stato della posizione debitoria.

In caso di sussistenza della posizione debitoria l’Utilizzatore finale può decidere se pagare o meno (*Gateway* G2.2.2).

-  Se decide di pagare, allora viene attivata la richiesta di pagamento telematico (*Task* T2.2.7)

-  In caso contrario il processo termina (*Task* T2.2.4)

Il Prestatore Servizi di Pagamento può, viceversa, invocare direttamente l’attivazione della richiesta di pagamento telematico (*Task* T2.2.6),
peraltro comprendente la verifica della posizione debitoria.

L’Ente Creditore esegue l’attivazione della richiesta di pagamento telematico (*Task* T2.2.7.

Il processo si svolge poi diversamente nei casi in cui l’Utilizzatore finale ha effettuato o meno il pagamento prima che il Prestatore di Servizi di
Pagamento richiedesse l’attivazione della richiesta di pagamento telematico (*Gateway* G2.2.6).

Nel caso che l’Utilizzatore finale non abbia ancora pagato, deve decidere se autorizzare il pagamento (*Gateway* G2.2.4):

-  In caso negativo, se non esisteva ancora una richiesta di pagamento telematico attiva (*Gateway* G2.2.7) è perché il Prestatore di Servizi di
   Pagamento aveva richiesto la verifica della posizione debitoria, quini il processo termina, altrimenti il Prestatore di Servizi di Pagamento genera
   una ricevuta telematica negativa (*Task* T2.2.10)

-  In caso positivo il Prestatore Servizi di Pagamento incassa il pagamento (*Task* T2.2.9)

Una volta effettuato l’incasso (*Task* T2.2.9) il Prestatore Servizi di Pagamento genera la ricevuta telematica positiva (*Task* T2.2.11) se aveva già
ricevuto una richiesta di pagamento telematico attivata (*Gateway* G2.2.5), perché lo aveva richiesto, altrimenti richiede la attivazione della
richiesta di pagamento telematico (*Task* T2.2.6) che viene generata dall’Ente Creditore (*Task* T2.2.7) e solo a questo punto il Prestatore Servizi
di Pagamento può generare la ricevuta telematica positiva (*Task* T2.2.11).

Nel caso di emissione di ricevuta telematica positiva il Prestatore di Servizi di Pagamento consegna all’Utilizzatore finale un’attestazione di
pagamento, contenente le informazioni specificate nella sezione III. Tale attestazione è opponibile all’EC.

Le ricevute telematiche sia positive che negative vengono trasmesse al NodoSPC.

Il NodoSPC mette la ricevuta telematica a disposizione dell’Ente Creditore (*Task* 2.2.12) che a sua volta può mettere a disposizione
dell’Utilizzatore finale una ricevuta (*Task* T2.2.13).

L’Utilizzatore finale a questo punto può ottenere la ricevuta (Task T2.2.14) e terminare il processo.

Trasmissione dati di accredito e rendicontazione
------------------------------------------------

Dopo aver effettuato il pagamento, il Prestatore Servizi di Pagamento accredita il conto dell’Ente Creditore specificato dalla richiesta di pagamento
telematico ed invia al NodoSPC i dati relativi alla ricevuta telematica accreditata (*Task* T2.2.15

Nel caso che in cui venga effettuato un accredito cumulativo il Prestatore Servizi di Pagamento invia i dati relativi alla rendicontazione al NodoSPC
(*Task* T2.2.16).

Il NodoSPC mette a disposizione i dati di rendicontazione per l’Ente Creditore (*Task* T2.2.17). Quando l’Ente Creditore scarica i dati di
rendicontazione (*Task* T2.2.18).

Attivazione della richiesta di pagamento 
-----------------------------------------

Il NodoSPC non controlla l’effettiva sequenza operativa scelta dal Prestatore di Servizi di Pagamento, relativa alle fasi del processo descritte in
precedenza: pertanto, un Prestatore di Servizi di Pagamento potrebbe effettuare la richiesta di attivazione della richiesta di pagamento telematico
senza aver preventivamente effettuato la fase di verifica. Con questo approccio è sconsigliato far precedere l’incasso alla richiesta di attivazione
della richiesta di pagamento telematico (*Task* T2.2.6), in quanto sul Sistema pagoPA non è gestito automaticamente il caso in cui l'Ente Creditore
non riesca a inviare la richiesta di pagamento telematico prevista dal *workflow*: per esempio, nel caso in cui il pagamento sia già stato eseguito
con un altro canale oppure perché l'importo dovuto sia diverso da quello stampato sull'avviso.

In questo caso il Prestatore di Servizi di Pagamento avrebbe incassato dei fondi ai quali non può essere associata una Ricevuta Telematica da inviare
all'Ente Creditore. Per questo caso, nella sezione III, sono previste delle gestioni semi-manuali. A tal proposito si ricorda che, ai sensi delle
Linee guida, i pagamenti effettuati attraverso il NodoSPC sono liberatori del debito a condizione che la Ricevuta Telematica sia congruente con le
informazioni presenti sulla relativa richiesta di pagamento telematico e quindi sull'archivio dei pagamenti in attesa.

Funzioni accessorie
===================

Revoca della Ricevuta Telematica
--------------------------------

Qualora l’utilizzatore finale - ai sensi degli articoli 13 e 14 del decreto legislativo 27 gennaio 2010, n. 11, ovvero per richieste regolamentate
connesse all’utilizzo di carte di pagamento (c.d.: procedura di *charge back*, nella quale non rientrano i casi di frode ma unicamente i casi in cui
l’Utilizzatore finale richieda un rimborso per un pagamento effettuato a fronte di un servizio di cui non ha usufruito) chieda al proprio prestatore
di servizi di pagamento il rimborso di un pagamento già completato, il Sistema pagoPA mette a disposizione di Prestatori di Servizi di Pagamento e
Enti Creditori idonee funzionalità per gestire la revoca della ricevuta telematica inviata in precedenza.

Come indicato in Figura 10, la revoca della ricevuta telematica si esplica nell’invio di una richiesta di revoca (RR) da parte del Prestatore di
Servizi di Pagamento, contenente i riferimenti della ricevuta telematica oggetto della revoca e nella risposta da parte dell’Ente Creditore contenente
l’esito della revoca (ER).

|image11|

**Figura 10 – Il processo di revoca**

Il processo è iniziato dall’Utilizzatore finale, che richiede la revoca al proprio Prestatore di Servizi di Pagamento (*Task* T3.1), a seguito della
quale quest’ultimo inoltra la richiesta all’Ente Creditore (*Task* T3.2) attraverso il NodoSPC (*Task* T3.3).

L’Ente Creditore esamina la richiesta (*Gateway* G3.1):

-  L'Ente Creditore non consente la revoca di una ricevuta telematica se il pagamento associato è contestuale all'erogazione di un servizio (ad
   esempio: acquisto di biglietti per musei o trasporti pubblici, prestazioni sanitarie già eseguite, ecc.) inviando un ER di esito negativo (*Task*
   T3.4) che viene trasmesso dal NodoSPC al Prestatore di servizi di Pagamento (*Task* T3.5) e da questi all’Utilizzatore finale (*Task* T3.6) che
   apprende l’esito (*Task* T3.5)

-  In caso contrario l’Ente Creditore, entro tempi compatibili con il procedimento richiesto, esamina la richiesta e invia l'esito della revoca,
   aggiornando i propri archivi informatici e riaprendo la posizione debitoria se necessario (*Task* T3.8). L’esito positivo è trasmetto dal NodoSPC
   al Prestatore di Servizi di Pagamento (*Task* T3.9), il quale esegue il riaccredito verso l’Utilizzatore finale (*Task* T3.10), il quale lo riceve
   direttamente senza l’intervento del NodoSPC (*Task* T3.7). Il Prestatore di servizi di Pagamento recupera la somma dovuta compensandola sui
   successivi accrediti da effettuare verso l’Ente Creditore ed espone la cifra (negativa) sul successivo rendiconto (*Task* T3.11), che viene
   trasmesso all’Ente Creditore attraverso il NodoSPC (*Task* T3.12). A questo punto l’Ente Creditore è in grado di riconciliare correttamente gli
   importi (*Task* T3.13)

In ogni caso, l’Ente Creditore deve predisporre - e darne evidenza sul proprio sito attraverso il quale sono effettuati i pagamenti - apposite
procedure amministrative di back-office al fine di gestire, nel rispetto della normativa vigente, i flussi relativi a reclami, rimborsi e revoche sia
dal punto di vista amministrativo, sia dal punto di vista contabile.

Annullo tecnico
---------------

L’annullo tecnico è una casistica dell’invio di una richiesta di revoca che indica che la RT inviata è tecnicamente errata, dunque il Prestatore di
Servizi di Pagamento può invocarla unicamente ricorra uno dei seguenti casi di errori procedurali:

a) Invio di una Ricevuta Telematica (RT) con esito **positivo**, tuttavia l’utilizzatore finale non ha ricevuto nessun addebito né il Prestatore di
      Servizi di Pagamento ha emesso alcuna attestazione di pagamento (scontrino, ricevuta, e-mail, ecc.);

b) Invio di una Ricevuta Telematica (RT) con esito **negativo**, tuttavia l’utilizzatore finale ha ricevuto un addebito e il Prestatore di Servizi di
      Pagamento ha emesso un’attestazione di pagamento (scontrino, ricevuta, e-mail, ecc.)

Al di fuori delle circostanze sopra descritte l’utilizzo dell’annullo tecnico non è ammesso.

Il processo di annullo tecnico, descritto in Figura 11, è il seguente

|image12|

**Figura 11 – Processo di annullo tecnico**

Il Prestatore di servizi di Pagamento invia la richiesta di annullo tecnico al NodoSPC (*Task* T4.1), che verifica la casistica del caso (*Gateway*
G4.1):

-  Nel caso in cui sia stata inviata una ricevuta telematica positiva senza l’avvenuto pagamento, il nodo aggiorna lo stato del pagamento ed invia
   l’informazione all’Ente Creditore (*Task* T4.2), il quale aggiorna i suoi archivi informatici (*Task* T4.4)

-  Nel caso in cui sia stata inviata una ricevuta telematica negativa a fronte di un avvenuto pagamento, in NodoSPC invia l’informazione di effettuare
   l’annullo tecnico (*Task* T4.3) sia all’Ente Creditore, in quale aggiorna i propri archivi informatici (*Task* T4.4), che al Prestatore di servizi
   di Pagamento, il quale può procedere all’invio dell’accredito (*Task* T4.6), che viene ricevuto dall’Ente Creditore (*Task* T4.8) attraverso il
   NodoSPC (*Task* T4.7), che all’inoltro della rendicontazione (*Task* T4.9), che viene anch’esso ricevuto dall’Ente Creditore (*Task* T4.11)
   attraverso il NodoSPC (*Task* T4.10)

Storno del pagamento 
---------------------

Qualora l’Utilizzatore finale chieda a vario titolo l’annullamento (storno) di un pagamento all’Ente Creditore presso il quale questo è stato
disposto, il sistema mette a disposizione dell’Ente Creditore e del Prestatore di Servizi di Pagamento idonee funzionalità del NodoSPC per gestire
detta operazione.

L’Ente Creditore deve predisporre - e darne evidenza sul proprio sito attraverso il quale sono effettuati i pagamenti - apposite procedure
amministrative di back-office al fine di gestire, nel rispetto della normativa vigente, le richieste di storno del pagamento ed i relativi flussi
economici.

|image13|

**Figura 12 – Processo di storno di un pagamento**

Il processo di storno viene iniziato dall’Utilizzatore finale che lo richiede all’Ente Creditore (*Task* T5.1)

L’Ente Creditore esamina la richiesta (*Gateway* G5.1):

-  In caso di esito negativo, l'Ente Creditore comunica l’informazione all’Utilizzatore finale (*Task* T5.2) che apprende l’esito (*Task* T5.3)

-  In caso contrario l’Ente Creditore, entro tempi compatibili con il procedimento richiesto, esamina la richiesta e invia l'esito dello storno,
   aggiornando i propri archivi informatici e riaprendo la posizione debitoria se necessario (*Task* T5.4). L’esito positivo è trasmesso dal NodoSPC
   al Prestatore di Servizi di Pagamento (*Task* T5.5), il quale esegue il riaccredito verso l’Utilizzatore finale (*Task* T5.6) che lo riceve
   direttamente senza l’intervento del NodoSPC (*Task* T5.7). Il Prestatore di Servizi di Pagamento recupera la somma dovuta compensandola sui
   successivi accrediti da effettuare verso l’Ente Creditore ed espone la cifra (negativa) sul successivo rendiconto (*Task* T5.8) che viene trasmesso
   all’Ente Creditore attraverso il NodoSPC (*Task* T5.8). A questo punto l’Ente Creditore è in grado di riconciliare correttamente gli importi
   (*Task* T5.10)

Attestazione del pagamento 
---------------------------

L’attestazione di avvenuto pagamento è rappresentata dal documento informatico (Ricevuta Telematica) che l’Ente Creditore riceve dal Prestatore di
Servizi di Pagamento.

L’Ente Creditore deve rendere disponibile, su richiesta dell’utilizzatore finale, tale documento, sia sotto forma di duplicato informatico che sotto
forma di copia analogica dello stesso. Poiché nelle ricevute telematiche possono essere contenuti da 1 a 5 pagamenti aventi lo stesso ente
beneficiario, sarà cura dell’Ente Creditore, se del caso, produrre tante copie analogiche quanti sono i pagamenti effettuati contenuti nella stessa
ricevuta telematica.

Nel caso di pagamento attivato presso il Prestatore di Servizi di Pagamento, questi fornisce direttamente all’Utilizzatore finale un documento
(ricevuta, scontrino, ecc.) che rappresenta un estratto analogico del documento informatico che il Prestatore di Servizi di Pagamento invierà
successivamente all’Ente Creditore. Tale documento può essere utilizzato dall’Utilizzatore finale per ottenere quietanza da parte dell’EC.

Le copie analogiche prodotte dall’Ente Creditore o dai Prestatori di Servizi di Pagamento devono necessariamente contenere, oltre al logo del Sistema
pagoPA, almeno le seguenti informazioni:

-  Data e ora dell’operazione

-  Codice fiscale e denominazione dell’Ente Creditore

-  Identificativo univoco versamento (IUV) - Identificativo univoco assegnato dall’Ente Creditore

-  Codice identificativo del Prestatore di Servizi di Pagamento

-  Numero univoco assegnato al pagamento dal Prestatore di Servizi di Pagamento

-  Importo dell’operazione

-  Causale del versamento indicata nella richiesta di pagamento telematico.

Riconciliazione dei pagamenti
-----------------------------

Con rifermento alle macro-fasi del processo, una volta effettuata la fase di “Regolamento contabile” da parte del Prestatore di Servizi di Pagamento,
l’Ente Creditore provvede a riconciliare le ricevute telematiche (RT) con le informazioni contabili fornite dal proprio istituto tesoriere o da Poste
Italiane in relazione agli incassi avvenuti sui c/c postali (ad esempio: Giornale di Cassa per le Pubbliche Amministrazioni che utilizzano il formato
OIL/OPI; altre modalità per le Pubbliche Amministrazioni centrali che possono richiedere tali informazioni alla Ragioneria Generale dello Stato).

Secondo quanto indicato dalle Linee guida e dal suo Allegato A *"Specifiche attuative dei codici identificativi di versamento, riversamento e
rendicontazione*", il Prestatore di Servizi di Pagamento che riceve l’ordine dal proprio cliente o che esegue l’incasso per conto dell’Ente Creditore
può regolare contabilmente l’operazione in modalità singola o in modalità cumulativa, il che comporta per l’Ente Creditore due diverse modalità di
riconciliazione.

**Riconciliazione in modalità singola**

Qualora, a fronte di ogni singolo set di informazioni contenuto in una richiesta di pagamento, il Prestatore di Servizi di Pagamento effettui una
singola disposizione di pagamento nei confronti dell’Ente Creditore per regolare contabilmente l’operazione (ad esempio: l’utilizzo della forma
tecnica “bonifico di tesoreria”), si parla di riconciliazione in modalità singola.

L’operazione di riconciliazione in modalità singola viene effettuata dall’Ente Creditore sulla base della seguente coppia di informazioni presenti
sulla ricevuta telematica inviata dal Prestatore di Servizi di Pagamento all’Ente Creditore:

-  Identificativo univoco versamento (IUV) che deve coincidere con la componente identificativo univoco versamento della causale della disposizione di
   accredito inviata al Prestatore di Servizi di Pagamento dall’Ente Creditore, secondo le indicazioni di cui alla Sezione I dell’Allegato A alle
   Linee guida;

-  ì-esima occorrenza del dato relativo al singolo importo pagato della Ricevuta Telematica che deve coincidere con il dato presente nell’informazione
   della disposizione di accredito inviata al Prestatore di Servizi di Pagamento dall’Ente Creditore.

**Riconciliazione in modalità multipla**

Qualora il Prestatore di Servizi di Pagamento effettui un’unica disposizione cumulativa di pagamento nei confronti dell’Ente Creditore per regolare
contabilmente i pagamenti relativi agli esiti contenuti in una o più ricevute telematiche, si parla di Riconciliazione in modalità multipla che viene
effettuata dall’Ente Creditore sulla base dei dati forniti dal proprio istituto tesoriere e di quelli contenuti nel flusso di rendicontazione che il
Prestatore di Servizi di Pagamento deve inviare all’Ente Creditore stesso.

La riconciliazione in questo caso deve essere effettuata in due fasi:

-  nella prima fase il dato identificativo del flusso - presente nella causale del SEPA Credit Transfer inviato dal Prestatore di Servizi di Pagamento
   all’Ente Creditore - deve essere abbinato con quello presente nel Flusso di rendicontazione inviato all’Ente Creditore dal Prestatore di Servizi di
   Pagamento che ha eseguito i pagamenti.

-  Nella seconda fase della riconciliazione l’Ente Creditore abbinerà i dati contenuti nel Flusso di rendicontazione di cui sopra con i dati presenti
   nelle ricevute telematiche (RT) memorizzate presso di sé sulla base della seguente coppia di informazioni:

a. Identificativo univoco versamento presente sulla ricevuta telematica inviata all’Ente Creditore che deve coincidere con lo stesso dato presente
   nella struttura dati del Flusso di rendicontazione;

b. importo presente sulla ricevuta telematica inviata all’Ente Creditore che deve coincidere con il dato omonimo presente nella struttura dati del
   Flusso di rendicontazione.

Il NodoSPC fornisce apposite funzioni centralizzate a disposizione dei Prestatori di Servizi di Pagamento e degli Enti Creditori, con le quali i primi
possono inviare il Flusso di rendicontazione e gli altri ricevere i dati ivi contenuti.

**Pagamento contenente più accrediti**

Qualora l’utilizzatore finale presenti al Prestatore di Servizi di Pagamento una RPT contenente più pagamenti ovvero presenti un “carrello” di
richieste di pagamento telematico aventi più beneficiari, il Prestatore di Servizi di Pagamento deve effettuare un unico addebito verso l’Utilizzatore
finale al quale attribuisce lo stesso identificativo univoco di riscossione: pertanto l’Ente Creditore dovrà opportunamente tenerne conto nelle
proprie procedure applicative di riconciliazione.

Altre funzioni accessorie
-------------------------

Seppur meno utilizzate nella pratica comune, si citano di seguito alcune ulteriori funzione accessorie messe a disposizione dal Sistema pagoPA:

-  Richiesta di una copia della ricevuta telematica

-  Richiesta dell’elenco delle richieste di pagamento telematico pendenti

-  Gestione della ricevuta telematica di notifica decorrenza termini

I dettagli relativi alle suddette funzioni sono riportati nella sezione III

componenti tecniche del NodoSPC
===============================

Il NodoSPC definisce modalità standard per la gestione dei flussi finanziari:

-  adotta gli standard XML ISO 20022 per i tracciati dei flussi finanziari correlati alle singole operazioni;

-  introduce uno standard per la richiesta di pagamento telematico e per la ricevuta telematica di pagamento adottato a livello nazionale su qualunque
      canale di pagamento, al fine di automatizzare la tratta G2B (*Government to Bank*);

-  nell’ambito delle attività legate al commercio elettronico abilita l’interconnessione con i circuiti internazionali di autorizzazione di tali
      pagamenti;

-  assicura l’univocità del pagamento attraverso la definizione di un codice identificativo del pagamento (IUV). Al suddetto identificativo può essere
      associato uno o più oggetti grafici (codice a barre, glifo, QR-code, ecc.), al fine di consentire e facilitare l’effettuazione del pagamento
      attraverso qualunque canale oggi esistente;

-  de-materializza tutte le ricevute di pagamento restituite all’Ente Creditore;

-  de-materializza gli avvisi di pagamento.

Nella Figura 13 sono evidenziate le componenti ed i soggetti che interagiscono tra di loro per consentire lo svolgersi del processo di pagamento
telematico secondo i modelli descritti in precedenza.

|image14|

**Figura 13 – Schema architetturale del Sistema pagoPA**

Gestore del Workflow Applicativo
--------------------------------

È la macro-componente principale che ha lo scopo di coordinare l’esecuzione delle richieste di servizio, richiamando componenti di utilità (quali ad
esempio, il modulo per la diagnostica) ed interfacciare l’infrastruttura di Rete SPC.È la macro-componente principale che ha lo scopo di coordinare
l’esecuzione delle richieste di servizio, richiamando componenti di utilità quali ad esempio, il modulo per la diagnostica, e di interfacciare
l’infrastruttura di Rete.

Il Gestore del *Workflow* Applicativo interfaccia sia le applicazioni degli Enti Creditori da cui provengono le richieste di servizio e a cui devono
essere indirizzate le relative risposte applicative, sia i Prestatori di Servizi di Pagamento che abilitano il pagamento sui diversi canali.

Comprende vari agenti software tra cui i principali sono quelli che permettono:

-  la gestione del “Giornale degli Eventi” dove sono registrati - per ogni operazione - tutti gli scambi necessari alla corretta esecuzione del
      processo;

-  la gestione del “Tavolo Operativo” dove sono monitorati tutti i componenti del sistema e lo stato di esecuzione delle operazioni;

-  l’indirizzamento ai singoli servizi e/o sotto-servizi in funzione delle richieste e delle risposte previste dai diversi modelli di funzionamento;

-  la memorizzazione e la gestione delle “richieste di servizio” per la tracciatura delle operazioni e la gestione delle eccezioni;

-  la gestione degli errori;

-  il mantenimento del sincronismo temporale.

Gestore della Connessione
-------------------------

La connessione al NodoSPC in applicazione al vigente modello di interoperabilità avviene nelle forme e nei metodi descritti nel documento collegato
“Specifiche di Connessione al sistema pagoPA”, pubblicato sul sito istituzionale di AgID.

 Gestore della Porta di Dominio
-------------------------------

Questa componente, deprecata e mantenuta per retro compatibilità, si occupa dello scambio dei messaggi da e verso SPC per il colloquio con l’Ente
Creditore secondo gli accordi di servizio stabiliti dalle regole tecniche SPCoop e pubblicati sui registri SICA. In coerenza con le logiche SPCoop,
permette di reindirizzare i messaggi alle Pubbliche Amministrazioni aderenti a SPC anche in via indiretta attraverso le reti territoriali,
eventualmente per mezzo di soggetti intermediari.

Tra le principali attività svolte dalla componente si richiamano, a titolo esemplificativo:

-  incapsulamento delle chiamate dei metodi *Web service*, rendendole disponibili in forma mediata verso la Porta di Dominio;

-  memorizzazione temporanea e trattamento, secondo la priorità indicata, dei messaggi verso la Porta di Dominio;

-  tracciamento dei riferimenti univoci dei messaggi;

-  trattamento degli header dei messaggi scambiati via Porta di Dominio ai fini della correlazione applicativa attuata dalla Porta di Dominio stessa;

-  gestione degli errori e delle conferme di natura trasmissiva;

-  generazione e propagazione dei messaggi d’errore di natura applicativa;

-  mantenimento di un proprio registro degli eventi finalizzato all’aggiornamento del Giornale degli Eventi;

-  mantenimento del sincronismo temporale.

Interfaccia di Canale
---------------------

Le attività svolte da questa componente sono analoghe a quelle svolte dal gestore della Porta di Dominio per gli Enti Creditori, ma istanziate per il
rapporto con i singoli Prestatori di Servizi di Pagamento. A tale scopo, il NodoSPC espone una modalità standard di colloquio verso i Prestatori di
Servizi di Pagamento, descritta nella Sezione IV. Nel caso di peculiari modalità tecnico trasmissive richieste dai Prestatori di Servizi di Pagamento,
sempre che di validità generale, possono essere realizzate allo scopo specifiche interfacce software.

Qualora il Prestatore di Servizi di Pagamento lo richieda, la componente permette di interfacciare il Prestatore di Servizi di Pagamento attraverso un
intermediario (soggetto giuridico o circuito) scelto dallo stesso Prestatore di Servizi di Pagamento. Tutti gli oneri derivanti sono a carico del
Prestatore di Servizi di Pagamento che mantiene la titolarità del rapporto con il NodoSPC.

Di seguito le principali attività svolte dalla componente:

-  incapsulamento delle chiamate al fine di renderle disponibili in forma mediata verso gli specifici canali;

-  memorizzazione temporanea dei messaggi applicativi verso i canali;

-  tracciamento dei riferimenti univoci dei messaggi memorizzati/inviati;

-  gestione degli errori e delle conferme di natura trasmissiva;

-  generazione e propagazione dei messaggi d’errore di natura applicativa;

-  mantenimento di un proprio registro degli eventi finalizzato all’aggiornamento del Giornale degli Eventi;

-  mantenimento del sincronismo temporale.

Repository ricevute telematiche
-------------------------------

Il *Repository* costituisce l’archivio in cui sono memorizzate tutte le ricevute telematiche processate dal NodoSPC e non ancora consegnate,
finalizzato al buon funzionamento del sistema.

Il *Repository* consente una verifica in merito al corretto trattamento dei flussi di pagamento del NodoSPC.

Componente Web-FESP
-------------------

La componente “Web-FESP” permette di effettuare il pagamento reindirizzando l’Utilizzatore finalee verso una *landing page* messa a disposizione dal
Prestatore di Servizi di Pagamento.

In questo caso:

-  il Prestatore di Servizi di Pagamento consente all’Utilizzatore finale di eseguire il pagamento con i diversi strumenti di pagamento;

-  la componente Web-FESP agisce da normalizzatore e provvede ad uniformare le informazioni ricevute, re-inviandole attraverso il NodoSPC all’Ente
      Creditore per consentire di completare l’operazione di pagamento.

Componente WISP
---------------

La componente “WISP” (*Wizard* Interattivo di Scelta del Prestatore di Servizi di Pagamento) consente all'utilizzatore finale di effettuare la scelta
del Prestatore di Servizi di Pagamento in modalità accentrata presso il NodoSPC, che mette a disposizione apposite pagine che standardizzano a livello
nazionale la *user experience* dei pagamenti verso la Pubblica Amministrazione, garantendo ai Prestatori di Servizi di Pagamento aderenti che
l'esposizione dei servizi da loro offerti sia proposta all'Utilizzatore finale attraverso schemi che consentano pari opportunità di trattamento,
concorrenza e non discriminazione.

La componente WISP inoltre fornisce all’Utilizzatore finale funzioni di supporto introducendo vari accorgimenti per semplificare la *user experience*,
anche nel caso di pagamento con dispositivi mobili. Inoltre l’Utilizzatore finale potrà memorizzare gli strumenti di pagamento utilizzati, evitando di
dover effettuare una nuova ricerca nelle occasioni successive.

Componente Wrapper MyBank 
--------------------------

Nell'ambito del collegamento tra il NodoSPC ed il circuito *e-commerce* MyBank, la componente "Wrapper MyBank" si occupa di effettuare le necessarie
conversioni di tracciati e di gestire il colloquio tra il NodoSPC e la componente *Initiating Party* messa a disposizione dalla *Seller Bank*,
rendendo possibile l’inoltro della richiesta di pagamento alla *Buyer Bank* ed il ritorno dell'esito del pagamento stesso.

In tale contesto, le *Seller Bank* aderenti al NodoSPC sono tenute ad utilizzare le specifiche di interfacciamento della componente “Wrapper MyBank”.

Componente per la gestione dell'avvisatura digitale in modalità push 
---------------------------------------------------------------------

La gestione dell'avvisatura digitale in modalità *push* avviene attraverso l'utilizzo di componenti del NodoSPC che consentono:

-  agli Enti Creditori l'invio degli avvisi sia in modalità SFTP (File transfer sicuro), sia attraverso l'utilizzo di appositi *web service*;

-  ai Prestatore di Servizi di Pagamento di inviare via *web service* al NodoSPC le richieste di iscrizione al servizio;

-  al NodoSPC di:

   -  inviare gli avvisi digitali ai Prestatori di Servizi di Pagamento via *web service*;

   -  inviare gli avvisi digitali agli Utilizzatori finali tramite e-mail (protocollo SMTP);

   -  notificare ai servizi di Cittadinanza Digitale gli avvisi digitali (predisposizione per funzionalità future).

File Transfer sicuro
--------------------

Il NodoSPC mette a disposizione dei soggetti aderenti una piattaforma *client-server* per il trasferimento sicuro dei dati in modalità *File
Transfer*. Tale piattaforma sostituirà progressivamente l'utilizzo delle primitive oggi impiegate per lo scambio di informazioni in modalità massiva
(ad esempio: i flussi di rendicontazione, i totali di traffico, ecc.).

Giornale degli Eventi
---------------------

È la componente che raccoglie tutte le informazioni attinenti ad ogni singola operazione sintetizzando le registrazioni effettuate dalle singole
componenti del NodoSPC: FESP; Web FESP; *Repository*, ecc.

Le principali attività svolte dalla componente riguardano:

-  la raccolta delle informazioni attinenti alle operazioni svolte dalle componenti del NodoSPC, come ad esempio:

-  tipo di operazione (RPT; RT; …),

-  identificativo univoco associato all’operazione,

-  *timestamp* dell’evento e della registrazione,

-  componente in cui si verifica l’evento (FESP; Web-FESP; *Repository*);

-  esposizione di un’interfaccia di interrogazione per l’accesso alle registrazioni degli eventi che consente:

-  la selezione degli eventi in base a criteri di ricerca (tipo di operazione, id, ecc.),

-  l’esame nel dettaglio di un evento selezionato;

-  la disponibilità di dati di sintesi (totali di tipo di operazione per stato, per intervallo temporale, ecc.).

Componenti di utilità
---------------------

Le componenti di utilità rappresentano un insieme di componenti “di servizio” invocate, in base alle necessità, dal *Workflow* Applicativo per
svolgere ruoli informativi specifici e utilizzabili da più servizi applicativi all'interno del NodoSPC:

-  traduttore XML: struttura e assembla i messaggi XML dei servizi;

-  modulo crittografia: cifra/decifra informazioni e gestisce i certificati crittografici;

-  modulo diagnostico: effettua controlli di natura sintattica e alcuni controlli semantici.

Ognuna delle componenti di utilità, oltre ad attività specifiche alla propria funzione, svolge le attività di interfacciamento ed integrazione con il
gestore del *Workflow* Applicativo.

Sistema di monitoring 
----------------------

Il sistema di *monitoring* svolge attività di controllo complessivo per quanto attiene alle tematiche di monitoraggio. Tale componente deve essere
considerata come una entità logica indipendente, con un proprio *workflow* specifico e proprie regole di funzionamento, in grado, quindi, di
verificare malfunzionamenti e condizioni di errore di qualsiasi altro modulo.

Nel sistema di *monitoring* è allocata la funzione di *throttling* che limita l’utilizzo del Sistema pagoPA oltre le possibilità di carico da cui
possa conseguire il verificarsi di disservizi generali. Tale funzionalità viene innescata automaticamente nel caso in cui un Ente Creditore tenti di
avviare, nell’unità di tempo, un numero di operazioni di pagamento superiori ai fabbisogni da esso stesso dichiarati. Le regole di *throttling* sono
indicate nel documento “\ *Indicatori di qualità per i Soggetti Aderenti*\ ” pubblicato sul sito istituzionale dell’Agenzia per l’Italia Digitale.

Sistema di Gestione del Tavolo Operativo
----------------------------------------

Il sistema ha lo scopo di fornire il supporto necessario alle attività del Tavolo Operativo, monitorando le altre componenti applicative e avendo
accesso alle informazioni relative ad ogni richiesta di intervento.

Fra le funzioni di supporto al Tavolo operativo è messo a disposizione un sistema di *Interactive Voice Response* (IVR, Risposta Vocale Interattiva)
per istradare le chiamate vocali, integrato a un sistema di *trouble-ticketing* per tracciare tutte le attività di assistenza.

Controlli
---------

Tutti i flussi/dati scambiati e previsti dai Servizi di Nodo devono risultare conformi agli Standard di Servizio.

Qualora fosse riscontrata una mancata conformità a detti Standard di Servizio, il soggetto ricevente ha l’obbligo:

-  di bloccare l’esecuzione del relativo flusso elaborativo e di trattamento dei dati;

-  rendere disponibile un’evidenza dello stato del flusso a fronte di una eventuale situazione di blocco del flusso stesso.

Servizi applicativi opzionali
-----------------------------

Rientrano in questa tipologia le funzioni che il Servizio mette a disposizione dei soggetti appartenenti al Dominio e che possono da questi essere
utilizzate nell’ambito dello svolgimento delle proprie attività.

Totali di traffico
~~~~~~~~~~~~~~~~~~

Il servizio di quadratura dei flussi di traffico mette a disposizione dei soggetti appartenenti al Dominio che ne facciano richiesta, un flusso
periodico relativo a tutte le interazioni (RPT e RT) transitate attraverso il NodoSPC e di stretta pertinenza del singolo richiedente.

Il NodoSPC mette a disposizione dell’Ente Creditore e del Prestatore di Servizi di Pagamento gli strumenti per la ricezione di tali flussi.

Il periodo temporale durante il quale saranno disponibili i flussi relativi ai “Totali di Traffico” non potrà superare i 10 giorni di calendario e
sarà comunque pubblicato sul sito dell’Agenzia per l’Italia Digitale.

SEZIONE III – SPECIFICHE TECNICHE

Introduzione 
=============

La presente sezione descrive le interfacce di cooperazione applicativa del software che implementa i servizi del NodoSPC.

Il NodoSPC definisce le regole di cooperazione tra i due attori (EC e PSP) del processo di pagamento, i quali sono connessi al NodoSPC per mezzo di
piattaforme software così denominate:

-  **stazioneIntermediarioPA**: rappresenta la piattaforma software utilizzata da un Ente Creditore per scambiare i messaggi all’interno del sistema
   pagoPA relativamente ai processi di pagamento di uno o più servizi.

-  **Canale**: rappresenta la piattaforma software messa a disposizione da un PSP (e connessa al NodoSPC) che realizza un servizio di pagamento messo
   a disposizione dell’utilizzatore finale al fine di completare un pagamento verso un Ente Creditore.

Entrambi gli attori possono utilizzare una molteplicità di piattaforme software per colloquiare con il NodoSPC, in funzione delle proprie esigenze.

Per la piena comprensione dell’interscambio dei messaggi all’interno del sistema, si deve tenere presente la possibilità che tra l’attore principale
ed il NodoSPC si interponga un intermediario (intermediarioPA, intermediarioPSP) a cui l’attore principale ha demandato il compito di gestire la
propria piattaforma software di interconnessione e rendere disponibili le interfacce verso il NodoSPC. Nella figura seguente sono rappresentate le
varie casistiche possibili.

|C:\Users\mogi\AppData\Local\Microsoft\Windows\INetCache\Content.Outlook\2QI8WBLX\deploymentDiagram.png|

**Figura XX – Diagramma delle connessioni logiche al NodoSPC**

Si definisce quindi:

-  **IntermediarioPA**: il soggetto che opera come intermediario per un Ente Creditore. Qualora l’Ente Creditore non si avvalga di un intermediario,
   rappresenta l’Ente Creditore stesso;

-  **IntermediarioPSP**: il soggetto che opera come intermediario per un PSP. Qualora il PSP non si avvalga di un intermediario, rappresenta il PSP
   stesso;

-  **StazioneIntermediarioPA**: il sistema software gestito da un IntermediarioPA, che si interfaccia direttamente col NodoSPC;

-  **Canale**: il sistema software gestito da un IntermediarioPSP, che si interfaccia direttamente al NodoSPC con le modalità previste.

Allo stesso soggetto è consentito di connettersi al NodoSPC in maniera diversa (diretta o intermediata) in funzione dei servizi offerti.

Nelle descrizioni seguenti si ometterà di fare riferimento a detti intermediari, in quanto essi non svolgono un ruolo logicamente distinguibile dai
soggetti intermediati.

Interfacce/Protocolli
---------------------

Il NodoSPC espone diverse interfacce per realizzare le funzioni di cooperazione:

-  **Web-services**, realizzati con protocollo SOAP;

-  **SFTP**, per il trasferimento sicuro di file che non necessitano di essere elaborati contestualmente;

-  **WISP**, *web app* (protocollo HTTPS) che realizza un *wizard* interattivo per la scelta del PSP con cui effettuare il pagamento da parte
   dell’Utilizzatore finale.

..

   |C:\Users\mogi\AppData\Local\Microsoft\Windows\INetCache\Content.Outlook\2QI8WBLX\cd_interfacce.png|

**Figura XX – Diagramma delle interfacce di comunicazione**

Le interfacce *web services* e SFTP rappresentate nella figura precedente sono ricapitolate in tabella:

+---------------+---------+------------+-------------------------------------------------------------------------------------+
| Denominazione | Formato | Protocollo | Descrizione                                                                         |
+===============+=========+============+=====================================================================================+
| NodoPerEc     | WSDL    | SOAP       | Raccolta di metodi e parametri di interfaccia esposti dal NodoSPC fruibili dagli EC |
+---------------+---------+------------+-------------------------------------------------------------------------------------+
| EcPerNodo     | WSDL    | SOAP       | Raccolta di metodi e parametri di interfaccia esposti dagli EC fruibili dal NodoSPC |
+---------------+---------+------------+-------------------------------------------------------------------------------------+
| NodoPerPSP    | WSDL    | SOAP       | Raccolta di metodi e parametri di interfaccia esposti dal NodoSPC fruibili dai PSP  |
+---------------+---------+------------+-------------------------------------------------------------------------------------+
| PspPerNodo    | WSDL    | SOAP       | Raccolta di metodi e parametri di interfaccia esposti dai PSP fruibili dal NodoSPC  |
+---------------+---------+------------+-------------------------------------------------------------------------------------+
|               |         |            |                                                                                     |
+---------------+---------+------------+-------------------------------------------------------------------------------------+
| SFTP          | Testo   | SFTP       | Raccolta di regole per la ricezione di file massivi e/o elementi dal NodoSPC.       |
+---------------+---------+------------+-------------------------------------------------------------------------------------+

**Tabella XX – Interfacce di comunicazione**

Le caratteristiche tecniche dei servizi utilizzati all’interno dei casi d’uso sono disponibili all’interno del progetto gitHub in formato WSDL (per le
chiamate SOAP). I dati per la configurazione dei servizi SFTP sono messi a disposizione ai soggetti aderenti, in forma testuale, mediante canali
riservati.

Per l’interfaccia WISP nei confronti dell’Utilizzatore finale sono resi disponibili per gli EC degli SDK per lo sviluppo di applicazioni *mobile*.

Architettura Funzionale
-----------------------

Per descrivere l’interazione tra EC, NodoSPC e PSP questa sezione è stata articolata nei seguenti capitoli:

-  **Modello dei Dati**: documenta le strutture dei dati scambiati all’interno dei servizi tra i diversi attori ed il NodoSPC.

-  **Pagamento Attivato presso EC**: documenta i metodi messi a disposizione dei soggetti aderenti per realizzare il modello di pagamento attivato
   presso l’EC.

-  **Pagamento Attivato presso PSP**: documenta i metodi messi a disposizione dei soggetti aderenti per realizzare un pagamento di una posizione
   debitoria presso un PSP.

-  **Avvisatura Digitale**: documenta i metodi messi a disposizione dei soggetti aderenti per realizzare la generazione e la distribuzione di un
   avviso di pagamento digitale.

-  **Back-Office**: documenta le funzioni accessorie che possono essere invocate per gestire scenari secondari del ciclo di vita del pagamento (es.
   storno, revoca).

-  **Ausiliarie**: documenta le funzioni di controllo che contribuiscono a monitorare lo stato di esecuzione di un pagamento (es. richiesta stato RPT,
   richiesta stato RT), al fine di attuare eventuali azioni di recupero.

Le funzioni del sistema sono descritte attraverso i casi d’uso secondo lo standard UML (Use Cases, da ora in avanti UC). In particolare per ogni
funzione, verrà fornita:

-  la descrizione degli attori coinvolti ed i loro obiettivi;

-  la descrizione del caso d’uso nominale, cioè il *workflow* che termina in assenza di errori

Nel dettaglio, ogni UC verrà descritto attraverso:

-  una condizione iniziale dello stato del pagamento che definisce il pre-requisito per l’attuazione del caso d’uso;

-  un trigger, cioè l’evento che scatena il caso d’uso;

-  una descrizione testuale del *workflow*;

-  una condizione finale che identifica lo stato del pagamento a conclusione dello UC;

-  uno (o più) *sequence diagram* che descrivono le interazioni nel tempo tra i diversi attori e le interfacce utilizzate.

Ogni messaggio contenuto all’interno dei *sequence diagram* sarà:

-  numerato in base all’ordine temporale di invio/ricezione del messaggio;

-  caratterizzato dalla notazione riportata in tabella;

-  corredato da una descrizione; nel caso di messaggio di risposta (*response*), indicherà l’esito della richiesta (*request*) effettuata.

La tabella seguente illustra le notazioni grafiche utilizzate nei *sequence diagrams*.

+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
|    Elemento                                     | Simbolo                                         | Vincoli / Note                                  |
+=================================================+=================================================+=================================================+
| Attore                                          | |image18|                                       | Rappresenta uno degli attori del Sistema pagoPA |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
| Richiesta SOAP                                  |                                                 | Freccia rossa linea continua, che rappresenta   |
|                                                 |                                                 | la richiesta entrante nell’interfaccia          |
|                                                 |                                                 | dell’attore che espone i servizi                |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
| Risposta SOAP                                   |                                                 | Freccia blu linea tratteggiata, che rappresenta |
|                                                 |                                                 | la risposta uscente dall’interfaccia            |
|                                                 |                                                 | dell’attore che espone i servizi; appare sempre |
|                                                 |                                                 | in corrispondenza di una richiesta SOAP         |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
| GET HTTP                                        |                                                 | Freccia verde linea continua, che rappresenta   |
|                                                 |                                                 | le chiamate effettuate dall’utilizzatore finale |
|                                                 |                                                 | per la fruizione delle applicazioni WEB fornite |
|                                                 |                                                 | dagli attori del processo                       |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
| Azione SFTP                                     |                                                 | Freccia viola linea continua, che rappresenta   |
|                                                 |                                                 | un’azione mediata dal protocollo SFPT           |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
| SFTP *response*                                 |                                                 | Freccia viola linea tratteggiata, che           |
|                                                 |                                                 | rappresenta la risposta ad un comando SFTP      |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
| Stato Pagamento                                 |                                                 | Losanga fondo giallo bordo rosso, che           |
|                                                 |                                                 | rappresenta lo stato del pagamento sul NodoSPC  |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+

**Tabella XX – Notazioni grafiche utilizzate nei sequence diagram**

Con l’obiettivo di favorire l’attuazione di strategie di ripristino, automatiche o manuali, da mettere in atto direttamente da parte degli attori
connessi al sistema (EC, PSP) i possibili errori saranno classificati in base alle categorie riportate nella figura sottostante.

|intro_errori_revoca_storno_riconciliazione|

**Figura XX – Raggruppamento delle possibili tipologie di errori**

Le tipologie di errori con relativa descrizione e macro-categoria di appartenenza sono descritte nella tabella sottostante.

+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
| Categoria                                       | Tipologia                                       | Descrizione                                     |
+=================================================+=================================================+=================================================+
| Errori Infrastrutturali                         | Superamento Soglie                              | Il soggetto fruitore ha superato i limiti di    |
|                                                 |                                                 | interazione applicativa (frequenza di richieste |
|                                                 |                                                 | troppo elevata) con il soggetto erogatore di    |
|                                                 |                                                 | cui al documento “Indicatori di qualità per i   |
|                                                 |                                                 | soggetti aderenti”                              |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
|                                                 | Connessione                                     | Impossibilità di interagire con la Controparte  |
|                                                 |                                                 | applicativa raggiunta mediante il NodoSPC       |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
|                                                 | *Timeout*/Congestioni                           | Superamento delle soglie temporali previste per |
|                                                 |                                                 | la risposta del soggetto erogatore di cui al    |
|                                                 |                                                 | documento “Indicatori di qualità per i soggetti |
|                                                 |                                                 | aderenti”                                       |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
| Errori Configurazione                           | Configurazione Chiamante                        | Errore nei dati di configurazione da parte del  |
|                                                 |                                                 | soggetto fruitore del servizio applicativo      |
|                                                 |                                                 | invocato                                        |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
|                                                 | Configurazione Controparte                      | Errore nei dati di configurazione della         |
|                                                 |                                                 | controparte applicativa raggiunta mediante il   |
|                                                 |                                                 | NodoSPC                                         |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
| Errori Controparte                              | *Timeout* Controparte                           | Superamento delle soglie temporali previste per |
|                                                 |                                                 | la risposta della controparte applicativa di    |
|                                                 |                                                 | cui al documento “Indicatori di qualità per i   |
|                                                 |                                                 | soggetti aderenti”                              |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
|                                                 | Errore *response* Controparte                   | Errore nella risposta da parte della            |
|                                                 |                                                 | controparte applicativa                         |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
| Errori Validazione                              | Validazione Sintattica                          | Errore nella sintassi dei messaggi scambiati    |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
|                                                 | Duplicazione Messaggi                           | Duplicazione dei messaggi scambiati tra         |
|                                                 |                                                 | soggetto erogatore e fruitore                   |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
|                                                 | Validazione Semantica                           | Errore di validazione semantica nell’esercizio  |
|                                                 |                                                 | del processi del sistema                        |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+

**Tabella XX – Descrizione delle categorie di errore**

Per gli errori che causano l’emanazione di un *faultBean* da parte del NodoSPC, in riferimento a ogni caso d’uso, saranno trattate le possibili
strategie di risoluzione ed evidenziati i percorsi critici per cui è necessario l’instaurazione del Tavolo Operativo di cui alla sezione IV.

Stato del Pagamento
-------------------

Nei processi di *business* descritti nella sezione II, il processo di pagamento può essere definito da un insieme discreto di transazioni fra stati
stabili del sistema, caratterizzati da un set di informazioni/condizioni di entrata e un set di informazioni/condizioni di uscita.

Gli stati tracciati nei *sequence diagram* dei casi d’uso e riportati nel presente documento, sono unicamente quelli in cui il *workflow* attraversa
l’interfaccia applicativa del NodoSPC. Quando un soggetto non può essere autonomo nella diagnosi di una anomalia, verranno fornite indicazioni per
l’attivazione del Tavolo Operativo con il NodoSPC e/o con la controparte interessata.

Il seguente diagramma evidenzia la successione temporale degli stati del processo di pagamento, la cui descrizione è riportata nella tabella
successiva.

|image20|

**Figura XX – Stati del pagamento
**

+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
| Stato                                           | Descrizione                                     | Tracciato su pagoPA                             |
+=================================================+=================================================+=================================================+
| S1 - “In attesa generazione PD”                 | Stato iniziale in cui permane il sistema se     | Si                                              |
|                                                 | fallisce l’avvio di un processo di pagamento    |                                                 |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
| S2 – “PD in attesa”                             | L’EC ha generato una Posizione Debitoria, di    | Si                                              |
|                                                 | propria iniziativa o in conseguenza di          |                                                 |
|                                                 | un’azione spontanea dell’Utilizzatore Finale.   |                                                 |
|                                                 |                                                 |                                                 |
|                                                 | *Sono in questo stato tutti i pagamenti per cui |                                                 |
|                                                 | esiste un IUV, un numero Avviso di Pagamento,   |                                                 |
|                                                 | ma ancora nessuna RPT associata è stata         |                                                 |
|                                                 | generata.*                                      |                                                 |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
| S3 – “RPT Attivata”                             | Nel dominio dell’EC è stata generata una RPT a  | Si                                              |
|                                                 | causa della scelta da parte dell’Utilizzatore   |                                                 |
|                                                 | Finale del PSP che gestirà il pagamento.        |                                                 |
|                                                 |                                                 |                                                 |
|                                                 | *Sono in questo stato tutti i pagamenti per cui |                                                 |
|                                                 | è stata generata una RPT. È stato generato un   |                                                 |
|                                                 | CCP che distingue il tentativo di pagamento. La |                                                 |
|                                                 | RPT risulta validata e presa in carico dal      |                                                 |
|                                                 | NodoSPC.*                                       |                                                 |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
| S4 – “Pagamento autorizzato”                    | Il pagamento risulta autorizzato                | Si (solo per i pagamenti autorizzati su WISP)   |
|                                                 | dall’Utilizzatore Finale attraverso i           |                                                 |
|                                                 | meccanismi previsti dal sistema pagoPA          |                                                 |
|                                                 |                                                 |                                                 |
|                                                 | *Sono in questo stato tutti i pagamenti per cui |                                                 |
|                                                 | la RPT risulta presa in carico da un PSP. Il    |                                                 |
|                                                 | PSP non ha ancora generato la RT                |                                                 |
|                                                 | corrispondente.*                                |                                                 |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
| S5 – “RPT Pagata”                               | Il pagamento risulta andato a buon fine ed il   | Si                                              |
|                                                 | PSP scelto dall’Utilizzatore Finale incassa la  |                                                 |
|                                                 | somma e genera la RT.                           |                                                 |
|                                                 |                                                 |                                                 |
|                                                 | *Sono in questo stato tutti i pagamenti andati  |                                                 |
|                                                 | a buon fine, per cui il PSP ha generato la RT.* |                                                 |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
| S6 – “RT Nodo”                                  | La RT generata dal PSP scelto dall’Utilizzatore | Si                                              |
|                                                 | Finale è consegnata al NodoSPC                  |                                                 |
|                                                 |                                                 |                                                 |
|                                                 | *Sono in questo stato tutti i pagamenti andati  |                                                 |
|                                                 | a buon fine, per cui il NodoSPC ha preso in     |                                                 |
|                                                 | carico la RT.*                                  |                                                 |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
| S7 – “RT EC”                                    | La RT è consegnata all’Ente Creditore dal       | Si                                              |
|                                                 | NodoSPC                                         |                                                 |
|                                                 |                                                 |                                                 |
|                                                 | *Sono in questo stato tutti i pagamenti andati  |                                                 |
|                                                 | a buon fine, per cui l’EC ha preso in carico la |                                                 |
|                                                 | RT.*                                            |                                                 |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
| S8 – “RT Accreditata”                           | Il PSP scelto dall’Utilizzatore Finale ha       | No                                              |
|                                                 | accreditato il pagamento sul conto indicato     |                                                 |
|                                                 | nella RPT dall’Ente Creditore.                  |                                                 |
|                                                 |                                                 |                                                 |
|                                                 | *Sono in questo stato tutti i pagamenti la cui  |                                                 |
|                                                 | RT può essere messa in relazione a SCT disposto |                                                 |
|                                                 | dal PSP.*                                       |                                                 |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
| S9 – “RT Rendicontata PSP”                      | Il PSP genera e mette a disposizione il flusso  | Si                                              |
|                                                 | di rendicontazione per l’EC sul Nodo SPC.       |                                                 |
|                                                 |                                                 |                                                 |
|                                                 | *Sono in questo stato tutti i pagamenti per il  |                                                 |
|                                                 | quali il PSP ha disposto un PSP cumulativo e    |                                                 |
|                                                 | possono essere messi in relazione a un flusso   |                                                 |
|                                                 | di rendicontazione.*                            |                                                 |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
| S10 – “Pronto per riconciliazione”              | Il pagamento è pronto per essere riconciliato   | Si                                              |
|                                                 | sui sistemi di *back-office* dell’EC            |                                                 |
|                                                 |                                                 |                                                 |
|                                                 | *Sono in questo stato tutti i pagamenti i cui   |                                                 |
|                                                 | flussi di rendicontazione, acquisiti dall’EC,   |                                                 |
|                                                 | quadrano con i corrispondenti SPC*              |                                                 |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
| S11 – “PD annullata”                            | L’EC ha annullato una Posizione Debitoria,      | No                                              |
|                                                 | precedentemente generata.                       |                                                 |
|                                                 |                                                 |                                                 |
|                                                 | *Sono in questo stato tutti i pagamenti         |                                                 |
|                                                 | disposti al di fuori del sistema pagoPA*        |                                                 |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+

**Tabella XX –** **Descrizione degli stati del pagamento**

La seguente tabella ha lo scopo di associare a ciascuno dei *task* dei modelli di business di cui alla sezione II le primitive SOAP coinvolte,
evidenziando le transizioni di stato causate dall’esecuzione degli stessi *task*.

+--------------------+--------------------+--------------------+--------------------+--------------------+--------------------+--------------------+
| Task               | Primitiva          | Stato di Ingresso  | Stato di Uscita    | Pre-condizioni     | Post-condizioni    | Note               |
+====================+====================+====================+====================+====================+====================+====================+
| T2.2.1             | -                  | n.a.               | S1 - “In attesa    | n.a.               | L’EC ha ricevuto   | Lo stato S1 è il   |
|                    |                    |                    | generazione PD”    |                    | la richiesta di    | primo stato        |
|                    |                    |                    |                    |                    | generazione della  | presente a sistema |
|                    |                    |                    |                    |                    | Posizione          | in caso di         |
|                    |                    |                    |                    |                    | Debitoria da parte | pagamento          |
|                    |                    |                    |                    |                    | del PSP            | spontaneo          |
+--------------------+--------------------+--------------------+--------------------+--------------------+--------------------+--------------------+
| T1.1.1             | *nodoInviaAvvisoDi | n.a.               | S2 – “PD in        | n.a.               | L’EC ha effettuato | Lo stato S2 è il   |
|                    | gitale*            |                    | attesa”            |                    | la generazione     | primo stato        |
|                    |                    |                    |                    |                    | della Posizione    | presente a sistema |
|                    |                    |                    |                    |                    | Debitoria, che è   | in caso di         |
|                    |                    |                    |                    |                    | pronta per essere  | pagamento con      |
|                    |                    |                    |                    |                    | lavorata           | avviso             |
+--------------------+--------------------+--------------------+--------------------+--------------------+--------------------+--------------------+
| T2.1.1             | -                  | n.a                | S2 – “PD in        | n.a.               | L’EC ha effettuato |                    |
|                    |                    |                    | attesa”            |                    | la generazione     |                    |
|                    |                    |                    |                    |                    | della Posizione    |                    |
|                    |                    |                    |                    |                    | Debitoria, che è   |                    |
|                    |                    |                    |                    |                    | pronta per essere  |                    |
|                    |                    |                    |                    |                    | lavorata           |                    |
+--------------------+--------------------+--------------------+--------------------+--------------------+--------------------+--------------------+
| T2.2.2             | -                  | S1 - “In attesa    | S2 – “PD in        | L’EC ha ricevuto   | L’EC ha effettuato |                    |
|                    |                    | generazione PD”    | attesa”            | la richiesta di    | la generazione     |                    |
|                    |                    |                    |                    | generazione della  | della Posizione    |                    |
|                    |                    |                    |                    | posizione          | Debitoria, che è   |                    |
|                    |                    |                    |                    | debitoria da parte | pronta per essere  |                    |
|                    |                    |                    |                    | del PSP            | lavorata           |                    |
+--------------------+--------------------+--------------------+--------------------+--------------------+--------------------+--------------------+
| T1.1.1             | -                  | S2 – “PD in        | S11 – “PD          | L’EC riceve il     | La Posizione       |                    |
|                    |                    | attesa”            | Annullata”         | pagamento al di    | Debitoria non è    |                    |
|                    |                    |                    |                    | fuori del circuito | più lavorabile     |                    |
|                    |                    |                    |                    | pagoPA oppure      |                    |                    |
|                    |                    |                    |                    | vuole annullare la |                    |                    |
|                    |                    |                    |                    | posizione          |                    |                    |
|                    |                    |                    |                    | debitoria perché   |                    |                    |
|                    |                    |                    |                    | errata             |                    |                    |
+--------------------+--------------------+--------------------+--------------------+--------------------+--------------------+--------------------+
| T2.1.2             | *nodoInviaRPT*     | S2 – “PD in        | S3 – “RPT          | E’ stata generata  | L’EC ha            |                    |
|                    |                    | attesa”            | Attivata”          | una Posizione      | indirizzato su     |                    |
|                    |                    |                    |                    | Debitoria.         | WISP e pagoPA ha   |                    |
|                    |                    |                    |                    |                    | preso in carico il |                    |
|                    |                    |                    |                    | L’Utilizzatore     | carrello di RPT    |                    |
|                    |                    |                    |                    | finale genera un   |                    |                    |
|                    |                    |                    |                    | carrello di RPT e  |                    |                    |
|                    |                    |                    |                    | avvia la procedura |                    |                    |
|                    |                    |                    |                    | di pagamento       |                    |                    |
+--------------------+--------------------+--------------------+--------------------+--------------------+--------------------+--------------------+
| T2.2.7             | *nodoInviaRPT*     | S2 – “PD in        | S3 – “RPT          | È stata generata   | L’EC ha attivato   |                    |
|                    |                    | attesa”            | Attivata”          | una Posizione      | l’RPT e l’ha       |                    |
|                    |                    |                    |                    | Debitoria.         | inoltrata al PSP   |                    |
|                    |                    |                    |                    |                    |                    |                    |
|                    |                    |                    |                    | L’EC riceve una    |                    |                    |
|                    |                    |                    |                    | richiesta di       |                    |                    |
|                    |                    |                    |                    | attivazione RPT da |                    |                    |
|                    |                    |                    |                    | parte del PSP      |                    |                    |
|                    |                    |                    |                    | oppure             |                    |                    |
|                    |                    |                    |                    | l’Utilizzatore     |                    |                    |
|                    |                    |                    |                    | finale accede      |                    |                    |
|                    |                    |                    |                    | direttamente ai    |                    |                    |
|                    |                    |                    |                    | canali messi a     |                    |                    |
|                    |                    |                    |                    | disposizione       |                    |                    |
|                    |                    |                    |                    | dall’EC ed ha      |                    |                    |
|                    |                    |                    |                    | scelto la          |                    |                    |
|                    |                    |                    |                    | Posizione          |                    |                    |
|                    |                    |                    |                    | Debitoria da       |                    |                    |
|                    |                    |                    |                    | pagare             |                    |                    |
+--------------------+--------------------+--------------------+--------------------+--------------------+--------------------+--------------------+
| T2.1.5             | -                  | S3 – “RPT          | S4 – “Pagamento    | La RPT è stata     | L’Utilizzatore     |                    |
|                    |                    | Attivata”          | autorizzato”       | attivata           | finale ha          |                    |
|                    |                    |                    |                    |                    | approvato il       |                    |
|                    |                    |                    |                    |                    | pagamento          |                    |
+--------------------+--------------------+--------------------+--------------------+--------------------+--------------------+--------------------+
| T2.2.8             | -                  | S3 – “RPT          | S4 – “Pagamento    | La RPT è stata     | L’Utilizzatore     |                    |
|                    |                    | Attivata”          | autorizzato”       | attivata           | finale ha          |                    |
|                    |                    |                    |                    |                    | approvato il       |                    |
|                    |                    |                    |                    |                    | pagamento          |                    |
+--------------------+--------------------+--------------------+--------------------+--------------------+--------------------+--------------------+
| T2.1.9             | *pspInviaRPT*      | S4 – “Pagamento    | S5 – “RPT Pagata”  | L’Utilizzatore     | Il PSP ha          |                    |
|                    |                    | autorizzato”       |                    | finale ha          | incassato il       |                    |
|                    |                    |                    |                    | approvato il       | pagamento          |                    |
|                    |                    |                    |                    | pagamento          |                    |                    |
+--------------------+--------------------+--------------------+--------------------+--------------------+--------------------+--------------------+
| T2.2.9             | -                  | S4 – “Pagamento    | S5 – “RPT Pagata”  | L’Utilizzatore     | Il PSP ha          | In caso di         |
|                    |                    | autorizzato”       |                    | finale ha          | incassato il       | pagamento          |
|                    |                    |                    |                    | approvato il       | pagamento          | attraverso PSP è   |
|                    |                    |                    |                    | pagamento          |                    | possibile che il   |
|                    |                    |                    |                    |                    |                    | pagamento da parte |
|                    |                    |                    |                    |                    |                    | dell’Utente finale |
|                    |                    |                    |                    |                    |                    | avvenga prima del  |
|                    |                    |                    |                    |                    |                    | ricevimento        |
|                    |                    |                    |                    |                    |                    | dell’RPT da parte  |
|                    |                    |                    |                    |                    |                    | dello stesso PSP,  |
|                    |                    |                    |                    |                    |                    | per questo si      |
|                    |                    |                    |                    |                    |                    | raccomanda di      |
|                    |                    |                    |                    |                    |                    | effettuare sempre  |
|                    |                    |                    |                    |                    |                    | la verifica        |
|                    |                    |                    |                    |                    |                    | dell’RPT           |
|                    |                    |                    |                    |                    |                    | (*Gateway* G2.5)   |
+--------------------+--------------------+--------------------+--------------------+--------------------+--------------------+--------------------+
| T2.1.12            | *nodoInviaRT*      | S5 – “RPT Pagata”  | S6 – “RT Nodo”     | Il PSP ha ricevuto | La RT è stata      |                    |
|                    |                    |                    |                    | la RPT ed ha       | ricevuta da pagoPA |                    |
|                    |                    |                    |                    | incassato il       |                    |                    |
|                    |                    |                    |                    | pagamento          |                    |                    |
+--------------------+--------------------+--------------------+--------------------+--------------------+--------------------+--------------------+
| T2.2.11            | *nodoInviaRT*      | S5 – “RPT Pagata”  | S6 – “RT Nodo”     | Il PSP ha ricevuto | La RT è stata      |                    |
|                    |                    |                    |                    | la RPT ed ha       | ricevuta da pagoPA |                    |
|                    |                    |                    |                    | incassato il       |                    |                    |
|                    |                    |                    |                    | pagamento          |                    |                    |
+--------------------+--------------------+--------------------+--------------------+--------------------+--------------------+--------------------+
| T2.1.13            | *paaInviaRT*       | S6 – “RT Nodo”     | S7 – “RT EC”       | La RT è stata      | L’EC ha ricevuto   |                    |
|                    |                    |                    |                    | ricevuta da pagoPA | l’RT               |                    |
+--------------------+--------------------+--------------------+--------------------+--------------------+--------------------+--------------------+
| T2.2.12            | *paaInviaRT*       | S6 – “RT Nodo”     | S7 – “RT EC”       | La RT è stata      | L’EC ha ricevuto   |                    |
|                    |                    |                    |                    | ricevuta da pagoPA | l’RT               |                    |
+--------------------+--------------------+--------------------+--------------------+--------------------+--------------------+--------------------+
| T2.1.16            | -                  | S7 – “RT EC”       | S8 – “Accreditata” | Il PSP ha          | Il PSP ha          |                    |
|                    |                    |                    |                    | incassato il       | accreditato il     |                    |
|                    |                    |                    |                    | pagamento          | pagamento sul      |                    |
|                    |                    |                    |                    |                    | conto dell’EC      |                    |
+--------------------+--------------------+--------------------+--------------------+--------------------+--------------------+--------------------+
| T2.2.15            | -                  | S7 – “RT EC”       | S8 – “Accreditata” | Il PSP ha          | Il PSP ha          |                    |
|                    |                    |                    |                    | incassato il       | accreditato il     |                    |
|                    |                    |                    |                    | pagamento          | pagamento sul      |                    |
|                    |                    |                    |                    |                    | conto dell’EC      |                    |
+--------------------+--------------------+--------------------+--------------------+--------------------+--------------------+--------------------+
| T2.1.17            | *nodoInviaFlussi*  | S8 – “Accreditata” | S9 – “RT           | Il PSP ha          | Il PSP ha inviato  |                    |
|                    |                    |                    | Rendicontata PSP”  | accreditato il     | il rendiconto      |                    |
|                    |                    |                    |                    | pagamento sul      | degli accrediti    |                    |
|                    |                    |                    |                    | conto dell’EC      | effettuati a       |                    |
|                    |                    |                    |                    |                    | pagoPA             |                    |
+--------------------+--------------------+--------------------+--------------------+--------------------+--------------------+--------------------+
| T2.2.16            | *nodoInviaFlussi*  | S8 – “Accreditata” | S9 – “RT           | Il PSP ha          | Il PSP ha inviato  | In caso di         |
|                    |                    |                    | Rendicontata PSP”  | accreditato il     | il rendiconto      | pagamento di       |
|                    |                    |                    |                    | pagamento sul      | degli accrediti    | singola RT, il PSP |
|                    |                    |                    |                    | conto dell’EC      | effettuati a       | potrebbe non       |
|                    |                    |                    |                    |                    | pagoPA             | inviare il         |
|                    |                    |                    |                    |                    |                    | rendiconto         |
+--------------------+--------------------+--------------------+--------------------+--------------------+--------------------+--------------------+
| T2.1.18            | *nodoChiediFlussoR | S9 – “RT           | S10 – “Pronto per  | Il PSP ha inviato  | pagoPA ha fornito  |                    |
|                    | endicontazione*    | Rendicontata PSP”  | riconciliazione”   | il rendiconto      | i rendiconti       |                    |
|                    |                    |                    |                    | degli accrediti    | ricevuti all’EC    |                    |
|                    |                    |                    |                    | effettuati a       |                    |                    |
|                    |                    |                    |                    | pagoPA             |                    |                    |
+--------------------+--------------------+--------------------+--------------------+--------------------+--------------------+--------------------+
| T2.2.17            | *nodoChiediFlussoR | S9 – “RT           | S10 – “Pronto per  | Il PSP ha inviato  | pagoPA ha fornito  |                    |
|                    | endicontazione*    | Rendicontata PSP”  | riconciliazione”   | il rendiconto      | i rendiconti       |                    |
|                    |                    |                    |                    | degli accrediti    | ricevuti all’EC    |                    |
|                    |                    |                    |                    | effettuati a       |                    |                    |
|                    |                    |                    |                    | pagoPA             |                    |                    |
+--------------------+--------------------+--------------------+--------------------+--------------------+--------------------+--------------------+

**Tabella XX – Quadro sinottico delle transazioni di stato**

Modello dei dati 
=================

Avvisatura digitale
-------------------

+-----------+-----------------------------------------------+
| |image21| | **Paragrafo soggetto a proposta di modifica** |
+-----------+-----------------------------------------------+

Questo paragrafo descrive gli elementi scambiati tra il NodoSPC e gli attori coinvolti per realizzare la funzione di Avvisatura Digitale.

In particolare, gli elementi principali che vengono scambiati sono:

-  **Avvisatura**, rappresenta il dato attraverso il quale un EC notifica ad un Soggetto Pagatore un avviso di pagamento digitale. Può essere
   scambiato singolarmente o attraverso una lista.

-  **Esito Inoltro Avvisatura**, rappresenta la notifica dell’avvenuta consegna dell’avviso precedentemente inviato.

-  **Iscrizione Servizio**, rappresenta la richiesta di un utente finale di ricezione degli avvisi di pagamento tramite uno dei canali messi a
   disposizione dai PSP.

Il seguente Diagramma delle classi rappresenta la relazione tra i diversi oggetti scambiati ed altri oggetti già descritti nei paragrafi precedenti.

|image22|

**Figura XX – Diagramma delle classi dell’avvisatura**

Avviso digitale
~~~~~~~~~~~~~~~

L’Avvisatura rappresenta il documento telematico con il quale un EC notifica ad un Soggetto Pagatore un Avviso di Pagamento.

|image23|

**Figura XX – Diagramma delle relazioni degli attributi dell’Avvisatura**

Una Avvisatura è descritta dai seguenti parametri:

-  *codiceAvviso*: è il numero dell’avviso di pagamento, composto come descritto nell’allegato A delle Linee Guida;

-  *tassonomiaAvviso*: classificazione dell’avviso;

-  *dataScadenzaPagamento*: rappresenta la data ultima entro la quale si richiede che venga pagato l’avviso di pagamento;

-  *dataScadenzaAvviso*: Indica la data, successiva alla data di scadenza del pagamento, sino alla quale si ritiene valido l'avviso;

-  *importoAvviso*: rappresenta l’importo da pagare, potrebbe subire delle variazioni;

-  *descrizionePagamento*: testo libero che descrive la natura dell’avviso;

-  *urlAvviso*: URL di una pagina web messa a disposizione dall'EC dove l'Utilizzatore finale può consultare l'avviso di pagamento;

-  *tipoPagamento* : indica la natura del pagamento;

-  *tipoOperazione*: indica il tipo di operazione connessa con l’avviso. Può assumere i seguenti valori:

..

   ‘C’ = Creazione di un nuovo avviso

   ‘U’= Modifica di un avviso esistente

   ‘D’= Cancellazione di un avviso esistente

Inoltre contiene informazioni in merito a:

-  **anagrafica beneficiario**: descrive l’EC che ha emesso l’avviso di pagamento;

-  **identificativo dominio**: contiene il codice fiscale del soggetto direttamente connesso che invia l'avviso Digitale;

-  **soggetto pagatore**: identifica il soggetto destinatario dell’avviso;

-  **dati Singolo Pagamento**: descrive i dettagli del pagamento da effettuare.

Il tipo *ListaAvvisiDigitali* è la struttura composta dall’insieme di più avvisi, purché di numero inferiore a 100.000 elementi.

Esito Inoltro Avvisatura
~~~~~~~~~~~~~~~~~~~~~~~~

È un oggetto informatico, predisposto dal Nodo-SPC, che permette all’EC di conoscere l’esito del relativo inoltro massivo di Avvisi digitali.

|image24|

**Figura XX – Diagramma delle classi dell’esito inoltro avvisatura**

Contiene al suo interno informazioni riguardo a:

-  **identificativoMessaggioRichiesta**: riferimento all’avviso inviato

-  **identificativoDominio**: il codice fiscale del soggetto direttamente connesso che ha inviato l'avviso Digitale di cui il NodoSPC sta fornendo
   l’Esito.

-  **EsitoAvvisatura**: struttura che descrive l’esito dell’inoltro dell’avvisatura.

L’esito di un avvisatura è descritto dai seguenti parametri:

-  *tipoCanaleEsito*: tipologia di canale usato per inviare l’avviso all'utente;

-  *IdentificativoCanale*: identificativo del canale “mobile” a cui si riferisce l’esito dell’avvisatura;

-  *codiceEsito*: esito dell'invio riferito al singolo canale;

-  *descrizioneEsito*: testo libero che, in caso di esito negativo (codiceEsito<>0), descrive l’evento stesso.

Iscrizione al servizio
~~~~~~~~~~~~~~~~~~~~~~

Definisce lo schema secondo il quale un PSP richiede al NodoSPC di ricevere le avvisature destinate ad un Soggetto Pagatore.

|image25|

**Figura XX – Diagramma delle classi dell’iscrizione al servizio**

Contiene al suo interno informazioni riguardo a:

-  **IdentificativoUnivocoSoggetto**: descrizione del Soggetto Pagatore del quale si vuole ricevere le avvisature.

È descritto dai seguenti parametri:

-  *azioneDiAggiornamento*: Indica il tipo di aggiornamento richiesto, può assumere i seguenti valori:

   -  ‘A’= Attivazione

   -  ‘D’= disattivazione

Pagamenti 
----------

In questo paragrafo sono descritti i seguenti documenti XML scambiati tra gli attori del sistema nell’ambito dei processi di pagamento:

-  Richiesta di Pagamento Telematico (RPT);

-  Ricevuta Telematica (RT);

-  Flusso di rendicontazione (FR);

-  Richiesta di Revoca (RR);

-  Esito Revoca (ER).

Ogni elemento è caratterizzato da un campo *versioneOggetto* che ne indica la versione di riferimento, ogni versione è composta dalla tripletta
numerica *Major.Minor.Patch*, che viene incrementata a seguito dei seguenti eventi:

-  un avanzamento di *Major revision* è causato da modifiche alla struttura dell’oggetto tali che impediscono la retro-compatibilità con le versioni
   precedenti dello stesso oggetto;

-  un avanzamento di *Minor revision* è ancora causato da modifiche all’oggetto ma tali che comunque garantiscono la retro-compatibilità con le
   versioni precedenti;

-  un avanzamento di *Patch revision* è invece causato dalla necessità di apportare correzioni o precisazioni di scarso impatto.

Il seguente *class diagram* mostra le relazioni che si instaurano tra gli elementi durante un tentativo di pagamento andato a buon fine.

|image26|

**Figura XX – Diagramma delle classi del pagamento**

In particolare:

-  come specificato all’interno dell’Allegato A delle linee guida, ogni Posizione Debitoria di un EC è identificata all’interno di pagoPA da un codice
   identificativo denominato *identificativoUnivocoVersamento* (IUV). Tale codice è univocamente generato da un EC;

-  per chiudere una Posizione Debitoria, l’Utilizzatore finale esegue una operazione di pagamento attraverso pagoPA con un PSP da lui stesso
   determinato. Ogni operazione (o tentativo) di pagamento, quindi, presuppone necessariamente l’esistenza di una Posizione Debitoria;

-  l’operazione di pagamento è univocamente identificata da un codice denominato *codiceContestoPagamento* (CCP) generato dal soggetto che innesca il
   pagamento;

-  IUV e CCP congiuntamente consentono di associare ogni RPT alla corrispondente RT.

-  ad ogni operazione di pagamento, corrisponde uno solo degli oggetti RPT, RT e Flusso di Rendicontazione. Nella eventualità che sia richiesta la
   revoca di un’operazione già conclusa si genera un'unica coppia di oggetti RR/ER;

-  ad un Flusso di Rendicontazione di uno specifico conto di accredito di un determinato EC corrispondono tutte le operazioni di pagamento andate a
   buon fine disposte nella singola giornata operativa;

-  ad ogni RPT corrisponde una ed una sola RT;

-  ad una RR corrisponde una ed una sola RT;

-  ad un ER corrisponde una ed una sola RR.

Richiesta di Pagamento Telematica (RPT)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

La RPT descrive una richiesta di pagamento di una Posizione Debitoria.

|image27|

**Figura XX – Diagramma delle classi della RPT**

In particolare, una RPT è composta dai seguenti elementi:

-  **dominio**: identifica il mittente della richiesta tramite i dati di configurazione;

-  **soggettoVersante**: identifica la persona, fisica o giuridica, che effettua il pagamento;

-  **soggettoPagatore**: identifica la persona fisica o giuridica associato alla Posizione Debitoria;

-  **enteBeneficiario**: identifica l’EC beneficiario del pagamento;

-  **datiVersamento**: descrive i dettagli necessari del (dei) versamento (i) utili al PSP per completare l’operazione di pagamento verso l’EC.

La trasmissione della RPT è infine identificata dai seguenti parametri generati dall’EC:

-  data di generazione della RPT (*dataOraMessaggioRichiesta*).

-  codice *IdentificativoMessaggioRichiesta*, univoco nell’ambito della stessa data di generazione della RPT.

Nel seguito si descrivono nel dettaglio gli elementi della RPT all’interno dello schema XSD a meno che non siano palesemente auto-esplicativi; inoltre
sono specificati i parametri associati agli attributi che vengono utilizzati per filtrare i PSP in grado di erogare il servizio di pagamento richiesto
durante il processo di selezione degli stessi da parte dell’Utilizzatore finale.

|image28|

**Figura XX – Diagramma delle classi del versamento**

Un versamento è caratterizzato dai seguenti attributi principali:

-  *dataEsecuzionePagamento*: indica la data in cui l’EC richiede che venga effettuato il versamento;

-  *ImportoTotaleDaVersare*: specifica l’importo totale del versamento, anche nel caso che includa l’acquisto di eventuali marche da bollo; la
   valorizzazione di tale parametro istruisce il NodoSPC a filtrare i servizi di pagamento dei PSP sulla base del massimo importo pagabile contenuto
   nel Catalogo Dati Informativi;

-  *Tipo Versamento*: campo mantenuto per retro-compatibilità; contiene sempre il valore “BBT”;

-  *identificativoUnivocoVersamento:* riferimento univoco assegnato al versamento da parte dell’EC (vedi allegato A alle Linee guida); identifica la
   Posizione Debitoria;

-  *CodiceContestoPagamento*: codice univoco necessario a definire il contesto nel quale viene effettuato il versamento; identifica il tentativo di
   pagamento;

-  *ibanAddebito e bicAddebito*: parametri opzionali che definiscono rispettivamente l’International Bank Account Number (ISO 13616) e il Bank
   Identifier Code (ISO 9362) del conto da addebitare;

-  *firma ricevuta*: campo mantenuto per retro-compatibilità, sempre valorizzato a 0.

Un unico pagamento disposto dall’Utilizzatore finale può comportare per il PSP, per richiesta dell’EC, la necessità di operare molteplici accrediti
(massimo cinque) su diversi conti dell’EC come specificato nella struttura *datiSingoloVersamento* che contiene i dati di dettaglio necessari per tali
operazioni:

-  *importoSingoloVersamento*: importo del singolo accredito (NB la somma dei singoli importi deve corrispondere al dato *ImportoTotaleDaVersare)*;

-  *ibanAccredito* e *bicAccredito*: entrambi i campi identificano univocamente il conto corrente specificato dall’EC da accreditare dell’importo del
   singolo versamento, che deve essere configurato sul NodoSPC;

-  *ibanAppoggio* e *bicAppoggio*: entrambi i campi identificano univocamente il conto corrente alternativo al conto di accredito che il PSP può
   utilizzare per gestire l’operazione di pagamento. La scelta di utilizzare il conto alternativo a quello di accredito è demandata al PSP in base
   alle proprie necessità operative, purché preventivamente dichiarate nella propria configurazione e purché la scelta rimanga coerente per tutti i
   singoli versamenti. In un caso d’uso notevole nella prassi tali campi sono valorizzati con il conto corrente postale, in alternativa a un conto
   bancario specificato come conto di accredito. Nello XSD il dato è facoltativo per gestire il caso in cui l’EC effettivamente non disponga di un
   conto corrente alternativo; viceversa, se presente, il conto corrente deve essere configurato sul NodoSPC;

-  *causaleVersamento*: rappresenta la descrizione estesa della causale del versamento che deve essere conforme a quanto indicato nella Sezione I
   dell’Allegato A alle Linee guida;

-  *datiSpecificiRiscossione*: rappresenta l’indicazione dell’imputazione della specifica entrata per esporre la natura contabile del pagamento,
   specificando il tipo e codice contabilità.

Richiesta di acquisto Marca da Bollo Digitale
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

L’EC può consentire all’Utilizzatore finale, con un unico versamento, il contestuale acquisto di uno o più Marche da bollo digitali, con le modalità
previste dall’Agenzia per le Entrate. A tal fine è necessario che almeno un singolo versamento contenga i seguenti campi:

-  *tipoBollo*: contiene uno dei tipi di Marca da Bollo Digitale per i quali l’Agenzia per le Entrate consente l’acquisto tramite pagoPA. A ogni tipo
   di bollo è associato un costo che deve essere coerente con il valore del campo *importoSingoloVersamento*;

-  *hashDocumento*: contiene l’impronta informatica (*digest*) del documento digitale a cui è associata la Marca da Bollo Digitale. L’algoritmo di
   *hash* da utilizzare per produrre l’impronta è lo SHA-256. La stringa di 256 bit (32 ottetti) risultato di tale algoritmo deve essere convertita in
   base64;

-  *provinciaResidenza*: sigla automobilistica della provincia di residenza del soggetto pagatore.

La valorizzazione della presente struttura dati istruisce il NodoSPC a rendere disponibili all’Utilizzatore finale, durante il processo di selezione
dei PSP, quelli convenzionati con l’Agenzia delle Entrate per l’acquisto della Marca da Bollo Digitale (sistema @e.bollo).

Ricevuta Telematica (RT)
~~~~~~~~~~~~~~~~~~~~~~~~

La RT restituisce all’EC il documento che conclude il flusso innescato da una richiesta di pagamento (RPT) ed attesta, qualora l’esito sia positivo,
l’esecuzione del versamento e la chiusura della Posizione Debitoria.

|image29|

**Figura XX – Diagramma delle classi della RT**

Questi sono i principali elementi:

-  **dominio**: identifica il mittente della richiesta tramite i dati di configurazione;

-  **soggettoVersante**: identifica la persona fisica o giuridica che effettua le operazioni di versamento;

-  **soggettoPagatore**: identifica la persona fisica o giuridica a cui è intestata la posizione debitoria;

-  **istitutoAttestante**: descrive il Prestatore di Servizi di Pagamento utilizzato per le operazioni

-  **enteBeneficiario**: identifica l’EC destinatario del pagamento l’EC che richiesto l’acquisto della Marca da Bollo Digitale;

-  **datiPagamento**: descrive il dettaglio del pagamento effettuato (con esito).

La trasmissione della RT è infine identificata dai seguenti parametri generati dal PSP:

-  *dataOraMessaggioRicevuta*: indica la data e l’ora del pagamento, liberatoria per l’Utilizzatore finale. Corrisponde con la data e ora del
   pagamento indicata dal PSP nell’attestazione.

-  *riferimentoMessaggioRichiesta*: nella generazione di una RT il PSP deve settare tale campo in modo che sia identico al campo
   *identificativoMessaggioRichiest*\ a della univoca RPT di riferimento.

Richiesta di revoca (RR)
~~~~~~~~~~~~~~~~~~~~~~~~

La RR contiene tutte le informazioni necessarie per gestire sia la revoca che lo storno di un pagamento, definiti in sezione II.

|image30|

**Figura XX – Diagramma delle classi della Richiesta di Revoca**

In particolare, la RR è composta dai seguenti elementi:

-  **dominio**: identifica il mittente della richiesta tramite i dati di configurazione;

-  **soggettoVersante**: identifica la persona fisica o giuridica che ha effettuato le operazioni di versamento;

-  **soggettoPagatore**: identifica la persona fisica o giuridica a cui è riferita la Posizione Debitoria di cui è richiesto il *rollback*;

-  **istitutoAttestante**: descrive il Prestatore di Servizi di Pagamento che ha emesso a RT e che ne richiede la revoca;

-  **datiRevoca**: descrive il dettaglio dell’operazione di revoca.

Esito Della Revoca (ER)
~~~~~~~~~~~~~~~~~~~~~~~

La ER descrive l’esito di una RR di un pagamento effettuato.

|C:\Users\mogi\AppData\Local\Microsoft\Windows\INetCache\Content.Outlook\2QI8WBLX\cd_ES.png|

**Figura XX – Diagramma delle classi dell’Esito della Revoca**

In particolare la ER è composta dai seguenti elementi:

-  **dominio**: identifica il mittente della richiesta tramite i dati di configurazione;

-  **soggettoVersante**: identifica la persona fisica o giuridica che ha effettuato le operazioni di versamento;

-  **soggettoPagatore**: identifica la persona fisica o giuridica a cui è riferita la Posizione Debitoria di cui è richiesto il *rollback*;

-  **istitutoAttestante**: descrive il Prestatore di Servizi di Pagamento che ha emesso a RT e che ne richiede la revoca;

-  **datiRevoca**: descrive il dettaglio dell’operazione di revoca.

-  **riferimento**: insieme dei campi che identificano la RR effettuata.

Flusso di rendicontazione (FR)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Il FR referenzia i singoli pagamenti accreditati tramite bonifico cumulativo di un conto corrente dell’EC, conformemente a quanto stabilito
nell’Allegato A delle Linee Guida.

Le informazioni che devono essere messe a disposizione dell'EC sono organizzate in flussi omogenei di dati e devono essere rese disponibili ai
soggetti interessati a cura del PSP che ha effettuato l’operazione di accredito. Il FR deve essere reso disponibile all’EC nella giornata successiva a
quella durante la quale è stato disposto il bonifico (D+2).

|image32|

**Figura XX – Diagramma delle classi del Flusso di Rendicontazione**

In particolare, il FR è identificato dai seguenti parametri:

-  *identificativoFlusso*: riferimento al componente <idFlusso> della causale del SEPA Credit Transfer di Riversamento (dato “Unstructured Remittance
   Information” – attributo AT-05)

-  *identificativoUnivocoRegolamento*: identificativo assegnato dal PSP all’operazione di trasferimento fondi, che può alternativamente essere così
   valorizzato:

   -  Transaction Reference Number (TRN, attributo AT-43 Originator Bank’s Reference), qualora il PSP, al momento della generazione del flusso di
      riversamento, disponga di tale dato;

   -  EndToEndId (attributo AT-41 Originator’s Reference): identificativo univoco assegnato dal PSP, nel caso in cui al momento della generazione del
      flusso di riversamento non sia disponibile il TRN;

-  *istitutoMittente*: struttura che identifica il PSP mittente che genera il FR;

-  *istitutoRicevente*: identifica l’EC destinatario del flusso;

-  *datiSingoloPagamento*: struttura che riporta la distinta dei versamenti cumulati all’interno del flusso SCT; ciascun versamento viene messo in
   relazione con i seguenti elementi:

   -  la Posizione Debitoria, attraverso l’\ *identificativoUnivocoVersamento* (IUV);

   -  le RT prodotte dal PSP, attraverso l’\ *identificativoUnivocoRiscossione* (IUR) ed eventualmente l’\ *indiceDatiSingoloPagamento* che specifica
      l’indice (numero d’ordine) nella lista di versamenti all’interno della RT.

.. _giornale-degli-eventi-1:

Giornale degli eventi
---------------------

Il Giornale degli Eventi (GDE) ha l’obiettivo di consentire la tracciabilità di ogni operazione di pagamento (andata a buon fine o abortita) per il
tramite del NodoSPC.

L'operazione di pagamento si sviluppa mediante la cooperazione applicativa tra sistemi diversi degli EC, del NodoSPC e dei PSP. È quindi necessario,
per ricostruire il processo complessivo, che ognuno dei sistemi interessati dal pagamento telematico si doti di funzioni specifiche per registrare in
modo standardizzato i passaggi principali del trattamento dell'operazione di pagamento. Gli eventi di ingresso e di uscita dal sistema, ovvero le
attività che comportano l’attraversamento di una interfaccia, sono punti cardine da tracciare obbligatoriamente. Sul Giornale degli Eventi si devono
altresì annotare i cambi di stato intermedi significativi per il sistema pagoPA.

Le tracce registrate dai singoli sistemi, in caso di richiesta di verifica, devono poter essere tempestivamente estratte, inviate al Tavolo Operativo
presidiato dal NodoSPC in modo da essere confrontate con le analoghe informazioni prodotte da tutti i sistemi di collaborazione coinvolti
nell’operazione in esame.

Ai fini del confronto sono state individuate tre aree di interesse da monitorare per poter tracciare un pagamento e risolvere eventuali anomalie:

-  i messaggi scambiati tramite le interfacce esterne (SOAP/http/SFTP);

-  gli oggetti scambiati durante un pagamento (RPT, RT, ecc.);

-  le operazioni interne più significative (rappresentate nei capitoli successivi all’interno della presente sezione dalle operazioni associate e
   descritte per i diversi attori).

Nella tabella **Tabella** sottostante sono indicate le informazioni e le specifiche di rappresentazione dei dati che i soggetti appartenenti al
Dominio sono tenuti a fornire per le verifiche di cui sopra. Questi dati sono altresì le informazioni "minime" da archiviare nel Giornale degli
Eventi. Tali informazioni devono essere memorizzate presso le strutture che scambiano le informazioni (EC, PSP, Intermediari tecnologici, NodoSPC) e
devono essere accessibili a richiesta, nei formati che saranno concordati.

+------------------------+------------------------+------------------------+------------------------+------------------------+------------------------+
| Dato                   | Liv                    | Genere                 | Occ                    | Len                    | Contenuto              |
+========================+========================+========================+========================+========================+========================+
|    dataOraEvento       | 1                      | an                     | 1..1                   | 19                     | Indica la data e l’ora |
|                        |                        |                        |                        |                        | dell’evento secondo il |
|                        |                        |                        |                        |                        | formato ISO 8601, alla |
|                        |                        |                        |                        |                        | risoluzione del        |
|                        |                        |                        |                        |                        | millisecondo e sempre  |
|                        |                        |                        |                        |                        | riferito al GMT.       |
|                        |                        |                        |                        |                        | Formato                |
|                        |                        |                        |                        |                        |                        |
|                        |                        |                        |                        |                        | **[YYYY]-[MM]-[DD]T[hh |
|                        |                        |                        |                        |                        | ]:[mm]:[ss.sss]**      |
+------------------------+------------------------+------------------------+------------------------+------------------------+------------------------+
|    identificativoDomin | 1                      | an                     | 1..1                   | 1..35                  | Campo alfanumerico     |
| io                     |                        |                        |                        |                        | contenente il codice   |
|                        |                        |                        |                        |                        | fiscale dell’EC che    |
|                        |                        |                        |                        |                        | invia la richiesta di  |
|                        |                        |                        |                        |                        | pagamento.             |
+------------------------+------------------------+------------------------+------------------------+------------------------+------------------------+
|    identificativoUnivo | 1                      | an                     | 1..1                   | 1..35                  | Riferimento univoco    |
| coVersamento           |                        |                        |                        |                        | assegnato al pagamento |
|                        |                        |                        |                        |                        | dall’ente beneficiario |
|                        |                        |                        |                        |                        | e presente nel         |
|                        |                        |                        |                        |                        | messaggio che ha       |
|                        |                        |                        |                        |                        | originato l’evento.    |
+------------------------+------------------------+------------------------+------------------------+------------------------+------------------------+
|    codiceContestoPagam | 1                      | an                     | 1..1                   | 1..35                  | Codice univoco         |
| ento                   |                        |                        |                        |                        | necessario a definire  |
|                        |                        |                        |                        |                        | il contesto nel quale  |
|                        |                        |                        |                        |                        | viene effettuato il    |
|                        |                        |                        |                        |                        | versamento presente    |
|                        |                        |                        |                        |                        | nel messaggio che ha   |
|                        |                        |                        |                        |                        | originato l’evento.    |
+------------------------+------------------------+------------------------+------------------------+------------------------+------------------------+
|    identificativoPrest | 1                      | an                     | 1..1                   | 1..35                  | identificativo del PSP |
| atoreServiziPagamento  |                        |                        |                        |                        | univoco nel Dominio    |
|                        |                        |                        |                        |                        | scelto                 |
|                        |                        |                        |                        |                        | dall’utilizzatore      |
|                        |                        |                        |                        |                        | finale e/o dall’EC     |
+------------------------+------------------------+------------------------+------------------------+------------------------+------------------------+
|    tipoVersamento      | 1                      | an                     | 0..1                   | 1..35                  | Forma tecnica di       |
|                        |                        |                        |                        |                        | pagamento presente nel |
|                        |                        |                        |                        |                        | messaggio che ha       |
|                        |                        |                        |                        |                        | originato l’evento.    |
+------------------------+------------------------+------------------------+------------------------+------------------------+------------------------+
|    componente          | 1                      | an                     | 1..1                   | 1..35                  | Sistema o sottosistema |
|                        |                        |                        |                        |                        | che ha generato        |
|                        |                        |                        |                        |                        | l’evento (es. FESP,    |
|                        |                        |                        |                        |                        | WFESP)                 |
+------------------------+------------------------+------------------------+------------------------+------------------------+------------------------+
|    categoriaEvento     | 1                      | an                     | 1..1                   | 1..35                  | INTERNO/INTERFACCIA,   |
|                        |                        |                        |                        |                        | indica se l'evento     |
|                        |                        |                        |                        |                        | tracciato è relativo   |
|                        |                        |                        |                        |                        | un'operazione di       |
|                        |                        |                        |                        |                        | interfaccia con altri  |
|                        |                        |                        |                        |                        | sistemi oppure se      |
|                        |                        |                        |                        |                        | rappresenta            |
|                        |                        |                        |                        |                        | un'operazione interna  |
|                        |                        |                        |                        |                        | (es. cambio di stato)  |
|                        |                        |                        |                        |                        | al proprio sistema     |
+------------------------+------------------------+------------------------+------------------------+------------------------+------------------------+
|    tipoEvento          | 1                      | an                     | 1..1                   | 1..35                  | Identificativo del     |
|                        |                        |                        |                        |                        | tipo di evento. Nel    |
|                        |                        |                        |                        |                        | caso di interazioni    |
|                        |                        |                        |                        |                        | SOAP è il nome del     |
|                        |                        |                        |                        |                        | metodo SOAP.           |
+------------------------+------------------------+------------------------+------------------------+------------------------+------------------------+
|    sottoTipoEvento     | 1                      | an                     | 1..1                   | 1..35                  | Nel caso di            |
|                        |                        |                        |                        |                        | interazioni SOAP       |
|                        |                        |                        |                        |                        | sincrone assume i      |
|                        |                        |                        |                        |                        | valori req/rsp per     |
|                        |                        |                        |                        |                        | indicare               |
|                        |                        |                        |                        |                        | rispettivamente SOAP   |
|                        |                        |                        |                        |                        | *Request* e SOAP       |
|                        |                        |                        |                        |                        | *Response*.            |
+------------------------+------------------------+------------------------+------------------------+------------------------+------------------------+
|    identificativoFruit | 1                      | an                     | 1..1                   | 1..35                  | Nel caso di eventi di  |
| ore                    |                        |                        |                        |                        | tipo INTERFACCIA si    |
|                        |                        |                        |                        |                        | deve utilizzare        |
|                        |                        |                        |                        |                        | l’Identificativo del   |
|                        |                        |                        |                        |                        | sistema del Soggetto   |
|                        |                        |                        |                        |                        | richiedente            |
|                        |                        |                        |                        |                        | nell’ambito del        |
|                        |                        |                        |                        |                        | Dominio.               |
|                        |                        |                        |                        |                        |                        |
|                        |                        |                        |                        |                        | (Es.                   |
|                        |                        |                        |                        |                        | *identificativoStazion |
|                        |                        |                        |                        |                        | eIntermediarioPA*      |
|                        |                        |                        |                        |                        | nel caso della         |
|                        |                        |                        |                        |                        | *nodoInviaRPT*)        |
|                        |                        |                        |                        |                        |                        |
|                        |                        |                        |                        |                        | Nel caso di eventi di  |
|                        |                        |                        |                        |                        | tipo INTERNO, si può   |
|                        |                        |                        |                        |                        | utilizzare un nome di  |
|                        |                        |                        |                        |                        | componente o sotto     |
|                        |                        |                        |                        |                        | componente che genera  |
|                        |                        |                        |                        |                        | l’evento.              |
+------------------------+------------------------+------------------------+------------------------+------------------------+------------------------+
|    identificativoEroga | 1                      | an                     | 1..1                   | 1..35                  | Nel caso di eventi di  |
| tore                   |                        |                        |                        |                        | tipo INTERFACCIA si    |
|                        |                        |                        |                        |                        | deve utilizzare        |
|                        |                        |                        |                        |                        | l’Identificativo del   |
|                        |                        |                        |                        |                        | sistema del Soggetto   |
|                        |                        |                        |                        |                        | rispondente            |
|                        |                        |                        |                        |                        | nell’ambito del        |
|                        |                        |                        |                        |                        | Dominio.               |
|                        |                        |                        |                        |                        |                        |
|                        |                        |                        |                        |                        | (Es.                   |
|                        |                        |                        |                        |                        | “NodoDeiPagamentiSPC”  |
|                        |                        |                        |                        |                        | nel caso della         |
|                        |                        |                        |                        |                        | *nodoInviaRPT*)        |
|                        |                        |                        |                        |                        |                        |
|                        |                        |                        |                        |                        | Nel caso di eventi di  |
|                        |                        |                        |                        |                        | tipo INTERNO, si può   |
|                        |                        |                        |                        |                        | utilizzare un nome di  |
|                        |                        |                        |                        |                        | componente o sotto     |
|                        |                        |                        |                        |                        | componente che         |
|                        |                        |                        |                        |                        | processa l’evento. Per |
|                        |                        |                        |                        |                        | quest’ultima tipologia |
|                        |                        |                        |                        |                        | il valore può          |
|                        |                        |                        |                        |                        | coincidere con         |
|                        |                        |                        |                        |                        | l’\ *identificativoFru |
|                        |                        |                        |                        |                        | itore*,                |
|                        |                        |                        |                        |                        | qualora non vi sia un  |
|                        |                        |                        |                        |                        | componente che         |
|                        |                        |                        |                        |                        | risponde all’evento    |
|                        |                        |                        |                        |                        | stesso.                |
+------------------------+------------------------+------------------------+------------------------+------------------------+------------------------+
|    identificativoStazi | 1                      | an                     | 0..1                   | 1..35                  | identificativo della   |
| oneIntermediarioPA     |                        |                        |                        |                        | Stazione               |
|                        |                        |                        |                        |                        | dell’intermediario     |
|                        |                        |                        |                        |                        | dell’EC nel sistema    |
|                        |                        |                        |                        |                        | del NodoSPC, da cui è  |
|                        |                        |                        |                        |                        | transitata la RPT/RT.  |
+------------------------+------------------------+------------------------+------------------------+------------------------+------------------------+
|    canalePagamento     | 1                      | an                     | 0..1                   | 1..35                  | identificativo del     |
|                        |                        |                        |                        |                        | Canale del PSP nel     |
|                        |                        |                        |                        |                        | sistema del NodoSPC da |
|                        |                        |                        |                        |                        | cui è transitata/si    |
|                        |                        |                        |                        |                        | vuole far transitare   |
|                        |                        |                        |                        |                        | la RPT/RT.             |
+------------------------+------------------------+------------------------+------------------------+------------------------+------------------------+
|    parametriSpecificiI | 1                      | an                     | 0..1                   | 1..512                 | parametri specifici    |
| nterfaccia             |                        |                        |                        |                        | utilizzati             |
|                        |                        |                        |                        |                        | nell’interfaccia dal   |
|                        |                        |                        |                        |                        | PSP o dall’ECnel       |
|                        |                        |                        |                        |                        | modello di pagamento 1 |
|                        |                        |                        |                        |                        | o 3                    |
+------------------------+------------------------+------------------------+------------------------+------------------------+------------------------+
|    Esito               | 1                      | an                     | 0..1                   | 1..35                  | Campo opzionale in     |
|                        |                        |                        |                        |                        | base allo stato        |
|                        |                        |                        |                        |                        | dell’operazione al     |
|                        |                        |                        |                        |                        | momento della          |
|                        |                        |                        |                        |                        | registrazione          |
|                        |                        |                        |                        |                        | dell’evento.           |
|                        |                        |                        |                        |                        |                        |
|                        |                        |                        |                        |                        | **Obbligatorio nel     |
|                        |                        |                        |                        |                        | caso di richieste      |
|                        |                        |                        |                        |                        | SOAP.**                |
+------------------------+------------------------+------------------------+------------------------+------------------------+------------------------+

**Tabella** XX **- Informazioni "minime" da archiviare nel "Giornale degli Eventi "**

Il GDE dovrà contenere sia tutti gli eventi andati a buon fine, sia quelli abortiti fra cui quelli che hanno dato seguito ad un errore (evidenziando
la categoria dell’errore ricevuto).

Qualora alcune delle informazioni richieste non fossero disponibili per una data operazione, i corrispondenti campi dovranno essere comunque
valorizzati in uno dei due seguenti modi:

-  N/A: nel caso il valore del campo non sia applicabile al sistema pagoPA per l’operazione tracciata (es. *identificativoErogatore* per un evento
   interno);

-  UNKNOW, nel caso il campo sia applicabile, ma non sia stato possibile tracciare l’informazione richiesta.

Per quanto riguarda i PSP si precisa che deve essere sempre registrato, all’interno del Giornale degli Eventi, l’evento relativo alla generazione
della RT (indipendentemente dall’esito del relativo pagamento) così valorizzando i seguenti campi del giornale:

-  *categoriaEvento* a “INTERNO”;

-  *identificativoErogatore* a “GENERAZIONE-RT”.

Messaggi di errore
------------------

In caso di errori verificatisi nel colloquio tra i vari soggetti aderenti (EC e PSP) ed il NodoSPC, i relativi messaggi di errore vengono descritti
utilizzando la struttura **faultBean** mostrata nel seguente diagramma.

|https://www.plantuml.com/plantuml/img/LOv12eDG34JtEONxN49gwGKyGV2d4eZvaiHLyUxQebXdDJnumxIHvBbC2di6fOZcJOlcWycQ3w0Km1_eQk6ZzkbY8s3X65pcb6g0mIwaWDLb52DzNT8DdV89dtyZw_T4orRsFni0|

**Figura XX – Oggetto fauBean**

La struttura contiene i seguenti parametri:

-  *id*: identificativo del soggetto che emette l’errore, valorizzato con idDominio (nel caso di EC), identificativoPSP (nel caso di PSP) e da una
   costante “NodoDeiPagamentiSPC” nel caso di errore identificato da parte del NodoSPC;

-  *faultCode:* codice dell’errore, composto secondo il seguente formato:

..

   <erogatore>_<codice errore>

   Dove <erogatore> rappresenta il soggetto che ha emesso l’errore e può assumere i seguenti valori:

   PPT: errore emesso da NodoSPC;

   PAA: errore emesso da EC;

   CANALE: errore emesso da PSP.

-  *faultString*: specifica del codice dell’errore. Ogni soggetto emittente valorizza tale parametro sulla base delle indicazioni fornite nella
   tabella dei Codici di errore di seguito riportata.

-  *description:* descrizione aggiuntiva dell’errore impostata dal soggetto che emette l’errore. Nella emissione di un **faultCode** *PAA_SEMANTICA*
   (EC) o *CANALE_SEMANTICA* (PSP), i soggetti erogatori (EC o PSP) dovranno indicare nel presente dato lo specifico errore legato all’elaborazione
   dell’oggetto ricevuto. Nel caso in cui il NodoSPC trasmetta verso un soggetto un errore di Controparte con **faultCode** valorizzato, a seconda del
   caso, a *PPT_ERRORE_EMESSO_DA_PAA* o *PPT_CANALE_ERRORE,* il campo è valorizzato con l’errore emesso dalla Controparte.

-  *serial*: posizione dell’elemento nella lista a cui fa riferimento. Utile quando si fornisce un parametro in forma di vettore (ad esempio, nella
   primitiva **nodoInviaCarrelloRPT**). Nel caso in cui l'errore sia generato dall'EC o dal PSP, il dato riporta il valore del dato *faultBean.serial*
   impostato dall'EC o dal PSP;

-  *originalFaultCode:* codice dell’errore generato dalla Controparte. Non è presente se il soggetto che emette l’errore è il NodoSPC;

-  *originalFaultString:* specifica dell’errore generato dalla Controparte. Non è presente se il soggetto che emette l’errore è il NodoSPC;

-  *originalDescription*: descrizione aggiuntiva dell’errore generato dalla Controparte. Non è presente se il soggetto che emette l’errore è il
   NodoSPC.

La tabella sottostante riporta l’elenco dei codici di errore (*faultCode*) che i soggetti dovranno utilizzare al verificarsi delle condizioni di
errore (*faultString*).

+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| faultCode                                                                | faultString                                                              |
+==========================================================================+==========================================================================+
| *CANALE_AVVISO_DUPLICATO*                                                | Messaggio di *warning* per Avviso duplicato                              |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *CANALE_BUSTA_ERRATA*                                                    | Messaggio dismesso                                                       |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *CANALE_ER_DUPLICATA*                                                    | ER duplicata                                                             |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *CANALE_FIRMA_SCONOSCIUTA*                                               | Messaggio dismesso                                                       |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *CANALE_INDISPONIBILE*                                                   | Servizio non disponibile                                                 |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *CANALE_RICHIEDENTE_ERRATO*                                              | Identificativo richiedente non valido                                    |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *CANALE_RPT_DUPLICATA*                                                   | RPT duplicata.                                                           |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *CANALE_RPT_RIFIUTATA*                                                   | RPT rifiutata                                                            |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *CANALE_RPT_SCONOSCIUTA*                                                 | RPT sconosciuta                                                          |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *CANALE_RT_NON_DISPONIBILE*                                              | RT non disponibile                                                       |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *CANALE_RT_SCONOSCIUTA*                                                  | RT sconosciuta                                                           |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *CANALE_SEMANTICA*                                                       | Errore semantico                                                         |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *CANALE_SINTASSI_EXTRAXSD*                                               | Errore di sintassi extra XSD                                             |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *CANALE_SINTASSI_XSD*                                                    | Errore di sintassi XSD                                                   |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *CANALE_SYSTEM_ERROR*                                                    | Errore generico                                                          |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PAA_ATTIVA_RPT_IMPORTO_NON_VALIDO*                                      | L’importo del pagamento in attesa non è congruente con il dato indicato  |
|                                                                          | dal PSP                                                                  |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PAA_ER_DUPLICATA*                                                       | Esito Revoca duplicato                                                   |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PAA_ERRORE_FORMATO_BUSTA_FIRMATA*                                       | Formato busta di firma errato o non corrispondente al *tipoFirma*        |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PAA_FIRMA_ERRATA*                                                       | Errore di firma                                                          |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PAA_FIRMA_INDISPONIBILE*                                                | Impossibile firmare                                                      |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PAA_ID_DOMINIO_ERRATO*                                                  | La PAA non corrisponde al Dominio indicato                               |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PAA_ID_INTERMEDIARIO_ERRATO*                                            | Identificativo intermediario non corrispondente                          |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PAA_PAGAMENTO_ANNULLATO*                                                | Pagamento in attesa risulta annullato all’Ente Creditore                 |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PAA_PAGAMENTO_DUPLICATO*                                                | Pagamento in attesa risulta concluso all’Ente Creditore                  |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PAA_PAGAMENTO_IN_CORSO*                                                 | Pagamento in attesa risulta in corso all’Ente Creditore                  |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PAA_PAGAMENTO_SCADUTO*                                                  | Pagamento in attesa risulta scaduto all’Ente Creditore                   |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PAA_PAGAMENTO_SCONOSCIUTO*                                              | Pagamento in attesa risulta sconosciuto all’Ente Creditore               |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PAA_RPT_SCONOSCIUTA*                                                    | La RPT risulta sconosciuta                                               |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PAA_RT_DUPLICATA*                                                       | La RT è già stata accettata                                              |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PAA_RT_SCONOSCIUTA*                                                     | RT sconosciuta                                                           |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PAA_SEMANTICA*                                                          | Errore semantico                                                         |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PAA_SINTASSI_EXTRAXSD*                                                  | Errore di sintassi extra XSD                                             |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PAA_SINTASSI_XSD*                                                       | Errore di sintassi XSD                                                   |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PAA_STAZIONE_INT_ERRATA*                                                | Stazione intermediario non corrispondente                                |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PAA_SYSTEM_ERROR*                                                       | Errore generico                                                          |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PAA_TIPOFIRMA_SCONOSCIUTO*                                              | Il campo *tipoFirma* non corrisponde ad alcun valore previsto            |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PPT_AUTENTICAZIONE*                                                     | Errore di autenticazione                                                 |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PPT_AUTORIZZAZIONE*                                                     | Il richiedente non ha i diritti per l’operazione                         |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PPT_CANALE_DISABILITATO*                                                | Canale conosciuto ma disabilitato da configurazione                      |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PPT_CANALE_ERR_PARAM_PAG_IMM*                                           | Parametri restituiti dal Canale per identificare il pagamento non        |
|                                                                          | corretti                                                                 |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PPT_CANALE_ERRORE*                                                      | Errore restituito dal Canale                                             |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PPT_CANALE_ERRORE_RESPONSE*                                             | La *response* ricevuta dal Canale è vuota o non corretta sintatticamente |
|                                                                          | o semanticamente                                                         |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PPT_CANALE_INDISPONIBILE*                                               | Nessun Canale utilizzabile e abilitato                                   |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PPT_CANALE_IRRAGGIUNGIBILE*                                             | Errore di connessione verso il Canale                                    |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PPT_CANALE_NONRISOLVIBILE*                                              | Il Canale non è specificato, e nessun Canale risulta utilizzabile        |
|                                                                          | secondo configurazione                                                   |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PPT_CANALE_SCONOSCIUTO*                                                 | Canale sconosciuto                                                       |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PPT_CANALE_SERVIZIO_NONATTIVO*                                          | Il servizio applicativo del Canale non è attivo                          |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PPT_CANALE_TIMEOUT*                                                     | *Timeout* risposta dal Canale                                            |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PPT_CODIFICA_PSP_SCONOSCIUTA*                                           | Valore di codificaInfrastruttura PSP non censito                         |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PPT_DOMINIO_DISABILITATO*                                               | Dominio disabilitato                                                     |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PPT_DOMINIO_SCONOSCIUTO*                                                | *IdentificativoDominio* sconosciuto                                      |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PPT_ERRORE_EMESSO_DA_PAA*                                               | Errore restituito dall’Ente Creditore                                    |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PPT_ERRORE_FORMATO_BUSTA_FIRMATA*                                       | Formato busta di firma errato o non corrispondente al *tipoFirma*        |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PPT_FIRMA_INDISPONIBILE*                                                | Impossibile firmare                                                      |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PPT_IBAN_NON_CENSITO*                                                   | Il codice IBAN indicato dall’Ente Creditore non è presente nella lista   |
|                                                                          | degli IBAN comunicati al sistema pagoPA                                  |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PPT_ID_CARRELLO_DUPLICATO*                                              | Identificativo Carrello RPT duplicato                                    |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PPT_ID_FLUSSO_SCONOSCIUTO*                                              | Identificativo flusso sconosciuto                                        |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PPT_ISCRIZIONE_NON_PRESENTE*                                            | Iscrizione non presente in archivio                                      |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PPT_OPER_NON_REVOCABILE*                                                | Operazione non revocabile                                                |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PPT_OPER_NON_STORNABILE*                                                | Operazione non stornabile                                                |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PPT_PSP_DISABILITATO*                                                   | PSP conosciuto ma disabilitato da configurazione                         |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PPT_PSP_SCONOSCIUTO*                                                    | PSP sconosciuto                                                          |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PPT_RPT_DUPLICATA*                                                      | RPT duplicata                                                            |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PPT_RPT_NON_INOLTRABILE*                                                | La RPT richiesta e fornita dalla PA non può essere inoltrata in quanto   |
|                                                                          | non corretta formalmente                                                 |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PPT_RPT_SCONOSCIUTA*                                                    | RPT sconosciuta                                                          |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PPT_RT_DUPLICATA*                                                       | La RT inviata dal PSP è già stata inviata (RT *push*)                    |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PPT_RT_NONDISPONIBILE*                                                  | RT non ancora pronta                                                     |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PPT_RT_SCONOSCIUTA*                                                     | RT sconosciuta                                                           |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PPT_SEMANTICA*                                                          | Errore semantico                                                         |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PPT_SINTASSI_EXTRAXSD*                                                  | Errore di sintassi extra XSD                                             |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PPT_SINTASSI_XSD*                                                       | Errore di sintassi XSD                                                   |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PPT_STAZIONE_INT_PA_DISABILITATA*                                       | Stazione disabilitata                                                    |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PPT_STAZIONE_INT_PA_IRRAGGIUNGIBILE*                                    | Errore di connessione verso la Stazione                                  |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PPT_STAZIONE_INT_PA_SCONOSCIUTA*                                        | *IdentificativoStazioneRichiedente* sconosciuto                          |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PPT_STAZIONE_INT_PA_SERVIZIO_NONATTIVO*                                 | Il Servizio Applicativo della Stazione non è attivo                      |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PPT_SUPERAMENTOSOGLIA*                                                  | Una qualche soglia fissata per PPT è temporaneamente superata e la       |
|                                                                          | richiesta è quindi rifiutata                                             |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PPT_SYSTEM_ERROR*                                                       | Errore generico                                                          |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PPT_TIPOFIRMA_SCONOSCIUTO*                                              | Il campo *tipoFirma* non corrisponde ad alcun valore previsto            |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PPT_ULTERIORE_ISCRIZIONE*                                               | Ulteriore iscrizione precedentemente censita                             |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PPT_WISP_SESSIONE_SCONOSCIUTA*                                          | La tripletta *idDominio*\ +\ *keyPA*\ +\ *keyWISP* non corrisponde ad    |
|                                                                          | alcuna sessione memorizzata nella componente WISP                        |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| *PPT_WISP_TIMEOUT_RECUPERO_SCELTA*                                       | La tripletta *idDominio*\ +\ *keyPA*\ +\ *keyWISP* è relativa ad una     |
|                                                                          | scelta effettuata scaduta                                                |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+

**Tabella** XX **– Codici di errore**

Configurazione
--------------

In questo paragrafo vengono descritte tutte le informazioni necessarie al NodoSPC per configurare opportunamente gli attori ad esso connessi, ovvero
EC e PSP.

Per la comunicazione di tali informazioni il NodoSPC mette a disposizione l’applicazione *web* Portale delle Adesioni. Per ulteriori dettagli
consultare la Sezione IV.

Ente Creditore
~~~~~~~~~~~~~~

L’oggetto Ente Creditore viene identificato nel sistema attraverso il proprio codice fiscale (campo *idDominio*) e caratterizzato dai seguenti
attributi:

-  Descrizione dell’erogazione dei servizi;

-  Dettaglio di eventuali servizi disponibili per pagamento spontaneo disposto presso il PSP;

-  Dettaglio dei conti correnti di accredito e di appoggio incasso utilizzati.

Il documento che raccoglie la porzione pubblica di tali informazioni che deve essere resa disponibile alle controparti è raccolta nel documento
Tabella delle Controparti che il NodoSPC rende disponibile tramite primitive SOAP descritte fra le funzioni ausiliarie.

|image34|

**Figura XX – Diagramma delle classi per la configurazione di un EC**

PSP
~~~

L’oggetto PSP viene identificato nel sistema (campo *identificativoPSP*) attraverso il codice BIC oppure da un codice formato dalla concatenazione
della stringa “ABI” con il valore del codice ABI del PSP. (La scelta fra i due identificativi deve essere compiuta dal PSP al momento della prima
configurazione e è irreversibile). Ogni PSP è caratterizzato dalle seguenti proprietà:

-  specifica sulla pubblicazione delle informazioni;

-  dettaglio dei servizi di pagamento attivati (canali).

|image35|

**Figura XX – Diagramma delle classi per la configurazione di un PSP**

Il documento che raccoglie la porzione pubblica di tali informazioni che deve essere resa disponibile alle controparti EC è raccolta nel documento
InformativaPSP che il NodoSPC rende disponibile tramite primitive SOAP descritte fra le funzioni ausiliarie.

Inoltre, per la configurazione delle modalità di pagamento nel sistema pagoPA, il PSP produce il documento Catalogo Dati Informativi, come riportato
nella sezione IV.

 Pubblicazione
~~~~~~~~~~~~~~

All’interno di questa struttura, il PSP specifica gli attributi comuni a tutti i servizi di pagamento che rende disponibili sul sistema:

-  *dataPubblicazione*: data e ora relativa all’invio dell’ultimo aggiornamento delle informazioni;

-  *dataInizioValidita*: data e ora di inizio validità delle informazioni;

-  *urlInformazioniPSP*: indirizzo di una pagina web gestita dal PSP rivolta all’Utilizzatore finale per la divulgazione di informazioni specifiche
   relative ai servizi di pagamento resi disponibili;

-  *LogoPSP*: logotipo del PSP;

-  *stornoPagamento*: *flag* che indica la capacità tecnica di gestire il processo di storno di un pagamento.

-  *marcaBolloDigitale*: *flag* che individua un PSP convenzionato con l’Agenzia delle Entrate come rivenditore della Marca da bollo digitale
   attraverso il sistema *@e.bollo*.

Canale
~~~~~~

La struttura raccoglie tutte le informazioni relative a un servizio di pagamento messo a disposizione dal PSP sul sistema pagoPA:

-  *identificativoIntermediario*: identificativo dell’Intermediario del PSP che fornisce lo specifico accesso (Canale) al PSP per l'erogazione del
   servizio. L'intermediario può coincidere con il PSP stesso;

-  *identificativoCanale*: identificativo del canale attraverso il quale viene effettuata la transazione;

-  *TipoVersamento*: codice che identifica il tipo di versamento utilizzato dal canale;

+----------------------------------+--------+------------------------------------------------------------------------------+
| Tipo Versamento                  | Codice | Descrizione                                                                  |
+==================================+========+==============================================================================+
| Pagamento con Carta              | CP     | Il PSP è abilitato a gestire pagamenti con carta di credito o debito         |
+----------------------------------+--------+------------------------------------------------------------------------------+
| Pagamento mediante MyBank        | OBEP   | Il PSP è abilitato a gestire pagamenti MyBank on line                        |
+----------------------------------+--------+------------------------------------------------------------------------------+
| Pagamento attivato presso il PSP | PO     | Il PSP è abilitato a gestire pagamenti interfacciando l’Utilizzatore finale. |
+----------------------------------+--------+------------------------------------------------------------------------------+
| Pagamento mediate Poste Italiane | BP     | Canale che identifica un canale on line gestito da Poste Italiane            |
+----------------------------------+--------+------------------------------------------------------------------------------+

..

   **Tabella XXX – Tipi di versamento**

-  *modelloPagamento*: codice che identifica il modello di pagamento gestito dal canale; i calori utilizzabili sono elencati nella seguente
   tabella\ **.**

+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
| Modello di pagamento                            | Codice                                          | Descrizione                                     |
+=================================================+=================================================+=================================================+
| Processo di pagamento con re indirizzamento     | 0                                               | Il PSP è abilitato a gestire pagamenti          |
| on-line                                         |                                                 | inizializzati dalla primitiva *nodoInviaRPT*    |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
| Processo di pagamento con re indirizzamento     | 1                                               | Il PSP è abilitato a gestire pagamenti          |
| on-line tramite carrello                        |                                                 | inizializzati dalla primitiva                   |
|                                                 |                                                 | *nodoInviaCarrelloRPT*                          |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
| Processo di pagamento con autorizzazione        | 2                                               | Il PSP è abilitato a gestire pagamenti con      |
| gestita dal PSP                                 |                                                 | autorizzazione differita                        |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
| Processo di pagamento attivato presso il PSP    | 4                                               | Il PSP è abilitato ad inizializzare un processo |
|                                                 |                                                 | di pagamento                                    |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+

**Tabella XXX – Modelli di pagamento**

-  *priorità*: campo *boolean* mantenuto per retro-compatibilità da valorizzare a ‘false’;

-  *canaleApp*: indica se il canale in questione può essere inserito all’interno della categoria “Altri Metodi di Pagamento”;

-  *servizioAlleImprese*: campo *boolean* che indica se il servizio erogato dal PSP è destinato ad un utilizzo solo da parte delle imprese.

Inoltre, un canale è definito dagli attributi di seguito descritti in paragrafi dedicati:

Servizio
~~~~~~~~

La struttura descrive come verrà visualizzato all’Utilizzatore finale per selezionare il PSP sul sistema WISP:

-  *nomeServizio*: nome commerciale del servizio / app

-  *logoServizio*: logotipo del servizio / app. Con risoluzione 400x128px.

Informazioni dettaglio Servizio
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

-  *codiceLingua*: identifica la lingua utilizzata per le informazioni di dettaglio della presente struttura. Le lingue supportate dal sistema pagoPA
   sono l’italiano e l’inglese oltre a quelle delle minoranze linguistiche tutelate (tedesco, francese e sloveno);

-  *descrizioneServizio*: testo libero a disposizione del PSP per specificare il servizio;

-  *disponibilitàServizio*: testo libero utilizzato dal PSP per specificare gli orari di erogazione tecnica del servizio;

-  *limitazioniServizio*: informazioni in formato testo che riportano eventuali limitazioni poste dal PSP nell'erogazione del servizio, (esempio:
   Servizio dedicato ad una particolare categoria di professionisti o imprese);

-  *urlInformazioniCanale*: URL di una pagina *web* contenente informazioni relative allo specifico servizio\ *;*

-  *tavoloOperativo*: indica i riferimenti del presidio tecnico predisposto per cooperare con il Tavolo Operativo del NodoSPC.

Plugin
~~~~~~

La struttura permette al PSP di definire un set di parametri personalizzato da utilizzare per interpretare i parametri della redirect di risposta alla
pagina di erogazione del servizio WISP vedi capitolo 9.

Costi
~~~~~

La struttura definisce la *policy* del calcolo delle commissioni che il sistema pagoPA deve applicare.

È possibile gestire le seguenti *policy* per il calcolo della commissione:

-  Numero dei versamenti (*tipoCostoTransazione* = 0): tale *policy* calcola il costo della commissione in base al numero di versamenti da effettuare.
   In questo caso:

   -  il numero delle occorrenze della struttura *fasceCostoServizio* dovrà essere pari a 1;

   -  l'elemento *tipoCommissione* dovrà essere 0 (in valore assoluto);

   -  l'elemento *costoFisso* dovrà essere 0.

-  Totale versamento (*tipoCostoTransazione* = 1): tale *policy* calcola il costo della commissione in base al totale della transazione da effettuare.
   In questo caso è possibile specificare il costo della commissione in base alla fascia di prezzo.

Acquirer
~~~~~~~~

L’\ *Acquirer* è un soggetto che ha instaurato un rapporto con un PSP aderente a pagoPA al fine di gestire le transazioni con le carte di pagamento,
interagendo con il VPOS-AgID.

L’\ *Acquirer* viene configurato attraverso i seguenti parametri:

-  *TerminalID*: Terminal Identification Number (TID);

-  *MerchantID*: Merchant Identification Number (MID) che identifica il PSP relazionato con l’\ *Aquirer*;

-  *Bin*: lista di Issuer Identification Number (IIN) che identifica le carte emesse dal PSP relazionato con l’\ *Aquirer*. Il pagamento con una carta
   il cui BIN è incluso in tale lista è autorizzato dall’\ *Aquirer* senza la necessità di accedere ai circuiti internazionali. Il NodoSPC gestirà
   questa tipologia di pagamenti inoltrando le relative RPT verso il canale ONUS del PSP. Il canale NOT_ON_US è utilizzato dal PSP per gestire i
   pagamenti con carte emesse da altri soggetti.

Pagamento presso l’Ente Creditore
=================================

Attori e casi d’uso
-------------------

All’interno di questo capitolo vengono descritti i casi d’uso per il pagamento innescato dall’Utilizzatore Finale attraverso l’interazione con i
sistemi degli Enti Creditori aderenti al Sistema pagoPA.

Gli attori coinvolti nel processo di pagamento sono i seguenti:

-  **Ente Creditore**: rappresenta un soggetto aderente a pagoPA che rende disponibile all’Utilizzatore finale la possibilità di comporre un carrello
   pagabile *online* tramite un Portale *web* o una *mobile app*;

-  **PSP**: rappresenta un Prestatore di Servizi di Pagamento aderente a pagoPA che rende disponibile almeno un canale di pagamento accessibile
   tramite la componente WISP del NodoSPC;

-  **Utilizzatore finale**, rappresenta una persona fisica e/o giuridica che si interfaccia con le risorse *web* o *mobile* dell’EC al fine di
   ottenere un servizio.

-  **Acquirer:** è il soggetto attraverso il quale un PSP gestisce le transazioni con le carte di pagamento.

Lo scenario di utilizzo è descritto dal seguente caso d’uso nominale:

-  **Pagamento online con guida interattiva di selezione del PSP (WISP):** un Utilizzatore finale effettua il pagamento tramite il Portale *web*
   dell’EC. La scelta dello strumento di pagamento è guidata tramite apposita interfaccia *web* resa disponibile dal NodoSPC.

Pagamento online con guida interattiva di selezione del PSP (WISP)
------------------------------------------------------------------

+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| Pre-Condizione                                                           | L’Utilizzatore finale innesca il processo di pagamento riferito a una    |
|                                                                          | Posizione Debitoria aperta.                                              |
+==========================================================================+==========================================================================+
| Trigger                                                                  | L’Utilizzatore finale esce dalla pagina di *check-out* sul Portale       |
|                                                                          | dell’EC innescando il processo di pagamento di un carrello di RPT        |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| Descrizione                                                              | -  L’EC compone il carrello di RPT e lo invia al NodoSPC                 |
|                                                                          |                                                                          |
|                                                                          | -  Il NodoSPC valida il carrello e replica all’EC fornendo la URL di     |
|                                                                          |    *redirect* per re-direzionare il browser dell’Utilizzatore finale     |
|                                                                          |    sulla pagina WISP per la scelta interattiva del PSP                   |
|                                                                          |                                                                          |
|                                                                          | -  L’Utilizzatore finale accede al WISP e procede alla selezione del     |
|                                                                          |    servizio di pagamento reso disponibile da un PSP.                     |
|                                                                          |                                                                          |
|                                                                          | -  Il NodoSPC invia al canale del PSP scelto dall’Utilizzatore finale il |
|                                                                          |    carrello di RPT;                                                      |
|                                                                          |                                                                          |
|                                                                          | -  Il PSP genera le RT attestanti l’esito del pagamento e la restituisce |
|                                                                          |    al NodoSPC                                                            |
|                                                                          |                                                                          |
|                                                                          | -  L’EC riceve le RT completando la transazione, potendo così erogare il |
|                                                                          |    servizio all’Utilizzatore finale                                      |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| Post-Condizione                                                          | Al termine delle operazioni il pagamento transisce allo stato RT-EC      |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+

Tabella XX: Caso d'uso del processo di pagamento online con guida interattiva di selezione del PSP

L’evoluzione nel tempo del processo di pagamento è la seguente:

|image36|

**Figura XX: Diagramma di sequenza del processo di pagamento iniziato presso l'EC**

1. L’Utilizzatore finale, dopo aver eseguito le operazioni di composizione del carrello, esegue il *check-out* sul Portale dell’EC.

2. Il Portale dell’EC compone il carrello di RPT e lo invia al NodoSPC mediante la primitiva *nodoInviaCarrelloRPT*.

3. Il NodoSPC valida formalmente sintassi e semantica dell’invocazione. Tra i parametri sottoposti a controllo si menzionano:

   a. *identificativoCarrello*: deve risultare univoco all’interno del Sistema pagoPA; il codice deve essere composto secondo il seguente formato:

..

   <Anno(4)><idDominio(11)><codice Sorgente(2)><Progressivo(19)>

   Dove:

   *Anno*: 4 caratteri numerici che rappresentano l’anno in cui viene effettuata la richiesta

   *idDominio*: valore del medesimo campo dell’RPT

   *codiceSorgente*: codice che permette di distinguere la sorgente del codice che genera l’identificativo Carrello (può coincidere con il codice
   segregazione della Stazione)

   *Progressivo*: numero progressivo esadecimale espresso in caratteri alfanumerici.

b. *ibanAccredito*: deve risultare inserito nella lista dei conti correnti dell’EC configurati sul NodoSPC;

c. *ibanAppoggio*: deve risultare inserito nella lista dei conti correnti dell’EC configurati sul NodoSPC;

4. Il NodoSPC fornisce la risposta all’invocazione precedente, modificando lo stato del pagamento in RPT Inviata e restituendo come parametri di
   output:

a. *URL di re-direzione:* risorsa a cui re-indirizzare il browser dell’Utilizzatore finale, contenente anche una query string “idSession=<idSession>”
   che identifica univocamente la sessione\ *;*

b. *esitoComplessivoOperazione*: rappresenta l’esito complessivo dell’operazione di invocazione che può assumere i valori OK e KO.

5. l’EC predispone l’\ *http REDIRECT* verso la URL fornita nella *response* alla primitiva di cui al precedente punto 2.

6. Il browser dell’Utilizzatore finale è re-direzionato verso il NodoSPC e l’Utilizzatore finale viene guidato nella selezione del servizio di
   pagamento.

A seconda delle scelte operate dall’Utilizzatore finale, sono possibili due differenti scenari alternativi.

-  Pagamento con carta;

-  Pagamento con altri strumenti.

**Pagamento con carta**

7.  Dopo che l’Utilizzatore finale ha inserito i dati della Carta di Pagamento, selezionato l’\ *Acquirer* da utilizzare per la transazione
    (eventualmente proposto dal NodoSPC), visualizzato l’importo totale del pagamento e autorizzato lo stesso, il NodoSPC esegue verso l’\ *Acquirer*
    una richiesta di prenotazione del credito sulla carta di pagamento inserita.

8.  L’\ *Acquirer*, a valle delle proprie verifiche, decide se autorizzare la prenotazione del credito.

9.  A conclusione del passo precedente, l’\ *Acquirer* restituisce al NodoSPC l’esito dell’operazione.

10. In caso di esito positivo, il NodoSPC informa l’Utilizzatore finale, tramite apposito messaggio, di aver preso in carico la transazione.

11. Il NodoSPC costruisce la URL di *redirect* per re-direzionare l’Utilizzatore finale sul Portale dell’EC.

12. Il browser dell’Utilizzatore finale è indirizzato sul Portale dell’EC specificando i seguenti parametri:

    d. *idDominio*: identificativo dell’EC che ha eseguito la richiesta di pagamento

    e. *idSession*: identificativo della sessione precedentemente creata

    f. *esito*: descrive l’esito dell’operazione, contiene sempre il valore DIFFERITO

13. A seguito dell’esito positivo della richiesta di prenotazione del credito, il PSP, collegato all’\ *Acquirer* selezionato, riceve dal NodoSPC il
    carrello di RPT, attraverso la primitiva *pspInviaCarrelloRPTCarte*.

14. A seguito della ricezione del carrello, il PSP esegue il controllo semantico del carrello.

15. Il PSP replica al NodoSPC mediante *response* positiva valorizzando il parametro di output *esitoComplessivoOperazione* con il valore OK.

16. Il NodoSPC esegue verso l’\ *Acquirer* una richiesta di contabilizzazione del credito prenotato sulla carta di pagamento inserita, modifica lo
    stato del pagamento in RT PSP e invia una mail all’Utilizzatore finale fornendo l’esito positivo dell’operazione.

**Pagamento mediante altri strumenti**

17. Se l’Utilizzatore finale ha selezionato un servizio di pagamento diverso dalla carta, il NodoSPC invia il carrello di RPT al PSP a cui afferisce
    il servizio di pagamento selezionato mediante la primitiva *pspInviaCarrelloRPT*.

18. Il PSP replica all’invocazione precedente fornendo eventualmente una URL di re-direct. Lo stato del pagamento transisce a RT PSP.

..

   In base alla presenza o meno dell’URL di re-direct, il *workflow* presenta le seguenti possibili alternative:

-  Pagamento mediante re-indirizzamento *on-line*

-  Pagamento mediante autorizzazione gestita dal PSP

**Pagamento mediante re-indirizzamento on-line**

19. Il NodoSPC utilizza la URL ricevuta per re-direzionare il browser dell’Utilizzatore finale.

20. L’Utilizzatore finale raggiunge le pagine messe a disposizione dal PSP per finalizzare il processo di pagamento.

21. L’Utilizzatore finale completa la transazione sulle pagine messe a disposizione dal PSP.

22. Il PSP predispone la http REDIRECT verso la URL del NodoSPC.

23. Il browser dell’Utilizzatore finale raggiunge il NodoSPC.

**Pagamento mediante autorizzazione gestita dal PSP**

24. Nel caso in cui il PSP replichi alla primitiva *pspInviaCarrelloRPT* fornendo la URL di *re-direct* con valore *null*, l’Utilizzatore finale
    autorizza il pagamento interagendo direttamente con il PSP. Tale casistica verrà approfondita al § 9.1.2.2.

Indipendentemente dal servizio di pagamento selezionato, l’Utilizzatore finale visualizza l’esito del pagamento.

25. Il NodoSPC mostra la pagina di riepilogo (“thank you page”) indicando che il pagamento è stato preso in carico.

26. Il NodoSPC re-indirizza verso l’EC accodando alla URL il parametro esito opportunamente valorizzato (OK, ERROR, DIFFERITO).

27. Il PSP genera la RT.

28. Il PSP invia la RT all’EC attraverso il NodoSPC mediante la primitiva *nodoInviaRT*.

29. Il NodoSPC inoltra la RT all’EC attraverso la primitiva *paaInviaRT*.

30. L’EC replica all’invocazione precedente e lo stato del pagamento transisce a RT EC ad indicare che la ricevuta telematica è stata consegnata
    all’Ente Creditore.

31. Il NodoSPC inoltra la *response* fornita dall’EC al PSP.

Caso acquisto Marca da bollo digitale
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Il pagamento di una Marca da Bollo Digitale avviene attraverso il medesimo *workflow* applicativo decritto nel paragrafo precedente. Si fa presente
che sarà necessario valorizzare nella RPT la struttura dati descritta al §8.2.2.

In particolare, l’EC nella predisposizione della RPT deve specificare, oltre all’importo richiesto per la Marca da Bollo Digitale, i seguenti dati:

-  il tipo di bollo da erogare (parametro *tipoBollo*);

-  l’impronta del documento da bollare (parametro *hashDocumento*);

-  la provincia di residenza del soggetto pagatore *(*\ parametro *provinciaResidenza).*

Inoltre la RPT non deve contenere, nella struttura *datiSingoloVersamento* relativa alla Marca da Bollo Digitale, la valorizzazione del parametro
*ibanAccredito*.

Caso autorizzazione gestita dal PSP
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Nel caso in cui il metodo di pagamento scelto dall’Utilizzatore finale preveda un processo autorizzativo gestito dal PSP, i meccanismi di
autorizzazione avvengono al di fuori del sistema pagoPA, tramite accordi specifici tra il PSP e l’Utilizzatore finale (soggetto versante). I sistemi
informatici del PSP acquisiscono tramite la RPT i dati del soggetto versante e procedono all’autenticazione dell’identità dichiarata autorizzando, se
del caso, l’accesso ai sistemi di pagamento.

Un esempio di tale casistica è rappresentato dalla sottoscrizione da parte dell’Utilizzatore finale di una manleva nei confronti del PSP, riguardante
la possibilità di addebito del proprio conto corrente per le richieste di pagamento provenienti da uno specifico EC. In questo specifico caso
l’acquisizione dei dati del soggetto versante è effettuata tramite il parametro *ibanAddebito* valorizzato dall’EC, all’interno della RPT, con il
codice IBAN del conto corrente del soggetto versante.

Prenotazione Rifiutata
----------------------

Si descrive nel seguito lo scenario secondario che si verifica quando l’\ *Acquirer* non autorizza il pagamento con carta.

+-----------------+------------------------------------------------------------------------------------------------------------------------+
| Pre-condizione  | L’Utilizzatore finale effettua pagamento tramite carta                                                                 |
+=================+========================================================================================================================+
| Descrizione     | Alla richiesta di prenotazione del credito effettuata dal NodoSPC all’\ *Acquirer*, questi risponde con esito negativo |
+-----------------+------------------------------------------------------------------------------------------------------------------------+
| Post-condizione | Lo stato del pagamento transisce a *Pagamento rifiutato*                                                               |
+-----------------+------------------------------------------------------------------------------------------------------------------------+

|SD_PRENOTAZIONE_RIFIUTATA|

Figura XX: Diagramma di sequenza della prenotazione rifiutata

L’evoluzione temporale è la seguente:

1. dopo che l’Utilizzatore finale ha confermato la volontà di pagare mediante Carta di Pagamento, il NodoSPC esegue verso l’\ *Acquirer* una richiesta
   di prenotazione del credito sulla carta di pagamento inserita.

2. l’\ *Acquirer* esegue le verifiche del caso.

A questo punto sono possibili le due seguenti alternative:

3. l’\ *Acquirer* comunica l’esito negativo della prenotazione del credito;

..

   oppure

4. il NodoSPC riscontra condizioni di *timeout.*

Il pagamento transisce a *PAGAMENTO_RIFIUTATO.*

5. la componente WISP del NodoSPC mostra all’Utilizzatore finale l’esito negativo delle operazioni;

6. il NodoSPC costruisce la URL di *redirect* verso il Portale dell’EC;

7. l’Utilizzatore finale è re-diretto verso il Portale dell’EC;

8. Il NodoSPC genera RT negativa.

Il *workflow* si conclude riprendendo dal punto 28 dello scenario nominale.

Gestione degli errori
---------------------

Il paragrafo descrive la gestione degli errori nel processo di Pagamento attivato presso l’Ente Creditore secondo le possibili eccezioni riportate nel
Paragrafo precedente.

**Carrello di RPT rifiutato dal Nodo**

+-----------------+---------------------------------------------------------+
| Pre-condizione  | L’EC compone e sottomette al NodoSPC un carrello di RPT |
+=================+=========================================================+
| Descrizione     | Il NodoSPC rifiuta il carrello di RPT                   |
+-----------------+---------------------------------------------------------+
| Post-condizione | Lo stato del pagamento transisce a *RPT Rifiutata*      |
+-----------------+---------------------------------------------------------+

|image38|

Figura XX: Scenario RPT rifiutata dal Nodo

1. l’Utilizzatore finale esegue il *check-out* sul portale dell’EC.

2. l’EC sottomette al NodoSPC il carrello di RPT mediante la primitiva *nodoInviaCarrelloRPT.*

3. il NodoSPC valida la richiesta.

4. il NodoSPC replica fornendo *response* con esito KO indicando un *faultBean* il cui *faultBean.faultCode* è rappresentativo dell’errore
   riscontrato.

..

   Lo stato del pagamento transisce a *RPT rifiutata.*

5. L’EC notifica all’Utilizzatore finale l’errore tecnico invitandolo a contattare il supporto messo a disposizione dall’EC stesso.

Le possibili azioni di controllo sono riportate nella tabella seguente.

+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
| Strategia di risoluzione                        | Tipologia Errore                                | Azione preventiva Suggerita                     |
+=================================================+=================================================+=================================================+
|                                                 | PPT_SINTASSI_EXTRAXSD                           | Verificare la composizione del carrello RPT     |
|                                                 |                                                 | (vedi documento “Elenco Controlli Primitive     |
|                                                 |                                                 | NodoSPC” per la relativa                        |
|                                                 |                                                 | primitiva/\ *FAULT_CODE*) e i parametri di      |
|                                                 |                                                 | invocazione della primitiva SOAP                |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
|                                                 | PPT_SINTASSI_XSD                                |                                                 |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
|                                                 | PPT_ID_CARRELLO_DUPLICATO                       | Utilizzare l’algoritmo specificato per creare   |
|                                                 |                                                 | un *identificativoCarrello* univoco nel sistema |
|                                                 |                                                 | pagoPA                                          |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
|                                                 | PPT_SEMANTICA                                   | Verificare la composizione del documento XML    |
|                                                 |                                                 | RPT controllando la correttezza di              |
|                                                 |                                                 | valorizzazione dei campi (vedi documento        |
|                                                 |                                                 | “Elenco Controlli Primitive NodoSPC” per la     |
|                                                 |                                                 | relativa primitiva/\ *FAULT_CODE*)              |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
|                                                 | PPT_IBAN_NON_CENSITO                            | Verificare preventivamente che il valore dei    |
|                                                 |                                                 | parametri *ibanAccredito* ed *ibanAppoggio*     |
|                                                 |                                                 | presenti nelle RPT siano presenti fra quelli    |
|                                                 |                                                 | forniti in fase di configurazione e attivati al |
|                                                 |                                                 | momento dell’utilizzo                           |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+

Tabella XX: Strategie di risoluzione per lo scenario carrello RPT rifiutato dal Nodo

**Pagamento non Contabilizzato**

+-----------------+----------------------------------------------------------+
| Pre-condizione  | L’Utilizzatore finale paga con carta                     |
+=================+==========================================================+
| Descrizione     | Il PSP rifiuta il carrello di RPT inviato dal NodoSPC    |
+-----------------+----------------------------------------------------------+
| Post-condizione | Lo stato del pagamento transisce a *Pagamento rifiutato* |
+-----------------+----------------------------------------------------------+

|SD_ERR_PAGAMENTO_NON_CONTABILIZZATO|

Figura XX: Diagramma di sequenza del pagamento non contabilizzato

L’evoluzione temporale è la seguente:

1. il NodoSPC esegue la richiesta di prenotazione del credito;

2. l’\ *Acquirer* esegue la verifica della richiesta;

3. l’\ *Acquirer* autorizza la richiesta di prenotazione del credito;

4. il NodoSPC mediante la componente WISP mostra all’Utilizzatore finale la “\ *thank you page*\ ” con il messaggio di presa in carico della
   richiesta;

5. il NodoSPC costruisce la URL di *redirect* verso il Portale dell’EC;

6. il browser dell’Utilizzatore finale è re-direzionato sul portale dell’EC. Il parametro esito sarà impostato al valore DIFFERITO.

7. il Nodo invia il carrello di RPT al PSP.

..

   Possono verificarsi i seguenti casi:

8. il PSP replica negativamente alla richiesta precedente fornendo esito KO alla primitiva di cui al punto 7;

..

   Il pagamento transisce allo stato *PAGAMENTO RIFIUTATO*

9.  il NodoSPC annulla la prenotazione del credito precedentemente effettuata

10. il NodoSPC genera RT negativa ed il processo riprende dal punto 28 dello scenario di pagamento nominale.

..

   Oppure

11. il NodoSPC riscontra condizioni di *timeout* della controparte;

12. il NodoSPC attiva i meccanismi di rientro procedendo ad interrogare la controparte sull’esito positivo o meno dell’inoltro della RPT di cui al
    punto 7 mediante la primitiva *pspChiediStatoRPT* fornendo in ingresso la chiave di pagamento.

13. il PSP ricerca nei propri archivi la RPT richiesta dal NodoSPC.

A questo punto possono verificarsi i seguenti scenari:

14. il PSP replica fornendo esito OK alla primitiva di cui al punto 12. Essendo la RPT giunta al PSP il NodoSPC non compie alcuna azione ed attende la
    generazione della RT da parte del PSP.

Lo stato del pagamento transisce a *RT PSP.*

15. il PSP replica fornendo esito KO alla primitiva di cui al punto 12 emettendo un *faultBean* il cui *faultBean.faultCode* è rappresentativo
    dell’errore riscontrato:

    -  CANALE_RPT_SCONOSCIUTA: il PSP non ha ricevuto alcun carrello di RPT da parte del NodoSPC o l’ha ricevuto parziale;

    -  CANALE_RPT_RIFIUTATA: il PSP ha ricevuto la RPT da parte del NodoSPC scartandola a seguito di errori di validazione;

16. il Nodo annulla la prenotazione del credito precedentemente effettuata;

17. il Nodo genera RT negativa.

..

   Il flusso riprende dal punto 28 dello scenario di pagamento nominale.

**RT rifiutata dal NodoSPC**

+-----------------+-------------------------------------------------------+
| Pre-condizione  | Il pagamento si trova nello stato *RT PSP*            |
+=================+=======================================================+
| Descrizione     | Il PSP invia la RT al NodoSPC                         |
|                 |                                                       |
|                 | Il NodoSPC rifiuta la RT fornendo *response* negativa |
+-----------------+-------------------------------------------------------+
| Post-condizione | Lo stato del pagamento permane in *RT PSP*            |
+-----------------+-------------------------------------------------------+

|SD_RT_RIFIUTATA_NODO|

Figura XX: Scenario RT rifiutata Nodo

L’evoluzione temporale è la seguente:

1. il PSP invia la RT attestante l’esito del pagamento mediante la primitiva *nodoInviaRPT;*

2. il NodoSPC replica negativamente fornendo *response* con esito KO emanando un *faultBean* il cui *faultBean.faultCode* è valorizzato al variare
   dell’errore riscontrato; in particolare:

-  PPT_RT_DUPLICATA nel caso in cui il PSP sottometta nuovamente una RT già invita in precedenza;

-  PPT_SEMANTICA nel caso in cui il NodoSPC riscontri errori di significato nei dati contenuti nella RT.

+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
| Strategia di risoluzione                        | Tipologia Errore                                | Azione di Controllo Suggerita                   |
+=================================================+=================================================+=================================================+
|                                                 | PPT_SINTASSI_EXTRAXSD                           | Verificare l’invocazione della primitiva (vedi  |
|                                                 |                                                 | documento “Elenco Controlli Primitive NodoSPC”  |
|                                                 |                                                 | per la relativa primitiva/\ *FAULT_CODE*)       |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
|                                                 | PPT_SINTASSI_XSD                                |                                                 |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
|                                                 | PPT_RT_DUPLICATA                                | Gestire il caso di RT duplicata il NodoSPC ha   |
|                                                 |                                                 | già ricevuto la RT verificando i propri sistemi |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
|                                                 | PPT_SEMANTICA                                   | Verificare il controllo fallito effettuato dal  |
|                                                 |                                                 | NodoSPC (vedi documento “Elenco Controlli       |
|                                                 |                                                 | Primitive NodoSPC” per la relativa              |
|                                                 |                                                 | primitiva/\ *FAULT_CODE*)                       |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+

Tabella XX: Strategia di risoluzione del caso RT rifiutata dal Nodo

**RT rifiutata dall’EC**

+-----------------+----------------------------------------------------------------------------------------------------------------------+
| Pre-condizione  | Il pagamento si trova nello stato RT_PSP                                                                             |
+=================+======================================================================================================================+
| Descrizione     | L’EC rifiuta la RT inviata dal NodoSPC producendo uno specifico codice di errore; il NodoSPC propaga l’errore al PSP |
+-----------------+----------------------------------------------------------------------------------------------------------------------+
| Post-condizione | Lo stato del pagamento permane in RT_PSP                                                                             |
+-----------------+----------------------------------------------------------------------------------------------------------------------+

|sd_RT_RIUTATA_EC|

Figura XX:Scenario RT rifiutata dall'EC

L’evoluzione temporale è la seguente:

1. il PSP sottomette al NodoSPC una RT mediante la primitiva *nodoInviaRT;*

2. il Nodo sottomette all’EC la RT ricevuta mediante la primitiva *paaInviaRT;*

3. l’EC replica negativamente fornendo *response* con esito KO emettendo un *faultBean* dove il valore del campo *faultBean.faultCode* è
   rappresentativo dell’errore riscontrato; in particolare:

-  PAA_RT_DUPLICATA nel caso in cui il NodoSPC abbia sottomesso una RT precedentemente inviata;

-  PAA_RPT_SCONOSCIUTA nel caso in cui alla RT consegnata non risulti associata alcuna RPT;

-  PAA_SEMANTICA nel caso in cui si riscontrano errori nel tracciato XML della RT;

4. il NodoSPC propaga l’errore riscontrato dall’EC emanando un *faultBean* il cui *faultBean.faultCode* è pari a PPT_ERRORE_EMESSO_DA_PAA.

+--------------------------+--------------------------+-------------------------------+
| Strategia di risoluzione | Tipologia Errore         | Azione di Controllo Suggerita |
+==========================+==========================+===============================+
|                          | PPT_ERRORE_EMESSO_DA_PAA | Attivazione TAVOLO OPERATIVO  |
+--------------------------+--------------------------+-------------------------------+

**RT mancante per timeout Controparti**

+-----------------+-----------------------------------------------------------------------------------------------------------------+
| Pre-condizione  | Il pagamento si trova nello stato *RT PSP*                                                                      |
+=================+=================================================================================================================+
| Descrizione     | Tale scenario può verificarsi per le seguenti condizioni:                                                       |
|                 |                                                                                                                 |
|                 | -  *Timeout*/Congestione del NodoSPC                                                                            |
|                 |                                                                                                                 |
|                 | -  *Timeout*/Congestione dell’EC                                                                                |
|                 |                                                                                                                 |
|                 | -  *Timeout*/Congestione del PSP nella ricezione della *response* inerente la primitiva *nodoInviaRT*           |
|                 |                                                                                                                 |
|                 | In tutti i casi il PSP predispone la RT nell’archivio per il *recovery* in modalità PULLL da parte del NodoSPC. |
+-----------------+-----------------------------------------------------------------------------------------------------------------+
| Post-condizione | Lo stato del pagamento permane in *RT PSP*                                                                      |
+-----------------+-----------------------------------------------------------------------------------------------------------------+

|SD_RT_TIMEOUT_CONTROPARTIpng|

Figura XX: Scenario RT mancante per *timeout* controparti

1. il PSP invia la RT al NodoSPC mediante la primitiva *nodoInviaRT;*

..

   L’EC riscontra condizioni di *timeout* per le quali:

2. il NodoSPC mediante la primitiva *paaInviaRT* non riesce a recapitare la RT all’EC

oppure

3. il NodoSPC mediante la primitiva *paaInviaRT* recapita la RT all’EC;

4. la *response* fornita dall’EC non è recapitata al NodoSPC;

5. il Nodo replica alla primitiva di cui al punto 1 emettendo un *faultBean* il cui *faultBean.faultCode* è rappresentativo dell’errore riscontrato:

   -  PPT_STAZIONE_INT_PA_IRRAGGIUNGIBILE: il NodoSPC riscontra condizioni di *timeout* nella *request* verso l’EC o nella ricezione della relativa
      *response*.

..

   *Timeout* NodoSPC / PSP

6. il NodoSPC riscontra condizioni di *timeout;*

+--------------------------+-----------------------------+----------------------------------------------------+
| Strategia di risoluzione | Tipologia Errore            | Azione di Controllo Suggerita                      |
+==========================+=============================+====================================================+
|                          | PPT_STAZIONE_INT_PA_TIMEOUT | Predisposizione RT in archivio per *recovery* PULL |
+--------------------------+-----------------------------+----------------------------------------------------+

Figura XX: Strategia di risoluzione dello scenario *timeout* delle controparti

Pagamento presso il PSP
=======================

.. _attori-e-casi-duso-1:

Attori e casi d’uso
-------------------

All’interno di questo capitolo vengono descritti i casi d’uso relativi ai possibili processi di pagamento da parte di un Utilizzatore finale,
attraverso uno dei canali messi a disposizione da un PSP, mediante la presentazione di un Avviso di Pagamento notificatogli da un EC. L’Avviso di
pagamento predisposto dall’EC dove essere conforme a quanto previsto nel documento “Il nuovo avviso di pagamento analogico nel sistema pagoPA Versione
2.2.1 - Dicembre 2018”.

Gli attori coinvolti sono i seguenti:

-  **PSP**: rappresenta un canale (fisico o digitale) che offre un servizio di pagamento all’Utilizzatore finale.

-  **Ente Erogatore**: soggetto che si incarica di abilitare all’interno del sistema pagoPA uno o più servizi di pagamento spontaneo.

-  **Ente Creditore**: rappresenta un soggetto aderente a pagoPA in grado di gestire i pagamenti attivati presso i PSP predisponendo e notificando
   (per mezzo cartaceo o digitale) agli utilizzatori finali un avviso di pagamento. Interagisce inoltre con l’Ente Erogatore per la gestione del caso
   di pagamento spontaneo

-  **Utilizzatore Finale**, rappresenta una persona fisica e/o giuridica che interagisce con uno dei canali messi a disposizione dal PSP al fine di
   pagare un servizio anche senza disporre di un avviso di pagamento.

Gli scenari di utilizzo sono descritti dai seguenti casi d’uso nominali:

-  **Pagamento mediante Avviso (scenario principale)**: l’Utilizzatore finale utilizza un canale (fisico o digitale) messo a disposizione da un PSP
   presentando un Avviso di Pagamento. Il pagamento viene perfezionato a valle della ricezione della RPT da parte del PSP.

-  **Pagamento mediante Avviso (scenario alternativo)**: l’Utilizzatore finale utilizza un canale (fisico o digitale) messo a disposizione da un PSP
   presentando un Avviso di Pagamento. Il pagamento viene effettuato a valle della verifica della correttezza dell’avviso ma prima della richiesta di
   attivazione della RPT da parte del PSP.

-  **Pagamento spontaneo presso il PSP:** l’Utilizzatore finale utilizza un canale (fisico o digitale) predisposto dal PSP per innescare il pagamento
   spontaneo di un servizio messo a disposizione da un Ente Erogatore. In tale scenario potrebbe non esistere alcuna posizione debitoria pre-esistente
   all’interno degli archivi di pagamento in attesa dell’EC.

..

   Oltre a suddetti casi d’uso, per il caso del pagamento della tassa automobilistica fare riferimento al documento “Allegato tecnico Pagamento della
   Tassa Automobilistica presso i PSP” pubblicato sul sito istituzionale dell’Agenzia.

Pagamento mediante Avviso (scenario principale) 
------------------------------------------------

+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| Pre-condizioni                                                           | L’Utilizzatore finale è in possesso di un Avviso di Pagamento notificato |
|                                                                          | dall’EC.                                                                 |
+==========================================================================+==========================================================================+
| Trigger                                                                  | L’Utilizzatore finale si presenta presso uno dei canali messi a          |
|                                                                          | disposizione dal PSP (ad esempio sportello fisico, ATM, Home Banking,    |
|                                                                          | *mobile app*, etc.) con l’Avviso di Pagamento.                           |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| Descrizione                                                              | -  Il PSP acquisisce le informazioni contenute nell’avviso tramite la    |
|                                                                          |    lettura di uno degli elementi grafici presenti (QR-Code / Data        |
|                                                                          |    matrix). Deve comunque essere reso possibile l’inserimento manuale    |
|                                                                          |    degli stessi dati.                                                    |
|                                                                          |                                                                          |
|                                                                          | -  Il PSP, tramite il NodoSPC, richiede l’attivazione del pagamento      |
|                                                                          |    descritto all’interno dell’avviso di pagamento. Tale operazione       |
|                                                                          |    verifica la sussistenza della posizione debitoria collegata           |
|                                                                          |    all’avviso di pagamento e determina l’importo del versamento          |
|                                                                          |    richiesto dall’EC. Nel caso in cui l’importo recuperato con tale      |
|                                                                          |    operazione prevale sul dato presente nell’Avviso di Pagamento.        |
|                                                                          |                                                                          |
|                                                                          | -  Il PSP riceve, tramite il NodoSPC, la relativa richiesta di pagamento |
|                                                                          |    telematico (RPT).                                                     |
|                                                                          |                                                                          |
|                                                                          | -  l’Utilizzatore finale, consapevole degli eventuali differenze         |
|                                                                          |    rispetto ai dati riportati sull’avviso, autorizza il pagamento con le |
|                                                                          |    modalità previste dal canale PSP.                                     |
|                                                                          |                                                                          |
|                                                                          | -  Il PSP rilascia l’attestazione di pagamento all’Utilizzatore finale.  |
|                                                                          |                                                                          |
|                                                                          | -  Il PSP, tramite il NodoSPC, invia la ricevuta telematica con esito    |
|                                                                          |    positivo                                                              |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| Post-Condizione                                                          | Al termine del caso d’uso il pagamento risulta completato con lo stato   |
|                                                                          | *RT EC*.                                                                 |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+

|image43|

**Fig. XX - XX**

1. l’Utilizzatore finale presenta un avviso di pagamento presso uno dei canali messi a disposizione dal PSP;

2. il PSP acquisisce le informazioni contenute dall’avviso di pagamento tramite lettura del codice QR-Code (ISO 18004). La lettura del QR-Code riporta
   una stringa composta dalla concatenazione dei seguenti campi.

..

   PAGOPA|002|<Numero Avviso>|<Identificativo Ente>|<Importo>\|

   dove:

+---------------------+----------------------------------------------------------------------------------------------------+
| Dato                | Contenuto                                                                                          |
+=====================+====================================================================================================+
| Numero Avviso       | Contiene il Numero Avviso la cui formattazione è descritta nell’Allegato A alle Linee Guida        |
+---------------------+----------------------------------------------------------------------------------------------------+
| Identificativo Ente | Contiene l’\ *idDominio* dell’Ente Creditore che corrisponde al Codice fiscale dell’Ente Creditore |
+---------------------+----------------------------------------------------------------------------------------------------+
| Importo             | Importo del pagamento espresso in centesimi di euro                                                |
+---------------------+----------------------------------------------------------------------------------------------------+

Nel caso che la lettura ottica dei codici non sia prevista, o possibile, le stesse informazioni sono imputate in maniera manuale o dall’operatore PSP
allo sportello o dall’Utilizzatore finale attraverso *user interface* messe a disposizione dal PSP.

3. il PSP richiede, attraverso la primitiva *nodoAttivaRPT,* l’attivazione del pagamento per la posizione debitoria collegata all’avviso di pagamento.
   Al fine di completare la richiesta, il campo *codificaInfrastruttura* e la struttura *codIdRPT* dovranno essere così valorizzati:

+---------------------------+---------------------------------------------------------------------------------------------------------------------+
| codificaInfrastrutturaPSP | Assume il valore fisso: “QR-CODE”                                                                                   |
+===========================+=====================================================================================================================+
| codIdRPT                  | Struttura dati composta da:                                                                                         |
+---------------------------+---------------------------------------------------------------------------------------------------------------------+
| CF                        |    Codice Fiscale dell’Ente Creditore, valore del campo Identificativo Ente, letto tramite QR-Code.                 |
+---------------------------+---------------------------------------------------------------------------------------------------------------------+
| CodStazPA                 |    Contiene il valore dell’\ *application code* o *codice segregazione* estratto dal numero di avviso (se presente) |
+---------------------------+---------------------------------------------------------------------------------------------------------------------+
| AuxDigit                  |    Contiene il codice aux-digit estratto dal numero avviso                                                          |
+---------------------------+---------------------------------------------------------------------------------------------------------------------+
| CodIUV                    |    Identificativo Univoco Versamento estratto dal Numero di Avviso                                                  |
+---------------------------+---------------------------------------------------------------------------------------------------------------------+

4. il Nodo effettua i controlli semantici e sintattici;

5. il NodoSPC provvede ad instradare la richiesta di attivazione all’EC che ha emesso l’avviso, tramite la chiamata *paaAttivaRPT*.

6. l’EC verifica le informazioni relative all’avviso e lo stato del pagamento. In caso di esito positivo, l’EC imposta lo stato del pagamento in
   IN_PAGAMENTO e genera una RPT che verrà successivamente inviata al NodoSPC tramite la primitiva *nodoInviaRPT*.

7. l’EC fornisce al NodoSPC l’esito dell’attivazione del pagamento restituendo le seguenti informazioni:

-  Importo del versamento (*ImportoSingoloVersamento*)

-  IBAN del conto corrente da accreditare (*IBANAccredito*)

-  Ente Creditore (*enteBeneficiario*)

-  Descrizione del Versamento (*causaleVersamento*)

8.  il NodoSPC inoltra le informazioni in risposta al PSP che ha effettuato la richiesta.

9.  il PSP riporta il risultato dell’operazione di attivazione all’Utilizzatore finale evidenziando il dettaglio dell’importo da pagare e la
    descrizione del versamento;

10. l’Utilizzatore finale autorizza il pagamento con le modalità proprie del canale utilizzato;

11. il PSP, a seguito dell’autorizzazione da parte dell’Utilizzatore finale, effettua il pagamento.

12. Il PSP, a seguito dell’avvenuto pagamento, rilascia all’Utilizzatore finale un attestato di pagamento

13. l’EC genera, a fronte della precedente richiesta di attivazione, una RPT valorizzata specificando il PSP indicato nella chiamata *nodoAttivaRPT*,
    in particolare:

    -  il parametro *IdentificativoPSP* deve essere valorizzato al pari del medesimo campo ricevuto dal messaggio *paaAttivaRPT;*

    -  il parametro *codiceContestoPagamento* deve essere valorizzato al pari del medesimo campo ricevuto dal messaggio *paaAttivaRPT*;

    -  la RPT deve contenere il campo *TipoVersamento* pari al valore “PO” che indica un pagamento iniziato presso il PSP;

14. il NodoSPC effettua controlli semantici e sintattici della richiesta pervenuta.

15. il NodoSPC risponde alla RPT generata;

16. il Nodo instrada la richiesta di pagamento ricevuta verso il PSP indicato all’interno della RPT

17. alla ricezione della *pspInviaRPT*, il PSP verifica l’univocità e la correttezza formale della RPT comunicando, tramite la *response* positiva, la
    presa in carico della richiesta di pagamento.

18. in merito all’operazione di pagamento, il PSP compone la RT e la invia al NodoSPC;

19. il NodoSPC effettua controlli semantici e sintattici della richiesta pervenuta;

20. il NodoSPC instrada la RT all’EC;

21. l’EC, ricevuta la RT, procede ad aggiornare l’Archivio dei Pagamenti in Attesa, lo stato del pagamento viene modificato in PAGATO;

22. l’EC notifica l’avvenuta ricezione della RT al NodoSPC;

23. il NodoSPC notifica al PSP la ricezione dell’RT da parte dell’EC.

Pagamento mediante Avviso (scenario alternativo) DEPRECATO
----------------------------------------------------------

+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| Pre-condizioni                                                           | L’Utilizzatore finale è in possesso di un Avviso di Pagamento.           |
+==========================================================================+==========================================================================+
| Trigger                                                                  | L’Utilizzatore finale si presenta presso uno dei canali messi a          |
|                                                                          | disposizione del PSP (ad esempio sportello fisico, punti di presenza,    |
|                                                                          | ATM, Home Banking, *mobile app*, etc.) con l’Avviso di Pagamento.        |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| Descrizione                                                              | In questo scenario il PSP decide di effettuare il pagamento dopo aver    |
|                                                                          | verificato l’Avviso di Pagamento, ma senza aver mai ricevuto alcuna RPT  |
|                                                                          | da parte dell’EC.                                                        |
|                                                                          |                                                                          |
|                                                                          | -  Il PSP acquisisce le informazioni contenute nell’avviso tramite la    |
|                                                                          |    lettura di uno degli elementi grafici presenti (QR-Code / Data        |
|                                                                          |    matrix). Deve comunque essere reso possibile l’inserimento manuale    |
|                                                                          |    degli stessi dati.                                                    |
|                                                                          |                                                                          |
|                                                                          | -  Il PSP, tramite il NodoSPC, verifica la sussistenza della posizione   |
|                                                                          |    debitoria collegata all’avviso di pagamento e determina l’importo del |
|                                                                          |    versamento richiesto dall’EC.                                         |
|                                                                          |                                                                          |
|                                                                          | -  L’Utilizzatore finale, consapevole degli eventuali differenze         |
|                                                                          |    rispetto ai dati riportati sull’avviso, autorizza il pagamento con le |
|                                                                          |    modalità previste dal canale PSP.                                     |
|                                                                          |                                                                          |
|                                                                          | -  Il PSP rilascia l’attestazione di pagamento all’Utilizzatore finale.  |
|                                                                          |                                                                          |
|                                                                          | -  Il PSP, tramite il NodoSPC, richiede l’attivazione della RPT relativa |
|                                                                          |    all’avviso di pagamento.                                              |
|                                                                          |                                                                          |
|                                                                          | -  Il PSP riceve, tramite il NodoSPC, la relativa richiesta di pagamento |
|                                                                          |    telematico (RPT).                                                     |
|                                                                          |                                                                          |
|                                                                          | Il PSP, tramite il NodoSPC, invia all’EC la relativa ricevuta telematica |
|                                                                          | con esito positivo.                                                      |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| Post-Condizione                                                          | Al termine del caso d’uso il pagamento risulta completato con lo stato   |
|                                                                          | RT EC.                                                                   |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+

|image44|

   **Figura XX – Diagramma di sequenza del pagamento con avviso di pagamento ( scenario alternativo)**

1. l’Utilizzatore finale presenta un avviso di pagamento (di cui al documento “L’avviso di Pagamento Analogico nel Sistema pagoPA”, pubblicato sul
   sito istituzionale dell’Agenzia) presso uno dei canali messi a disposizione dal PSP;

2. il PSP acquisisce le informazioni contenute dall’avviso di pagamento tramite lettura del codice QR-Code (ISO 18004). La lettura del QR-Code riporta
   una stringa composta dalla concatenazione dei seguenti campi.

..

   PAGOPA|002|<Numero Avviso>|<Identificativo Ente>|<Importo>\|

   dove:

+---------------------+----------------------------------------------------------------------------------------------------+
| Dato                | Contenuto                                                                                          |
+=====================+====================================================================================================+
| Numero Avviso       | Contiene il Numero Avviso la cui formattazione è descritta nell’Allegato A alle Linee Guida        |
+---------------------+----------------------------------------------------------------------------------------------------+
| Identificativo Ente | Contiene l’\ *idDominio* dell’Ente Creditore che corrisponde al Codice fiscale dell’Ente Creditore |
+---------------------+----------------------------------------------------------------------------------------------------+
| Importo             | Importo del pagamento espresso in centesimi di euro                                                |
+---------------------+----------------------------------------------------------------------------------------------------+

Nel caso che la lettura ottica dei codici non sia prevista o possibile le stesse informazioni sono imputate in maniera manuale o dall’operatore PSP
allo sportello o dall’utilizzatore finale attraverso *user interface* messe a disposizione dal PSP.

3. una volta acquisite le informazioni necessarie, il PSP richiede attraverso la primitiva *nodoVerificaRPT* i dettagli del pagamento per la posizione
   debitoria collegata all’avviso di pagamento. Al fine di completare la richiesta, il campo *codificaInfrastruttura* e la struttura *codIdRPT*
   dovranno essere così valorizzati:

+------------------------------+------------------------------------------------------------------------------------------------------------------+
|    codificaInfrastrutturaPSP | Assume il valore fisso: “QR-CODE”.                                                                               |
+==============================+==================================================================================================================+
|    codIdRPT                  | Struttura dati composta da                                                                                       |
+------------------------------+------------------------------------------------------------------------------------------------------------------+
|    CF                        | Codice Fiscale dell’Ente Creditore, valore del campo                                                             |
|                              |                                                                                                                  |
|                              | Identificativo Ente, letto tramite QR-Code.                                                                      |
+------------------------------+------------------------------------------------------------------------------------------------------------------+
|    CodStazPA                 | Contiene il valore dell’\ *aplication code* o *codice segregazione* estratto dal numero di avviso ( se presenti) |
+------------------------------+------------------------------------------------------------------------------------------------------------------+
|    AuxDigit                  | Contiene il codice aux-digit estratto dal numero avviso                                                          |
+------------------------------+------------------------------------------------------------------------------------------------------------------+
|    CodIUV                    | Identificativo Univoco Versamento estratto dal Numero di Avviso                                                  |
+------------------------------+------------------------------------------------------------------------------------------------------------------+

4. il Nodo effettua i controlli semantici e sintattici;

5. superati i controlli, il NodoSPC provvede ad instradare la richiesta all’EC che ha emesso l’avviso tramite la chiamata *paaVerificaRPT* riempita
   con le informazioni contenute nella *nodoVerificaRPT*.

6. alla ricezione della chiamata *paaVerificaRPT*, l’EC ricerca all’interno del proprio Archivio dei Pagamenti in Attesa (APA) la posizione debitoria
   utilizzando come chiave di ricerca lo IUV ed il CCP contenuto all’interno dei parametri della primitiva e verificandone le informazioni e lo stato
   del pagamento.

7. l’EC fornisce al NodoSPC l’esito della ricerca aggiornando le informazioni relative all’avviso di pagamento, specificando:

-  Importo del versamento (*ImportoSingoloVersamento*)

-  IBAN del conto corrente (*IBANAccredito*)

-  identificativo della banca (opzionale, *bicAccredito*)

-  Ente Creditore (*enteBeneficiario*)

-  Dettagli del soggetto pagatore (*credenzialiPagatore*)

-  Descrizione del versamento (*causaleVersamento*)

8.  il NodoSPC inoltra la risposta al PSP che ha effettuato la richiesta.

9.  il PSP riporta il risultato dell’operazione all’Utilizzatore finale;

10. l’Utilizzatore finale autorizza il pagamento;

11. il PSP, procede al pagamento del servizio identificato dall’Avviso di Pagamento.

12. Il PSP rilascia l’attestazione del pagamento all’Utilizzatore finale.

13. il PSP richiede al NodoSPC l’inoltro all’Ente Creditore della RPT. La primitiva *nodoAttivaRPT* sarà composta utilizzando i valori
    *codificaInfrastrutturaPSP*, *codiceIdRPT* e *datiPagamentoPSP* acquisiti nella fase precedente;

14. il NodoSPC effettua controlli semantici e sintattici della richiesta;

15. il NodoSPC inoltra la richiesta di attivazione del pagamento attraverso la primitiva *paaNodoAttivaRPT*, con le informazioni ricevute da parte del
    PSP.

16. alla ricezione della primitiva *paaAttivaRPT*, l’EC verifica le informazioni relative all’avviso e lo stato del pagamento. In caso di esito
    positivo, l’EC imposta lo stato del pagamento in IN_PAGAMENTO e genera una RPT che verrà successivamente inviata al NodoSPC tramite la primitiva
    *nodoInviaRPT*.

17. l’ente Creditore risponde alla richiesta di attivazione;

18. il NodoSPC inoltra l’esito della risposta al PSP;

19. l’EC genera, a fronte della precedente richiesta, una RPT valorizzata specificando il PSP indicato nella chiamata *nodoAttivaRPT*, in particolare:

    -  il parametro *IdentificativoPSP* deve essere valorizzato al pari del medesimo campo ricevuto dal messaggio *paaAttivaRPT;*

    -  il parametro *codiceContestoPagamento* deve essere valorizzato al pari del medesimo campo ricevuto dal messaggio *paaAttivaRPT*;

    -  la RPT deve contenere il campo *TipoVersamento* pari al valore “PO” che indica un pagamento iniziato presso il PSP;

20. il NodoSPC effettua controlli semantici e sintattici della richiesta pervenuta.

21. il NodoSPC risponde alla RPT generata;

22. il Nodo instrada la richiesta di pagamento ricevuta verso il PSP indicato all’interno della RPT;

23. alla ricezione della *pspInviaRPT*, il PSP notifica l’univocità e la correttezza formale della RPT;

24. a fronte del pagamento avvenuto precedentemente, il PSP compone la RT.

25. il PSP invia la RT al NodoSPC;

26. il NodoSPC effettua controlli semantici e sintattici della richiesta pervenuta;

27. il NodoSPC instrada la RT all’Ente Creditore;

28. l’EC, ricevuta la RT, procede ad aggiornare l’Archivio dei Pagamenti in Attesa, lo stato del pagamento viene modificato in PAGATO;

29. l’EC notifica l’avvenuta ricezione della RT al NodoSPC;

30. il NodoSPC notifica al PSP la ricezione dell’RT da parte dell’EC;

31. il PSP può concludere il pagamento.

Pagamento spontaneo
-------------------

+-----------+-----------------------------------------------+
| |image45| | **Paragrafo soggetto a proposta di modifica** |
+-----------+-----------------------------------------------+

+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| Pre-condizioni                                                           | Un Ente Erogatore ha messo a disposizione del NodoSPC un servizio per il |
|                                                                          | quale non è necessario inviare un Avviso di Pagamento poiché             |
|                                                                          | l’Utilizzatore finale è già in possesso di tutti i dati necessari per    |
|                                                                          | avviare il pagamento.                                                    |
+==========================================================================+==========================================================================+
| Trigger                                                                  | L’Utilizzatore finale si presenta presso uno dei canali messi a          |
|                                                                          | disposizione dal PSP in possesso di tutte le informazioni necessarie per |
|                                                                          | avviare il pagamento.                                                    |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| Descrizione                                                              | -  Attraverso il canale messo a disposizione dal PSP, l’Utilizzatore     |
|                                                                          |    finale (o l’operatore del PSP) ricerca e seleziona il servizio messo  |
|                                                                          |    a disposizione da un Ente Erogatore.                                  |
|                                                                          |                                                                          |
|                                                                          | -  Il PSP acquisisce (mediante una propria soluzione specifica) da parte |
|                                                                          |    dell’Utilizzatore finale i dati necessari alla richiesta di           |
|                                                                          |    attivazione del pagamento spontaneo.                                  |
|                                                                          |                                                                          |
|                                                                          | -  Il PSP invia, per mezzo del NodoSPC, la richiesta di pagamento        |
|                                                                          |    spontaneo all’Ente Erogatore del servizio.                            |
|                                                                          |                                                                          |
|                                                                          | -  L’Ente Erogatore, in base ai dati ricevuti, identifica l’Ente         |
|                                                                          |    Creditore del pagamento al quale invia, tramite NodoSPC, la richiesta |
|                                                                          |    di pagamento spontaneo.                                               |
|                                                                          |                                                                          |
|                                                                          | -  L’Ente Creditore, in base alla richiesta ricevuta, crea (o ricerca)   |
|                                                                          |    la relativa posizione debitoria all’interno dell’Archivio dei         |
|                                                                          |    Pagamenti in Attesa.                                                  |
|                                                                          |                                                                          |
|                                                                          | -  L’Ente crea un avviso digitale relativo alla posizione debitoria e lo |
|                                                                          |    invia al NodoSPC.                                                     |
|                                                                          |                                                                          |
|                                                                          | -  L’Ente Creditore risponde alla richiesta dell’Ente Erogatore          |
|                                                                          |    restituendo, tramite NodoSPC, l’avviso digitale relativo alla         |
|                                                                          |    posizione debitoria.                                                  |
|                                                                          |                                                                          |
|                                                                          | -  L’Ente Erogatore, tramite NodoSPC, invia al PSP l’avviso digitale     |
|                                                                          |    relativo alla posizione debitoria creata.                             |
|                                                                          |                                                                          |
|                                                                          | -  Il PSP propone all’Utilizzatore finale, il pagamento dell’avviso      |
|                                                                          |    digitale.                                                             |
|                                                                          |                                                                          |
|                                                                          | -  l’Utilizzatore finale autorizza il pagamento che prosegue come un     |
|                                                                          |    pagamento presso il PSP.                                              |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| Post-Condizione                                                          | Al termine di tale caso d’uso lo stato del pagamento è *RT_EC*.          |
|                                                                          |                                                                          |
|                                                                          | L’Utilizzatore finale possiede uno scontrino che attesta il pagamento    |
|                                                                          | del servizio e l’Ente Beneficiario ha ricevuto la RT.                    |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+

Il sequence di tale processo è ancora in fase di definizione.

.. _gestione-degli-errori-1:

Gestione degli errori
---------------------

Il paragrafo descrive la gestione degli errori nel processo di Pagamento attivato presso il PSP secondo le possibili eccezioni riportate nel Paragrafo
precedente.

**Errore di Attivazione/Verifica**

+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| Pre-condizioni                                                           | Il PSP compone e sottomette una richiesta di attivazione o verifica di   |
|                                                                          | una RPT.                                                                 |
+==========================================================================+==========================================================================+
| Descrizione                                                              | Il NodoSPC rifiuta l’attivazione o la verifica della RPT.                |
|                                                                          |                                                                          |
|                                                                          | Per semplicità il *sequence* riporta esclusivamente il caso della        |
|                                                                          | chiamata *nodoAttivaRPT*, ma il comportamento sarà il medesimo nel caso  |
|                                                                          | dell’invocazione della primitiva *nodoVerificaRPT*                       |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| Post-condizione                                                          | Lo stato del pagamento non viene modificato                              |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+

|image46|

**Figura XX - XX**

1. il PSP richiede l’attivazione di un pagamento mediante la primitiva *nodoAttivaRPT*;

2. il NodoSPC valida la richiesta;

3. il NodoSPC replica fornendo *response* con esito KO indicando un *faultBean* il cui *faultBean.faultCode* è rappresentativo dell’errore
   riscontrato.

..

   Lo stato del pagamento non viene modificato.

4. il PSP notifica all’Utilizzatore finale l’errore tecnico con un messaggio di errore esplicativo invitando eventualmente a contattare il servizio
   clienti.

Le possibili azioni di controllo sono riportate nella Tabella seguente:

+--------------------------+-----------------------+----------------------------------------------------------------------------------------------------------+
| Strategia di risoluzione | Tipologia Errore      | Azione di Controllo Suggerita                                                                            |
+==========================+=======================+==========================================================================================================+
|                          | PPT_SINTASSI_XSD      | Verificare la composizione della richiesta ed i parametri di invocazione della primitiva SOAP.           |
|                          |                       |                                                                                                          |
|                          | PPT_SINTASSI_EXTRAXSD |                                                                                                          |
+--------------------------+-----------------------+----------------------------------------------------------------------------------------------------------+
|                          | PPT_SEMANTICA         | Verificare la composizione del documento XML RPT controllando la correttezza di valorizzazione dei campi |
+--------------------------+-----------------------+----------------------------------------------------------------------------------------------------------+
|                          | PPT_IBAN_NON_CENSITO  | Verificare il valore dei parametri *ibanAccredito* ed *ibanAppoggio* presenti nelle RPT                  |
+--------------------------+-----------------------+----------------------------------------------------------------------------------------------------------+

**Tabella XX – XX**

**Pagamento non eseguibile**

+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| Pre-condizioni                                                           | Il PSP è in possesso dei dati di pagamento ottenuti mediante lettura     |
|                                                                          | dell’avviso di pagamento.                                                |
+==========================================================================+==========================================================================+
| Descrizione                                                              | L’EC, a seguito della ricezione di una primitiva *paaAttivaRPT* o        |
|                                                                          | *paaVerificaRPT*, verifica lo stato del pagamento all’interno del        |
|                                                                          | proprio Archivio Pagamenti in Attesa e riscontra uno stato del pagamento |
|                                                                          | non conforme con la richiesta pervenuta. Possono essere segnalati i      |
|                                                                          | seguenti codici di errore:                                               |
|                                                                          |                                                                          |
|                                                                          | -  PAA_PAGAMENTO_SCONOSCIUTO nel caso in cui la ricerca all’interno      |
|                                                                          |    dell’Archivio Pagamenti in Attesa non abbia dato alcun risultato.     |
|                                                                          |                                                                          |
|                                                                          | -  PAA_PAGAMENTO_DUPLICATO nel caso che lo stato della posizione         |
|                                                                          |    debitoria risulti essere PAGATO.                                      |
|                                                                          |                                                                          |
|                                                                          | -  PAA_PAGAMENTO_IN_CORSO nel caso che lo stato della posizione          |
|                                                                          |    debitoria sia PAGAMENTO_IN_CORSO.                                     |
|                                                                          |                                                                          |
|                                                                          | -  PAA_PAGAMENTO_ANNULLATO nel caso che lo stato della posizione         |
|                                                                          |    debitoria sia ….                                                      |
|                                                                          |                                                                          |
|                                                                          | -  PAA_PAGAMENTO_SCADUTO nel caso che la posizione debitoria non sia più |
|                                                                          |    solvibile. stato della posizione debitoria sia ….                     |
|                                                                          |                                                                          |
|                                                                          | -  PAA_ATTIVA_RPT_IMPORTO_NON_VALIDO, nel caso in cui l’importo          |
|                                                                          |    contenuto all’interno dell’Archivio dei Pagamenti in Attesa sia       |
|                                                                          |    diverso da quanto ricevuto.                                           |
|                                                                          |                                                                          |
|                                                                          | Per semplicità il *sequence* riporta esclusivamente il caso della        |
|                                                                          | chiamata *paaAttivaRPT*, ma il medesimo comportamento viene replicato    |
|                                                                          | nel caso della primitiva *paaVerificaRPT* .                              |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| Post-Condizione                                                          | Lo stato del pagamento non viene modificato                              |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+

|image47|

**Figura XX - XX**

1. il PSP richiede l’attivazione di un pagamento mediante la primitiva *nodoAttivaRPT*;

2. il NodoSPC inoltra la richiesta di attivazione all’EC tramite la primitiva *paaAttivaRPT;*

3. l’EC valida la richiesta, verificando lo stato e l’importo (solo nel caso di attivazione) del pagamento all’interno del proprio Archivio dei
   Pagamenti in Attesa.

4. L’EC notifica uno dei possibili *fault_code:*

-  PAA_PAGAMENTO_DUPLICATO

-  PAA_PAGAMENTO_IN_CORSO

-  PAA_PAGAMENTO_ANNULLATO

-  PAA_PAGAMENTO_SCADUTO

-  PAA_PAGAMENTO_SCONOSCIUTO

-  PAA_ATTIVA_RPT_IMPORTO_NON_VALIDO (solo in caso di attivazione)

5. Il NodoSPC inoltra l’errore al PSP tramite la *response* alla primitiva *nodoAttivaRPT* con *fault_code* PPT_ERRORE_EMESSO_DA_PAA.

Le possibili azioni di controllo sono riportate nella Tabella seguente.

+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
| Strategia di risoluzione                        | Tipologia Errore                                | Azione di Controllo Suggerita                   |
+=================================================+=================================================+=================================================+
|                                                 | PAA_PAGAMENTO_DUPLICATO                         | Il pagamento deve essere interrotto in modo da  |
|                                                 |                                                 | evitare possibili pagamenti duplicati.          |
|                                                 | PAA_PAGAMENTO_IN_CORSO                          |                                                 |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
|                                                 | PAA_PAGAMENTO_SCADUTO                           | Il pagamento deve essere interrotto in quanto   |
|                                                 |                                                 | l’EC non accetta più il pagamento. È necessario |
|                                                 | PAA_PAGAMENTO_ANNULLATO                         | che l’utente contatti il supporto messo a       |
|                                                 |                                                 | disposizione dall’EC al fine di poter           |
|                                                 |                                                 | proseguire con il pagamento.                    |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
|                                                 | PAA_PAGAMENTO_SCONOSCIUTO                       | Il pagamento deve essere interrotto. E’         |
|                                                 |                                                 | necessario attivare un TAVOLO OPERATIVO al fine |
|                                                 |                                                 | di risolvere l’anomalia.                        |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
|                                                 | PAA_ATTIVA_RPT_IMPORTO_NON_VALIDO               | Il pagamento deve essere nuovamente attivato    |
|                                                 |                                                 | con l’importo corretto riportato all’interno    |
|                                                 |                                                 | della risposta.                                 |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+

**Tabella XX - XX**

**RT respinta dal NodoSPC**

+-----------------+---------------------------------------------------------------------------------------------------------------------------+
| Pre-condizioni  | Il PSP ha effettuato il pagamento ed ha generato la RT da inviare all’EC. Lo stato del pagamento risulta RT presso PSP.   |
+=================+===========================================================================================================================+
| Descrizione     | Il NodoSPC non prende in carico la RT inviata dal PSP in seguito al verificarsi di uno dei seguenti scenari alternativi:  |
|                 |                                                                                                                           |
|                 | -  Il NodoSPC evidenzia un’incoerenza nello stato del pagamento, l’RT inviata risulta sia già stata consegnata all’EC     |
|                 |                                                                                                                           |
|                 | -  Il NodoSPC evidenzia un’incoerenza tra l’esito della RT e quello restituito durante l’operazioni di re-direct on-line. |
|                 |                                                                                                                           |
|                 | -  Il NodoSPC è indisponibile.                                                                                            |
+-----------------+---------------------------------------------------------------------------------------------------------------------------+
| Post-Condizione | Al termine di tale scenario, lo stato del pagamento non viene variato.                                                    |
+-----------------+---------------------------------------------------------------------------------------------------------------------------+

|image48|

**Figura XX - XX**

   L’evoluzione temporale è la seguente:

1. Il PSP invia la RT al NodoSPC affinché possa essere recapitato all’EC descritto nella RT.

2. Il NodoSPC effettua i controlli semantici sulla richiesta.

..

   Il workflow prosegue su uno dei due possibili scenari alternativi:

3. I controlli eseguiti dal NodoSPC evidenziano che una RT caratterizzata dagli stessi parametri chiave è già stata recapitata all’EC.

4. Il PSP deve essere in grado di gestire la segnalazione di RT duplicata evitando che la richiesta sia reiterata automaticamente e, eventualmente,
   ingaggiando il tavolo operativo per ogni altra casistica.

5. Il NodoSPC non fornisce una risposta entro i termini previsti.

6. A seguito di una mancata risposta nei tempi previsti dai livelli di servizio da parte del NodoSPC, il PSP archivia la RT al fine che possa essere
   recuperata attraverso la modalità PULL.

Le possibili azioni di controllo sono riportate nella Tabella seguente.

+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
| Strategia di risoluzione                        | Tipologia Errore                                | Azione di Controllo Suggerita                   |
+=================================================+=================================================+=================================================+
|                                                 | PPT_RT_DUPLICATA                                | L’errore riscontrato non comporta alcuna        |
|                                                 |                                                 | ripercussione in merito al pagamento in corso.  |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
|                                                 | *Timeout*                                       | In caso di mancata risposta da parte del        |
|                                                 |                                                 | NodoSPC , la RT generata deve essere archiviata |
|                                                 |                                                 | al fine di essere reperita successivamente dal  |
|                                                 |                                                 | NodoSPC.                                        |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+

**RT non consegnata all’EC**

+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| Pre-condizioni                                                           | Il PSP ha effettuato il pagamento ed ha generato la RT, accettata dal    |
|                                                                          | NodoSPC e da inviare all’EC                                              |
+==========================================================================+==========================================================================+
| Descrizione                                                              | L’EC non riceve la RT, a causa dell’impossibilità da parte del NodoSPC a |
|                                                                          | recapitare la RT consegnata dal PSP.                                     |
|                                                                          |                                                                          |
|                                                                          | Gli scenari che possono portare a tale casistica sono tre:               |
|                                                                          |                                                                          |
|                                                                          | -  L’EC evidenzia una incoerenza nello stato del pagamento, la RT        |
|                                                                          |    ricevuta risulta già pervenuta ed elaborata.                          |
|                                                                          |                                                                          |
|                                                                          | -  L’EC non può accettare la RT consegnata in quanto evidenzia un errore |
|                                                                          |    oppure non riconosce la posizione debitoria associata.                |
|                                                                          |                                                                          |
|                                                                          | -  L’EC non è raggiungibile.                                             |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| Post-Condizione                                                          | Al termine di tale scenario, il PSP deve archiviare la RT all’interno    |
|                                                                          | del proprio archivio al fine di poter essere recuperata dal NodoSPC      |
|                                                                          | attraverso la modalità PULL                                              |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+

|image49|

**Figura XX - XX**

   L’evoluzione temporale è la seguente:

1. Il NodoSPC invia la RT all’EC tramite la chiamata *paaInviaRT*

..

   A questo punto sono possibili le tre seguenti alternative:

2.  L’EC evidenzia all’interno dei propri sistemi la presenza della medesima RT in arrivo, e risponde utilizzando il *fault code* PAA_RT_DUPLICATA

3.  Il Nodo inoltra l’errore al PSP incapsulandolo all’interno del *fault code* PPT_ERRORE_EMESSO_DA_PAA

4.  Il PSP a seguito dell’inoltro dell’errore verifica lo stato del pagamento all’interno dei propri sistemi.

5.  L’EC evidenzia un errore all’interno della RT ricevuta, in particolare verifica la conformità della RT e l’associazione della stessa con un
    pagamento presente all’interno del proprio archivio pagamenti in attesa nello stato IN_PAGAMENTO.

6.  Il NodoSPC inoltra l’esito ricevuto dall’Ente, incapsulandolo all’interno del *fault code* PPT_ERRORE_EMESSO_DA_PAA

7.  Il PSP, presa nota dell’impossibilità da parte dell’EC di accettare la RT emessa, attiva il TAVOLO OPERATIVO al fine di risolvere l’anomalia.

8.  Il NodoSPC rileva che non è stato possibile contattare l’EC nei tempi previsti.

9.  Il NodoSPC notifica l’impossibilità di consegnare la RT all’EC tramite il *fault code* PPT_STAZIONE_INT_PA_IRRAGGIUNGIBILE

10. Il PSP archivia la RT al fine che possa essere recuperata attraverso la modalità PULL.

Le possibili azioni di controllo sono riportate nella Tabella seguente.

+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
| Strategia di risoluzione                        | Tipologia Errore                                | Azione di Controllo Suggerita                   |
+=================================================+=================================================+=================================================+
|                                                 | PAA_RT_DUPLICATA                                | Nessuna azione, l’errore riscontrato non        |
|                                                 |                                                 | comporta alcuna anomalia di pagamento.          |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
|                                                 | PAA_SEMANTICA                                   | A seguito di tale errore è necessario attivare  |
|                                                 |                                                 | il TAVOLO OPERATIVO per risolvere l’anomalia    |
|                                                 | PAA_RPT_SCONOSCIUTA                             |                                                 |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
|                                                 | PPT_STAZIONE_INT_PA_IRRANGIUNGIBILE             | In caso di mancata risposta da parte del        |
|                                                 |                                                 | NodoSPC , la RT generata deve essere archiviata |
|                                                 |                                                 | al fine di essere reperita dal NodoSPC          |
|                                                 |                                                 | successivamente                                 |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+

**Tabella XX - XX**

Avvisatura
==========

+-----------+-----------------------------------------------+
| |image50| | **Paragrafo soggetto a proposta di modifica** |
+-----------+-----------------------------------------------+

Scenari e casi d’uso
--------------------

La funzionalità di Avvisatura Digitale consente ad un EC la trasmissione in formato elettronico di avvisi di pagamenti bonari agli Utilizzatori finali
che si sono iscritti al servizio mediante uno o più strumenti messi a disposizione dai PSP. In tal modo sarà possibile procedere in maniera
semplificata (ovvero senza la necessità di un avviso di pagamento cartaceo) al pagamento presso il PSP.

La trasmissione dell’avviso è unidirezionale. L’EC emette un avviso digitale ogni volta che apre, aggiorna o chiude una posizione debitoria sul
proprio sistema informativo. Questa informazione è trasmessa al PSP che quindi è messo nelle condizioni di gestire di conseguenza il pagamento.

Gli attori coinvolti sono:

-  EC (Ente Creditore): rappresenta una pubblica amministrazione aderente al NodoSPC la quale necessita di notificare agli Utilizzatori finali gli
   avvisi di pagamento per mezzo di uno o più canali messi a disposizione dai PSP.

-  Utilizzatore Finale /PSP, rappresenta l’utilizzatore finale all’interno del canale messo a disponibile da un PSP. Questo attore può essere sia un
   attore primario (in caso di iscrizione al servizio), sia un attore secondario (nel caso di creazione/aggiornamento) dell’avviso.

I casi d’uso sono:

-  Iscrizione Servizio Avvisatura: l’obiettivo dell’Utilizzatore finale in questo caso d’uso è istruire il sistema al fine di ricevere (attraverso il
   canale prescelto) gli avvisi digitali di uno specifico Ente Creditore.

-  Invio Sincrono di un Avviso Digitale: l’obiettivo dell’Ente Creditore in questo caso d’uso è trasmettere l’avviso digitale al soggetto pagatore
   qualora esso sia iscritto mediante un qualsiasi canale.

-  Invio Massivo Avvisi Digitali: l’obiettivo dell’Ente Creditore è inviare molteplici avvisi digitali sino ad un massimo di 100.000 avvisi in una
   giornata.

-  Avvisatura pull: l’obiettivo dell’Utilizzatore finale in questo caso d’uso è interrogare l’EC al fine di reperire tutti gli avvisi di pagamento a
   lui intestati.

Iscrizione avvisatura
---------------------

+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| Pre-condizioni                                                           | N/A                                                                      |
+==========================================================================+==========================================================================+
| Trigger                                                                  | L’Utilizzatore finale richiede di ricevere (o non ricevere più) gli      |
|                                                                          | avvisi di pagamento tramite uno dei canali messi a disposizione dal PSP  |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| Descrizione                                                              | -  Il PSP aggiorna l’iscrizione alla ricezione degli avvisi digitali     |
|                                                                          |                                                                          |
|                                                                          | -  Il NodoSPC riceve la richiesta ed aggiorna la lista delle iscrizioni. |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| Post-Condizione                                                          | Iscrizione Avvisatura aggiornata                                         |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+

|image51|

**Fig. XX - XX**

1. l’Utilizzatore finale richiede al PSP di riceve gli Avvisi di Pagamento da parte di uno o più EC aderenti al sistema;

2. il PSP aggiorna le iscrizioni del servizio avvisatura al NodoSPC valorizzando la struttura *identificativoUnivocoSoggetto* con i dati
   dell’Utilizzatore finale ed impostando il parametro *azioneDiAggiornamento* al valore ‘A’ ( Aggiornamento) o ‘C’ (Cancellazione) nel caso in cui si
   stia richiedendo la rimozione della sottoscrizione;

3. il NodoSPC aggiunge il PSP all’elenco dei destinatari a cui inviare gli avvisi digitali che contengono il campo *codiceIdentificativoUnivoco*
   (attributo della struttura *identificativoUnivocoPagatore* che identifica un *soggettoPagatore*) pari al *codiceIdentificativoUnivoco* della
   richiesta;

4. il NodoSPC notifica l’avvenuta iscrizione del PSP.

Invio sincrono avviso digitale
------------------------------

+-----------------+--------------------------------------------------------------------------------------------------------------------------------+
| Pre-condizioni  | Esiste una posizione debitoria all’interno dell’Archivio Pagamenti in Attesa riferita al soggetto pagatore.                    |
+=================+================================================================================================================================+
| Trigger         | L’EC invia un avviso di pagamento in formato elettronico                                                                       |
+-----------------+--------------------------------------------------------------------------------------------------------------------------------+
| Descrizione     | -  L’EC prepara un avviso di pagamento digitale e lo invia al NodoSPC                                                          |
|                 |                                                                                                                                |
|                 | -  Il NodoSPC distribuisce l’avviso di pagamento digitale ai PSP secondo i criteri di registrazione al servizio di avvisatura  |
|                 |                                                                                                                                |
|                 | -  Il PSP riceve l’avviso digitale e lo notifica all’Utilizzatore finale attraverso uno dei suoi canali                        |
+-----------------+--------------------------------------------------------------------------------------------------------------------------------+
| Post-Condizione | Al termine del caso d’uso il pagamento risulta in stato PD IN ATTESA e l’Utilizzatore finale riceve la notifica del pagamento. |
+-----------------+--------------------------------------------------------------------------------------------------------------------------------+

|image52|

**Figura XX - XX**

1.  l’EC, tramite la primitiva *nodoInviaAvvisoDigitale,* richiede al NodoSPC di inoltrare l’avviso al soggetto pagatore. L’avviso digitale contiene
    al suo interno il tipo di operazione richiesta (CREAZIONE, AGGIORNAMENTO, CANCELLAZIONE);

2.  il NodoSPC verifica la struttura sintattica dell’avviso digitale ricevuto;

3.  il NodoSPC ricerca all’interno dell’archivio sottoscrizioni Avvisatura la lista dei PSP abilitati dal *soggettoPagatore* contenuto all’interno
    dell’Avviso Digitale.

4.  per ogni PSP collegato al *soggettoPagatore*, il NodoSPC inoltra l’avviso digitale con la primitiva *pspInviaAvvisoDigitale;*

5.  il PSP notifica l’avvenuta presa in carico dell’avviso tramite la *response* alla primitiva *pspInviaAvvisoDigitale;*

6.  il NodoSPC aggiorna l’esito delle richieste per il soggetto pagatore;

7.  il NodoSPC notifica l’avvenuta presa in carico di almeno un PSP collegato al servizio di avvisatura digitale per il *soggettoPagatore* dell’avviso
    inoltrato per mezzo della primitiva *nodoInviaAvvisoDigitale*.

8.  l’EC aggiorna l’Archivio dei Pagamenti in Attesa in base all’esito ottenuto dal NodoSPC.

9.  nel caso in cui il *tipoOperazione* specificato all’interno dell’avviso richieda una cancellazione di tale avviso, il PSP procede a cancellare
    l’avviso digitale all’interno dei suoi sistemi.

10. in conformità al canale sottoscritto per mezzo del PSP, il soggetto pagatore riceverà notifica dell’avviso.

Invio massivo avvisi digitali
-----------------------------

+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| Pre-condizioni                                                           | Esistono molteplici posizione debitorie all’interno dell’Archivio        |
|                                                                          | Pagamenti in Attesa.                                                     |
+==========================================================================+==========================================================================+
| Trigger                                                                  | L’EC invia al NodoSPC tramite SFTP gli avvisi di pagamento.              |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| Descrizione                                                              | -  L’EC prepara gli avvisi digitale e li invia al NodoSPC con protocollo |
|                                                                          |    SFTP                                                                  |
|                                                                          |                                                                          |
|                                                                          | -  Il NodoSPC analizza gli avvisi arrivati (eventualmente segnalando     |
|                                                                          |    eventuali anomalie) e li distribuisce ai PSP secondo i criteri di     |
|                                                                          |    registrazione al servizio di avvisatura                               |
|                                                                          |                                                                          |
|                                                                          | -  Il PSP riceve l’avviso digitale e lo notifica all’Utilizzatore finale |
|                                                                          |    attraverso uno dei suoi canali                                        |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| Post-Condizione                                                          | Al termine del caso d’uso il pagamento risulta in stato PD IN ATTESA e   |
|                                                                          | l’utilizzatore finale riceve la notifica del pagamento.                  |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+

|image53|

**Figura XX - XX**

1. l’EC, a partire dall’Archivio dei Pagamenti in Attesa, genera il file contenente l’elenco degli Avvisi Digitali;

2. l’EC comprime il file con algoritmo gzip. nominandolo secondo la seguente nomenclatura:

..

   **<idIntermediario>_<idDominio>_<idSessioneTrasmissione>_<progressivoFile>_AV**

nel quale le varie componenti assumono il seguente significato:

a) *idIntermediario:* è il codice fiscale del soggetto intermediario mittente, può coincidere con il dato <idDominio>;

b) *idDominio:* è il codice fiscale del soggetto mittente del flusso; deve coincidere con il dato identificativoDominio presente nel flusso;

c) *idSessioneTrasmissione*: è la data di invio del flusso, nel formato YYYYMMDD;

d) *progressivoFile*: è un numero di due cifre rappresentativo del file inviato nell’ambito della stessa sessione:‘00’ per il primo, ‘01’ per il
   secondo, ecc. [3]_;

Esempio: 12345678901_10987654321_20181201_00_AV.zip

3. l’EC invia il file compresso al NodoSPC utilizzando il protocollo di trasferimento dati SFTP;

4. il NodoSPC, in maniera asincrona rispetto ai dati ricevuti, estrae ed analizza il file ricevuto, e notifica la ricezione dei file creando un
   archivio in formato gzip secondo la seguente nomenclatura:

**<idIntermediario>_<idDominio>_<idSessioneTrasmissione>_<progressivoFile>_AV_ACK**

5.  il NodoSPC invia il file compresso all’EC utilizzando il protocollo di trasferimenti dati SFTP;

6.  l’EC estrae il file inviato dal NodoSPC e lo analizza verificando che tutti gli avvisi precedentemente inviati siano stati ricevuti dal NodoSPC;

7.  il NodoSPC elabora gli avvisi digitali ed individua la lista dei PSP iscritti per il soggetto pagatore;

8.  il PSP notifica la presa in carico dell’Avviso Digitale;

9.  il NodoSPC, in base alle risposte ottenute compila l’esito per la lista degli avvisi digitali.

10. il NodoSPC crea un archivio informato gzip secondo la seguente nomenclatura:

..

   **<idIntermediario>_<idDominio>_<idSessioneTrasmissione>_<progressivoFile>_ESITO**

11. il NodoSPC invia il file compresso all’EC utilizzando il protocollo di trasferimenti dati SFTP;

12. l’EC elabora il file, verificando che ogni avviso sia stato elaborato e, al fine di notificare l’avvenuta ricezione, crea un archivio in formato
    gzip secondo la seguente nomenclatura:

**<idIntermediario>_<idDominio>_<idSessioneTrasmissione>_<progressivoFile>_ESITO_ACK**

13. l’EC invia il file compresso al NodoSPC utilizzando il protocollo di trasferimenti dati SFTP;

14. il PSP , qualora il *tipoOperazione* descritto all’interno dell’avviso digitale si riferisca alla cancellazione, elimina l’avviso di pagamento dai
    canali messi a disposizione del soggetto pagatore.

Avvisatura pull
---------------

+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| Pre-condizioni                                                           | N/A.                                                                     |
+==========================================================================+==========================================================================+
| Trigger                                                                  | L’Utilizzatore finale richiede, tramite uno dei canali messi a           |
|                                                                          | disposizione del PSP, l’elenco degli avvisi digitali a lui intestati per |
|                                                                          | uno o più Enti Creditori.                                                |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| Descrizione                                                              | -  L’Utilizzatore finale richiede al PSP di visualizzare tutte posizione |
|                                                                          |    debitorie a lui intestate presso un Ente , oppure presso tutti gli    |
|                                                                          |    Enti Creditori aderenti                                               |
|                                                                          |                                                                          |
|                                                                          | -  Il PSP richiede l’elenco degli avvisi digitali al NodoSPC             |
|                                                                          |    specificando o meno l’EC                                              |
|                                                                          |                                                                          |
|                                                                          | -  Il NodoSPC contatta l’EC recuperando tutti gli avvisi digitali        |
|                                                                          |    esistenti per l’Utilizzatore finale                                   |
|                                                                          |                                                                          |
|                                                                          | -  Il NodoSPC re-inoltra l’elenco di tali avvisi ricevuti verso il PSP   |
|                                                                          |    che a sua volta li mostra all’Utilizzatore finale.                    |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| Post-Condizione                                                          | Al termine del caso d’uso il pagamento risulta in stato PD IN ATTESA e   |
|                                                                          | l’Utilizzatore finale riceve la notifica del pagamento.                  |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+

|image54|

**Fig. XX - XX**

1. l’Utilizzatore finale richiede, tramite il canale del PSP, di ricevere le posizioni debitorie a lui intestate presso uno o tutti gli EC all’interno
   di un arco temporale. E’ possibile specificare un particolare servizio;

2. il PSP identifica e verifica l’Utilizzatore finale in modo tale che esso possa ricercare esclusivamente posizione debitorie per codici fiscali che
   è lecito siano di sua conoscenza;

3. il PSP contatta l’EC indicato dall’Utilizzatore finale, per mezzo del NodoSPC, utilizzando la primitiva *nodoChiediAvvisiDigitali* ed impostando i
   parametri:

   a. *codiceFiscaleUtente*: pari al codice fiscale dell’Utilizzatore finale;

   b. *codiceFiscalePA*: pari al codice fiscale dell’EC indicato (se non presente la richiesta viene inoltrata a tutti gli EC);

   c. *periodoRiferimento*: l’arco temporale richiesto da parte dell’Utilizzatore finale;

4. il NodoSPC effettua i controlli semantici e sintattici per la richiesta pervenuta;

5. il NodoSPC inoltra la richiesta all’EC, utilizzando la primitiva *paaChiediElencoAvvisiDigitali;*

6. l’EC, ricevuta la richiesta, ricerca all’interno del proprio Archivio Pagamenti in Attesa tutte le posizioni debitorie /avvisi digitali intestati
   al codice fiscale contenuto nella richiesta;

7. l’EC fornisce l’elenco di tali avvisi digitali rispondendo alla primitiva *paaChiediElencoAvvisiDigitali;*

8. il NodoSPC inoltra gli avvisi ricevuti presso il PSP;

9. il PSP espone gli avvisi all’Utilizzatore finale.

.. _gestione-degli-errori-2:

Gestione degli errori
---------------------

Il paragrafo descrive la gestione degli errori nel processo di Avvisatura Digitale.

**Errore nella composizione sintattica**

+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| Pre-condizioni                                                           | N/A                                                                      |
+==========================================================================+==========================================================================+
| Descrizione                                                              | -  L’EC invia l’avviso di pagamento attraverso la primitiva              |
|                                                                          |    *nodoInviaAvvisoDigitale*                                             |
|                                                                          |                                                                          |
|                                                                          | -  Il NodoSPC evidenzia un errore semantico all’interno dell’avviso      |
|                                                                          |    ricevuto e lo notifica all’EC                                         |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| Post-Condizione                                                          | Al termine del caso d’uso l’EC ha evidenziato un anomalia che se non è   |
|                                                                          | in grado di risolvere necessiterà l’attivazione del tavolo operativo.    |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+

..

   |image55|

**Figura XX - XX**

   L’evoluzione temporale è la seguente:

1. L’EC invia un avviso digitale tramite la primitiva *nodoInviaAvvisoDigitale*;

2. Il NodoSPC analizza l’avviso digitale ed evidenzia un errore semantico;

3. Il NodoSPC notifica tramite la *response* della primitiva l’errore riscontrato;

4. L’EC analizza l’errore ricevuto, modifica l’avviso digitale e proverà successivamente ad inviarlo nuovamente. In caso non sia in grado di risolvere
   l’anomalia, attiverà il TAVOLO OPERATIVO.

+--------------------------+------------------+-----------------------------------------------------------------------------------+
| Strategia di risoluzione | Tipologia Errore | Azione di Controllo Suggerita                                                     |
+==========================+==================+===================================================================================+
|                          | PPT_SEMANTICA    | Verificare l’avviso digitale inviato, eventualmente attivare il TAVOLO OPERATIVO. |
+--------------------------+------------------+-----------------------------------------------------------------------------------+

**Tabella XX - XX**

**Mancata Consegna al PSP**

+-----------------+--------------------------------------------------------------------------------------------------------------------------+
| Pre-condizioni  | N/A                                                                                                                      |
+=================+==========================================================================================================================+
| Descrizione     | -  L’EC invia l’avviso di pagamento tramite la primitiva *nodoInviaAvvisoDigitale*                                       |
|                 |                                                                                                                          |
|                 | -  Il NodoSPC ricerca i PSP per i quali il SoggettoPagatore contenuto all’interno dell’avviso ha effettuato l’iscrizione |
|                 |                                                                                                                          |
|                 | -  Il NodoSPC invia l’avviso verso i PSP trovati                                                                         |
|                 |                                                                                                                          |
|                 | -  Tutti i PSP contattati risultano irraggiungibili o rifiutano l’avviso                                                 |
|                 |                                                                                                                          |
|                 | -  Il NodoSPC notifica l’assenza dei PSP all’EC                                                                          |
|                 |                                                                                                                          |
|                 | -                                                                                                                        |
+-----------------+--------------------------------------------------------------------------------------------------------------------------+
| Post-Condizione |    Il NodoSPC apre il Tavolo Operativo al fine di risolvere l’anomalia con i PSP                                         |
+-----------------+--------------------------------------------------------------------------------------------------------------------------+

|image56|

**Figura XX - XX**

   L’evoluzione temporale è la seguente:

1. L’EC invia un avviso digitale tramite la primitiva *nodoInviaAvvisoDigitale*

2. Il NodoSPC effettua controlli sintattici e semantici dell’avviso ricevuto;

3. Il NodoSPC ricerca le sottoscrizioni per il *SoggettoPagatore;*

4. Per ogni PSP iscritto inoltra l’avviso digitale.

..

   Possono verificarsi i seguenti scenari alternativi:

5. Nel caso in cui l’avviso non venga accettato dal PSP, il PSP invierà uno dei seguenti *fault code*: CANALE_SINTASSI_XSD, CANALE_SINTASSI_EXTRASD,
   CANALE_SEMANTICA

6. Il PSP non invia alcuna risposta al NodoSPC nei tempi attesi;

7. In entrambi in casi, il NodoSPC elabora l’esito dell’avviso digitale tenendo conto delle risposte (e di eventuali errori /timeout);

..

   A seconda dell’esito elaborato, possono verificarsi i seguenti scenari alternativi:

8.  Nel caso in cui tutti i PSP iscritti per il SoggettoPagatore risultino non raggiungibili (timeout) oppure non accettino l’avviso digitale, l’esito
    della richiesta da parte dell’EC sarà negativa con *fault_code* PPT_CANALE_ERRORE;

9.  L’EC deve aggiornare il proprio archivio dei pagamenti in attesa segnalando l’impossibilità di notifica digitale dell’avviso.

10. Nel caso in cui almeno uno dei PSP accetti l’avviso di pagamento inviato (codiceEsito = 1), l’esito della richiesta da parte dell’EC sarà
    positiva;

11. In caso in cui tutti i *codiceEsito* siano negativi (ma senza codici di errori) risulta impossibile notificare l’utente tramite il sistema
    (l’utente non è sottoscritto presso alcun PSP), e quindi sarà necessario notificare il *SoggettoPagatore* con altri mezzi;

+--------------------------+-------------------+---------------------------------------------------------+
| Strategia di risoluzione | Tipologia Errore  | Azione di Controllo Suggerita                           |
+==========================+===================+=========================================================+
|                          | PPT_CANALE_ERRORE | Tale condizione, potrebbe attivare il Tavolo Operativo. |
+--------------------------+-------------------+---------------------------------------------------------+

**Errore di trasferimento**

+-----------------+----------------------------------------------------------------------------------------------------------------------------+
| Pre-condizioni  |                                                                                                                            |
+=================+============================================================================================================================+
| Descrizione     | Questo caso d’uso descrive i possibili errori che possono verificarsi durante un trasferimento di dati su protocollo SFTP. |
|                 |                                                                                                                            |
|                 | Tale casistica può verificarsi sia durante l’invio di una lista di avvisi digitali che degli esiti di *ack*.               |
|                 |                                                                                                                            |
|                 | -  L’EC invia un avviso di pagamento o *ack* tramite SFTP,                                                                 |
|                 |                                                                                                                            |
|                 | -  L’EC riceve un *error code* definito dal protocollo SFTP                                                                |
|                 |                                                                                                                            |
|                 | -                                                                                                                          |
+-----------------+----------------------------------------------------------------------------------------------------------------------------+
| Post-Condizione |    L’EC attiva il TAVOLO OPERATIVO                                                                                         |
+-----------------+----------------------------------------------------------------------------------------------------------------------------+

|image57|

**Figura XX - XX**

L’evoluzione temporale può essere originata da una delle seguenti alternative:

1. L’EC invia una lista di avvisi digitali al NodoSPC tramite protocollo SFTP

2. L’EC invia una lista di esiti Ack al NodoSPC tramite protocollo SFTP

3. In entrambi i casi, il NodoSPC notifica un errore dalla lista degli *error code* del protocollo SFTP

4. L’EC analizza l’errore ricevuto, se è in grado di risolvere l’anomalia procederà a inviare nuovamente il file al NodoSPC, altrimenti dovrà attivare
   il TAVOLO OPERATIVO

**Mancata Ricezione Dati Attesi**

+-----------------+--------------------------------------------------------------------------------------------------+
| Pre-condizioni  |                                                                                                  |
+=================+==================================================================================================+
| Trigger         | Mancata ricezione dei file attesi                                                                |
+-----------------+--------------------------------------------------------------------------------------------------+
| Descrizione     | A seguito di un trasferimento eseguito con successo, non vengono ricevuti uno dei seguenti file: |
|                 |                                                                                                  |
|                 | -  file di ACK degli avvisi inviati                                                              |
|                 |                                                                                                  |
|                 | -  lista esito degli avvisi                                                                      |
+-----------------+--------------------------------------------------------------------------------------------------+
| Post-Condizione | L’EC attiva il TAVOLO OPERATIVO                                                                  |
+-----------------+--------------------------------------------------------------------------------------------------+

|image58|

**Figura XX - XX**

L’evoluzione temporale può essere originata da una delle seguenti alternative:

1. L’EC invia la lista degli avvisi digitali

2. Il NodoSPC elabora gli avvisi

3. Il NodoSPC non riesce a trasferire i file di *Ack*;

4. l’EC programmerà un nuovo trasferimento dei file. Qualora persista l’errore, l’EC attiverà il TAVOLO OPERATIVO.

5. Il NodoSPC non trasferisce i file degli esiti.

6. Se non vengono ricevuti i file degli esiti nei tempi prestabiliti, al fine di risolvere l’anomalia l’EC attiverà il TAVOLO OPERATIVO.

**Errore nel recupero degli avvisi digitali**

+-----------------+--------------------------------------------------------------------------------------------------------------+
| Pre-condizioni  | L’Utilizzatore finale richiede l’elenco delle proprie posizioni debitorie                                    |
+=================+==============================================================================================================+
| Trigger         | Mancata ricezione dei file attesi                                                                            |
+-----------------+--------------------------------------------------------------------------------------------------------------+
| Descrizione     |    Nel tentativo di recuperare gli avvisi digitali di un EC si evidenziano errori di semantica o connessione |
+-----------------+--------------------------------------------------------------------------------------------------------------+
| Post-Condizione | Necessario un nuovo trasferimento, oppure un tavolo operativo.                                               |
+-----------------+--------------------------------------------------------------------------------------------------------------+

|image59|

**Figura XX - XX**

L’evoluzione temporale è la seguente:

1. L’Utilizzatore finale tramite i canali messi a disposizione dal PSP richiede al NodoSPC l’elenco degli avvisi digitali emessi da un EC tramite la
   primitiva *nodoChiediElencoAvvisiDigitali*

2. Il NodoSPC effettua controlli sintattici e semantici

3. il NodoSPC inoltra la richiesta all’EC al fine di recuperare gli avvisi digitali

..

   Possono verificarsi i seguenti scenari alternativi:

4.  L’EC evidenzia uno o più problemi di natura semantica notificandoli al NodoSPC

5.  Il NodoSPC ritrasmette l’errore al PSP utilizzando il *fault_bean* PPT_ERRORE_EMESSO_DA_PAA

6.  Il PSP analizza l’errore ricevuto e non avendo avuto alcuna notifica di natura semantica da parte del NodoSPC, attiva il Tavolo Operativo al fine
    di risolvere l’anomalia.

7.  Il NodoSPC evidenzia una mancata risposta da parte dell’EC entro i tempi previsti.

8.  IL NodoSPC evidenzia un errore al PSP di mancato contatto con l’EC

9.  Il PSP non può procedere oltre e attiva il Tavolo Operativo al fine di risolvere l’anomalia.

10. Il NodoSPC evidenzia degli errori di natura semantica o di sintassi nella chiamata ricevuta

11. Il PSP analizza autonomamente l’errore ed interroga nuovamente il NodoSPC.

12. Il NodoSPC non riesce a contattare nella risposta il PSP

13. Il PSP non avendo ricevuto alcuna risposta da parte del NodoSPC non può procedere oltre. Piò tentare nuovamente una richiesta ed eventualmente
    attivare il Tavolo Operativo.

+--------------------------+--------------------------------+----------------------------------------------------------------------------------------------+
| Strategia di risoluzione | Tipologia Errore               | Azione di Controllo Suggerita                                                                |
+==========================+================================+==============================================================================================+
|                          | PPT_ERRORE_EMESSO_DA_PAA       | Il PSP attiva il Tavolo Operativo.                                                           |
+--------------------------+--------------------------------+----------------------------------------------------------------------------------------------+
|                          | *Timeout* da parte del NodoSPC | Il PSP può tentare di contattare nuovamente il NodoSPC , oppure attivare il Tavolo Operativo |
+--------------------------+--------------------------------+----------------------------------------------------------------------------------------------+
|                          | *Timeout* da parte dell’EC     | Il PSP deve attivare il Tavolo Operativo                                                     |
+--------------------------+--------------------------------+----------------------------------------------------------------------------------------------+

Back-office
===========

Revoca e storno
---------------

Il NodoSPC mette a disposizione degli EC e dei PSP aderenti, rispettivamente, i processi di storno e revoca di pagamento, da intendersi come
funzionalità di supporto del sistema pagoPA a cui ricorrere per sanare situazioni di eccezione. Come specificato nella figura successiva, tali
funzionalità sono istanziate per scopi di business ben definiti; ad esempio per il rientro da situazioni anomale o di incoerenza nei documenti
prodotti durante il ciclo di vita del pagamento, rispetto allo stato di fatto del pagamento stesso. Al variare del soggetto istanziante e delle
motivazioni che innescano l’esecuzione del processo, possono verificarsi le situazioni mostrate nella figura seguente.

|info|

Figura XX: Attori coinvolti nell'innesco dei processi di revoca e storno di una RT

+----------+-----------------+
| Processo | Innesco         |
+==========+=================+
| RevocaRT | Avviato dal PSP |
+----------+-----------------+
| Storno   | Avviato dall’EC |
+----------+-----------------+

Tabella XX: Soggetti che istanziano i processi di Revoca e Storno di un pagamento

Il processo di revoca può essere a sua volta diversificato sulla base delle motivazioni che ne determinano l’innesco, come da tabella successiva:

+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
| Processo                                        | Tipologia                                       | Descrizione                                     |
+=================================================+=================================================+=================================================+
| RevocaRT                                        | Annullo Tecnico                                 | Innescato dal PSP quando, in casi assolutamente |
|                                                 |                                                 | eccezionali, lo stato effettivo del pagamento   |
|                                                 |                                                 | non è coerente con i documenti in possesso      |
|                                                 |                                                 | dell’Utilizzatore finale:                       |
|                                                 |                                                 |                                                 |
|                                                 |                                                 | -  il PSP ha emesso una RT negativa e l’importo |
|                                                 |                                                 |    dovuto risulta addebitato al soggetto        |
|                                                 |                                                 |    versante il quale è in possesso di una       |
|                                                 |                                                 |    attestazione di pagamento                    |
|                                                 |                                                 |                                                 |
|                                                 |                                                 | -  Il PSP ha emesso una RT positiva ma il       |
|                                                 |                                                 |    soggetto versante non è stato addebitato     |
|                                                 |                                                 |    della somma dovuta né è in possesso di una   |
|                                                 |                                                 |    attestazione di pagamento                    |
|                                                 |                                                 |                                                 |
|                                                 |                                                 | Si fa presente che è fatto obbligo per il PSP   |
|                                                 |                                                 | di implementare le funzionalità di annullo      |
|                                                 |                                                 | tecnico e per EC di predisporre le opportune    |
|                                                 |                                                 | soluzioni tecniche per la gestione di tali      |
|                                                 |                                                 | richieste                                       |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
|                                                 | *charge-back* Utente                            | Innescato dal PSP nel caso in cui               |
|                                                 |                                                 | l’Utilizzatore finale chieda il riaccredito     |
|                                                 |                                                 | delle somme versate per un pagamento conclusosi |
|                                                 |                                                 | con esito positivo                              |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
| Storno                                          | Storno                                          | L’Utilizzatore finale richiede all’EC lo storno |
|                                                 |                                                 | delle somme precedentemente pagate al PSP.      |
|                                                 |                                                 |                                                 |
|                                                 |                                                 | Si fa presente che non è fatto obbligo al PSP   |
|                                                 |                                                 | implementare tale funzionalità                  |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+

Tabella XX: Descrizione sintetica delle motivazioni per l'innesco dei processi di revoca e storno

Processo di Revoca per Annullo Tecnico
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Il processo di revoca di una ricevuta telematica per Annullo Tecnico consente il rientro da situazioni anomale o di incoerenza nello stato di fatto
del pagamento rispetto a quanto rappresentato dalla RT generata dal PSP attestante il pagamento. Il caso d’uso nominale è rappresentato nella tabella
successiva.

+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| Pre-Condizione                                                           | -  è stata recapitata all’EC una RT positiva, ma l’Utilizzatore finale   |
|                                                                          |    non è stato addebitato                                                |
|                                                                          |                                                                          |
|                                                                          | -  è stata recapitata all’EC una RT negativa, ma l’Utilizzatore finale è |
|                                                                          |    stato addebitato                                                      |
|                                                                          |                                                                          |
|                                                                          | -  la richiesta di Annullo Tecnico è avanzata entro le ore 01:00 del     |
|                                                                          |    giorno solare successivo a quello di creazione della RT               |
|                                                                          |    (*dataOraMessaggioRicevuta*)                                          |
+==========================================================================+==========================================================================+
| Trigger                                                                  | Il PSP ha evidenza di una squadratura puntuale fra incasso e relativa RT |
|                                                                          | .                                                                        |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| Descrizione                                                              | -  il PSP sottomette al NodoSPC la richiesta di revoca di una RT;        |
|                                                                          |                                                                          |
|                                                                          | -  il NodoSPC valida la richiesta e la accetta;                          |
|                                                                          |                                                                          |
|                                                                          | -  l’EC riceve mediante il NodoSPC la richiesta di revoca;               |
|                                                                          |                                                                          |
|                                                                          | -  l’EC valida la richiesta di revoca producendo il relativo esito;      |
|                                                                          |                                                                          |
|                                                                          | -  l’EC invia al PSP, mediante il NodoSPC, l’esito della richiesta di    |
|                                                                          |    revoca                                                                |
|                                                                          |                                                                          |
|                                                                          | -  Il PSP produce e invia la RT che sovrascrive quella revocata          |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| Post-Condizione                                                          | -  Il pagamento transisce allo stato *Pagamento_revocato*                |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+

Tabella XX: Caso d'uso del processo di revoca per annullo tecnico

L’evoluzione temporale del processo di revoca è il seguente:

|C:\Users\mogi\AppData\Local\Microsoft\Windows\INetCache\Content.Outlook\2QI8WBLX\SD_Annullo_Tecnico.png|

**Figura XX: Diagramma di sequenza del processo di revoca di una RT per Annullo Tecnico**

1.  il PSP compone il documento XML per la richiesta di revoca e lo sottomette all’EC attraverso il NodoSPC mediante la primitiva
    *nodoInviaRichiestaRevoca*;

    a. In questo caso il valore del campo *tipoRevoca* all’interno della struttura *datiRevoca* sarà pari ad 1;

2.  il NodoSPC valida la richiesta inviata dal PSP;

3.  il NodoSPC inoltra la richiesta di revoca all’EC mediante la primitiva *paaInviaRichiestaRevoca*;

4.  l’EC replica al PSP fornendo esito positivo mediante *response* alla primitiva precedente;

5.  il NodoSPC inoltra la replica dell’EC al PSP fornendo *response* positiva alla primitiva di cui al punto 1.

6.  l’EC esegue il *rollback* del sistema relativamente alla posizione debitoria interessata e predispone il documento informativo XML ER attestante
    l’esito della revoca;

7.  l’EC invia il documento ER al PSP mediante il Nodo attraverso la primitiva *nodoInviaRispostaRevoca*;

8.  il NodoSPC valida il documento ER ricevuto;

9.  il NodoSPC inoltra il documento ER al PSP mediante la primitiva *pspInviaRispostaRevoca*;

10. il PSP conferma la ricezione del messaggio di esito della revoca fornendo *response* OK alla primitiva precedente;

11. il NodoSPC conferma all’EC la ricezione dell’esito della revoca da parte del PSP fornendo *response* OK alla primitiva di cui al punto 7.

Il *workflow* si conclude con l’invio da parte del PSP della RT che andrà a sovrascrivere quella revocata. In questo caso il parametro
*Forzacontrollosegno* nella SOAP *request* *nodoInviaRT* deve essere impostato a 1.

Processo di Revoca di una Ricevuta Telematica per *charge-back*
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Il processo di revoca per *charge-back* di una RT è innescato dal PSP solo verso l’EC che aderisce al servizio e sarà realizzabile solo per i
pagamenti effettivamente revocabili (sono esclusi tutti i pagamenti a fronte di servizi già erogati al momento della richiesta di *charge-back*)
purché la posizione debitoria dell’utilizzatore finale risulti pagata. Il caso d’uso nominale è così descritto:

+-----------------+-----------------------------------------------------------------------------------------------------+
| Pre-Condizione  | -  Pagamento effettuato con esito positivo – Stato Pagamento: *RT_EC*                               |
|                 |                                                                                                     |
|                 | -  Adesione dell’EC al servizio di revoca per *charge-back*                                         |
|                 |                                                                                                     |
|                 | -  Il pagamento è rimborsabile dall’EC                                                              |
+=================+=====================================================================================================+
| Trigger         | L’Utilizzatore finale avanza la richiesta di revoca al PSP con cui ha effettuato il pagamento       |
+-----------------+-----------------------------------------------------------------------------------------------------+
| Descrizione     | -  Il PSP sottomette al NodoSPC la richiesta di revoca della RT                                     |
|                 |                                                                                                     |
|                 | -  Il NodoSPC valida la richiesta e la accetta                                                      |
|                 |                                                                                                     |
|                 | -  L’EC riceve mediante il NodoSPC la richiesta di revoca                                           |
|                 |                                                                                                     |
|                 | -  L’EC valida la richiesta di revoca, esegue il *rollback* del sistema e produce il relativo esito |
|                 |                                                                                                     |
|                 | -  L’EC invia al PSP mediante il NodoSPC l’esito della richiesta di revoca                          |
|                 |                                                                                                     |
|                 | -  Il *workflow* si conclude senza l’invio di una nuova RT                                          |
+-----------------+-----------------------------------------------------------------------------------------------------+
| Post-Condizione | -  Il pagamento transisce allo stato *Pagamento Revocato*                                           |
+-----------------+-----------------------------------------------------------------------------------------------------+

Tabella XX: Scenario d'uso del processo di revoca di una RT per *charge-back*

Al pari dei casi d’uso riportati nei capitoli precedenti, l’evoluzione temporale e le primitive coinvolte nel processo di revoca sono riportate nella
figura successiva, avendo cura di notare che il caso d’uso rappresenta lo scenario in cui le cui invocazioni SOAP si concludono con esito positivo
(esito: OK come parametro di *output*).

|C:\Users\mogi\AppData\Local\Microsoft\Windows\INetCache\Content.Outlook\2QI8WBLX\SD_ChargeBack.png|

Figura XX: Diagramma di sequenza del processo di revoca per *charge-back*

1.  l’Utilizzatore finale richiede al PSP attestante il pagamento la revoca della RT per *charge-back*;

2.  il PSP compone il documento informativo XML Richiesta di Revoca (RR) e la invia al NodoSPC mediante la primitiva SOAP *nodoInviaRichiestaRevoca;*

3.  il NodoSPC valida la richiesta di revoca;

4.  il NodoSPC invia la richiesta di revoca all’EC mediante la primitiva *paaInviaRichiestaRevoca;*

5.  l’Ente Creditore, accettata la RR, replica al PSP attraverso il NodoSPC fornendo *response* OK;

6.  il NodoSPC inoltra al PSP la replica positiva dell’EC fornendo *response* OK alla primitiva di cui al punto 2.

7.  l’EC, dopo aver verificato positivamente la possibilità di revoca della RT, riporta la Posizione Debitoria allo stato precedente al pagamento e
    procede alla generazione del documento informativo XML Esito Revoca (ER);

8.  l’EC invia il documento ER al PSP mediante il Nodo attraverso la primitiva *nodoInviaRispostaRevoca;*

9.  il NodoSPC valida il documento ER ricevuto;

10. il NodoSPC inoltra il documento ER al PSP mediante la primitiva *pspInviaRispostaRevoca;*

11. il PSP conferma la ricezione del messaggio di esito della revoca fornendo *response* OK alla primitiva precedente;

12. il NodoSPC conferma all’EC la ricezione dell’esito della revoca da parte del PSP fornendo *response* OK alla primitiva di cui al punto 8;

13. il PSP notifica l’Utilizzatore finale circa l’esito positivo della procedura di revoca della ricevuta telematica.

Processo di Storno di un pagamento
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Il processo di storno di un pagamento, attivato dall’EC, è innescato quando l’Utilizzatore finale richieda a vario titolo la cancellazione di un
pagamento precedentemente avvenuto. Il caso d’uso nominale e l’evoluzione temporale sono mostrate nella figura successiva.

+-----------------+---------------------------------------------------------------------------------------------------------------------------+
| Pre-Condizione  | -  Il PSP utilizzato per il pagamento supporti le funzionalità di storno                                                  |
|                 |                                                                                                                           |
|                 | -  Il pagamento si trova nello stato RT EC                                                                                |
+=================+===========================================================================================================================+
| Trigger         | L’utilizzatore richiede lo storno di un pagamento precedentemente avvenuto                                                |
+-----------------+---------------------------------------------------------------------------------------------------------------------------+
| Descrizione     | -  L’Ente Creditore sottomette al PSP mediante il nodo una richiesta di storno generando il documento RR-Richiesta Revoca |
|                 |                                                                                                                           |
|                 | -  Il PSP replica positivamente e genera il documento ER inviato all’Ente Creditore mediante il NodoSPC.                  |
+-----------------+---------------------------------------------------------------------------------------------------------------------------+
| Post-Condizione | -  Il pagamento si trova nello stato RT Stornata                                                                          |
+-----------------+---------------------------------------------------------------------------------------------------------------------------+

Tabella XX: Caso d'uso del processo di storno di un pagamento

|image63|

Tabella XX: Evoluzione temporale del processo di storno di un pagamento

1.  l’Utilizzatore finale richiede lo storno di un pagamento effettuato all’EC;

2.  l’EC genera il documento XML RR;

3.  mediante la primitiva *nodoInviaRichiestaStorno* l’EC invia al NodoSPC il documento RR;

4.  il NodoSPC valida il documento RR ricevuto;

5.  il NodoSPC inoltra al PSP la RR generata dall’EC mediante la primitiva *pspInviaRichiestaStorno;*

6.  il PSP replica positivamente alla primitiva precedente fornendo *Esito* OK\ *;*

7.  il NodoSPC inoltra la replica precedente all’EC fornendo *response* OK alla primitiva di cui al punto 3;

8.  il PSP predispone il documento Esito Revoca – RR;

9.  il PSP inoltra all’EC mediante il NodoSPC l’esito della revoca attraverso la primitiva *nodoInviaEsitoStorno;*

10. il NodoSPC valida il documento ER;

11. il NodoSPC inoltra all’Ente Creditore il documento ER mediante la primitiva *paaInviaEsitoStorno;*

12. l’EC replica positivamente al PSP mediante il NodoSPC fornendo *response* OK alla primitiva di cui al punto 11;

13. il NodoSPC inoltra la replica precedente al PSP fornendo *response* OK mediante la primitiva *nodoInviaEsitoStorno;*

14. l’EC informa l’Utilizzatore finale in merito all’esito delle operazioni di storno.

Riconciliazione
---------------

All’interno di questo paragrafo vengono descritti i casi d’uso che descrivono il processo contabile operato dall’Ente Creditore al fine di
riconciliare i pagamenti effettuati dall’Utilizzatore finale.

Attori del processo di Riconciliazione Contabile e casi d’uso
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Gli attori coinvolti nel processo di riconciliazione sono i seguenti:

-  **Ente Creditore:** rappresenta una Pubblica Amministrazione che ha ricevuto i pagamenti effettuati dall’Utilizzatore finale e necessita di
   riconciliare i pagamenti a suo favore

-  **PSP:** rappresenta un Prestatore di Servizi di Pagamento che ha accreditato il conto di un EC con le somme incassate nella giornata operativa

-  **Banca Tesoriera/ Cassiera:** rappresenta il Prestatore di Servizi di Pagamento che gestisce il conto di incasso di un EC. E’ il destinatario del
   flusso di riversamento SCT e notifica all’EC l’avvenuto incasso su sistemi esterni a pagoPA

*Worflow* di Riconciliazione
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Il processo di riconciliazione comporta il seguente *workflow* dove saranno utilizzati i seguenti termini:

-  Giorno D: giorno lavorativo in cui è stato eseguito il pagamento

-  Giorno D+1: giorno lavorativo successivo al giorno D

-  Giorno D+2: giorno lavorativo successivo al giorno D+1

-  *Cut-off*: orario di termine della giornata operativa. (NB la giornata operativa pagoPA termina alle ore 13)

+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| Pre-Condizione                                                           | -  L’EC ha ricevuto dei pagamenti su un conto destinato all’incasso      |
|                                                                          |    tramite pagoPA                                                        |
|                                                                          |                                                                          |
|                                                                          | -  Entro D+1 il PSP accredita (con uno o più SCT) il conto dell’EC per   |
|                                                                          |    l’importo delle somme relative a RPT con valore del *tag*             |
|                                                                          |    *dataOraMessaggioRichiesta* antecedente al *cut-off* della giornata   |
|                                                                          |    operativa pagoPA del giorno D.                                        |
|                                                                          |                                                                          |
|                                                                          | -  Per ogni SCT cumulativo di più pagamenti, il PSP genera un flusso di  |
|                                                                          |    rendicontazione, contenente la distinta dei pagamenti cumulati.       |
|                                                                          |                                                                          |
|                                                                          | -  Entro D+2 il PSP sottomette al NodoSPC il flusso di rendicontazione   |
|                                                                          |    di cui al punto precedente.                                           |
|                                                                          |                                                                          |
|                                                                          | -  Il Nodo valida la richiesta e archivia il flusso rendendolo           |
|                                                                          |    disponibile per l’EC.                                                 |
+==========================================================================+==========================================================================+
| Trigger                                                                  | L’EC riconcilia gli accrediti SCT ricevuti sul conto indicato nelle RPT  |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| Descrizione                                                              | -  L’EC richiede la lista dei flussi disponibili sul Nodo relativa ai    |
|                                                                          |    pagamenti da riconciliare.                                            |
|                                                                          |                                                                          |
|                                                                          | -  L’EC richiede il flusso di interesse, lo riceve e procede alla        |
|                                                                          |    riconciliazione dei pagamenti.                                        |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| Post-Condizione                                                          | Il pagamento transisce allo stato *Pagamento Rendicontato*               |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+

L’evoluzione temporale è la seguente:

|image64|

Figura XX: Diagramma di sequenza del processo di riconciliazione contabile

1. il PSP accredita con SCT il conto di un EC. L’importo dello SCT può essere pari all’importo di un singolo pagamento ovvero pari all’importo
   cumulativo di più pagamenti, purché tali pagamenti siano stati incassati a favore del medesimo EC nella medesima giornata operativa pagoPA.

Nel caso di riversamento cumulativo, l’SCT dovrà riportare all’interno dell’attributo AT-05 *(Unstructured Remittance Information*) il valore:

/PUR/LGPE-RIVERSAMENTO/URI/<identificativoFlusso>,

dove *identificativoFlusso* specifica il dato relativo all’informazione di rendicontazione inviata al NodoSPC.

Nel caso di riversamento singolo, l’SCT dovrà riportare all’interno dell’attributo AT-05 *(Unstructured Remittance Information*) il valore della
causale di versamento indicato nella RPT.

2. il PSP genera il flusso di rendicontazione componendo il file XML di rendicontazione codificato in *base64*;

3. il PSP pone il file XML di rendicontazione nella propria coda di invio.

Sono possibili i seguenti scenari:

   **Utilizzo della componente SFTP_NodoSPC**

4. il PSP, autenticandosi mediante *username* e *password*, invia il file XML di rendicontazione alla componente server SFTP_NodoSPC all’interno della
   *directory* assegnata;

5. il PSP segnala al NodoSPC la presenza di un nuovo flusso di rendicontazione da elaborare mediante la primitiva SOAP
   *nodoInviaFlussoRendicontazione*; in particolare:

   a. valorizza il parametro di input *identificativoFlusso* con il medesimo valore del campo *identificativoFlusso* contenuto nel file XML di
      rendicontazione inviato nel punto 4;

   b. non valorizza il parametro di input *XMLRendicontazione* (invio già effettuato nel punto 4);

6. il NodoSPC preleva dalla *directory* assegnata al PSP il file XML di rendicontazione\ *;*

..

   **Utilizzo primitiva SOAP**

7. il PSP, mediante la primitiva *nodoInviaFlussoRendicontazione*, invia al NodoSPC il flusso di rendicontazione generato, valorizzando i parametri di
   input *identificativoFlusso* con l’identificativo del flusso di rendicontazione da trasmettere e il parametro *xmlRendicontazione* con il file XML
   di rendicontazione codificato in base64.

..

   Eseguito uno dei due scenari alternativi, il flusso procede come segue:

8.  il NodoSPC verifica il file XML di rendicontazione;

9.  il NodoSPC elabora il file XML di rendicontazione\ *;*

10. il NodoSPC esegue l’archiviazione del flusso di rendicontazione sulle proprie basi di dati;

11. il NodoSPC replica fornendo esito OK alla primitiva *nodoInviaFlussoRendicontazione;*

12. il PSP rimuove il file XML di rendicontazione dalla coda di invio.

..

   Il *workflow* prosegue descrivendo le operazioni lato EC. Il consumo delle interfacce esposte dal NodoSPC avviene in modalità *pull*.

13. l’EC, mediante la primitiva *nodoChiediElencoFlussiRendicontazione,* richiede al NodoSPC la lista dei flussi di rendicontazione disponibili;

14. il NodoSPC elabora la richiesta;

15. il NodoSPC, a seguito della validazione della richiesta, replica con *response* OK fornendo in output la lista completa di tutti i flussi
    disponibili per l’EC;

16. l’EC richiede al NodoSPC uno specifico flusso di rendicontazione presente nella lista, mediante la primitiva *nodoChiediFlussoRendicontazione*
    valorizzando nella *request* il parametro di input *identificativoFlusso* con l’identificativo del flusso di rendicontazione richiesto\ *;*

17. il NodoSPC elabora la richiesta.

..

   Il *workflow* prosegue con i seguenti scenari alternativi:

   **Flusso mediante response SOAP**

18. il Nodo invia all’Ente Creditore il flusso richiesto mediante *response* positiva alla primitiva di cui al punto 16.

..

   **Flusso mediante protocollo SFTP**

19. il NodoSPC colloca il file XML di rendicontazione richiesto nella *directory* assegnata all’EC;

20. il Nodo invia all’EC *response* OK (senza flusso allegato) per segnalare la possibilità da parte dell’EC di poter procedere al prelievo del file
    XML dalla *directory* assegnata nella componente SFTP_NodoSPC;

21. l’EC preleva il file XML di rendicontazione dalla componente SFTP_NodoSPC;

22. l’EC elabora il flusso di rendicontazione veicolandolo verso i propri sistemi di riconciliazione;

23. l’EC riceve dalla propria Banca di Tesoreria in modalità digitale un flusso contenente i movimenti registrati sul proprio conto; in caso di
    utilizzo da parte dell’EC di SIOPE+, tale flusso è rappresentato dal Giornale di Cassa nel formato OPI;

24. L’EC, sulla base dell’identificativo flusso ricevuto nel file XML di rendicontazione e delle RT archiviate, effettua la riconciliazione contabile.

*Motore di Riconciliazione*
~~~~~~~~~~~~~~~~~~~~~~~~~~~

L’obiettivo del presente paragrafo è quello di tratteggiare per termini essenziali il modello concettuale di un algoritmo che consenta all’EC di
riconciliare i flussi informativi degli incassi messi a disposizioni da pagoPA con quelli finanziari.

Nell’ipotesi semplificativa in cui la data richiesta per il pagamento coincida con la data di invio della richiesta di pagamento, il processo di
riconciliazione opera riproducendo ricorsivamente un ciclo di quattro passi da compiersi nella successione riportata di seguito per ogni PSP aderente
al NodoSPC:

1. a chiusura del giorno lavorativo (D), il motore individua le RPT inviate prima del *cut-off*. Per ognuna di tali RPT il motore seleziona le
   corrispondenti RT, ne controlla la quadratura e distingue, accantonandole, quelle relative a un incasso (RT+);

2. nel giorno D+1, la Banca Cassiera/Tesoriera riceve da ogni PSP, tramite SCT, i flussi finanziari relativi agli incassi del giorno D. In generale,
   per ogni PSP, l’EC può ricevere un SCT cumulativo e un numero indeterminato di SCT singoli relativi a una sola RT+;

3. nel giorno D+2 il motore, interrogando il NodoSPC, può effettuare il downloading del Flusso di Rendicontazione (FDR) relativo al giorno D. Il
   motore può quindi controllare la quadratura dello FDR, abbinando ad esso, in base allo IUV, le RT+ relative al giorno D. Per ogni PSP, il motore
   distingue e accantona le RT+ non abbinate a un FDR (RT:sub:`S`);

4. a chiusura del giorno lavorativo D+2 il motore elabora tutte le notifiche di incasso relative al giorno D+1 ricevute dalla Banca Cassiera/Tesoriera
   (nel caso SIOPE+ la notifica è rappresentata dal "Giornale di Cassa" OPI). Per ogni PSP il motore conclude il processo di riconciliazione:

   -  controlla la quadratura di ogni riversamento singolo, abbinandolo alla corrispondente RT\ :sub:`S;`

   -  controlla la quadratura di ogni riversamento cumulativo, abbinandolo al corrispondente FDR.

.. _gestione-degli-errori-3:

Gestione degli errori
---------------------

Gestione degli errori di revoca 
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Il paragrafo mostra i casi di errore che si possono verificare durante il processo di richiesta di revoca di una Ricevuta Telematica, sia nel caso di
revoca per Annullo Tecnico che per Charge-Back. Con assoluta generalità si documentano nei paragrafi successivi le tipologie di errori che afferiscono
alle categorie “Errori Controparte” ed “Errori Validazione”; come specificato nel paragrafo Architettura Funzionale. Nell’analisi degli scenari si
assume l’ulteriore semplificazione che l’interazione applicativa tra il NodoSPC ed i soggetti fruitori dei servizi esposti dal Nodo stesso non sia
soggetta a fenomeni di timeout o congestione di rete. Si fa presente che nella gestione del ciclo di vita del pagamento tutti i casi riportati in
seguito comportano la mancata ricezione del documento ER attestante l’esito positivo o meno del processo di revoca del pagamento.

**RR Rifiutata dal NodoSPC**

+-----------------+-----------------------------------------------------------------------------------------------------------------------------------+
| Pre-condizione  | Il PSP sottomette all’EC una Richiesta di Revoca di una RT                                                                        |
+=================+===================================================================================================================================+
| Descrizione     | Il NodoSPC esegue la validazione del documento RR replicando esito KO all’invocazione di invio richiesta revoca da parte del PSP. |
+-----------------+-----------------------------------------------------------------------------------------------------------------------------------+
| Post-condizione | Lo stato del pagamento è in Revoca Rifiutata                                                                                      |
+-----------------+-----------------------------------------------------------------------------------------------------------------------------------+

|SD_ERR_nodoInviaRichiestaRevoca|

Figura XX: Diagramma di sequenza nel caso di RR rifiutata dal Nodo

L’evoluzione temporale è la seguente:

1. l’utilizzatore finale richiede la revoca di una RT [4]_;

2. il PSP sottomette al NodoSPC il documento RR mediante la primitiva *nodoInviaRichiestaRevoca;*

3. il NodoSPC valida la richiesta;

4. il NodoSPC emana *response* KO emanando un *faultBean* il cui *faultBean.faultCode* è rappresentativo dell’errore riscontrato; in particolare:

   -  PPT_SINTASSI EXTRAXSD: in caso di errori nella SOAP *request*

   -  PPT_SINTASSI_XSD: in caso di errori nel documento XML RR

   -  PPT_RR_DUPLICATA: in caso di sottomissione di una richiesta di revoca precedentemente sottomessa

   -  PPT_OPER_NON_REVOCABILE: nel caso non sussistano le condizioni per poter fruire del servizio di revoca (vedi caso d’uso nominale)

   -  PPT_SEMANTICA: nel caso di errori semantici

5. il PSP comunica all’Utilizzatore Finale l’impossibilità di procedere nell’operazione di revoca [5]_.

Le azioni di controllo suggerite sono riportate nella Tabella successiva

+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
| Strategia di risoluzione                        | Tipologia Errore                                | Azione di Controllo Suggerita                   |
+=================================================+=================================================+=================================================+
|                                                 | PPT_OPER_NON_REVOCABILE                         | Verificare la revocabilità dell’operazione      |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
|                                                 | PPT_RR_DUPLICATA                                | Verificare la composizione del documento XML RR |
|                                                 |                                                 | e della SOAP *request* (vedi documento “Elenco  |
|                                                 |                                                 | Controlli Primitive NodoSPC” per la relativa    |
|                                                 |                                                 | primitiva/\ *FAULT_CODE*)                       |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
|                                                 | PPT_SINTASSI_EXTRAXSD                           |                                                 |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
|                                                 | PPT_SINTASSI_XSD                                |                                                 |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
|                                                 | PPT_SEMANTICA                                   | Verificare la composizione del documento XML RR |
|                                                 |                                                 | (vedi documento “Elenco Controlli Primitive     |
|                                                 |                                                 | NodoSPC” per la relativa                        |
|                                                 |                                                 | primitiva/\ *FAULT_CODE*)                       |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+

Tabella XX: Strategie di risoluzione nel caso di RR rifiutata dal Nodo

**RR rifiutata dall’EC**

+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| Pre-condizione                                                           | Il PSP sottomette all’EC una Richiesta di Revoca di una RT               |
+==========================================================================+==========================================================================+
| Descrizione                                                              | Il NodoSPC valida positivamente il documento informativo RR:             |
|                                                                          |                                                                          |
|                                                                          | -  l’EC risponde negativamente alla revoca                               |
|                                                                          |                                                                          |
|                                                                          | -  Il NodoSPC propaga al PSP l’errore emesso dall’EC mediante il         |
|                                                                          |    *faultBean* il cui *faultBean.faultCode* è pari a                     |
|                                                                          |    PPT_ERRORE_EMESSO_DA_PAA                                              |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| Post-condizione                                                          | Lo stato del pagamento è in Revoca Rifiutata                             |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+

|C:\Users\gianni.papetti\AppData\Local\Microsoft\Windows\INetCache\Content.Word\SD_ERR_paaInviaRichiestaRevoca.png|

Figura XX: Diagramma di sequenza per il caso di errore di RR rifiutata dall'EC

L’evoluzione temporale del caso d’uso è la seguente (dal punto 4):

1. il Nodo invia all’EC la Richiesta di Revoca mediante la primitiva *paaInviaRichiestaRevoca;*

2. l’EC fornisce esito KO nella *response* emanando un *faultBean* il cui *faultBean.faultCode* è rappresentativo dell’errore riscontrato; in
   particolare:

   -  PAA_RR_DUPLICATA nel caso il PSP sottomette una richiesta di revoca precedentemente gestita

   -  PAA_OPER_NON_REVOCABILE

3. il NodoSPC inoltra l’errore emesso dall’EC fornendo *response* KO alla primitiva di cui al punto 1 dello scenario precedente.

La Tabella successiva mostra le azioni di controllo suggerite per la risoluzione dell’anomalia.

+--------------------------+--------------------------+----------------------------------+
| Strategia di risoluzione | Tipologia Errore         | Azione di Controllo Suggerita    |
+==========================+==========================+==================================+
|                          | PPT_ERRORE_EMESSO_DA_PAA | Attivazione del Tavolo Operativo |
+--------------------------+--------------------------+----------------------------------+

Figura XX: Strategia di risoluzione dello scenario RR rifiutata dall'EC

**ER Rifiutata dal NodoSPC**

+-----------------+-----------------------------------------------------------------------------------+
| Pre-condizione  | L’EC ha verificato la revocabilità di una RT a seguito di una richiesta di revoca |
+=================+===================================================================================+
| Descrizione     | -  L’EC compone il documento informativo di esito revoca ER e lo invia al NodoSPC |
|                 |                                                                                   |
|                 | -  Il NodoSPC esegue la validazione replicando con esito negativo                 |
+-----------------+-----------------------------------------------------------------------------------+
| Post-condizione | Lo stato del pagamento è in Esito Revoca Rifiutata                                |
+-----------------+-----------------------------------------------------------------------------------+

|SD_ERR_nodoInviaRispostaRevoca|

Figura XX: Diagramma di sequenza per lo scenario di ER rifiutata dal Nodo

L’evoluzione temporale dello scenario è il seguente­:

1. l’EC predispone il documento ER;

2. l’EC invia al NodoSPC il documento ER mediante la primitiva *nodoInviaRispostaRevoca;*

3. il NodoSPC valida negativamente il documento ER;

4. Il Nodo fornisce esito KO nella *response* della primitiva di cui al punto 2 dove il valore del parametro *faultBean.faultCode* è rappresentativo
   dell’errore riscontrato; in particolare:

   -  PPT_ER_DUPLICATA nel caso di sottomissione di una ER già inoltrata

   -  PPT_RR_SCONOSCIUTA nel caso in cui rispetto all’ER inviato non risultasse alcuna RR precedentemente gestita

La Tabella successiva mostra le azioni di controllo suggerite per la risoluzione delle anomalie

+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
| Strategia di risoluzione                        | Tipologia di Errore                             | Azione di Controllo Suggerita                   |
+=================================================+=================================================+=================================================+
|                                                 | PPT_OPER_NON_REVOCABILE                         | Verificare la revocabilità dell’operazione      |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
|                                                 | PPT_RR_DUPLICATA                                | Verificare la composizione del documento XML RR |
|                                                 |                                                 | (vedi documento “Elenco Controlli Primitive     |
|                                                 |                                                 | NodoSPC” per la relativa                        |
|                                                 |                                                 | primitiva/\ *FAULT_CODE*) e della SOAP          |
|                                                 |                                                 | *request*                                       |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
|                                                 | PPT_SINTASSI_EXTRAXSD                           |                                                 |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
|                                                 | PPT_SINTASSI_XSD                                |                                                 |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
|                                                 | PPT_SEMANTICA                                   | Verificare la composizione del documento XML RR |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+

Tabella XX: Azioni di controllo per la risoluzione dello scenario di ER rifiutata dal Nodo

**ER Rifiutata dal PSP**

+-----------------+----------------------------------------------------------------------------------+
| Pre-condizione  | Il NodoSPC ha validato il documento ER                                           |
+=================+==================================================================================+
| Descrizione     | Il PSP replica con esito KO alla invio della Esito della Revoca da parte dell’EC |
+-----------------+----------------------------------------------------------------------------------+
| Post-condizione | Lo stato del pagamento è in Esito Revoca Rifiutata                               |
+-----------------+----------------------------------------------------------------------------------+

|SD_ERR_nodoInviaRispostaRevoca_ERR_PSP|

Figura XX: Diagramma di sequenza per il caso ER rifiutata dal PSP

L’evoluzione dello scenario in esame è il seguente (si assume validazione positiva da parte del NodoSPC, punto 3)

1. il Nodo sottomette l’ER al PSP mediante la primitiva *pspInviaRispostaRevoca;*

2. il PSP replica negativamente alla primitiva precedente fornendo *response* KO dove il valore del parametro *faultBean.faultCode* è rappresentativo
   dell’errore riscontrato; in particolare:

   -  CANALE_ER_DUPLICATA nel caso di ricezione di un ER precedentemente sottomessa

   -  CANALE_RR_SCONOSCIUTA nel caso l’ER sottomesso dal NodoSPC non corrisponda ad una precedente RR.

La Tabella successiva mostra le azioni di controllo suggerite per la risoluzione dell’anomalia

+--------------------------+--------------------------+----------------------------------+
| Strategia di risoluzione | Tipologia Errore         | Azione di Controllo Suggerita    |
+==========================+==========================+==================================+
|                          | PPT_ERRORE_EMESSO_DA_PAA | Attivazione del Tavolo Operativo |
+--------------------------+--------------------------+----------------------------------+

Figura XX: Strategia di risoluzione dello scenario RR rifiutata dall'EC

Gestione degli errori di storno 
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Il paragrafo mostra i casi di errore che si possono verificare durante il processo di storno di un pagamento. Con assoluta generalità si documentano
le tipologie di errori riportate nei paragrafi successivi che afferiscono alle categorie “Errori Controparte” ed “Errori Validazione”. Nell’analisi
degli scenari si assume l’ulteriore semplificazione che l’interazione applicativa tra il NodoSPC ed i soggetti fruitori dei servizi esposti dal Nodo
stesso non sia soggetta a fenomeni di timeout o congestione di rete. Si fa presente che nella gestione del ciclo di vita del pagamento tutti i casi
riportati in seguito comportano la mancata ricezione del documento ER attestante l’esito positivo o meno del processo di storno del pagamento.

**Richiesta Storno rifiutata dal Nodo**

+-----------------+---------------------------------------------------------------------+
| Pre-condizione  | L’EC esegue una richiesta di storno                                 |
+=================+=====================================================================+
| Descrizione     | Il Nodo a seguito della validazione replica fornendo esito negativo |
+-----------------+---------------------------------------------------------------------+
| Post-condizione | Il pagamento si trova in stato Storno Rifiutato                     |
+-----------------+---------------------------------------------------------------------+

|image69|

Tabella XX: Diagramma di sequenza dello scenario richiesta storno rifiutata dal Nodo

L’evoluzione temporale è la seguente:

1. l’Utilizzatore finale richiede all’EC lo storno di un pagamento;

2. l’EC genera il documento xml RR;

3. l’EC sottomette al NodoSPC il documento RR mediante la primitiva *nodoInviaRichiestaStorno;*

4. il NodoSPC valida il documento RR;

5. il NodoSPC replica negativamente alla primitiva precedente fornendo *response* KO dove il valore del parametro *faultBean.faultCode* è
   rappresentativo dell’errore riscontrato; in particolare:

   -  PPT_OPER_NON_STORNABILE nel caso in cui il PSP con il quale è stato effettuato il pagamento non supporta le funzionalità di storno

   -  PPT_RT_SCONOSCIUTA nel caso in cui la richiesta di storno non risulti associata ad alcuna RT positiva

La tabella successiva mostra le azioni di controllo suggerite per la risoluzione delle anomalie.

+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
| Strategia di risoluzione                        | Tipologia Errore                                | Azione di Controllo Suggerita                   |
+=================================================+=================================================+=================================================+
|                                                 | PPT_SINTASSI_EXTRAXSD                           | Verificare la composizione del documento XML RR |
|                                                 |                                                 | (vedi documento “Elenco Controlli Primitive     |
|                                                 |                                                 | NodoSPC” per la relativa                        |
|                                                 |                                                 | primitiva/\ *FAULT_CODE*) e della SOAP          |
|                                                 |                                                 | *request*                                       |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
|                                                 | PPT_SINTASSI_XSD                                |                                                 |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
|                                                 | PPT_RT_SCONOSCIUTA                              | Verificare la composizione del documento XML RR |
|                                                 |                                                 | e della SOAP *request* con particolare          |
|                                                 |                                                 | riferimento alla congruenza tra dati RR e dati  |
|                                                 |                                                 | presenti nella RT attestante il pagamento da    |
|                                                 |                                                 | stornare                                        |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
|                                                 | PPT_OPER_NON_STORNABILE                         | Verificare la composizione del documento XML RR |
|                                                 |                                                 | e della SOAP *request*; verificare l’adesione   |
|                                                 |                                                 | del PSP alle funzionalità di storno.            |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
|                                                 | PPT_SEMANTICA                                   | Verificare la composizione del documento XML RR |
|                                                 |                                                 | (vedi documento “Elenco Controlli Primitive     |
|                                                 |                                                 | NodoSPC” per la relativa                        |
|                                                 |                                                 | primitiva/\ *FAULT_CODE*)                       |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+

Tabella XX: Azioni di controllo suggerite per lo scenario Richiesta Storno rifiutata dal Nodo

**Richiesta Storno Rifiutata dal PSP**

+-----------------+------------------------------------------------------------------+
| Pre-condizione  | Il NodoSPC ha validato la richiesta di storno sottomessa dall’EC |
+=================+==================================================================+
| Descrizione     | Il PSP valida la richiesta di storno e fornisce esito KO         |
+-----------------+------------------------------------------------------------------+
| Post-condizione | Il pagamento si trova in stato Storno Rifiutato                  |
+-----------------+------------------------------------------------------------------+

|SD_ERR_RICHIESTA_STORNO_KO_PSP|

Figura XX: Evoluzione temporale dello scenario richiesta storno rifiutata dal PSP

L’evoluzione temporale è la seguente (dal punto 4):

1. il NodoSPC valida positivamente la richiesta di storno;

2. il NodoSPC sottomette la richiesta di storno mediante la primitiva *pspInviaRichiestaStorno;*

3. il PSP replica con esito KO indicando un fault.bean il cui fault.code specifica l’errore riscontrato; in particolare:

-  CANALE_SEMANTICA nel caso di errori nel tracciato XML RR

-  CANALE_OPER_NON_STORNABILE nel caso di operazione non stornabile dal PSP

-  CANALE_RR_DUPLICATA nel caso in cui l’EC sottomette una richiesta di storno precedentemente inviata

-  CANALE_RT_SCONOSCIUTA nel caso in cui non sussista corrispondenza tra la richiesta di storno e la RT attestante il pagamento da stornare

4. il NodoSPC emette esito KO alla primitiva *nodoInviaRichiestaStorno* inoltrando l’errore riscontrato dal PSP emanando un *faultBean* il cui
   *faultBean.faultCode* è rappresentativo dell’errore riscontrato.

5. l’EC notifica l’utilizzatore finale dell’esito KO dell’operazione.

La tabella successiva mostra le azioni di controllo suggerite per la risoluzione dell’anomalia.

+--------------------------+-------------------+----------------------------------+
| Strategia di risoluzione | Tipologia Errore  | Azione di Controllo Suggerita    |
+==========================+===================+==================================+
|                          | PPT_CANALE_ERRORE | Attivazione del Tavolo Operativo |
+--------------------------+-------------------+----------------------------------+

Tabella XX: Azioni di controllo suggerite per lo scenario Richiesta Storno rifiutata dal PSP

**Esito Storno Rifiutato dal Nodo**

+-----------------+-----------------------------------------------------------------------------------------------------------------------+
| Pre-condizione  | Il PSP ha validato una richiesta di storno precedentemente sottomessa dal NodoSPC e procede ad inviare l’esito storno |
+=================+=======================================================================================================================+
| Descrizione     | Il NodoSPC valida negativamente l’Esito storno                                                                        |
+-----------------+-----------------------------------------------------------------------------------------------------------------------+
| Post-condizione | Il pagamento si trova in stato Storno Rifiutato                                                                       |
+-----------------+-----------------------------------------------------------------------------------------------------------------------+

|SD_ERR_ESITO_STORNO_KO_NODO|

Figura XX: Scenario Esito Storno rifiutato dal Nodo

L’evoluzione temporale è la seguente:

1. il PSP predispone il documento XML ER attestante l’esito delle operazioni di storno;

2. il PSP invia al NodoSPC il documento ER mediante la primitiva *nodoInviaEsitoStorno;*

3. il NodoSPC valida negativamente la richiesta precedente;

4. il NodoSPC fornisce *response* negativa mediante esito KO emanando un *faultBean* il cui *faultBean.FaultCode* è rappresentativo dell’errore
   riscontrato; in particolare:

   -  PPT_ER_DUPLICATA nel caso il PSP sottomette al NodoSPC un esito storno precedentemente inviato

   -  PPT_RR_SCONOSCIUTA nel caso il PSP sottomette al NodoSPC un documento ER non coerente con la precedente richiesta di storno

   -  PPT_SEMANTICA nel caso il NodoSPC riscontrasse errori nel tracciato XML ER.

La tabella successiva mostra le azioni di controllo suggerite per la risoluzione delle anomalie.

+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
| Strategia di risoluzione                        | Tipologia Errore                                | Azione di Controllo Suggerita                   |
+=================================================+=================================================+=================================================+
|                                                 | PPT_SINTASSI_EXTRAXSD                           | Verificare la composizione del documento XML RR |
|                                                 |                                                 | (vedi documento “Elenco Controlli Primitive     |
|                                                 |                                                 | NodoSPC” per la relativa                        |
|                                                 |                                                 | primitiva/\ *FAULT_CODE*) e della SOAP          |
|                                                 |                                                 | *request*                                       |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
|                                                 | PPT_SINTASSI_XSD                                |                                                 |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
|                                                 | PPT_ER_DUPLICATA                                | Verificare la composizione del documento XML RR |
|                                                 |                                                 | e della SOAP *request* con particolare          |
|                                                 |                                                 | riferimento alla congruenza tra dati RR e dati  |
|                                                 |                                                 | presenti nella RT attestante il pagamento da    |
|                                                 |                                                 | stornare                                        |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
|                                                 | PPT_RR_SCONOSCIUTA                              |                                                 |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
|                                                 | PPT_SEMANTICA                                   | Verificare la composizione del documento XML ER |
|                                                 |                                                 | Verificare la composizione del documento XML RR |
|                                                 |                                                 | (vedi documento “Elenco Controlli Primitive     |
|                                                 |                                                 | NodoSPC” per la relativa                        |
|                                                 |                                                 | primitiva/\ *FAULT_CODE*)                       |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+

Tabella XX: Strategie di risoluzione per il caso ER rifiutata dal Nodo

**Esito Storno rifiutato dall’EC**

+-----------------+-----------------------------------------------------------------------------------------------------------------------+
| Pre-condizione  | Il PSP ha validato una richiesta di storno precedentemente sottomessa dal NodoSPC e procede ad inviare l’esito storno |
+=================+=======================================================================================================================+
| Descrizione     | L’EC valida negativamente l’Esito storno                                                                              |
+-----------------+-----------------------------------------------------------------------------------------------------------------------+
| Post-condizione | Il pagamento si trova in stato Storno Rifiutato                                                                       |
+-----------------+-----------------------------------------------------------------------------------------------------------------------+

|SD_ERR_ESITO_STORNO_KO_EC|

Figura XX: Scenario Esito Storno rifiutato da EC

L’evoluzione temporale dello scenario è il seguente (dal punto 4):

1. il NodoSPC invia il documento ER all’EC mediante la primitiva *paaInviaEsitoStorno;*

2. l’EC risponde negativamente all’invocazione precedente mediante esito KO emanando un *faultBean* il cui *faultBean.faultCode* è rappresentativo
   dell’errore riscontrato; in particolare:

   a. PAA_ER_DUPLICATA nel caso l’esito storno risultasse precedentemente inviato

   b. PAA_RR_SCONOSCIUTA nel caso in cui all’ER sottomessa non corrisponda alcuna RR precedentemente generata

   c. PAA_SEMANTICA nel caso in cui si riscontrino errori nel tracciato ER

3. il NodoSPC propaga l’errore riscontato dall’EC mediante faultBean il cui faultBean.faultCode è pari a PPT_ERRORE_EMESSO_DA_PAA.

La tabella successiva mostra le azioni di controllo suggerite per la risoluzione delle anomalie

+--------------------------+--------------------------+----------------------------------+
| Strategia di risoluzione | Tipologia Errore         | Azione di Controllo Suggerita    |
+==========================+==========================+==================================+
|                          | PPT_ERRORE_EMESSO_DA_PAA | Attivazione del Tavolo Operativo |
+--------------------------+--------------------------+----------------------------------+

Tabella XX: Strategie di risoluzione per il caso ER rifiutata dall'EC

**ER Mancante per timeout delle controparti**

Gli scenari di errore proposti nei paragrafi precedenti mostrano i possibili casi di ER mancante a causa di errori applicativi rappresentati
dall’emanazione da parte degli attori coinvolti di un faultBean contenente un’eccezione applicativa appartenente ad una determinata famiglia di
errori. Un ulteriore caso da prendere in esame è rappresentato dall’impossibilità di chiusura del processo di storno nel caso in cui le parti
riscontrassero fenomeni di timeout.

+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| Pre-condizione                                                           | La posizione debitoria è nello stato Richiesta Storno Inviata            |
+==========================================================================+==========================================================================+
| Descrizione                                                              | Il PSP e l’EC riscontrano fenomeni applicativo/infrastrutturali per i    |
|                                                                          | quali si manifestano condizioni di *timeout* nell’invocazione delle      |
|                                                                          | primitive e/o nella ricezione delle relative *response*.                 |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| Post-condizione                                                          | Il pagamento permane in stato Richiesta Storno Inviata                   |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+

|SD_ERR_ESITO_STORNO_TIMEOUT|

Figura XX: Evoluzione temporale dello scenario Esito Storno mancate per timeout

L’evoluzione temporale è la seguente:

1. il PSP predispone il documento XML ER;

A questo punto sono possibili i seguenti scenari:

*Timeout* PSP in fase di invocazione

2. La primitiva *nodoInviaEsitoStorno* non va a buon fine a causa di fenomeni di congestione imputabili al NodoSPC.

*Timeout* EC

3. il PSP invia il documento ER mediante la primitiva *nodoInviaEsitoStorno*;

4. Il NodoSPC valida positivamente la richiesta.

..

   Alternativamente

5. l’EC riscontra condizioni di *timeout* per le quali fallisce l’invocazione della primitiva *paaInviaEsitoStorno;*

oppure

6. l’EC riscontra condizioni di *timeout* imputabili al NodoSPC per le quali la *response* alla primitiva *paaInviaEsitoStorno* non giunge al PSP.

..

   In ogni caso

7. il NodoSPC invia *response* KO alla primitiva *nodoInviaEsitoStorno* emanando un *faultBean* il cui *faultCode* è pari a
   PPT_STAZIONE_INT_PA_TIMEOUT.

*Timeout* PSP in ricezione *response*

8.  il PSP invia il documento ER mediante la primitiva *nodoInviaEsitoStorno*;

9.  Il NodoSPC valida positivamente la richiesta;

10. l’EC riceve l’esito storno mediante la primitiva *paaInviaEsitoStorno*;

11. l’EC emana *response* (di qualsiasi esito) alla primitiva precedente;

12. Il NodoSPC inoltra la *response* al PSP che fallisce per condizioni di *timeout*.

+--------------------------+------------------------------+----------------------------------+
| Strategia di risoluzione | Tipologia Errore             | Azione di Controllo Suggerita    |
+==========================+==============================+==================================+
|                          | PPT_STAZIONE_INT_PA_TIMEOUT  | Attivazione del Tavolo Operativo |
+--------------------------+------------------------------+----------------------------------+
|                          | Nessuna ricezione *response* |                                  |
+--------------------------+------------------------------+----------------------------------+

Tabella XX: XX

Gestione degli errori di riconciliazione 
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Il paragrafo descrive la gestione degli errori che possono verificarsi durante l’esercizio del processo di riconciliazione contabile. In particolare
sono prese in esame le eccezioni per le quali si riscontra il fallimento delle primitive in gioco oppure l’esito negativo del *workflow* di
riconciliazione; tutte le eccezioni riportate non permettono al pagamento di transire allo stato “Pagamento riconciliato”. I casi di errore descritti
prevedono l’attivazione del Tavolo Operativo [6]_ nel caso in cui i soggetti erogatori e fruitori dei servizi applicativi risultassero impossibilitati
a procedere in autonomia nella risoluzione delle anomalie oppure l’azione di controllo suggerita non risultasse risolutiva.

**SCT singolo in assenza di RPT**

+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| Pre-condizione                                                           | Il PSP ha incassato diversi servizi                                      |
+==========================================================================+==========================================================================+
| Descrizione                                                              | Nell’elaborare un SCT singolo di riversamento relativamente ad un flusso |
|                                                                          | di rendicontazione in assenza di RPT ( codice 9 ), il PSP evidenzia la   |
|                                                                          | mancanza di il PSP non evidenzia la mancanza della RPT.                  |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| Post-condizione                                                          | N/A                                                                      |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+

In caso di mancanza di RPT, il PSP non è in grado di valorizzare l’attributo AT-05 con la causale di versamento in quanto tale informazione sarebbe
dovuta essere reperibile all’interno della RPT non ricevuta.

Le possibili azioni di controllo sono riportate nella tabella successiva:

+--------------------------+------------------+--------------------------------------------+
| Strategia di risoluzione | Tipologia Errore | Azione di Controllo Suggerita              |
+==========================+==================+============================================+
|                          | Flusso codice 9  | E’ necessario attivare un TAVOLO OPERATIVO |
+--------------------------+------------------+--------------------------------------------+
|                          |                  |                                            |
+--------------------------+------------------+--------------------------------------------+

**Invio flusso rifiutato dal NodoSPC**

+-----------------+--------------------------------------------------------------------------+
| Pre-condizione  | Il PSP invia al NodoSPC un flusso di rendicontazione                     |
+=================+==========================================================================+
| Descrizione     | Il NodoSPC esegue la validazione del flusso fornendo *response* negativa |
+-----------------+--------------------------------------------------------------------------+
| Post-condizione | Lo stato del pagamento permane in *RT_PAGATA*                            |
+-----------------+--------------------------------------------------------------------------+

|SD_ERR_FLUSSO_KO_NODO|

Figura XX: Evoluzione temporale dello scenario flusso rifiutato dal Nodo

L’evoluzione temporale dello scenario è la seguente:

1. il PSP genera il flusso di rendicontazione componendo il file XML di rendicontazione codificato in *base64*;

2. il PSP pone il file XML di rendicontazione nella propria coda di invio.

Sono possibili i seguenti scenari

   Utilizzo della componente *SFTP_NodoSPC*

3. il PSP, autenticandosi mediante *username* e *password*, invia il file XML di rendicontazione alla componente server SFTP_NodoSPC all’interno della
   *directory* assegnata;

4. il PSP segnala al NodoSPC la presenza di un nuovo flusso di rendicontazione da elaborare mediante la primitiva SOAP
   *nodoInviaFlussoRendicontazione*; in particolare:

   -  valorizza il parametro di input *identificativoFlusso* con il medesimo valore del campo *identificativoFlusso* contenuto nel file XML di
      rendicontazione inviato nel punto 4;

   -  non valorizza il parametro di input *XMLRendicontazione* (invio già effettuato nel punto 4);

5. il NodoSPC preleva dalla *directory* assegnata al PSP il file XML di rendicontazione\ *;*

6. il NodoSPC verifica il file XML di rendicontazione;

..

   Utilizzo primitiva SOAP

7. il PSP, mediante la primitiva *nodoInviaFlussoRendicontazione*, invia al NodoSPC il flusso di rendicontazione generato, valorizzando i parametri di
   input *identificativoFlusso* con l’identificativo del flusso di rendicontazione da trasmettere e il parametro *xmlRendicontazione* con il file XML
   di rendicontazione codificato in base64.

8. il NodoSPC verifica il file XML di rendicontazione;

..

   Eseguito uno degli scenari alternativi, il flusso procede come segue:

9. il Nodo replica negativamente alla primitiva precedente fornendo *response* con esito KO emanando un *faultBean* il cui *faultBean.faultCode*
   rappresenta l’errore riscontrato; in particolare:

   -  PPT_FLUSSO_SCONOSCIUTO: il NodoSPC non riscontra alcuna congruenza tra il valore del parametro di input *identificativoFlusso* della primitiva
      di richiesta ed il valore del parametro *identificativoFlusso* nel file XML di rendicontazione;

   -  PPT_SEMANTICA nel caso di riscontro di errori nel tracciato *xml* del file XML di rendicontazione.

Le possibili azioni di controllo sono riportate nella tabella successiva:

+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
| Strategia di risoluzione                        | Tipologia Errore                                | Azione di Controllo Suggerita                   |
+=================================================+=================================================+=================================================+
|                                                 | PPT_FLUSSO_SCONOSCIUTO                          | Verificare la composizione della SOAP *request* |
|                                                 |                                                 | *nodoInviaFlussoRendicontazione* ed il          |
|                                                 |                                                 | contenuto del file XML di rendicontazione       |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
|                                                 | PPT_SEMANTICA                                   | Verificare la composizione del file XML di      |
|                                                 |                                                 | rendicontazione (vedi documento “Elenco         |
|                                                 |                                                 | Controlli Primitive NodoSPC” per la relativa    |
|                                                 |                                                 | primitiva/\ *FAULT_CODE*)                       |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+

Tabella XX: Strategia di risoluzione dello scenario Flusso rifiutato dal Nodo

**Timeout invio flusso di rendicontazione**

Il seguente scenario, nel trattare in generale il caso di timeout successivo all’invio del flusso di rendicontazione, si sofferma sulla gestione dei
messaggi di errore maggiormente rappresentativi.

+-----------------+-------------------------------------------------------------------------------------------------------------+
| Pre-condizione  | Il tempo di attesa della *response* del NodoSPC supera il *timeout* di cui al documento Livelli di Servizio |
+=================+=============================================================================================================+
| Descrizione     | Il NodoSPC manifesta condizioni di *timeout* ed il PSP esegue il relativo processo di gestione              |
+-----------------+-------------------------------------------------------------------------------------------------------------+
| Post-condizione | Lo stato del pagamento permane in RT_EC                                                                     |
+-----------------+-------------------------------------------------------------------------------------------------------------+

L’evoluzione temporale è la seguente:

|image75|

Figura XX: XX

1. il PSP accredita con SCT il conto dell’EC per l’importo delle somme incassate (l’SCT contiene l’indicazione del flusso di rendicontazione)

2. il PSP genera il flusso di rendicontazione componendo il file XML di rendicontazione codificato in *base64*.

..

   Si possono presentare i seguenti casi:

   Utilizzo *SFTP_NodoSPC*

3. il PSP pone il file XML di rendicontazione nella propria coda di invio;

4. il PSP invia alla componente SFTP_NodoSPC il file XML di rendicontazione;

5. il PSP avvisa il NodoSPC della presenza di un nuovo XML di rendicontazione da elaborare mediante la primitiva *nodoInviaFlussoRendicontazione*.

..

   Utilizzo primitiva SOAP

6. il PSP invia al NodoSPC il file XML di rendicontazione da elaborare mediante la primitiva *nodoInviaFlussoRendicontazione;*

..

   Eseguito uno degli scenari alternativi, il flusso procede come segue:

7.  il NodoSPC non risponde manifestando una condizione di *timeout*;

8.  il PSP richiede lo stato di elaborazione del flusso di rendicontazione inviato mediante la primitiva
    *nodoChiediStatoElaborazioneFlussoRendicontazione* valorizzando il parametro di input *identificativoFlusso* con il valore dell’identificativo
    flusso di cui richiedere lo stato;

9.  Il NodoSPC effettua il controllo sullo stato di elaborazione del flusso inviato;

10. Il NodoSPC replica mediante *response* OK alla primitiva di cui al punto 8 fornendo lo stato di elaborazione del flusso di rendicontazione; in
    particolare:

-  FLUSSO_IN_ELABORAZIONE: il NodoSPC deve terminare le operazioni di archiviazione dei flussi sulle proprie basi di dati;

-  FLUSSO_ELABORATO: il NodoSPC ha elaborato il flusso di rendicontazione inviato dal PSP;

11. il PSP gestisce lo stato riscontrato dal NodoSPC eliminando il file XML di rendicontazione nel caso di FLUSSO_ELABORATO oppure attendendo oltre
    nel caso di FLUSSO_IN_ELABORAZIONE.

**Richiesta lista flussi di rendicontazione rifiutata dal NodoSPC**

+-----------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Pre-condizioni  | La posizione debitoria si trova nello stato *PAGATA* e lo stato del pagamento è in *RT_EC.*                                          |
|                 |                                                                                                                                      |
|                 | L’EC richiede la lista dei flussi di rendicontazione                                                                                 |
+=================+======================================================================================================================================+
| Descrizione     | L’EC non riceve la lista dei flussi di rendicontazione richiesta ed è impossibilitato a procedere alla riconciliazione dei pagamenti |
+-----------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Post-condizione | Lo stato del pagamento è in *RT_EC*                                                                                                  |
+-----------------+--------------------------------------------------------------------------------------------------------------------------------------+

|SD_ERR_RICHIESTA_FLUSSI_KO|

Figura XX: XX

L’evoluzione temporale dello scenario è la seguente:

1. l’EC richiede, mediante la primitiva *nodoChiediElencoFlussiRendicontazione,* la lista dei flussi di rendicontazione archiviata sul NodoSPC\ *;*

2. Il NodoSPC valida negativamente la richiesta ed emana *response* negativa con esito KO e *faultBean.FaultCode* rappresentativo dell’errore
   riscontrato.

+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
| Strategia di risoluzione                        | Tipologia Errore                                | Azione di Controllo Suggerita                   |
+=================================================+=================================================+=================================================+
|                                                 | PPT_SINTASSI_EXTRAXSD                           | Verificare la composizione della SOAP *request* |
|                                                 |                                                 | (vedi documento “Elenco Controlli Primitive     |
|                                                 |                                                 | NodoSPC” per la relativa                        |
|                                                 |                                                 | primitiva/\ *FAULT_CODE*)                       |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
|                                                 | PPT_PSP_SCONOSCIUTO                             | Verificare il parametro *identificativoPSP*     |
|                                                 |                                                 | nella SOAP *request*                            |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+

Tabella XX: Strategia di risoluzione dello scenario richiesta lista flussi rifiutata dal Nodo

**Richiesta Flusso Rifiutata dal Nodo / Nessun flusso presente**

+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| Pre-condizione                                                           | La posizione debitoria si trova nello stato *PAGATA* e lo stato del      |
|                                                                          | pagamento è in *RT_EC e* L’EC richiede uno specifico flusso di           |
|                                                                          | rendicontazione                                                          |
+==========================================================================+==========================================================================+
| Descrizione                                                              | L’Ente Creditore non riceve lo specifico flusso richiesto                |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| Post-condizione                                                          | Lo stato del pagamento è in RT_EC                                        |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+

|SD_ERR_RICHIESTA_FLUSSO_KO|

Figura XX: Evoluzione temporale dello scenario richiesta Flusso rifiutata dal Nodo / Flusso mancate

L’evoluzione temporale dello scenario è la seguente:

1. l’EC richiede al NodoSPC uno specifico flusso di rendicontazione mediante la primitiva *nodoChiediFlussoRendicontazione;*

2. il Nodo replica negativamente alla richiesta fornendo *response* con esito KO emanando un *faultBean* il cui *faultBean.faultCode* rappresenta
   l’errore riscontrato; in particolare:

   -  PPT_SINTASSI_EXTRAXSD: nel caso di errori di invocazione della SOAP *request;*

   -  PPT_ID_FLUSSO_SCONOSCIUTO: nel caso l’EC richieda un flusso il cui *identificativoFlusso* risulti non registrato nelle basi di dati del NodoSPC;

   -  PPT_SYSTEM_ERROR: nel caso in cui il NodoSPC riscontri errori nell’inizializzazione client-side del trasferimento SFTP del flusso richiesto;

   -  PPT_FLUSSO_ESISTENTE: il flusso di rendicontazione richiesto è stato già depositato nella *directory* della componente SFTP_NodoSPC dedicata
      all’EC.

+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
| Strategia di risoluzione                        | Tipologia Errore                                | Azione di Controllo Suggerita                   |
+=================================================+=================================================+=================================================+
|                                                 | PPT_SINTASSI_EXTRAXSD                           | Verificare la composizione della richiesta SOAP |
|                                                 |                                                 | (vedi documento “Elenco Controlli Primitive     |
|                                                 |                                                 | NodoSPC” per la relativa                        |
|                                                 |                                                 | primitiva/\ *FAULT_CODE*)                       |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
|                                                 | PPT_SEMANTICA                                   |                                                 |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
|                                                 | PPT_ID_FLUSSO_SCONOSCIUTO                       | Verificare il valore del parametro di input     |
|                                                 |                                                 | IDFLUSSO nella richiesta SOAP                   |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+
|                                                 | PPT_SYSTEM_ERROR                                | Ritentare nuovamente la richiesta del flusso di |
|                                                 |                                                 | rendicontazione, altrimenti innescare il Tavolo |
|                                                 |                                                 | Operativo                                       |
+-------------------------------------------------+-------------------------------------------------+-------------------------------------------------+

Tabella XX: XX

Ausiliarie
==========

Scenari, casi d’uso e attori
----------------------------

Le funzionalità ausiliarie disponibili all’interno del Sistema pagoPA rappresentano funzionalità accessorie per la gestione dei processi correlati
alle operazioni di pagamento e possono essere utilizzate dagli EC per il rientro da situazioni anomale o per le quali si renda necessario il
ripristino di situazioni precedenti. Tali operazioni sono utilizzate anche dai PSP al fine di interrogare le basi di dati messe a disposizione dal
NodoSPC per l’esercizio del ciclo di vita del pagamento. Si fa presente che le funzionalità ausiliarie sono offerte dal NodoSPC attraverso interfacce
SOAP consumabili dagli attori coinvolti. A sua volta, anche il NodoSPC, in qualità di fruitore, utilizza le funzionalità ausiliarie messe a
disposizione dai PSP per la verifica e gestione degli errori nei processi di pagamento.

|Intro|

Figura XX: Rappresentazione degli erogatori e fruitori delle funzionalità di supporto

Funzioni Ausiliarie per L’Ente Creditore
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Il paragrafo si focalizza sulle funzioni ausiliarie del NodoSPC, ovvero quelle funzioni, dedicate all’EC, che permettono l’espletamento dei processi
correlati alle operazioni di pagamento e/o consentono la risoluzione di eventuali situazioni anomale o il rientro a stati preesistenti.

**Richiesta della copia di una RT**

L’EC ha facoltà di richiedere una copia della RT precedentemente recapitata.

+-----------------+-----------------------------------------------------------------------------------------------------------------------------------+
| Pre-Condizione  | L’EC riscontra delle condizioni anomale sui pagamenti effettuati dagli utilizzatori finali o riscontra la perdita di una o più RT |
+=================+===================================================================================================================================+
| Trigger         | Necessità di ripristino di una RT                                                                                                 |
+-----------------+-----------------------------------------------------------------------------------------------------------------------------------+
| Descrizione     | L’EC sottomette la richiesta di ricevere una specifica RT precedentemente ricevuta                                                |
+-----------------+-----------------------------------------------------------------------------------------------------------------------------------+
| Post-Condizione | L’EC riceve la RT                                                                                                                 |
+-----------------+-----------------------------------------------------------------------------------------------------------------------------------+

Tabella XX: XX

   |nodoChiediCopiaRT|

Figura XX: XX

1. l’EC sottomette al NodoSPC la richiesta di ricevere una copia della RT mediante la primitiva *nodoChiediCopiaRT;*

..

   Caso *OK*

2. La RT è correttamente trovata dal NodoSPC e restituita all’EC in allegato alla *response* positiva alla primitiva di cui al punto 1

Caso KO

3. il NodoSPC replica negativamente alla richiesta precedente fornendo *response* KO alla primitiva di cui al punto 1 emanando un *faultBean* il cui
   *faultBean.faultCode* è rappresentativo dell’errore riscontrato; in particolare:

-  PPT_SINTASSI_XSD: nel caso di errore di validazione della richiesta

-  PPT_SINTASSI_EXTRAXSD: nel caso di errore di validazione della SOAP *request*

-  PPT_SEMANTICA: nel caso di errori semantici

-  PPT_RT_SCONOSCIUTA: i parametri di input specificati nella richiesta non consentono di trovare alcuna RT

-  PPT_RT_NONDOSPONIBILE: la RT richiesta non è disponibile.

**Richiesta della Lista delle RPT Pendenti**

L’EC ha facoltà di domandare la lista delle RPT correttamente inviate al PSP tramite il NodoSPC per le quali ancora non sono state ricevute le RT.

+-----------------+------------------------------------------------------------------------------+
| Pre-Condizione  | L’EC ha sottomesso al NodoSPC un certo numero di RPT e non ha ricevuto le RT |
+=================+==============================================================================+
| Trigger         | Necessità di riconciliazione o chiusura delle posizioni pendenti             |
+-----------------+------------------------------------------------------------------------------+
| Descrizione     | L’EC sottomette la richiesta di ricevere la lista delle RPT pendenti         |
+-----------------+------------------------------------------------------------------------------+
| Post-Condizione | L’EC riceve la lista delle RPT                                               |
+-----------------+------------------------------------------------------------------------------+

Tabella XX: XX

|nodoChiediRPTPendenti|

Figura XX: XX

1. l’EC, mediante la primitiva *nodoChiediListaPendentiRPT* richiede al NodoSPC il numero e le RPT correttamente sottomesse ai PSP per le quali ancora
   non è stata ricevuta alcuna RT;

Caso OK

2. il NodoSPC replica con esito OK indicando il numero totale e le RPT pendenti consegnate al PSP scelto dall’Utilizzatore finale per le quali ancora
   non è stata consegnata al NodoSPC alcuna RT;

Caso KO

3. il NodoSPC replica con esito KO alla primitiva di cui al punto 1 emanando un *faultBean* il cui *faultBean.faultCode* è rappresentativo dell’errore
   riscontrato; in particolare:

   -  PPT_SINTASSI_EXTRAXSD: nel caso di errori nella SOAP *request*

   -  PPT_SEMANTICA: nel caso di errori semantici.

**Verifica dello stato di una RPT**

+-----------------+-------------------------------------------------------------------------+
| Pre-Condizione  | L’EC ha sottomesso al NodoSPC una RPT                                   |
+=================+=========================================================================+
| Trigger         | L’EC necessita di conoscere l’evoluzione temporale di una specifica RPT |
+-----------------+-------------------------------------------------------------------------+
| Descrizione     | L’EC sottomette la richiesta di conoscere lo stato di una specifica RPT |
+-----------------+-------------------------------------------------------------------------+
| Post-Condizione | L’EC riceve le informazioni inerenti lo stato della RPT                 |
+-----------------+-------------------------------------------------------------------------+

Tabella XX: XX

|nodoChiediStatoRPT|

Figura XX: XX

L’evoluzione temporale è la seguente:

1. l’EC richiede di conoscere lo stato di una RPT mediante la primitiva *nodoChiediStatoRPT.*

Caso OK

2. il NodoSPC replica positivamente alla primitiva di cui al punto 1 fornendo nella *response* le informazioni peculiari per il tracciamento della RPT
   stessa; in particolare:

   -  *Redirect*: specifica se il pagamento prevede o meno una *redirect*

   -  *URL*: eventuale URL di *redirezione*

   -  *STATO*: stato della RPT

   -  *Descrizione*: descrizione dello stato della RPT

   -  *versamentiLista*: struttura contenente una lista di elementi che identificano gli stati assunti da ogni singolo versamento presente nella RPT
      da quando la RPT è stata ricevuta dal PSP. Ogni elemento della lista è costituito da:

      -  *progressivo*: numero del versamento nella RPT

      -  *data*: data relativa allo stato del versamento

      -  *stato*: stato della RPT alla data indicata

      -  *descrizione*: descrizione dello stato alla data

Caso KO

3. il NodoSPC fornisce esito KO alla primitiva di cui al punto 1 emanando un *fault.Bean* il cui *faultBean.faultCode* è rappresentativo dell’errore
   riscontrato; in particolare:

   -  PPT_RPT_SCONOSCIUTA: la RPT di cui si chiede lo stato non è stata trovata

   -  PPT_SEMANTICA: nel caso di errori semantici

   -  PPT_SINTASSI_EXTRAXSD: Errore nella composizione della SOAP *request*

**Richiesta Catalogo Dati Informativi**

+-----------------+-------------------------------------------------------------------------------------------------------------------------+
| Pre-Condizione  | n.a.                                                                                                                    |
+=================+=========================================================================================================================+
| Trigger         | L’EC necessita di conoscere il Catalogo Dati Informativi elaborato dal NodoSPC per verificare i servizi erogati dai PSP |
+-----------------+-------------------------------------------------------------------------------------------------------------------------+
| Descrizione     | L’EC sottomette la richiesta di scaricare il Catalogo Dati Informativi messo a disposizione dal NodoSPC                 |
+-----------------+-------------------------------------------------------------------------------------------------------------------------+
| Post-Condizione | L’EC riceve il Catalogo Dati Informativi                                                                                |
+-----------------+-------------------------------------------------------------------------------------------------------------------------+

Tabella XX: XX

|SD_nodoChiediInformativaPSP|

Figura XX: XX

L’evoluzione temporale è la seguente:

1. l’EC richiede al NodoSPC il Catalogo Dati Informativi mediante la primitiva *nodoChiediInformativaPSP;*

..

   Caso OK - Ricezione mediante SOAP *response*

2. il NodoSPC replica all’invocazione precedente fornendo *response* OK ed il file XML relativo al Catalogo Dati Informativi dei PSP codificato in
   Base64;

..

   Caso OK - Ricezione mediante componente SFTP_NodoSPC

3. il NodoSPC deposita il file XML relativo al Catalogo Dati Informativi dei PSP codificato in Base64 nella directory assegnata all’EC;

4. il NodoSPC replica alla primitiva di cui al punto 1 fornendo *response* OK ad indicare la corretta elaborazione della richiesta e la presenza del
   documento richiesto nella directory assegnata all’EC sulla componete SFTP_NodoSPC del NodoSPC;

5. l’EC preleva autenticandosi con username e password il file XML richiesto dalla directory assegnata sulla componente SFTP_NodoSPC del NodoSPC.

..

   Caso KO

6. il NodoSPC replica negativamente alla richiesta di cui al punto 1 emanando un *faultBean* il cui *faultBean*.\ *faultCode* è rappresentativo
   dell’errore riscontrato; in particolare:

-  PPT_SINTASSI_EXTRAXSD: Errore nella SOAP *request*

-  PPT_SEMANTICA: Errore semantico

-  PPT_INFORMATIVAPSP_PRESENTE: il NodoSPC ha già depositato il file XML richiesto nella directory assegnata all’EC sulla componente SFTP_NodSPC

-  PPT_SYSTEM_ERROR: errore nella generazione del file XML richiesto

Funzioni ausiliarie per il PSP
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**Richiesta del Catalogo dei Servizi**

Il PSP interroga la base di dati del NodoSPC al fine di scaricare l’ultima versione del Catalogo dei Servizi offerti dagli EC, da utilizzare
nell’ambito del Pagamento Spontaneo presso i PSP.

+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| Pre-Condizione                                                           | Il PSP decide di supportare i pagamenti spontanei pressi i propri        |
|                                                                          | sportelli                                                                |
+==========================================================================+==========================================================================+
| Trigger                                                                  | Necessità di conoscere i servizi offerti dalle PA                        |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| Descrizione                                                              | Il PSP sottomette la richiesta di ricevere il file XML Catalogo dei      |
|                                                                          | Servizi attestante i servizi offerti dagli EC o da uno specifico Ente    |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| Post-Condizione                                                          | Il PSP riceve il Catalogo dei Servizi degli EC                           |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+

Tabella XX: XX

|SD_nodoChiediCatalogoServizi|

Figura XX: XX

1. il PSP richiede al NodoSPC di ricevere il Catalogo dei Servizi offerto dagli EC mediante la primitiva *nodoChiediCatalogoServizi;*

..

   Caso OK

2. il NodoSPC replica con *response* OK fornendo il tracciato XML del Catalogo dei Servizi codificato in Base64;

..

   Caso KO

-  Il NodoSPC replica con *response* KO emanando un *faultBean* il cui *faultBean*.\ *faultCode* è PPT_SINTASSI_EXTRAXSD.

**Richiesta template del Catalogo Dati Informativi**

Il PSP ha facoltà di richiedere al NodoSPC l’ultima versione del Catalogo Dati Informativi comunicato per motivazioni di verifica o aggiornamenti

+-----------------+--------------------------------------------------------------------------------------------------+
| Pre-Condizione  | Il PSP ha (o meno) precedentemente comunicato al Nodo il Catalogo Dati Informativi               |
+=================+==================================================================================================+
| Trigger         | Necessità del PSP di aggiornare il proprio Catalogo                                              |
+-----------------+--------------------------------------------------------------------------------------------------+
| Descrizione     | Il PSP sottomette la richiesta di ricevere il file XML attestante l’ultimo Catalogo Dati inviato |
+-----------------+--------------------------------------------------------------------------------------------------+
| Post-Condizione | Il PSP riceve il Catalogo Dati Informativi di propria competenza (o il *template*)               |
+-----------------+--------------------------------------------------------------------------------------------------+

Tabella XX: XX

|SD_nodoChiediTemplateInformativaPSP|

Figura XX: XX

1. il PSP richiede al NodoSPC, attraverso la primitiva *nodoChiediTemplateInformativaPSP,* l’ultima versione del Catalogo Dati Informativi
   precedentemente inviato;

..

   Caso OK – precedente invio Catalogo Dati Informativi

2. il PSP riceve *response* OK ed il file XML del Catalogo Dati Informativi in formato Base64 precedentemente inviato;

..

   Caso OK – nessun invio precedente Catalogo Dati Informativi

3. il PSP riceve *response* OK e solo il *template* del Catalogo Dati Informativi;

..

   Caso KO

4. il PSP riceve *response KO* emanando un *faultBean* il cui *faultBean*.\ *faultCode* è PPT_SINTASSI_EXTRAXSD.

**Richiesta informativa PA**

+-----------------+--------------------------------------------------------------------------------------------------------+
| Pre-Condizione  | L’EC ha sottomesso al Nodo la Tabella delle Controparti                                                |
+=================+========================================================================================================+
| Trigger         | Il PSP necessita di conoscere la disponibilità dei servizi offerti dagli EC e i dati ad essi correlati |
+-----------------+--------------------------------------------------------------------------------------------------------+
| Descrizione     | Il PSP sottomette al NodoSPC la richiesta della Tabella delle Controparti                              |
+-----------------+--------------------------------------------------------------------------------------------------------+
| Post-Condizione | Il PSP riceve dal Nodo la Tabella delle Controparti                                                    |
+-----------------+--------------------------------------------------------------------------------------------------------+

Tabella XX: XX

|SD_nodoChiediInformativaPA|

Figura XX: XX

1. il PSP, mediante la primitiva *nodoChiediInformativaPA,* richiede al NodoSPC la Tabella delle Controparti degli EC.

..

   Caso OK

2. il NodoSPC replica con esito OK fornendo in output il documento XML codificato in Base64 rappresentante la Tabella delle Controparti degli EC;

..

   Caso KO

5. il NodoSPC replica con esito KO emanando un *faultBean* il cui *faultBean*.\ *faultCode* è PPT_SINTASSI_EXTRAXSD.

**Richiesta Stato Elaborazione Flusso di Rendicontazione**

+-----------------+--------------------------------------------------------------------------------------------------------------------------------+
| Pre-Condizione  | Il PSP ha sottomesso un file XML di rendicontazione al NodoSPC (mediante SOAP *request* o componente SFTP_NodoSPC)             |
+=================+================================================================================================================================+
| Trigger         | Il PSP necessita di conoscere lo stato di elaborazione del file XML di rendicontazione                                         |
+-----------------+--------------------------------------------------------------------------------------------------------------------------------+
| Descrizione     | Il PSP sottomette la richiesta passando come parametro di input *l’identificativoFlusso* del flusso di rendicontazione inviato |
+-----------------+--------------------------------------------------------------------------------------------------------------------------------+
| Post-Condizione | Il NodoSPC replica fornendo lo stato di elaborazione del flusso di rendicontazione                                             |
+-----------------+--------------------------------------------------------------------------------------------------------------------------------+

Tabella XX: XX

|sd_nodoChiediStatoElaborazioneFlussoRendicontazione|

Figura XX: XX

1. il PSP, attraverso la primitiva *nodoChiediStatoFlussoRendicontazione*, sottomette al NodoSPC la richiesta di conoscere lo stato di elaborazione di
   un flusso XML di rendicontazione precedentemente inviato valorizzando il parametro di input *identificaficativoFlusso*

..

   Caso OK

2. il NodoSPC replica positivamente alla primitiva precedente fornendo lo stato di elaborazione del flusso XML; in particolare:

   -  FLUSSO_IN_ELABORAZIONE: il flusso XML è in fase di elaborazione/storicizzazione sulle basi di dati del NodoSPC

   -  FLUSSO_ELABORATO: Il flusso è stato correttamente elaborato e storicizzato dal NodoSPC

   -  FLUSSO_SCONOSCIUTO: il Nodo non conosce il flusso richiesto

   -  FLUSSO_DUPLICATO: il Nodo rileva che il flusso inviato è già stato sottomesso.

Caso KO

3. Il NodoSPC il NodoSPC replica con esito KO emanando un *faultBean* il cui *faultBean*.\ *faultCode* è PPT_SEMANTICA.

Funzioni Ausiliarie per il NodoSPC
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**Richiesta avanzamento RPT**

+-----------------+--------------------------------------------------------------------------------------------+
| Pre-Condizione  | Il NodoSPC ha sottomesso una RPT o un carrello di RPT al PSP                               |
+=================+============================================================================================+
| Trigger         | Il NodoSPC necessita di verificare lo stato di avanzamento di una RTP o di un              |
+-----------------+--------------------------------------------------------------------------------------------+
| Descrizione     | Il NodoSPC sottomette la richiesta di ricevere lo stato di una RPT o di un carrello di RPT |
+-----------------+--------------------------------------------------------------------------------------------+
| Post-Condizione | Il NodoSPC riceve lo stato della RPT o del carrello di RPT                                 |
+-----------------+--------------------------------------------------------------------------------------------+

Tabella XX: XX

|pspChiediAvanzamentoRPT|

Figura XX: XX

1. il NodoSPC, mediante la primitiva *pspChiediAvanzamentoRPT,* richiede al PSP informazioni in merito allo stato di avanzamento di una RPT o di un
   carrello di RPT.

Caso OK

2. il PSP replica con esito OK fornendo lo stato della RPT o del carrello di RPT;

Caso KO

3. il PSP replica con esito KO emanando un *faultBean* il cui *faultBean*.\ *faultCode* è rappresentativo dell’errore riscontrato; in particolare:

   -  CANALE_RPT_SCONOSCIUTA: non è possibile trovare la RPT o il carrello di RPT per cui si richiede lo stato di elaborazione

   -  CANALE \_RPT_RIFIUTATA: la RPT o il carrello di RPT sottomessi dal NodoSPC sono stati rifiutati dal PSP.

**Richiesta di avanzamento RT**

+-----------------+----------------------------------------------------------------------------------------------------------------------------------+
| Pre-Condizione  | Il NodoSPC verifica lo stato avanzamento di una RT                                                                               |
+=================+==================================================================================================================================+
| Trigger         | Il NodoSPC necessita di verificare lo stato di avanzamento della produzione della RT associata ad una RPT o a un carrello di RPT |
+-----------------+----------------------------------------------------------------------------------------------------------------------------------+
| Descrizione     | Il NodoSPC sottomette la richiesta di ricevere lo stato di una RT                                                                |
+-----------------+----------------------------------------------------------------------------------------------------------------------------------+
| Post-Condizione | Il NodoSPC riceve lo stato della RT                                                                                              |
+-----------------+----------------------------------------------------------------------------------------------------------------------------------+

Tabella XX: XX

|pspChiediAvanzamentoRT|

Figura XX: XX

1. il NodoSPC, mediante la primitiva *pspChiediAvanzamentoRT,* richiede al PSP informazioni in merito allo stato di avanzamento della RT;

2. Il PSP ricerca la RT nel proprio archivio;

..

   Caso OK

3. il PSP replica con esito OK fornendo lo stato della RT, specificando eventualmente il tempo richiesto per la sua generazione ed invio;

..

   Caso KO

4. il PSP replica con esito KO emanando un *faultBean* il cui *faultBean.faultCode* è rappresentativo dell’errore riscontrato; in particolare:

-  CANALE_RT_SCONOSCIUTA: non è stata trovata la RT per la quale si richiede di conoscere lo stato di avanzamento

-  CANALE_RT_RIFIUTATA_EC: la RT è stata rifiutata dall’EC.

Sezione IV – Processo di adesione ed Esercizio

Adesione al sistema pagoPA
==========================

Le Pubbliche Amministrazioni sono tenute per legge ad aderire al sistema di pagamento pagoPA. Le PA che non hanno rapporti diretti con cittadini e
imprese, possono essere esentate dall’adesione al sistema, purché abbiano inviato ad AgID la specifica dichiarazione per tale esenzione disponibile
sul sito dell’Agenzia.

L’obbligo di adesione al sistema pagoPA è esteso anche ai gestori di pubblici servizi e alle società a controllo pubblico. Il D.Lgs. n. 179/2016 (G.U.
n. 214 del 13.9.2016) e il D.Lgs n. 217/2017 (G.U. n. 9 del 12.01.2018) hanno rispettivamente modificato e corretto l’articolo 2, comma 2, del CAD
introducendo nel perimetro soggettivo del CAD anche i gestori di pubblici servizi e le società a controllo pubblico, come definite nel decreto
legislativo adottato in attuazione dell’articolo 18 della legge n. 124 del 2015, escluse le società quotate. Il D.Lgs. n. 175/2016, all’articolo 2,
lettera m), ha delineato il concetto di società a controllo pubblico. In particolare, le società a controllo pubblico sono definite come quelle
società in cui una o più amministrazioni pubbliche esercitano poteri di controllo ai sensi dell'articolo 2359 del codice civile.

I Prestatori di Servizi di Pagamento (PSP), come le banche, le poste, gli istituti di pagamento e ogni altro soggetto abilitato da Banca d’Italia ad
eseguire servizi di pagamento, aderiscono su base volontaria al sistema pagoPA per erogare i propri servizi di pagamento a cittadini e imprese.

Il Decreto legislativo 13 dicembre 2017, n. 217 (G.U. n. 9 del 12.01.2018) a correzione del CAD, ha introdotto all’articolo 65, comma 2, del Codice
«L’obbligo per i prestatori di servizi di pagamento abilitati di utilizzare esclusivamente la piattaforma di cui all’articolo 5, comma 2, del decreto
legislativo n. 82 del 2005 per i pagamenti verso le pubbliche amministrazioni decorre dal 1° gennaio 2019». Pertanto, i PSP autorizzati ad operare in
Italia dalla Banca d’Italia **non potranno in alcun modo eseguire servizi di pagamento che non transitino per il sistema pagoPA**, ove abbiano come
beneficiario un soggetto pubblico che risulti obbligato all’adesione al sistema.

Pertanto, i soggetti pubblici obbligati all’adesione a pagoPA, alla data del 1 gennaio 2019, ove non aderenti ancora a pagoPA, non potranno più
incassare in proprio attraverso l’attività di un PSP, salvo l’affidamento di tutte le loro entrate ad un riscuotitore speciale che sia già aderente a
pagoPA.

L’adesione a pagoPA avviene con procedure e modalità definite da AgID e disciplinate nelle Linee Guida. L’iter è differenziato per tipologia di
soggetto aderente (Ente Creditore o Prestatore di Servizi di Pagamento) e può avvenire, per entrambe le tipologie, sia in modalità diretta che in
modalità indiretta. Le indicazioni relative alla procedura di adesione da parte degli Enti Creditori e dei Prestatori di Servizi di Pagamento sono
disponibili sul sito istituzionale dell’Agenzia.

La procedura di adesione:

-  Individua gli obblighi e le responsabilità inerenti l’utilizzo del Sistema pagoPA;

-  Consente il censimento degli Enti Creditori (PA, gestori di pubblici servizi e società a controllo pubblico) e dei PSP aderenti al Sistema pagoPA
   nel dominio gestito dal sistema stesso;

-  Prevede la comunicazione da parte degli Enti Creditori aderenti dei dati di configurazione necessari alla fruizione del servizio, ivi inclusi i
   codici IBAN dei conti di accredito;

-  Prevede la comunicazione da parte dei Prestatori di Servizi di Pagamento dei dati necessari alla fruizione del servizio, come specificati
   nell’Accordo di servizio.

Adesione di un Ente Creditore.
------------------------------

Per aderire a pagoPA in qualità di Ente Creditore, le PA, i gestori di pubblici servizi e le società a controllo pubblico devono utilizzare
il \ **Portale delle Adesioni** che rende disponibili funzionalità per la compilazione, in via automatica, della lettera di adesione e l’invio della
stessa all’Agenzia per l’Italia Digitale.

Il Portale delle Adesioni è uno strumento Web predisposto da AgID al fine di supportare gli Enti Creditori nei processi di adesione e di attivazione
su pagoPA ed è messo a disposizione di tutti i soggetti che, con ruoli differenti, intervengono in tali processi.

Per accedere al Portale delle Adesioni, gli Enti devono richiedere ad AgID (via PEC all’indirizzo \ protocollo@pec.agid.gov.it) le credenziali di
primo accesso. Preventivamente alla compilazione della lettera di adesione, l’Ente Creditore dovrà aver individuato il nominativo del “Referente dei
Pagamenti”, ossia della persona indicata quale interlocutore unico con l’Agenzia per l’Italia Digitale relativamente alle attività di carattere
amministrativo ed al quale l’Agenzia provvederà tramite PEC ad inviare le credenziali nominali di accesso.

Tutti i passi che deve compiere il Referente dei Pagamenti per portare a termine l’adesione dell’Ente Creditore sono descritti nel Manuale Utente del
Portale delle Adesioni disponibile sul sito dell’AgID.

L’Ente Creditore, esclusivamente tramite il Portale delle Adesioni, deve inviare ad AgID la Lettera di Adesione, sottoscritta digitalmente dal
rappresentante legale dell’Ente e, solo successivamente all’accettazione di essa, avrà ultimato la procedura di adesione.

Prerequisito per l’adesione da parte degli Enti Creditori è l’accreditamento nell’archivio IPA (Indice delle Pubbliche Amministrazioni).

Adesione di un Prestatore di Servizi di Pagamento
-------------------------------------------------

I Prestatori di Servizi di Pagamento come le banche, le poste, gli istituti di pagamento e ogni altro soggetto abilitato da Banca d’Italia ad eseguire
servizi di pagamento, aderiscono su base volontaria al sistema pagoPA per erogare i propri servizi di pagamento a cittadini e imprese.

Sia i PSP che i consorzi o le associazioni di categoria possono aderire in qualità di “intermediari tecnologici” a supporto di altri PSP o degli Enti
Creditori.

Per formalizzare l’adesione i PSP sottoscrivono con l’AgID appositi Accordi di servizio, secondo i seguenti modelli:

-  Accordo di servizio per PSP, nel caso in cui il PSP voglia aderire al Sistema pagoPA esclusivamente per l'erogazione di servizi di pagamento,
   eventualmente anche usufruendo dell'attività di intermediazione di un PSP già aderente;

-  Accordo di servizio per PSP anche intermediario tecnologico, nel caso in cui il PSP voglia aderire al Sistema pagoPA svolgendo anche l'attività di
   intermediazione per altri soggetti.

Entrambi i modelli, validati anche dall’ABI-Associazione Bancaria Italiana, sono pubblicati sul sito dell’Agenzia per l’Italia Digitale.

L’accordo di servizio deve essere compilato e sottoscritto digitalmente dal legale rappresentante del PSP o da chi ha potere di firma. L’accordo, così
completato, deve essere inviato tramite PEC all’indirizzo \ protocollo@pec.agid.gov.it, specificando nell’oggetto della email “Adesione al sistema dei
Pagamenti”.

Con la sottoscrizione dell’accordo di servizio e la conseguente accettazione di quanto stabilito nelle Linee Guida e nei relativi allegati, il PSP, a
titolo gratuito, autorizza l’Agenzia per l’Italia Digitale a utilizzare e pubblicare il marchio identificativo del PSP aderente, nonché ogni proprio
ulteriore marchio identificativo dei servizi da questo erogati attraverso il Nodo-SPC.

Inoltre, in forza dell’integrazione automatica stabilita negli accordi di servizio sottoscritti con i PSP, ogni nuova disposizione e/o previsione
contenuta nelle Linee Guida e nei relativi allegati e/o documentazione monografica di riferimento risulterà inserita e/o richiamata nell’accordo di
servizio già sottoscritto, quale parte integrante dello stesso, anche in sostituzione delle clausole difformi apposte in esso, senza alcun ulteriore
consenso tra le parti sottoscrittrici.

Sempre in forza della stabilita integrazione automatica, gli stessi accordi di servizio già sottoscritti risulteranno altresì automaticamente
integrati con ogni nuova disposizione e/o previsione contenuta nel nuovo modello standard di accordo di servizio, anche in sostituzione delle clausole
difformi apposte, senza alcun ulteriore consenso tra le parti sottoscrittrici.

L’adesione formale a pagoPA consente il censimento del soggetto nel Dominio dei soggetti aderenti. Il “Referente” per l’attuazione dell’accordo,
ovvero la persona indicata nell’accordo di servizio, è l’unico interlocutore del PSP con l’Agenzia per l’Italia Digitale.

Intermediari e Partner tecnologici nel sistema pagoPA
-----------------------------------------------------

Gli Enti Creditori e i PSP aderenti al Sistema pagoPA, si possono avvalere di uno o più soggetti terzi, intermediari tecnologici, che, in nome e per
conto del soggetto aderente, si occuperanno di gestire le attività di interconnessione all’infrastruttura del Nodo-SPC, mantenendo inalterate le
responsabilità di Ente Creditore e PSP nei confronti delle proprie controparti diverse dall’AgID e, in particolare, degli utilizzatori finali.

L’Intermediario tecnologico è un soggetto già aderente e attivo sul Sistema e come tale ha già accettato in proprio e si è obbligato in proprio al
rispetto delle Linee Guida e dei relativi allegati.

Gli Enti Creditori possono interconnettersi al Nodo di Pagamenti-SPC delegando le attività tecniche ad un **Intermediario tecnologico** oppure ad un
**Partner tecnologico**.

Il Partner tecnologico è un fornitore dell’Ente Creditore che si occupa delle attività tecniche necessarie per l’interfacciamento con il Nodo-SPC,
ferma restando la responsabilità nei confronti di AgID in capo all’Ente Creditore. AgID esclude l’adesione al sistema pagoPA da parte del Partner
tecnologico in quanto tale.

Un Ente Creditore può avvalersi contemporaneamente di uno o più Intermediari e/o Partner potendo i servizi essere erogati da una molteplicità di
soggetti, sempre nel rispetto delle Linee Guida.

L’Agenzia conserva le informazioni relative ad Intermediari e Partner tecnologici nelle proprie basi dati e pubblica sul proprio sito istituzionale
l’elenco di tali soggetti.

Attivazione sul sistema pagoPA
==============================

Gli Enti Creditori, nel processo di attivazione sul Sistema pagoPA, sono supportati dal Portale delle Adesioni messo a disposizione di tutti i
soggetti che, con ruoli differenti, intervengono in tale processo ovvero:

-  I soggetti incaricati dagli Enti Creditori (Referenti Pagamenti);

-  Le figure tecniche degli Enti Creditori direttamente connessi al Nodo (eventualmente Intermediari) e dei Partner tecnologici (Referenti Tecnici);

-  Gli operatori del Nodo-SPC;

-  l’Agenzia per l’Italia Digitale.

Il **Referente Pagamenti** (RP) è la figura incaricata dall’Ente Creditore, mediante delega del legale rappresentante, che opera nell’ambito del
Sistema pagoPA per attivare e gestire le connessioni logiche dell'Ente Creditore, per nominare il Referente Tecnico in caso di connessione diretta,
per gestire la lista degli IBAN dei conti di accredito che l’Ente Creditore intende utilizzare per l’incasso delle somme dovute. Uno stesso Referente
Pagamenti può essere designato da più Enti Creditori.

Il **Referente Tecnico** (RT) è la figura tecnica di riferimento di un soggetto direttamente connesso al Nodo-SPC (Ente o Partner tecnologico). Ogni
connessione logica di un Ente Creditore prevede un Referente Tecnico: quello nominato dal Referente Pagamenti dell’Ente Creditore (in caso di
connessione diretta) oppure quello nominato dall’Intermediario/Partner Tecnologico (in caso di connessione intermediata). Il Referente Tecnico sarà lo
stesso per tutti gli enti per i quali l’Intermediario/Partner tecnologico svolge tale ruolo.

I Prestatori di Servizi di Pagamento aderenti sono supportati nel processo di attivazione sul Sistema pagoPA dalla struttura di AgID che per tutte le
attività tecniche ed organizzative si interfaccia con il Referente dei Servizi nominato dal Prestatore nell’Accordo di Servizio.

Il **Referente dei servizi** (RS) è la figura delegata dal Prestatore aderente ad eseguire ogni comunicazione all'Agenzia tramite sistemi di PEC,
inerente tutti i dati tecnici e amministrativi, ivi inclusi quelli bancari, necessari all'attivazione e alla configurazione del servizio e le
eventuali modifiche e/o aggiornamenti che dovessero intervenire.

Il Prestatore aderente delega altresì il Referente dei servizi a ricevere ogni comunicazione proveniente dall'Agenzia, anche nel caso in cui esse
comportino la pronta attuazione delle indicazioni ivi contenute.

Il dettaglio del processo di attivazione sul sistema pagoPA è disponibile sul documento intitolato “Processo di avvio in esercizio di soggetti
collegati direttamente al Nodo dei Pagamenti-SPC”, disponibile sul sito istituzionale dell’Agenzia.

Attivazione di un EC direttamente connesso
==========================================

Il Referente Pagamenti di un Ente Creditore che abbia deciso di attivarsi su pagoPA collegandosi direttamente all’infrastruttura del Nodo-SPC, deve
censire sul Portale delle Adesioni una connessione logica diretta indicando i modelli di pagamento su cui l’Ente Creditore intende attivarsi;
contestualmente è tenuto a nominare la figura del Referente Tecnico.

Il Referente Tecnico, ricevuta la nomina e le credenziali di accesso al Portale delle Adesioni, dovrà innanzitutto individuare la soluzione più
adeguata per realizzare il **collegamento fisico** al Nodo-SPC.

Il **collegamento fisico** si riferisce alla tipologia del supporto di rete utilizzato per connettere la piattaforma del soggetto aderente al
Nodo-SPC; l’individuazione del collegamento fisico prevede la raccolta di tutte le informazioni tecniche che lo rendono possibile: indirizzi IP, porte
IP assegnate, configurazioni firewall, ecc.

Allo stato attuale il Nodo-SPC può raggiungere il perimetro dell’Ente Creditore utilizzando i seguenti tipi di connettività:

-  SPC

-  Internet

-  Linea dedicata

Per la connettività SPC possono essere utilizzare le seguenti modalità di colloquio applicativo:

-  PdD: Porta di Dominio

-  SGPdD: Software di Gestione Porta di Dominio (Porta di Dominio equivalente)

-  GAD: Gateway Accesso Diretto

Per la connettività Internet possono essere utilizzare le seguenti modalità di colloquio applicativo:

-  GAD: Gateway Accesso Diretto

Per la connettività su Linea dedicata possono essere utilizzare le seguenti modalità di colloquio applicativo:

-  GTS: Gateway Trasporto Sicuro

Il set di dati necessario alla configurazione della connettività tramite PdD è identico al set di dati di configurazione di una SGPdD.

Qualora il soggetto che intende connettersi direttamente al Nodo sia un **Ente Creditore** i collegamenti fisici possono essere di tipo PdD o GAD.

Qualora il soggetto che intende connettersi direttamente al Nodo sia un **Partner Tecnologico** i collegamenti fisici possono essere di tipo: SGPdD o
GTS o GAD.

Il Nodo-SPC è strutturato in due ambienti distinti e indipendenti: un ambiente di Test Esterno (disponibile per eseguire tutti i test di attivazione e
integrazione previsti da AgID) ed uno per l'Esercizio.

Ogni aderente al Nodo potrà quindi, in qualsiasi momento, effettuare test di integrazione interfacciandosi, presso l'ambiente di test del Nodo-SPC, o
con un emulatore PSP o con gli ambienti di test predisposti dai PSP aderenti al Nodo.

Gli ambienti del Nodo-SPC saranno allineati alle Specifiche Attuative di riferimento, pubblicate sul sito istituzionale dell’Agenzia, tranne nei
periodi transitori di modifica per l'implementazione di nuove specifiche.

Processo di avvio in Esercizio
------------------------------

Il processo di avvio in Esercizio di un Ente Creditore collegato direttamente all’infrastruttura del Nodo-SPC prevede il soddisfacimento di alcuni
prerequisiti riguardanti la predisposizione di un ambiente di Collaudo e di un ambiente di Esercizio e un piano per il *disaster recovery*.

L’Ente Creditore che intenda infatti iniziare il processo che lo porterà a rendere disponibili i propri servizi attraverso l’esecuzione di operazioni
di pagamento sul Sistema pagoPA secondo i modelli dichiarati, sarà tenuto ad attivare un collegamento fisico (di Collaudo) con l’ambiente di Test
Esterno del Nodo-SPC ed un collegamento fisico (di Esercizio) con l’ambiente di Esercizio del Nodo-SPC.

Per completare le configurazioni dovrà inoltre fornire tutte le informazioni necessarie all’attivazione di almeno una Stazione in ambiente di Collaudo
ed almeno una Stazione in ambiente di Esercizio. La definizione della Stazione è di competenza del soggetto collegato direttamente all’infrastruttura
del Nodo-SPC.

Ogni collegamento fisico può avere un numero variabile di Stazioni, in funzione dei modelli di pagamento implementati e delle regole/preferenze del
soggetto direttamente connesso al Nodo. La configurazione di un Ente sul Nodo-SPC si completa con l’associazione dell’Ente stesso ad almeno una delle
sue Stazioni. Il RT può portare a termine tutte le attività descritte utilizzando il Portale delle Adesioni (per i dettagli si rimanda al Manuale
Utente disponibile sul sito dell’Agenzia).

Per completare il processo di avvio in Esercizio l’Ente Creditore deve soddisfare un ulteriore requisito: la compilazione di un documento di manleva
all'esecuzione dei servizi oggetto dei casi di test indicati da AgID. Il documento di manleva deve essere recapitato ad AgID, firmato digitalmente,
dal Referente Tecnico dell’Ente Creditore al fine di completare il processo di attivazione in Esercizio.

Nel documento di manleva il RT dichiara di voler rendere disponibili i propri servizi attraverso l’esecuzione di operazioni di pagamento sul sistema
pagoPA e garantisce di aver effettuato con esito positivo, sia in ambiente di Test Esterno che in ambiente di Esercizio, tutti i casi di test previsti
da AgID alla data di sottoscrizione del documento. Il documento di manleva è disponibile sul sito istituzionale dell’Agenzia.

Soddisfatti tutti i requisiti iniziali il Referente Tecnico, utilizzando il Portale delle Adesioni, può avviare il processo procedendo come segue:

1. Accede alla funzionalità preposta e crea una nuova pianificazione indicando tutti i Modelli di Pagamento su cui intende attivare l’Ente Creditore.

2. Decide se procedere o meno con l’esecuzione dei test previsti in ambiente di Collaudo con il supporto del personale AgID. Se decide di eseguire i
   test deve:

   a. Fornire gli IBAN di accredito da utilizzare in ambiente di Collaudo;

   b. Proporre ad AgID una data di inizio dei test al fine di coordinare le attività previste;

   c. Configurati gli IBAN di Collaudo ed ultimati i test con il supporto di AgID, il RT deve compilare il “Verbale di Collaudo” e rimanere in attesa
      che AgID lo validi per chiudere formalmente la fase di Collaudo;

3. Terminata la fase di Collaudo (3.c) oppure avendo deciso di non coinvolgere AgID in tale fase, il RT esprime la volontà di procedere o meno con
   l’esecuzione dei test previsti in ambiente di Esercizio con il supporto del personale AgID. Se decide di eseguire i test deve:

   d. Fornire gli IBAN di accredito da utilizzare in ambiente di Esercizio (ne potrebbe inserire di nuovi o utilizzare IBAN già attivi per
      quell’Ente);

   e. Proporre ad AgID una data di inizio dei test al fine di coordinare le attività previste;

   f. Configurati gli IBAN in fase di Pre-Esercizio ed ultimati i test con il supporto di AgID, il RT deve compilare il “Verbale di Pre-Esercizio” e
      rimanere in attesa che AgID lo validi per chiudere le attività di Pre-Esercizio.

4. Ultimata la fase di Pre-Esercizio oppure avendo deciso di non coinvolgere AgID in tale fase, il RT deve compilare il documento di manleva affinchè
   AgID lo possa validare e chiudere formalmente la fase di Pre-Esercizio;

5. Al fine di completare la procedura di avvio in esercizio dell'Ente Creditore il RT deve:

   g. Fornire la "Tabella delle Controparti";

   h. Indicare tutte le informazioni riguardanti il “Tavolo operativo”.

6. AgID autorizza all’Esercizio l’Ente Creditore invitando il Referente Pagamenti dell’Ente ad attivare sul PdA (qualora non ne esistano) almeno un
   IBAN di accredito.

Per tutti i dettagli fare riferimento al Manuale Utente disponibile sul sito dell’Agenzia.

Attivazione di un EC intermediato
=================================

Come previsto dal modello di funzionamento, gli aderenti al sistema pagoPA possono servirsi anche di Intermediari e/o Partner tecnologici per
interconnettersi al Nodo di Pagamenti-SPC.

Un Ente Creditore può infatti decidere di:

-  Connettersi al Nodo di Pagamenti-SPC direttamente;

-  Connettersi al Nodo di Pagamenti-SPC indirettamente delegando le attività tecniche ad un **Intermediario tecnologico**;

-  Connettersi al Nodo di Pagamenti-SPC indirettamente delegando le attività tecniche ad un **Partner tecnologico**.

Le tre soluzioni possono anche coesistere tra di loro potendo l’Ente Creditore in autonomia decidere a quanti eventualmente affidare l’onere
dell’interconnessione con il Nodo-SPC.

Attivazione di un EC con un Intermediario Tecnologico
-----------------------------------------------------

Il Referente dei Pagamenti di un Ente Creditore che abbia deciso di connettersi al Nodo-SPC indirettamente, delegando le attività tecniche ad un
**Intermediario tecnologico**, deve:

-  Censire sul PdA una connessione logica con l’Intermediario tecnologico prescelto;

-  Attivare tutti gli IBAN di accredito dell’Ente Creditore (operazione possibile solo se l’Ente abbia almeno una connessione logica in Esercizio).

Per tutte le attività in carico al Referente Tecnico l’Ente Creditore farà riferimento alla figura tecnica designata dall’Intermediario tecnologico
scelto, senza facoltà di nomina o sostituzione in forza dell’avvenuta delega delle attività tecniche.

Per attivare un Ente Creditore, ovvero la sua connessione logica, il Referente Tecnico dell’Intermediario tecnologico deve utilizzare una apposita
funzionalità messa a disposizione dal Portale delle Adesioni con cui fornire ad AgID tutti i dati richiesti.

Per tutti i dettagli riguardanti le attività da eseguire sul Portale delle Adesioni fare riferimento al Manuale Utente disponibile sul sito
dell’Agenzia.

Attivazione di un EC con un Partner Tecnologico
-----------------------------------------------

Il Referente dei Pagamenti di un Ente Creditore che abbia deciso di connettersi al Nodo di Pagamenti-SPC indirettamente delegando le attività tecniche
ad un **Partner tecnologico** deve:

-  Censire sul PdA una connessione intermediata dal Partner tecnologico prescelto;

-  Attivare tutti gli IBAN di accredito dell’Ente Creditore (operazione possibile solo se l’Ente abbia almeno una connessione logica in Esercizio).

Per tutte le attività in carico al Referente Tecnico l’Ente Creditore farà riferimento alla figura tecnica designata dal Partner tecnologico scelto,
senza facoltà di nomina o sostituzione in forza dell’avvenuta delega delle attività tecniche.

Il processo di avvio in esercizio di un Ente Creditore che abbia delegato un Partner tecnologico dipende dal ruolo che ricopre l’Ente rispetto
all’attivazione del Partner sul sistema pagoPA.

Per un Partner tecnologico infatti l’Ente Creditore può rappresentare l’\ *Ente pilota* ovvero il primo Ente Creditore per il quale il Partner attiva
uno o più modelli di pagamento oppure un Ente Creditore che si aggiunge a quelli che già abbiano delegato il medesimo Partner.

Attivazione di Ente Creditore “pilota”
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Qualora l’Ente Creditore rappresenti l’Ente “pilota” del Partner ovvero il primo Ente Creditore per il quale il Partner richiede di attivare uno o più
modelli di pagamento, il processo di avvio in esercizio ricalca esattamente il processo di avvio in esercizio di un Ente Creditore direttamente
connesso al Nodo-SPC ove il Referente Tecnico è la figura designata dal Partner tecnologico a svolgere quel ruolo per tutti gli Enti.

Attivazione di Ente Creditore “non pilota”
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Per attivare un Ente Creditore “non pilota” (che quindi abbia scelto di avvalersi di un Partner Tecnologico che abbia già attivato in esercizio altri
Enti sul/i modello/i di pagamento prescelto/i) il processo ricalca esattamente il processo di avvio in esercizio di un Ente Creditore intermediato da
un Intermediario Tecnologico.

Attivazione di un PSP sul sistema pagoPA
========================================

Ciascun PSP deve sottoscrivere con AgID un atto formale, l’\ **Accordo di servizio**, indispensabile per utilizzare l’infrastruttura del Nodo-SPC e
per usufruire dei servizi di supporto connessi.

Come previsto dalle Linee Guida, un PSP può erogare su pagoPA in forma autonoma servizi di pagamento e altresì utilizzare il servizio di
intermediazione tecnologica erogato da terzi per altri servizi di pagamento. In altri termini, un PSP può risultare - a sua libera scelta - sia
erogatore di servizi, sia soggetto intermediato, a seconda del servizio di pagamento offerto.

Con l’Accordo di servizio è nominato il “Referente dei Servizi” (RS) del PSP che svolge funzioni di unico interlocutore nei confronti di AgID per ogni
attività tecnica ed è delegato a gestire ogni informazione inerente dati tecnici e amministrativi, ivi inclusi quelli bancari, necessari alla
configurazione e all'attivazione del PSP nonché gestire tutti gli aggiornamenti che dovessero intervenire successivamente.

Il **Catalogo dei Dati Informativi**, la cui struttura è ampiamente descritta nella Sezione III delle SANP, è lo strumento con il quale il PSP
comunica ad AgID tutte le informazioni relative ai servizi di pagamento offerti comprese le condizioni di utilizzo ed i costi di commissione massimi
applicati.

Il processo di avvio in Esercizio sul sistema pagoPA di un PSP dipende dai modelli di pagamento e/o dai servizi di pagamento che il PSP intende
erogare.

Se il PSP aderente intende implementare i modelli di pagamento attivati presso l’Ente Creditore e/o quelli attivati presso il PSP è necessario che si
colleghi direttamente all’infrastruttura del Nodo-SPC oppure si faccia intermediare da un altro PSP già attivo su quei modelli di pagamento.

Se il PSP aderente intende erogare servizi di pagamento CBill e MyBank non è necessario che si colleghi direttamente al Nodo-SPC. Anche nel caso in
cui un PSP aderente intenda svolgere il ruolo di Acquirer sul sistema pagoPA non è necessario che si colleghi direttamente al Nodo-SPC.

Attivazione di un PSP che si collega direttamente al Nodo
---------------------------------------------------------

Il Referente dei Servizi di un PSP che debba attivarsi su pagoPA collegandosi direttamente all’infrastruttura del Nodo-SPC, deve configurare un
collegamento fisico con l’infrastruttura del Nodo-SPC individuando la soluzione più adeguata per realizzarlo e garantire i livelli di servizio imposti
dall’Agenzia, prevedendo anche un piano per il *disaster recovery*.

Per collegarsi al Nodo-SPC i PSP devono utilizzare una linea dedicata.

Il processo di avvio in Esercizio di un PSP collegato direttamente all’infrastruttura del Nodo-SPC prevede il soddisfacimento di alcuni prerequisiti:
l’attivazione di un collegamento fisico (di Collaudo) con l’ambiente di Test Esterno del Nodo-SPC ed un collegamento fisico (di Esercizio) con
l’ambiente di Esercizio del Nodo-SPC.

Per completare il processo di avvio il PSP deve soddisfare un ulteriore requisito: la compilazione di un documento di manleva all'esecuzione dei
servizi oggetto dei casi di test indicati da AgID.

Il documento di manleva firmato digitalmente deve essere recapitato ad AgID dal Referente dei Servizi del PSP al fine completare il processo di
attivazione in Esercizio. In esso il Referente garantisce di aver effettuato con esito positivo, sia in ambiente di Test Esterno che in ambiente di
Esercizio tutti i casi di test previsti da AgID alla data di sottoscrizione del documento.

Il documento di manleva è disponibile sul sito istituzionale dell’Agenzia.

Soddisfatti tutti i pre-requisiti il Referente dei Servizi, può avviare il processo operando come segue:

1. Compila il Catalogo Dati Informativi da utilizzare in ambiente di Collaudo;

2. Fornisce al Nodo tutti le informazioni necessarie a completare la configurazione dei Canali di Pagamenti presenti nel Catalogo;

3. Decide di procedere o meno con l’esecuzione dei test previsti in ambiente di Collaudo con il supporto del personale AgID. Se decide di eseguire i
   test deve:

   a. Proporre ad AgID una data di inizio dei test al fine di coordinare le attività previste;

   b. Ultimati i test con il supporto di AgID, il RS deve compilare il “Verbale di Collaudo” e rimanere in attesa che AgID lo validi per chiudere
      formalmente la fase di Collaudo;

4. Terminata la fase di Collaudo (3.b) oppure avendo deciso di non coinvolgere AgID in tale fase, il RS compila il Catalogo Dati Informativi da
   utilizzare in ambiente di Esercizio;

5. Fornisce al Nodo tutte le informazioni necessarie a completare la configurazione dei Canali di Pagamenti presenti nel Catalogo di Esercizio;

6. Decide di procedere o meno con l’esecuzione dei test previsti in fase di Pre-Esercizio con il supporto del personale AgID. Se decide di eseguire i
   test deve:

   c. Proporre ad AgID una data di inizio dei test al fine di coordinare le attività previste;

   d. Terminati i test con il supporto di AgID, il RS deve compilare il “Verbale di Pre-Esercizio” e rimanere in attesa che AgID lo validi per
      chiudere le attività di Pre-Esercizio.

7. Ultimata la fase di Pre-Esercizio oppure avendo deciso di non coinvolgere AgID in tale fase, il RS deve compilare il documento di manleva affinchè
   AgID lo possa validare e chiudere formalmente la fase di Pre-Esercizio;

8. Al fine di completare il processo, il RS deve fornire ad AgID tutte le informazioni riguardanti il “Tavolo operativo”.

Attivazione di un PSP che svolge il ruolo di Acquirer
-----------------------------------------------------

Il processo di configurazione che devono eseguire i PSP che intendono svolgere il ruolo di acquirer nel sistema pagoPA tramite il POS virtuale AgID è
descritto nell’apposita **monografia,** intitolata "Transazioni attraverso il POS Virtuale AgID del Nodo dei Pagamenti-SPC" e pubblicata sul sito
istituzionale dell’Agenzia.

Attivazione di un PSP che offre il servizio MyBank
--------------------------------------------------

Il servizio MyBank consente di ottenere, in tempo reale, un’autorizzazione per il trasferimento di fondi dal conto bancario del cliente a quello
dell’esercente online, utilizzando un bonifico SEPA.

Il modello di funzionamento del servizio si identifica con il “processo di pagamento con re-indirizzamento online”.

La sottoscrizione dell’Accordo di servizio è un atto formale indispensabile per poter utilizzare il servizio MyBank. I PSP possono svolgere sul
Nodo-SPC sia il ruolo di banca del debitore (c.d. *Buyer Bank*) sia il ruolo di banca dell'esercente (c.d. *Seller Bank*).

PSP che intendono svolgere il ruolo di Banca Buyer
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

I PSP che intendono svolgere il ruolo di Banca Buyer devono inviare ad AgID tutte le informazioni necessarie sul loro Catalogo Dati Informativi. La
procedura di abilitazione per l'avvio in esercizio viene attivata su richiesta del RS ed ha l’obiettivo di verificare che l’operatività dei modelli di
pagamento implementati corrisponda alle specifiche attuative vigenti e viene certificata mediante un verbale semplificato in cui si attesta la
corretta esecuzione di almeno un bonifico SCT.

I dettagli del CDI per PSP di Buyer Bank sono riportati nella **monografia** intitolata “Erogazione del servizio MyBank attraverso il Nodo del
Pagamenti-SPC” disponibile sul sito istituzionale dell’Agenzia.

PSP che intendono svolgere il ruolo di Banca Seller
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

I PSP che intendono offrire servizi sul Nodo-SPC attraverso il servizio MyBank in qualità di **Seller** Bank per le operazioni di pagamenti eseguite
in favore degli Enti Creditori che abbiano in essere un rapporto di conto corrente con il Prestatore Aderente devono rispettare quanto previsto nella
**monografia** intitolata "Transazioni MyBank attraverso il Nodo dei Pagamenti-SPC", disponibile sul sito istituzionale dell’Agenzia. Anche in questo
caso, i PSP che intendono svolgere il ruolo di Banca Seller devono inviare ad AgID tutte le informazioni necessarie sul loro Catalogo Dati
Informativi.

Al fine di consentire all’utilizzatore finale di eseguire operazioni di pagamento in favore di un Ente Creditore mediante la soluzione MyBank, con
accredito su un conto corrente intestato a detto Ente, il PSP aderente nel ruolo di *Seller Bank* presterà il servizio di *Routing Service*, anche
tramite uno specifico soggetto terzo detto *Routing Service Provider*, purché rispetti le specifiche di interfacciamento del servizio di routing.

La *Seller Bank* accrediterà gli importi versati dagli utilizzatori finali in favore di Singoli Enti Creditori mediante il Nodo-SPC, assicurando il
rispetto della normativa di riferimento pro tempore vigente.

Attivazione di un PSP che offre il servizio CBILL
-------------------------------------------------

In questo paragrafo sono descritte le attività che devono essere effettuate dai Prestatori di Servizi di Pagamento che intendono utilizzare il
servizio CBILL del consorzio CBI (Customer to Business Interaction) per interagire con il Nodo-SPC.

I dettagli sul funzionamento del servizio CBILL in pagoPA sono riportati nella **monografia** intitolata “Erogazione del servizio CBILL attraverso il
Nodo dei Pagamenti-SPC”, disponibile sul sito dell’Agenzia.

La sottoscrizione dell’Accordo di servizio è un atto formale indispensabile per poter utilizzare il servizio CBILL, tuttavia i PSP che intendono
offrire il servizio CBILL sul sistema pagoPA hanno un iter di attivazione facilitato, in quanto le fasi di realizzazione del collegamento al Nodo-SPC
sono già state effettuate dal Consorzio CBI, che assume il ruolo di "Intermediario Tecnologico" nei confronti dei propri aderenti. Per completare la
fase di avvio in esercizio è necessario inviare ad AgID tutte le informazioni relative al “Catalogo Dati Informativi” utilizzato.

Invece, i PSP che sono già aderenti a pagoPA ed al Nodo-SPC, e che vogliono erogare i servizi di pagamento in argomento, devono fare riferimento alle
sole attività previste per l’invio delle informazioni relative al “Catalogo Dati Informativi”.

 Attivazione di un PSP intermediato
-----------------------------------

I PSP aderenti che intendono utilizzare il Sistema pagoPA indirettamente, possono servirsi di Intermediari a cui delegano lo svolgimento di tutte le
attività tecniche (connessione al Nodo-SPC). Per tutte le attività in carico al Referente Servizi il PSP farà riferimento alla figura tecnica
designata dall’intermediario tecnologico scelto, senza facoltà di nomina o sostituzione in forza dell’avvenuta delega delle attività tecniche.

Sarà cura dell’Agenzia censire i PSP che intendono aderire al sistema pagoPA e completare il processo di adesione, indicando le modalità per procedere
con la configurazione dei canali di connessione e del catalogo dati informativo.

Adempimenti durante l’erogazione del servizio
=============================================

Gli adempimenti che gli Enti Creditori, i Prestatori di Servizi di Pagamento e i Partner Tecnologici sono tenuti ad osservare durante l’erogazione del
servizio, dipendono dalle modalità di collegamento degli stessi.

Adempimenti dei soggetti direttamente collegati al Nodo-SPC
-----------------------------------------------------------

Tutti i soggetti collegati direttamente al Nodo-SPC devono farsi carico degli obblighi e adempimenti di seguito descritti.

Tavoli operativi
~~~~~~~~~~~~~~~~

Il processo di avvio in Esercizio sul Sistema pagoPA di tutti i soggetti collegati direttamente al Nodo-SPC obbliga tali soggetti a dotarsi di un
Tavolo Operativo che sia in grado di fornire il supporto necessario a rilevare e gestire eventuali anomalie di funzionamento in Esercizio.

Il Referente Tecnico dell’Ente Creditore e del Partner Tecnologico ed il Referente dei Servizi del Prestatore di Servizi di Pagamento sono tenuti a
fornire all’Agenzia per l’Italia Digitale tutte le informazioni relative al Tavolo Operativo, che costituisce un ulteriore punto di contatto per
l’Agenzia nel caso in cui pervengano segnalazioni di anomalie di funzionamento.

I Tavoli Operativi devono essere attivi 24 ore su 24, 7 giorni su 7. I Referenti Tecnici e i Referenti dei Servizi hanno l’onere di garantire che il
Tavolo Operativo possa far fronte sia alla operatività ordinaria (rilevazione e gestione di specifiche anomalie di funzionamento) che a procedure di
emergenza da attivare in caso di gravi malfunzionamenti.

Monitoraggio e controllo
~~~~~~~~~~~~~~~~~~~~~~~~

I soggetti direttamente collegati al Nodo-SPC devono:

-  Utilizzare un sistema che monitori lo stato del servizio e sia disponibile anche al Tavolo Operativo;

-  Implementare il “Giornale degli Eventi”, come indicato nella Sezione III;

-  Registrare e classificare le segnalazioni pervenute al Tavolo Operativo al fine di favorire lo scambio di informazioni con l’Agenzia.

Business continuity e Disaster Recovery
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Ogni soggetto collegato direttamente al Nodo-SPC è tenuto a predisporre ed implementare soluzioni tecniche ed organizzative atte a garantire la
Business Continuity e il Disaster Recovery come previsto dalla normativa vigente (in particolare nel “Codice dell'amministrazione digitale”, D. Lgs.
N. 82/2005 s.m.i. - artt. 50-bis e 51).

Qualora si verifichino eventi che pregiudichino la Business Continuity è fatto altresì obbligo al soggetto di darne tempestiva comunicazione
all’Agenzia per l’Italia Digitale.

Archiviazione dei dati
~~~~~~~~~~~~~~~~~~~~~~

Fatti salvi gli obblighi di legge in tema di tenuta e conservazione della documentazione attinente alle attività svolte per l’erogazione del Servizio
e la fruizione delle Funzioni, nonché le disposizioni previste dalla normativa vigente relativa alla privacy, ogni soggetto collegato direttamente al
Nodo-SPC (Ente Creditore o Prestatore di Servizi di Pagamento) è tenuto ad archiviare, senza alcuna modifica, i dati trasmessi e ricevuti tramite il
Servizio.

Ulteriori adempimenti
~~~~~~~~~~~~~~~~~~~~~

Gli Enti Creditori collegati direttamente al Nodo-SPC devono:

a) Comunicare al proprio utilizzatore finale gli eventuali vincoli, disponibilità dei propri servizi con particolare riferimento ai pagamenti attivati
   presso le strutture dei Prestatori di Servizi di Pagamento;

b) Comunicare all’utilizzatore finale le caratteristiche tipiche dei servizi di pagamento offerti attraverso il Nodo-SPC;

c) Attivare tutti i servizi di pagamento destinati all’utilizzatore finale attraverso il sistema pagoPA;

d) Rispettare le disponibilità di servizio indicate;

e) Mantenere disponibili le figure del Referente Pagamenti e del Referente Tecnico e provvedere ad aggiornare l’Agenzia per l’Italia Digitale in caso
   di loro avvicendamento.

I PSP collegati direttamente al Nodo-SPC devono inoltre:

a) Mantenere aggiornato il Catalogo Dati Informativi;

b) Mantenere disponibile la figura del Referente Servizi indicata nell’accordo di servizio e provvedere ad aggiornare l’Agenzia per l’Italia Digitale
   in caso di suo avvicendamento;

c) Se offrono servizi presso proprie strutture e/o punti di prossimità, comunicare agli utilizzatori finali tale possibilità, esponendo in loco
   l’apposito “Logo” registrato dall’Agenzia per l’Italia Digitale;

d) Comunicare e mantenere aggiornati i dati relativi ai canali di pagamento disponibili (es. sportello fisico, home banking, app mobile, ATM).

Adempimenti dei soggetti non direttamente collegati al Nodo-SPC
---------------------------------------------------------------

Tutti i soggetti non direttamente collegati al Nodo-SPC devono farsi carico degli adempimenti di seguito descritti.

Per quanto riguarda i Tavoli Operativi, il soggetto aderente al Sistema pagoPA che abbia deciso di delegare le attività tecniche ad uno o più
Intermediari tecnologici e/o ad uno o più Partner Tecnologici deve garantirsi la possibilità di comunicare con i Tavoli Operativi di tutti i suoi
Intermediari/Partner.

Deve inoltre garantirsi che i propri Intermediari/Partner abbiano implementato tutte le soluzioni previste riguardanti:

-  Sistemi di monitoraggio e controllo;

-  Business Continuity e Disaster Recovery;

-  Archiviazione dei dati.

Tutti gli Enti Creditori non direttamente collegati al Nodo-SPC hanno altresì l’obbligo di:

a) Comunicare al proprio utilizzatore finale gli eventuali vincoli, disponibilità dei propri servizi con particolare riferimento ai pagamenti attivati
   presso le strutture dei Prestatori di Servizi di Pagamento;

b) Comunicare all’utilizzatore finale le caratteristiche tipiche dei servizi di pagamento offerti attraverso il Nodo-SPC;

c) Attivare tutti i servizi di pagamento destinati all’utilizzatore finale attraverso il sistema pagoPA;

d) Rispettare le disponibilità di servizio indicate;

e) Mantenere disponibile la figura del Referente Pagamenti nominata in fase di adesione e provvedere ad aggiornare l’Agenzia per l’Italia Digitale in
   caso di suo avvicendamento.

I PSP non collegati direttamente al Nodo-SPC devono inoltre:

a) Mantenere aggiornato il Catalogo Dati Informativi;

b) Mantenere disponibile la figura del Referente Servizi indicata nell’accordo di servizio e provvedere ad aggiornare l’Agenzia per l’Italia Digitale
   in caso di suo avvicendamento;

c) Se offrono servizi presso proprie strutture e/o punti di prossimità, comunicare agli utilizzatori finali tale possibilità, esponendo in loco
   l’apposito “Logo” registrato dall’Agenzia per l’Italia Digitale;

d) Comunicare e mantenere aggiornati i dati relativi ai canali di pagamento disponibili (es. sportello fisico, home banking, app mobile, ATM).

Utilizzo del marchio pagoPA
===========================

L’Agenzia per l’Italia Digitale ha realizzato e registrato il marchio pagoPA attraverso la definizione di un logotipo atto a individuare i soggetti
aderenti e attivi sul Sistema pagoPA, siano essi Enti Creditori (pubbliche amministrazioni, società a controllo pubblico o gestori di pubblici
servizi), siano essi Prestatori di Servizi di Pagamento.

In particolare, l’Agenzia per l’Italia Digitale, nell’intento di agevolare l’utilizzatore finale, ha previsto la diffusione di tale logotipo per fare
comprendere all’utenza con più immediatezza e facilità se un soggetto pubblico - in qualità di beneficiario - oppure un soggetto privato - in qualità
di PSP - sia attivo sul Sistema pagoPA.

In considerazione della valenza strategica e legale del "Logo", anche al fine di evitare confusioni e/o frodi nei confronti della clientela privata,
l’Agenzia per l’Italia Digitale ha provveduto alla registrazione del logotipo presso le competenti amministrazioni al fine di garantire allo stesso
logotipo una tutela a livello nazionale.

In merito, si segnala che nel caso in esame non siamo di fronte alla registrazione di un semplice marchio d’impresa ma a quella di un marchio
collettivo, ossia di un marchio il cui uso può essere concesso a soggetti che siano adeguati all’erogazione di servizi coerenti e in linea con il
marchio stesso.

In virtù della qualificazione come marchio collettivo, unitamente alla registrazione di un esemplare del marchio, l’Agenzia per l’Italia Digitale ha
registrato anche il Regolamento inerente l’uso del marchio collettivo registrato pagoPA, pubblicato sul sito istituzionale dell’Agenzia per l’Italia
Digitale, che avrà cura di aggiornarlo nel tempo.

Pertanto, sia gli Enti Creditori, sia i PSP, in sede di adesione al Nodo-SPC, e precisamente, con l’accettazione di quanto stabilito nelle Linee Guida
e nei relativi allegati:

-  Dichiarano di avere preso visione del “Regolamento inerente l’uso del marchio collettivo registrato pagoPA”, nella versione pubblicata sul sito
   istituzionale dell’Agenzia per l’Italia Digitale e di accettare incondizionatamente quanto in esso stabilito;

-  Si obbligano a rispettare integralmente quanto previsto nel “Regolamento inerente l’uso del marchio collettivo registrato pagoPA”, nella versione
   pubblicata sul sito istituzionale dell’Agenzia per l’Italia Digitale.

..

   Sul sito istituzionale dell’Agenzia è disponibile la documentazione che regola l’utilizzo del logo pagoPA in tutte le versioni di esso disponibili.

   Coloro che lo utilizzano per la prima volta, hanno l’obbligo di scegliere l’ultima versione disponibile del logo; tutti gli altri possono mantenere
   la precedente versione per il periodo necessario ad adeguarsi.

Disponibilità dei Servizi
=========================

Ogni soggetto aderente al Sistema pagoPA è tenuto a rendere disponibili le soluzioni tecniche ed organizzative secondo le indicazioni riportate nel
documento “Indicatori di qualità per i Soggetti Aderenti” pubblicato sul sito dell’Agenzia per l’Italia Digitale.

Nodo-SPC
--------

Il Servizio erogato dal Nodo-SPC è operativo 24 ore su 24, 7 su 7; in particolare, i Servizi di Nodo garantiscono le seguenti disponibilità:

-  **Servizi Base**: sono resi in modalità on-line;

-  **Servizio Repository**: è reso in modalità on-line;

-  **Servizio Ricezione totali di traffico**: è reso sulla base della periodicità da definire con il fruitore;

-  **Servizio di Invio e ricezione dei flussi di rendicontazione**: è reso in modalità on-line e in modalità File Transfer sicuro.

Enti Creditori 
---------------

La disponibilità dei servizi erogati dagli Enti Creditori è dettagliata nel documento “\ *Indicatori di qualità per i Soggetti Aderenti*\ ” pubblicato
sul sito dell’Agenzia per l’Italia Digitale.

Prestatori di servizi di pagamento aderenti
-------------------------------------------

La disponibilità dei servizi erogati dai prestatori di servizi di pagamento aderenti è dettagliata nel documento “\ *Indicatori di qualità per i
Soggetti Aderenti*\ ” pubblicato sul sito dell’Agenzia per l’Italia Digitale.

Livelli di Servizio
===================

I livelli di servizio, intesi come tempi massimi di risposta applicativa percepiti dall’utilizzatore finale del sistema pagoPA, devono essere conformi
a quanto specificato nel documento dal titolo “\ *Indicatori di qualità per i soggetti aderenti*\ ”, disponibile sul sito istituzionale dell’Agenzia.

Indicatori di qualità del Nodo-SPC
----------------------------------

Gli indicatori di qualità inerenti i servizi erogati dal Nodo-SPC ai soggetti aderenti sono valutati sulla base di indicatori di performance (KPI) la
cui struttura è dettagliata nel citato documento “\ *Indicatori di qualità per i Soggetti Aderenti*\ ”, disponibile sul sito istituzionale
dell’Agenzia.

Le statistiche relative a tali indicatori saranno rese disponibili attraverso il Servizio di Reporting del Nodo-SPC.

Responsabilità dei soggetti aderenti
====================================

Di seguito sono indicati gli oneri in capo ai soggetti aderenti al Nodo-SPC.

Responsabilità dell’Ente Creditore 
-----------------------------------

L’Ente Creditore è responsabile anche sotto il profilo giuridico:

-  Della qualità, della correttezza e della completezza dei dati che trasmette, ivi incluso l’IBAN del conto da accreditare;

-  Del corretto aggiornamento dei dati del proprio sistema informativo;

-  Della sicurezza all’interno del proprio dominio;

-  Se del caso, dell’assegnazione delle firme digitali ai soggetti autorizzati e del controllo del corretto utilizzo delle stesse.

L’Ente Creditore è altresì responsabile dell’errata e/o omessa indicazione dei dati comunicati all’utilizzatore finale e/o pubblicati per l’esecuzione
del pagamento nei propri confronti.

Nel caso in cui l’Ente Creditore proceda all’identificazione del soggetto pagatore, l’Ente Creditore risulterà responsabile della correttezza e
dell’autenticità dei dati identificativi del pagatore ai fini del buon esito del pagamento.

L’Ente Creditore è responsabile della omessa verifica della coincidenza tra i dati inseriti nella Richiesta di Pagamento Telematico (RPT) rispetto a
quelli propri della relativa Ricevuta Telematica (RT) al fine del rilascio della quietanza di pagamento.

L’Ente Creditore autorizza, sin da ora, l’Agenzia per l’Italia Digitale e/o suoi aventi causa, a monitorare l’erogazione dei servizi offerti oggetto
delle presenti specifiche tecniche, nonché alla pubblicazione dei dati rivenienti dal relativo monitoraggio.

Responsabilità del Prestatore di Servizi di Pagamento
-----------------------------------------------------

Il Prestatore di Servizi di Pagamento è tenuto a eseguire l’operazione di pagamento richiesta dall’utilizzatore finale secondo le modalità e le
tempistiche previste dal D.lgs. del 27 gennaio 2010, n. 11 e relativi provvedimenti attuativi emanati dalla Banca d’Italia.

Il Prestatore di Servizi di Pagamento è responsabile anche sotto il profilo giuridico:

-  Della qualità, della correttezza e della completezza dei dati che trasmette;

-  Del corretto aggiornamento dei dati del proprio sistema informativo;

-  Della sicurezza all’interno del proprio dominio;

-  Se del caso, dell’assegnazione delle firme digitali ai soggetti autorizzati e del controllo del corretto utilizzo delle stesse.

A prescindere dall’identificazione del pagatore eseguita dall’Ente Creditore, se del caso, anche per il tramite del proprio Intermediario/Partner
Tecnologico, il Prestatore di Servizi di Pagamento, resta responsabile dell’identificazione del soggetto Versante (titolare del C/C di addebito), in
quanto suo cliente.

Il Prestatore di Servizi di Pagamento autorizza, sin da ora, l’Agenzia per l’Italia Digitale e/o suoi aventi causa, a monitorare l’erogazione dei
servizi offerti oggetto delle presenti specifiche attuative, nonché alla pubblicazione dei dati rivenienti dal relativo monitoraggio.

APPENDICE I – APPROFONDIMENTI (ENTI CREDITORI)

Integrità e non ripudiabilità della Ricevuta Telematica
-------------------------------------------------------

Laddove il *workflow* del procedimento amministrativo consenta all’Ente Creditore di ricevere la ricevuta telematica dal Prestatore di Servizi di
Pagamento direttamente per il tramite del NodoSPC, si evidenzia agli Enti Creditori che non potranno sussistere incertezze circa l’integrità e la non
ripudiabilità del documento stesso poiché il *workflow* del pagamento si sviluppa all’interno di un “circuito di trust” senza alcuna possibilità di
ingerenza e/o manomissione da parte di terzi; da qui l’inopportunità di garantire l’integrità e non ripudiabilità della ricevuta telematica attraverso
la firma digitale o la firma elettronica qualificata dello stesso da parte del Prestatore di Servizi di Pagamento.

Acquisto della marca da bollo digitale 
---------------------------------------

L'Agenzia delle Entrate ha realizzato il servizio @e.bollo che permette a cittadini ed imprese di acquistare la marca da bollo digitale ed assolvere
in tale modo l'imposta di bollo dovuta sulle istanze inviate telematicamente alla Pubblica Amministrazione nonché sui relativi atti rilasciati tramite
canali telematici.

Non essendo questa la sede per descrivere in dettaglio tale progetto si rimanda al provvedimento del Direttore dell’Agenzia delle Entrate “Modalità di
pagamento in via telematica dell'imposta di bollo dovuta per le istanze e per i relativi atti e provvedimenti trasmessi in via telematica ai sensi
dell’art. 1, comma 596, della legge 27 dicembre 2013, n. 147 - servizio *@e.bollo*\ ” e altra documentazione collegata emessa dalla stessa Agenzia.

Il servizio di vendita al cittadino è reso esclusivamente da rivenditori convenzionati con l’Agenzia delle Entrate che hanno stipulato con la stessa
un'apposita convenzione. Un Prestatore di Servizi di Pagamento aderente al Sistema pagoPA che aderisca anche al sistema *@e.bollo* può rendere
disponibile una soluzione di pagamento telematico integrata con il Sistema pagoPA.

Le Pubbliche Amministrazioni potranno consentire ai cittadini l’acquisto di marca da bollo digitale necessaria per la presentazione di un’istanza,
utilizzando gli stessi oggetti informatici (RPT e RT) utilizzati per i pagamenti. Sarà possibile attuare tale soluzione nel caso di procedimenti
amministrativi che richiedono la presentazione di una istanza in bollo e nel caso che il procedimento preveda il rilascio di documento in bollo.

È bene evidenziare che, nella soluzione di integrazione trattata nel presente capitolo, la Pubblica Amministrazione destinataria dell’istanza non è la
beneficiaria del pagamento, ma svolge unicamente una funzione di supporto per il cittadino, veicolando verso il Prestatore di Servizi di Pagamento
convenzionato con l’Agenzia delle Entrate, selezionato dal cittadino stesso fra quelli disponibili, le informazioni necessarie alla produzione della
marca da bollo digitale.

Nel processo di acquisto in parola la Ricevuta Telematica (RT) svolge unicamente il ruolo di vettore della marca da bollo digitale acquistata dal
cittadino. In mancanza di un corrispondente flusso finanziario verso la Pubblica Amministrazione, questa tipologia di ricevute telematiche (RT) non è
soggetta a riconciliazione, limitatamente agli importi riguardanti la marca da bollo.

Il caso d’uso del pagamento della marca da bollo digitale è descritto nel dettaglio nella Sezione III del presente documento.

APPENDICE II – APPROFONDIMENTI (PRESTATORI DI SERVIZI DI PAGAMENTO)

Il servizio MyBank
------------------

La trattazione completa dell'argomento è consultabile nel documento monografico "*Transazioni MyBank attraverso il Nodo dei Pagamenti-SPC*" pubblicato
sul sito istituzionale di AgID.

FINE DOCUMENTO

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
