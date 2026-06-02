# Gebäudebrüter der Stadt Zürich

Interaktive Auswertung der Nistplatzstandorte von Gebäudebrütern in der Stadt Zürich. Die Webseite zeigt Karte, Diagramme und Tabellen auf Basis von Open Government Data.

**[Live-Demo](https://dongoginho.github.io/mcp-gebaeudebrueter/)**

## Datenquellen

- [Gebäudebrüter – Inventar Nistplatzstandorte](https://data.stadt-zuerich.ch/dataset/geo_gebaeudebrueter) (Grün Stadt Zürich, CC0) — [Metadaten (geocat.ch)](https://www.geocat.ch/geonetwork/srv/ger/catalog.search#/metadata/0bd44405-438a-81ea-103a-d8a244a4f34f/formatters/xsl-view?root=div&view=advanced)
- [Stadtkreise](https://data.stadt-zuerich.ch/dataset/geo_stadtkreise) (Stadt Zürich, CC0)

Die Daten werden live via WFS (Web Feature Service) als GeoJSON geladen.

## Inhalte

- **Hintergrund** – Einführung zum Gebäudebrüter-Inventar mit Referenzen zu [Grün Stadt Zürich](https://www.stadt-zuerich.ch/de/umwelt-und-energie/natur/naturschutz-und-stadtoekologie/kartierungen-und-inventare.html), [Orniplan AG](https://orniplan.ch) und dem [Gebäudebrüter-Inventar](https://www.stadt-zuerich.ch/de/planen-und-bauen/bauberatung-und-dienstleistungen/bauberatung/gruenraeume-freiraeume/gebaeudebrueter-und-schutz-vor-vogelschlag/gebaeudebrueter-inventar.html)
- **Kennzahlen** – KPI-Kacheln (Anzahl Standorte, Vogelarten, häufigste Art, KSO-Objekte)
- **Karte** – Interaktive Leaflet-Karte mit Vogelarten-Filter, Stadtkreis-Grenzen und Top-20-Strassen-Tabelle
- **Vogelarten** – Balkendiagramm nach Vogelart und Stacked Bar nach Stadtkreis (Spatial Join)

## Datencheck (Jupyter Notebook)

`datencheck.ipynb` — Notebook zur periodischen Prüfung der Daten. Lädt die gleichen WFS-Quellen, berechnet die Kennzahlen mit pandas und zeigt Auswertungen (Vogelarten, Stadtkreise, Top-Strassen, KSO, Datenqualität). Erkennt Veränderungen gegenüber definierten Referenzwerten.

Abhängigkeiten: `requests`, `pandas`, `matplotlib`, `shapely`

## Technik

- Einzelne HTML-Datei (CSS + JS inline), keine Build-Tools
- [Chart.js 4](https://www.chartjs.org/) für Diagramme
- [Leaflet 1.9](https://leafletjs.com/) für die Karte
- Point-in-Polygon (Ray-Casting) für den Spatial Join mit Stadtkreisen

## Entstehung

Diese Webseite wurde mit Hilfe des [OGD-MCP-Servers der Stadt Zürich](https://www.stadt-zuerich.ch/de/politik-und-verwaltung/statistik-und-daten/open-government-data/anwendungen/anwendungen-2026/ckan-mcp-server.html) und [Claude](https://claude.ai) erstellt.

## Weitere Beispiele

Weitere MCP-Server-Beispiele: [dongoginho.github.io](https://dongoginho.github.io/)
