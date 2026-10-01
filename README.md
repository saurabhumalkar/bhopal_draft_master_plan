# Bhopal Development Plan 2047 — V1 OSM Overlay Viewer

This is the first prototype of the proposed Bhopal DP-2047 map viewer.

## What it does

- OpenStreetMap standard road/base map
- Official Bhopal Development Plan 2047 zoning map as an image overlay
- Overlay opacity slider
- Show/hide overlay
- Fit map to the DP-2047 planning-map extent
- Basic DP-2047 land-use legend
- **No Google Maps API key or Google Cloud billing is required**

## Important

The supplied PDF was produced by Esri ArcMap and contains embedded GeoPDF geographic viewports. The V1 overlay was rendered from the main Bhopal planning-area map frame and positioned using the embedded geographic extent.

The four-corner geographic extent used by this prototype is approximately:

- North: 23.43375
- South: 23.06022
- West: 77.15675
- East: 77.61473

This is a visual prototype, not a cadastral/survey/legal map. Before relying on parcel-level alignment, the overlay should be validated against known coordinates and, if necessary, upgraded to a quadrilateral/true GeoPDF-to-Web-Mercator transformation.

## Run

1. Unzip this folder.
2. Start a local web server from this directory:

   `python -m http.server 8080`

3. Open:

   `http://localhost:8080/`

No API key is required.

## Base map

The viewer uses the standard OpenStreetMap tile service at `https://tile.openstreetmap.org/{z}/{x}/{y}.png` and displays the required OpenStreetMap attribution.

The standard OSM tile service is not an unlimited public CDN. This is appropriate for a small prototype and local testing. If the application is later published to many users, use a suitable third-party tile provider or host your own tiles according to the provider's terms.

## Source

Directorate of Town & Country Planning, Madhya Pradesh, Bhopal — Bhopal Development Plan 2047 (Draft), Map No. 14.2, dated 25 September 2026.
