# 🚀 sc-component-data

**El corazón de datos del Stream Deck de Star Citizen de @raspiardui** — extraído de **su propia instalación del juego** (Data.p4k vía StarBreaker + sc-gamedata-extractor) y complementado con fuentes de la comunidad (siempre acreditadas).

La app web (`192.168.1.139:5001`) lo consume con un botón 🔄, y cada parche de SC genera su propio **commit + tag con el número de build** (`build-4.10.196.36804` / estilo launcher `4.10.2-live.12881860`).

## 📦 Contenido

| Ruta | Qué es | Origen |
|---|---|---|
| `power_components.json` | Potencia: generación de plants, consumo de coolers/escudos/QD + **curvas PowerRangeParams (0.7/0.85/1)** | 🟢 Mi juego |
| `ships/ships_stock.json` | Stock de componentes por nave (loadout real de puertos) + info (rol/crew/dims) | 🟢 Mi juego |
| `ships/weapon_ports.json` | 191 defs de puertos de armas (SItemPortDef: MinSize/MaxSize) | 🟢 Mi juego |
| `ships/ships_catalog_app.json` | Catálogo de la app (318 naves/vehículos con fotos) | App |
| `components/*.json` | **81 categorías / 8.030 componentes** (`components_all.json` = merge) | 🟢 Mi juego |
| `data/components_stats.json` | **Stats reales**: daño/rango/RPM (armas), salud/regen (escudos), EM/IR... (747) | 🔵 scunpacked (wiki) |
| `data/geodesy.json` | 38 cuerpos + **626 POIs con coordenadas** (radios, cuaterniones) | 🔵 Navitool |
| `data/starmap_positions.json` | Posiciones absolutas del starmap | 🔵 scunpacked |
| `images/ships/` | **291 fotos de naves** (100% del catálogo) | 🟡 wiki + BlueMystical |
| `images/components/` | **245 renders de componentes** + `manifest.json` (cutouts ingame de la wiki) | 🟡 wiki |
| `PENDIENTES.md` | Checklist de faltantes | — |

## 🔄 Actualización por parche

1. Parche de Star Citizen → el pipeline lee `D:\StarCitizen\LIVE\build_manifest.id`
2. Botón **📤 Extraer y publicar** en la app (solo en el PC del dueño)
3. Commit: `build 4.10.196.36804 sc-alpha-4.10.2 - fecha` + **dos tags**: `build-X` + `<parche>-live.<cambio>`
4. Los amigos solo pulsan **🔄** y ya tienen los datos del parche

Manual: `extraer_y_publicar.ps1 -Repo "git@github.com-datos:raspiardui/sc-component-data.git"`

## 🤝 Fuentes y créditos

- 🟢 **Lo principal sale del Data.p4k del propio juego** (StarBreaker + extractores propios)
- 🔵 [scunpacked-data](https://github.com/StarCitizenWiki/scunpacked-data) (StarCitizenWiki) — stats
- 🔵 [Navitool](https://zakuul.horizongames.es/horizons-command/) — geodesia/coords
- 🔵 [SeekND/Hardpoint](https://github.com/SeekND/Hardpoint) — rangos por nave (suplemento)
- 🟡 [starcitizen.tools wiki](https://starcitizen.tools) — fotos de naves + cutouts de componentes (autores de la comunidad, licencia CC-BY-SA)
- 🟡 [BlueMystical/SC-Ships](https://github.com/BlueMystical/SC-Ships) — fotos de relleno

> Los datos del juego son © Cloud Imperium Games (uso comunitario/de referencia). Las imágenes pertenecen a sus autores respectivos.

## 📋 Estado

- Naves/vehículos: **318/318 con foto**
- Componentes: 8.030 extraídos · 747 con stats · 245 con render
- Build activo: mira el último tag 🏷️
