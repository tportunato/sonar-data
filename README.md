# sonar-data

Open French public data, stored per commune so an application can read it in
one request instead of paging three public services.

Each file `v1/<INSEE code>.json.gz` holds, for one commune, as fetched on the
date in its `at` field:

- **parcels**: the cadastre (DGFiP, served by IGN's API Carto)
- **buildings**: BD TOPO (IGN)
- **zones**: local planning zones (Géoportail de l'urbanisme)

`v1/index.json` lists the files with their date and counts.

Sources are published under Licence Ouverte 2.0. Nothing here is modified: the
files are a copy of what those services returned on that day, and they can be
out of date. The official services are the reference.
