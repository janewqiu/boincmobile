# Profiling SETI on Nehalem/Westmere (Core i3 330M) #

```

Mon Oct  3 00:32:53 CDT 2011
CPU: Intel Westmere microarchitecture, speed 2.133e+06 MHz (estimated)
Counted CPU_CLK_UNHALTED events (Clock cycles when not halted) with a unit mask of 0x00 (No unit mask) count 200000
Counted INST_RETIRED events (number of instructions retired) with a unit mask of 0x00 (No unit mask) count 200000
Counted LLC_MISSES events (Last level cache demand requests from this core that missed the LLC) with a unit mask of 0x41 (No unit mask) count 200000
Counted LLC_REFS events (Last level cache demand requests from this core) with a unit mask of 0x4f (No unit mask) count 200000
CPU_CLK_UNHALT...|INST_RETIRED:2...|LLC_MISSES:200000|  LLC_REFS:200000|
  samples|      %|  samples|      %|  samples|      %|  samples|      %|
------------------------------------------------------------------------
   612285 97.4238    783789 98.7377       503 95.6274      1920 94.9555 seti_boinc
     4204  0.6689       458  0.0577         0       0         3  0.1484 no-vmlinux
     1525  0.2427      1136  0.1431         2  0.3802        10  0.4946 libc-2.12.1.so
     1393  0.2216      2106  0.2653         2  0.3802         2  0.0989 oprofiled
     1275  0.2029       739  0.0931         2  0.3802         6  0.2967 libglib-2.0.so.0.2600.0
      935  0.1488      1526  0.1922         2  0.3802         2  0.0989 libdrm_intel.so.1.0.0
      709  0.1128       551  0.0694         0       0         5  0.2473 libcairo.so.2.11000.0
      630  0.1002       120  0.0151         5  0.9506        10  0.4946 python2.6
      540  0.0859       205  0.0258         2  0.3802        13  0.6429 Xorg
      527  0.0839       333  0.0419         0       0         6  0.2967 libgobject-2.0.so.0.2600.0
      414  0.0659       218  0.0275         1  0.1901         8  0.3956 libgtk-x11-2.0.so.0.2200.0
      371  0.0590       332  0.0418         0       0         7  0.3462 libpthread-2.12.1.so
      362  0.0576       237  0.0299         0       0         1  0.0495 ld-2.12.1.so
      356  0.0566       235  0.0296         1  0.1901         3  0.1484 libpango-1.0.so.0.2800.1
      298  0.0474       136  0.0171         0       0         4  0.1978 libgdk-x11-2.0.so.0.2200.0
      297  0.0473       220  0.0277         1  0.1901         2  0.0989 intel_drv.so
      281  0.0447       316  0.0398         0       0         1  0.0495 libpangoft2-1.0.so.0.2800.1
      188  0.0299       287  0.0362         0       0         0       0 libpcre.so.3.12.1
      153  0.0243        28  0.0035         0       0         1  0.0495 perl
      152  0.0242       133  0.0168         0       0         0       0 libpixman-1.so.0.18.4
      151  0.0240        25  0.0031         0       0         2  0.0989 i965_dri.so
      125  0.0199        48  0.0060         0       0         2  0.0989 libdbus-1.so.3.5.2
      113  0.0180        60  0.0076         1  0.1901         1  0.0495 mysqld
       89  0.0142        18  0.0023         1  0.1901         3  0.1484 libX11.so.6.3.0
       81  0.0129        73  0.0092         0       0         0       0 ophelp
       80  0.0127        65  0.0082         1  0.1901         1  0.0495 dbus-daemon
       72  0.0115         7 8.8e-04         0       0         2  0.0989 libxcb.so.1.1.0
       70  0.0111        56  0.0071         0       0         1  0.0495 librsvg-2.so.2.32.0
       64  0.0102         7 8.8e-04         1  0.1901         1  0.0495 compiz
       63  0.0100        54  0.0068         0       0         1  0.0495 dash
       54  0.0086        47  0.0059         0       0         1  0.0495 libpangocairo-1.0.so.0.2800.1
       50  0.0080        41  0.0052         0       0         1  0.0495 libgthread-2.0.so.0.2600.0
       34  0.0054        30  0.0038         0       0         0       0 libgdk_pixbuf-2.0.so.0.2200.0
       30  0.0048        29  0.0037         0       0         0       0 libxml2.so.2.7.7
       29  0.0046         3 3.8e-04         0       0         1  0.0495 libfade.so
       28  0.0045         7 8.8e-04         0       0         0       0 libgtksourceview-2.0.so.0.0.0
       26  0.0041        29  0.0037         0       0         0       0 gawk
       25  0.0040         8  0.0010         0       0         0       0 libm-2.12.1.so
       22  0.0035         1 1.3e-04         0       0         0       0 libpyglib-2.0-python2.6.so.0.0.0
       21  0.0033         8  0.0010         0       0         0       0 libvte.so.9.2600.0
       16  0.0025         6 7.6e-04         0       0         0       0 libXrender.so.1.3.0
       16  0.0025         4 5.0e-04         0       0         0       0 rsyslogd
       13  0.0021        14  0.0018         0       0         0       0 libmurrine.so
       13  0.0021         1 1.3e-04         0       0         0       0 _glib.so
       13  0.0021         5 6.3e-04         0       0         1  0.0495 libextmod.so
       12  0.0019         1 1.3e-04         0       0         0       0 libanimation.so
       12  0.0019         4 5.0e-04         0       0         0       0 libdecoration.so
       12  0.0019         3 3.8e-04         0       0         0       0 libdbus-glib-1.so.2.1.0
       12  0.0019         1 1.3e-04         0       0         0       0 libGL.so.1.2
       11  0.0018         3 3.8e-04         0       0         0       0 libexpo.so
       10  0.0016         0       0         0       0         0       0 librt-2.12.1.so
       10  0.0016         1 1.3e-04         0       0         0       0 libfb.so
        9  0.0014         1 1.3e-04         0       0         0       0 libXfixes.so.3.1.0
        9  0.0014         1 1.3e-04         0       0         0       0 evdev_drv.so
        8  0.0013         0       0         0       0         0       0 libdrm.so.2.4.0
        8  0.0013         2 2.5e-04         0       0         0       0 libgio-2.0.so.0.2600.0
        8  0.0013        15  0.0019         0       0         0       0 pango-basic-fc.so
        7  0.0011         1 1.3e-04         0       0         0       0 libresize.so
        7  0.0011         1 1.3e-04         0       0         0       0 libwall.so
        7  0.0011         1 1.3e-04         0       0         0       0 _gtk.so
        6 9.5e-04         1 1.3e-04         0       0         0       0 libstaticswitcher.so
        6 9.5e-04         0       0         0       0         0       0 libsvg.so
        5 8.0e-04         1 1.3e-04         0       0         0       0 gedit
        5 8.0e-04         0       0         0       0         0       0 libORBit-2.so.0.1.0
        5 8.0e-04         0       0         0       0         0       0 libXext.so.6.4.0
        5 8.0e-04         4 5.0e-04         0       0         0       0 libmetacity-private.so.0.0.0
        5 8.0e-04         0       0         0       0         0       0 libwnck-1.so.22.3.30
        4 6.4e-04         1 1.3e-04         0       0         0       0 sudo
        4 6.4e-04         0       0         0       0         0       0 libneg.so
        4 6.4e-04         1 1.3e-04         0       0         0       0 libscale.so
        4 6.4e-04         0       0         0       0         0       0 _gobject.so
        4 6.4e-04         0       0         0       0         0       0 libdri2.so
        3 4.8e-04         2 2.5e-04         0       0         0       0 grep
        3 4.8e-04         0       0         0       0         0       0 libudev.so.0.9.1
        3 4.8e-04         0       0         0       0         0       0 vmware-usbarbitrator
        3 4.8e-04         0       0         0       0         0       0 apache2
        3 4.8e-04         2 2.5e-04         0       0         0       0 libmove.so
        3 4.8e-04         0       0         0       0         0       0 libresizeinfo.so
        3 4.8e-04         1 1.3e-04         0       0         0       0 libgvfscommon.so.0.0.0
        3 4.8e-04         0       0         0       0         0       0 libstartup-notification-1.so.0.0.0
        3 4.8e-04         2 2.5e-04         0       0         0       0 NetworkManager
        2 3.2e-04         0       0         0       0         0       0 bash
        2 3.2e-04         1 1.3e-04         0       0         0       0 libdl-2.12.1.so
        2 3.2e-04         0       0         0       0         0       0 libresolv-2.12.1.so
        2 3.2e-04         0       0         0       0         0       0 gnome-panel
        2 3.2e-04         0       0         0       0         0       0 libccp.so
        2 3.2e-04         0       0         0       0         0       0 libezoom.so
        2 3.2e-04         0       0         0       0         0       0 libregex.so
        2 3.2e-04         0       0         0       0         0       0 libscaleaddon.so
        2 3.2e-04         0       0         0       0         0       0 libXdamage.so.1.1.0
        2 3.2e-04         0       0         0       0         0       0 libbonobo-2.so.0.0.0
        2 3.2e-04         0       0         0       0         0       0 libcompizconfig.so.0.0.0
        2 3.2e-04         3 3.8e-04         0       0         0       0 libmysqlclient.so.16.0.0
        2 3.2e-04         0       0         0       0         0       0 libnm-glib.so.2.4.1
        2 3.2e-04         0       0         0       0         0       0 libstdc++.so.6.0.14
        1 1.6e-04         0       0         0       0         0       0 cat
        1 1.6e-04         0       0         0       0         0       0 libgcc_s.so.1
        1 1.6e-04         0       0         0       0         0       0 libnss_dns-2.12.1.so
        1 1.6e-04         0       0         0       0         0       0 libnss_files-2.12.1.so
        1 1.6e-04         1 1.3e-04         0       0         0       0 libpng12.so.0.44.0
        1 1.6e-04         0       0         0       0         0       0 libz.so.1.2.3.4
        1 1.6e-04         0       0         0       0         0       0 wpa_supplicant
        1 1.6e-04         0       0         0       0         0       0 gtk-window-decorator
        1 1.6e-04         1 1.3e-04         0       0         0       0 nm-applet
        1 1.6e-04         0       0         0       0         0       0 libplace.so
        1 1.6e-04         0       0         0       0         0       0 libsnap.so
        1 1.6e-04         0       0         0       0         0       0 libtext.so
        1 1.6e-04         0       0         0       0         0       0 libworkarounds.so
        1 1.6e-04         0       0         0       0         0       0 libpixbufloader-svg.so
        1 1.6e-04         0       0         0       0         0       0 libfilebrowser.so
        1 1.6e-04         0       0         0       0         0       0 libspell.so
        1 1.6e-04         0       0         0       0         0       0 libkeyboard.so
        1 1.6e-04         0       0         0       0         0       0 libpixmap.so
        1 1.6e-04         0       0         1  0.1901         0       0 im-ibus.so
        1 1.6e-04         0       0         0       0         0       0 libXi.so.6.1.0
        1 1.6e-04         0       0         0       0         0       0 libbonoboui-2.so.0.0.0
        1 1.6e-04         0       0         0       0         0       0 libdecoration.so.0.0.0
        1 1.6e-04         0       0         0       0         0       0 libfontconfig.so.1.4.4
        1 1.6e-04         0       0         0       0         0       0 libgconf-2.so.4.1.5
        1 1.6e-04         0       0         0       0         0       0 libpulse-mainloop-glib.so.0.0.4
        1 1.6e-04         0       0         0       0         0       0 libssl3.so
        1 1.6e-04         0       0         0       0         0       0 smtp
        1 1.6e-04         0       0         0       0         0       0 DBI.so
        1 1.6e-04         0       0         0       0         0       0 imklog.so
        0       0         1 1.3e-04         0       0         0       0 libpam.so.0.82.2
        0       0         1 1.3e-04         0       0         0       0 mysql.so
 
CPU: Intel Westmere microarchitecture, speed 2.133e+06 MHz (estimated)
Counted CPU_CLK_UNHALTED events (Clock cycles when not halted) with a unit mask of 0x00 (No unit mask) count 200000
Counted INST_RETIRED events (number of instructions retired) with a unit mask of 0x00 (No unit mask) count 200000
Counted LLC_MISSES events (Last level cache demand requests from this core that missed the LLC) with a unit mask of 0x41 (No unit mask) count 200000
Counted LLC_REFS events (Last level cache demand requests from this core) with a unit mask of 0x4f (No unit mask) count 200000
samples  %        samples  %        samples  %        samples  %        symbol name
62524    10.2120  88119    11.2431  0              0  2         0.1042  foldArrayBy4(float**, PoTPlan*)
57512     9.3934  70993     9.0580  0              0  0              0  foldArrayBy5(float**, PoTPlan*)
52775     8.6197  115215   14.7003  0              0  0              0  foldArrayBy2A(float**, PoTPlan*)
45620     7.4511  87459    11.1589  0              0  6         0.3125  foldArrayBy3(float**, PoTPlan*)
35146     5.7404  13637     1.7399  0              0  0              0  f_GetChiSq(float*, int, int, float, float, float*, float*)
27067     4.4208  28430     3.6274  0              0  6         0.3125  GaussFit(float*, int, int)
21346     3.4864  18892     2.4104  0              0  0              0  lcgf(double, double)
18047     2.9476  7870      1.0041  103      20.4771  579      30.1562  GetFixedPoT(float*, int, int, float*, int, int)
17374     2.8377  28106     3.5861  0              0  1         0.0521  find_pulse(float const*, int, float, int, int)
16955     2.7693  34045     4.3438  0              0  0              0  foldArrayBy2AL(float**, PoTPlan*)
15305     2.4998  5716      0.7293  83       16.5010  416      21.6667  analyze_pot(float*, int, ChirpFftPair_t&)
13426     2.1929  774       0.0988  0              0  0              0  sincos
12812     2.0926  29612     3.7782  0              0  0              0  f_GetPeak(float*, int, int, float, float, float*)
12755     2.0833  31103     3.9684  0              0  0              0  f_GetTrueMean(float*, int, float, int, int)
11429     1.8667  12675     1.6172  0              0  3         0.1562  sse2_ChirpData_ak(float (*) [2], float (*) [2], int, double, int, double)
11045     1.8040  9255      1.1808  62       12.3260  203      10.5729  n1bv_128
8209      1.3408  292       0.0373  5         0.9940  3         0.1562  ChooseChirpData()
8130      1.3279  14769     1.8844  0              0  0              0  foldArrayBy2LO(float**, PoTPlan*)
7975      1.3026  5231      0.6674  0              0  0              0  __ieee754_log
7575      1.2372  4593      0.5860  0              0  0              0  strlen
7236      1.1819  4696      0.5992  0              0  0              0  float_to_uchar(float*, unsigned char*, long, float)
6784      1.1080  12619     1.6101  0              0  0              0  t_funct(int, int, int)
5486      0.8960  10130     1.2925  0              0  1         0.0521  FindSpikes(float*, int, int, SETI_WU_INFO&)
4951      0.8086  6788      0.8661  0              0  6         0.3125  fftwf_cpy2d_pair
4809      0.7855  5320      0.6788  0              0  0              0  __ieee754_pow
4578      0.7477  4647      0.5929  0              0  212      11.0417  n1fv_128
4176      0.6821  10114     1.2904  0              0  23        1.1979  find_triplets(float const*, int, float, int, int)
3393      0.5542  3        3.8e-04  0              0  0              0  _dl_sysinfo_int80
3338      0.5452  135       0.0172  0              0  0              0  v_vpfTranspose8x4ntw(int, int, float*, float*)
3198      0.5223  8876      1.1325  0              0  0              0  strchr
3182      0.5197  122       0.0156  0              0  0              0  v_vTranspose4ntw(int, int, float*, float*)
3130      0.5112  6091      0.7772  0              0  8         0.4167  malloc
3118      0.5093  3830      0.4887  1         0.1988  1         0.0521  floor
3026      0.4942  1103      0.1407  0              0  0              0  v_vChirpData_x86_64(float (*) [2], float (*) [2], int, double, int, double)
2762      0.4511  1893      0.2415  0              0  2         0.1042  floorf
2741      0.4477  2916      0.3721  0              0  3         0.1562  _int_malloc
2693      0.4398  3343      0.4265  0              0  16        0.8333  t2bv_64
2535      0.4140  2262      0.2886  0              0  2         0.1042  ReportPulseEvent(float, float, float, int, int, float, float, float*, int, int)
2452      0.4005  947       0.1208  0              0  0              0  isnan
2420      0.3953  5874      0.7495  0              0  2         0.1042  free
2388      0.3900  2155      0.2750  0              0  18        0.9375  fftwf_cpy2d
2248      0.3672  4032      0.5144  0              0  7         0.3646  t1bv_8
2199      0.3592  4177      0.5329  0              0  0              0  foldArrayBy5LO(float**, PoTPlan*)
2197      0.3588  4010      0.5116  1         0.1988  8         0.4167  v_GetPowerSpectrum(float (*) [2], float*, int)
2146      0.3505  35        0.0045  0              0  0              0  v_ChirpData(float (*) [2], float (*) [2], int, double, int, double)
2116      0.3456  3791      0.4837  0              0  7         0.3646  t1bv_16
2007      0.3278  367       0.0468  42        8.3499  53        2.7604  v_Transpose(int, int, float*, float*)
1889      0.3085  2248      0.2868  0              0  0              0  fftwf_twiddle_awake
1787      0.2919  3064      0.3909  0              0  0              0  foldArrayBy3LO(float**, PoTPlan*)
1708      0.2790  2052      0.2618  0              0  0              0  foldArrayBy4LO(float**, PoTPlan*)
1682      0.2747  118       0.0151  0              0  0              0  v_vTranspose4x8ntw(int, int, float*, float*)
1650      0.2695  405       0.0517  73       14.5129  80        4.1667  __memset_sse2_rep
1622      0.2649  2454      0.3131  0              0  0              0  fpu_ChirpData(float (*) [2], float (*) [2], int, double, int, double)
1503      0.2455  113       0.0144  0              0  0              0  v_vTranspose4x16ntw(int, int, float*, float*)
1488      0.2430  2175      0.2775  0              0  1         0.0521  pow
1411      0.2305  1555      0.1984  5         0.9940  10        0.5208  n2bv_64
1317      0.2151  407       0.0519  22        4.3738  29        1.5104  v_Transpose2(int, int, float*, float*)
1298      0.2120  485       0.0619  22        4.3738  30        1.5625  v_pfTranspose2(int, int, float*, float*)
1249      0.2040  1310      0.1671  0              0  0              0  sse3_ChirpData_ak(float (*) [2], float (*) [2], int, double, int, double)
1175      0.1919  130       0.0166  0              0  2         0.1042  log
1172      0.1914  702       0.0896  16        3.1809  19        0.9896  v_pfTranspose8(int, int, float*, float*)
1068      0.1744  1349      0.1721  0              0  0              0  _int_free
1052      0.1718  1969      0.2512  0              0  1         0.0521  sse1_ChirpData_ak(float (*) [2], float (*) [2], int, double, int, double)
983       0.1606  608       0.0776  20        3.9761  21        1.0938  v_Transpose8(int, int, float*, float*)
968       0.1581  739       0.0943  0              0  0              0  PulseProgressUnits(double, int)
955       0.1560  1045      0.1333  1         0.1988  1         0.0521  malloc_consolidate
896       0.1463  1633      0.2084  0              0  1         0.0521  time_to_ra_dec(double, double*, double*)
863       0.1410  1255      0.1601  0              0  0              0  fraction_done(double, double)
796       0.1300  1166      0.1488  0              0  0              0  random
721       0.1178  382       0.0487  10        1.9881  12        0.6250  v_pfTranspose4(int, int, float*, float*)
716       0.1169  1332      0.1700  0              0  6         0.3125  t1fv_16
714       0.1166  852       0.1087  0              0  6         0.3125  n1fv_64
692       0.1130  1199      0.1530  0              0  4         0.2083  t1bv_32
631       0.1031  322       0.0411  11        2.1869  14        0.7292  v_Transpose4(int, int, float*, float*)
600       0.0980  135       0.0172  12        2.3857  15        0.7812  v_vTranspose4np(int, int, float*, float*)
591       0.0965  921       0.1175  0              0  0              0  ChooseGaussEvent(int, float, float, float, float, int, float, float, float*)
563       0.0920  183       0.0233  11        2.1869  13        0.6771  v_vTranspose4(int, int, float*, float*)
546       0.0892  968       0.1235  0              0  3         0.1562  recur
544       0.0889  568       0.0725  0              0  0              0  q1fv_8
531       0.0867  884       0.1128  0              0  1         0.0521  t2_64
519       0.0848  442       0.0564  0              0  0              0  analysis_config::analysis_config()
516       0.0843  451       0.0575  0              0  0              0  q1fv_4
487       0.0795  571       0.0729  0              0  0              0  operator new(unsigned int)
475       0.0776  720       0.0919  0              0  2         0.1042  t2fv_32
466       0.0761  498       0.0635  0              0  0              0  n1fv_32
463       0.0756  755       0.0963  0              0  3         0.1562  t1_64
449       0.0733  767       0.0979  0              0  0              0  t2_32
427       0.0697  632       0.0806  0              0  4         0.2083  t2fv_8
411       0.0671  659       0.0841  0              0  3         0.1562  t1_32
372       0.0608  727       0.0928  0              0  1         0.0521  t1fv_4
348       0.0568  493       0.0629  1         0.1988  0              0  result::result()
341       0.0557  247       0.0315  0              0  0              0  v_BaseLineSmooth(float (*) [2], int, int, int)
340       0.0555  592       0.0755  0              0  0              0  t2_16
335       0.0547  473       0.0604  0              0  1         0.0521  workunit_grp::workunit_grp()
329       0.0537  324       0.0413  0              0  0              0  q1fv_2
312       0.0510  532       0.0679  0              0  0              0  t1_16
311       0.0508  591       0.0754  0              0  0              0  t2_8
306       0.0500  460       0.0587  0              0  0              0  t2bv_32
300       0.0490  283       0.0361  0              0  12        0.6250  n1fv_16
291       0.0475  405       0.0517  0              0  1         0.0521  __i686.get_pc_thunk.bx
291       0.0475  375       0.0478  0              0  0              0  cexp_zero
290       0.0474  265       0.0338  0              0  0              0  operator delete(void*)
289       0.0472  476       0.0607  0              0  0              0  n1_16
288       0.0470  2395      0.3056  0              0  0              0  boinc_fraction_done
279       0.0456  364       0.0464  0              0  0              0  cnvt_bin_hz(int, int)
279       0.0456  519       0.0662  0              0  1         0.0521  t1_8
275       0.0449  326       0.0416  0              0  7         0.3646  recur
259       0.0423  220       0.0281  0              0  0              0  seti_analyze(ANALYSIS_STATE&)
249       0.0407  438       0.0559  0              0  1         0.0521  ChooseTranspose()
246       0.0402  471       0.0601  0              0  0              0  t2_4
245       0.0400  92        0.0117  0              0  0              0  __ieee754_log10
244       0.0399  296       0.0378  0              0  1         0.0521  n2bv_32
242       0.0395  447       0.0570  1         0.1988  0              0  n1_8
233       0.0381  160       0.0204  0              0  0              0  checkpoint(unsigned char)
233       0.0381  16        0.0020  0              0  0              0  vec_recip1(float __vector)
226       0.0369  251       0.0320  0              0  1         0.0521  data_description_t::data_description_t()
226       0.0369  423       0.0540  0              0  0              0  finite
225       0.0367  378       0.0482  0              0  1         0.0521  workunit_header::workunit_header()
218       0.0356  306       0.0390  0              0  0              0  gaussian::gaussian()
218       0.0356  441       0.0563  0              0  0              0  t1_4
213       0.0348  301       0.0384  0              0  0              0  t1fuv_4
212       0.0346  494       0.0630  0              0  0              0  splitter_config::splitter_config()
211       0.0345  209       0.0267  0              0  0              0  calc_detection_freq(double, double, double)
205       0.0335  339       0.0433  0              0  0              0  t1fuv_2
202       0.0330  295       0.0376  0              0  0              0  t2bv_16
188       0.0307  206       0.0263  0              0  0              0  _int_memalign
188       0.0307  243       0.0310  0              0  1         0.0521  t1fuv_8
183       0.0299  248       0.0316  0              0  0              0  receiver_config::receiver_config()
172       0.0281  289       0.0369  0              0  0              0  t1_2
170       0.0278  231       0.0295  0              0  0              0  SpikeProgressUnits(int)
165       0.0269  9         0.0011  0              0  9         0.4688  memcpy
163       0.0266  246       0.0314  0              0  0              0  dobatch
162       0.0265  284       0.0362  0              0  1         0.0521  memalign
161       0.0263  149       0.0190  0              0  0              0  tape::tape()
157       0.0256  265       0.0338  0              0  0              0  t2fv_16
153       0.0250  255       0.0325  0              0  0              0  std::vector<unsigned char, std::allocator<unsigned char> >::_M_fill_insert(__gnu_cxx::__normal_iterator<unsigned char*, std::vector<unsigned char, std::allocator<unsigned char> > >, unsigned int, unsigned char const&)
151       0.0247  164       0.0209  0              0  0              0  TripletProgressUnits()
149       0.0243  269       0.0343  0              0  0              0  t1fv_8
147       0.0240  97        0.0124  0              0  0              0  T.9614
143       0.0234  94        0.0120  0              0  0              0  random_r
140       0.0229  224       0.0286  0              0  0              0  subband_description_t::subband_description_t()
134       0.0219  286       0.0365  0              0  0              0  fftwf_md5putc
134       0.0219  212       0.0270  0              0  3         0.1562  t1fv_32
132       0.0216  19        0.0024  0              0  0              0  time
128       0.0209  66        0.0084  0              0  0              0  bits_to_floats(unsigned char*, float (*) [2], int)
124       0.0203  194       0.0248  0              0  0              0  t2fv_64
122       0.0199  118       0.0151  0              0  0              0  GenChirpFftPairs(ChirpFftPair_t**, double*)
121       0.0198  190       0.0242  0              0  0              0  fftwf_cpy1d
121       0.0198  186       0.0237  0              0  0              0  n2bv_16
119       0.0194  178       0.0227  0              0  0              0  t3fv_32
111       0.0181  52        0.0066  0              0  0              0  T.9615
111       0.0181  155       0.0198  0              0  2         0.1042  t1fv_64
110       0.0180  139       0.0177  0              0  0              0  n1fv_8
105       0.0171  76        0.0097  0              0  1         0.0521  pulse::pulse()
104       0.0170  191       0.0244  0              0  0              0  n1_64
102       0.0167  76        0.0097  0              0  0              0  T.9610
95        0.0155  174       0.0222  0              0  0              0  t1bv_4
92        0.0150  41        0.0052  1         0.1988  0              0  GaussianProgressUnits()
89        0.0145  176       0.0225  0              0  0              0  fftwf_cpy2d_pair_ci
89        0.0145  131       0.0167  0              0  0              0  recorder_config::recorder_config()
89        0.0145  133       0.0170  0              0  0              0  t3fv_16
88        0.0144  157       0.0200  0              0  1         0.0521  __memmove_ssse3_rep
88        0.0144  86        0.0110  0              0  0              0  t1fv_2
86        0.0140  123       0.0157  0              0  0              0  spike::spike()
81        0.0132  154       0.0196  0              0  0              0  n2fv_64
79        0.0129  149       0.0190  0              0  0              0  q1_8
78        0.0127  117       0.0149  0              0  0              0  invoke_solver
74        0.0121  123       0.0157  0              0  0              0  GAUSS_INFO::~GAUSS_INFO()
73        0.0119  162       0.0207  0              0  0              0  t3fv_8
72        0.0118  57        0.0073  0              0  1         0.0521  apply
69        0.0113  121       0.0154  0              0  0              0  q1_4
68        0.0111  87        0.0111  0              0  0              0  MFILE::MFILE()
67        0.0109  134       0.0171  0              0  0              0  fftwf_cpy2d_pair_co
65        0.0106  120       0.0153  0              0  0              0  n1_32
62        0.0101  58        0.0074  0              0  0              0  apply
62        0.0101  81        0.0103  0              0  0              0  cexpl_sqrtn_table
60        0.0098  120       0.0153  0              0  0              0  t3fv_4
59        0.0096  57        0.0073  0              0  0              0  fftwf_tile2d
59        0.0096  79        0.0101  0              0  0              0  t2bv_8
58        0.0095  24        0.0031  0              0  0              0  apply_dit
56        0.0091  83        0.0106  0              0  0              0  search0
55        0.0090  104       0.0133  0              0  0              0  n2fv_32
54        0.0088  37        0.0047  0              0  0              0  apply
54        0.0088  34        0.0043  0              0  0              0  fftwf_measure_execution_time
54        0.0088  75        0.0096  0              0  0              0  t2bv_2
53        0.0087  48        0.0061  0              0  0              0  apply_buf
51        0.0083  131       0.0167  0              0  0              0  MFILE::~MFILE()
49        0.0080  33        0.0042  0              0  0              0  T.9619
48        0.0078  51        0.0065  0              0  1         0.0521  SPIKE_INFO::SPIKE_INFO()
48        0.0078  93        0.0119  0              0  0              0  q1_2
47        0.0077  2        2.6e-04  0              0  0              0  boinc_time_to_checkpoint
47        0.0077  0              0  0              0  0              0  hires_timer::find_frequency()
47        0.0077  70        0.0089  0              0  0              0  top_sum2(float**, PoTPlan*)
46        0.0075  20        0.0026  0              0  0              0  fftwf_execute_dft
45        0.0073  59        0.0075  0              0  0              0  t2fv_4
43        0.0070  0              0  0              0  0              0  rand
42        0.0069  35        0.0045  0              0  0              0  calloc_a(unsigned int, unsigned int, unsigned int)
41        0.0067  21        0.0027  0              0  0              0  GAUSS_INFO::GAUSS_INFO()
41        0.0067  25        0.0032  0              0  0              0  log10
39        0.0064  38        0.0048  0              0  0              0  ChooseFoldSubs(ChirpFftPair_t*, int, int)
39        0.0064  54        0.0069  0              0  0              0  invert_lcgf(float, float, float)
39        0.0064  62        0.0079  0              0  0              0  t2fv_2
37        0.0060  67        0.0085  0              0  0              0  fftwf_choose_radix
35        0.0057  62        0.0079  0              0  0              0  fftwf_transpose
35        0.0057  55        0.0070  0              0  0              0  mkplan
34        0.0056  87        0.0111  0              0  0              0  SPIKE_INFO::~SPIKE_INFO()
31        0.0051  21        0.0027  0              0  0              0  PULSE_INFO::PULSE_INFO()
31        0.0051  28        0.0036  0              0  0              0  fftwf_dft_solve
29        0.0047  27        0.0034  0              0  0              0  fftwf_ct_applicable
29        0.0047  36        0.0046  0              0  1         0.0521  mkplan
29        0.0047  46        0.0059  0              0  0              0  top_sum3(float**, PoTPlan*)
27        0.0044  44        0.0056  0              0  0              0  BYTWJ1
27        0.0044  40        0.0051  0              0  0              0  fftwf_md5putb
25        0.0041  26        0.0033  0              0  0              0  htab_lookup
25        0.0041  64        0.0082  0              0  0              0  sw_sum2_t31(float**, PoTPlan*)
24        0.0039  30        0.0038  0              0  0              0  PULSE_INFO::~PULSE_INFO()
23        0.0038  17        0.0022  0              0  0              0  fftwf_isqrt
23        0.0038  30        0.0038  0              0  0              0  fftwf_md5end
22        0.0036  25        0.0032  0              0  0              0  std::_Rb_tree_insert_and_rebalance(bool, std::_Rb_tree_node_base*, std::_Rb_tree_node_base*, std::_Rb_tree_node_base&)
22        0.0036  29        0.0037  0              0  0              0  sw_sum4_t31(float**, PoTPlan*)
22        0.0036  26        0.0033  0              0  0              0  top_sum5(float**, PoTPlan*)
21        0.0034  21        0.0027  0              0  0              0  cexp_generic
20        0.0033  23        0.0029  0              0  0              0  n1fv_2
19        0.0031  33        0.0042  0              0  0              0  dotile_buf
19        0.0031  0              0  0              0  0              0  fftwf_free
18        0.0029  19        0.0024  0              0  0              0  GetPulsePoTLen(long, int*, int*)
18        0.0029  41        0.0052  0              0  0              0  top_sum4(float**, PoTPlan*)
17        0.0028  17        0.0022  0              0  0              0  ChooseGetPowerSpectrum()
17        0.0028  22        0.0028  0              0  0              0  VZMULJ
17        0.0028  24        0.0031  0              0  0              0  fftwf_kernel_malloc
17        0.0028  33        0.0042  0              0  0              0  n2fv_16
17        0.0028  30        0.0038  0              0  0              0  sw_sum5_t31(float**, PoTPlan*)
16        0.0026  22        0.0028  0              0  0              0  dotile
16        0.0026  25        0.0032  0              0  0              0  fftwf_kernel_free
16        0.0026  10        0.0013  0              0  0              0  std::_Rb_tree_decrement(std::_Rb_tree_node_base const*)
15        0.0024  2        2.6e-04  0              0  0              0  fftwf_elapsed_since
15        0.0024  1        1.3e-04  0              0  0              0  gettimeofday
15        0.0024  22        0.0028  0              0  0              0  malloc_a(unsigned int, unsigned int)
15        0.0024  31        0.0040  0              0  0              0  n1_2
15        0.0024  26        0.0033  0              0  0              0  sw_sum3_t31(float**, PoTPlan*)
14        0.0023  19        0.0024  0              0  0              0  fftwf_cpy2d_ci
14        0.0023  15        0.0019  0              0  0              0  sse_pulPoTf2u(float**, PoTPlan*)
14        0.0023  24        0.0031  0              0  1         0.0521  v_vGetPowerSpectrum2(float (*) [2], float*, int)
13        0.0021  19        0.0024  0              0  0              0  fftwf_malloc
13        0.0021  0              0  0              0  0              0  free_a(void*)
13        0.0021  20        0.0026  0              0  0              0  n1fv_4
12        0.0020  9         0.0011  0              0  0              0  apply_buf
12        0.0020  11        0.0014  0              0  0              0  sse_pulPoTf2L4(float**, PoTPlan*)
12        0.0020  22        0.0028  0              0  0              0  sse_pulPoTf4u(float**, PoTPlan*)
12        0.0020  12        0.0015  0              0  0              0  std::_Rb_tree<long long, std::pair<long long const, ChirpFftPair_t>, std::_Select1st<std::pair<long long const, ChirpFftPair_t> >, std::less<long long>, std::allocator<std::pair<long long const, ChirpFftPair_t> > >::_M_insert_unique_(std::_Rb_tree_const_iterator<std::pair<long long const, ChirpFftPair_t> >, std::pair<long long const, ChirpFftPair_t> const&)
11        0.0018  11        0.0014  0              0  0              0  dotile
11        0.0018  14        0.0018  0              0  0              0  fftwf_cpy2d_co
11        0.0018  25        0.0032  0              0  0              0  n1_4
11        0.0018  11        0.0014  0              0  0              0  sse_pulPoTf5u(float**, PoTPlan*)
11        0.0018  32        0.0041  0              0  1         0.0521  v_vGetPowerSpectrum(float (*) [2], float*, int)
11        0.0018  23        0.0029  0              0  0              0  v_vGetPowerSpectrumUnrolled2(float (*) [2], float*, int)
10        0.0016  3        3.8e-04  0              0  0              0  apply_dif
10        0.0016  15        0.0019  0              0  0              0  dobatch
10        0.0016  10        0.0013  0              0  0              0  fftwf_mkstride
10        0.0016  8         0.0010  0              0  0              0  mkplan
9         0.0015  18        0.0023  0              0  0              0  planFoldTest(PoTPlan*, float*, int (*) [5])
9         0.0015  3        3.8e-04  0              0  0              0  std::_Rb_tree<long long, std::pair<long long const, ChirpFftPair_t>, std::_Select1st<std::pair<long long const, ChirpFftPair_t> >, std::less<long long>, std::allocator<std::pair<long long const, ChirpFftPair_t> > >::_M_insert_(std::_Rb_tree_node_base const*, std::_Rb_tree_node_base const*, std::pair<long long const, ChirpFftPair_t> const&)
8         0.0013  9         0.0011  0              0  0              0  GetProgressUnitSize(int, int)
8         0.0013  16        0.0020  0              0  0              0  sse_pulPoTf3u(float**, PoTPlan*)
8         0.0013  16        0.0020  0              0  0              0  sse_pulPoTf4L8(float**, PoTPlan*)
8         0.0013  5        6.4e-04  0              0  0              0  std::_Rb_tree_increment(std::_Rb_tree_node_base const*)
8         0.0013  26        0.0033  0              0  0              0  v_vGetPowerSpectrumUnrolled(float (*) [2], float*, int)
7         0.0011  0              0  0              0  0              0  __nanosleep_nocancel
7         0.0011  7        8.9e-04  0              0  0              0  copy
7         0.0011  19        0.0024  0              0  0              0  sse_pulPoTf2(float**, PoTPlan*)
7         0.0011  5        6.4e-04  0              0  1         0.0521  std::_Rb_tree<long long, std::pair<long long const, ChirpFftPair_t>, std::_Select1st<std::pair<long long const, ChirpFftPair_t> >, std::less<long long>, std::allocator<std::pair<long long const, ChirpFftPair_t> > >::_M_erase(std::_Rb_tree_node<std::pair<long long const, ChirpFftPair_t> >*)
7         0.0011  20        0.0026  0              0  0              0  std::vector<unsigned char, std::allocator<unsigned char> > x_setiathome_decode<unsigned char>(char const*, unsigned int)
6        9.8e-04  7        8.9e-04  0              0  0              0  apply_extra_iter
6        9.8e-04  13        0.0017  0              0  0              0  htab_insert
6        9.8e-04  5        6.4e-04  0              0  0              0  msort_with_tmp
6        9.8e-04  13        0.0017  0              0  0              0  sse_pulPoTf2L8(float**, PoTPlan*)
6        9.8e-04  10        0.0013  0              0  0              0  sse_pulPoTf3L8(float**, PoTPlan*)
5        8.2e-04  2        2.6e-04  0              0  0              0  apply
5        8.2e-04  0              0  0              0  0              0  boinc_sleep(double)
5        8.2e-04  2        2.6e-04  0              0  0              0  fftwf_md5int
5        8.2e-04  2        2.6e-04  0              0  0              0  hires_timer::ticks()
5        8.2e-04  10        0.0013  0              0  0              0  sse_pulPoTf5L4(float**, PoTPlan*)
4        6.5e-04  4        5.1e-04  0              0  0              0  apply
4        6.5e-04  2        2.6e-04  0              0  0              0  apply_iter
4        6.5e-04  2        2.6e-04  0              0  0              0  fftwf_iabs
4        6.5e-04  3        3.8e-04  0              0  0              0  fftwf_md5puts
4        6.5e-04  0              0  0              0  0              0  fftwf_mktensor
4        6.5e-04  6        7.7e-04  0              0  0              0  fftwf_rdft_solve
4        6.5e-04  12        0.0015  0              0  0              0  fftwf_tensor_compress
4        6.5e-04  4        5.1e-04  0              0  0              0  fill_slot
4        6.5e-04  12        0.0015  0              0  0              0  hinsert0
4        6.5e-04  5        6.4e-04  0              0  0              0  mkcldw
4        6.5e-04  2        2.6e-04  0              0  0              0  mkplan
4        6.5e-04  0              0  0              0  0              0  mkplan
4        6.5e-04  8         0.0010  0              0  0              0  sse_pulPoTf3(float**, PoTPlan*)
4        6.5e-04  7        8.9e-04  0              0  0              0  sse_pulPoTf5L8(float**, PoTPlan*)
4        6.5e-04  3        3.8e-04  0              0  0              0  transpose_rec
3        4.9e-04  2        2.6e-04  0              0  0              0  ComputePoTInfo(int, int)
3        4.9e-04  4        5.1e-04  0              0  0              0  __i686.get_pc_thunk.cx
3        4.9e-04  2        2.6e-04  0              0  0              0  apply_before
3        4.9e-04  0              0  0              0  0              0  dtime()
3        4.9e-04  6        7.7e-04  0              0  0              0  fftwf_compute_tilesz
3        4.9e-04  1        1.3e-04  0              0  0              0  fftwf_ifree
3        4.9e-04  2        2.6e-04  0              0  0              0  fftwf_malloc_plain
3        4.9e-04  1        1.3e-04  0              0  0              0  fftwf_ops_zero
3        4.9e-04  4        5.1e-04  0              0  0              0  fftwf_plan_awake
3        4.9e-04  1        1.3e-04  0              0  0              0  fftwf_taint
3        4.9e-04  6        7.7e-04  0              0  0              0  fftwf_tensor_compress_contiguous
3        4.9e-04  5        6.4e-04  0              0  0              0  fftwf_tensor_copy_inplace
3        4.9e-04  5        6.4e-04  0              0  0              0  fftwf_tensor_md5
3        4.9e-04  5        6.4e-04  0              0  0              0  mkplan
3        4.9e-04  4        5.1e-04  0              0  0              0  sse_pulPoTf2AL4(float**, PoTPlan*)
2        3.3e-04  2        2.6e-04  0              0  0              0  applicable
2        3.3e-04  1        1.3e-04  0              0  0              0  apply_cpy2dco
2        3.3e-04  0              0  0              0  0              0  apply_tiledbuf
2        3.3e-04  0              0  0              0  0              0  awake
2        3.3e-04  0              0  0              0  0              0  destroy
2        3.3e-04  1        1.3e-04  0              0  0              0  fftwf_cpy2d_tiled
2        3.3e-04  1        1.3e-04  0              0  0              0  fftwf_dimcmp
2        3.3e-04  1        1.3e-04  0              0  0              0  fftwf_have_sse
2        3.3e-04  2        2.6e-04  0              0  0              0  fftwf_md5INT
2        3.3e-04  0              0  0              0  0              0  fftwf_mkproblem_dft
2        3.3e-04  1        1.3e-04  0              0  0              0  fftwf_null_awake
2        3.3e-04  1        1.3e-04  0              0  0              0  fftwf_pickdim
2        3.3e-04  1        1.3e-04  0              0  0              0  fftwf_plan_destroy_internal
2        3.3e-04  4        5.1e-04  0              0  0              0  fftwf_tensor_copy
2        3.3e-04  1        1.3e-04  0              0  0              0  fftwf_tensor_inplace_locations
2        3.3e-04  1        1.3e-04  0              0  0              0  mkplan
2        3.3e-04  0              0  0              0  0              0  mkplan
2        3.3e-04  0              0  0              0  0              0  mkplan
2        3.3e-04  0              0  0              0  0              0  mkplan
2        3.3e-04  4        5.1e-04  0              0  0              0  n2fv_8
2        3.3e-04  1        1.3e-04  0              0  0              0  okp
2        3.3e-04  0              0  0              0  0              0  okp
2        3.3e-04  3        3.8e-04  0              0  0              0  okp_t1f
2        3.3e-04  3        3.8e-04  0              0  0              0  sse_pulPoTf2ALu(float**, PoTPlan*)
2        3.3e-04  6        7.7e-04  0              0  0              0  sse_pulPoTf4(float**, PoTPlan*)
2        3.3e-04  1        1.3e-04  0              0  0              0  sse_pulPoTf5(float**, PoTPlan*)
2        3.3e-04  1        1.3e-04  0              0  0              0  timer_handler()
1        1.6e-04  0              0  0              0  0              0  __dynamic_cast
1        1.6e-04  0              0  0              0  0              0  __strstr_sse42
1        1.6e-04  0              0  0              0  0              0  applicable_tiled
1        1.6e-04  1        1.3e-04  0              0  0              0  apply
1        1.6e-04  1        1.3e-04  0              0  0              0  apply_after
1        1.6e-04  0              0  0              0  0              0  awake
1        1.6e-04  0              0  0              0  0              0  awake
1        1.6e-04  0              0  0              0  0              0  destroy
1        1.6e-04  0              0  0              0  0              0  fftwf_alignment_of
1        1.6e-04  0              0  0              0  0              0  fftwf_codelet_t2bv_32
1        1.6e-04  0              0  0              0  0              0  fftwf_cpy2d_tiledbuf
1        1.6e-04  0              0  0              0  0              0  fftwf_ct_uglyp
1        1.6e-04  1        1.3e-04  0              0  0              0  fftwf_dft_zerotens
1        1.6e-04  0              0  0              0  0              0  fftwf_get_crude_time
1        1.6e-04  3        3.8e-04  0              0  0              0  fftwf_hc2hc_applicable
1        1.6e-04  1        1.3e-04  0              0  0              0  fftwf_md5begin
1        1.6e-04  1        1.3e-04  0              0  0              0  fftwf_mkplan
1        1.6e-04  1        1.3e-04  0              0  0              0  fftwf_mkplan_dft
1        1.6e-04  0              0  0              0  0              0  fftwf_mkproblem_rdft
1        1.6e-04  0              0  0              0  0              0  fftwf_mktriggen
1        1.6e-04  1        1.3e-04  0              0  0              0  fftwf_ops_madd
1        1.6e-04  6        7.7e-04  0              0  0              0  fftwf_tensor_append
1        1.6e-04  0              0  0              0  0              0  fftwf_tensor_min_ostride
1        1.6e-04  0              0  0              0  0              0  fftwf_triggen_destroy
1        1.6e-04  0              0  0              0  0              0  memcpy_loop
1        1.6e-04  0              0  0              0  0              0  mkplan
1        1.6e-04  0              0  0              0  0              0  mkplan
1        1.6e-04  0              0  0              0  0              0  mkplan
1        1.6e-04  3        3.8e-04  0              0  0              0  mkplan
1        1.6e-04  0              0  0              0  0              0  mkplan
1        1.6e-04  0              0  0              0  0              0  mkplan
1        1.6e-04  0              0  0              0  0              0  okp_commonu
1        1.6e-04  0              0  0              0  0              0  okp_t2f
1        1.6e-04  0              0  0              0  0              0  plan_PulsePoT(PoTPlan*, int, float*, int*)
1        1.6e-04  0              0  0              0  0              0  putulong
1        1.6e-04  0              0  0              0  0              0  real_cexp
1        1.6e-04  1        1.3e-04  0              0  0              0  sse_pulPoTf2AL8(float**, PoTPlan*)
1        1.6e-04  1        1.3e-04  0              0  0              0  std::num_get<char, std::istreambuf_iterator<char, std::char_traits<char> > >::_M_extract_float(std::istreambuf_iterator<char, std::char_traits<char> >, std::istreambuf_iterator<char, std::char_traits<char> >, std::ios_base&, std::_Ios_Iostate&, std::string&) const
1        1.6e-04  0              0  0              0  0              0  timeout_p
1        1.6e-04  1        1.3e-04  0              0  0              0  usleep
1        1.6e-04  0              0  0              0  0              0  worker_signal_handler(int)
0              0  1        1.3e-04  0              0  0              0  bool std::has_facet<std::num_get<char, std::istreambuf_iterator<char, std::char_traits<char> > > >(std::locale const&)
0              0  1        1.3e-04  0              0  0              0  destroy
0              0  4        5.1e-04  0              0  0              0  dotile_buf
0              0  2        2.6e-04  0              0  0              0  evaluate_plan
0              0  1        1.3e-04  0              0  0              0  fftwf_hash
0              0  1        1.3e-04  0              0  0              0  fftwf_ifree0
0              0  1        1.3e-04  0              0  0              0  fftwf_imin
0              0  1        1.3e-04  0              0  0              0  fftwf_mkplan_f_d
0              0  1        1.3e-04  0              0  0              0  fftwf_mkproblem
0              0  1        1.3e-04  0              0  0              0  fftwf_mkproblem_dft_d
0              0  1        1.3e-04  0              0  0              0  fftwf_mktensor_2d
0              0  1        1.3e-04  0              0  0              0  fftwf_problem_destroy
0              0  1        1.3e-04  0              0  0              0  fftwf_tensor_destroy
0              0  2        2.6e-04  0              0  0              0  fftwf_tensor_inplace_strides2
0              0  3        3.8e-04  0              0  0              0  fftwf_tensor_sz
0              0  2        2.6e-04  0              0  0              0  fftwf_tensor_tornk1
0              0  1        1.3e-04  0              0  0              0  getchr_str
0              0  5        6.4e-04  0              0  0              0  hash
0              0  2        2.6e-04  0              0  0              0  hgrow
0              0  1        1.3e-04  0              0  0              0  imprt
0              0  1        1.3e-04  0              0  0              0  mkcldw
0              0  1        1.3e-04  0              0  0              0  mkplan
0              0  1        1.3e-04  0              0  0              0  mkplan
0              0  1        1.3e-04  0              0  0              0  mkplan
0              0  1        1.3e-04  0              0  0              0  okp
0              0  2        2.6e-04  0              0  0              0  qsort_r
0              0  2        2.6e-04  0              0  0              0  register_solver
0              0  2        2.6e-04  0              0  0              0  sse_pulPoTf2AL(float**, PoTPlan*)
0              0  1        1.3e-04  0              0  0              0  std::istreambuf_iterator<char, std::char_traits<char> > std::num_get<char, std::istreambuf_iterator<char, std::char_traits<char> > >::_M_extract_int<long>(std::istreambuf_iterator<char, std::char_traits<char> >, std::istreambuf_iterator<char, std::char_traits<char> >, std::ios_base&, std::_Ios_Iostate&, long&) const
0              0  1        1.3e-04  0              0  0              0  std::locale::id::_M_id() const
0              0  1        1.3e-04  0              0  0              0  transpose
0              0  2        2.6e-04  0              0  0              0  vprint
0              0  2        2.6e-04  0              0  0              0  zero
Mon Oct  3 00:33:59 CDT 2011
CPU: Intel Westmere microarchitecture, speed 2.133e+06 MHz (estimated)
Counted DTLB_LOAD_MISSES events (DTLB load misses) with a unit mask of 0x01 (any DTLB load misses) count 200000
Counted DTLB_MISSES events (DTLB misses) with a unit mask of 0x01 (any DTLB misses) count 200000
Counted ITLB_MISSES events (ITLB miss) with a unit mask of 0x01 (any ITLB miss) count 200000
Counted ITLB_MISS_RETIRED events (Retired instructions that missed the ITLB (Precise Event)) with a unit mask of 0x20 (No unit mask) count 200000
DTLB_LOAD_MISS...|DTLB_MISSES:20...|ITLB_MISSES:20...|ITLB_MISS_RETI...|
  samples|      %|  samples|      %|  samples|      %|  samples|      %|
------------------------------------------------------------------------
     2722 98.3026      2733 98.1329         1  3.4483         3  5.2632 seti_boinc
        8  0.2889         7  0.2513         4 13.7931         5  8.7719 libcairo.so.2.11000.0
        6  0.2167         4  0.1436         2  6.8966         1  1.7544 libdrm_intel.so.1.0.0
        5  0.1806         2  0.0718         1  3.4483         3  5.2632 libgobject-2.0.so.0.2600.0
        4  0.1445         6  0.2154         4 13.7931         4  7.0175 libglib-2.0.so.0.2600.0
        4  0.1445         4  0.1436         4 13.7931         5  8.7719 Xorg
        4  0.1445         1  0.0359         2  6.8966         4  7.0175 libgtk-x11-2.0.so.0.2200.0
        3  0.1083        11  0.3950         2  6.8966         4  7.0175 libc-2.12.1.so
        3  0.1083         2  0.0718         0       0         2  3.5088 python2.6
        2  0.0722         0       0         0       0         3  5.2632 libgdk-x11-2.0.so.0.2200.0
        2  0.0722         0       0         2  6.8966         3  5.2632 libpangoft2-1.0.so.0.2800.1
        1  0.0361         1  0.0359         0       0         3  5.2632 libpthread-2.12.1.so
        1  0.0361         0       0         0       0         0       0 no-vmlinux
        1  0.0361         0       0         0       0         0       0 gedit
        1  0.0361         1  0.0359         2  6.8966         1  1.7544 libX11.so.6.3.0
        1  0.0361         0       0         0       0         0       0 libXrender.so.1.3.0
        1  0.0361         2  0.0718         1  3.4483         1  1.7544 libpango-1.0.so.0.2800.1
        0       0         0       0         0       0         2  3.5088 libdbus-1.so.3.5.2
        0       0         0       0         0       0         1  1.7544 libm-2.12.1.so
        0       0         0       0         1  3.4483         0       0 librt-2.12.1.so
        0       0         0       0         1  3.4483         0       0 compiz
        0       0         2  0.0718         0       0         0       0 libfade.so
        0       0         1  0.0359         0       0         0       0 i965_dri.so
        0       0         0       0         0       0         1  1.7544 libpangocairo-1.0.so.0.2800.1
        0       0         2  0.0718         1  3.4483         2  3.5088 libpixman-1.so.0.18.4
        0       0         0       0         0       0         3  5.2632 libxcb.so.1.1.0
        0       0         6  0.2154         1  3.4483         3  5.2632 intel_drv.so
        0       0         0       0         0       0         2  3.5088 libextmod.so
        0       0         0       0         0       0         1  1.7544 evdev_drv.so
 
CPU: Intel Westmere microarchitecture, speed 2.133e+06 MHz (estimated)
Counted DTLB_LOAD_MISSES events (DTLB load misses) with a unit mask of 0x01 (any DTLB load misses) count 200000
Counted DTLB_MISSES events (DTLB misses) with a unit mask of 0x01 (any DTLB misses) count 200000
Counted ITLB_MISSES events (ITLB miss) with a unit mask of 0x01 (any ITLB miss) count 200000
Counted ITLB_MISS_RETIRED events (Retired instructions that missed the ITLB (Precise Event)) with a unit mask of 0x20 (No unit mask) count 200000
samples  %        samples  %        samples  %        samples  %        symbol name
1819     66.8259  1810     66.2276  0              0  0              0  GetFixedPoT(float*, int, int, float*, int, int)
878      32.2557  887      32.4552  0              0  0              0  analyze_pot(float*, int, ChirpFftPair_t&)
6         0.2204  6         0.2195  0              0  0              0  GaussFit(float*, int, int)
3         0.1102  13        0.4757  0              0  0              0  _int_malloc
3         0.1102  4         0.1464  0              0  0              0  malloc
3         0.1102  2         0.0732  0              0  0              0  sse2_ChirpData_ak(float (*) [2], float (*) [2], int, double, int, double)
2         0.0735  0              0  0              0  0              0  floor
2         0.0735  3         0.1098  0              0  0              0  n1bv_128
2         0.0735  2         0.0732  0              0  0              0  pow
1         0.0367  2         0.0732  1        100.000  0              0  GaussianProgressUnits()
1         0.0367  0              0  0              0  0              0  fraction_done(double, double)
1         0.0367  0              0  0              0  0              0  malloc_consolidate
1         0.0367  0              0  0              0  0              0  time_to_ra_dec(double, double*, double*)
0              0  0              0  0              0  1        33.3333  ChooseGaussEvent(int, float, float, float, float, int, float, float, float*)
0              0  1         0.0366  0              0  0              0  boinc_fraction_done
0              0  0              0  0              0  1        33.3333  checkpoint(unsigned char)
0              0  1         0.0366  0              0  0              0  f_GetChiSq(float*, int, int, float, float, float*, float*)
0              0  1         0.0366  0              0  0              0  n2bv_64
0              0  0              0  0              0  1        33.3333  operator delete(void*)
0              0  1         0.0366  0              0  0              0  v_GetPowerSpectrum(float (*) [2], float*, int)
Mon Oct  3 00:35:04 CDT 2011
CPU: Intel Westmere microarchitecture, speed 2.133e+06 MHz (estimated)
Counted BR_INST_RETIRED events (number of branch instructions retired) with a unit mask of 0x00 (No unit mask) count 10000
Counted BR_MISS_PRED_RETIRED events (number of mispredicted branches retired (precise)) with a unit mask of 0x00 (No unit mask) count 10000
Counted RESOURCE_STALLS events (Resource related stall cycles) with a unit mask of 0x01 (any Resource related stall cycles) count 2000000
Counted UOPS_EXECUTED events (Cycles Uops executed on any port (core count)) with a unit mask of 0x3f (core_active_cycles Cycles Uops executed on any port (core count)) count 2000000
BR_INST_RETIRE...|BR_MISS_PRED_R...|RESOURCE_STALL...|UOPS_EXECUTED:...|
  samples|      %|  samples|      %|  samples|      %|  samples|      %|
------------------------------------------------------------------------
  1525270 96.7213     13566 89.0099     32515 98.7697     43452 97.2712 seti_boinc
     9692  0.6146       107  0.7021        60  0.1823       143  0.3201 oprofiled
     7366  0.4671       493  3.2347        39  0.1185       192  0.4298 libcairo.so.2.11000.0
     6889  0.4368        98  0.6430        40  0.1215       160  0.3582 libpixman-1.so.0.18.4
     5248  0.3328       234  1.5353        67  0.2035       116  0.2597 libc-2.12.1.so
     4577  0.2902        46  0.3018        24  0.0729        78  0.1746 libdrm_intel.so.1.0.0
     2842  0.1802        66  0.4330        11  0.0334        60  0.1343 libgobject-2.0.so.0.2600.0
     2775  0.1760       119  0.7808        32  0.0972        87  0.1948 libglib-2.0.so.0.2600.0
     1781  0.1129        96  0.6299        19  0.0577        64  0.1433 Xorg
     1593  0.1010        22  0.1443        10  0.0304        21  0.0470 libpthread-2.12.1.so
     1361  0.0863        42  0.2756        15  0.0456        40  0.0895 libgtk-x11-2.0.so.0.2200.0
      963  0.0611        32  0.2100         2  0.0061        12  0.0269 libpango-1.0.so.0.2800.1
      939  0.0595        10  0.0656         7  0.0213        19  0.0425 libpangoft2-1.0.so.0.2800.1
      926  0.0587        38  0.2493         7  0.0213        24  0.0537 ld-2.12.1.so
      874  0.0554        25  0.1640        12  0.0365        21  0.0470 intel_drv.so
      469  0.0297        28  0.1837         6  0.0182        18  0.0403 libgdk-x11-2.0.so.0.2200.0
      438  0.0278        57  0.3740        12  0.0365        38  0.0851 python2.6
      425  0.0270         5  0.0328         1  0.0030         3  0.0067 ophelp
      273  0.0173        13  0.0853         2  0.0061         4  0.0090 dash
      268  0.0170         5  0.0328         2  0.0061         7  0.0157 dbus-daemon
      243  0.0154        10  0.0656         4  0.0122         5  0.0112 libdbus-1.so.3.5.2
      240  0.0152         0       0         6  0.0182         5  0.0112 mysqld
      130  0.0082         3  0.0197         0       0         4  0.0090 gawk
      119  0.0075         7  0.0459         5  0.0152        13  0.0291 libmurrine.so
      107  0.0068         2  0.0131         0       0        17  0.0381 no-vmlinux
       99  0.0063        16  0.1050         1  0.0030         7  0.0157 i965_dri.so
       95  0.0060         3  0.0197         0       0         3  0.0067 libgthread-2.0.so.0.2600.0
       94  0.0060        21  0.1378         2  0.0061        12  0.0269 libX11.so.6.3.0
       89  0.0056        16  0.1050         1  0.0030         5  0.0112 perl
       88  0.0056         1  0.0066         0       0         7  0.0157 libm-2.12.1.so
       87  0.0055         4  0.0262         3  0.0091         3  0.0067 libpangocairo-1.0.so.0.2800.1
       60  0.0038         0       0         0       0         1  0.0022 pango-basic-fc.so
       58  0.0037         6  0.0394         0       0         1  0.0022 libXrender.so.1.3.0
       54  0.0034         8  0.0525         0       0         2  0.0045 libxcb.so.1.1.0
       44  0.0028         0       0         0       0         0       0 libextmod.so
       39  0.0025         6  0.0394         5  0.0152         1  0.0022 libhunspell-1.2.so.0.0.0
       33  0.0021         3  0.0197         4  0.0122         2  0.0045 compiz
       30  0.0019         4  0.0262         0       0         1  0.0022 libfb.so
       28  0.0018         1  0.0066         0       0         0       0 libxml2.so.2.7.7
       25  0.0016         2  0.0131         0       0         0       0 librsvg-2.so.2.32.0
       20  0.0013         1  0.0066         0       0         3  0.0067 rsyslogd
       19  0.0012         0       0         0       0         1  0.0022 libvte.so.9.2600.0
       18  0.0011         1  0.0066         0       0         1  0.0022 gvfsd-metadata
       16  0.0010         2  0.0131         0       0         1  0.0022 libgtksourceview-2.0.so.0.0.0
       13 8.2e-04         1  0.0066         0       0         0       0 libpam.so.0.82.2
       11 7.0e-04         0       0         0       0         0       0 _glib.so
       10 6.3e-04         0       0         1  0.0030         2  0.0045 libdecoration.so
       10 6.3e-04         1  0.0066         0       0         1  0.0022 libdbus-glib-1.so.2.1.0
       10 6.3e-04         0       0         0       0         2  0.0045 libpyglib-2.0-python2.6.so.0.0.0
        8 5.1e-04         2  0.0131         0       0         0       0 evdev_drv.so
        7 4.4e-04         0       0         0       0         2  0.0045 libgio-2.0.so.0.2600.0
        7 4.4e-04         1  0.0066         0       0         0       0 libmysqlclient.so.16.0.0
        7 4.4e-04         0       0         0       0         1  0.0022 libGL.so.1.2
        6 3.8e-04         0       0         3  0.0091         2  0.0045 libfade.so
        5 3.2e-04         0       0         0       0         0       0 grep
        5 3.2e-04         2  0.0131         0       0         0       0 gedit
        5 3.2e-04         1  0.0066         0       0         1  0.0022 libanimation.so
        5 3.2e-04         0       0         0       0         1  0.0022 libresize.so
        5 3.2e-04         1  0.0066         0       0         1  0.0022 libXfixes.so.3.1.0
        4 2.5e-04         0       0         0       0         0       0 libORBit-2.so.0.1.0
        4 2.5e-04         0       0         0       0         0       0 libdri2.so
        3 1.9e-04         0       0         0       0         0       0 librt-2.12.1.so
        3 1.9e-04         1  0.0066         0       0         0       0 sudo
        3 1.9e-04         0       0         0       0         0       0 libnm-util.so.1.6.0
        3 1.9e-04         0       0         0       0         0       0 NetworkManager
        2 1.3e-04         0       0         0       0         0       0 bash
        2 1.3e-04         0       0         0       0         0       0 ls
        2 1.3e-04         0       0         0       0         0       0 wpa_supplicant
        2 1.3e-04         0       0         0       0         0       0 gnome-session
        2 1.3e-04         1  0.0066         0       0         0       0 libexpo.so
        2 1.3e-04         0       0         0       0         0       0 libmove.so
        2 1.3e-04         0       0         0       0         0       0 libstaticswitcher.so
        2 1.3e-04         0       0         0       0         0       0 libXext.so.6.4.0
        2 1.3e-04         0       0         0       0         0       0 libgvfscommon.so.0.0.0
        1 6.3e-05         0       0         0       0         0       0 sleep
        1 6.3e-05         0       0         0       0         0       0 libnss_files-2.12.1.so
        1 6.3e-05         1  0.0066         0       0         0       0 libpopt.so.0.0.0
        1 6.3e-05         0       0         0       0         0       0 pam_limits.so
        1 6.3e-05         0       0         0       0         0       0 dirname
        1 6.3e-05         1  0.0066         0       0         0       0 libezoom.so
        1 6.3e-05         0       0         0       0         1  0.0022 libscale.so
        1 6.3e-05         1  0.0066         0       0         0       0 libwall.so
        1 6.3e-05         1  0.0066         0       0         0       0 libworkarounds.so
        1 6.3e-05         0       0         0       0         0       0 libXi.so.6.1.0
        1 6.3e-05         0       0         0       0         0       0 libgconf-2.so.4.1.5
        1 6.3e-05         0       0         0       0         0       0 libgdk_pixbuf-2.0.so.0.2200.0
        1 6.3e-05         0       0         0       0         0       0 libstartup-notification-1.so.0.0.0
        1 6.3e-05         0       0         0       0         0       0 libtalloc.so.2.0.1
        1 6.3e-05         0       0         0       0         0       0 libxklavier.so.16.0.0
        1 6.3e-05         0       0         0       0         1  0.0022 DBI.so
        1 6.3e-05         1  0.0066         0       0         0       0 _gobject.so
        1 6.3e-05         0       0         0       0         0       0 imklog.so
        0       0         1  0.0066         0       0         0       0 mkdir
        0       0         1  0.0066         0       0         0       0 libdl-2.12.1.so
        0       0         1  0.0066         0       0         0       0 libdrm.so.2.4.0
        0       0         1  0.0066         0       0         0       0 libplace.so
        0       0         0       0         0       0         1  0.0022 libresizeinfo.so
        0       0         0       0         0       0         1  0.0022 libscaleaddon.so
        0       0         1  0.0066         0       0         0       0 libvpswitch.so
        0       0         1  0.0066         1  0.0030         0       0 libXdamage.so.1.1.0
        0       0         0       0         1  0.0030         0       0 gconfd-2
 
CPU: Intel Westmere microarchitecture, speed 2.133e+06 MHz (estimated)
Counted BR_INST_RETIRED events (number of branch instructions retired) with a unit mask of 0x00 (No unit mask) count 10000
Counted BR_MISS_PRED_RETIRED events (number of mispredicted branches retired (precise)) with a unit mask of 0x00 (No unit mask) count 10000
Counted RESOURCE_STALLS events (Resource related stall cycles) with a unit mask of 0x01 (any Resource related stall cycles) count 2000000
Counted UOPS_EXECUTED events (Cycles Uops executed on any port (core count)) with a unit mask of 0x3f (core_active_cycles Cycles Uops executed on any port (core count)) count 2000000
samples  %        samples  %        samples  %        samples  %        symbol name
249772   16.3775  2992     22.0551  1235      3.7985  3160      7.2724  f_GetTrueMean(float*, int, float, int, int)
158948   10.4222  3053     22.5048  3372     10.3712  5591     12.8671  GaussFit(float*, int, int)
158138   10.3691  99        0.7298  201       0.6182  1044      2.4027  FindSpikes(float*, int, int, SETI_WU_INFO&)
120248    7.8846  315       2.3220  125       0.3845  659       1.5166  find_triplets(float const*, int, float, int, int)
113023    7.4109  16        0.1179  798       2.4544  3157      7.2655  f_GetPeak(float*, int, int, float, float, float*)
56800     3.7244  25        0.1843  3854     11.8537  3394      7.8109  GetFixedPoT(float*, int, int, float*, int, int)
52638     3.4515  1500     11.0571  3597     11.0633  2938      6.7615  lcgf(double, double)
48481     3.1789  1         0.0074  86        0.2645  310       0.7134  free
47301     3.1015  0              0  28        0.0861  645       1.4844  __ieee754_pow
45282     2.9691  23        0.1695  7619     23.4337  2347      5.4014  f_GetChiSq(float*, int, int, float, float, float*, float*)
39766     2.6074  186       1.3711  2340      7.1971  2746      6.3196  analyze_pot(float*, int, ChirpFftPair_t&)
38312     2.5121  1735     12.7893  195       0.5998  882       2.0298  find_pulse(float const*, int, float, int, int)
34288     2.2483  30        0.2211  129       0.3968  476       1.0955  malloc
34186     2.2416  0              0  226       0.6951  1190      2.7387  __ieee754_log
29520     1.9356  6         0.0442  1431      4.4013  1218      2.8031  float_to_uchar(float*, unsigned char*, long, float)
29105     1.9084  6         0.0442  15        0.0461  162       0.3728  fraction_done(double, double)
28593     1.8748  691       5.0936  123       0.3783  728       1.6754  foldArrayBy2LO(float**, PoTPlan*)
22244     1.4585  259       1.9092  144       0.4429  421       0.9689  foldArrayBy3LO(float**, PoTPlan*)
22106     1.4495  0              0  5         0.0154  247       0.5684  pow
16085     1.0547  273       2.0124  150       0.4614  440       1.0126  foldArrayBy4LO(float**, PoTPlan*)
15471     1.0144  1         0.0074  64        0.1968  229       0.5270  PulseProgressUnits(double, int)
12952     0.8493  0              0  1         0.0031  46        0.1059  boinc_fraction_done
11850     0.7770  0              0  8         0.0246  533       1.2266  isnan
11028     0.7231  265       1.9534  114       0.3506  293       0.6743  _int_malloc
10980     0.7200  3         0.0221  55        0.1692  162       0.3728  _int_free
10812     0.7089  541       3.9879  77        0.2368  291       0.6697  foldArrayBy3(float**, PoTPlan*)
10063     0.6598  244       1.7986  148       0.4552  337       0.7756  foldArrayBy4(float**, PoTPlan*)
10053     0.6592  247       1.8207  10        0.0308  103       0.2370  time_to_ra_dec(double, double*, double*)
9939      0.6517  0              0  177       0.5444  509       1.1714  v_GetPowerSpectrum(float (*) [2], float*, int)
7291      0.4781  97        0.7150  70        0.2153  150       0.3452  ChooseGaussEvent(int, float, float, float, float, int, float, float, float*)
5893      0.3864  0              0  1840      5.6593  1980      4.5568  sse2_ChirpData_ak(float (*) [2], float (*) [2], int, double, int, double)
5879      0.3855  194       1.4300  17        0.0523  125       0.2877  foldArrayBy2A(float**, PoTPlan*)
5293      0.3471  183       1.3490  240       0.7382  525       1.2082  foldArrayBy5LO(float**, PoTPlan*)
4455      0.2921  119       0.8772  82        0.2522  186       0.4281  foldArrayBy5(float**, PoTPlan*)
4192      0.2749  125       0.9214  32        0.0984  66        0.1519  malloc_consolidate
3091      0.2027  0              0  16        0.0492  67        0.1542  operator new(unsigned int)
2646      0.1735  1         0.0074  25        0.0769  59        0.1358  workunit_grp::workunit_grp()
2614      0.1714  94        0.6929  18        0.0554  55        0.1266  foldArrayBy2AL(float**, PoTPlan*)
2518      0.1651  18        0.1327  4         0.0123  52        0.1197  checkpoint(unsigned char)
2501      0.1640  33        0.2433  61        0.1876  89        0.2048  floor
1983      0.1300  6         0.0442  0              0  16        0.0368  GAUSS_INFO::~GAUSS_INFO()
1980      0.1298  1         0.0074  17        0.0523  28        0.0644  receiver_config::receiver_config()
1967      0.1290  1         0.0074  9         0.0277  33        0.0759  std::vector<unsigned char, std::allocator<unsigned char> >::_M_fill_insert(__gnu_cxx::__normal_iterator<unsigned char*, std::vector<unsigned char, std::allocator<unsigned char> > >, unsigned int, unsigned char const&)
1924      0.1262  0              0  4         0.0123  13        0.0299  MFILE::~MFILE()
1587      0.1041  8         0.0590  1         0.0031  40        0.0921  TripletProgressUnits()
1558      0.1022  2         0.0147  31        0.0953  46        0.1059  result::result()
1457      0.0955  0              0  24        0.0738  18        0.0414  splitter_config::splitter_config()
1411      0.0925  1         0.0074  200       0.6151  571       1.3141  t1bv_8
1359      0.0891  1         0.0074  6         0.0185  21        0.0483  __memset_sse2_rep
1278      0.0838  0              0  8         0.0246  15        0.0345  __memmove_ssse3_rep
1164      0.0763  0              0  4         0.0123  8         0.0184  recorder_config::recorder_config()
1148      0.0753  6         0.0442  50        0.1538  35        0.0805  gaussian::gaussian()
1139      0.0747  3         0.0221  28        0.0861  42        0.0967  workunit_header::workunit_header()
1093      0.0717  1         0.0074  23        0.0707  51        0.1174  cnvt_bin_hz(int, int)
1078      0.0707  0              0  9         0.0277  20        0.0460  __i686.get_pc_thunk.bx
1026      0.0673  0              0  0              0  13        0.0299  MFILE::MFILE()
939       0.0616  0              0  3         0.0092  41        0.0944  operator delete(void*)
802       0.0526  14        0.1032  14        0.0431  17        0.0391  calc_detection_freq(double, double, double)
752       0.0493  2         0.0147  23        0.0707  63        0.1450  analysis_config::analysis_config()
705       0.0462  0              0  15        0.0461  38        0.0875  data_description_t::data_description_t()
584       0.0383  12        0.0885  242       0.7443  490       1.1277  t1bv_16
552       0.0362  95        0.7003  5         0.0154  18        0.0414  GaussianProgressUnits()
547       0.0359  0              0  16        0.0492  17        0.0391  subband_description_t::subband_description_t()
486       0.0319  0              0  8         0.0246  24        0.0552  tape::tape()
283       0.0186  2         0.0147  60        0.1845  193       0.4442  log
267       0.0175  0              0  6         0.0185  7         0.0161  T.9610
223       0.0146  3         0.0221  8         0.0246  26        0.0598  T.9614
162       0.0106  1         0.0074  2098      6.4528  2620      6.0296  n1bv_128
120       0.0079  0              0  426       1.3102  607       1.3969  t2bv_64
119       0.0078  0              0  1         0.0031  38        0.0875  finite
95        0.0062  0              0  0              0  1         0.0023  SpikeProgressUnits(int)
90        0.0059  1         0.0074  3         0.0092  8         0.0184  seti_analyze(ANALYSIS_STATE&)
84        0.0055  5         0.0369  5         0.0154  5         0.0115  GAUSS_INFO::GAUSS_INFO()
79        0.0052  0              0  233       0.7166  323       0.7433  n2bv_64
62        0.0041  2         0.0147  92        0.2830  126       0.2900  t1bv_32
61        0.0040  0              0  1         0.0031  3         0.0069  apply
52        0.0034  3         0.0221  0              0  2         0.0046  ReportPulseEvent(float, float, float, int, int, float, float, float*, int, int)
52        0.0034  0              0  7         0.0215  2         0.0046  apply
48        0.0031  0              0  0              0  0              0  SPIKE_INFO::~SPIKE_INFO()
47        0.0031  2         0.0147  24        0.0738  40        0.0921  t2bv_16
42        0.0028  0              0  0              0  0              0  memalign
40        0.0026  1         0.0074  1         0.0031  2         0.0046  apply_dit
36        0.0024  2         0.0147  0              0  1         0.0023  spike::spike()
35        0.0023  0              0  49        0.1507  86        0.1979  t2bv_32
33        0.0022  2         0.0147  0              0  9         0.0207  boinc_time_to_checkpoint
30        0.0020  0              0  1         0.0031  3         0.0069  __ieee754_log10
21        0.0014  0              0  15        0.0461  21        0.0483  n2bv_32
20        0.0013  0              0  0              0  0              0  _int_memalign
15       9.8e-04  0              0  1         0.0031  2         0.0046  apply
15       9.8e-04  0              0  4         0.0123  6         0.0138  t2bv_8
10       6.6e-04  0              0  0              0  0              0  invert_lcgf(float, float, float)
9        5.9e-04  0              0  0              0  0              0  floorf
9        5.9e-04  3         0.0221  0              0  0              0  log10
8        5.2e-04  3         0.0221  0              0  1         0.0023  fftwf_execute_dft
8        5.2e-04  0              0  0              0  0              0  fftwf_kernel_malloc
7        4.6e-04  0              0  0              0  0              0  PULSE_INFO::~PULSE_INFO()
6        3.9e-04  0              0  5         0.0154  16        0.0368  T.9615
5        3.3e-04  3         0.0221  0              0  0              0  SPIKE_INFO::SPIKE_INFO()
4        2.6e-04  0              0  0              0  0              0  plan_PulsePoT(PoTPlan*, int, float*, int*)
3        2.0e-04  0              0  0              0  1         0.0023  PULSE_INFO::PULSE_INFO()
3        2.0e-04  0              0  0              0  0              0  calloc_a(unsigned int, unsigned int, unsigned int)
3        2.0e-04  0              0  0              0  0              0  pulse::pulse()
2        1.3e-04  0              0  0              0  0              0  fftwf_kernel_free
2        1.3e-04  0              0  0              0  0              0  malloc_a(unsigned int, unsigned int)
1        6.6e-05  0              0  0              0  0              0  dtime()
1        6.6e-05  0              0  0              0  0              0  fftwf_malloc
1        6.6e-05  0              0  0              0  0              0  std::string::assign(std::string const&)
1        6.6e-05  0              0  0              0  0              0  t_funct(int, int, int)
1        6.6e-05  0              0  0              0  0              0  timer_handler()
1        6.6e-05  0              0  0              0  0              0  usleep
0              0  1         0.0074  1         0.0031  12        0.0276  T.9619
0              0  1         0.0074  0              0  0              0  ___printf_fp
0              0  1         0.0074  0              0  0              0  __libc_enable_asynccancel
0              0  0              0  0              0  1         0.0023  __mpn_mul_1
0              0  1         0.0074  0              0  0              0  __restore
0              0  1         0.0074  0              0  0              0  nanosleep
```

