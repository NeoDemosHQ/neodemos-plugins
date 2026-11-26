# NeoDemos plugins

Het voorwerk is gedaan, het denkwerk is aan jou. NeoDemos ontsluit openbare raadsstukken van Nederlandse gemeenten en provincies: moties, notulen, begrotingen, collegebrieven en stemmingen. Je stelt een vraag in gewone taal, de plugin zoekt in de stukken en geeft bij elk antwoord de bron mee, tot op het oorspronkelijke document. De dekking groeit; de plugin laat zelf zien welke stukken voor jouw gemeente beschikbaar zijn.

De contextprimer vertelt wie er nu in het college zit en welke coalities er waren. Het instrumentadvies zegt of je met een motie, een amendement of een initiatiefvoorstel het verst komt. Je laat een concepttekst beoordelen, verzamelt context met citaten, en laat een fractienotitie of raadsstuk opstellen met de bronvermelding er al in.

Je logt één keer in met je NeoDemos-account. Fractieleden lezen ook hun fractiewerkruimte en slaan daar stukken op na bevestiging. Documentatie: <https://neodemos.nl/koppelen>.

Deze repository bevat de plugin-manifesten en het beeldmateriaal. De server en
de documentatie staan op [neodemos.nl](https://neodemos.nl/mcp-installer).

## Claude Code / Claude Desktop

```
/plugin marketplace add NeoDemosHQ/neodemos-plugins
/plugin install neodemos@neodemos
```

## Codex (CLI en app)

```
codex plugin marketplace add NeoDemosHQ/neodemos-plugins
codex plugin add neodemos
```

## Claude Cowork en Claude Desktop

Open het pluginmenu (+ → Plugins → Add plugin), kies de marketplace
`NeoDemosHQ/neodemos-plugins` en installeer `neodemos`. Dezelfde marketplace
werkt in Claude Code en Cowork.

## Andere clients (Cursor, Gemini CLI, Le Chat, Windsurf)

Elke client die een remote MCP-server over Streamable HTTP ondersteunt kan
rechtstreeks verbinden met `https://mcp.neodemos.nl/mcp`. Je logt één keer in
via de browser. Voorbeeld voor Claude Code zonder plugin:

```
claude mcp add --transport http neodemos https://mcp.neodemos.nl/mcp
```

## Claude.ai (zonder plugin)

Voeg de server toe als custom connector:
<https://claude.ai/customize/connectors?modal=add-custom-connector&connectorName=NeoDemos&connectorUrl=https%3A%2F%2Fmcp.neodemos.nl%2Fpublic%2Fmcp>

## Fractie-werkruimte

De werkruimte (notities, opgeslagen stukken, spreektijd) staat op de
OAuth-beveiligde server `https://mcp.neodemos.nl/mcp`. Die is bewust niet in
deze plugin opgenomen; voeg hem toe als custom connector of via
`claude mcp add --transport http neodemos-werkruimte https://mcp.neodemos.nl/mcp`.

## Versie

De pluginversie volgt de live serverversie (`serverInfo.version`).
Wijzigingen: [CHANGELOG](https://neodemos.nl/wat-is-nieuw).

Licentie voor deze manifesten: MIT. De dienst zelf valt onder de
[gebruiksvoorwaarden](https://neodemos.nl/voorwaarden) en de
[privacyverklaring](https://neodemos.nl/privacy) van NeoDemos.
