# 古文觀止

## Dependencies
- uplatex
- Microsoft fonts `simsun.ttc`, `simhei.ttf`, `simkai.ttf`, `simsunb.ttf`
- [BabelStone Han](https://www.babelstone.co.uk/Fonts/Han.html): `BabelStoneHan.ttf`

## Build
Build `upzhserif-v.tfm` (overriding the CTeX default):
```
jfmutil zpl2tfm -u --lenient upzhserif-v.zpl
```
Make sure that the fonts used in this document are reachable:
```
ln -s /path/to/simsun.ttc simsun.ttc
ln -s /path/to/simkai.ttf simkai.ttf
ln -s /path/to/simhei.ttf simhei.ttf
ln -s /path/to/simsunb.ttf simsunb.ttf
ln -s /path/to/BabelStoneHan.ttf BabelStoneHan.ttf
```
Build using `uplatex`: 
```
uplatex gwgz && uplatex gwgz && dvipdfmx gwgz
```

## WARNING
The `gwgz.pdf` is not updated for each commit, therefore may not always represent the current build.
