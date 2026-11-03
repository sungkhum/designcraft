# Khmer wrapping and justification evidence

These are unmodified DesignCraft CLI exports, showing the downstream integration of the shared engine in storytold/craft-libs#551 with the app changes in storytold/designcraft#2238. The shared library itself has no UI or layout composer.

Both builds render the same saved document with identical text, frame widths and formatting: Content Enhanced Regular 18 pt, 29 pt leading, paragraph composer, Ligatures On, 270 pt column width, output scale 2. Left column: left aligned. Right column: justified. The paragraph is a user-supplied regression example; no private InDesign book content is included.

Before: the retained local CLI build from before Khmer composition integration. After: the DesignCraft preview at 79521fb0, using the shared Khmer engine at 6be86aa0. Later review fixes in #551 do not change these layout examples. The comparison demonstrates the combined app integration, not changes attributable to the shared library alone or a shipping release.

Supply Content Enhanced Regular in a local Document Fonts folder beside the document, replace /PATH/ in composition-reproduce.json with that absolute directory, then:

```sh
designcraft-cli script composition-reproduce.json --save /PATH/Public-Khmer-Composition.designcraft --export khmer-composition-after.png
designcraft-cli-before run --in /PATH/Public-Khmer-Composition.designcraft --scale 2 --export khmer-composition-before.png
```

The separate subscript PNGs document an app shaping fix; they are not evidence of a change made in craft-libs#551. See README.md for that reproduction.
