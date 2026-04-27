# GeoNewsletter Routine

## Notifica Telegram al termine

Al termine di ogni generazione della newsletter GIS/Geospatial, esegui
obbligatoriamente il seguente comando Bash come ultimo passo:

```bash
curl -s -X POST "https://api.telegram.org/bot${TELEGRAM_BOT_TOKEN}/sendMessage" \
  -d chat_id=${TELEGRAM_CHAT_ID} \
  -d text="✅ GeoNewsletter ${MESE} generata — ${NUM_NEWS} news raccolte"
```

Sostituisci `${MESE}` con il mese di riferimento (es. "Marzo 2026") e
`${NUM_NEWS}` con il numero totale di news incluse nella newsletter.

Il comando deve essere eseguito tramite tool Bash, non solo stampato come testo.
