# Example Configurations

## Basic Configuration

```yaml
type: custom:power-flow-card
name: Home Energy Flow
threshold: 10
entities:
  solar_power: sensor.solar_power
  grid_import_power: sensor.grid_import
  grid_export_power: sensor.grid_export
```

## Full Configuration with All Options

```yaml
type: custom:power-flow-card
name: Home Energy Flow
threshold: 10
entities:
  solar_power: sensor.solar_power
  grid_import_power: sensor.grid_import
  grid_export_power: sensor.grid_export
  grid_import_daily: sensor.grid_import_daily
  ev_charge_power: sensor.ev_charge
  battery_charge_power: sensor.battery_charge
  battery_discharge_power: sensor.battery_discharge
```

## Custom Styling Examples

### Dark Theme with Blue Accent

```yaml
type: custom:power-flow-card
name: Energy Monitor
threshold: 10
entities:
  solar_power: sensor.solar_power
  grid_import_power: sensor.grid_import
  grid_export_power: sensor.grid_export
styles:
  card-background: "#1a1a2e"
  solar-color: "#ffd700"
  grid-import-color: "#0f3460"
  grid-export-color: "#16213e"
  battery-color: "#533483"
  header-color: "#eaeaea"
```

### Light Theme

```yaml
type: custom:power-flow-card
name: Energy Flow
threshold: 10
entities:
  solar_power: sensor.solar_power
  grid_import_power: sensor.grid_import
  grid_export_power: sensor.grid_export
styles:
  card-background: "#ffffff"
  card-shadow: "0 2px 8px rgba(0,0,0,0.1)"
  solar-color: "#ff9800"
  grid-import-color: "#2196f3"
  grid-export-color: "#4caf50"
  header-color: "#333333"
  label-value-color: "#333333"
  label-text-color: "#666666"
```

### Neon Theme

```yaml
type: custom:power-flow-card
name: Power Flow
threshold: 10
entities:
  solar_power: sensor.solar_power
  grid_import_power: sensor.grid_import
  grid_export_power: sensor.grid_export
styles:
  card-background: "#0a0a0a"
  solar-color: "#00ff00"
  grid-import-color: "#00ffff"
  grid-export-color: "#ff00ff"
  battery-color: "#ffff00"
  ev-color: "#ff0080"
  header-color: "#00ffff"
```

### Minimal Style

```yaml
type: custom:power-flow-card
name: Energy
threshold: 10
entities:
  solar_power: sensor.solar_power
  grid_import_power: sensor.grid_import
  grid_export_power: sensor.grid_export
styles:
  card-background: "transparent"
  card-shadow: "none"
  card-border-radius: "0"
  header-font-size: "14px"
  label-value-font-size: "14px"
  label-text-font-size: "10px"
```

## Using Custom Background SVG

```yaml
type: custom:power-flow-card
name: Home Energy Flow
threshold: 10
background_svg: "/local/custom-background.svg"
entities:
  solar_power: sensor.solar_power
  grid_import_power: sensor.grid_import
  grid_export_power: sensor.grid_export
```