## Oprofile SETI script ##

```
#!/bin/bash
SleepSeconds=60 

./seti_boinc --standalone &
sleep 10
# Running Timer Mode
sudo rm -r /var/lib/oprofile/
sudo rm -r /root/.oprofile/daemonrc
sudo opcontrol --init
sudo opcontrol --no-vmlinux
sudo opcontrol --reset
sudo opcontrol --event=CPU_CLK_UNHALTED:200000:0x0:0:1 --event=INST_RETIRED:200000:0x0:0:1 --event=LLC_MISSES:200000:0x41:0:1 --event=LLC_REFS:200000:0x4f:0:1
sudo opcontrol --start
sudo opcontrol --status
echo "profiling for $SleepSeconds seconds"
sleep $SleepSeconds
sudo opcontrol --dump
date >> Nehalem.txt
sudo opreport >> Nehalem.txt
echo " " >> Nehalem.txt
sudo opreport -l /home/jeff/stuff/seti_boinc/client/seti_boinc >> Nehalem.txt
sudo opcontrol --shutdown

# 1)DTLB - any miss 2) 
sudo rm -r /var/lib/oprofile/
sudo rm -r /root/.oprofile/daemonrc
sudo opcontrol --init
sudo opcontrol --no-vmlinux
sudo opcontrol --reset
sudo opcontrol --event=DTLB_LOAD_MISSES:200000:0x1:0:1 --event=DTLB_MISSES:200000:0x1:0:1 --event=ITLB_MISSES:200000:0x1:0:1 --event=ITLB_MISS_RETIRED:200000:0x20:0:1
sudo opcontrol --start
sudo opcontrol --status
echo "profiling for $SleepSeconds seconds"
sleep $SleepSeconds
sudo opcontrol --dump
date >> Nehalem.txt
sudo opreport >> Nehalem.txt
echo " " >> Nehalem.txt
sudo opreport -l /home/jeff/stuff/seti_boinc/client/seti_boinc >> Nehalem.txt
sudo opcontrol --shutdown

# 1)DTLB - any miss 2) 
sudo rm -r /var/lib/oprofile/
sudo rm -r /root/.oprofile/daemonrc
sudo opcontrol --init
sudo opcontrol --no-vmlinux
sudo opcontrol --reset
sudo opcontrol --event=BR_INST_RETIRED:10000:0x0:0:1 --event=BR_MISS_PRED_RETIRED:10000:0x0:0:1 --event=RESOURCE_STALLS:2000000:0x1:0:1 --event=UOPS_EXECUTED:2000000:0x3f:0:1
sudo opcontrol --start
sudo opcontrol --status
echo "profiling for $SleepSeconds seconds"
sleep $SleepSeconds
sudo opcontrol --dump
date >> Nehalem.txt
sudo opreport >> Nehalem.txt
echo " " >> Nehalem.txt
sudo opreport -l /home/jeff/stuff/seti_boinc/client/seti_boinc >> Nehalem.txt
sudo opcontrol --shutdown
```