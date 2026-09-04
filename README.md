For the original Archipelago README.md and project, please visit the upstream [ArchipelagoMW repository](https://github.com/ArchipelagoMW/Archipelago).

# Archipelago: Material You Enhanced

A Fork of the Archipelago Launcher that exposes more of the underlying Material You Color features of KivyMD, allowing for more advanced theming.

# Features

- Auto-generating colors from a provided wallpaper
- Meticulous specification of Material You Colors
- Live hot reloading of themes

# Limitations

- Text colored with Text Markup are not affected
- Clients with widgets that uses colors not provided by the KivyMD Theme Manager or the JSONParser are not affected

# Usage

Archipelago MYE will look for a file `data/themes/theme.yml` in the Archipelago directory. This theme file specifies the wallpaper to use for color generation, or the values of the Material You Color properties. This file is always watched for changes, meaning that Archipelago will always update the colors immediately as soon as the change is detected.

## Templates

Inside the `data/themes/templates` folder are templates for common use. They can be used as foundation for a new theme. This folder also includes templates for external color generators, allowing for an easy way to make Archipelago stay consistent with your system and other applications color and theme.
