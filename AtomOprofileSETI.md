# Profiling SETI on Atom #

```
Mon Oct  3 01:43:49 CDT 2011
CPU: Intel Atom, speed 1795.54 MHz (estimated)
Counted CPU_CLK_UNHALTED events (Clock cycles when not halted) with a unit mask of 0x00 (core_p Core cycles when core is not halted) count 200000
Counted INST_RETIRED events (number of instructions retired) with a unit mask of 0x01 (No unit mask) count 200000
CPU_CLK_UNHALT...|INST_RETIRED:2...|
  samples|      %|  samples|      %|
------------------------------------
  2533910 99.1760    924637 99.1310 seti_boinc
	CPU_CLK_UNHALT...|INST_RETIRED:2...|
	  samples|      %|  samples|      %|
	------------------------------------
	  2533841 99.9973    924635 99.9998 seti_boinc
	       69  0.0027         2 2.2e-04 [vdso] (tgid:7512 range:0x531000-0x532000)
     6473  0.2533      5095  0.5462 oprofiled
	CPU_CLK_UNHALT...|INST_RETIRED:2...|
	  samples|      %|  samples|      %|
	------------------------------------
	     6469 99.9382      5095 100.000 oprofiled
	        4  0.0618         0       0 [vdso] (tgid:7893 range:0xe74000-0xe75000)
     4050  0.1585       377  0.0404 nvidia_drv.so
     3321  0.1300       290  0.0311 no-vmlinux
     1838  0.0719       816  0.0875 libc-2.12.1.so
     1725  0.0675       112  0.0120 Xorg
	CPU_CLK_UNHALT...|INST_RETIRED:2...|
	  samples|      %|  samples|      %|
	------------------------------------
	     1369 79.3623        47 41.9643 [vdso] (tgid:1248 range:0xb56000-0xb57000)
	      356 20.6377        65 58.0357 Xorg
      682  0.0267       459  0.0492 libcairo.so.2.11000.0
      510  0.0200       251  0.0269 bash
	CPU_CLK_UNHALT...|INST_RETIRED:2...|
	  samples|      %|  samples|      %|
	------------------------------------
	      507 99.4118       251 100.000 bash
	        3  0.5882         0       0 [vdso] (tgid:7992 range:0xaac000-0xaad000)
      453  0.0177       185  0.0198 ld-2.12.1.so
      421  0.0165       103  0.0110 libglib-2.0.so.0.2600.1
      219  0.0086        54  0.0058 libpthread-2.12.1.so
      202  0.0079        84  0.0090 dbus-daemon
      181  0.0071        41  0.0044 libdbus-1.so.3.5.2
      173  0.0068        45  0.0048 libgobject-2.0.so.0.2600.1
       92  0.0036        43  0.0046 libGL.so.260.19.06
       82  0.0032        19  0.0020 libX11.so.6.3.0
       61  0.0024        14  0.0015 libnvidia-glcore.so.260.19.06
       56  0.0022        17  0.0018 gnome-screensaver
	CPU_CLK_UNHALT...|INST_RETIRED:2...|
	  samples|      %|  samples|      %|
	------------------------------------
	       51 91.0714        17 100.000 gnome-screensaver
	        5  8.9286         0       0 [vdso] (tgid:1596 range:0x825000-0x826000)
       55  0.0022        10  0.0011 libgtk-x11-2.0.so.0.2200.0
       47  0.0018         3 3.2e-04 libgdk-x11-2.0.so.0.2200.0
       47  0.0018         9 9.6e-04 libxcb.so.1.1.0
       40  0.0016        16  0.0017 libORBit-2.so.0.1.0
       37  0.0014        23  0.0025 ophelp
       31  0.0012         1 1.1e-04 compiz
	CPU_CLK_UNHALT...|INST_RETIRED:2...|
	  samples|      %|  samples|      %|
	------------------------------------
	       30 96.7742         1 100.000 compiz
	        1  3.2258         0       0 [vdso] (tgid:1521 range:0xc40000-0xc41000)
       24 9.4e-04         0       0 libdbus-glib-1.so.2.1.0
       18 7.0e-04         5 5.4e-04 libgconf-2.so.4.1.5
       15 5.9e-04         0       0 NetworkManager
       13 5.1e-04         3 3.2e-04 mawk
       12 4.7e-04         1 1.1e-04 libgthread-2.0.so.0.2600.1
       11 4.3e-04         1 1.1e-04 libgio-2.0.so.0.2600.1
       11 4.3e-04         3 3.2e-04 irqbalance
        9 3.5e-04         6 6.4e-04 libpangoft2-1.0.so.0.2800.2
        7 2.7e-04         2 2.1e-04 libm-2.12.1.so
        6 2.3e-04         1 1.1e-04 librt-2.12.1.so
        6 2.3e-04         0       0 libusbmuxd.so.1.0.4
        5 2.0e-04         1 1.1e-04 dash
        5 2.0e-04         0       0 libgvfscommon.so.0.0.0
        5 2.0e-04         0       0 libpixman-1.so.0.18.4
        4 1.6e-04         0       0 libdl-2.12.1.so
        4 1.6e-04         0       0 libanimation.so
        4 1.6e-04         0       0 libXext.so.6.4.0
        4 1.6e-04         0       0 gconfd-2
	CPU_CLK_UNHALT...|INST_RETIRED:2...|
	  samples|      %|  samples|      %|
	------------------------------------
	        3 75.0000         0       0 [vdso] (tgid:1496 range:0xb85000-0xb86000)
	        1 25.0000         0       0 gconfd-2
        4 1.6e-04         2 2.1e-04 libpango-1.0.so.0.2800.2
        4 1.6e-04         0       0 evdev_drv.so
        3 1.2e-04         2 2.1e-04 grep
        3 1.2e-04         0       0 libccp.so
        3 1.2e-04         0       0 libresize.so
        3 1.2e-04         0       0 libscale.so
        3 1.2e-04         0       0 libavahi-common.so.3.5.2
        3 1.2e-04         1 1.1e-04 libnm-util.so.1.6.0
        3 1.2e-04         0       0 libpulse-mainloop-glib.so.0.0.4
        3 1.2e-04         0       0 libnvidia-tls.so.260.19.06
        3 1.2e-04         1 1.1e-04 libglx.so.260.19.06
        3 1.2e-04         1 1.1e-04 libextmod.so
        2 7.8e-05         1 1.1e-04 libpam.so.0.82.2
        2 7.8e-05         1 1.1e-04 ssh-agent
        2 7.8e-05         0       0 sudo
        2 7.8e-05         0       0 libdecoration.so
        2 7.8e-05         0       0 libezoom.so
        2 7.8e-05         0       0 libvpswitch.so
        2 7.8e-05         0       0 clock-applet
	CPU_CLK_UNHALT...|INST_RETIRED:2...|
	  samples|      %|  samples|      %|
	------------------------------------
	        1 50.0000         0       0 clock-applet
	        1 50.0000         0       0 [vdso] (tgid:1681 range:0x7ed000-0x7ee000)
        2 7.8e-05         0       0 liba11y-keyboard.so
        2 7.8e-05         0       0 libXcursor.so.1.0.2
        2 7.8e-05         0       0 libXi.so.6.1.0
        2 7.8e-05         0       0 libXxf86vm.so.1.0.0
        2 7.8e-05         1 1.1e-04 libgconfbackend-xml.so
        2 7.8e-05         0       0 libnm-glib.so.2.4.1
        2 7.8e-05         0       0 libxklavier.so.16.0.0
        2 7.8e-05         0       0 libwfb.so
        1 3.9e-05         1 1.1e-04 ls
        1 3.9e-05         0       0 libnss_files-2.12.1.so
        1 3.9e-05         1 1.1e-04 libudev.so.0.9.1
        1 3.9e-05         0       0 pam_unix.so
        1 3.9e-05         0       0 gnome-panel
	CPU_CLK_UNHALT...|INST_RETIRED:2...|
	  samples|      %|  samples|      %|
	------------------------------------
	        1 100.000         0       0 [vdso] (tgid:1528 range:0x1a2000-0x1a3000)
        1 3.9e-05         0       0 gtk-window-decorator
	CPU_CLK_UNHALT...|INST_RETIRED:2...|
	  samples|      %|  samples|      %|
	------------------------------------
	        1 100.000         0       0 [vdso] (tgid:1612 range:0x419000-0x41a000)
        1 3.9e-05         0       0 nm-applet
	CPU_CLK_UNHALT...|INST_RETIRED:2...|
	  samples|      %|  samples|      %|
	------------------------------------
	        1 100.000         0       0 [vdso] (tgid:1525 range:0xd93000-0xd94000)
        1 3.9e-05         0       0 libexpo.so
        1 3.9e-05         0       0 libmove.so
        1 3.9e-05         0       0 libplace.so
        1 3.9e-05         0       0 libresizeinfo.so
        1 3.9e-05         0       0 libscaleaddon.so
        1 3.9e-05         0       0 libsnap.so
        1 3.9e-05         0       0 libstaticswitcher.so
        1 3.9e-05         0       0 libwall.so
        1 3.9e-05         0       0 libworkarounds.so
        1 3.9e-05         0       0 libgconf.so
        1 3.9e-05         1 1.1e-04 libmurrine.so
        1 3.9e-05         0       0 gvfs-afc-volume-monitor
	CPU_CLK_UNHALT...|INST_RETIRED:2...|
	  samples|      %|  samples|      %|
	------------------------------------
	        1 100.000         0       0 [vdso] (tgid:1593 range:0x635000-0x636000)
        1 3.9e-05         1 1.1e-04 libavahi-core.so.7.0.0
        1 3.9e-05         0       0 libcompizconfig.so.0.0.0
        1 3.9e-05         0       0 libgmodule-2.0.so.0.2600.1
        1 3.9e-05         0       0 libpangocairo-1.0.so.0.2800.2
        1 3.9e-05         0       0 libstartup-notification-1.so.0.0.0
        1 3.9e-05         0       0 udisks-daemon
        1 3.9e-05         0       0 rsyslogd
        1 3.9e-05         0       0 sshd
        0       0         1 1.1e-04 libnss_compat-2.12.1.so
        0       0         1 1.1e-04 libselinux.so.1
 
CPU: Intel Atom, speed 1795.54 MHz (estimated)
Counted CPU_CLK_UNHALTED events (Clock cycles when not halted) with a unit mask of 0x00 (core_p Core cycles when core is not halted) count 200000
Counted INST_RETIRED events (number of instructions retired) with a unit mask of 0x01 (No unit mask) count 200000
samples  %        samples  %        image name               symbol name
226796    8.9508  11339     1.2264  seti_boinc               GetFixedPoT(float*, int, int, float*, int, int)
206100    8.1340  21493     2.3246  seti_boinc               f_GetChiSq(float*, int, int, float, float, float*, float*)
162388    6.4089  27496     2.9739  seti_boinc               lcgf(double, double)
154657    6.1038  10218     1.1052  seti_boinc               analyze_pot(float*, int, ChirpFftPair_t&)
148399    5.8568  34955     3.7806  seti_boinc               GaussFit(float*, int, int)
131266    5.1806  54239     5.8664  seti_boinc               sse2_ChirpData_ak(float (*) [2], float (*) [2], int, double, int, double)
90007     3.5523  51424     5.5619  seti_boinc               sse_pulPoTf2u(float**, PoTPlan*)
86743     3.4234  45309     4.9005  seti_boinc               FindSpikes(float*, int, int, SETI_WU_INFO&)
81018     3.1975  45594     4.9313  seti_boinc               n1bv_128
80468     3.1758  42044     4.5474  seti_boinc               sse_pulPoTf3u(float**, PoTPlan*)
76124     3.0043  43050     4.6562  seti_boinc               f_GetTrueMean(float*, int, float, int, int)
76070     3.0022  40796     4.4124  seti_boinc               sse_pulPoTf4u(float**, PoTPlan*)
71353     2.8161  37994     4.1093  seti_boinc               sse_pulPoTf5u(float**, PoTPlan*)
67143     2.6499  35863     3.8789  seti_boinc               q1bv_8
60961     2.4059  57034     6.1687  seti_boinc               f_GetPeak(float*, int, int, float, float, float*)
59652     2.3543  24033     2.5994  seti_boinc               t1bv_8
54584     2.1542  27831     3.0101  seti_boinc               fftwf_cpy2d
53150     2.0976  7444      0.8051  seti_boinc               float_to_uchar(float*, unsigned char*, long, float)
43128     1.7021  21650     2.3416  seti_boinc               find_pulse(float const*, int, float, int, int)
40743     1.6080  27123     2.9336  seti_boinc               t1bv_4
36119     1.4255  3608      0.3902  seti_boinc               __ieee754_log
34469     1.3604  22799     2.4659  seti_boinc               t3bv_4
28070     1.1078  12250     1.3249  seti_boinc               find_triplets(float const*, int, float, int, int)
27039     1.0671  17922     1.9384  seti_boinc               v_GetPowerSpectrum(float (*) [2], float*, int)
24388     0.9625  11904     1.2875  seti_boinc               sse_pulPoTf2ALu(float**, PoTPlan*)
22625     0.8929  7211      0.7799  seti_boinc               n1bv_64
19699     0.7774  12358     1.3366  seti_boinc               __i686.get_pc_thunk.bx
15959     0.6298  11291     1.2212  seti_boinc               t1bv_16
14147     0.5583  6812      0.7368  seti_boinc               __ieee754_pow
13148     0.5189  413       0.0447  seti_boinc               sincos
12155     0.4797  7394      0.7997  seti_boinc               t_funct(int, int, int)
10646     0.4202  306       0.0331  seti_boinc               ChooseChirpData()
10594     0.4181  7739      0.8370  seti_boinc               pow
10440     0.4120  3769      0.4076  seti_boinc               isnan
10221     0.4034  4214      0.4558  seti_boinc               log
9271      0.3659  6229      0.6737  seti_boinc               sse_pulPoTf2(float**, PoTPlan*)
7909      0.3121  5374      0.5812  seti_boinc               _int_malloc
7105      0.2804  3749      0.4055  seti_boinc               sse_pulPoTf2L8(float**, PoTPlan*)
6880      0.2715  6211      0.6718  seti_boinc               fftwf_cpy2d_pair
6553      0.2586  3174      0.3433  seti_boinc               sse_pulPoTf2L4(float**, PoTPlan*)
6460      0.2550  2231      0.2413  seti_boinc               n1fv_64
6429      0.2537  4422      0.4783  seti_boinc               sse_pulPoTf4L8(float**, PoTPlan*)
6315      0.2492  2481      0.2683  seti_boinc               n2bv_64
6271      0.2475  2442      0.2641  seti_boinc               v_vChirpData_x86_64(float (*) [2], float (*) [2], int, double, int, double)
6192      0.2444  2731      0.2954  seti_boinc               n1fv_128
6134      0.2421  4458      0.4822  seti_boinc               sse_pulPoTf3(float**, PoTPlan*)
5862      0.2314  2474      0.2676  seti_boinc               sse_pulPoTf3L8(float**, PoTPlan*)
5780      0.2281  1536      0.1661  seti_boinc               ChooseGaussEvent(int, float, float, float, float, int, float, float, float*)
5756      0.2272  1431      0.1548  seti_boinc               fraction_done(double, double)
5720      0.2257  3291      0.3559  seti_boinc               t1bv_2
5369      0.2119  368       0.0398  seti_boinc               v_Transpose(int, int, float*, float*)
5077      0.2004  3716      0.4019  seti_boinc               _int_free
4886      0.1928  822       0.0889  seti_boinc               floorf
4651      0.1836  1847      0.1998  seti_boinc               time_to_ra_dec(double, double*, double*)
4547      0.1795  3155      0.3412  seti_boinc               malloc
4462      0.1761  421       0.0455  seti_boinc               PulseProgressUnits(double, int)
4096      0.1617  1712      0.1852  seti_boinc               t2bv_64
3928      0.1550  1879      0.2032  seti_boinc               sse_pulPoTf2AL4(float**, PoTPlan*)
3611      0.1425  1310      0.1417  seti_boinc               sse3_ChirpData_ak(float (*) [2], float (*) [2], int, double, int, double)
3581      0.1413  1132      0.1224  seti_boinc               ReportPulseEvent(float, float, float, int, int, float, float, float*, int, int)
3459      0.1365  1622      0.1754  seti_boinc               sse1_ChirpData_ak(float (*) [2], float (*) [2], int, double, int, double)
3237      0.1278  2613      0.2826  seti_boinc               sse_pulPoTf5L4(float**, PoTPlan*)
3234      0.1276  737       0.0797  seti_boinc               __memset_sse2
3181      0.1255  2334      0.2524  seti_boinc               free
3014      0.1190  1994      0.2157  seti_boinc               t1fv_16
2915      0.1150  2166      0.2343  seti_boinc               sse_pulPoTf5(float**, PoTPlan*)
2798      0.1104  407       0.0440  seti_boinc               v_Transpose2(int, int, float*, float*)
2702      0.1066  1765      0.1909  seti_boinc               fftwf_twiddle_awake
2657      0.1049  2131      0.2305  seti_boinc               sse_pulPoTf4(float**, PoTPlan*)
2536      0.1001  608       0.0658  seti_boinc               v_Transpose8(int, int, float*, float*)
2282      0.0901  1505      0.1628  seti_boinc               sse_pulPoTf5L8(float**, PoTPlan*)
2148      0.0848  876       0.0947  seti_boinc               t2_64
2108      0.0832  1340      0.1449  seti_boinc               sse_pulPoTf2AL(float**, PoTPlan*)
2032      0.0802  134       0.0145  seti_boinc               v_vpfTranspose8x4ntw(int, int, float*, float*)
1978      0.0781  657       0.0711  seti_boinc               n1fv_32
1951      0.0770  1421      0.1537  seti_boinc               q1fv_4
1889      0.0746  749       0.0810  seti_boinc               t2_32
1888      0.0745  485       0.0525  seti_boinc               v_pfTranspose2(int, int, float*, float*)
1838      0.0725  121       0.0131  seti_boinc               v_vTranspose4ntw(int, int, float*, float*)
1793      0.0708  112       0.0121  seti_boinc               v_vTranspose4x16ntw(int, int, float*, float*)
1781      0.0703  743       0.0804  seti_boinc               t1_64
1721      0.0679  550       0.0595  seti_boinc               analysis_config::analysis_config()
1715      0.0677  300       0.0324  seti_boinc               cnvt_bin_hz(int, int)
1582      0.0624  702       0.0759  seti_boinc               v_pfTranspose8(int, int, float*, float*)
1551      0.0612  880       0.0952  seti_boinc               q1fv_8
1543      0.0609  118       0.0128  seti_boinc               v_vTranspose4x8ntw(int, int, float*, float*)
1539      0.0607  321       0.0347  seti_boinc               v_Transpose4(int, int, float*, float*)
1535      0.0606  917       0.0992  seti_boinc               TripletProgressUnits()
1531      0.0604  249       0.0269  seti_boinc               v_BaseLineSmooth(float (*) [2], int, int, int)
1519      0.0599  188       0.0203  seti_boinc               calc_detection_freq(double, double, double)
1504      0.0594  659       0.0713  seti_boinc               t1_32
1498      0.0591  183       0.0198  seti_boinc               v_vTranspose4(int, int, float*, float*)
1489      0.0588  838       0.0906  seti_boinc               malloc_consolidate
1471      0.0581  739       0.0799  seti_boinc               checkpoint(unsigned char)
1470      0.0580  1136      0.1229  seti_boinc               operator new(unsigned int)
1438      0.0568  765       0.0827  seti_boinc               t2bv_32
1424      0.0562  752       0.0813  seti_boinc               sse_pulPoTf2AL8(float**, PoTPlan*)
1423      0.0562  134       0.0145  seti_boinc               v_vTranspose4np(int, int, float*, float*)
1402      0.0553  583       0.0631  seti_boinc               t2_16
1383      0.0546  921       0.0996  seti_boinc               t3fv_4
1318      0.0520  384       0.0415  seti_boinc               gaussian::gaussian()
1312      0.0518  590       0.0638  seti_boinc               t2_8
1238      0.0489  927       0.1003  seti_boinc               __i686.get_pc_thunk.cx
1196      0.0472  433       0.0468  seti_boinc               receiver_config::receiver_config()
1171      0.0462  517       0.0559  seti_boinc               t1_16
1128      0.0445  144       0.0156  seti_boinc               floor
1095      0.0432  525       0.0568  seti_boinc               t1_8
1079      0.0426  207       0.0224  seti_boinc               boinc_fraction_done
1025      0.0405  608       0.0658  seti_boinc               operator delete(void*)
1019      0.0402  155       0.0168  seti_boinc               finite
983       0.0388  384       0.0415  seti_boinc               v_pfTranspose4(int, int, float*, float*)
957       0.0378  520       0.0562  seti_boinc               ChooseTranspose()
911       0.0360  450       0.0487  seti_boinc               t2_4
870       0.0343  975       0.1055  seti_boinc               recur
866       0.0342  489       0.0529  seti_boinc               std::vector<unsigned char, std::allocator<unsigned char> >::_M_fill_insert(__gnu_cxx::__normal_iterator<unsigned char*, std::vector<unsigned char, std::allocator<unsigned char> > >, unsigned int, unsigned char const&)
863       0.0341  535       0.0579  seti_boinc               cexp_zero
833       0.0329  150       0.0162  seti_boinc               seti_analyze(ANALYSIS_STATE&)
817       0.0322  298       0.0322  seti_boinc               data_description_t::data_description_t()
788       0.0311  448       0.0485  seti_boinc               workunit_grp::workunit_grp()
776       0.0306  403       0.0436  seti_boinc               n1fv_16
753       0.0297  484       0.0523  seti_boinc               t2fv_16
743       0.0293  417       0.0451  seti_boinc               t1_4
702       0.0277  529       0.0572  seti_boinc               t1fuv_4
693       0.0274  352       0.0381  seti_boinc               t1fuv_8
634       0.0250  280       0.0303  seti_boinc               t1fv_8
604       0.0238  390       0.0422  seti_boinc               GAUSS_INFO::~GAUSS_INFO()
602       0.0238  221       0.0239  seti_boinc               __memmove_ssse3
546       0.0215  344       0.0372  seti_boinc               result::result()
536       0.0212  336       0.0363  seti_boinc               recur
520       0.0205  111       0.0120  seti_boinc               apply
509       0.0201  373       0.0403  seti_boinc               t1fv_4
497       0.0196  281       0.0304  seti_boinc               t1_2
485       0.0191  200       0.0216  seti_boinc               T.9614
470       0.0185  181       0.0196  seti_boinc               splitter_config::splitter_config()
466       0.0184  4        4.3e-04  seti_boinc               memcpy
465       0.0184  116       0.0125  seti_boinc               apply
460       0.0182  341       0.0369  seti_boinc               dobatch
458       0.0181  148       0.0160  seti_boinc               tape::tape()
445       0.0176  108       0.0117  seti_boinc               GaussianProgressUnits()
423       0.0167  362       0.0392  seti_boinc               vec_recip1(float __vector)
418       0.0165  283       0.0306  seti_boinc               MFILE::MFILE()
415       0.0164  42        0.0045  seti_boinc               __ieee754_log10
411       0.0162  177       0.0191  seti_boinc               n1_64
407       0.0161  131       0.0142  seti_boinc               GAUSS_INFO::GAUSS_INFO()
398       0.0157  169       0.0183  seti_boinc               recorder_config::recorder_config()
398       0.0157  173       0.0187  seti_boinc               workunit_header::workunit_header()
396       0.0156  184       0.0199  seti_boinc               n2bv_32
394       0.0155  57        0.0062  seti_boinc               SpikeProgressUnits(int)
386       0.0152  83        0.0090  seti_boinc               apply_dit
381       0.0150  282       0.0305  seti_boinc               q1fv_2
366       0.0144  307       0.0332  seti_boinc               fftwf_cpy1d
362       0.0143  172       0.0186  seti_boinc               subband_description_t::subband_description_t()
347       0.0137  130       0.0141  seti_boinc               t2fv_64
344       0.0136  211       0.0228  seti_boinc               MFILE::~MFILE()
339       0.0134  166       0.0180  seti_boinc               t1fv_64
334       0.0132  144       0.0156  seti_boinc               t1fv_32
331       0.0131  302       0.0327  seti_boinc               fftwf_md5putc
330       0.0130  136       0.0147  seti_boinc               _int_memalign
326       0.0129  137       0.0148  seti_boinc               q1_8
312       0.0123  170       0.0184  seti_boinc               t3fv_32
310       0.0122  140       0.0151  seti_boinc               apply
298       0.0118  87        0.0094  seti_boinc               T.9610
272       0.0107  138       0.0149  seti_boinc               T.9615
254       0.0100  138       0.0149  seti_boinc               t3fv_8
238       0.0094  132       0.0143  seti_boinc               invoke_solver
237       0.0094  139       0.0150  seti_boinc               t3fv_16
221       0.0087  46        0.0050  seti_boinc               spike::spike()
219       0.0086  162       0.0175  seti_boinc               t2fv_4
216       0.0085  136       0.0147  seti_boinc               n1bv_8
206       0.0081  156       0.0169  seti_boinc               fftwf_cpy2d_pair_ci
206       0.0081  115       0.0124  seti_boinc               q1_4
204       0.0081  163       0.0176  seti_boinc               fftwf_cpy2d_pair_co
201       0.0079  63        0.0068  seti_boinc               top_sum2(float**, PoTPlan*)
200       0.0079  59        0.0064  seti_boinc               pulse::pulse()
200       0.0079  11        0.0012  seti_boinc               random_r
197       0.0078  78        0.0084  seti_boinc               n1_32
183       0.0072  99        0.0107  seti_boinc               memalign
178       0.0070  308       0.0333  seti_boinc               random
177       0.0070  138       0.0149  seti_boinc               t1fuv_2
175       0.0069  108       0.0117  seti_boinc               t2bv_4
174       0.0069  113       0.0122  seti_boinc               boinc_time_to_checkpoint
172       0.0068  87        0.0094  seti_boinc               q1_2
170       0.0067  60        0.0065  seti_boinc               T.9619
169       0.0067  71        0.0077  seti_boinc               SPIKE_INFO::~SPIKE_INFO()
166       0.0066  88        0.0095  seti_boinc               t2fv_2
152       0.0060  25        0.0027  seti_boinc               apply
152       0.0060  81        0.0088  seti_boinc               n2fv_64
151       0.0060  54        0.0058  seti_boinc               sw_sum2_t31(float**, PoTPlan*)
150       0.0059  114       0.0123  seti_boinc               n1bv_16
150       0.0059  77        0.0083  seti_boinc               n2bv_16
150       0.0059  55        0.0059  seti_boinc               t2fv_8
150       0.0059  46        0.0050  seti_boinc               top_sum3(float**, PoTPlan*)
147       0.0058  42        0.0045  seti_boinc               fftwf_execute_dft
147       0.0058  143       0.0155  seti_boinc               t1fv_2
142       0.0056  36        0.0039  seti_boinc               log10
135       0.0053  62        0.0067  seti_boinc               t2fv_32
135       0.0053  41        0.0044  seti_boinc               top_sum4(float**, PoTPlan*)
131       0.0052  77        0.0083  seti_boinc               n1fv_8
126       0.0050  5        5.4e-04  seti_boinc               apply_before
123       0.0049  78        0.0084  seti_boinc               search0
118       0.0047  0              0  seti_boinc               apply_iter
108       0.0043  7        7.6e-04  seti_boinc               apply
105       0.0041  30        0.0032  seti_boinc               fftwf_measure_execution_time
104       0.0041  44        0.0048  seti_boinc               ChooseFoldSubs(ChirpFftPair_t*, int, int)
103       0.0041  45        0.0049  seti_boinc               fftwf_tile2d
95        0.0037  21        0.0023  seti_boinc               fftwf_choose_radix
95        0.0037  41        0.0044  seti_boinc               top_sum5(float**, PoTPlan*)
93        0.0037  35        0.0038  seti_boinc               n1_16
92        0.0036  29        0.0031  seti_boinc               SPIKE_INFO::SPIKE_INFO()
92        0.0036  16        0.0017  seti_boinc               apply_dif
91        0.0036  65        0.0070  seti_boinc               apply_buf
81        0.0032  38        0.0041  seti_boinc               mkplan
79        0.0031  38        0.0041  seti_boinc               foldArrayBy2LO(float**, PoTPlan*)
78        0.0031  29        0.0031  seti_boinc               fftwf_ct_applicable
78        0.0031  12        0.0013  seti_boinc               htab_lookup
76        0.0030  62        0.0067  seti_boinc               apply_extra_iter
76        0.0030  11        0.0012  seti_boinc               calloc_a(unsigned int, unsigned int, unsigned int)
73        0.0029  29        0.0031  seti_boinc               sw_sum3_t31(float**, PoTPlan*)
71        0.0028  27        0.0029  seti_boinc               sw_sum4_t31(float**, PoTPlan*)
69        0.0027  2        2.2e-04  [vdso] (tgid:7512 range:0x531000-0x532000) [vdso] (tgid:7512 range:0x531000-0x532000)
69        0.0027  12        0.0013  seti_boinc               GetPulsePoTLen(long, int*, int*)
65        0.0026  27        0.0029  seti_boinc               sw_sum5_t31(float**, PoTPlan*)
64        0.0025  19        0.0021  seti_boinc               fftwf_cpy2d_ci
63        0.0025  33        0.0036  seti_boinc               mkplan
62        0.0024  17        0.0018  seti_boinc               PULSE_INFO::PULSE_INFO()
62        0.0024  37        0.0040  seti_boinc               PULSE_INFO::~PULSE_INFO()
60        0.0024  11        0.0012  seti_boinc               copy
60        0.0024  9        9.7e-04  seti_boinc               fftwf_malloc
57        0.0022  30        0.0032  seti_boinc               BYTWJ1
57        0.0022  25        0.0027  seti_boinc               n1_8
56        0.0022  30        0.0032  seti_boinc               invert_lcgf(float, float, float)
49        0.0019  30        0.0032  seti_boinc               dotile
48        0.0019  12        0.0013  seti_boinc               fftwf_dft_solve
48        0.0019  18        0.0019  seti_boinc               foldArrayBy3(float**, PoTPlan*)
48        0.0019  40        0.0043  seti_boinc               n2bv_8
46        0.0018  21        0.0023  seti_boinc               fftwf_md5putb
46        0.0018  17        0.0018  seti_boinc               foldArrayBy4(float**, PoTPlan*)
43        0.0017  18        0.0019  seti_boinc               GetProgressUnitSize(int, int)
43        0.0017  40        0.0043  seti_boinc               dotile_buf
42        0.0017  7        7.6e-04  seti_boinc               fftwf_isqrt
42        0.0017  19        0.0021  seti_boinc               fftwf_kernel_malloc
41        0.0016  14        0.0015  seti_boinc               foldArrayBy3LO(float**, PoTPlan*)
40        0.0016  19        0.0021  seti_boinc               foldArrayBy5LO(float**, PoTPlan*)
37        0.0015  23        0.0025  seti_boinc               fftwf_kernel_free
37        0.0015  17        0.0018  seti_boinc               foldArrayBy4LO(float**, PoTPlan*)
35        0.0014  21        0.0023  seti_boinc               foldArrayBy2A(float**, PoTPlan*)
32        0.0013  18        0.0019  seti_boinc               planFoldTest(PoTPlan*, float*, int (*) [5])
30        0.0012  10        0.0011  seti_boinc               fftwf_elapsed_since
30        0.0012  25        0.0027  seti_boinc               fftwf_transpose
29        0.0011  18        0.0019  seti_boinc               foldArrayBy5(float**, PoTPlan*)
27        0.0011  8        8.7e-04  seti_boinc               fftwf_free
26        0.0010  0              0  seti_boinc               rand
25       9.9e-04  4        4.3e-04  seti_boinc               free_a(void*)
24       9.5e-04  5        5.4e-04  seti_boinc               fftwf_tensor_compress
24       9.5e-04  13        0.0014  seti_boinc               n2fv_32
21       8.3e-04  14        0.0015  seti_boinc               fftwf_cpy2d_co
21       8.3e-04  9        9.7e-04  seti_boinc               htab_insert
20       7.9e-04  14        0.0015  seti_boinc               VZMULJ
20       7.9e-04  0              0  seti_boinc               timer_handler()
18       7.1e-04  16        0.0017  seti_boinc               fftwf_md5end
18       7.1e-04  2        2.2e-04  seti_boinc               gettimeofday
18       7.1e-04  8        8.7e-04  seti_boinc               msort_with_tmp
17       6.7e-04  0              0  seti_boinc               __nanosleep_nocancel
17       6.7e-04  0              0  seti_boinc               boinc_sleep(double)
17       6.7e-04  7        7.6e-04  seti_boinc               hinsert0
17       6.7e-04  8        8.7e-04  seti_boinc               mkplan
16       6.3e-04  4        4.3e-04  seti_boinc               foldArrayBy2AL(float**, PoTPlan*)
16       6.3e-04  8        8.7e-04  seti_boinc               malloc_a(unsigned int, unsigned int)
16       6.3e-04  11        0.0012  seti_boinc               n1_2
16       6.3e-04  15        0.0016  seti_boinc               n1fv_2
16       6.3e-04  16        0.0017  seti_boinc               n1fv_4
15       5.9e-04  1        1.1e-04  seti_boinc               __libc_disable_asynccancel
15       5.9e-04  7        7.6e-04  seti_boinc               mkcldw
15       5.9e-04  11        0.0012  seti_boinc               n1_4
14       5.5e-04  8        8.7e-04  seti_boinc               fftwf_malloc_plain
14       5.5e-04  18        0.0019  seti_boinc               fftwf_mkstride
14       5.5e-04  6        6.5e-04  seti_boinc               fftwf_tensor_compress_contiguous
14       5.5e-04  6        6.5e-04  seti_boinc               mkplan
13       5.1e-04  5        5.4e-04  seti_boinc               apply_buf
13       5.1e-04  10        0.0011  seti_boinc               dotile
13       5.1e-04  0              0  seti_boinc               dtime()
13       5.1e-04  9        9.7e-04  seti_boinc               fftwf_ifree
13       5.1e-04  8        8.7e-04  seti_boinc               fftwf_mktensor
12       4.7e-04  7        7.6e-04  seti_boinc               dobatch
12       4.7e-04  2        2.2e-04  seti_boinc               fftwf_plan_awake
11       4.3e-04  2        2.2e-04  seti_boinc               fftwf_dimcmp
10       3.9e-04  7        7.6e-04  seti_boinc               fftwf_md5INT
10       3.9e-04  3        3.2e-04  seti_boinc               fftwf_tensor_destroy
10       3.9e-04  1        1.1e-04  seti_boinc               okp
10       3.9e-04  0              0  seti_boinc               worker_signal_handler(int)
9        3.6e-04  4        4.3e-04  seti_boinc               fftwf_mkproblem_dft
9        3.6e-04  7        7.6e-04  seti_boinc               fftwf_ops_madd
9        3.6e-04  5        5.4e-04  seti_boinc               fftwf_rdft_solve
9        3.6e-04  6        6.5e-04  seti_boinc               fftwf_tensor_append
8        3.2e-04  3        3.2e-04  seti_boinc               fftwf_tensor_sz
8        3.2e-04  0              0  seti_boinc               timer_thread(void*)
7        2.8e-04  4        4.3e-04  seti_boinc               apply
7        2.8e-04  2        2.2e-04  seti_boinc               evaluate_plan
7        2.8e-04  1        1.1e-04  seti_boinc               fftwf_null_awake
7        2.8e-04  3        3.2e-04  seti_boinc               fftwf_plan_destroy_internal
7        2.8e-04  1        1.1e-04  seti_boinc               fftwf_tensor_copy
7        2.8e-04  1        1.1e-04  seti_boinc               fftwf_tensor_destroy2
7        2.8e-04  0              0  seti_boinc               mkplan
7        2.8e-04  4        4.3e-04  seti_boinc               n2fv_16
7        2.8e-04  2        2.2e-04  seti_boinc               qsort_r
6        2.4e-04  1        1.1e-04  seti_boinc               apply_cpy2dco
6        2.4e-04  1        1.1e-04  seti_boinc               fftwf_compute_tilesz
6        2.4e-04  2        2.2e-04  seti_boinc               fftwf_iabs
6        2.4e-04  2        2.2e-04  seti_boinc               fftwf_ops_zero
6        2.4e-04  6        6.5e-04  seti_boinc               fftwf_tensor_tornk1
5        2.0e-04  0              0  seti_boinc               awake
5        2.0e-04  0              0  seti_boinc               fftwf_ct_uglyp
5        2.0e-04  10        0.0011  seti_boinc               fftwf_md5int
5        2.0e-04  1        1.1e-04  seti_boinc               fftwf_md5puts
5        2.0e-04  2        2.2e-04  seti_boinc               fftwf_mkplan
5        2.0e-04  1        1.1e-04  seti_boinc               fftwf_problem_destroy
5        2.0e-04  0              0  seti_boinc               fftwf_stride_destroy
5        2.0e-04  4        4.3e-04  seti_boinc               fftwf_tensor_md5
5        2.0e-04  7        7.6e-04  seti_boinc               fill_slot
5        2.0e-04  1        1.1e-04  seti_boinc               hgrow
5        2.0e-04  1        1.1e-04  seti_boinc               mkplan
5        2.0e-04  5        5.4e-04  seti_boinc               mkplan
5        2.0e-04  0              0  seti_boinc               zero
4        1.6e-04  5        5.4e-04  seti_boinc               applicable
4        1.6e-04  0              0  seti_boinc               awake
4        1.6e-04  2        2.2e-04  seti_boinc               fftwf_have_sse
4        1.6e-04  0              0  seti_boinc               fftwf_md5begin
4        1.6e-04  2        2.2e-04  seti_boinc               fftwf_mkproblem_dft_d
4        1.6e-04  1        1.1e-04  seti_boinc               fftwf_mkproblem_rdft
4        1.6e-04  1        1.1e-04  seti_boinc               fftwf_taint
4        1.6e-04  0              0  seti_boinc               fftwf_tensor_inplace_locations
4        1.6e-04  0              0  seti_boinc               hash
4        1.6e-04  0              0  seti_boinc               usleep
3        1.2e-04  1        1.1e-04  seti_boinc               apply
3        1.2e-04  2        2.2e-04  seti_boinc               apply_tiled
3        1.2e-04  1        1.1e-04  seti_boinc               awake
3        1.2e-04  0              0  seti_boinc               awake
3        1.2e-04  0              0  seti_boinc               fftwf_alignment_of
3        1.2e-04  1        1.1e-04  seti_boinc               fftwf_cpy2d_tiledbuf
3        1.2e-04  0              0  seti_boinc               fftwf_ifree0
3        1.2e-04  0              0  seti_boinc               fftwf_md5unsigned
3        1.2e-04  0              0  seti_boinc               fftwf_mkplan_d
3        1.2e-04  1        1.1e-04  seti_boinc               fftwf_mkplan_dftw
3        1.2e-04  0              0  seti_boinc               fftwf_mkproblem_rdft_1
3        1.2e-04  0              0  seti_boinc               fftwf_mktensor_2d
3        1.2e-04  0              0  seti_boinc               fftwf_ops_madd2
3        1.2e-04  1        1.1e-04  seti_boinc               fftwf_tensor_copy_inplace
3        1.2e-04  1        1.1e-04  seti_boinc               fftwf_tensor_inplace_strides
3        1.2e-04  1        1.1e-04  seti_boinc               getrusage
3        1.2e-04  2        2.2e-04  seti_boinc               hash
3        1.2e-04  0              0  seti_boinc               mkplan
3        1.2e-04  0              0  seti_boinc               mkplan
3        1.2e-04  1        1.1e-04  seti_boinc               mkplan
3        1.2e-04  0              0  seti_boinc               mkplan
3        1.2e-04  2        2.2e-04  seti_boinc               mkplan
3        1.2e-04  0              0  seti_boinc               nanosleep
3        1.2e-04  4        4.3e-04  seti_boinc               okp_common
3        1.2e-04  0              0  seti_boinc               okp_t1f
3        1.2e-04  2        2.2e-04  seti_boinc               okp_t1fu
3        1.2e-04  4        4.3e-04  seti_boinc               transpose
2        7.9e-05  2        2.2e-04  seti_boinc               ChirpProgressUnits()
2        7.9e-05  0              0  seti_boinc               ___printf_fp
2        7.9e-05  0              0  seti_boinc               __libc_enable_asynccancel
2        7.9e-05  2        2.2e-04  seti_boinc               apply_ip_sq
2        7.9e-05  0              0  seti_boinc               apply_memcpy_loop
2        7.9e-05  0              0  seti_boinc               destroy
2        7.9e-05  2        2.2e-04  seti_boinc               fftwf_hc2hc_applicable
2        7.9e-05  0              0  seti_boinc               fftwf_mkplan_dft
2        7.9e-05  2        2.2e-04  seti_boinc               fftwf_mkproblem
2        7.9e-05  1        1.1e-04  seti_boinc               fftwf_mktriggen
2        7.9e-05  0              0  seti_boinc               fftwf_tensor_strides_decrease
2        7.9e-05  1        1.1e-04  seti_boinc               hires_timer::ticks()
2        7.9e-05  3        3.2e-04  seti_boinc               hlookup
2        7.9e-05  0              0  seti_boinc               mkplan
2        7.9e-05  1        1.1e-04  seti_boinc               mkplan
2        7.9e-05  0              0  seti_boinc               mkplan
2        7.9e-05  5        5.4e-04  seti_boinc               n2fv_8
2        7.9e-05  0              0  seti_boinc               okp
2        7.9e-05  0              0  seti_boinc               okp
2        7.9e-05  0              0  seti_boinc               okp_t2f
2        7.9e-05  0              0  seti_boinc               result_group_start()
2        7.9e-05  1        1.1e-04  seti_boinc               timeout_p
1        3.9e-05  0              0  seti_boinc               __ieee754_exp
1        3.9e-05  0              0  seti_boinc               analysis_config::operator=(analysis_config const&)
1        3.9e-05  0              0  seti_boinc               applicable_cut
1        3.9e-05  0              0  seti_boinc               applicable_memcpy
1        3.9e-05  0              0  seti_boinc               apply_after
1        3.9e-05  1        1.1e-04  seti_boinc               apply_tiledbuf
1        3.9e-05  0              0  seti_boinc               awake
1        3.9e-05  0              0  seti_boinc               awake
1        3.9e-05  0              0  seti_boinc               destroy
1        3.9e-05  0              0  seti_boinc               destroy
1        3.9e-05  2        2.2e-04  seti_boinc               destroy
1        3.9e-05  0              0  seti_boinc               dotile_buf
1        3.9e-05  0              0  seti_boinc               fftwf_bufdist
1        3.9e-05  0              0  seti_boinc               fftwf_cpy2d_tiled
1        3.9e-05  2        2.2e-04  seti_boinc               fftwf_get_crude_time
1        3.9e-05  0              0  seti_boinc               fftwf_imax
1        3.9e-05  0              0  seti_boinc               fftwf_join_taint
1        3.9e-05  0              0  seti_boinc               fftwf_mktensor_1d
1        3.9e-05  0              0  seti_boinc               fftwf_nbuf_redundant
1        3.9e-05  0              0  seti_boinc               fftwf_ops_other
1        3.9e-05  1        1.1e-04  seti_boinc               fftwf_pickdim
1        3.9e-05  1        1.1e-04  seti_boinc               fftwf_tensor_copy_except
1        3.9e-05  0              0  seti_boinc               fftwf_tensor_destroy4
1        3.9e-05  0              0  seti_boinc               fftwf_tensor_inplace_strides2
1        3.9e-05  0              0  seti_boinc               fftwf_tensor_min_istride
1        3.9e-05  0              0  seti_boinc               fftwf_tensor_min_ostride
1        3.9e-05  0              0  seti_boinc               int std::__int_to_char<char, unsigned long>(char*, unsigned long, char const*, std::_Ios_Fmtflags, bool)
1        3.9e-05  0              0  seti_boinc               memcpy_loop
1        3.9e-05  0              0  seti_boinc               mkcld_before
1        3.9e-05  0              0  seti_boinc               mkplan
1        3.9e-05  0              0  seti_boinc               mkplan
1        3.9e-05  0              0  seti_boinc               mkplan
1        3.9e-05  0              0  seti_boinc               mkplan
1        3.9e-05  0              0  seti_boinc               mkplan
1        3.9e-05  0              0  seti_boinc               okp
1        3.9e-05  0              0  seti_boinc               okp
1        3.9e-05  1        1.1e-04  seti_boinc               okp
1        3.9e-05  0              0  seti_boinc               okp
1        3.9e-05  1        1.1e-04  seti_boinc               okp_commonu
1        3.9e-05  0              0  seti_boinc               okp_t1b
1        3.9e-05  1        1.1e-04  seti_boinc               plan_PulsePoT(PoTPlan*, int, float*, int*)
1        3.9e-05  1        1.1e-04  seti_boinc               qsort
1        3.9e-05  0              0  seti_boinc               really_pickdim
1        3.9e-05  0              0  seti_boinc               receiver_config::operator=(receiver_config const&)
1        3.9e-05  2        2.2e-04  seti_boinc               transpose_rec
0              0  1        1.1e-04  seti_boinc               Ntuple_transposable
0              0  1        1.1e-04  seti_boinc               _IO_default_xsputn
0              0  1        1.1e-04  seti_boinc               applicable_tiled
0              0  1        1.1e-04  seti_boinc               apply_ip_sq_tiledbuf
0              0  1        1.1e-04  seti_boinc               destroy
0              0  2        2.2e-04  seti_boinc               fftwf_imin
0              0  1        1.1e-04  seti_boinc               fftwf_nbuf
0              0  1        1.1e-04  seti_boinc               fftwf_ops_add
0              0  1        1.1e-04  seti_boinc               fftwf_tensor_equal
0              0  1        1.1e-04  seti_boinc               fftwf_transpose_tiled
0              0  1        1.1e-04  seti_boinc               fftwf_transpose_tiledbuf
0              0  1        1.1e-04  seti_boinc               n2fv_2
0              0  1        1.1e-04  seti_boinc               std::locale::id::_M_id() const
Mon Oct  3 01:48:47 CDT 2011
CPU: Intel Atom, speed 1795.54 MHz (estimated)
Counted LLC_MISSES events (Last level cache demand requests from this core that missed the LLC) with a unit mask of 0x41 (No unit mask) count 200000
Counted LLC_REFS events (Last level cache demand requests from this core) with a unit mask of 0x4f (No unit mask) count 200000
LLC_MISSES:200000|  LLC_REFS:200000|
  samples|      %|  samples|      %|
------------------------------------
     4802 99.8544     21250 99.8496 seti_boinc
        2  0.0416         1  0.0047 libdbus-1.so.3.5.2
        1  0.0208         4  0.0188 libc-2.12.1.so
        1  0.0208         1  0.0047 no-vmlinux
        1  0.0208         0       0 Xorg
        1  0.0208         0       0 libgdk-x11-2.0.so.0.2200.0
        1  0.0208         0       0 libxcb.so.1.1.0
        0       0         2  0.0094 bash
        0       0         1  0.0047 cat
        0       0         4  0.0188 dbus-daemon
        0       0         6  0.0282 ld-2.12.1.so
        0       0         2  0.0094 libglib-2.0.so.0.2600.1
        0       0         2  0.0094 libORBit-2.so.0.1.0
        0       0         5  0.0235 libcairo.so.2.11000.0
        0       0         1  0.0047 libdbus-glib-1.so.2.1.0
        0       0         1  0.0047 libgobject-2.0.so.0.2600.1
        0       0         1  0.0047 libgtk-x11-2.0.so.0.2200.0
        0       0         1  0.0047 libusbmuxd.so.1.0.4
 
CPU: Intel Atom, speed 1795.54 MHz (estimated)
Counted LLC_MISSES events (Last level cache demand requests from this core that missed the LLC) with a unit mask of 0x41 (No unit mask) count 200000
Counted LLC_REFS events (Last level cache demand requests from this core) with a unit mask of 0x4f (No unit mask) count 200000
samples  %        samples  %        symbol name
2702     56.2682  2760     12.9882  GetFixedPoT(float*, int, int, float*, int, int)
1364     28.4048  2618     12.3200  analyze_pot(float*, int, ChirpFftPair_t&)
329       6.8513  342       1.6094  sse2_ChirpData_ak(float (*) [2], float (*) [2], int, double, int, double)
100       2.0825  1289      6.0659  n1bv_128
50        1.0412  1976      9.2988  fftwf_cpy2d
37        0.7705  1534      7.2188  n1bv_64
34        0.7080  649       3.0541  t3bv_4
31        0.6456  879       4.1365  v_GetPowerSpectrum(float (*) [2], float*, int)
26        0.5414  2703     12.7200  q1bv_8
26        0.5414  1007      4.7388  t1bv_4
25        0.5206  195       0.9176  n2bv_64
20        0.4165  605       2.8471  FindSpikes(float*, int, int, SETI_WU_INFO&)
7         0.1458  3719     17.5012  t1bv_8
6         0.1249  36        0.1694  find_pulse(float const*, int, float, int, int)
4         0.0833  116       0.5459  t1bv_2
3         0.0625  10        0.0471  GaussFit(float*, int, int)
3         0.0625  19        0.0894  find_triplets(float const*, int, float, int, int)
3         0.0625  6         0.0282  n2bv_32
3         0.0625  1         0.0047  operator new(unsigned int)
2         0.0416  7         0.0329  TripletProgressUnits()
2         0.0416  17        0.0800  __i686.get_pc_thunk.bx
2         0.0416  28        0.1318  _int_malloc
2         0.0416  5         0.0235  analysis_config::analysis_config()
2         0.0416  0              0  apply_iter
2         0.0416  0              0  boinc_fraction_done
2         0.0416  0              0  fftwf_execute_dft
2         0.0416  3         0.0141  fraction_done(double, double)
2         0.0416  3         0.0141  seti_analyze(ANALYSIS_STATE&)
2         0.0416  273       1.2847  t1bv_16
1         0.0208  6         0.0282  __ieee754_pow
1         0.0208  6         0.0282  __memset_sse2
1         0.0208  11        0.0518  apply
1         0.0208  14        0.0659  apply
1         0.0208  0              0  apply_before
1         0.0208  2         0.0094  free
1         0.0208  1         0.0047  log
1         0.0208  3         0.0141  sse_pulPoTf3(float**, PoTPlan*)
1         0.0208  3         0.0141  tape::tape()
0              0  11        0.0518  ChooseGaussEvent(int, float, float, float, float, int, float, float, float*)
0              0  1         0.0047  GAUSS_INFO::~GAUSS_INFO()
0              0  2         0.0094  GaussianProgressUnits()
0              0  7         0.0329  MFILE::MFILE()
0              0  2         0.0094  ReportPulseEvent(float, float, float, int, int, float, float, float*, int, int)
0              0  2         0.0094  SPIKE_INFO::~SPIKE_INFO()
0              0  2         0.0094  SpikeProgressUnits(int)
0              0  1         0.0047  T.9610
0              0  1         0.0047  T.9614
0              0  2         0.0094  __ieee754_log
0              0  2         0.0094  __ieee754_log10
0              0  1         0.0047  __memmove_ssse3
0              0  1         0.0047  __nanosleep_nocancel
0              0  5         0.0235  _int_free
0              0  1         0.0047  apply
0              0  4         0.0188  apply
0              0  5         0.0235  apply
0              0  2         0.0094  apply_dif
0              0  7         0.0329  apply_dit
0              0  2         0.0094  boinc_time_to_checkpoint
0              0  3         0.0141  calc_detection_freq(double, double, double)
0              0  6         0.0282  checkpoint(unsigned char)
0              0  1         0.0047  cnvt_bin_hz(int, int)
0              0  2         0.0094  copy
0              0  2         0.0094  data_description_t::data_description_t()
0              0  2         0.0094  f_GetChiSq(float*, int, int, float, float, float*, float*)
0              0  1         0.0047  f_GetPeak(float*, int, int, float, float, float*)
0              0  2         0.0094  f_GetTrueMean(float*, int, float, int, int)
0              0  1         0.0047  float_to_uchar(float*, unsigned char*, long, float)
0              0  2         0.0094  floor
0              0  3         0.0141  gaussian::gaussian()
0              0  7         0.0329  isnan
0              0  2         0.0094  lcgf(double, double)
0              0  6         0.0282  malloc
0              0  8         0.0376  malloc_consolidate
0              0  1         0.0047  operator delete(void*)
0              0  3         0.0141  pow
0              0  2         0.0094  receiver_config::receiver_config()
0              0  1         0.0047  recorder_config::recorder_config()
0              0  5         0.0235  splitter_config::splitter_config()
0              0  5         0.0235  sse_pulPoTf2(float**, PoTPlan*)
0              0  2         0.0094  sse_pulPoTf2AL(float**, PoTPlan*)
0              0  1         0.0047  sse_pulPoTf2AL4(float**, PoTPlan*)
0              0  2         0.0094  sse_pulPoTf2L4(float**, PoTPlan*)
0              0  3         0.0141  sse_pulPoTf2L8(float**, PoTPlan*)
0              0  1         0.0047  sse_pulPoTf2u(float**, PoTPlan*)
0              0  3         0.0141  sse_pulPoTf3L8(float**, PoTPlan*)
0              0  1         0.0047  sse_pulPoTf4u(float**, PoTPlan*)
0              0  1         0.0047  sse_pulPoTf5L4(float**, PoTPlan*)
0              0  1         0.0047  sse_pulPoTf5u(float**, PoTPlan*)
0              0  4         0.0188  std::vector<unsigned char, std::allocator<unsigned char> >::_M_fill_insert(__gnu_cxx::__normal_iterator<unsigned char*, std::vector<unsigned char, std::allocator<unsigned char> > >, unsigned int, unsigned char const&)
0              0  35        0.1647  t2bv_32
0              0  204       0.9600  t2bv_64
0              0  14        0.0659  time_to_ra_dec(double, double*, double*)
0              0  2         0.0094  timer_handler()
0              0  4         0.0188  workunit_grp::workunit_grp()
Mon Oct  3 01:53:45 CDT 2011
CPU: Intel Atom, speed 1795.54 MHz (estimated)
Counted ITLB events (ITLB events) with a unit mask of 0x02 (misses ITLB misses) count 200000
Counted DATA_TLB_MISSES events (Memory accesses that missed the DTLB) with a unit mask of 0x07 (dtlb_miss Memory accesses that missed the DTLB) count 200000
      ITLB:200000|DATA_TLB_MISSE...|
  samples|      %|  samples|      %|
------------------------------------
       60 86.9565      2549 99.8824 seti_boinc
        3  4.3478         0       0 libdbus-1.so.3.5.2
        2  2.8986         0       0 libeggdbus-1.so.0.0.0
        1  1.4493         1  0.0392 libc-2.12.1.so
        1  1.4493         0       0 libgdk-x11-2.0.so.0.2200.0
        1  1.4493         0       0 libgio-2.0.so.0.2600.1
        1  1.4493         0       0 libgobject-2.0.so.0.2600.1
        0       0         1  0.0392 ld-2.12.1.so
        0       0         1  0.0392 libudev.so.0.9.1
 
CPU: Intel Atom, speed 1795.54 MHz (estimated)
Counted ITLB events (ITLB events) with a unit mask of 0x02 (misses ITLB misses) count 200000
Counted DATA_TLB_MISSES events (Memory accesses that missed the DTLB) with a unit mask of 0x07 (dtlb_miss Memory accesses that missed the DTLB) count 200000
samples  %        samples  %        symbol name
6        10.0000  0              0  GAUSS_INFO::GAUSS_INFO()
6        10.0000  7         0.2746  _int_malloc
6        10.0000  0              0  checkpoint(unsigned char)
4         6.6667  0              0  GAUSS_INFO::~GAUSS_INFO()
4         6.6667  1         0.0392  _int_free
4         6.6667  0              0  operator delete(void*)
3         5.0000  3         0.1177  malloc
2         3.3333  0              0  ChooseGaussEvent(int, float, float, float, float, int, float, float, float*)
2         3.3333  0              0  SPIKE_INFO::SPIKE_INFO()
2         3.3333  1         0.0392  __i686.get_pc_thunk.bx
2         3.3333  1         0.0392  apply_iter
2         3.3333  5         0.1962  boinc_fraction_done
2         3.3333  0              0  malloc_consolidate
2         3.3333  10        0.3923  n1bv_128
2         3.3333  0              0  recorder_config::recorder_config()
2         3.3333  0              0  result::result()
1         1.6667  8         0.3138  GaussFit(float*, int, int)
1         1.6667  0              0  __memmove_ssse3
1         1.6667  0              0  cnvt_bin_hz(int, int)
1         1.6667  0              0  free
1         1.6667  0              0  lcgf(double, double)
1         1.6667  0              0  operator new(unsigned int)
1         1.6667  0              0  tape::tape()
1         1.6667  1         0.0392  worker_signal_handler(int)
1         1.6667  0              0  workunit_header::workunit_header()
0              0  7         0.2746  FindSpikes(float*, int, int, SETI_WU_INFO&)
0              0  1         0.0392  GaussianProgressUnits()
0              0  1362     53.4327  GetFixedPoT(float*, int, int, float*, int, int)
0              0  20        0.7846  TripletProgressUnits()
0              0  7         0.2746  __ieee754_log
0              0  2         0.0785  __ieee754_pow
0              0  1         0.0392  __memset_sse2
0              0  979      38.4072  analyze_pot(float*, int, ChirpFftPair_t&)
0              0  1         0.0392  apply
0              0  1         0.0392  apply
0              0  1         0.0392  apply
0              0  30        1.1769  fftwf_cpy2d
0              0  4         0.1569  find_pulse(float const*, int, float, int, int)
0              0  21        0.8239  find_triplets(float const*, int, float, int, int)
0              0  4         0.1569  log
0              0  1         0.0392  n1bv_64
0              0  1         0.0392  n2bv_32
0              0  1         0.0392  n2bv_64
0              0  8         0.3138  pow
0              0  8         0.3138  q1bv_8
0              0  6         0.2354  sse2_ChirpData_ak(float (*) [2], float (*) [2], int, double, int, double)
0              0  2         0.0785  sse_pulPoTf3(float**, PoTPlan*)
0              0  2         0.0785  sse_pulPoTf3L8(float**, PoTPlan*)
0              0  2         0.0785  sse_pulPoTf3u(float**, PoTPlan*)
0              0  4         0.1569  t1bv_16
0              0  2         0.0785  t1bv_2
0              0  7         0.2746  t1bv_4
0              0  4         0.1569  t1bv_8
0              0  13        0.5100  t3bv_4
0              0  10        0.3923  v_GetPowerSpectrum(float (*) [2], float*, int)
Mon Oct  3 01:58:43 CDT 2011
CPU: Intel Atom, speed 1795.54 MHz (estimated)
Counted BR_INST_RETIRED events (number of branch instructions retired) with a unit mask of 0x00 (any Retired branch instructions) count 200000
Counted BR_MISS_PRED_RETIRED events (number of mispredicted branches retired (precise)) with a unit mask of 0x00 (No unit mask) count 200000
BR_INST_RETIRE...|BR_MISS_PRED_R...|
  samples|      %|  samples|      %|
------------------------------------
    82646 99.2936      1685 97.8513 seti_boinc
      284  0.3412        13  0.7549 libc-2.12.1.so
       94  0.1129         7  0.4065 libcairo.so.2.11000.0
       51  0.0613         4  0.2323 bash
       30  0.0360         2  0.1161 ld-2.12.1.so
       25  0.0300         2  0.1161 dbus-daemon
       22  0.0264         2  0.1161 oprofiled
       17  0.0204         5  0.2904 libdbus-1.so.3.5.2
       15  0.0180         1  0.0581 libglib-2.0.so.0.2600.1
       11  0.0132         0       0 libpthread-2.12.1.so
        9  0.0108         1  0.0581 libgobject-2.0.so.0.2600.1
        6  0.0072         0       0 ophelp
        5  0.0060         0       0 nvidia_drv.so
        3  0.0036         0       0 Xorg
        3  0.0036         0       0 libdbus-glib-1.so.2.1.0
        3  0.0036         0       0 libgconf-2.so.4.1.5
        2  0.0024         0       0 libgdu.so.0.0.0
        1  0.0012         0       0 dash
        1  0.0012         0       0 no-vmlinux
        1  0.0012         0       0 libORBit-2.so.0.1.0
        1  0.0012         0       0 libX11.so.6.3.0
        1  0.0012         0       0 libgthread-2.0.so.0.2600.1
        1  0.0012         0       0 libxcb.so.1.1.0
        1  0.0012         0       0 libnvidia-glcore.so.260.19.06
        1  0.0012         0       0 NetworkManager
 
CPU: Intel Atom, speed 1795.54 MHz (estimated)
Counted BR_INST_RETIRED events (number of branch instructions retired) with a unit mask of 0x00 (any Retired branch instructions) count 200000
Counted BR_MISS_PRED_RETIRED events (number of mispredicted branches retired (precise)) with a unit mask of 0x00 (No unit mask) count 200000
samples  %        samples  %        symbol name
19889    24.0659  2         0.1187  FindSpikes(float*, int, int, SETI_WU_INFO&)
9583     11.5955  488      28.9614  f_GetTrueMean(float*, int, float, int, int)
5968      7.2213  0              0  f_GetPeak(float*, int, int, float, float, float*)
5965      7.2177  0              0  fftwf_cpy2d
5450      6.5946  138       8.1899  GaussFit(float*, int, int)
4204      5.0869  94        5.5786  find_triplets(float const*, int, float, int, int)
3265      3.9507  70        4.1543  find_pulse(float const*, int, float, int, int)
2125      2.5713  23        1.3650  GetFixedPoT(float*, int, int, float*, int, int)
2068      2.5023  101       5.9941  analyze_pot(float*, int, ChirpFftPair_t&)
1789      2.1647  11        0.6528  f_GetChiSq(float*, int, int, float, float, float*, float*)
1771      2.1429  8         0.4748  __ieee754_pow
1688      2.0425  47        2.7893  lcgf(double, double)
1228      1.4859  1         0.0593  v_GetPowerSpectrum(float (*) [2], float*, int)
1201      1.4532  0              0  isnan
1195      1.4460  0              0  pow
1170      1.4157  43        2.5519  float_to_uchar(float*, unsigned char*, long, float)
1085      1.3129  0              0  __i686.get_pc_thunk.bx
1040      1.2584  42        2.4926  _int_free
817       0.9886  38        2.2552  _int_malloc
795       0.9620  4         0.2374  malloc
732       0.8857  4         0.2374  __ieee754_log
691       0.8361  1         0.0593  log
689       0.8337  1         0.0593  free
673       0.8143  1         0.0593  sse2_ChirpData_ak(float (*) [2], float (*) [2], int, double, int, double)
591       0.7151  2         0.1187  t1bv_4
560       0.6776  0              0  fraction_done(double, double)
423       0.5118  0              0  t3bv_4
371       0.4489  16        0.9496  time_to_ra_dec(double, double*, double*)
341       0.4126  3         0.1780  operator new(unsigned int)
318       0.3848  43        2.5519  sse_pulPoTf3(float**, PoTPlan*)
251       0.3037  34        2.0178  sse_pulPoTf2(float**, PoTPlan*)
217       0.2626  0              0  TripletProgressUnits()
214       0.2589  1         0.0593  t1bv_8
213       0.2577  5         0.2967  checkpoint(unsigned char)
210       0.2541  0              0  PulseProgressUnits(double, int)
188       0.2275  0              0  __i686.get_pc_thunk.cx
183       0.2214  42        2.4926  sse_pulPoTf2AL4(float**, PoTPlan*)
181       0.2190  59        3.5015  sse_pulPoTf2L8(float**, PoTPlan*)
177       0.2142  64        3.7982  sse_pulPoTf2L4(float**, PoTPlan*)
167       0.2021  0              0  t1bv_2
164       0.1984  11        0.6528  ChooseGaussEvent(int, float, float, float, float, int, float, float, float*)
147       0.1779  0              0  operator delete(void*)
146       0.1767  4         0.2374  GAUSS_INFO::~GAUSS_INFO()
146       0.1767  9         0.5341  malloc_consolidate
134       0.1621  20        1.1869  sse_pulPoTf3L8(float**, PoTPlan*)
132       0.1597  0              0  std::vector<unsigned char, std::allocator<unsigned char> >::_M_fill_insert(__gnu_cxx::__normal_iterator<unsigned char*, std::vector<unsigned char, std::allocator<unsigned char> > >, unsigned int, unsigned char const&)
103       0.1246  17        1.0089  sse_pulPoTf3u(float**, PoTPlan*)
103       0.1246  19        1.1276  sse_pulPoTf5(float**, PoTPlan*)
90        0.1089  54        3.2047  sse_pulPoTf4L8(float**, PoTPlan*)
89        0.1077  11        0.6528  sse_pulPoTf4(float**, PoTPlan*)
86        0.1041  11        0.6528  sse_pulPoTf4u(float**, PoTPlan*)
84        0.1016  19        1.1276  __memmove_ssse3
84        0.1016  23        1.3650  sse_pulPoTf5L8(float**, PoTPlan*)
81        0.0980  11        0.6528  sse_pulPoTf2AL(float**, PoTPlan*)
74        0.0895  0              0  MFILE::MFILE()
71        0.0859  0              0  GaussianProgressUnits()
67        0.0811  11        0.6528  sse_pulPoTf2u(float**, PoTPlan*)
63        0.0762  19        1.1276  __memset_sse2
58        0.0702  0              0  finite
51        0.0617  0              0  workunit_grp::workunit_grp()
49        0.0593  0              0  receiver_config::receiver_config()
48        0.0581  0              0  MFILE::~MFILE()
48        0.0581  0              0  analysis_config::analysis_config()
48        0.0581  4         0.2374  t1bv_16
46        0.0557  0              0  T.9614
46        0.0557  5         0.2967  gaussian::gaussian()
46        0.0557  10        0.5935  sse_pulPoTf5u(float**, PoTPlan*)
45        0.0545  0              0  result::result()
44        0.0532  0              0  data_description_t::data_description_t()
40        0.0484  0              0  cnvt_bin_hz(int, int)
36        0.0436  7         0.4154  sse_pulPoTf2AL8(float**, PoTPlan*)
35        0.0424  0              0  boinc_fraction_done
34        0.0411  0              0  splitter_config::splitter_config()
32        0.0387  9         0.5341  GAUSS_INFO::GAUSS_INFO()
30        0.0363  0              0  subband_description_t::subband_description_t()
29        0.0351  0              0  tape::tape()
26        0.0315  15        0.8902  sse_pulPoTf5L4(float**, PoTPlan*)
24        0.0290  2         0.1187  calc_detection_freq(double, double, double)
23        0.0278  0              0  boinc_time_to_checkpoint
22        0.0266  0              0  T.9615
22        0.0266  0              0  T.9619
21        0.0254  0              0  T.9610
21        0.0254  1         0.0593  q1bv_8
21        0.0254  0              0  recorder_config::recorder_config()
20        0.0242  0              0  n1bv_128
19        0.0230  0              0  workunit_header::workunit_header()
15        0.0182  1         0.0593  apply
15        0.0182  0              0  sse_pulPoTf2ALu(float**, PoTPlan*)
11        0.0133  0              0  floor
8         0.0097  0              0  SPIKE_INFO::~SPIKE_INFO()
8         0.0097  0              0  apply
6         0.0073  0              0  apply
5         0.0061  0              0  SpikeProgressUnits(int)
5         0.0061  0              0  n1bv_64
4         0.0048  2         0.1187  apply_dit
3         0.0036  0              0  ReportPulseEvent(float, float, float, int, int, float, float, float*, int, int)
3         0.0036  0              0  _int_memalign
3         0.0036  1         0.0593  apply_dif
3         0.0036  0              0  n2bv_64
3         0.0036  0              0  seti_analyze(ANALYSIS_STATE&)
3         0.0036  0              0  t2bv_32
2         0.0024  0              0  PULSE_INFO::~PULSE_INFO()
2         0.0024  0              0  fftwf_execute_dft
2         0.0024  1         0.0593  t2bv_64
1         0.0012  0              0  __ieee754_log10
1         0.0012  0              0  apply_iter
1         0.0012  0              0  boinc_sleep(double)
1         0.0012  0              0  copy
1         0.0012  1         0.0593  fftwf_cpy2d_ci
1         0.0012  0              0  log10
1         0.0012  0              0  memalign
1         0.0012  0              0  spike::spike()
1         0.0012  0              0  usleep
0              0  1         0.0593  SPIKE_INFO::SPIKE_INFO()
```


