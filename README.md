
# Urban green accessibility in Turin
## Do residents of Turin have equal access to green spaces?

This project analyses the spatial relationship between residential buildings 
and publicly accessible green spaces across Turin's 8 administrative districts 
(*circoscrizioni*), using open data and open source tools.

## Key findings

| Circoscrizione | Green access |
|---|---|
| Borgo Vittoria - Madonna di Campagna - Lucento | 4.9% |
| Barriera di Milano - Regio Parco - Barca - Bertolla | 8.2% |
| Aurora - Vanchiglia - Sassi - Madonna del Pilone | 55.9% |
| San Salvario - Cavoretto - Borgo Po - Nizza Millefonti | 57.1% |
| San Donato - Campidoglio - Parella | 59.2% |
| Centro - Crocetta | 66.1% |
| San Paolo - Cenisia - Pozzo Strada - Cit Turin | 83.5% |
| Santa Rita - Mirafiori | 95.6% |

## Data sources
- Overture Maps (2026-02-18) — residential buildings
- OpenStreetMap via Overpass Turbo — parks, gardens, forests, recreation areas
- Comune di Torino — administrative boundaries (EPSG:3003)

## Tools
- DuckDB + spatial extension — spatial queries and ST_DWithin analysis
- QGIS — green layer extraction and clipping
- Python / Pandas — data wrangling and export

## How to run
1. Clone the repository
2. Set `BASE_DIR` and `SHP_DIR` in the first cell of the notebook to point to your dir.
3. Run all cells — the S3 query requires an internet connection
4. Output files are saved in `BASE_DIR`

## Methodology notes
- Green access defined as at least one green space within 300m walking distance
- Analysis covers 17,178 residential buildings inside the municipal boundary
- Does not distinguish between public and private green spaces
- Private gardens and enclosed parks may inflate accessibility figures 
  in hillside districts (circoscrizione 7)
- AI assistance: Claude (Anthropic)
