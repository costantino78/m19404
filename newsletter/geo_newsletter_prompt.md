# Prompt — Newsletter GIS & Geospatial Mensile

## Istruzioni di esecuzione

**Trigger:** questo prompt viene eseguito il **primo giorno di ogni mese**.

**Periodo di riferimento:** il **mese solare immediatamente precedente** a quello della data di esecuzione.
- Esempio: se la run avviene il 1° maggio 2026, raccogliere solo news pubblicate tra il **1° aprile 2026** e il **30 aprile 2026** (estremi inclusi).
- Calcolo pratico: `mese_riferimento = mese(data_run) - 1`; raccogliere news con data compresa tra `primo_giorno(mese_riferimento)` e `ultimo_giorno(mese_riferimento)`.

**Lingua:** cercare fonti sia in italiano che in inglese.

---

## Compito

Raccogliere da internet informazioni, news e post tecnici sul mondo GIS e Geospatial
pubblicati nel **mese solare precedente** (vedi sopra) e creare una newsletter.

Per ogni news includere:
- Titolo
- Fonte e URL
- Data di pubblicazione
- Riassunto di 2-3 righe (in italiano)
- Categoria: [News Industria | Cloud-Native Tech | EO/Satellite | Open Source | GeoAI | Standard & Spec]

---

## Numero massimo e distribuzione

**NUMERO MASSIMO:** 30 news totali, distribuite come segue.
Nel caso in cui non vengano trovate abbastanza news per una categoria,
non aggiungere contenuti di riempimento: riportare solo quelle effettivamente
trovate nel periodo, anche se il totale è inferiore a 30.

### Distribuzione per fonte (target)

**[A] 8 — Blog tecnici specialistici**
- forrest.nyc
- developmentseed.org/blog
- cloudnativegeo.org/blog
- thrivegeo.com
- wherobots.com/blog
- element84.com/blog
- fused.io/blog
- mapscaping.com/blog

**[B] 5 — Progetti open source (blog e changelog ufficiali)**
- geoserver.org/blog
- qgis.org (changelog e news)
- postgis.net/news
- gdal.org (release notes e GitHub)
- stacspec.org/en/news

**[C] 6 — Istituzioni EO e dati ufficiali**
- earth.esa.int/eogateway/news
- earthdata.nasa.gov/news
- sentinel-hub.com/blogs
- copernicus.eu/en/news
- usgs.gov/news
- planet.com/pulse

**[D] 6 — News generalisti tecnici**
- geospatialworld.net
- gim-international.com
- spacenews.com
- esri.com/arcgis-blog (includere SOLO post con tag: developers,
  data-management, open-data — escludere contenuti puramente commerciali)
- eijournal.com
- ogc.org/news

**[E] 5 — Community e aggregatori**
- planet.osgeo.org
- reddit.com/r/gis (solo post con alto engagement, no domande base)
- medium.com/tag/geospatial (solo articoli tecnici approfonditi)
- towardsdatascience.com (filtra per tag: geospatial, remote-sensing, geoai)
- radiantearth.medium.com

---

## Priorità tematiche

Ordinare i contenuti per rilevanza rispetto a questi topic:

1. Cloud-native formats: STAC, COG, GeoParquet, Zarr, FlatGeobuf, PMTiles
2. GeoAI e Foundation Models per EO (Prithvi, Clay, etc.)
3. Earth Observation e dati satellitari (Sentinel, Landsat, SAR)
4. Release di tool open source (GeoServer, QGIS, GDAL, PostGIS, TiTiler, etc.)
5. Standard OGC e evoluzioni spec (OGC API, GeoZarr SWG, STAC spec)
6. Data Engineering geospatiale (DuckDB Spatial, Apache Sedona, Iceberg+Geo)
7. WebGIS e visualizzazione (MapLibre, deck.gl, Kepler.gl)

---

## Regole di esclusione

- Escludere news pubblicate **al di fuori del mese solare di riferimento**
  (vedere "Periodo di riferimento" in cima al documento)
- Escludere news puramente commerciali o di marketing senza contenuto tecnico
- Escludere annunci di prodotto senza dettagli tecnici
- Escludere contenuti duplicati (stessa notizia da fonti diverse: tenere la fonte primaria)

---

## Formato output

Organizzare la newsletter in **sezioni tematiche** (non per fonte), nell'ordine
delle priorità tematiche sopra indicate.
Ogni sezione ha un titolo e le news sono numerate progressivamente.
In fondo alla newsletter aggiungere una sezione "📌 Da tenere d'occhio" con
3-5 trend o sviluppi emergenti dedotti dall'insieme delle news trovate.
