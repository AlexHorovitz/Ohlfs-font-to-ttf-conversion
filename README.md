# Ohlfs-font-to-ttf-conversion
Among the many UI accomplishments by Keith Ohlfs at NeXT is this wonderful little font. It has never been modernized to work on the current version of the OS and unfortunately Keith passed away unexpectedly (October 26th, 2016). Anyone who is willing to help in this effort is invited to join.  

## Files

Original sources from NeXTStep /Library/Fonts are in `Ohlfs.font/`.

BDF files from which `Ohlfs.font/Ohlfs.bepf` is generated are archived in [github.com/johnsonjh/NeXTDPS](https://github.com/johnsonjh/NeXTDPS/tree/master/fonts-21/bitmapSources/Ohlfs).

Updated BDF files (see [Process](#process)) are in `Updated_BDFs/`.

`Ohlfs-Light.otf` is based on the updated bitmaps for 9, 10, 12, and 14px; it includes a vector description and embedded bitmaps

`Ohlfs-Medium.otf` is based on the updated bitmaps for 16 and 18px; it also includes a vector description and embedded bitmaps

`Ohlfs.dfont` and `Ohlfs.ttf` are based on the original (non-updated) BDF files

## Process

The files in `Updated_BDFs/` were amended to include lines explicitly describing `pixel_size`, `point_size`, and resolution. This makes them interpretable by FontForge, from which SFD-format bitmaps were generated. These SFDs were fed through [BitsNPicas](https://github.com/kreativekorp/bitsnpicas) to generate vector fonts. FontForge was then used again to combine those vectored fonts with their bitmap strikes. 

Since the bitmap strikes for 9-14px and 16-18px are substantially different, they are presented here as different weights of the Ohlfs font family.