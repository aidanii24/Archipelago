For the original Archipelago README.md and project, please visit the upstream [ArchipelagoMW repository](https://github.com/ArchipelagoMW/Archipelago).

# Archipelago: Material You Enhanced

![image](https://i.imgur.com/FzFnjhf.gif)

A Fork of the Archipelago Launcher that exposes more of the underlying Material You Color features of KivyMD, allowing for more advanced theming.

# Features

- Auto-generating colors from a provided wallpaper
- Meticulous specification of Material You Colors
- Live hot reloading of themes

# Limitations

- Tkinter Components are not affected
- Text colored with Text Markup (Item messages on the Archipelago Tab of a Text Client) will only use the colors available when they are first rendered, and will not change if the theme changes.
- Most custom widgets from clients may not be affected, or may only apply the initial colors on launch at best, depending on if and how they set the colors.

# Usage

Archipelago MYE refers to a `theme.yml` file for it's current theming. It will try to find it inside the Archipelago directory, under `data/themes/`. When this file is present and is valid, it will use its content to theme the Launcher and Clients where possible.

The `theme.yml` is always watched for changes, so Archipelago will update its theme in real time when it detects changes to the file.

## Templates

Templates are available and come with the package inside the Archipelago directory, under `data/themes/templates/`. They can be used as foundation for your own custom theme, or be fed to a templating engine to automatically generate a theme for you. More details on how to use the templates can be found inside them.

## Specification

Below are the available properties that can be set for the `theme.yml` file.
|Property|Value |Description|
|--------|-------------------|------------|
|`mode` |`"Light"`, "`Dark`"|Whether the theme is a Light or Dark mode theme.|
|`scheme`| `"TONAL_SPOT"`, `"SPRITZ"`, `"VIBRANT"`, `"EXPRESSIVE"`, `"FRUIT_SALAD"`, `"RAINBOW"`, `"MONOCHROME"`, `"FIDELITY"`, `"CONTENT"`| The Material You Scheme used for Color Generation.|
|`use_wallpaper`|`true`, `false`|Whether to use the provided Wallpaper and automatically generate colors from it. Any custom Material You Color properties set in the file will be ignored if a wallpaper is used.|
|`path_to_wallpaper`|Image path (e.g. `/home/aginah/Pictures/wallpaper.jpg`)|Path to the wallpaper image.|
|Dynamic Colors|Color in Hex Format (e.g. `#FF5030`)|The colors as specified in the Material You Color design specification. The main colors that will applied application-wide.|
|Base16 Colors|Color in Hex Format (e.g. `#FF5030`)|The original 16 Colors as specified by the ANSI Colors standard. These are primarily used to override the Text Colors in `data/client.kv`.

### Dynamic Colors

These are the valid Dynamic Color property names recognized by Archipelago MYE, used to color KivyMD components that derives from the KivyMD Theme Manager.

- `background_color`
- `error_color`
- `error_container_color`
- `error_dim_color`
- `error_palette_key_color_color`
- `inverse_on_surface_color`
- `inverse_primary_color`
- `inverse_surface_color`
- `neutral_palette_key_color_color`
- `neutral_variant_palette_key_color_color`
- `on_background_color`
- `on_error_color`
- `on_error_container_color`
- `on_primary_color`
- `on_primary_container_color`
- `on_primary_fixed_color`
- `on_primary_fixed_variant_color`
- `on_secondary_color`
- `on_secondary_container_color`
- `on_secondary_fixed_color`
- `on_secondary_fixed_variant_color`
- `on_surface_color`
- `on_surface_variant_color`
- `on_tertiary_color`
- `on_tertiary_container_color`
- `on_tertiary_fixed_color`
- `on_tertiary_fixed_variant_color`
- `outline_color`
- `outline_variant_color`
- `primary_color`
- `primary_container_color`
- `primary_dim_color`
- `primary_fixed_color`
- `primary_fixed_dim_color`
- `primary_palette_key_color_color`
- `scrim_color`
- `secondary_color`
- `secondary_container_color`
- `secondary_dim_color`
- `secondary_fixed_color`
- `secondary_fixed_dim_color`
- `secondary_palette_key_color_color`
- `shadow_color`
- `surface_color`
- `surface_bright_color`
- `surface_container_color`
- `surface_container_high_color`
- `surface_container_highest_color`
- `surface_container_low_color`
- `surface_container_lowest_color`
- `surface_dim_color`
- `surface_tint_color`
- `surface_variant_color`
- `tertiary_color`
- `tertiary_container_color`
- `tertiary_dim_color`
- `tertiary_fixed_color`
- `tertiary_fixed_dim_color`
- `tertiary_palette_key_color_color`

### Base16/ANSI Colors

These are the valid Base16/ANSI Color names recognized by Archipelago MYE. They are mapped accordingly to the Text Colors specified in `data/client.kv` and will supercede them when these colors are present.

- `"base00"` (0, Black)
- `"base01"` (1, Red)
- `"base02"` (2, Green)
- `"base03"` (3, Yellow)
- `"base04"` (4, Blue)
- `"base05"` (5, Magenta)
- `"base06"` (6, Cyan)
- `"base07"` (7, White)
- `"base08"` (8, Bright Black)
- `"base09"` (9, Bright Red)
- `"base0a"` (A, Bright Green)
- `"base0b"` (B, Bright Yellow)
- `"base0c"` (C, Bright Blue)
- `"base0d"` (D, Bright Magenta)
- `"base0e"` (E, Bright Cyan)
- `"base0f"` (F, Bright White)
