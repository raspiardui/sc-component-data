# sc-component-data
Datos de Star Citizen extraidos por @raspiardui desde su propia instalacion del juego.
Fuente: Data.p4k via StarBreaker + sc-gamedata-extractor.

## Contenido
- `power_components.json` - potencia: plants (Generation.Power) y consumo (Usage) de coolers/shields/QD
- `ships/ships_stock.json` - stock de componentes por nave (puertos del loadout real)

## Actualizar (por parche)
Boton **Pulsa en la app** ... o manualmente:
`extraer_y_publicar.ps1 -Repo "git@github.com-datos:raspiardui/sc-component-data.git"`

## Consumo
La app Stream Deck lo lee desde raw.githubusercontent.com y tambien hay un boton de actualizacion.
