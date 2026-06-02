# Open Data Stadt Zürich – Interaktive Auswertungen

Interaktive Auswertungen auf Basis von Open Government Data der Stadt Zürich. Alle Daten stammen von [data.stadt-zuerich.ch](https://data.stadt-zuerich.ch) (CC0-Lizenz).

**[dongoginho.github.io](https://dongoginho.github.io/)**

## MCP-Server Beispiele

Erstellt mit [Claude](https://claude.ai) und dem [OGD-MCP-Server](https://www.stadt-zuerich.ch/de/politik-und-verwaltung/statistik-und-daten/open-government-data/anwendungen/anwendungen-2026/ckan-mcp-server.html). Der MCP-Server stellt Tools bereit, mit denen Claude direkt SQL-Abfragen auf die offenen Datensätze der Stadt Zürich ausführen kann.

| Beispiel | Beschreibung | Datenquelle |
|---|---|---|
| [Personenwagen](https://dongoginho.github.io/mcp-personenwagen/) | Bestand, Treibstoffarten, Marken und Motorisierungsgrad 2002–2025 | [OD2001](https://data.stadt-zuerich.ch/dataset/prd_ssz_fz_pw_bestand_jahr_quartier_antriebsart_rechtsform_od2001), [OD2003](https://data.stadt-zuerich.ch/dataset/prd_ssz_fz_pw_bestand_marke_quartier_od2003) u.a. |
| [Hunde](https://dongoginho.github.io/mcp-hunde/) | Hundebestand, Rassen, Alterspyramiden und Namen 2014–2025 | [OD1001](https://data.stadt-zuerich.ch/dataset/sid_stapo_hundebestand_od1001), [OD1002](https://data.stadt-zuerich.ch/dataset/sid_stapo_hundenamen_od1002) |
| [Gebäudebrüter](https://dongoginho.github.io/mcp-gebaeudebrueter/) | Nistplatzstandorte mit Karte, Vogelarten nach Stadtkreis | [Gebäudebrüter-Inventar](https://data.stadt-zuerich.ch/dataset/geo_gebaeudebrueter) |

## Projektstruktur

```
dongoginho.github.io/
├── index.html                 Landing Page
├── assets/                    Gemeinsame Ressourcen
│   └── 2026_logo_mcp_server_alex.png
├── mcp-personenwagen/         Personenwagen-Beispiel
│   ├── index.html
│   └── README.md
├── mcp-hunde/                 Hunde-Beispiel
│   ├── index.html
│   ├── update_data.py         Daten-Update-Script
│   ├── CLAUDE.md              Technische Dokumentation
│   └── README.md
└── mcp-gebaeudebrueter/       Gebäudebrüter-Beispiel
    ├── index.html
    └── README.md
```

## Technik

Alle Beispiele sind als einzelne HTML-Dateien umgesetzt (CSS + JS inline, kein Build-Tool). Diagramme werden mit [Chart.js 4](https://www.chartjs.org/) gerendert, Karten mit [Leaflet](https://leafletjs.com/). Die Daten werden live via CKAN Datastore API bzw. WFS von [data.stadt-zuerich.ch](https://data.stadt-zuerich.ch) geladen.

Das Design orientiert sich am Erscheinungsbild von [Statistik Stadt Zürich](https://www.stadt-zuerich.ch/de/politik-und-verwaltung/statistik-und-daten.html) mit Farben aus [zuericolors](https://github.com/StatistikStadtZuerich/zuericolors) und UI-Styling nach [zuericssstyle](https://github.com/StatistikStadtZuerich/zuericssstyle).

## Daten aktualisieren

Das Hunde-Beispiel verfügt über ein Python-Script zur automatischen Datenaktualisierung:

```
cd mcp-hunde
python update_data.py --dry-run   # Vorschau
python update_data.py              # Aktualisieren
```

Details siehe [mcp-hunde/README.md](mcp-hunde/README.md).
