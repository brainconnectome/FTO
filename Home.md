Welcome to the code_fto_c2b2 wiki!

2018/03/14

1. Testing newest eddy_cuda (cuda runtime 7.5 installed on c2b2) with --repol and --s2vr options

-eddy_cuda took ~1hr per image (28 dirs)

-before and after eddy_cuda

-note that *CERTAIN* GPU cards in c2b2 have outdated drivers that are *NOT* compatible with either cuda runtime version of 7.5, 8.0. 

![eddy_cuda before and after](https://github.com/jcha9928/code_fto_c2b2/blob/master/img/eddy_cuda.jpg)


2. subjects with irregular # of slices
subject 10750 (slice #53) and 133997 (slice #58) have irregular slice numbers. This must be corrected for dwipreprocess, particularly with eddy_cuda with s2v correction option where you need to provide slice order information as a text file (slspec.txt).

*These two subjects were cropped to have 52 (even number) slices.