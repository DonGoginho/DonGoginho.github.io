# Personenwagen der Stadt Zürich

Interaktive Auswertung des Personenwagenbestands der Stadt Zürich mit Zeitreihen von 2002 bis 2025. Die Webseite zeigt Trends, Marken, Treibstoffarten und Motorisierungsgrad auf Basis von Open Government Data.

**[Live-Demo](https://dongoginho.github.io/mcp-personenwagen/)**

## Datenquellen

- [Bestand der Personenwagen nach Treibstoffart, Rechtsform und Stadtquartier (OD2001)](https://data.stadt-zuerich.ch/dataset/prd_ssz_fz_pw_bestand_jahr_quartier_antriebsart_rechtsform_od2001) (Statistik Stadt Zürich, CC0)
- [Bestand der Personenwagen nach Marke und Stadtquartier (OD2003)](https://data.stadt-zuerich.ch/dataset/prd_ssz_fz_pw_bestand_marke_quartier_od2003) (Statistik Stadt Zürich, CC0)
- [Neuzulassungen nach Treibstoffart (OD2004)](https://data.stadt-zuerich.ch/dataset/prd_ssz_fz_pw_neuzulassungen_jahr_quartier_antriebsart_rechtsform_od2004) (Statistik Stadt Zürich, CC0)
- [Motorisierungsgrad nach Stadtquartier (OD2005)](https://data.stadt-zuerich.ch/dataset/prd_ssz_fz_motorisierungsgrad_jahr_quartier_od2005) (Statistik Stadt Zürich, CC0)
- [Bevölkerung nach Alter, Herkunft und Geschlecht (OD3903)](https://data.stadt-zuerich.ch/dataset/bev_bestand_jahr_quartier_alter_herkunft_geschlecht_od3903) (Statistik Stadt Zürich, CC0)

## Inhalte

- **Bestand vs. Bevölkerung** – Personenwagen und Wohnbevölkerung ab 18 Jahren im Vergleich
- **Motorisierungsgrad** – Personenwagen pro 1'000 Einwohner nach Stadtkreis
- **Bestandsentwicklung** – Zeitreihe 2002–2025
- **Treibstoffarten** – Neuzulassungen nach Antriebsart (Elektro, Benzin, Diesel etc.)
- **Marken** – Top-10-Marken, Top-5-Elektromarken, grösste Gewinner und Verlierer

## Technik

- Einzelne HTML-Datei (CSS + JS inline), keine Build-Tools
- [Chart.js 4](https://www.chartjs.org/) für Diagramme
- Daten via CKAN Datastore SQL API

## Entstehung

Diese Webseite wurde mit Hilfe des [OGD-MCP-Servers der Stadt Zürich](https://www.stadt-zuerich.ch/de/politik-und-verwaltung/statistik-und-daten/open-government-data/anwendungen/anwendungen-2026/ckan-mcp-server.html) und [Claude](https://claude.ai) erstellt.

## Weitere Beispiele

Weitere MCP-Server-Beispiele: [dongoginho.github.io](https://dongoginho.github.io/)
