\# HEXA Power Community Edition

Sistema semplice e open-source per controllare caricatore HEXA da Home Assistant.



Licenza: GNU GPL v3



\---



\# Funzioni



\- Controllo manuale caricatore

\- Automazione surplus fotovoltaico

\- Dashboard Home Assistant inclusa

\- Comunicazione API locale HEXA

\- Configurazione semplice

\- Nessuna dipendenza proprietaria

\- Il sistema prevede una presa smart per lo spegnimento (sonoff)

\---



\# Requisiti
aver installato file editor in home assistant


\- Home Assistant 

\- Caricatore HEXA compatibile API

\- Smart plug opzionale

\- Sensore flusso rete o surplus FV

\- AI varia aiuta nelle piccolezze.. 

\--- Home Assistant collegato al  wifi al charger (meglio con scheda wifi dedicata )  


\- Per usare tutte le automazioni è necessario un sensore  che rilevi i consumi, ad esempio un  meter TA. Così facendo si ha molto di più di un carica batterie... ma propio un sistema per l'autocarica che sfrutta il surplus energetico... )


\# Installazione

     


\## 1. Copiare il package

a. Apri il tuo file configuration.yaml e assicurati che sotto la voce homeassistant: sia presente la riga packages: !include_dir_named packages. Se hai già una sezione homeassistant:, aggiungi solo la riga dei packages come nell'esempio:
YAML

homeassistant:
  # Altre configurazioni esistenti (es. name, latitude, ecc.)
  packages: !include_dir_named packages


b. incollare testo in /homeassistant/configuration.yaml:

 lovelace:
  mode: storage
  dashboards:
    hexa-power:
      mode: yaml
      title: Hexa Power
      icon: mdi:solar-power-variant
      show_in_sidebar: true
      filename: dashboards/hexa_power_dashboard.yaml


\## 2. Copiare il package


a. copia il file "hexa_power_dashboard_portabile.yaml" della dashboard sotto la  cartella "dashboards" (se non c'è creala).

b. copia il file "hexa_power_portabile.yaml" della dashboard sotto la  cartella "packages" (se non c'è creala).


\## 3. Test e riavvio

testa la configurazione:
impostazioni / strumenti per sviluppatori / controlla e riavvia

controlla la configurazione ;  se  ok = riavvio / riavvia home assistant

