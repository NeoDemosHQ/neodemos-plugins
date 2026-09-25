# NeoDemos plugins

NeoDemos ontsluit de raadsinformatie van Rotterdam: moties, notulen, begrotingen en collegebrieven van 2002 tot vandaag, ruim 90.000 documenten. Je stelt een vraag, de plugin zoekt in de stukken en geeft bij elk antwoord de bron mee, tot op het oorspronkelijke document.

Je zoekt in moties, notulen, begrotingen en stemmingen, laat een concepttekst beoordelen, verzamelt context met citaten en laat een fractienotitie of raadsstuk opstellen met de bronvermelding er al in.

Je logt één keer in met je NeoDemos-account; de plugin verbindt met `https://mcp.neodemos.nl/mcp`. Heb je een fractie-account, dan kun je bij het inloggen ook toegang geven tot de fractiewerkruimte met notities en opgeslagen stukken.

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

Elke client die een remote MCP-server over Streamable HTTP met OAuth
ondersteunt kan rechtstreeks verbinden met `https://mcp.neodemos.nl/mcp`. Je
logt één keer in via de browser. Voorbeeld voor Claude Code zonder plugin:

```
claude mcp add --transport http neodemos https://mcp.neodemos.nl/mcp
```

## Claude.ai (zonder plugin)

Voeg de server toe als custom connector:
<https://claude.ai/customize/connectors?modal=add-custom-connector&connectorName=NeoDemos&connectorUrl=https%3A%2F%2Fmcp.neodemos.nl%2Fmcp>

## Inloggen

Sinds 25 september 2026 werkt de NeoDemos-MCP alleen na inloggen met je
NeoDemos-account. Het oude adres `https://mcp.neodemos.nl/public/mcp` stopt;
een verbinding die daar nog naar wijst, krijgt de melding om in te loggen.
Werk de plugin bij (`/plugin update neodemos@neodemos`) of vervang in je
client het adres door `https://mcp.neodemos.nl/mcp`. Nog geen account?
Maak er een aan op [neodemos.nl](https://neodemos.nl/mcp-installer).

## Versie

De pluginversie volgt de live serverversie (`serverInfo.version`).
Wijzigingen: [CHANGELOG](https://neodemos.nl/wat-is-nieuw).

Licentie voor deze manifesten: MIT. De dienst zelf valt onder de
[gebruiksvoorwaarden](https://neodemos.nl/voorwaarden) en de
[privacyverklaring](https://neodemos.nl/privacy) van NeoDemos.
