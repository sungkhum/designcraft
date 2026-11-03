# Khmer justification evidence

An unmodified DesignCraft CLI export at 50fb910b, using the shared Khmer engine at 2322f68f (storytold/craft-libs#551).

Content Enhanced Regular 18 pt, 29 pt leading, paragraph composer, Ligatures On, 270 pt columns, output scale 2. The justified columns use Word Spacing 100/100/100%, Letter Spacing 0/0/0%, Glyph Scaling 96/100/104% and Single Word Justification Align Left. The paragraph is a user-supplied regression example; the right column adds real spaces to it at word boundaries. No private book content is included.

Supply Content Enhanced Regular in a local Document Fonts folder beside the document, replace /PATH/ in justification-reproduce.json with that absolute directory, then:

```sh
designcraft-cli script justification-reproduce.json --save /PATH/Public-Khmer-Justification.designcraft --export khmer-justification-after.png
```
