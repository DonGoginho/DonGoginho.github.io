# Gebäudebrüter der Stadt Zürich

Interaktive Auswertung der Nistplatzstandorte von Gebäudebrütern in der Stadt Zürich. Die Webseite zeigt Karte, Diagramme und Tabellen auf Basis von Open Government Data.

**[Live-Demo](https://dongoginho.github.io/mcp-gebaeudebrueter/)**

## Datenquellen

- [Gebäudebrüter – Inventar Nistplatzstandorte](https://data.stadt-zuerich.ch/dataset/geo_gebaeudebrueter) (Grün Stadt Zürich, CC0)
- [Stadtkreise](https://data.stadt-zuerich.ch/dataset/geo_stadtkreise) (Stadt Zürich, CC0)

Die Daten werden live via WFS (Web Feature Service) als GeoJSON geladen.

## Inhalte

- **Übersicht** – Einführung und Kennzahlen (863 Standorte, 12 Vogelarten, 24 KSO-Objekte)
- **Karte** – Interaktive Leaflet-Karte mit Vogelarten-Filter, Stadtkreis-Grenzen und Top-20-Strassen-Tabelle
- **Vogelarten** – Balkendiagramm nach Vogelart und Stacked Bar nach Stadtkreis (Spatial Join)

## Technik

- Einzelne HTML-Datei (CSS + JS inline), keine Build-Tools
- [Chart.js 4](https://www.chartjs.org/) für Diagramme
- [Leaflet 1.9](https://leafletjs.com/) für die Karte
- Point-in-Polygon (Ray-Casting) für den Spatial Join mit Stadtkreisen

## Entstehung

Diese Webseite wurde mit Hilfe des [OGD-MCP-Servers der Stadt Zürich](https://www.stadt-zuerich.ch/de/politik-und-verwaltung/statistik-und-daten/open-government-data/anwendungen/anwendungen-2026/ckan-mcp-server.html) und [Claude](https://claude.ai) erstellt.

## Weitere Beispiele

Weitere MCP-Server-Beispiele: [dongoginho.github.io](https://dongoginho.github.io/)
