# KiCad Library

## Description

This is parts library to be used for any KiCad project. It includes
common symbols, footprints, 3D models and should be updated
every time a new part is used. A lot of these have been taken from the
[KiCad library](https://gitlab.com/kicad/libraries) and modified to remove
excess silkscreen and adjust pads. Some common parts have been added as well,
including new footprints and 3D models.

This library is composed of several folders:
- `3dmodels` contains the 3D models
- `footprints` contains the footprints
- `symbols` contains the schematic symbols

## Usage

Add the following environment variables in Preferences -> Configure Paths:
- `USER_3DMODEL_DIR`: the absolute path of the `3dmodels` folder
- `USER_FOOTPRINT_DIR`: the absolute path of the `footprints` folder
- `USER_SYMBOL_DIR`: the absolute path of the `symbols` folder

The library can also be added as a submodule of a KiCad project. In that case,
the base directory can be configured as `${KIPRJMOD}/kicad-library/`,
e.g. `${KIPRJMOD}/kicad-library/3dmodels` for the `USER_3DMODEL_DIR` variable.

Replace or merge the symbol and footprint tables (`sym-lib-table`,
`fp-lib-table`) present in the KiCad preferences folder with the files in the
folder `config`.

On Linux, the preferences are in `~/.config/kicad`.
On Windows, the preferences are in `%APPDATA%\kicad`
(= `%HOMEPATH%\AppData\Roaming\kicad`).
On macOS, the preferences are in `~/Library/Preferences/kicad`.
