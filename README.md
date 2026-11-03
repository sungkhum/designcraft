# Khmer subscript shaping evidence

Visual evidence for storytold/designcraft#2238, fix 79521fb0edaf2bfb19508ee00d563f1e9b4a1f38.

Both PNGs are unmodified DesignCraft CLI exports of the same document: Content Enhanced Regular, 36 pt, Ligatures Off, 2x output scale. The before binary precedes the shaping fix (2cf9b371); the after binary includes it (79521fb0).

Text: ក្ខ    ខ្មែរ    ព្រះ    ស្ត្រី    ប្រទេស

The corrected export is byte-identical to a reference export from the earlier binary with Ligatures On. This verifies preservation of that previously correct rendering; it does not claim correctness for every font or document.

No private book content or font binaries are included. To reproduce, supply Content Enhanced Regular locally in a `Document Fonts` folder beside `Public-Khmer-Shaping.designcraft`, substitute an absolute output path for `/PATH/` in the script, and run:

```sh
designcraft-cli script reproduce.json --save /PATH/Public-Khmer-Shaping.designcraft --export after.png
# Use the pre-fix binary with the same document and font:
designcraft-cli-before run --in /PATH/Public-Khmer-Shaping.designcraft --scale 2 --export before.png
```
