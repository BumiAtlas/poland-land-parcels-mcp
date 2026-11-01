# Poland Land Parcels & Sale Price Lookup MCP (Polska)

[Polski](#polski)

Connect your AI assistant (Claude, ChatGPT, Cursor) to [BumiAtlas](https://bumiatlas.com) for Polish land research through the Model Context Protocol (MCP).

This listing is a focused entry point for:

- Cadastral parcels (działki) from GUGiK's open EGiB (land and building register) exports
- Parcel lookup by id_działki (`040602_2.0008.66`: TERYT unit, obręb, number) or coordinates
- Registered area, land-use classes (klasoużytki), obręb and gmina
- Recorded sales from the RCN price register: date, deed, price (whole transaction and the parcel's share, PLN), seller and buyer types, land use and zoning
- Satellite and street map images of a parcel and its neighbours, labelled by parcel number

Names aren't searchable: search by id_działki or coordinates. Sales list party types (a private person, the gmina, …), never names.

## Connect

```
https://bumiatlas.com/mcp/poland
```

Add it as a custom connector in any MCP client and sign in with Google. Tools, examples and data notes: [bumiatlas.com/mcp-docs/poland](https://bumiatlas.com/mcp-docs/poland).

- **Claude:** Settings → Connectors → Add custom connector, paste the URL, then Connect.
- **ChatGPT:** Settings → Apps & Connectors → Advanced → Developer mode, then Create with the URL and OAuth authentication.

## Tools

| Tool | Description |
|---|---|
| `PL_parcel_search` | Find parcels by id_działki or `latitude, longitude`; each result is the whole record with up to 10 recorded sales, the boundary as GeoJSON on request |
| `PL_parcel_image` | Satellite or street map image of a parcel or point, with every parcel in view outlined and labelled with its number |

## Example prompts

- *"Which parcel is at 52.2297, 21.0122? Has it been sold?"*
- *"Look up parcel 040602_2.0008.66 and show it on satellite imagery."*
- *"What did the parcels around this point sell for?"*
- *"What land-use classes does this parcel have?"*

## Data source

Działki © GUGiK, Ewidencja Gruntów i Budynków and Rejestr Cen Nieruchomości (geoportal.gov.pl open data). A copy of public data for research, not a legal land record.

## Polski

Połącz swojego asystenta AI (Claude, ChatGPT lub Cursor) z [BumiAtlas](https://bumiatlas.com) przez Model Context Protocol (MCP), aby badać działki w Polsce.

- Działki ewidencyjne z otwartych danych EGiB (GUGiK)
- Wyszukiwanie po identyfikatorze działki (`040602_2.0008.66`) lub współrzędnych
- Powierzchnia, klasoużytki i transakcje z Rejestru Cen Nieruchomości (RCN)

Transakcje podają rodzaj strony (osoba fizyczna, gmina…), nigdy nazwiska.

**Połączenie:** dodaj `https://bumiatlas.com/mcp/poland` jako własny konektor w kliencie MCP i zaloguj się kontem Google. Nazwy narzędzi są po angielsku, ale asystent może odpowiadać po polsku.
