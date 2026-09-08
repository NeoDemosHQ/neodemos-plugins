# NeoDemos plugins

Plugin-marketplace voor de NeoDemos MCP-server: bronverankerde raadsinformatie
voor Nederlandse gemeenteraden (nu Rotterdam, 2002–heden). De plugin verbindt
je AI-client met de publieke server `https://mcp.neodemos.nl/public/mcp`; er is
geen login nodig en het verkeer is per IP begrensd.

Deze repository bevat alleen manifesten en beeldmateriaal. De server zelf en
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
[privacyverklaring](https://neodemos.nl/privacy) van NeoDemos.
