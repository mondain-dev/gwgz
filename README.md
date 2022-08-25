# 古文觀止

## Dependencies
- uplatex
- [rIMing font](https://github.com/mondain-dev/rIMing)
- [源石黑體](https://github.com/ButTaiwan/genseki-font): `GenSekiGothic-M.ttc`
- AR PL UKai: `ukai.ttc`

## Build
Build `upzhserif-v.tfm`, `upzhserif-v.vf`, `upzhserifb-v.vf`, `uptchrm-v.vf` (overriding the CTeX default):
```
jfmutil zpl2tfm -u --lenient upzhserif-v.zpl
jfmutil zvp02vf -u --lenient upzhserif-v.zvp0
jfmutil zvp2vf -u --lenient upzhserifb-v.zvp 
jfmutil zvp2vf -u --lenient uptchrm-v.zvp 
```
Make sure that the fonts used in this document are reachable:
```
ln -s /path/to/rIMing.ttf rIMing.ttf
ln -s /path/to/GenSekiGothic-M.ttc GenSekiGothic-M.ttc
ln -s /path/to/ukai.ttc ukai.ttc
```
Build using `uplatex`: 
```
uplatex gwgz && uplatex gwgz && dvipdfmx gwgz
```
