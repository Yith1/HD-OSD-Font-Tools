# HD OSD Font Tools

A tool for building and manipulating the HD OSD fonts for HDZERO VRXs and goggles. The initial version is supposed to build HD OSD fonts for the Betaflight (BTLF) FC variant. For the INAV6 FC variant the tool has a limited support to create the logo.

- [HD OSD Font Tools](#hd-osd-font-tools)
  - [Usage](#usage)
  - [Command line options and values](#command-line-options-and-values)
    - [Option `-base`](#option--base)
  - [Option values](#option-values)
    - [Values for bitmaps](#values-for-bitmaps)


## Usage

The tool is command line based with a graphical preview of the built font. User can choose one or more sources to build the font.

The source can be:

- HDZERO OSD font (.bmp)
- true type font file (.ttf)
- Analog OSD font file (.mcm)
- Analog OSD font preview file (.png / .bmp)
- Generic bitmap, typically containing a logo (.png / .bmp / .jpg)

The source can be used as a part of the built font such as:

- all glyphs
- characters
- numbers
- letters
- special characters
- values icons
- units symbols
- home arrow
- AHI elements
- logo
- etc.

## Command line options and values

Typical usage is:

```
fontbuilder.exe -option1 file1 value01 value02 value03 -option2 file2 -option3 -option4
```

Each option sets the source of the font to be built. The options are processed in order as they are entered. Please note that some options may overwrite the glyphs generated by previous option(s).


### Option `-base`

- sets the base content of the font
- loads all the possible glyphs from the source file
- valid file formats
  - png
  - bmp
  - mcm
  - ttf


## Option values

Option values are dependent on the input file formats. The values tell how the input file is used to render given glyphs

### Values for bitmaps

Bitmap files (png, bmp) don't support any values, the input bitmap file is taken as-is and is processed automatically. The tool will automatically guess the content of the bitmap and will use it accordingly (glyphs, logo, etc...)

