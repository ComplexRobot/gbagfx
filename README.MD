# gbagfx

Windows port of gbagfx from [pokefirered](https://github.com/pret/pokefirered).

Usage:
```
gbagfx <input_file> <output_file> [<options>]
```

The operation performed is determined by the extensions of the files specified in `input_file` and `output_file`.


## Supported conversions

### GBA to/from PNG

`*.1bpp` `*.4bpp` `*.8bpp` ⟷ `*.png`

Options (GBA to PNG):
```
-palette <file>       Set palette
-object               Enable transparency
-width <value>        Set width
-mwidth <value>       Set metatile width
-mheight <value>      Set metatile height
-tilemap <file>       Set tilemap (*.bin)
-affine               Enable affine map
-plain                Disable tiled
-data_width <value>   Set data width
```

Options (PNG to GBA):
```
-num_tiles <value>    Set number of tiles
-Wnum_tiles           Enable number of tiles warning
-Werror=num_tiles     Enable number of tiles error
-mwidth <value>       Set metatile width
-mheight <value>      Set metatile height
-plain                Disable tiled
-data_width <value>   Set data width
```

### PNG to/from FONT

`*.png` ⟷ `*.latfont` `*.hwjpnfont` `*.fwjpnfont`

### PNG to Palette

`*.png` ⟶ `*.gbapal` `*.pal`

### GBA Palette to/from JASC Palette

`*.gbapal` ⟷ `*.pal`

Options (JASC Palette to GBA Palette):
```
-num_colors   Set number of colors
```

### Compress/Decompress

`*.*` ⟷ `*.huff` `*.lz` `*.rl`

Options (to `*.lz`):
```
-overflow <size>   Set overflow size
-search <size>     Set LZ min search distance
```

Options (to `*.huff`):
```
-depth (4|8)   Set bit depth
```