## Atom Oprofile SETI script ##
```
#!/bin/bash
SleepSeconds=292 
# atom processor 

./seti_boinc --standalone &

sudo rm -r /var/lib/oprofile/
sudo rm -r /root/.oprofile/daemonrc
sudo opcontrol --init
sudo opcontrol --no-vmlinux
sudo opcontrol --reset
sudo opcontrol --event=CPU_CLK_UNHALTED:200000:0x0:0:1 --event=INST_RETIRED:200000:0x1:0:1
sudo opcontrol --start
sudo opcontrol --status
echo "profiling for $SleepSeconds seconds"
sleep $SleepSeconds
sudo opcontrol --dump
date >> Atom.txt
sudo opreport >> Atom.txt
echo " " >> Atom.txt
sudo opreport -l /home/xbmc/Documents/boinc/seti_boinc/client/seti_boinc >> Atom.txt
sudo opcontrol --shutdown


sudo rm -r /var/lib/oprofile/
sudo rm -r /root/.oprofile/daemonrc
sudo opcontrol --init
sudo opcontrol --no-vmlinux
sudo opcontrol --reset
sudo opcontrol --event=LLC_MISSES:200000:0x41:0:1 --event=LLC_REFS:200000:0x4f:0:1
sudo opcontrol --start
sudo opcontrol --status
echo "profiling for $SleepSeconds seconds"
sleep $SleepSeconds
sudo opcontrol --dump
date >> Atom.txt
sudo opreport >> Atom.txt
echo " " >> Atom.txt
sudo opreport -l /home/xbmc/Documents/boinc/seti_boinc/client/seti_boinc >> Atom.txt
sudo opcontrol --shutdown

# 1)DTLB - any miss 2) 
sudo rm -r /var/lib/oprofile/
sudo rm -r /root/.oprofile/daemonrc
sudo opcontrol --init
sudo opcontrol --no-vmlinux
sudo opcontrol --reset
sudo opcontrol --event=DATA_TLB_MISSES:200000:0x7:0:1 --event=ITLB:200000:0x02:0:1 
sudo opcontrol --start
sudo opcontrol --status
echo "profiling for $SleepSeconds seconds"
sleep $SleepSeconds
sudo opcontrol --dump
date >> Atom.txt
sudo opreport >> Atom.txt
echo " " >> Atom.txt
sudo opreport -l /home/xbmc/Documents/boinc/seti_boinc/client/seti_boinc >> Atom.txt
sudo opcontrol --shutdown

# 1)DTLB - any miss 2) 
sudo rm -r /var/lib/oprofile/
sudo rm -r /root/.oprofile/daemonrc
sudo opcontrol --init
sudo opcontrol --no-vmlinux
sudo opcontrol --reset
sudo opcontrol --event=BR_INST_RETIRED:200000:0x0:0:1 --event=BR_MISS_PRED_RETIRED:200000:0x0:0:1
sudo opcontrol --start
sudo opcontrol --status
echo "profiling for $SleepSeconds seconds"
sleep $SleepSeconds
sudo opcontrol --dump
date >> Atom.txt
sudo opreport >> Atom.txt
echo " " >> Atom.txt
sudo opreport -l /home/xbmc/Documents/boinc/seti_boinc/client/seti_boinc >> Atom.txt
sudo opcontrol --shutdown
```