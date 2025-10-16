# 古文觀止

## Dependencies
- uplatex
- [rIMing font](https://github.com/mondain-dev/rIMing)
- AR PL UKai: `ukai.ttc`
- [KingHwa_OldSong](https://zhuanlan.zhihu.com/p/637491623)
- OldHeiGBK


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
ln -s /path/to/ukai.ttc ukai.ttc
ln -s /path/to/京華老宋体v2.ttf kinghwa.ttf
ln -s /path/to/OLDHEIGBK.ttf OLDHEIGBK.ttf 
```
Build using `uplatex`: 
```
uplatex gwgz && uplatex gwgz && dvipdfmx gwgz
```
