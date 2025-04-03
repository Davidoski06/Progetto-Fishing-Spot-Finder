# Progetto-Fishing-Spot-Finder
Progetto Scolastico - Tepsit
# Fishing Spot Finder

Fishing Spot Finder è un'applicazione web che aiuta gli appassionati di pesca a trovare i migliori spot di pesca vicino alla loro posizione. Il progetto integra diverse API per fornire informazioni in tempo reale sul meteo, la geolocalizzazione degli spot e le recensioni degli utenti.

## Caratteristiche Principali

- **Spot Finder**: Ricerca spot di pesca in base alla posizione.
- **Meteo in tempo reale**: Integrazione con l'OpenWeather API per mostrare le condizioni meteo locali.
- **Mappa interattiva**: Visualizzazione degli spot su una mappa tramite la Google Maps API.
- **Recensioni e Foto**: Possibilità per gli utenti di aggiungere recensioni e foto agli spot.
- **CRUD Completo**: Funzionalità per creare, leggere, aggiornare ed eliminare gli spot.

## Tecnologie Utilizzate

- **Back-End**: Node.js con Express
- **Database**: MySQL
- **Front-End**: HTML, CSS, JavaScript (con integrazione di Google Maps)
- **API Esterne**:
  - [OpenWeather API](https://openweathermap.org/api)
  - [Google Maps API](https://developers.google.com/maps)
  - [Fishbrain API](https://fishbrain.com/api) *(se integrata)*

## Struttura del Progetto

## Installazione

1. **Clona il repository**:
   git clone https://github.com/tuo-username/fishing-spot-finder.git
   cd fishing-spot-finder

**Installa le dipendenze:**
  npm install

**Configura le variabili d'ambiente:**

  Crea un file .env nella root del progetto con il seguente contenuto (aggiorna i valori secondo le tue necessità):
  
  .env
  DB_HOST=localhost
  DB_USER=root
  DB_PASS=
  DB_NAME=fishing_spots_db
  
  OPENWEATHER_API_KEY=tuo_openweather_api_key
  GOOGLE_MAPS_API_KEY=tuo_google_maps_api_key
  FISHBRAIN_API_KEY=tuo_fishbrain_api_key
  
**Avvio del Progetto**
  Modalità di sviluppo: Usa nodemon per avviare il server e riavviarlo automaticamente ad ogni modifica.
  
  nodemon server.js
  Modalità normale: Avvia il server con Node.js.
  
  node server.js
  Apri il browser e visita http://localhost:3000 per vedere l'applicazione in azione.

**API Endpoints**
  
  GET /
  Restituisce un messaggio di benvenuto.
  
  GET /spots
  Restituisce tutti gli spot di pesca.
  
  POST /spots
  Inserisce un nuovo spot.
  Esempio di corpo della richiesta (JSON):
  
  GET /spots/:id
  Restituisce un singolo spot in base all'ID.
  
  PUT /spots/:id
  Aggiorna i dati di uno spot esistente.
  Esempio di corpo della richiesta (JSON):
  
  DELETE /spots/:id
  Elimina uno spot.
  
  GET /geocode?address=tuo_indirizzo
  Utilizza la Google Geocoding API per convertire un indirizzo in coordinate (latitudine e longitudine).
