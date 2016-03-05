# Introduction #

# ARM Cortex-A8 (i.MX53) #
## Oprofile Cortex-A8 Events ##
```
lucid@lucid-desktop:~$ sudo opcontrol --list-events                             
                                                     
oprofile: available events for CPU type "ARM V7 PMNC"                           
                                                                                
See ARM11 Technical Reference Manual                                            
Cortex A8 DDI (ARM DDI 0344B, revision r1p1)                                    
PMNC_SW_INCR: (counter: 1, 2, 3, 4)                                             
        Software increment of PMNC registers (min count: 500)                   
IFETCH_MISS: (counter: 1, 2, 3, 4)                                              
        Instruction fetch misses from cache or normal cacheable memory (min cou 
ITLB_MISS: (counter: 1, 2, 3, 4)                                                
        Instruction fetch misses from TLB (min count: 500)                      
DCACHE_REFILL: (counter: 1, 2, 3, 4)                                            
        Data R/W operation that causes a refill from cache or normal cacheable  
        500)                                                                    
DCACHE_ACCESS: (counter: 1, 2, 3, 4)                                            
        Data R/W from cache (min count: 500)                                    
DTLB_REFILL: (counter: 1, 2, 3, 4)                                              
        Data R/W that causes a TLB refill (min count: 500)                      
DREAD: (counter: 1, 2, 3, 4)                                                    
        Data read architecturally executed (note: architecturally executed = fo 
        are unconditional or that pass the condition code) (min count: 500)     
DWRITE: (counter: 1, 2, 3, 4)                                                   
        Data write architecturally executed (min count: 500)                    
INSTR_EXECUTED: (counter: 1, 2, 3, 4)                                           
        All executed instructions (min count: 500)                              
EXC_TAKEN: (counter: 1, 2, 3, 4)                                                
        Exception taken (min count: 500)                                        
EXC_EXECUTED: (counter: 1, 2, 3, 4)                                             
        Exception return architecturally executed (min count: 500)              
CID_WRITE: (counter: 1, 2, 3, 4)                                                
        Instruction that writes to the Context ID Register architecturally exec 
        500)                                                                    
PC_WRITE: (counter: 1, 2, 3, 4)                                                 
        SW change of PC, architecturally executed (not by exceptions) (min coun 
PC_IMM_BRANCH: (counter: 1, 2, 3, 4)                                            
        Immediate branch instruction executed (taken or not) (min count: 500)   
PC_PROC_RETURN: (counter: 1, 2, 3, 4)                                           
        Procedure return architecturally executed (not by exceptions) (min coun 
UNALIGNED_ACCESS: (counter: 1, 2, 3, 4)                                         
        Unaligned access architecturally executed (min count: 500)              
PC_BRANCH_MIS_PRED: (counter: 1, 2, 3, 4)                                       
        Branch mispredicted or not predicted. Counts pipeline flushes because o 
        count: 500)                                                             
PC_BRANCH_MIS_USED: (counter: 1, 2, 3, 4)                                       
        Branch or change in program flow that could have been predicted (min co 
WRITE_BUFFER_FULL: (counter: 1, 2, 3, 4)                                        
        Any write buffer full cycle (min count: 500)                            
L2_STORE_MERGED: (counter: 1, 2, 3, 4)                                          
        Any store that is merged in L2 cache (min count: 500)                   
L2_STORE_BUFF: (counter: 1, 2, 3, 4)                                            
        Any bufferable store from load/store to L2 cache (min count: 500)       
L2_ACCESS: (counter: 1, 2, 3, 4)                                                
        Any access to L2 cache (min count: 500)                                 
L2_CACH_MISS: (counter: 1, 2, 3, 4)                                             
        Any cacheable miss in L2 cache (min count: 500)                         
AXI_READ_CYCLES: (counter: 1, 2, 3, 4)                                          
        Number of cycles for an active AXI read (min count: 500)                
AXI_WRITE_CYCLES: (counter: 1, 2, 3, 4)                                         
        Number of cycles for an active AXI write (min count: 500)               
MEMORY_REPLAY: (counter: 1, 2, 3, 4)                                            
        Any replay event in the memory subsystem (min count: 500)               
UNALIGNED_ACCESS_REPLAY: (counter: 1, 2, 3, 4)                                  
        Unaligned access that causes a replay (min count: 500)                  
L1_DATA_MISS: (counter: 1, 2, 3, 4)                                             
        L1 data cache miss as a result of the hashing algorithm (min count: 500 
L1_INST_MISS: (counter: 1, 2, 3, 4)                                             
        L1 instruction cache miss as a result of the hashing algorithm (min cou 
L1_DATA_COLORING: (counter: 1, 2, 3, 4)                                         
        L1 data access in which a page coloring alias occurs (min count: 500)   
L1_NEON_DATA: (counter: 1, 2, 3, 4)                                             
        NEON data access that hits L1 cache (min count: 500)                    
L1_NEON_CACH_DATA: (counter: 1, 2, 3, 4)                                        
        NEON cacheable data access that hits L1 cache (min count: 500)          
L2_NEON: (counter: 1, 2, 3, 4)                                                  
        L2 access as a result of NEON memory access (min count: 500)            
L2_NEON_HIT: (counter: 1, 2, 3, 4)                                              
        Any NEON hit in L2 cache (min count: 500)                               
L1_INST: (counter: 1, 2, 3, 4)                                                  
        Any L1 instruction cache access, excluding CP15 cache accesses (min cou 
PC_RETURN_MIS_PRED: (counter: 1, 2, 3, 4)                                       
        Return stack misprediction at return stack pop (incorrect target addres 
PC_BRANCH_FAILED: (counter: 1, 2, 3, 4)                                         
        Branch prediction misprediction (min count: 500)                        
PC_BRANCH_TAKEN: (counter: 1, 2, 3, 4)                                          
        Any predicted branch that is taken (min count: 500)                     
PC_BRANCH_EXECUTED: (counter: 1, 2, 3, 4)                                       
        Any taken branch that is executed (min count: 500)                      
OP_EXECUTED: (counter: 1, 2, 3, 4)                                              
        Number of operations executed (in instruction or mutli-cycle instructio 
CYCLES_INST_STALL: (counter: 1, 2, 3, 4)                                        
        Cycles where no instruction available (min count: 500)                  
CYCLES_INST: (counter: 1, 2, 3, 4)                                              
        Number of instructions issued in a cycle (min count: 500)               
CYCLES_NEON_DATA_STALL: (counter: 1, 2, 3, 4)                                   
        Number of cycles the processor waits on MRC data from NEON (min count:  
CYCLES_NEON_INST_STALL: (counter: 1, 2, 3, 4)                                   
        Number of cycles the processor waits on NEON instruction queue or NEON  
        count: 500)                                                             
NEON_CYCLES: (counter: 1, 2, 3, 4)                                              
        Number of cycles NEON and integer processors are not idle (min count: 5 
PMU0_EVENTS: (counter: 1, 2, 3, 4)                                              
        Number of events from external input source PMUEXTIN[0] (min count: 500 
PMU1_EVENTS: (counter: 1, 2, 3, 4)                                              
        Number of events from external input source PMUEXTIN[1] (min count: 500 
PMU_EVENTS: (counter: 1, 2, 3, 4)                                               
        Number of events from both external input sources PMUEXTIN[0] and PMUEX 
        500)                                                                    
CPU_CYCLES: (counter: 0)                                                        
        Number of CPU cycles (min count: 500)                                   
lucid@lucid-desktop:~$
```
## Event Data on i.MX53 ##
```
Tue Sep 20 09:36:34 CST 2011
CPU: ARM V7 PMNC, speed 0 MHz (estimated)
Counted CPU_CYCLES events (Number of CPU cycles) with a unit mask of 0x00 (No unit mask) count 10000
 CPU_CYCLES:10000|
  samples|      %|
------------------
 11940765 94.3225 seti_boinc
	 CPU_CYCLES:10000|
	  samples|      %|
	------------------
	 11937088 99.9692 seti_boinc
	     3677  0.0308 [vectors] (tgid:18176 range:0xffff0000-0xffff1000)
   709950  5.6080 oprofiled
	 CPU_CYCLES:10000|
	  samples|      %|
	------------------
	   709857 99.9869 oprofiled
	       93  0.0131 [vectors] (tgid:18689 range:0xffff0000-0xffff1000)
     6405  0.0506 libc-2.11.1.so
      682  0.0054 ntpd
	 CPU_CYCLES:10000|
	  samples|      %|
	------------------
	      677 99.2669 ntpd
	        5  0.7331 [vectors] (tgid:4355 range:0xffff0000-0xffff1000)
      634  0.0050 libavahi-core.so.6.0.1
      632  0.0050 libavahi-common.so.3.5.1
      160  0.0013 ld-2.11.1.so
      118 9.3e-04 rsyslogd
	 CPU_CYCLES:10000|
	  samples|      %|
	------------------
	      112 94.9153 rsyslogd
	        6  5.0847 [vectors] (tgid:3140 range:0xffff0000-0xffff1000)
       60 4.7e-04 libpthread-2.11.1.so
       50 3.9e-04 avahi-daemon
	 CPU_CYCLES:10000|
	  samples|      %|
	------------------
	       32 64.0000 [vectors] (tgid:3240 range:0xffff0000-0xffff1000)
	       18 36.0000 avahi-daemon
       16 1.3e-04 sshd
       14 1.1e-04 bash
       13 1.0e-04 libcrypto.so.0.9.8
        5 3.9e-05 libgcc_s.so.1
        5 3.9e-05 imklog.so
        3 2.4e-05 cron
 
CPU: ARM V7 PMNC, speed 0 MHz (estimated)
Counted CPU_CYCLES events (Number of CPU cycles) with a unit mask of 0x00 (No unit mask) count 10000
samples  %        image name               symbol name
4482906  37.4155  seti_boinc               top_sum2(float**, PoTPlan*)
2639826  22.0327  seti_boinc               top_sum3(float**, PoTPlan*)
2107189  17.5872  seti_boinc               top_sum4(float**, PoTPlan*)
2048447  17.0969  seti_boinc               top_sum5(float**, PoTPlan*)
102943    0.8592  seti_boinc               __ieee754_log
72492     0.6050  seti_boinc               sw_sum2_t31(float**, PoTPlan*)
45976     0.3837  seti_boinc               t_funct(int, int, int)
45630     0.3808  seti_boinc               find_pulse(float const*, int, float, int, int)
38491     0.3213  seti_boinc               __ieee754_pow
28458     0.2375  seti_boinc               n1_8
25432     0.2123  seti_boinc               FindSpikes(float*, int, int, SETI_WU_INFO&)
22217     0.1854  seti_boinc               time_to_ra_dec(double, double*, double*)
20168     0.1683  seti_boinc               __exp1
18808     0.1570  seti_boinc               GetFixedPoT(float*, int, int, float*, int, int)
18410     0.1537  seti_boinc               v_GetPowerSpectrum(float (*) [2], float*, int)
16327     0.1363  seti_boinc               lcgf(double, double)
15957     0.1332  seti_boinc               t1_32
13328     0.1112  seti_boinc               n1_64
10810     0.0902  seti_boinc               analyze_pot(float*, int, ChirpFftPair_t&)
10369     0.0865  seti_boinc               ReportPulseEvent(float, float, float, int, int, float, float, float*, int, int)
10281     0.0858  seti_boinc               v_BaseLineSmooth(float (*) [2], int, int, int)
10030     0.0837  seti_boinc               malloc
8806      0.0735  seti_boinc               SpikeProgressUnits(int)
8656      0.0722  seti_boinc               _int_malloc
7943      0.0663  seti_boinc               logl
7531      0.0629  seti_boinc               calc_detection_freq(double, double, double)
7123      0.0595  seti_boinc               seti_analyze(ANALYSIS_STATE&)
6981      0.0583  seti_boinc               __divsi3
6799      0.0567  seti_boinc               analysis_config::analysis_config()
6332      0.0528  seti_boinc               n1_32
6255      0.0522  seti_boinc               t1_16
5868      0.0490  seti_boinc               free
5533      0.0462  seti_boinc               _int_free
5159      0.0431  seti_boinc               q1_8
4754      0.0397  seti_boinc               splitter_config::splitter_config()
4682      0.0391  seti_boinc               q1_4
4196      0.0350  seti_boinc               powl
4008      0.0335  seti_boinc               t1_4
3858      0.0322  seti_boinc               t1_8
3759      0.0314  seti_boinc               cnvt_bin_hz(int, int)
3682      0.0307  [vectors] (tgid:18176 range:0xffff0000-0xffff1000) [vectors] (tgid:18176 range:0xffff0000-0xffff1000)
3610      0.0301  seti_boinc               find_triplets(float const*, int, float, int, int)
3262      0.0272  seti_boinc               fraction_done(double, double)
3227      0.0269  seti_boinc               memcpy
3135      0.0262  seti_boinc               data_description_t::data_description_t()
3067      0.0256  seti_boinc               workunit_grp::workunit_grp()
2787      0.0233  seti_boinc               __ieee754_log10
2652      0.0221  seti_boinc               operator new(unsigned int)
2616      0.0218  seti_boinc               tape::tape()
2360      0.0197  seti_boinc               GetPulsePoTLen(long, int*, int*)
2315      0.0193  seti_boinc               malloc_consolidate
2275      0.0190  seti_boinc               memset
2172      0.0181  seti_boinc               isnanl
2097      0.0175  seti_boinc               log10l
1928      0.0161  seti_boinc               recorder_config::recorder_config()
1851      0.0154  seti_boinc               spike::spike()
1749      0.0146  seti_boinc               SPIKE_INFO::~SPIKE_INFO()
1702      0.0142  seti_boinc               subband_description_t::subband_description_t()
1685      0.0141  seti_boinc               fftwf_execute_dft
1446      0.0121  seti_boinc               boinc_fraction_done
1376      0.0115  seti_boinc               receiver_config::receiver_config()
1328      0.0111  seti_boinc               result::result()
1266      0.0106  seti_boinc               GetProgressUnitSize(int, int)
1168      0.0097  seti_boinc               pulse::pulse()
1161      0.0097  seti_boinc               operator delete(void*)
1083      0.0090  seti_boinc               workunit_header::workunit_header()
894       0.0075  seti_boinc               T.9826
761       0.0064  seti_boinc               invert_lcgf(float, float, float)
735       0.0061  seti_boinc               apply
721       0.0060  seti_boinc               T.9822
604       0.0050  seti_boinc               PULSE_INFO::~PULSE_INFO()
517       0.0043  seti_boinc               std::vector<unsigned char, std::allocator<unsigned char> >::_M_fill_insert(__gnu_cxx::__normal_iterator<unsigned char*, std::vector<unsigned char, std::allocator<unsigned char> > >, unsigned int, unsigned char const&)
513       0.0043  seti_boinc               T.9827
484       0.0040  seti_boinc               nanosleep
457       0.0038  seti_boinc               SPIKE_INFO::SPIKE_INFO()
451       0.0038  seti_boinc               floorf
433       0.0036  seti_boinc               finite
423       0.0035  seti_boinc               PULSE_INFO::PULSE_INFO()
403       0.0034  seti_boinc               timer_handler()
307       0.0026  seti_boinc               __ieee754_fmod
276       0.0023  seti_boinc               __libc_disable_asynccancel
276       0.0023  seti_boinc               fmodl
233       0.0019  seti_boinc               __aeabi_read_tp
227       0.0019  seti_boinc               boinc_sleep(double)
227       0.0019  seti_boinc               worker_signal_handler(int)
219       0.0018  seti_boinc               GenChirpFftPairs(ChirpFftPair_t**, double*)
186       0.0016  seti_boinc               PulseProgressUnits(double, int)
182       0.0015  seti_boinc               calloc_a(unsigned int, unsigned int, unsigned int)
182       0.0015  seti_boinc               getrusage
179       0.0015  seti_boinc               usleep
167       0.0014  seti_boinc               dtime()
155       0.0013  seti_boinc               GaussianProgressUnits()
130       0.0011  seti_boinc               gettimeofday
116      9.7e-04  seti_boinc               fftwf_malloc
111      9.3e-04  seti_boinc               fftwf_kernel_malloc
100      8.3e-04  seti_boinc               timer_thread(void*)
92       7.7e-04  seti_boinc               __default_sa_restorer_v2
86       7.2e-04  seti_boinc               ____libc_disable_asynccancel_veneer
81       6.8e-04  seti_boinc               __libc_enable_asynccancel
73       6.1e-04  seti_boinc               memmove
66       5.5e-04  seti_boinc               TripletProgressUnits()
62       5.2e-04  seti_boinc               isinfl
62       5.2e-04  seti_boinc               std::_Rb_tree_insert_and_rebalance(bool, std::_Rb_tree_node_base*, std::_Rb_tree_node_base*, std::_Rb_tree_node_base&)
58       4.8e-04  seti_boinc               free_a(void*)
41       3.4e-04  seti_boinc               malloc_a(unsigned int, unsigned int)
39       3.3e-04  seti_boinc               T.9831
33       2.8e-04  seti_boinc               fftwf_free
28       2.3e-04  seti_boinc               __aeabi_d2ulz
28       2.3e-04  seti_boinc               fftwf_kernel_free
25       2.1e-04  seti_boinc               boinc_worker_thread_cpu_time
21       1.8e-04  seti_boinc               floor
18       1.5e-04  seti_boinc               ____libc_enable_asynccancel_veneer
17       1.4e-04  seti_boinc               GaussFit(float*, int, int)
15       1.3e-04  seti_boinc               std::_Rb_tree<long long, std::pair<long long const, ChirpFftPair_t>, std::_Select1st<std::pair<long long const, ChirpFftPair_t> >, std::less<long long>, std::allocator<std::pair<long long const, ChirpFftPair_t> > >::_M_insert_unique_(std::_Rb_tree_const_iterator<std::pair<long long const, ChirpFftPair_t> >, std::pair<long long const, ChirpFftPair_t> const&)
14       1.2e-04  seti_boinc               apply_dit
14       1.2e-04  seti_boinc               boinc_info
13       1.1e-04  seti_boinc               std::_Rb_tree<long long, std::pair<long long const, ChirpFftPair_t>, std::_Select1st<std::pair<long long const, ChirpFftPair_t> >, std::less<long long>, std::allocator<std::pair<long long const, ChirpFftPair_t> > >::_M_insert_(std::_Rb_tree_node_base const*, std::_Rb_tree_node_base const*, std::pair<long long const, ChirpFftPair_t> const&)
12       1.0e-04  seti_boinc               __ieee754_exp
12       1.0e-04  seti_boinc               apply
12       1.0e-04  seti_boinc               apply
12       1.0e-04  seti_boinc               std::_Rb_tree_decrement(std::_Rb_tree_node_base const*)
11       9.2e-05  seti_boinc               ChirpProgressUnits()
6        5.0e-05  seti_boinc               __fixdfdi
6        5.0e-05  seti_boinc               apply
6        5.0e-05  seti_boinc               checkpoint(unsigned char)
6        5.0e-05  seti_boinc               receiver_config::operator=(receiver_config const&)
5        4.2e-05  seti_boinc               workunit_grp::operator=(workunit_grp const&)
4        3.3e-05  seti_boinc               analysis_config::operator=(analysis_config const&)
4        3.3e-05  seti_boinc               apply_dif
4        3.3e-05  seti_boinc               data_description_t::operator=(data_description_t const&)
2        1.7e-05  seti_boinc               fftwf_execute
1        8.3e-06  seti_boinc               SPIKE_INFO::operator=(SPIKE_INFO const&)
1        8.3e-06  seti_boinc               __sync_val_compare_and_swap_4
1        8.3e-06  seti_boinc               boinc_time_to_checkpoint
1        8.3e-06  seti_boinc               exp
1        8.3e-06  seti_boinc               f_GetPeakScaleFactor(float)
1        8.3e-06  seti_boinc               fftwf_dft_solve
1        8.3e-06  seti_boinc               pulse::operator=(pulse const&)
1        8.3e-06  seti_boinc               result::operator=(result const&)
1        8.3e-06  seti_boinc               splitter_config::operator=(splitter_config const&)
1        8.3e-06  seti_boinc               sqlblob<unsigned char>::operator=(sqlblob<unsigned char> const&)
1        8.3e-06  seti_boinc               subband_description_t::operator=(subband_description_t const&)
 
 
Tue Sep 20 09:40:35 CST 2011
CPU: ARM V7 PMNC, speed 0 MHz (estimated)
Counted INSTR_EXECUTED events (All executed instructions) with a unit mask of 0x00 (No unit mask) count 10000
INSTR_EXECUTED...|
  samples|      %|
------------------
  4682193 96.2740 seti_boinc
	INSTR_EXECUTED...|
	  samples|      %|
	------------------
	  4681599 99.9873 seti_boinc
	      594  0.0127 [vectors] (tgid:18176 range:0xffff0000-0xffff1000)
   134519  2.7659 oprofiled
	INSTR_EXECUTED...|
	  samples|      %|
	------------------
	   134488 99.9770 oprofiled
	       31  0.0230 [vectors] (tgid:19917 range:0xffff0000-0xffff1000)
    34340  0.7061 libc-2.11.1.so
     7964  0.1638 bash
	INSTR_EXECUTED...|
	  samples|      %|
	------------------
	     7244 90.9593 bash
	      361  4.5329 [vectors] (tgid:20064 range:0xffff0000-0xffff1000)
	      357  4.4827 [vectors] (tgid:19920 range:0xffff0000-0xffff1000)
	        1  0.0126 [vectors] (tgid:18175 range:0xffff0000-0xffff1000)
	        1  0.0126 anon (tgid:19920 range:0x2aaf7000-0x2aaf8000)
     3446  0.0709 ld-2.11.1.so
      201  0.0041 libavahi-common.so.3.5.1
      175  0.0036 ophelp
      120  0.0025 gawk
      115  0.0024 tr
       59  0.0012 ntpd
       47 9.7e-04 libavahi-core.so.6.0.1
       43 8.8e-04 libpam.so.0.82.2
       42 8.6e-04 sudo
	INSTR_EXECUTED...|
	  samples|      %|
	------------------
	       27 64.2857 sudo
	       10 23.8095 [vectors] (tgid:20064 range:0xffff0000-0xffff1000)
	        5 11.9048 [vectors] (tgid:19920 range:0xffff0000-0xffff1000)
       38 7.8e-04 dash
       15 3.1e-04 grep
       14 2.9e-04 rsyslogd
	INSTR_EXECUTED...|
	  samples|      %|
	------------------
	       12 85.7143 rsyslogd
	        2 14.2857 [vectors] (tgid:3140 range:0xffff0000-0xffff1000)
       10 2.1e-04 LC_COLLATE
       10 2.1e-04 avahi-daemon
	INSTR_EXECUTED...|
	  samples|      %|
	------------------
	        9 90.0000 [vectors] (tgid:3240 range:0xffff0000-0xffff1000)
	        1 10.0000 avahi-daemon
        6 1.2e-04 libnss_compat-2.11.1.so
        6 1.2e-04 libpthread-2.11.1.so
        5 1.0e-04 libcrypto.so.0.9.8
        5 1.0e-04 libdl-2.11.1.so
        5 1.0e-04 libgcc_s.so.1
        4 8.2e-05 ls
        4 8.2e-05 libselinux.so.1
        3 6.2e-05 libm-2.11.1.so
        3 6.2e-05 LC_CTYPE
        2 4.1e-05 libpopt.so.0.0.0
        2 4.1e-05 gconv-modules.cache
        2 4.1e-05 sshd
        1 2.1e-05 mkdir
        1 2.1e-05 sleep
	INSTR_EXECUTED...|
	  samples|      %|
	------------------
	        1 100.000 [vectors] (tgid:20062 range:0xffff0000-0xffff1000)
        1 2.1e-05 libncurses.so.5.7
        1 2.1e-05 seq
        1 2.1e-05 LC_ADDRESS
        1 2.1e-05 LC_TELEPHONE
 
CPU: ARM V7 PMNC, speed 0 MHz (estimated)
Counted INSTR_EXECUTED events (All executed instructions) with a unit mask of 0x00 (No unit mask) count 10000
samples  %        image name               symbol name
1857612  39.6740  seti_boinc               top_sum2(float**, PoTPlan*)
1048792  22.3996  seti_boinc               top_sum3(float**, PoTPlan*)
906753   19.3660  seti_boinc               top_sum4(float**, PoTPlan*)
767201   16.3855  seti_boinc               top_sum5(float**, PoTPlan*)
28943     0.6182  seti_boinc               t_funct(int, int, int)
25761     0.5502  seti_boinc               sw_sum2_t31(float**, PoTPlan*)
21435     0.4578  seti_boinc               find_pulse(float const*, int, float, int, int)
9065      0.1936  seti_boinc               __divsi3
4109      0.0878  seti_boinc               ReportPulseEvent(float, float, float, int, int, float, float, float*, int, int)
2616      0.0559  seti_boinc               _int_malloc
1939      0.0414  seti_boinc               find_triplets(float const*, int, float, int, int)
1080      0.0231  seti_boinc               _int_free
953       0.0204  seti_boinc               memset
850       0.0182  seti_boinc               analyze_pot(float*, int, ChirpFftPair_t&)
681       0.0145  seti_boinc               malloc
596       0.0127  [vectors] (tgid:18176 range:0xffff0000-0xffff1000) [vectors] (tgid:18176 range:0xffff0000-0xffff1000)
498       0.0106  seti_boinc               free
449       0.0096  seti_boinc               malloc_consolidate
256       0.0055  seti_boinc               operator new(unsigned int)
216       0.0046  seti_boinc               time_to_ra_dec(double, double*, double*)
183       0.0039  seti_boinc               PULSE_INFO::~PULSE_INFO()
179       0.0038  seti_boinc               analysis_config::analysis_config()
178       0.0038  seti_boinc               workunit_grp::workunit_grp()
156       0.0033  seti_boinc               pulse::pulse()
141       0.0030  seti_boinc               T.9826
109       0.0023  seti_boinc               result::result()
106       0.0023  seti_boinc               receiver_config::receiver_config()
100       0.0021  seti_boinc               operator delete(void*)
99        0.0021  seti_boinc               tape::tape()
93        0.0020  seti_boinc               workunit_header::workunit_header()
90        0.0019  seti_boinc               data_description_t::data_description_t()
85        0.0018  seti_boinc               std::vector<unsigned char, std::allocator<unsigned char> >::_M_fill_insert(__gnu_cxx::__normal_iterator<unsigned char*, std::vector<unsigned char, std::allocator<unsigned char> > >, unsigned int, unsigned char const&)
82        0.0018  seti_boinc               splitter_config::splitter_config()
73        0.0016  seti_boinc               PULSE_INFO::PULSE_INFO()
59        0.0013  seti_boinc               cnvt_bin_hz(int, int)
50        0.0011  seti_boinc               recorder_config::recorder_config()
44       9.4e-04  seti_boinc               subband_description_t::subband_description_t()
43       9.2e-04  seti_boinc               calc_detection_freq(double, double, double)
42       9.0e-04  seti_boinc               T.9827
41       8.8e-04  seti_boinc               fftwf_malloc
38       8.1e-04  seti_boinc               floorf
36       7.7e-04  seti_boinc               calloc_a(unsigned int, unsigned int, unsigned int)
34       7.3e-04  seti_boinc               fftwf_free
34       7.3e-04  seti_boinc               free_a(void*)
33       7.0e-04  seti_boinc               T.9822
31       6.6e-04  seti_boinc               T.9831
28       6.0e-04  seti_boinc               fftwf_kernel_malloc
21       4.5e-04  seti_boinc               memcpy
14       3.0e-04  seti_boinc               __ieee754_fmod
14       3.0e-04  seti_boinc               malloc_a(unsigned int, unsigned int)
13       2.8e-04  seti_boinc               nanosleep
12       2.6e-04  seti_boinc               dtime()
11       2.3e-04  seti_boinc               __aeabi_read_tp
11       2.3e-04  seti_boinc               memmove
9        1.9e-04  seti_boinc               boinc_sleep(double)
9        1.9e-04  seti_boinc               getrusage
8        1.7e-04  seti_boinc               fftwf_kernel_free
8        1.7e-04  seti_boinc               timer_handler()
5        1.1e-04  seti_boinc               gettimeofday
4        8.5e-05  seti_boinc               __ieee754_log
4        8.5e-05  seti_boinc               __libc_enable_asynccancel
4        8.5e-05  seti_boinc               hack_digit.11765
4        8.5e-05  seti_boinc               worker_signal_handler(int)
3        6.4e-05  seti_boinc               __default_sa_restorer_v2
3        6.4e-05  seti_boinc               __udivsi3
3        6.4e-05  seti_boinc               fmodl
3        6.4e-05  seti_boinc               isinfl
3        6.4e-05  seti_boinc               isnanl
3        6.4e-05  seti_boinc               std::basic_ostream<char, std::char_traits<char> >& std::__ostream_insert<char, std::char_traits<char> >(std::basic_ostream<char, std::char_traits<char> >&, char const*, int)
3        6.4e-05  seti_boinc               usleep
3        6.4e-05  seti_boinc               vfprintf
2        4.3e-05  seti_boinc               ___printf_fp
2        4.3e-05  seti_boinc               __cxxabiv1::__vmi_class_type_info::__do_dyncast(int, __cxxabiv1::__class_type_info::__sub_kind, __cxxabiv1::__class_type_info const*, void const*, __cxxabiv1::__class_type_info const*, void const*, __cxxabiv1::__class_type_info::__dyncast_result&) const
2        4.3e-05  seti_boinc               __libc_disable_asynccancel
2        4.3e-05  seti_boinc               __mpn_divrem
2        4.3e-05  seti_boinc               boinc_worker_thread_cpu_time
2        4.3e-05  seti_boinc               gaussian::print_xml(int, int, int, char const*) const
2        4.3e-05  seti_boinc               std::basic_streambuf<char, std::char_traits<char> >::xsputn(char const*, int)
1        2.1e-05  seti_boinc               TripletProgressUnits()
1        2.1e-05  seti_boinc               ____libc_disable_asynccancel_veneer
1        2.1e-05  seti_boinc               ____libc_enable_asynccancel_veneer
1        2.1e-05  seti_boinc               __exp1
1        2.1e-05  seti_boinc               __ieee754_pow
1        2.1e-05  seti_boinc               boinc_info
1        2.1e-05  seti_boinc               std::__use_cache<std::__numpunct_cache<char> >::operator()(std::locale const&) const
1        2.1e-05  seti_boinc               std::basic_ostream<char, std::char_traits<char> >& std::operator<< <std::char_traits<char> >(std::basic_ostream<char, std::char_traits<char> >&, char const*)
1        2.1e-05  seti_boinc               std::basic_stringbuf<char, std::char_traits<char>, std::allocator<char> >::str() const
1        2.1e-05  seti_boinc               std::ostreambuf_iterator<char, std::char_traits<char> > std::num_put<char, std::ostreambuf_iterator<char, std::char_traits<char> > >::_M_insert_int<long long>(std::ostreambuf_iterator<char, std::char_traits<char> >, std::ios_base&, char, long long) const
1        2.1e-05  seti_boinc               std::string::_Rep::_S_create(unsigned int, unsigned int, std::allocator<char> const&)
1        2.1e-05  seti_boinc               std::type_info::operator==(std::type_info const&) const
1        2.1e-05  seti_boinc               workunit_grp::operator=(workunit_grp const&)
1        2.1e-05  seti_boinc               x_csv_encode_char(unsigned char const*, unsigned int)
 
 
Tue Sep 20 09:44:33 CST 2011
CPU: ARM V7 PMNC, speed 0 MHz (estimated)
Counted L2_CACH_MISS events (Any cacheable miss in L2 cache) with a unit mask of 0x00 (No unit mask) count 10000
L2_CACH_MISS:1...|
  samples|      %|
------------------
     1826 92.2688 seti_boinc
	L2_CACH_MISS:1...|
	  samples|      %|
	------------------
	     1786 97.8094 seti_boinc
	       40  2.1906 [vectors] (tgid:18176 range:0xffff0000-0xffff1000)
       56  2.8297 libc-2.11.1.so
       44  2.2233 ld-2.11.1.so
       43  2.1728 bash
        3  0.1516 gawk
        2  0.1011 grep
        1  0.0505 libcrypto.so.0.9.8
        1  0.0505 libdl-2.11.1.so
        1  0.0505 libavahi-common.so.3.5.1
        1  0.0505 libavahi-core.so.6.0.1
        1  0.0505 ntpd
 
CPU: ARM V7 PMNC, speed 0 MHz (estimated)
Counted L2_CACH_MISS events (Any cacheable miss in L2 cache) with a unit mask of 0x00 (No unit mask) count 10000
samples  %        image name               symbol name
421      23.0559  seti_boinc               memset
310      16.9770  seti_boinc               analyze_pot(float*, int, ChirpFftPair_t&)
110       6.0241  seti_boinc               analysis_config::analysis_config()
104       5.6955  seti_boinc               GetFixedPoT(float*, int, int, float*, int, int)
93        5.0931  seti_boinc               splitter_config::splitter_config()
74        4.0526  seti_boinc               top_sum2(float**, PoTPlan*)
67        3.6692  seti_boinc               top_sum3(float**, PoTPlan*)
60        3.2859  seti_boinc               data_description_t::data_description_t()
58        3.1763  seti_boinc               pulse::pulse()
51        2.7930  seti_boinc               operator new(unsigned int)
50        2.7382  seti_boinc               workunit_grp::workunit_grp()
40        2.1906  [vectors] (tgid:18176 range:0xffff0000-0xffff1000) [vectors] (tgid:18176 range:0xffff0000-0xffff1000)
39        2.1358  seti_boinc               tape::tape()
37        2.0263  seti_boinc               malloc
37        2.0263  seti_boinc               subband_description_t::subband_description_t()
26        1.4239  seti_boinc               result::result()
20        1.0953  seti_boinc               T.9826
20        1.0953  seti_boinc               find_triplets(float const*, int, float, int, int)
20        1.0953  seti_boinc               workunit_header::workunit_header()
19        1.0405  seti_boinc               ReportPulseEvent(float, float, float, int, int, float, float, float*, int, int)
19        1.0405  seti_boinc               top_sum4(float**, PoTPlan*)
17        0.9310  seti_boinc               n1_32
14        0.7667  seti_boinc               recorder_config::recorder_config()
14        0.7667  seti_boinc               t_funct(int, int, int)
10        0.5476  seti_boinc               receiver_config::receiver_config()
10        0.5476  seti_boinc               top_sum5(float**, PoTPlan*)
9         0.4929  seti_boinc               FindSpikes(float*, int, int, SETI_WU_INFO&)
8         0.4381  seti_boinc               v_GetPowerSpectrum(float (*) [2], float*, int)
7         0.3834  seti_boinc               _int_malloc
6         0.3286  seti_boinc               floorf
6         0.3286  seti_boinc               spike::spike()
5         0.2738  seti_boinc               T.9822
4         0.2191  seti_boinc               find_pulse(float const*, int, float, int, int)
4         0.2191  seti_boinc               seti_analyze(ANALYSIS_STATE&)
4         0.2191  seti_boinc               sw_sum2_t31(float**, PoTPlan*)
4         0.2191  seti_boinc               time_to_ra_dec(double, double*, double*)
3         0.1643  seti_boinc               SPIKE_INFO::SPIKE_INFO()
3         0.1643  seti_boinc               __ieee754_log
3         0.1643  seti_boinc               calloc_a(unsigned int, unsigned int, unsigned int)
3         0.1643  seti_boinc               cnvt_bin_hz(int, int)
2         0.1095  seti_boinc               T.9827
2         0.1095  seti_boinc               T.9831
2         0.1095  seti_boinc               __aeabi_read_tp
2         0.1095  seti_boinc               _int_free
2         0.1095  seti_boinc               malloc_consolidate
2         0.1095  seti_boinc               std::vector<unsigned char, std::allocator<unsigned char> >::_M_fill_insert(__gnu_cxx::__normal_iterator<unsigned char*, std::vector<unsigned char, std::allocator<unsigned char> > >, unsigned int, unsigned char const&)
1         0.0548  seti_boinc               boinc_sleep(double)
1         0.0548  seti_boinc               boinc_worker_thread_cpu_time
1         0.0548  seti_boinc               calc_detection_freq(double, double, double)
1         0.0548  seti_boinc               free
1         0.0548  seti_boinc               isnanl
 
 
Tue Sep 20 09:48:30 CST 2011
CPU: ARM V7 PMNC, speed 0 MHz (estimated)
Counted L2_ACCESS events (Any access to L2 cache) with a unit mask of 0x00 (No unit mask) count 10000
  L2_ACCESS:10000|
  samples|      %|
------------------
    44407 98.7064 seti_boinc
	  L2_ACCESS:10000|
	  samples|      %|
	------------------
	    44314 99.7906 seti_boinc
	       93  0.2094 [vectors] (tgid:18176 range:0xffff0000-0xffff1000)
      193  0.4290 libc-2.11.1.so
      185  0.4112 bash
      164  0.3645 ld-2.11.1.so
       10  0.0222 gawk
        8  0.0178 libavahi-core.so.6.0.1
        5  0.0111 ntpd
        4  0.0089 oprofiled
        2  0.0044 ls
        2  0.0044 libpthread-2.11.1.so
        2  0.0044 tr
        2  0.0044 libavahi-common.so.3.5.1
        1  0.0022 dash
        1  0.0022 libgcc_s.so.1
        1  0.0022 libpam.so.0.82.2
        1  0.0022 libpopt.so.0.0.0
        1  0.0022 sudo
 
CPU: ARM V7 PMNC, speed 0 MHz (estimated)
Counted L2_ACCESS events (Any access to L2 cache) with a unit mask of 0x00 (No unit mask) count 10000
samples  %        image name               symbol name
8925     20.0982  seti_boinc               n1_32
6976     15.7092  seti_boinc               sinl
4176      9.4039  seti_boinc               analyze_pot(float*, int, ChirpFftPair_t&)
2951      6.6453  seti_boinc               GetFixedPoT(float*, int, int, float*, int, int)
2429      5.4699  seti_boinc               n1_64
2301      5.1816  seti_boinc               t1_16
1751      3.9431  seti_boinc               fftwf_cpy2d_pair
1631      3.6728  seti_boinc               apply
1299      2.9252  seti_boinc               top_sum2(float**, PoTPlan*)
1108      2.4951  seti_boinc               v_GetPowerSpectrum(float (*) [2], float*, int)
928       2.0898  seti_boinc               v_ChirpData(float (*) [2], float (*) [2], int, double, int, double)
768       1.7295  seti_boinc               top_sum3(float**, PoTPlan*)
591       1.3309  seti_boinc               t1_32
579       1.3038  seti_boinc               top_sum4(float**, PoTPlan*)
481       1.0832  seti_boinc               __ieee754_log
449       1.0111  seti_boinc               top_sum5(float**, PoTPlan*)
448       1.0088  seti_boinc               FindSpikes(float*, int, int, SETI_WU_INFO&)
435       0.9796  seti_boinc               memset
421       0.9480  seti_boinc               find_pulse(float const*, int, float, int, int)
314       0.7071  seti_boinc               sw_sum2_t31(float**, PoTPlan*)
309       0.6958  seti_boinc               rotate_sqrtn_table
276       0.6215  seti_boinc               cosl
267       0.6013  seti_boinc               _int_malloc
262       0.5900  seti_boinc               t_funct(int, int, int)
235       0.5292  seti_boinc               malloc
210       0.4729  seti_boinc               analysis_config::analysis_config()
208       0.4684  seti_boinc               __exp1
201       0.4526  seti_boinc               __ieee754_pow
195       0.4391  seti_boinc               t1_8
176       0.3963  seti_boinc               find_triplets(float const*, int, float, int, int)
173       0.3896  seti_boinc               sw_sum3_t31(float**, PoTPlan*)
149       0.3355  seti_boinc               t1_64
143       0.3220  seti_boinc               splitter_config::splitter_config()
118       0.2657  seti_boinc               _int_free
118       0.2657  seti_boinc               tape::tape()
117       0.2635  seti_boinc               workunit_grp::workunit_grp()
116       0.2612  seti_boinc               time_to_ra_dec(double, double*, double*)
99        0.2229  seti_boinc               operator new(unsigned int)
98        0.2207  seti_boinc               boinc_fraction_done
95        0.2139  seti_boinc               ReportPulseEvent(float, float, float, int, int, float, float, float*, int, int)
95        0.2139  seti_boinc               pulse::pulse()
93        0.2094  [vectors] (tgid:18176 range:0xffff0000-0xffff1000) [vectors] (tgid:18176 range:0xffff0000-0xffff1000)
88        0.1982  seti_boinc               q1_4
87        0.1959  seti_boinc               malloc_consolidate
86        0.1937  seti_boinc               GaussFit(float*, int, int)
83        0.1869  seti_boinc               result::result()
80        0.1802  seti_boinc               logl
79        0.1779  seti_boinc               subband_description_t::subband_description_t()
74        0.1666  seti_boinc               TripletProgressUnits()
73        0.1644  seti_boinc               data_description_t::data_description_t()
69        0.1554  seti_boinc               workunit_header::workunit_header()
67        0.1509  seti_boinc               recorder_config::recorder_config()
53        0.1194  seti_boinc               calc_detection_freq(double, double, double)
51        0.1148  seti_boinc               checkpoint(unsigned char)
46        0.1036  seti_boinc               ChooseGaussEvent(int, float, float, float, float, int, float, float, float*)
39        0.0878  seti_boinc               n1_16
37        0.0833  seti_boinc               cnvt_bin_hz(int, int)
33        0.0743  seti_boinc               std::vector<unsigned char, std::allocator<unsigned char> >::_M_fill_insert(__gnu_cxx::__normal_iterator<unsigned char*, std::vector<unsigned char, std::allocator<unsigned char> > >, unsigned int, unsigned char const&)
32        0.0721  seti_boinc               gaussian::gaussian()
29        0.0653  seti_boinc               t1_4
28        0.0631  seti_boinc               GaussianProgressUnits()
28        0.0631  seti_boinc               floorf
27        0.0608  seti_boinc               sw_sum5_t31(float**, PoTPlan*)
25        0.0563  seti_boinc               __divsi3
24        0.0540  seti_boinc               f_GetPeak(float*, int, int, float, float, float*)
24        0.0540  seti_boinc               f_GetTrueMean(float*, int, float, int, int)
24        0.0540  seti_boinc               seti_analyze(ANALYSIS_STATE&)
22        0.0495  seti_boinc               spike::spike()
21        0.0473  seti_boinc               free
20        0.0450  seti_boinc               T.9826
19        0.0428  seti_boinc               apply_dit
18        0.0405  seti_boinc               __aeabi_read_tp
17        0.0383  seti_boinc               PULSE_INFO::PULSE_INFO()
16        0.0360  seti_boinc               T.9822
16        0.0360  seti_boinc               floor
16        0.0360  seti_boinc               receiver_config::receiver_config()
14        0.0315  seti_boinc               SpikeProgressUnits(int)
14        0.0315  seti_boinc               fraction_done(double, double)
12        0.0270  seti_boinc               apply
11        0.0248  seti_boinc               calloc_a(unsigned int, unsigned int, unsigned int)
10        0.0225  seti_boinc               __dubcos
10        0.0225  seti_boinc               __ieee754_log10
10        0.0225  seti_boinc               __udivsi3
10        0.0225  seti_boinc               operator delete(void*)
9         0.0203  seti_boinc               apply
9         0.0203  seti_boinc               log10l
8         0.0180  seti_boinc               MFILE::MFILE()
8         0.0180  seti_boinc               sw_sum4_t31(float**, PoTPlan*)
7         0.0158  seti_boinc               fftwf_execute_dft
6         0.0135  seti_boinc               __dubsin
6         0.0135  seti_boinc               apply
6         0.0135  seti_boinc               csloww
6         0.0135  seti_boinc               csloww1
5         0.0113  seti_boinc               T.9827
5         0.0113  seti_boinc               __libc_disable_asynccancel
5         0.0113  seti_boinc               memcpy
5         0.0113  seti_boinc               nanosleep
4         0.0090  seti_boinc               PULSE_INFO::~PULSE_INFO()
4         0.0090  seti_boinc               fftwf_cpy2d_pair_co
4         0.0090  seti_boinc               lcgf(double, double)
4         0.0090  seti_boinc               powl
3         0.0068  seti_boinc               SPIKE_INFO::SPIKE_INFO()
3         0.0068  seti_boinc               T.9831
3         0.0068  seti_boinc               f_GetChiSq(float*, int, int, float, float, float*, float*)
3         0.0068  seti_boinc               fftwf_malloc
3         0.0068  seti_boinc               sincos
3         0.0068  seti_boinc               timer_handler()
3         0.0068  seti_boinc               usleep
3         0.0068  seti_boinc               worker_signal_handler(int)
2         0.0045  seti_boinc               __ieee754_fmod
2         0.0045  seti_boinc               apply
2         0.0045  seti_boinc               boinc_sleep(double)
2         0.0045  seti_boinc               isnanl
1         0.0023  seti_boinc               GAUSS_INFO::GAUSS_INFO()
1         0.0023  seti_boinc               PulseProgressUnits(double, int)
1         0.0023  seti_boinc               SPIKE_INFO::~SPIKE_INFO()
1         0.0023  seti_boinc               ____libc_enable_asynccancel_veneer
1         0.0023  seti_boinc               __default_sa_restorer_v2
1         0.0023  seti_boinc               __libc_enable_asynccancel
1         0.0023  seti_boinc               boinc_time_to_checkpoint
1         0.0023  seti_boinc               fftwf_kernel_free
1         0.0023  seti_boinc               fftwf_kernel_malloc
1         0.0023  seti_boinc               fftwf_malloc_plain
1         0.0023  seti_boinc               finite
1         0.0023  seti_boinc               float_to_uchar(float*, unsigned char*, long, float)
1         0.0023  seti_boinc               fmodl
1         0.0023  seti_boinc               free_a(void*)
1         0.0023  seti_boinc               getrusage
1         0.0023  seti_boinc               plan_PulsePoT(PoTPlan*, int, float*, int*)
1         0.0023  seti_boinc               timer_thread(void*)
1         0.0023  seti_boinc               vsnprintf
 
 
Tue Sep 20 09:52:28 CST 2011
CPU: ARM V7 PMNC, speed 0 MHz (estimated)
Counted PC_BRANCH_EXECUTED events (Any taken branch that is executed) with a unit mask of 0x00 (No unit mask) count 10000
PC_BRANCH_EXEC...|
  samples|      %|
------------------
   185396 96.8854 seti_boinc
	PC_BRANCH_EXEC...|
	  samples|      %|
	------------------
	   185101 99.8409 seti_boinc
	      295  0.1591 [vectors] (tgid:18176 range:0xffff0000-0xffff1000)
     3889  2.0323 libc-2.11.1.so
      892  0.4661 bash
	PC_BRANCH_EXEC...|
	  samples|      %|
	------------------
	      838 93.9462 bash
	       54  6.0538 [vectors] (tgid:23748 range:0xffff0000-0xffff1000)
      703  0.3674 oprofiled
      358  0.1871 ld-2.11.1.so
       25  0.0131 gawk
       21  0.0110 tr
       17  0.0089 libavahi-common.so.3.5.1
       12  0.0063 ntpd
        9  0.0047 ophelp
        7  0.0037 libpam.so.0.82.2
        6  0.0031 sudo
	PC_BRANCH_EXEC...|
	  samples|      %|
	------------------
	        4 66.6667 sudo
	        2 33.3333 [vectors] (tgid:23748 range:0xffff0000-0xffff1000)
        5  0.0026 libavahi-core.so.6.0.1
        4  0.0021 rsyslogd
	PC_BRANCH_EXEC...|
	  samples|      %|
	------------------
	        3 75.0000 rsyslogd
	        1 25.0000 [vectors] (tgid:3140 range:0xffff0000-0xffff1000)
        3  0.0016 dash
        2  0.0010 libnss_compat-2.11.1.so
        1 5.2e-04 grep
        1 5.2e-04 libdl-2.11.1.so
        1 5.2e-04 libncurses.so.5.7
        1 5.2e-04 libnss_files-2.11.1.so
        1 5.2e-04 libpopt.so.0.0.0
        1 5.2e-04 libselinux.so.1
        1 5.2e-04 sshd
 
CPU: ARM V7 PMNC, speed 0 MHz (estimated)
Counted PC_BRANCH_EXECUTED events (Any taken branch that is executed) with a unit mask of 0x00 (No unit mask) count 10000
samples  %        image name               symbol name
27828    15.0100  seti_boinc               v_ChirpData(float (*) [2], float (*) [2], int, double, int, double)
26476    14.2808  seti_boinc               cosl
25153    13.5672  seti_boinc               sinl
13154     7.0951  seti_boinc               FindSpikes(float*, int, int, SETI_WU_INFO&)
11477     6.1905  seti_boinc               f_GetTrueMean(float*, int, float, int, int)
10257     5.5325  seti_boinc               rotate_sqrtn_table
8220      4.4338  seti_boinc               sincos
6594      3.5567  seti_boinc               v_GetPowerSpectrum(float (*) [2], float*, int)
6184      3.3356  seti_boinc               GaussFit(float*, int, int)
6134      3.3086  seti_boinc               f_GetPeak(float*, int, int, float, float, float*)
4517      2.4364  seti_boinc               fftwf_cpy2d_pair
4066      2.1931  seti_boinc               floor
3391      1.8291  seti_boinc               apply
2858      1.5416  seti_boinc               find_triplets(float const*, int, float, int, int)
2340      1.2622  seti_boinc               __ieee754_log
2106      1.1359  seti_boinc               GetFixedPoT(float*, int, int, float*, int, int)
1998      1.0777  seti_boinc               powl
1948      1.0507  seti_boinc               analyze_pot(float*, int, ChirpFftPair_t&)
1910      1.0302  seti_boinc               f_GetChiSq(float*, int, int, float, float, float*, float*)
1688      0.9105  seti_boinc               float_to_uchar(float*, unsigned char*, long, float)
1604      0.8652  seti_boinc               lcgf(double, double)
1226      0.6613  seti_boinc               _int_malloc
1213      0.6543  seti_boinc               t1_4
1175      0.6338  seti_boinc               __ieee754_pow
735       0.3964  seti_boinc               find_pulse(float const*, int, float, int, int)
711       0.3835  seti_boinc               logl
581       0.3134  seti_boinc               _int_free
564       0.3042  seti_boinc               __exp1
536       0.2891  seti_boinc               free
509       0.2745  seti_boinc               n1_16
432       0.2330  seti_boinc               t1_16
431       0.2325  seti_boinc               sw_sum3_t31(float**, PoTPlan*)
419       0.2260  seti_boinc               malloc
385       0.2077  seti_boinc               __divsi3
331       0.1785  seti_boinc               fraction_done(double, double)
314       0.1694  seti_boinc               q1_4
311       0.1677  seti_boinc               time_to_ra_dec(double, double*, double*)
302       0.1629  seti_boinc               ChooseGaussEvent(int, float, float, float, float, int, float, float, float*)
301       0.1624  seti_boinc               TripletProgressUnits()
295       0.1591  [vectors] (tgid:18176 range:0xffff0000-0xffff1000) [vectors] (tgid:18176 range:0xffff0000-0xffff1000)
289       0.1559  seti_boinc               checkpoint(unsigned char)
278       0.1499  seti_boinc               csloww1
273       0.1473  seti_boinc               sw_sum5_t31(float**, PoTPlan*)
268       0.1446  seti_boinc               isnanl
254       0.1370  seti_boinc               sw_sum4_t31(float**, PoTPlan*)
227       0.1224  seti_boinc               n1_32
181       0.0976  seti_boinc               malloc_consolidate
179       0.0966  seti_boinc               __udivsi3
160       0.0863  seti_boinc               cnvt_bin_hz(int, int)
138       0.0744  seti_boinc               apply
136       0.0734  seti_boinc               GAUSS_INFO::~GAUSS_INFO()
130       0.0701  seti_boinc               t1_8
127       0.0685  seti_boinc               operator new(unsigned int)
125       0.0674  seti_boinc               analysis_config::analysis_config()
113       0.0610  seti_boinc               PulseProgressUnits(double, int)
107       0.0577  seti_boinc               operator delete(void*)
105       0.0566  seti_boinc               apply
104       0.0561  seti_boinc               apply_dit
103       0.0556  seti_boinc               receiver_config::receiver_config()
103       0.0556  seti_boinc               std::vector<unsigned char, std::allocator<unsigned char> >::_M_fill_insert(__gnu_cxx::__normal_iterator<unsigned char*, std::vector<unsigned char, std::allocator<unsigned char> > >, unsigned int, unsigned char const&)
94        0.0507  seti_boinc               gaussian::gaussian()
92        0.0496  seti_boinc               data_description_t::data_description_t()
80        0.0432  seti_boinc               memset
79        0.0426  seti_boinc               boinc_fraction_done
77        0.0415  seti_boinc               T.9826
67        0.0361  seti_boinc               workunit_grp::workunit_grp()
64        0.0345  seti_boinc               boinc_time_to_checkpoint
59        0.0318  seti_boinc               GAUSS_INFO::GAUSS_INFO()
50        0.0270  seti_boinc               __dubsin
49        0.0264  seti_boinc               GaussianProgressUnits()
43        0.0232  seti_boinc               __dubcos
43        0.0232  seti_boinc               apply_dif
41        0.0221  seti_boinc               memcpy
39        0.0210  seti_boinc               n1_64
37        0.0200  seti_boinc               calc_detection_freq(double, double, double)
37        0.0200  seti_boinc               recorder_config::recorder_config()
32        0.0173  seti_boinc               apply
29        0.0156  seti_boinc               MFILE::~MFILE()
29        0.0156  seti_boinc               result::result()
25        0.0135  seti_boinc               subband_description_t::subband_description_t()
23        0.0124  seti_boinc               T.9822
23        0.0124  seti_boinc               finite
21        0.0113  seti_boinc               csloww
20        0.0108  seti_boinc               MFILE::MFILE()
19        0.0102  seti_boinc               T.9831
19        0.0102  seti_boinc               splitter_config::splitter_config()
17        0.0092  seti_boinc               T.9827
16        0.0086  seti_boinc               memmove
15        0.0081  seti_boinc               t1_32
11        0.0059  seti_boinc               fftwf_cpy2d_pair_co
11        0.0059  seti_boinc               workunit_header::workunit_header()
10        0.0054  seti_boinc               __docos
9         0.0049  seti_boinc               apply
9         0.0049  seti_boinc               tape::tape()
5         0.0027  seti_boinc               SPIKE_INFO::~SPIKE_INFO()
5         0.0027  seti_boinc               t1_64
2         0.0011  seti_boinc               SpikeProgressUnits(int)
2         0.0011  seti_boinc               __aeabi_read_tp
2         0.0011  seti_boinc               __ieee754_fmod
2         0.0011  seti_boinc               __ieee754_log10
2         0.0011  seti_boinc               isinfl
2         0.0011  seti_boinc               seti_analyze(ANALYSIS_STATE&)
1        5.4e-04  seti_boinc               SPIKE_INFO::SPIKE_INFO()
1        5.4e-04  seti_boinc               ____libc_enable_asynccancel_veneer
1        5.4e-04  seti_boinc               __default_sa_restorer_v2
1        5.4e-04  seti_boinc               __libc_enable_asynccancel
1        5.4e-04  seti_boinc               boinc_sleep(double)
1        5.4e-04  seti_boinc               fftwf_execute_dft
1        5.4e-04  seti_boinc               getrusage
1        5.4e-04  seti_boinc               log10l
1        5.4e-04  seti_boinc               timer_thread(void*)
1        5.4e-04  seti_boinc               usleep
1        5.4e-04  seti_boinc               worker_signal_handler(int)
 
 
Tue Sep 20 09:56:25 CST 2011
CPU: ARM V7 PMNC, speed 0 MHz (estimated)
Counted PC_BRANCH_MIS_PRED events (Branch mispredicted or not predicted. Counts pipeline flushes because of misprediction) with a unit mask of 0x00 (No unit mask) count 10000
PC_BRANCH_MIS_...|
  samples|      %|
------------------
     6885 91.1800 seti_boinc
	PC_BRANCH_MIS_...|
	  samples|      %|
	------------------
	     6873 99.8257 seti_boinc
	       12  0.1743 [vectors] (tgid:18176 range:0xffff0000-0xffff1000)
      358  4.7411 libc-2.11.1.so
      166  2.1984 bash
      118  1.5627 ld-2.11.1.so
        7  0.0927 libavahi-common.so.3.5.1
        4  0.0530 libavahi-core.so.6.0.1
        3  0.0397 gawk
        2  0.0265 ophelp
        2  0.0265 sudo
	PC_BRANCH_MIS_...|
	  samples|      %|
	------------------
	        1 50.0000 sudo
	        1 50.0000 [vectors] (tgid:24977 range:0xffff0000-0xffff1000)
        2  0.0265 rsyslogd
        1  0.0132 libpam.so.0.82.2
        1  0.0132 libpthread-2.11.1.so
        1  0.0132 tr
        1  0.0132 ntpd
 
CPU: ARM V7 PMNC, speed 0 MHz (estimated)
Counted PC_BRANCH_MIS_PRED events (Branch mispredicted or not predicted. Counts pipeline flushes because of misprediction) with a unit mask of 0x00 (No unit mask) count 10000
samples  %        image name               symbol name
1826     26.5214  seti_boinc               cosl
1428     20.7407  seti_boinc               sinl
550       7.9884  seti_boinc               f_GetTrueMean(float*, int, float, int, int)
227       3.2970  seti_boinc               sw_sum4_t31(float**, PoTPlan*)
220       3.1954  seti_boinc               sw_sum2_t31(float**, PoTPlan*)
204       2.9630  seti_boinc               sw_sum3_t31(float**, PoTPlan*)
171       2.4837  seti_boinc               _int_malloc
160       2.3239  seti_boinc               __ieee754_log
155       2.2513  seti_boinc               analyze_pot(float*, int, ChirpFftPair_t&)
142       2.0625  seti_boinc               find_triplets(float const*, int, float, int, int)
141       2.0479  seti_boinc               powl
138       2.0044  seti_boinc               GaussFit(float*, int, int)
130       1.8882  seti_boinc               sw_sum5_t31(float**, PoTPlan*)
118       1.7139  seti_boinc               __divsi3
95        1.3798  seti_boinc               find_pulse(float const*, int, float, int, int)
87        1.2636  seti_boinc               __ieee754_pow
74        1.0748  seti_boinc               ChooseGaussEvent(int, float, float, float, float, int, float, float, float*)
67        0.9731  seti_boinc               lcgf(double, double)
65        0.9441  seti_boinc               free
60        0.8715  seti_boinc               checkpoint(unsigned char)
47        0.6826  seti_boinc               GetFixedPoT(float*, int, int, float*, int, int)
41        0.5955  seti_boinc               float_to_uchar(float*, unsigned char*, long, float)
37        0.5374  seti_boinc               __udivsi3
34        0.4938  seti_boinc               t1_4
32        0.4648  seti_boinc               apply_dit
32        0.4648  seti_boinc               malloc_consolidate
31        0.4503  seti_boinc               _int_free
31        0.4503  seti_boinc               apply
26        0.3776  seti_boinc               apply
26        0.3776  seti_boinc               f_GetChiSq(float*, int, int, float, float, float*, float*)
26        0.3776  seti_boinc               malloc
21        0.3050  seti_boinc               logl
20        0.2905  seti_boinc               memset
19        0.2760  seti_boinc               GaussianProgressUnits()
19        0.2760  seti_boinc               csloww1
17        0.2469  seti_boinc               TripletProgressUnits()
17        0.2469  seti_boinc               n1_16
16        0.2324  seti_boinc               PulseProgressUnits(double, int)
16        0.2324  seti_boinc               apply_dif
15        0.2179  seti_boinc               __dubcos
15        0.2179  seti_boinc               apply
15        0.2179  seti_boinc               n1_32
14        0.2033  seti_boinc               time_to_ra_dec(double, double*, double*)
13        0.1888  seti_boinc               v_ChirpData(float (*) [2], float (*) [2], int, double, int, double)
12        0.1743  [vectors] (tgid:18176 range:0xffff0000-0xffff1000) [vectors] (tgid:18176 range:0xffff0000-0xffff1000)
12        0.1743  seti_boinc               memcpy
11        0.1598  seti_boinc               cnvt_bin_hz(int, int)
9         0.1307  seti_boinc               FindSpikes(float*, int, int, SETI_WU_INFO&)
9         0.1307  seti_boinc               boinc_time_to_checkpoint
9         0.1307  seti_boinc               data_description_t::data_description_t()
9         0.1307  seti_boinc               operator delete(void*)
9         0.1307  seti_boinc               workunit_header::workunit_header()
8         0.1162  seti_boinc               __dubsin
8         0.1162  seti_boinc               gaussian::gaussian()
7         0.1017  seti_boinc               __exp1
7         0.1017  seti_boinc               result::result()
7         0.1017  seti_boinc               t1_16
6         0.0871  seti_boinc               csloww
6         0.0871  seti_boinc               floor
6         0.0871  seti_boinc               splitter_config::splitter_config()
6         0.0871  seti_boinc               subband_description_t::subband_description_t()
5         0.0726  seti_boinc               GAUSS_INFO::~GAUSS_INFO()
5         0.0726  seti_boinc               apply
5         0.0726  seti_boinc               apply
5         0.0726  seti_boinc               sincos
5         0.0726  seti_boinc               std::vector<unsigned char, std::allocator<unsigned char> >::_M_fill_insert(__gnu_cxx::__normal_iterator<unsigned char*, std::vector<unsigned char, std::allocator<unsigned char> > >, unsigned int, unsigned char const&)
5         0.0726  seti_boinc               workunit_grp::workunit_grp()
4         0.0581  seti_boinc               GAUSS_INFO::GAUSS_INFO()
4         0.0581  seti_boinc               fftwf_cpy2d_pair
4         0.0581  seti_boinc               q1_4
4         0.0581  seti_boinc               rotate_sqrtn_table
4         0.0581  seti_boinc               seti_analyze(ANALYSIS_STATE&)
3         0.0436  seti_boinc               MFILE::MFILE()
3         0.0436  seti_boinc               __docos
3         0.0436  seti_boinc               fraction_done(double, double)
3         0.0436  seti_boinc               memmove
3         0.0436  seti_boinc               n1_64
3         0.0436  seti_boinc               operator new(unsigned int)
3         0.0436  seti_boinc               receiver_config::receiver_config()
3         0.0436  seti_boinc               timer_handler()
3         0.0436  seti_boinc               v_GetPowerSpectrum(float (*) [2], float*, int)
2         0.0290  seti_boinc               calc_detection_freq(double, double, double)
2         0.0290  seti_boinc               dtime()
2         0.0290  seti_boinc               fftwf_cpy2d_pair_co
2         0.0290  seti_boinc               isnanl
2         0.0290  seti_boinc               recorder_config::recorder_config()
2         0.0290  seti_boinc               t1_32
2         0.0290  seti_boinc               t1_8
2         0.0290  seti_boinc               worker_signal_handler(int)
1         0.0145  seti_boinc               __ieee754_fmod
1         0.0145  seti_boinc               __libc_disable_asynccancel
1         0.0145  seti_boinc               __mpn_divrem
1         0.0145  seti_boinc               analysis_config::analysis_config()
1         0.0145  seti_boinc               boinc_fraction_done
1         0.0145  seti_boinc               boinc_info
1         0.0145  seti_boinc               boinc_sleep(double)
1         0.0145  seti_boinc               f_GetPeak(float*, int, int, float, float, float*)
1         0.0145  seti_boinc               gettimeofday
1         0.0145  seti_boinc               hack_digit.11765
1         0.0145  seti_boinc               t1_64
1         0.0145  seti_boinc               tape::tape()
1         0.0145  seti_boinc               usleep
```

# Intel Nehalem (Core i3 330M) #
## Oprofile Core i3 Events ##
```
oprofile: available events for CPU type "Intel Architectural Perfmon"
CPU_CLK_UNHALTED: (counter: all)
	Clock cycles when not halted (min count: 6000) 
INST_RETIRED: (counter: all)
	number of instructions retired (min count: 6000) 
LLC_MISSES: (counter: all)
	Last level cache demand requests from this core that missed the LLC (min count: 6000) 
	Unit masks (default 0x41)
	----------
	0x41: No unit mask 
LLC_REFS: (counter: all)
	Last level cache demand requests from this core (min count: 6000) 
	Unit masks (default 0x4f)
	----------
	0x4f: No unit mask 
BR_INST_RETIRED: (counter: all)
	number of branch instructions retired (min count: 500) 
BR_MISS_PRED_RETIRED: (counter: all)
	number of mispredicted branches retired (precise) (min count: 500) 
```
### Event Data on Core i3 ###

```
CPU: Intel Architectural Perfmon, speed 2130 MHz (estimated)
Counted CPU_CLK_UNHALTED events (Clock cycles when not halted) with a unit mask of 0x00 (No unit mask) count 10000
CPU_CLK_UNHALT...|
  samples|      %|
------------------
  8585025 95.0181 seti_boinc
   192488  2.1304 oprofiled
    26774  0.2963 libc-2.12.1.so
    25846  0.2861 python2.6
    25324  0.2803 libcairo.so.2.11000.0
    21048  0.2330 libglib-2.0.so.0.2600.0
    18191  0.2013 Xorg
    13028  0.1442 libdrm_intel.so.1.0.0
    12832  0.1420 libpixman-1.so.0.18.4
    11352  0.1256 chromium-browser
	CPU_CLK_UNHALT...|
	  samples|      %|
	------------------
	    11034 97.1987 chromium-browser
	      152  1.3390 anon (tgid:4700 range:0xdaf000-0xe13000)
	       95  0.8369 anon (tgid:4700 range:0x71225000-0x71245000)
	       30  0.2643 anon (tgid:4700 range:0x5ef9e000-0x5efbe000)
	       24  0.2114 anon (tgid:4700 range:0x2fe0b000-0x2fe2b000)
	       12  0.1057 anon (tgid:4700 range:0x2fff5000-0x30015000)
	        5  0.0440 anon (tgid:4700 range:0xe1a000-0xe43000)
    10073  0.1115 libpthread-2.12.1.so
     9292  0.1028 libgobject-2.0.so.0.2600.0
     7246  0.0802 libgdk-x11-2.0.so.0.2200.0
     6996  0.0774 intel_drv.so
     6392  0.0707 perl
     6119  0.0677 no-vmlinux
     5951  0.0659 ld-2.12.1.so
     5203  0.0576 i965_dri.so
     4900  0.0542 libgtk-x11-2.0.so.0.2200.0
     4677  0.0518 bash
     4224  0.0468 libdbus-1.so.3.5.2
     3646  0.0404 libX11.so.6.3.0
     2947  0.0326 mysqld
     2216  0.0245 libxcb.so.1.1.0
     1896  0.0210 compiz
     1627  0.0180 libvte.so.9.2600.0
     1503  0.0166 dbus-daemon
     1202  0.0133 libpango-1.0.so.0.2800.1
     1125  0.0125 libmurrine.so
     1105  0.0122 libfade.so
      889  0.0098 libm-2.12.1.so
      779  0.0086 libgthread-2.0.so.0.2600.0
      756  0.0084 libgdk_pixbuf-2.0.so.0.2200.0
      679  0.0075 libpyglib-2.0-python2.6.so.0.0.0
      673  0.0074 libpangoft2-1.0.so.0.2800.1
      575  0.0064 libXrender.so.1.3.0
      564  0.0062 _glib.so
      531  0.0059 libfb.so
      514  0.0057 libGL.so.1.2
      416  0.0046 libanimation.so
      410  0.0045 evdev_drv.so
      396  0.0044 librt-2.12.1.so
      343  0.0038 libdecoration.so
      330  0.0037 libdbus-glib-1.so.2.1.0
      310  0.0034 libexpo.so
      285  0.0032 rsyslogd
      280  0.0031 libextmod.so
      249  0.0028 _gtk.so
      230  0.0025 libgio-2.0.so.0.2600.0
      228  0.0025 libdrm.so.2.4.0
      221  0.0024 gawk
      203  0.0022 libscale.so
      200  0.0022 libwall.so
      188  0.0021 libXfixes.so.3.1.0
      179  0.0020 libstaticswitcher.so
      170  0.0019 libpangocairo-1.0.so.0.2800.1
      169  0.0019 libgvfscommon.so.0.0.0
      164  0.0018 libavahi-common.so.3.5.2
      164  0.0018 _gobject.so
      149  0.0016 libORBit-2.so.0.1.0
      143  0.0016 libstdc++.so.6.0.14
      138  0.0015 libezoom.so
      136  0.0015 libavahi-core.so.7.0.0
      135  0.0015 libdri2.so
      130  0.0014 libresize.so
      130  0.0014 libgnome-keyring.so.0.1.1
      124  0.0014 libudev.so.0.9.1
      124  0.0014 libresizeinfo.so
      109  0.0012 libwnck-1.so.22.3.30
      106  0.0012 libgcc_s.so.1
      106  0.0012 libworkarounds.so
      103  0.0011 libscaleaddon.so
       96  0.0011 libmove.so
       91  0.0010 libmysqlclient.so.16.0.0
       89 9.9e-04 libstartup-notification-1.so.0.0.0
       86 9.5e-04 vmware-usbarbitrator
       86 9.5e-04 libcompizconfig.so.0.0.0
       74 8.2e-04 libsvg.so
       71 7.9e-04 apache2
       69 7.6e-04 libXdamage.so.1.1.0
       66 7.3e-04 libneg.so
       63 7.0e-04 dash
       62 6.9e-04 libsession.so
       59 6.5e-04 libgtksourceview-2.0.so.0.0.0
       57 6.3e-04 libmetacity-private.so.0.0.0
       56 6.2e-04 libapr-1.so.0.4.2
       55 6.1e-04 grep
       52 5.8e-04 libvpswitch.so
       52 5.8e-04 libXext.so.6.4.0
       46 5.1e-04 NetworkManager
       45 5.0e-04 libplace.so
       44 4.9e-04 sudo
       40 4.4e-04 libpam.so.0.82.2
       37 4.1e-04 libregex.so
       35 3.9e-04 libcrypto.so.0.9.8
       32 3.5e-04 ophelp
       32 3.5e-04 libxklavier.so.16.0.0
       31 3.4e-04 libpcre.so.3.12.1
       29 3.2e-04 libccp.so
       29 3.2e-04 libgconf-2.so.4.1.5
       29 3.2e-04 libusbmuxd.so.1.0.4
       25 2.8e-04 gnome-panel
       25 2.8e-04 pango-basic-fc.so
       24 2.7e-04 libsnap.so
       22 2.4e-04 DBI.so
       18 2.0e-04 libgconf.so
       18 2.0e-04 libXi.so.6.1.0
       18 2.0e-04 mysql.so
       17 1.9e-04 libdl-2.12.1.so
       17 1.9e-04 libresolv-2.12.1.so
       17 1.9e-04 libpulse-mainloop-glib.so.0.0.4
       16 1.8e-04 libpixmap.so
       15 1.7e-04 wpa_supplicant
       15 1.7e-04 gtk-window-decorator
       15 1.7e-04 libbonobo-2.so.0.0.0
       14 1.5e-04 gedit
       14 1.5e-04 udisks-daemon
       13 1.4e-04 libkeyboard.so
       12 1.3e-04 gconfd-2
       11 1.2e-04 imklog.so
       10 1.1e-04 libncurses.so.5.7
       10 1.1e-04 libpopt.so.0.0.0
       10 1.1e-04 gnome-terminal
       10 1.1e-04 libmouse.so
        9 1.0e-04 liba11y-keyboard.so
        8 8.9e-05 _dbus_bindings.so
        7 7.7e-05 ls
        7 7.7e-05 rm
        6 6.6e-05 libnss_compat-2.12.1.so
        6 6.6e-05 libnss_files-2.12.1.so
        6 6.6e-05 gnome-power-manager
        6 6.6e-05 ssh-agent
        6 6.6e-05 libmousepoll.so
        6 6.6e-05 libcanberra-gtk-module.so
        6 6.6e-05 libbonoboui-2.so.0.0.0
        6 6.6e-05 libnm-util.so.1.6.0
        6 6.6e-05 libpanel-applet-2.so.0.2.68
        6 6.6e-05 nullmailer-send
        5 5.5e-05 libselinux.so.1
        5 5.5e-05 seq
        5 5.5e-05 libnl.so.1.1
        4 4.4e-05 libnss_dns-2.12.1.so
        4 4.4e-05 libsyncdaemon-1.0.so.1.0.0
        4 4.4e-05 smtp
        4 4.4e-05 imuxsock.so
        4 4.4e-05 cron
        3 3.3e-05 libnss_mdns4_minimal.so.2
        3 3.3e-05 pam_limits.so
        3 3.3e-05 libtext.so
        3 3.3e-05 libkeybindings.so
        3 3.3e-05 libmedia-keys.so
        3 3.3e-05 libupower-glib.so.1.0.1
        2 2.2e-05 cat
        2 2.2e-05 sleep
        2 2.2e-05 libnss_mdns4.so.2
        2 2.2e-05 id
        2 2.2e-05 tr
        2 2.2e-05 libgnomecompat.so
        2 2.2e-05 libimgjpeg.so
        2 2.2e-05 clock-applet
        2 2.2e-05 wnck-applet
        2 2.2e-05 libhousekeeping.so
        2 2.2e-05 libxrandr.so
        2 2.2e-05 libdecoration.so.0.0.0
        2 2.2e-05 libgnome-desktop-2.so.17.1.4
        2 2.2e-05 libnss3.so
        2 2.2e-05 notify-osd
        2 2.2e-05 avahi-daemon
        1 1.1e-05 libnsl-2.12.1.so
        1 1.1e-05 libnss_nis-2.12.1.so
        1 1.1e-05 pam_gnome_keyring.so
        1 1.1e-05 pam_unix.so
        1 1.1e-05 dirname
        1 1.1e-05 expr
        1 1.1e-05 nm-applet
        1 1.1e-05 update-notifier
        1 1.1e-05 vmnet-bridge
        1 1.1e-05 gnome-settings-daemon
        1 1.1e-05 im-ibus.so
        1 1.1e-05 libck-connector.so.0.0.0
        1 1.1e-05 libfreetype.so.6.6.0
        1 1.1e-05 libplc4.so
        1 1.1e-05 libssl3.so
        1 1.1e-05 libtalloc.so.2.0.1
        1 1.1e-05 crypto.so
        1 1.1e-05 rtkit-daemon
 
CPU: Intel Architectural Perfmon, speed 2130 MHz (estimated)
Counted CPU_CLK_UNHALTED events (Clock cycles when not halted) with a unit mask of 0x00 (No unit mask) count 10000
samples  %        symbol name
1169889  13.5610  f_GetChiSq(float*, int, int, float, float, float*, float*)
890831   10.3262  GaussFit(float*, int, int)
773521    8.9664  GetFixedPoT(float*, int, int, float*, int, int)
734503    8.5141  analyze_pot(float*, int, ChirpFftPair_t&)
696438    8.0729  lcgf(double, double)
452407    5.2442  f_GetTrueMean(float*, int, float, int, int)
434401    5.0354  f_GetPeak(float*, int, int, float, float, float*)
376546    4.3648  n1bv_128
359234    4.1641  sse2_ChirpData_ak(float (*) [2], float (*) [2], int, double, int, double)
251436    2.9146  __ieee754_log
239902    2.7809  float_to_uchar(float*, unsigned char*, long, float)
167098    1.9369  FindSpikes(float*, int, int, SETI_WU_INFO&)
154125    1.7866  find_pulse(float const*, int, float, int, int)
151763    1.7592  __ieee754_pow
140399    1.6275  find_triplets(float const*, int, float, int, int)
127515    1.4781  foldArrayBy2LO(float**, PoTPlan*)
101743    1.1794  t2bv_64
77183     0.8947  isnan
76157     0.8828  t1bv_8
74230     0.8605  foldArrayBy4(float**, PoTPlan*)
73435     0.8512  foldArrayBy5LO(float**, PoTPlan*)
71130     0.8245  v_GetPowerSpectrum(float (*) [2], float*, int)
69448     0.8050  t1bv_16
66449     0.7703  malloc
61319     0.7108  _int_malloc
59979     0.6953  foldArrayBy3(float**, PoTPlan*)
58931     0.6831  free
54740     0.6345  foldArrayBy3LO(float**, PoTPlan*)
51471     0.5966  n2bv_64
50719     0.5879  foldArrayBy4LO(float**, PoTPlan*)
47131     0.5463  foldArrayBy5(float**, PoTPlan*)
46922     0.5439  pow
41411     0.4800  PulseProgressUnits(double, int)
40554     0.4701  foldArrayBy2A(float**, PoTPlan*)
37605     0.4359  log
27315     0.3166  _int_free
26836     0.3111  fraction_done(double, double)
24169     0.2802  t1bv_32
22354     0.2591  ChooseGaussEvent(int, float, float, float, float, int, float, float, float*)
21185     0.2456  time_to_ra_dec(double, double*, double*)
16254     0.1884  malloc_consolidate
15924     0.1846  foldArrayBy2AL(float**, PoTPlan*)
13376     0.1551  floor
11667     0.1352  t2bv_32
8980      0.1041  checkpoint(unsigned char)
8927      0.1035  operator new(unsigned int)
8481      0.0983  t2bv_16
7739      0.0897  analysis_config::analysis_config()
7566      0.0877  gaussian::gaussian()
7111      0.0824  operator delete(void*)
7071      0.0820  boinc_fraction_done
6462      0.0749  n2bv_32
6442      0.0747  finite
6088      0.0706  t_funct(int, int, int)
6019      0.0698  workunit_grp::workunit_grp()
5915      0.0686  result::result()
5764      0.0668  TripletProgressUnits()
5498      0.0637  cnvt_bin_hz(int, int)
5133      0.0595  __i686.get_pc_thunk.bx
4600      0.0533  std::vector<unsigned char, std::allocator<unsigned char> >::_M_fill_insert(__gnu_cxx::__normal_iterator<unsigned char*, std::vector<unsigned char, std::allocator<unsigned char> > >, unsigned int, unsigned char const&)
4293      0.0498  calc_detection_freq(double, double, double)
4278      0.0496  workunit_header::workunit_header()
3576      0.0415  receiver_config::receiver_config()
3273      0.0379  data_description_t::data_description_t()
3272      0.0379  __memmove_ssse3_rep
3193      0.0370  splitter_config::splitter_config()
3120      0.0362  GaussianProgressUnits()
3087      0.0358  GAUSS_INFO::~GAUSS_INFO()
2820      0.0327  __memset_sse2_rep
2540      0.0294  tape::tape()
2329      0.0270  subband_description_t::subband_description_t()
2252      0.0261  T.9614
2211      0.0256  MFILE::MFILE()
2104      0.0244  MFILE::~MFILE()
1602      0.0186  T.9615
1363      0.0158  recorder_config::recorder_config()
1258      0.0146  GAUSS_INFO::GAUSS_INFO()
1253      0.0145  boinc_time_to_checkpoint
1183      0.0137  T.9610
1112      0.0129  T.9619
1044      0.0121  apply
1002      0.0116  seti_analyze(ANALYSIS_STATE&)
910       0.0105  t2bv_8
885       0.0103  apply_dit
796       0.0092  ReportPulseEvent(float, float, float, int, int, float, float, float*, int, int)
634       0.0073  __ieee754_log10
491       0.0057  apply
445       0.0052  apply
400       0.0046  SpikeProgressUnits(int)
356       0.0041  fftwf_execute_dft
345       0.0040  spike::spike()
191       0.0022  SPIKE_INFO::SPIKE_INFO()
180       0.0021  t1bv_4
174       0.0020  _int_memalign
164       0.0019  log10
137       0.0016  __nanosleep_nocancel
133       0.0015  timer_handler()
126       0.0015  memalign
118       0.0014  SPIKE_INFO::~SPIKE_INFO()
116       0.0013  boinc_sleep(double)
92        0.0011  pulse::pulse()
78       9.0e-04  _dl_sysinfo_int80
51       5.9e-04  __libc_disable_asynccancel
42       4.9e-04  floorf
41       4.8e-04  gettimeofday
38       4.4e-04  PULSE_INFO::~PULSE_INFO()
35       4.1e-04  dtime()
33       3.8e-04  usleep
28       3.2e-04  PULSE_INFO::PULSE_INFO()
26       3.0e-04  GetPulsePoTLen(long, int*, int*)
22       2.6e-04  plan_PulsePoT(PoTPlan*, int, float*, int*)
20       2.3e-04  invert_lcgf(float, float, float)
19       2.2e-04  fftwf_malloc
19       2.2e-04  malloc_a(unsigned int, unsigned int)
18       2.1e-04  calloc_a(unsigned int, unsigned int, unsigned int)
18       2.1e-04  fftwf_kernel_malloc
15       1.7e-04  free_a(void*)
12       1.4e-04  nanosleep
11       1.3e-04  fftwf_kernel_free
9        1.0e-04  fftwf_free
6        7.0e-05  result_group_start()
5        5.8e-05  ChirpProgressUnits()
5        5.8e-05  boinc_worker_thread_cpu_time
3        3.5e-05  __libc_enable_asynccancel
3        3.5e-05  boinc_info
3        3.5e-05  timer_thread(void*)
2        2.3e-05  __restore
1        1.2e-05  getrusage

CPU: Intel Architectural Perfmon, speed 933 MHz (estimated)
Counted INST_RETIRED events (number of instructions retired) with a unit mask of 0x00 (No unit mask) count 10000
INST_RETIRED:1...|
  samples|      %|
------------------
  8651508 89.7130 seti_boinc
   520800  5.4005 chromium-browser
	INST_RETIRED:1...|
	  samples|      %|
	------------------
	   520708 99.9823 chromium-browser
	       42  0.0081 anon (tgid:4700 range:0xdaf000-0xe13000)
	       27  0.0052 anon (tgid:4700 range:0x71225000-0x71245000)
	       11  0.0021 anon (tgid:4700 range:0xe1a000-0xe43000)
	        4 7.7e-04 anon (tgid:4700 range:0x2fe0b000-0x2fe2b000)
	        4 7.7e-04 anon (tgid:4700 range:0x5a499000-0x5a4b9000)
	        3 5.8e-04 anon (tgid:4700 range:0x5c05f000-0x5c07f000)
	        1 1.9e-04 anon (tgid:4700 range:0x32975000-0x32995000)
   284157  2.9466 oprofiled
    24212  0.2511 libc-2.12.1.so
    22696  0.2353 libpixman-1.so.0.18.4
    18579  0.1927 libpthread-2.12.1.so
    16921  0.1755 libgobject-2.0.so.0.2600.0
    15789  0.1637 libglib-2.0.so.0.2600.0
    15730  0.1631 libcairo.so.2.11000.0
    11627  0.1206 libmurrine.so
     9953  0.1032 Xorg
     9711  0.1007 libdrm_intel.so.1.0.0
     5210  0.0540 bash
     4580  0.0475 python2.6
     3850  0.0399 libgtk-x11-2.0.so.0.2200.0
     3407  0.0353 ld-2.12.1.so
     3171  0.0329 libgdk-x11-2.0.so.0.2200.0
     2280  0.0236 intel_drv.so
     1928  0.0200 mysqld
     1904  0.0197 libstdc++.so.6.0.14
     1613  0.0167 libdbus-1.so.3.5.2
     1474  0.0153 dbus-daemon
     1138  0.0118 i965_dri.so
     1020  0.0106 libX11.so.6.3.0
      981  0.0102 libm-2.12.1.so
      852  0.0088 no-vmlinux
      811  0.0084 libpangoft2-1.0.so.0.2800.1
      794  0.0082 libvte.so.9.2600.0
      779  0.0081 perl
      626  0.0065 libxcb.so.1.1.0
      571  0.0059 libfreebl3.so
      521  0.0054 libgthread-2.0.so.0.2600.0
      484  0.0050 compiz
      432  0.0045 libgdk_pixbuf-2.0.so.0.2200.0
      244  0.0025 libpango-1.0.so.0.2800.1
      197  0.0020 gawk
      173  0.0018 libgcc_s.so.1
      152  0.0016 libfreetype.so.6.6.0
      134  0.0014 libavahi-common.so.3.5.2
      133  0.0014 evdev_drv.so
      132  0.0014 rsyslogd
      124  0.0013 librt-2.12.1.so
      116  0.0012 libXrender.so.1.3.0
      101  0.0010 libexpo.so
       99  0.0010 libfade.so
       91 9.4e-04 libanimation.so
       79 8.2e-04 libgvfscommon.so.0.0.0
       76 7.9e-04 libmysqlclient.so.16.0.0
       75 7.8e-04 libextmod.so
       70 7.3e-04 libdbus-glib-1.so.2.1.0
       69 7.2e-04 libscale.so
       64 6.6e-04 libdecoration.so
       63 6.5e-04 libfb.so
       62 6.4e-04 libORBit-2.so.0.1.0
       59 6.1e-04 libpyglib-2.0-python2.6.so.0.0.0
       58 6.0e-04 _glib.so
       52 5.4e-04 libgio-2.0.so.0.2600.0
       51 5.3e-04 libGL.so.1.2
       50 5.2e-04 libavahi-core.so.7.0.0
       47 4.9e-04 libstaticswitcher.so
       39 4.0e-04 grep
       39 4.0e-04 libmove.so
       37 3.8e-04 libresize.so
       35 3.6e-04 libcrypto.so.0.9.8
       35 3.6e-04 libpam.so.0.82.2
       34 3.5e-04 libdrm.so.2.4.0
       31 3.2e-04 dash
       30 3.1e-04 libgcrypt.so.11.5.3
       29 3.0e-04 ophelp
       29 3.0e-04 libwall.so
       27 2.8e-04 librsvg-2.so.2.32.0
       25 2.6e-04 libwnck-1.so.22.3.30
       24 2.5e-04 sudo
       24 2.5e-04 libpangocairo-1.0.so.0.2800.1
       23 2.4e-04 libsvg.so
       22 2.3e-04 NetworkManager
       18 1.9e-04 libpcre.so.3.12.1
       18 1.9e-04 libXfixes.so.3.1.0
       18 1.9e-04 libnm-util.so.1.6.0
       17 1.8e-04 libxml2.so.2.7.7
       16 1.7e-04 libmetacity-private.so.0.0.0
       14 1.5e-04 libezoom.so
       13 1.3e-04 libscaleaddon.so
       13 1.3e-04 libsoftokn3.so
       12 1.2e-04 libdri2.so
       11 1.1e-04 libresolv-2.12.1.so
       11 1.1e-04 wpa_supplicant
       11 1.1e-04 libXdamage.so.1.1.0
       10 1.0e-04 libstartup-notification-1.so.0.0.0
       10 1.0e-04 pango-basic-fc.so
        9 9.3e-05 libsession.so
        9 9.3e-05 libworkarounds.so
        8 8.3e-05 libudev.so.0.9.1
        7 7.3e-05 libnss_files-2.12.1.so
        7 7.3e-05 im-ibus.so
        7 7.3e-05 libXext.so.6.4.0
        7 7.3e-05 _gtk.so
        6 6.2e-05 libxklavier.so.16.0.0
        5 5.2e-05 ls
        5 5.2e-05 libresizeinfo.so
        5 5.2e-05 libgnome-keyring.so.0.1.1
        5 5.2e-05 mysql.so
        5 5.2e-05 _gobject.so
        4 4.1e-05 vmware-usbarbitrator
        4 4.1e-05 libneg.so
        4 4.1e-05 libregex.so
        4 4.1e-05 libsnap.so
        4 4.1e-05 libgconf-2.so.4.1.5
        4 4.1e-05 libnss3.so
        4 4.1e-05 imklog.so
        3 3.1e-05 gnome-panel
        3 3.1e-05 gnome-terminal
        3 3.1e-05 libpixmap.so
        3 3.1e-05 libapr-1.so.0.4.2
        3 3.1e-05 libnssutil3.so
        3 3.1e-05 libpulse-mainloop-glib.so.0.0.4
        3 3.1e-05 winbindd
        2 2.1e-05 cat
        2 2.1e-05 libdl-2.12.1.so
        2 2.1e-05 libnss_compat-2.12.1.so
        2 2.1e-05 libnss_dns-2.12.1.so
        2 2.1e-05 libpopt.so.0.0.0
        2 2.1e-05 libccp.so
        2 2.1e-05 libplace.so
        2 2.1e-05 libvpswitch.so
        2 2.1e-05 liba11y-keyboard.so
        2 2.1e-05 libkeyboard.so
        2 2.1e-05 libcompizconfig.so.0.0.0
        2 2.1e-05 libnspr4.so
        2 2.1e-05 DBI.so
        2 2.1e-05 _dbus_bindings.so
        1 1.0e-05 mkdir
        1 1.0e-05 rm
        1 1.0e-05 libnss_mdns4.so.2
        1 1.0e-05 gnome-screensaver
        1 1.0e-05 gtk-window-decorator
        1 1.0e-05 seq
        1 1.0e-05 tr
        1 1.0e-05 apache2
        1 1.0e-05 libdbus.so
        1 1.0e-05 libmousepoll.so
        1 1.0e-05 libmedia-keys.so
        1 1.0e-05 libmouse.so
        1 1.0e-05 libXi.so.6.1.0
        1 1.0e-05 libbonobo-2.so.0.0.0
        1 1.0e-05 gconfd-2
        1 1.0e-05 libnl.so.1.1
        1 1.0e-05 libpanel-applet-2.so.0.2.68
        1 1.0e-05 libplds4.so
        1 1.0e-05 notify-osd
        1 1.0e-05 smtp
        1 1.0e-05 _heapq.so
        1 1.0e-05 imuxsock.so
        1 1.0e-05 libglx.so
        1 1.0e-05 nullmailer-send
 
CPU: Intel Architectural Perfmon, speed 933 MHz (estimated)
Counted INST_RETIRED events (number of instructions retired) with a unit mask of 0x00 (No unit mask) count 10000
samples  %        symbol name
1074057  12.3539  f_GetTrueMean(float*, int, float, int, int)
906614   10.4280  f_GetPeak(float*, int, int, float, float, float*)
852335    9.8036  GaussFit(float*, int, int)
586146    6.7419  lcgf(double, double)
435604    5.0104  f_GetChiSq(float*, int, int, float, float, float*, float*)
372907    4.2892  sse2_ChirpData_ak(float (*) [2], float (*) [2], int, double, int, double)
281519    3.2381  n1bv_128
279130    3.2106  FindSpikes(float*, int, int, SETI_WU_INFO&)
257413    2.9608  find_pulse(float const*, int, float, int, int)
257321    2.9597  find_triplets(float const*, int, float, int, int)
255990    2.9444  __ieee754_pow
238857    2.7474  GetFixedPoT(float*, int, int, float*, int, int)
224128    2.5779  analyze_pot(float*, int, ChirpFftPair_t&)
212625    2.4456  foldArrayBy2LO(float**, PoTPlan*)
149591    1.7206  float_to_uchar(float*, unsigned char*, long, float)
140074    1.6111  foldArrayBy2A(float**, PoTPlan*)
133731    1.5382  foldArrayBy3(float**, PoTPlan*)
133064    1.5305  foldArrayBy4(float**, PoTPlan*)
123888    1.4250  t1bv_8
123432    1.4197  malloc
121711    1.3999  __ieee754_log
120817    1.3896  t1bv_16
119223    1.3713  foldArrayBy3LO(float**, PoTPlan*)
111872    1.2868  free
110494    1.2709  v_GetPowerSpectrum(float (*) [2], float*, int)
107708    1.2389  foldArrayBy5LO(float**, PoTPlan*)
95680     1.1005  t2bv_64
89048     1.0242  foldArrayBy4LO(float**, PoTPlan*)
87680     1.0085  foldArrayBy5(float**, PoTPlan*)
70870     0.8152  _int_malloc
63488     0.7302  pow
51006     0.5867  foldArrayBy2AL(float**, PoTPlan*)
46131     0.5306  n2bv_64
44673     0.5138  fraction_done(double, double)
32659     0.3756  t1bv_32
31360     0.3607  time_to_ra_dec(double, double*, double*)
28077     0.3229  ChooseGaussEvent(int, float, float, float, float, int, float, float, float*)
22536     0.2592  isnan
21487     0.2471  _int_free
21303     0.2450  t_funct(int, int, int)
21068     0.2423  PulseProgressUnits(double, int)
16028     0.1844  malloc_consolidate
13975     0.1607  t2bv_32
12463     0.1434  floor
10392     0.1195  workunit_grp::workunit_grp()
9860      0.1134  cnvt_bin_hz(int, int)
9513      0.1094  boinc_fraction_done
9401      0.1081  gaussian::gaussian()
8918      0.1026  operator new(unsigned int)
8896      0.1023  t2bv_16
8327      0.0958  analysis_config::analysis_config()
7772      0.0894  std::vector<unsigned char, std::allocator<unsigned char> >::_M_fill_insert(__gnu_cxx::__normal_iterator<unsigned char*, std::vector<unsigned char, std::allocator<unsigned char> > >, unsigned int, unsigned char const&)
7767      0.0893  TripletProgressUnits()
6692      0.0770  checkpoint(unsigned char)
6073      0.0699  receiver_config::receiver_config()
5963      0.0686  workunit_header::workunit_header()
5888      0.0677  MFILE::~MFILE()
5880      0.0676  __i686.get_pc_thunk.bx
5750      0.0661  result::result()
5472      0.0629  finite
5388      0.0620  splitter_config::splitter_config()
5114      0.0588  subband_description_t::subband_description_t()
4802      0.0552  __memmove_ssse3_rep
4568      0.0525  data_description_t::data_description_t()
4392      0.0505  operator delete(void*)
4184      0.0481  calc_detection_freq(double, double, double)
3804      0.0438  GAUSS_INFO::~GAUSS_INFO()
3609      0.0415  n2bv_32
3430      0.0395  log
3290      0.0378  tape::tape()
2945      0.0339  ReportPulseEvent(float, float, float, int, int, float, float, float*, int, int)
2941      0.0338  __memset_sse2_rep
2644      0.0304  recorder_config::recorder_config()
2523      0.0290  MFILE::MFILE()
2283      0.0263  n2bv_16
1862      0.0214  t2bv_8
1556      0.0179  t1bv_4
1279      0.0147  T.9610
1133      0.0130  T.9614
1113      0.0128  GaussianProgressUnits()
955       0.0110  seti_analyze(ANALYSIS_STATE&)
892       0.0103  SpikeProgressUnits(int)
736       0.0085  T.9615
689       0.0079  GAUSS_INFO::GAUSS_INFO()
674       0.0078  t2bv_2
507       0.0058  _int_memalign
486       0.0056  apply
471       0.0054  apply
449       0.0052  apply_dit
402       0.0046  spike::spike()
355       0.0041  memalign
335       0.0039  SPIKE_INFO::~SPIKE_INFO()
297       0.0034  __ieee754_log10
228       0.0026  SPIKE_INFO::SPIKE_INFO()
209       0.0024  apply
189       0.0022  T.9619
174       0.0020  pulse::pulse()
116       0.0013  floorf
95        0.0011  log10
86       9.9e-04  boinc_time_to_checkpoint
83       9.5e-04  calloc_a(unsigned int, unsigned int, unsigned int)
66       7.6e-04  invert_lcgf(float, float, float)
62       7.1e-04  PULSE_INFO::~PULSE_INFO()
59       6.8e-04  fftwf_execute_dft
49       5.6e-04  fftwf_malloc
47       5.4e-04  malloc_a(unsigned int, unsigned int)
45       5.2e-04  fftwf_kernel_free
27       3.1e-04  PULSE_INFO::PULSE_INFO()
26       3.0e-04  fftwf_kernel_malloc
17       2.0e-04  plan_PulsePoT(PoTPlan*, int, float*, int*)
7        8.1e-05  timer_handler()
5        5.8e-05  boinc_sleep(double)
3        3.5e-05  dtime()
3        3.5e-05  fftwf_free
3        3.5e-05  free_a(void*)
2        2.3e-05  GetPulsePoTLen(long, int*, int*)
2        2.3e-05  nanosleep
2        2.3e-05  usleep
1        1.2e-05  __libc_enable_asynccancel
1        1.2e-05  __nanosleep_nocancel

CPU: Intel Architectural Perfmon, speed 933 MHz (estimated)
Counted LLC_MISSES events (Last level cache demand requests from this core that missed the LLC) with a unit mask of 0x41 (No unit mask) count 10000
 LLC_MISSES:10000|
  samples|      %|
------------------
    54637 96.3157 seti_boinc
      455  0.8021 chromium-browser
	 LLC_MISSES:10000|
	  samples|      %|
	------------------
	      454 99.7802 chromium-browser
	        1  0.2198 anon (tgid:4700 range:0x71225000-0x71245000)
      181  0.3191 libc-2.12.1.so
      167  0.2944 libglib-2.0.so.0.2600.0
      161  0.2838 python2.6
      140  0.2468 Xorg
       90  0.1587 libgtk-x11-2.0.so.0.2200.0
       85  0.1498 libgdk-x11-2.0.so.0.2200.0
       75  0.1322 libcairo.so.2.11000.0
       71  0.1252 i965_dri.so
       68  0.1199 libdrm_intel.so.1.0.0
       62  0.1093 libgobject-2.0.so.0.2600.0
       56  0.0987 libpthread-2.12.1.so
       45  0.0793 perl
       33  0.0582 compiz
       31  0.0546 libX11.so.6.3.0
       31  0.0546 intel_drv.so
       28  0.0494 libdbus-1.so.3.5.2
       24  0.0423 mysqld
       19  0.0335 libfade.so
       19  0.0335 libpixman-1.so.0.18.4
       15  0.0264 libstdc++.so.6.0.14
       14  0.0247 libpango-1.0.so.0.2800.1
       13  0.0229 libpangoft2-1.0.so.0.2800.1
       12  0.0212 libxcb.so.1.1.0
       11  0.0194 no-vmlinux
       11  0.0194 libdecoration.so
        9  0.0159 ld-2.12.1.so
        9  0.0159 libanimation.so
        9  0.0159 libXrender.so.1.3.0
        8  0.0141 libmurrine.so
        8  0.0141 libpyglib-2.0-python2.6.so.0.0.0
        6  0.0106 libm-2.12.1.so
        6  0.0106 libwall.so
        6  0.0106 libpangocairo-1.0.so.0.2800.1
        6  0.0106 evdev_drv.so
        5  0.0088 libscale.so
        5  0.0088 libgtksourceview-2.0.so.0.0.0
        4  0.0071 libstaticswitcher.so
        4  0.0071 libdbus-glib-1.so.2.1.0
        4  0.0071 libgvfscommon.so.0.0.0
        4  0.0071 libGL.so.1.2
        4  0.0071 libfb.so
        3  0.0053 bash
        3  0.0053 gedit
        3  0.0053 im-ibus.so
        3  0.0053 libgthread-2.0.so.0.2600.0
        3  0.0053 libstartup-notification-1.so.0.0.0
        3  0.0053 libvte.so.9.2600.0
        3  0.0053 _gobject.so
        3  0.0053 libdri2.so
        2  0.0035 libdrm.so.2.4.0
        2  0.0035 libgcc_s.so.1
        2  0.0035 libezoom.so
        2  0.0035 libmove.so
        2  0.0035 libneg.so
        2  0.0035 libplace.so
        2  0.0035 libresize.so
        2  0.0035 libresizeinfo.so
        2  0.0035 libscaleaddon.so
        2  0.0035 libworkarounds.so
        2  0.0035 libXfixes.so.3.1.0
        2  0.0035 librsvg-2.so.2.32.0
        2  0.0035 libwnck-1.so.22.3.30
        2  0.0035 _glib.so
        2  0.0035 libextmod.so
        1  0.0018 dbus-daemon
        1  0.0018 librt-2.12.1.so
        1  0.0018 libudev.so.0.9.1
        1  0.0018 libz.so.1.2.3.4
        1  0.0018 wpa_supplicant
        1  0.0018 sudo
        1  0.0018 vmware-usbarbitrator
        1  0.0018 apache2
        1  0.0018 libexpo.so
        1  0.0018 libvpswitch.so
        1  0.0018 liba11y-keyboard.so
        1  0.0018 libpixmap.so
        1  0.0018 libORBit-2.so.0.1.0
        1  0.0018 libXdamage.so.1.1.0
        1  0.0018 libcompizconfig.so.0.0.0
        1  0.0018 libfontconfig.so.1.4.4
        1  0.0018 libgconf-2.so.4.1.5
        1  0.0018 libgio-2.0.so.0.2600.0
        1  0.0018 libxklavier.so.16.0.0
        1  0.0018 notify-osd
        1  0.0018 pango-basic-fc.so
        1  0.0018 _gtk.so
 
CPU: Intel Architectural Perfmon, speed 933 MHz (estimated)
Counted LLC_MISSES events (Last level cache demand requests from this core that missed the LLC) with a unit mask of 0x41 (No unit mask) count 10000
samples  %        symbol name
28811    52.7317  GetFixedPoT(float*, int, int, float*, int, int)
19382    35.4741  analyze_pot(float*, int, ChirpFftPair_t&)
5235      9.5814  n1bv_128
619       1.1329  n2bv_64
118       0.2160  sse2_ChirpData_ak(float (*) [2], float (*) [2], int, double, int, double)
104       0.1903  v_GetPowerSpectrum(float (*) [2], float*, int)
81        0.1483  n2bv_32
56        0.1025  _int_malloc
36        0.0659  malloc_consolidate
22        0.0403  t2bv_64
17        0.0311  _int_free
16        0.0293  pow
14        0.0256  free
9         0.0165  malloc
8         0.0146  result::result()
7         0.0128  FindSpikes(float*, int, int, SETI_WU_INFO&)
6         0.0110  GaussFit(float*, int, int)
6         0.0110  t1bv_32
6         0.0110  t1bv_8
6         0.0110  time_to_ra_dec(double, double*, double*)
5         0.0092  MFILE::MFILE()
5         0.0092  __ieee754_pow
4         0.0073  checkpoint(unsigned char)
4         0.0073  spike::spike()
4         0.0073  t2bv_32
3         0.0055  ChooseGaussEvent(int, float, float, float, float, int, float, float, float*)
3         0.0055  __memmove_ssse3_rep
3         0.0055  __memset_sse2_rep
3         0.0055  fraction_done(double, double)
3         0.0055  t1bv_16
2         0.0037  __ieee754_log
2         0.0037  __ieee754_log10
2         0.0037  apply
2         0.0037  f_GetPeak(float*, int, int, float, float, float*)
2         0.0037  f_GetTrueMean(float*, int, float, int, int)
2         0.0037  find_triplets(float const*, int, float, int, int)
2         0.0037  foldArrayBy3(float**, PoTPlan*)
2         0.0037  seti_analyze(ANALYSIS_STATE&)
2         0.0037  std::vector<unsigned char, std::allocator<unsigned char> >::_M_fill_insert(__gnu_cxx::__normal_iterator<unsigned char*, std::vector<unsigned char, std::allocator<unsigned char> > >, unsigned int, unsigned char const&)
1         0.0018  GaussianProgressUnits()
1         0.0018  PulseProgressUnits(double, int)
1         0.0018  T.9615
1         0.0018  TripletProgressUnits()
1         0.0018  _dl_sysinfo_int80
1         0.0018  _int_memalign
1         0.0018  apply_dit
1         0.0018  boinc_sleep(double)
1         0.0018  calc_detection_freq(double, double, double)
1         0.0018  data_description_t::data_description_t()
1         0.0018  dtime()
1         0.0018  fftwf_execute_dft
1         0.0018  find_pulse(float const*, int, float, int, int)
1         0.0018  foldArrayBy4LO(float**, PoTPlan*)
1         0.0018  foldArrayBy5LO(float**, PoTPlan*)
1         0.0018  lcgf(double, double)
1         0.0018  log
1         0.0018  operator delete(void*)
1         0.0018  operator new(unsigned int)
1         0.0018  subband_description_t::subband_description_t()
1         0.0018  tape::tape()
1         0.0018  timer_handler()
1         0.0018  workunit_header::workunit_header()

CPU: Intel Architectural Perfmon, speed 933 MHz (estimated)
Counted LLC_REFS events (Last level cache demand requests from this core) with a unit mask of 0x4f (No unit mask) count 10000
   LLC_REFS:10000|
  samples|      %|
------------------
   108756 91.0473 seti_boinc
     1282  1.0733 Xorg
     1200  1.0046 libc-2.12.1.so
     1185  0.9920 libglib-2.0.so.0.2600.0
     1005  0.8414 libcairo.so.2.11000.0
      848  0.7099 libgobject-2.0.so.0.2600.0
      684  0.5726 libgtk-x11-2.0.so.0.2200.0
      474  0.3968 libgdk-x11-2.0.so.0.2200.0
      406  0.3399 libdrm_intel.so.1.0.0
      381  0.3190 python2.6
      381  0.3190 libpango-1.0.so.0.2800.1
      365  0.3056 intel_drv.so
      362  0.3031 libpthread-2.12.1.so
      238  0.1992 libpixman-1.so.0.18.4
      200  0.1674 libX11.so.6.3.0
      146  0.1222 libpangoft2-1.0.so.0.2800.1
      140  0.1172 i965_dri.so
      113  0.0946 libxcb.so.1.1.0
       87  0.0728 libmurrine.so
       80  0.0670 libdbus-1.so.3.5.2
       79  0.0661 no-vmlinux
       74  0.0620 compiz
       74  0.0620 perl
       73  0.0611 chromium-browser
	   LLC_REFS:10000|
	  samples|      %|
	------------------
	       68 93.1507 chromium-browser
	        2  2.7397 anon (tgid:4700 range:0x71225000-0x71245000)
	        2  2.7397 anon (tgid:4700 range:0xdaf000-0xe13000)
	        1  1.3699 anon (tgid:4700 range:0x5ef9e000-0x5efbe000)
       52  0.0435 libpangocairo-1.0.so.0.2800.1
       51  0.0427 libXrender.so.1.3.0
       40  0.0335 ld-2.12.1.so
       39  0.0326 libm-2.12.1.so
       37  0.0310 evdev_drv.so
       34  0.0285 libgtksourceview-2.0.so.0.0.0
       33  0.0276 libfade.so
       32  0.0268 bash
       29  0.0243 libfb.so
       27  0.0226 libgthread-2.0.so.0.2600.0
       27  0.0226 librsvg-2.so.2.32.0
       27  0.0226 mysqld
       21  0.0176 libGL.so.1.2
       20  0.0167 libextmod.so
       19  0.0159 libdecoration.so
       17  0.0142 librt-2.12.1.so
       17  0.0142 libanimation.so
       16  0.0134 libvte.so.9.2600.0
       15  0.0126 libgio-2.0.so.0.2600.0
       13  0.0109 libexpo.so
       13  0.0109 libstaticswitcher.so
       13  0.0109 pango-basic-fc.so
       13  0.0109 _glib.so
       12  0.0100 libdrm.so.2.4.0
       12  0.0100 libudev.so.0.9.1
       11  0.0092 libscale.so
       10  0.0084 libresize.so
        9  0.0075 oprofiled
        9  0.0075 libwall.so
        9  0.0075 libXfixes.so.3.1.0
        9  0.0075 libpyglib-2.0-python2.6.so.0.0.0
        8  0.0067 libezoom.so
        7  0.0059 dbus-daemon
        6  0.0050 libscaleaddon.so
        6  0.0050 libsvg.so
        6  0.0050 libxml2.so.2.7.7
        5  0.0042 libplace.so
        5  0.0042 libdbus-glib-1.so.2.1.0
        5  0.0042 libgnome-keyring.so.0.1.1
        5  0.0042 libgvfscommon.so.0.0.0
        5  0.0042 rsyslogd
        4  0.0033 libregex.so
        4  0.0033 libworkarounds.so
        4  0.0033 libpixmap.so
        4  0.0033 libORBit-2.so.0.1.0
        4  0.0033 libfreetype.so.6.6.0
        3  0.0025 gedit
        3  0.0025 libmove.so
        3  0.0025 libwnck-1.so.22.3.30
        3  0.0025 libdri2.so
        2  0.0017 gawk
        2  0.0017 libgvfsdbus.so
        2  0.0017 libXdamage.so.1.1.0
        2  0.0017 libXext.so.6.4.0
        2  0.0017 libavahi-core.so.7.0.0
        2  0.0017 libgdk_pixbuf-2.0.so.0.2200.0
        2  0.0017 libmetacity-private.so.0.0.0
        2  0.0017 libstartup-notification-1.so.0.0.0
        2  0.0017 _gtk.so
        1 8.4e-04 libdl-2.12.1.so
        1 8.4e-04 libpam.so.0.82.2
        1 8.4e-04 libpcre.so.3.12.1
        1 8.4e-04 libpng12.so.0.44.0
        1 8.4e-04 libz.so.1.2.3.4
        1 8.4e-04 sudo
        1 8.4e-04 vmware-usbarbitrator
        1 8.4e-04 apache2
        1 8.4e-04 libneg.so
        1 8.4e-04 libresizeinfo.so
        1 8.4e-04 libsession.so
        1 8.4e-04 libsnap.so
        1 8.4e-04 libvpswitch.so
        1 8.4e-04 libpixbufloader-svg.so
        1 8.4e-04 liba11y-keyboard.so
        1 8.4e-04 im-ibus.so
        1 8.4e-04 libcanberra-gtk-module.so
        1 8.4e-04 libavahi-common.so.3.5.2
        1 8.4e-04 libfontconfig.so.1.4.4
        1 8.4e-04 libmysqlclient.so.16.0.0
        1 8.4e-04 libstdc++.so.6.0.14
        1 8.4e-04 libxklavier.so.16.0.0
        1 8.4e-04 smtp
 
CPU: Intel Architectural Perfmon, speed 933 MHz (estimated)
Counted LLC_REFS events (Last level cache demand requests from this core) with a unit mask of 0x4f (No unit mask) count 10000
samples  %        symbol name
57987    53.3184  GetFixedPoT(float*, int, int, float*, int, int)
33162    30.4921  analyze_pot(float*, int, ChirpFftPair_t&)
12033    11.0642  n1bv_128
1456      1.3388  t2bv_64
672       0.6179  n2bv_64
623       0.5728  t1bv_8
445       0.4092  t1bv_32
348       0.3200  v_GetPowerSpectrum(float (*) [2], float*, int)
324       0.2979  t1bv_16
240       0.2207  sse2_ChirpData_ak(float (*) [2], float (*) [2], int, double, int, double)
152       0.1398  _int_malloc
124       0.1140  malloc
110       0.1011  FindSpikes(float*, int, int, SETI_WU_INFO&)
82        0.0754  n2bv_32
68        0.0625  find_pulse(float const*, int, float, int, int)
68        0.0625  malloc_consolidate
62        0.0570  seti_analyze(ANALYSIS_STATE&)
57        0.0524  find_triplets(float const*, int, float, int, int)
44        0.0405  apply
41        0.0377  time_to_ra_dec(double, double*, double*)
40        0.0368  _int_free
34        0.0313  foldArrayBy3(float**, PoTPlan*)
33        0.0303  GaussFit(float*, int, int)
23        0.0211  pow
22        0.0202  apply_dit
22        0.0202  calc_detection_freq(double, double, double)
20        0.0184  foldArrayBy4(float**, PoTPlan*)
17        0.0156  analysis_config::analysis_config()
17        0.0156  free
16        0.0147  foldArrayBy5(float**, PoTPlan*)
15        0.0138  cnvt_bin_hz(int, int)
14        0.0129  checkpoint(unsigned char)
13        0.0120  SpikeProgressUnits(int)
13        0.0120  __ieee754_pow
13        0.0120  tape::tape()
12        0.0110  apply
11        0.0101  T.9614
11        0.0101  __ieee754_log
11        0.0101  __ieee754_log10
11        0.0101  apply
11        0.0101  foldArrayBy2LO(float**, PoTPlan*)
11        0.0101  result::result()
11        0.0101  spike::spike()
11        0.0101  workunit_grp::workunit_grp()
10        0.0092  log
10        0.0092  splitter_config::splitter_config()
9         0.0083  MFILE::MFILE()
9         0.0083  SPIKE_INFO::SPIKE_INFO()
9         0.0083  foldArrayBy2A(float**, PoTPlan*)
9         0.0083  foldArrayBy3LO(float**, PoTPlan*)
9         0.0083  foldArrayBy4LO(float**, PoTPlan*)
9         0.0083  workunit_header::workunit_header()
8         0.0074  ChooseGaussEvent(int, float, float, float, float, int, float, float, float*)
8         0.0074  T.9610
8         0.0074  __memmove_ssse3_rep
8         0.0074  __memset_sse2_rep
8         0.0074  f_GetChiSq(float*, int, int, float, float, float*, float*)
8         0.0074  operator new(unsigned int)
7         0.0064  f_GetTrueMean(float*, int, float, int, int)
7         0.0064  floor
7         0.0064  lcgf(double, double)
7         0.0064  log10
6         0.0055  foldArrayBy5LO(float**, PoTPlan*)
5         0.0046  PulseProgressUnits(double, int)
5         0.0046  TripletProgressUnits()
5         0.0046  __nanosleep_nocancel
5         0.0046  fftwf_execute_dft
5         0.0046  isnan
5         0.0046  t2bv_16
5         0.0046  t2bv_32
4         0.0037  __i686.get_pc_thunk.bx
4         0.0037  foldArrayBy2AL(float**, PoTPlan*)
4         0.0037  operator delete(void*)
3         0.0028  T.9615
3         0.0028  boinc_fraction_done
3         0.0028  f_GetPeak(float*, int, int, float, float, float*)
3         0.0028  fraction_done(double, double)
3         0.0028  std::vector<unsigned char, std::allocator<unsigned char> >::_M_fill_insert(__gnu_cxx::__normal_iterator<unsigned char*, std::vector<unsigned char, std::allocator<unsigned char> > >, unsigned int, unsigned char const&)
2         0.0018  MFILE::~MFILE()
2         0.0018  PULSE_INFO::PULSE_INFO()
2         0.0018  _dl_sysinfo_int80
2         0.0018  boinc_time_to_checkpoint
2         0.0018  n2bv_16
2         0.0018  recorder_config::recorder_config()
2         0.0018  subband_description_t::subband_description_t()
2         0.0018  timer_handler()
1        9.2e-04  SPIKE_INFO::~SPIKE_INFO()
1        9.2e-04  _int_memalign
1        9.2e-04  boinc_sleep(double)
1        9.2e-04  data_description_t::data_description_t()
1        9.2e-04  fftwf_kernel_malloc
1        9.2e-04  float_to_uchar(float*, unsigned char*, long, float)
1        9.2e-04  getrusage
1        9.2e-04  malloc_a(unsigned int, unsigned int)
1        9.2e-04  plan_PulsePoT(PoTPlan*, int, float*, int*)
1        9.2e-04  pulse::pulse()
1        9.2e-04  receiver_config::receiver_config()
1        9.2e-04  worker_signal_handler(int)


CPU: Intel Architectural Perfmon, speed 933 MHz (estimated)
Counted BR_INST_RETIRED events (number of branch instructions retired) with a unit mask of 0x00 (No unit mask) count 10000
BR_INST_RETIRE...|
  samples|      %|
------------------
  2435093 96.2380 seti_boinc
    14681  0.5802 oprofiled
    11215  0.4432 libdrm_intel.so.1.0.0
    10554  0.4171 libglib-2.0.so.0.2600.0
     8548  0.3378 libc-2.12.1.so
     7430  0.2936 libgobject-2.0.so.0.2600.0
     7409  0.2928 libcairo.so.2.11000.0
     5699  0.2252 libpangoft2-1.0.so.0.2800.1
     4706  0.1860 libpthread-2.12.1.so
     4275  0.1690 libgtk-x11-2.0.so.0.2200.0
     3187  0.1260 Xorg
     3165  0.1251 libpixman-1.so.0.18.4
     1688  0.0667 libpango-1.0.so.0.2800.1
     1659  0.0656 intel_drv.so
     1460  0.0577 libgdk-x11-2.0.so.0.2200.0
     1163  0.0460 bash
     1153  0.0456 chromium-browser
	BR_INST_RETIRE...|
	  samples|      %|
	------------------
	     1148 99.5663 chromium-browser
	        3  0.2602 anon (tgid:4700 range:0xdaf000-0xe13000)
	        2  0.1735 anon (tgid:4700 range:0x71225000-0x71245000)
      923  0.0365 python2.6
      575  0.0227 librsvg-2.so.2.32.0
      561  0.0222 ld-2.12.1.so
      450  0.0178 libxml2.so.2.7.7
      401  0.0158 mysqld
      380  0.0150 libgthread-2.0.so.0.2600.0
      375  0.0148 libvte.so.9.2600.0
      326  0.0129 libdbus-1.so.3.5.2
      295  0.0117 i965_dri.so
      284  0.0112 no-vmlinux
      279  0.0110 libX11.so.6.3.0
      269  0.0106 dbus-daemon
      244  0.0096 libpangocairo-1.0.so.0.2800.1
      207  0.0082 libxcb.so.1.1.0
      150  0.0059 perl
      127  0.0050 libpcre.so.3.12.1
      127  0.0050 libgdk_pixbuf-2.0.so.0.2200.0
      121  0.0048 libm-2.12.1.so
      121  0.0048 compiz
       88  0.0035 libextmod.so
       82  0.0032 pango-basic-fc.so
       65  0.0026 libmurrine.so
       62  0.0025 libXrender.so.1.3.0
       45  0.0018 libfb.so
       42  0.0017 libavahi-common.so.3.5.2
       42  0.0017 libgio-2.0.so.0.2600.0
       39  0.0015 gawk
       37  0.0015 libgtksourceview-2.0.so.0.0.0
       31  0.0012 gvfsd-metadata
       29  0.0011 evdev_drv.so
       26  0.0010 rsyslogd
       22 8.7e-04 librt-2.12.1.so
       22 8.7e-04 libdecoration.so
       21 8.3e-04 libGL.so.1.2
       20 7.9e-04 gedit
       17 6.7e-04 libexpo.so
       16 6.3e-04 libavahi-core.so.7.0.0
       16 6.3e-04 _glib.so
       15 5.9e-04 libmysqlclient.so.16.0.0
       15 5.9e-04 libpyglib-2.0-python2.6.so.0.0.0
       14 5.5e-04 libanimation.so
       14 5.5e-04 libdbus-glib-1.so.2.1.0
       13 5.1e-04 libdrm.so.2.4.0
       12 4.7e-04 libXfixes.so.3.1.0
       11 4.3e-04 grep
       11 4.3e-04 libfade.so
       10 4.0e-04 libpam.so.0.82.2
       10 4.0e-04 libresize.so
       10 4.0e-04 libscale.so
       10 4.0e-04 libgvfscommon.so.0.0.0
        9 3.6e-04 libcrypto.so.0.9.8
        8 3.2e-04 libstaticswitcher.so
        7 2.8e-04 gnome-panel
        7 2.8e-04 libwall.so
        7 2.8e-04 libmetacity-private.so.0.0.0
        7 2.8e-04 libwnck-1.so.22.3.30
        6 2.4e-04 dash
        5 2.0e-04 libORBit-2.so.0.1.0
        4 1.6e-04 wpa_supplicant
        4 1.6e-04 libfreetype.so.6.6.0
        4 1.6e-04 libstartup-notification-1.so.0.0.0
        3 1.2e-04 ophelp
        3 1.2e-04 libsvg.so
        2 7.9e-05 ls
        2 7.9e-05 libgcc_s.so.1
        2 7.9e-05 libpng12.so.0.44.0
        2 7.9e-05 sudo
        2 7.9e-05 libezoom.so
        2 7.9e-05 libmove.so
        2 7.9e-05 libresizeinfo.so
        2 7.9e-05 libXdamage.so.1.1.0
        2 7.9e-05 libgconf-2.so.4.1.5
        2 7.9e-05 libxklavier.so.16.0.0
        2 7.9e-05 _gobject.so
        2 7.9e-05 libdri2.so
        1 4.0e-05 libgcrypt.so.11.5.3
        1 4.0e-05 gnome-power-manager
        1 4.0e-05 libregex.so
        1 4.0e-05 libworkarounds.so
        1 4.0e-05 libmodelines.so
        1 4.0e-05 libgvfsdbus.so
        1 4.0e-05 libpixmap.so
        1 4.0e-05 im-ibus.so
        1 4.0e-05 libXext.so.6.4.0
        1 4.0e-05 libapr-1.so.0.4.2
        1 4.0e-05 libnm-util.so.1.6.0
        1 4.0e-05 libpanel-applet-2.so.0.2.68
        1 4.0e-05 libstdc++.so.6.0.14
        1 4.0e-05 mysql.so
        1 4.0e-05 _gtk.so
        1 4.0e-05 imuxsock.so
        1 4.0e-05 NetworkManager
 
CPU: Intel Architectural Perfmon, speed 933 MHz (estimated)
Counted BR_INST_RETIRED events (number of branch instructions retired) with a unit mask of 0x00 (No unit mask) count 10000
samples  %        symbol name
387161   15.9013  f_GetTrueMean(float*, int, float, int, int)
247973   10.1847  FindSpikes(float*, int, int, SETI_WU_INFO&)
242469    9.9586  GaussFit(float*, int, int)
192552    7.9084  find_triplets(float const*, int, float, int, int)
178200    7.3190  f_GetPeak(float*, int, int, float, float, float*)
87765     3.6047  GetFixedPoT(float*, int, int, float*, int, int)
80973     3.3257  lcgf(double, double)
77264     3.1734  free
69686     2.8621  f_GetChiSq(float*, int, int, float, float, float*, float*)
68229     2.8023  find_pulse(float const*, int, float, int, int)
67260     2.7625  __ieee754_pow
55677     2.2867  foldArrayBy2LO(float**, PoTPlan*)
55129     2.2642  analyze_pot(float*, int, ChirpFftPair_t&)
53933     2.2151  malloc
51243     2.1046  fraction_done(double, double)
45690     1.8766  float_to_uchar(float*, unsigned char*, long, float)
45495     1.8686  __ieee754_log
34606     1.4213  pow
32833     1.3485  foldArrayBy3LO(float**, PoTPlan*)
31990     1.3139  PulseProgressUnits(double, int)
31819     1.3069  foldArrayBy4LO(float**, PoTPlan*)
27619     1.1344  boinc_fraction_done
24830     1.0198  _int_malloc
22504     0.9243  foldArrayBy3(float**, PoTPlan*)
18806     0.7724  foldArrayBy2A(float**, PoTPlan*)
18798     0.7721  foldArrayBy4(float**, PoTPlan*)
15967     0.6558  _int_free
15591     0.6403  v_GetPowerSpectrum(float (*) [2], float*, int)
15513     0.6371  time_to_ra_dec(double, double*, double*)
14311     0.5878  isnan
11281     0.4633  ChooseGaussEvent(int, float, float, float, float, int, float, float, float*)
10159     0.4172  foldArrayBy5(float**, PoTPlan*)
8982      0.3689  sse2_ChirpData_ak(float (*) [2], float (*) [2], int, double, int, double)
8281      0.3401  foldArrayBy5LO(float**, PoTPlan*)
7822      0.3213  malloc_consolidate
7281      0.2990  foldArrayBy2AL(float**, PoTPlan*)
4896      0.2011  checkpoint(unsigned char)
4568      0.1876  operator new(unsigned int)
4134      0.1698  floor
3996      0.1641  workunit_grp::workunit_grp()
3616      0.1485  t_funct(int, int, int)
3141      0.1290  receiver_config::receiver_config()
2971      0.1220  std::vector<unsigned char, std::allocator<unsigned char> >::_M_fill_insert(__gnu_cxx::__normal_iterator<unsigned char*, std::vector<unsigned char, std::allocator<unsigned char> > >, unsigned int, unsigned char const&)
2965      0.1218  GAUSS_INFO::~GAUSS_INFO()
2816      0.1157  MFILE::~MFILE()
2446      0.1005  splitter_config::splitter_config()
2428      0.0997  result::result()
2295      0.0943  TripletProgressUnits()
2285      0.0938  __memmove_ssse3_rep
2134      0.0876  t1bv_8
1865      0.0766  workunit_header::workunit_header()
1862      0.0765  __memset_sse2_rep
1830      0.0752  gaussian::gaussian()
1719      0.0706  __i686.get_pc_thunk.bx
1686      0.0692  recorder_config::recorder_config()
1637      0.0672  MFILE::MFILE()
1493      0.0613  operator delete(void*)
1461      0.0600  cnvt_bin_hz(int, int)
1293      0.0531  calc_detection_freq(double, double, double)
1166      0.0479  analysis_config::analysis_config()
1085      0.0446  data_description_t::data_description_t()
972       0.0399  subband_description_t::subband_description_t()
912       0.0375  t1bv_16
756       0.0311  GaussianProgressUnits()
756       0.0311  tape::tape()
422       0.0173  log
413       0.0170  T.9610
375       0.0154  T.9614
231       0.0095  n1bv_128
230       0.0094  seti_analyze(ANALYSIS_STATE&)
205       0.0084  ReportPulseEvent(float, float, float, int, int, float, float, float*, int, int)
200       0.0082  SpikeProgressUnits(int)
164       0.0067  t2bv_64
142       0.0058  n2bv_64
135       0.0055  finite
121       0.0050  GAUSS_INFO::GAUSS_INFO()
117       0.0048  t1bv_32
101       0.0041  t2bv_16
90        0.0037  SPIKE_INFO::~SPIKE_INFO()
85        0.0035  _int_memalign
81        0.0033  apply
81        0.0033  memalign
80        0.0033  apply
65        0.0027  n2bv_32
62        0.0025  t2bv_32
59        0.0024  apply_dit
54        0.0022  __ieee754_log10
48        0.0020  spike::spike()
37        0.0015  t2bv_8
33        0.0014  fftwf_execute_dft
28        0.0012  apply
27        0.0011  t1bv_4
24       9.9e-04  log10
23       9.4e-04  boinc_time_to_checkpoint
21       8.6e-04  PULSE_INFO::~PULSE_INFO()
21       8.6e-04  calloc_a(unsigned int, unsigned int, unsigned int)
21       8.6e-04  floorf
20       8.2e-04  pulse::pulse()
13       5.3e-04  SPIKE_INFO::SPIKE_INFO()
13       5.3e-04  malloc_a(unsigned int, unsigned int)
11       4.5e-04  fftwf_kernel_free
10       4.1e-04  fftwf_malloc
7        2.9e-04  plan_PulsePoT(PoTPlan*, int, float*, int*)
6        2.5e-04  PULSE_INFO::PULSE_INFO()
6        2.5e-04  invert_lcgf(float, float, float)
4        1.6e-04  T.9615
2        8.2e-05  T.9619
2        8.2e-05  fftwf_kernel_malloc
1        4.1e-05  GetPulsePoTLen(long, int*, int*)
1        4.1e-05  fftwf_free
1        4.1e-05  result_group_start()
1        4.1e-05  timer_thread(void*)
1        4.1e-05  usleep
CPU: Intel Architectural Perfmon, speed 933 MHz (estimated)
Counted BR_MISS_PRED_RETIRED events (number of mispredicted branches retired (precise)) with a unit mask of 0x00 (No unit mask) count 10000
BR_MISS_PRED_R...|
  samples|      %|
------------------
    25264 97.6122 seti_boinc
       97  0.3748 python2.6
       78  0.3014 libcairo.so.2.11000.0
       69  0.2666 libc-2.12.1.so
       50  0.1932 libglib-2.0.so.0.2600.0
       46  0.1777 chromium-browser
	BR_MISS_PRED_R...|
	  samples|      %|
	------------------
	       45 97.8261 chromium-browser
	        1  2.1739 anon (tgid:4700 range:0xdaf000-0xe13000)
       29  0.1120 bash
       26  0.1005 ld-2.12.1.so
       22  0.0850 Xorg
       20  0.0773 libpthread-2.12.1.so
       20  0.0773 perl
       19  0.0734 i965_dri.so
       16  0.0618 libgobject-2.0.so.0.2600.0
       12  0.0464 libdrm_intel.so.1.0.0
       11  0.0425 libgdk-x11-2.0.so.0.2200.0
       11  0.0425 libpixman-1.so.0.18.4
       10  0.0386 libdbus-1.so.3.5.2
       10  0.0386 libX11.so.6.3.0
        8  0.0309 dbus-daemon
        8  0.0309 no-vmlinux
        7  0.0270 libgtk-x11-2.0.so.0.2200.0
        6  0.0232 libxcb.so.1.1.0
        5  0.0193 compiz
        5  0.0193 intel_drv.so
        2  0.0077 gawk
        2  0.0077 sudo
        2  0.0077 libXext.so.6.4.0
        2  0.0077 libavahi-core.so.7.0.0
        2  0.0077 libgvfscommon.so.0.0.0
        2  0.0077 libpyglib-2.0-python2.6.so.0.0.0
        2  0.0077 libstdc++.so.6.0.14
        2  0.0077 libvte.so.9.2600.0
        2  0.0077 libGL.so.1.2
        2  0.0077 _glib.so
        1  0.0039 libudev.so.0.9.1
        1  0.0039 vmware-usbarbitrator
        1  0.0039 libanimation.so
        1  0.0039 libdecoration.so
        1  0.0039 libexpo.so
        1  0.0039 libvpswitch.so
        1  0.0039 libXfixes.so.3.1.0
        1  0.0039 libdbus-glib-1.so.2.1.0
        1  0.0039 libgthread-2.0.so.0.2600.0
        1  0.0039 libmysqlclient.so.16.0.0
        1  0.0039 libpangoft2-1.0.so.0.2800.1
        1  0.0039 evdev_drv.so
        1  0.0039 mysqld
 
CPU: Intel Architectural Perfmon, speed 933 MHz (estimated)
Counted BR_MISS_PRED_RETIRED events (number of mispredicted branches retired (precise)) with a unit mask of 0x00 (No unit mask) count 10000
samples  %        symbol name
4094     16.2049  foldArrayBy2A(float**, PoTPlan*)
3657     14.4751  GaussFit(float*, int, int)
3431     13.5806  f_GetTrueMean(float*, int, float, int, int)
3326     13.1650  find_pulse(float const*, int, float, int, int)
1876      7.4256  lcgf(double, double)
1526      6.0402  foldArrayBy2AL(float**, PoTPlan*)
1442      5.7077  foldArrayBy2LO(float**, PoTPlan*)
1137      4.5005  foldArrayBy3(float**, PoTPlan*)
624       2.4699  foldArrayBy4(float**, PoTPlan*)
473       1.8722  find_triplets(float const*, int, float, int, int)
398       1.5754  _int_malloc
394       1.5595  foldArrayBy5(float**, PoTPlan*)
361       1.4289  FindSpikes(float*, int, int, SETI_WU_INFO&)
342       1.3537  time_to_ra_dec(double, double*, double*)
317       1.2547  foldArrayBy4LO(float**, PoTPlan*)
302       1.1954  foldArrayBy3LO(float**, PoTPlan*)
293       1.1598  floor
256       1.0133  GetFixedPoT(float*, int, int, float*, int, int)
213       0.8431  foldArrayBy5LO(float**, PoTPlan*)
192       0.7600  malloc_consolidate
189       0.7481  analyze_pot(float*, int, ChirpFftPair_t&)
104       0.4117  ChooseGaussEvent(int, float, float, float, float, int, float, float, float*)
99        0.3919  free
41        0.1623  ReportPulseEvent(float, float, float, int, int, float, float, float*, int, int)
31        0.1227  f_GetChiSq(float*, int, int, float, float, float*, float*)
20        0.0792  _int_free
18        0.0712  calc_detection_freq(double, double, double)
16        0.0633  __memset_sse2_rep
15        0.0594  t1bv_16
14        0.0554  malloc
11        0.0435  operator delete(void*)
8         0.0317  checkpoint(unsigned char)
7         0.0277  n1bv_128
6         0.0237  seti_analyze(ANALYSIS_STATE&)
5         0.0198  std::vector<unsigned char, std::allocator<unsigned char> >::_M_fill_insert(__gnu_cxx::__normal_iterator<unsigned char*, std::vector<unsigned char, std::allocator<unsigned char> > >, unsigned int, unsigned char const&)
4         0.0158  GaussianProgressUnits()
4         0.0158  __i686.get_pc_thunk.bx
3         0.0119  __memmove_ssse3_rep
2         0.0079  apply
2         0.0079  cnvt_bin_hz(int, int)
2         0.0079  operator new(unsigned int)
1         0.0040  SPIKE_INFO::SPIKE_INFO()
1         0.0040  __ieee754_pow
1         0.0040  apply
1         0.0040  invert_lcgf(float, float, float)
1         0.0040  spike::spike()
1         0.0040  t1bv_32
1         0.0040  t2bv_64
1         0.0040  t_funct(int, int, int)
1         0.0040  timer_handler()

```

















# Intel Atom D525 #

## Oprofile Intel Atom Events ##
```
xbmc@atom:~/Documents/boinc/seti_boinc/client$ sudo opcontrol --list-events | more
oprofile: available events for CPU type "Intel Atom"

See Intel Architecture Developer's Manual Volume 3B, Appendix A and
Intel Architecture Optimization Reference Manual (730795-001)

CPU_CLK_UNHALTED: (counter: all)
        Clock cycles when not halted (min count: 6000) 
        Unit masks (default 0x0)
        ----------
        0x00: core_p Core cycles when core is not halted 
        0x01: bus Bus cycles when core is not halted 
        0x02: no_other Bus cycles when core is active and the other is halted 
UNHALTED_REFERENCE_CYCLES: (counter: all)
        Unhalted reference cycles (min count: 6000) 
        Unit masks (default 0x1)
        ----------
        0x01: No unit mask 
INST_RETIRED: (counter: all)
        number of instructions retired (min count: 6000) 
        Unit masks (default 0x1)
        ----------
        0x01: No unit mask 
LLC_MISSES: (counter: all)
        Last level cache demand requests from this core that missed the LLC (min count: 6000) 
        Unit masks (default 0x41)
        ----------
        0x41: No unit mask 
LLC_REFS: (counter: all)
        Last level cache demand requests from this core (min count: 6000) 
        Unit masks (default 0x4f)
        ----------
        0x4f: No unit mask 
BR_INST_RETIRED: (counter: all)
        number of branch instructions retired (min count: 500) 
        Unit masks (default 0x0)
        ----------
        0x00: any Retired branch instructions 
        0x01: pred_not_taken Retired branch instructions that were predicted not-taken 
        0x02: mispred_not_taken Retired branch instructions that were mispredicted not-taken 
        0x04: pred_taken Retired branch instructions that were predicted taken 
        0x08: mispred_taken Retired branch instructions that were mispredicted taken 
        0x0a: mispred Retired mispredicted branch instructions (precise event) 
        0x0c: taken Retired taken branch instructions 
        0x0f: any1 Retired branch instructions 
BR_MISS_PRED_RETIRED: (counter: all)
        number of mispredicted branches retired (precise) (min count: 500) 
STORE_FORWARDS: (counter: all)
        Good store forwards (min count: 6000) 
        Unit masks (default 0x81)
        ----------
        0x81: good Good store forwards 
SEGMENT_REG_LOADS: (counter: all)
        Number of segment register loads (min count: 6000) 
        Unit masks (default 0x0)
        ----------
        0x00: any Number of segment register loads 
PREFETCH: (counter: all)
        Streaming SIMD Extensions (SSE) Prefetch instructions executed (min count: 6000) 
        Unit masks (default 0x1)
        ----------
        0x01: prefetcht0 Streaming SIMD Extensions (SSE) PrefetchT0 instructions executed 
        0x06: sw_l2 Streaming SIMD Extensions (SSE) PrefetchT1 and PrefetchT2 instructions executed 
        0x08: prefetchnta Streaming SIMD Extensions (SSE) Prefetch NTA instructions executed 
DATA_TLB_MISSES: (counter: all)
        Memory accesses that missed the DTLB (min count: 6000) 
        Unit masks (default 0x7)

        0x07: dtlb_miss Memory accesses that missed the DTLB 
        0x05: dtlb_miss_ld DTLB misses due to load operations 
        0x09: l0_dtlb_miss_ld L0_DTLB misses due to load operations 
        0x06: dtlb_miss_st DTLB misses due to store operations 
PAGE_WALKS: (counter: all)
        Page walks (min count: 6000) 
        Unit masks (default 0x3)
        ----------
        0x03: walks Number of page-walks executed 
        0x03: cycles Duration of page-walks in core cycles 
X87_COMP_OPS_EXE: (counter: all)
        Floating point computational micro-ops (min count: 6000) 
        Unit masks (default 0x81)
        ----------
        0x01: s Floating point computational micro-ops executed 
        0x81: ar Floating point computational micro-ops retired 
FP_ASSIST: (counter: all)
        Floating point assists (min count: 6000) 
        Unit masks (default 0x81)
        ----------
        0x81: ar Floating point assists 
MUL: (counter: all)
        Multiply operations (min count: 6000) 
        Unit masks (default 0x1)
        ----------
        0x01: s Multiply operations executed 
        0x81: ar Multiply operations retired 
DIV: (counter: all)
        Divide operations (min count: 6000) 
        Unit masks (default 0x1)
        ----------
        0x01: s Divide operations executed 
        0x81: ar Divide operations retired 
CYCLES_DIV_BUSY: (counter: all)
        Cycles the driver is busy (min count: 6000) 
        Unit masks (default 0x1)
        ----------
        0x01: No unit mask 
CORE: (counter: all)
        Cycles L2 address bus is in use (min count: 6000) 
        Unit masks (default 0x180)
        ----------
        0x180: all All cores. 
        0x80: this This Core. 
L2_DBUS_BUSY: (counter: all)
        Cycles the L2 cache data bus is busy (min count: 6000) 
        Unit masks (default 0x180)
        ----------
        0x180: all All cores. 
        0x80: this This Core. 
L2_LINES_IN: (counter: all)
        L2 cache misses (min count: 500) 
        Unit masks (default 0x1e0)
        ----------
        0x180: all All cores. 
        0x80: this This Core. 
        0x60: all All inclusive 
        0x20: hw Hardware prefetch only 
        0x00: exclude_hw Exclude hardware prefetch 
L2_M_LINES_IN: (counter: all)
        L2 cache line modifications (min count: 500) 
        Unit masks (default 0x180)
        ----------
        0x180: all All cores. 
        0x80: this This Core. 
L2_LINES_OUT: (counter: all)
        L2 cache lines evicted (min count: 500) 
        Unit masks (default 0x1e0)
        ----------
        0x180: all All cores. 
        0x80: this This Core. 
        0x60: all All inclusive 
        0x20: hw Hardware prefetch only 
        0x00: exclude_hw Exclude hardware prefetch 
L2_M_LINES_OUT: (counter: all)
        Modified lines evicted from the L2 cache (min count: 500) 
        Unit masks (default 0x1e0)
        ----------
        0x180: all All cores. 
        0x80: this This Core. 
        0x60: all All inclusive 
        0x20: hw Hardware prefetch only 
        0x00: exclude_hw Exclude hardware prefetch 
L2_IFETCH: (counter: all)
        L2 cacheable instruction fetch requests (min count: 6000) 
        Unit masks (default 0x18f)
        ----------
        0x180: all All cores. 
        0x80: this This Core. 
        0x08: modified Counts modified state 
        0x04: exclusive Counts exclusive state 
        0x02: shared Counts shared state 
        0x01: invalid Counts invalid state 
L2_LD: (counter: all)
        L2 cache reads (min count: 6000) 
        Unit masks (default 0x1ef)
        ----------
        0x180: all All cores. 
        0x80: this This Core.
        0x60: all All inclusive 
        0x20: hw Hardware prefetch only 
        0x00: exclude_hw Exclude hardware prefetch 
        0x08: modified Counts modified state 
        0x04: exclusive Counts exclusive state 
        0x02: shared Counts shared state 
        0x01: invalid Counts invalid state 
L2_ST: (counter: all)
        L2 store requests (min count: 6000) 
        Unit masks (default 0x18f)
        ----------
        0x180: all All cores. 
        0x80: this This Core. 
        0x08: modified Counts modified state 
        0x04: exclusive Counts exclusive state 
        0x02: shared Counts shared state 
        0x01: invalid Counts invalid state 
L2_LOCK: (counter: all)
        L2 locked accesses (min count: 6000) 
        Unit masks (default 0x18f)
        ----------
        0x180: all All cores. 
        0x80: this This Core. 
        0x08: modified Counts modified state 
        0x04: exclusive Counts exclusive state 
        0x02: shared Counts shared state 
        0x01: invalid Counts invalid state 
L2_RQSTS: (counter: all)
        L2 cache requests (min count: 6000) 
        Unit masks (default 0x1ef)
        ----------
        0x41: i_state L2 cache demand requests from this core that missed the L2 
        0x4f: mesi L2 cache demand requests from this core 

        0x180: all All cores. 
        0x80: this This Core. 
        0x60: all All inclusive 
        0x20: hw Hardware prefetch only 
        0x00: exclude_hw Exclude hardware prefetch 
        0x08: modified Counts modified state 
        0x04: exclusive Counts exclusive state 
        0x02: shared Counts shared state 
        0x01: invalid Counts invalid state 
L2_REJECT_BUSQ: (counter: all)
        Rejected L2 cache requests (min count: 500) 
        Unit masks (default 0x1ef)
        ----------
        0x180: all All cores. 
        0x80: this This Core. 
        0x60: all All inclusive 
        0x20: hw Hardware prefetch only 
        0x00: exclude_hw Exclude hardware prefetch 
        0x08: modified Counts modified state 
        0x04: exclusive Counts exclusive state 
        0x02: shared Counts shared state 
        0x01: invalid Counts invalid state 
L2_NO_REQ: (counter: all)
        Cycles no L2 cache requests are pending (min count: 6000) 
        Unit masks (default 0x180)
        ----------
        0x180: all All cores. 
        0x80: this This Core. 
EIST_TRANS: (counter: all)
        Number of Enhanced Intel SpeedStep(R) Technology (EIST) transitions (min count: 6000) 
THERMAL_TRIP: (counter: all)
        Number of thermal trips (min count: 6000) 
        Unit masks (default 0xc0)
        ----------
        0xc0: thermal_trip Number of thermal trips. 
L1D_CACHE: (counter: all)
        L1d Cache accesses (min count: 6000) 
        Unit masks (default 0x21)
        ----------
        0x21: ld L1 Cacheable Data Reads 
        0x22: st L1 Cacheable Data Writes 
BUS_REQUEST_OUTSTANDING: (counter: all)
        Outstanding cacheable data read bus requests duration (min count: 6000) 
        Unit masks (default 0x180)
        ----------
        0x180: all All cores. 
        0x80: this This Core. 
        0x00: this This agent 
        0x40: any Include any agents 
BUS_BNR_DRV: (counter: all)
        Number of Bus Not Ready signals asserted (min count: 6000) 
        Unit masks (default 0x0)
        ----------
        0x00: this This agent 
        0x40: any Include any agents 
BUS_DRDY_CLOCKS: (counter: all)
        Bus cycles when data is sent on the bus (min count: 6000) 
        Unit masks (default 0x0)
        ----------
        0x00: this This agent 
        0x40: any Include any agents 
BUS_LOCK_CLOCKS: (counter: all)
        Bus cycles when a LOCK signal is asserted. (min count: 6000) 
        Unit masks (default 0x180)
        ----------
        0x180: all All cores. 
        0x80: this This Core. 
        0x00: this This agent 
        0x40: any Include any agents 
BUS_DATA_RCV: (counter: all)
        Bus cycles while processor receives data (min count: 6000) 
        Unit masks (default 0x180)
        ----------
        0x180: all All cores. 
        0x80: this This Core. 
BUS_TRANS_BRD: (counter: all)
        Burst read bus transactions (min count: 500) 
        Unit masks (default 0x180)
        ----------
        0x180: all All cores. 
        0x80: this This Core. 
        0x00: this This agent 
        0x40: any Include any agents 
BUS_TRANS_RFO: (counter: all)
        RFO bus transactions (min count: 500) 
        Unit masks (default 0x180)
        ----------
        0x180: all All cores. 
        0x80: this This Core. 
        0x00: this This agent 
        0x40: any Include any agents 
BUS_TRANS_WB: (counter: all)
        Explicit writeback bus transactions (min count: 500) 
        Unit masks (default 0x180)
        ----------
        0x180: all All cores. 
        0x80: this This Core. 
        0x00: this This agent 
        0x40: any Include any agents
BUS_TRANS_IFETCH: (counter: all)
        Instruction-fetch bus transactions. (min count: 500) 
        Unit masks (default 0x180)
        ----------
        0x180: all All cores. 
        0x80: this This Core. 
        0x00: this This agent 
        0x40: any Include any agents 
BUS_TRANS_INVAL: (counter: all)
        Invalidate bus transactions (min count: 500) 
        Unit masks (default 0x180)
        ----------
        0x180: all All cores. 
        0x80: this This Core. 
        0x00: this This agent 
        0x40: any Include any agents 
BUS_TRANS_PWR: (counter: all)
        Partial write bus transaction. (min count: 500) 
        Unit masks (default 0x180)
        ----------
        0x180: all All cores. 
        0x80: this This Core. 
        0x00: this This agent 
        0x40: any Include any agents 
BUS_TRANS_P: (counter: all)
        Partial bus transactions (min count: 500) 
        Unit masks (default 0x180)
        ----------
        0x180: all All cores. 
        0x80: this This Core. 
        0x00: this This agent 
        0x40: any Include any agents 
BUS_TRANS_IO: (counter: all)

        IO bus transactions (min count: 500) 
        Unit masks (default 0x180)
        ----------
        0x180: all All cores. 
        0x80: this This Core. 
        0x00: this This agent 
        0x40: any Include any agents 
BUS_TRANS_DEF: (counter: all)
        Deferred bus transactions (min count: 500) 
        Unit masks (default 0x180)
        ----------
        0x180: all All cores. 
        0x80: this This Core. 
        0x00: this This agent 
        0x40: any Include any agents 
BUS_TRANS_BURST: (counter: all)
        Burst (full cache-line) bus transactions. (min count: 500) 
        Unit masks (default 0x180)
        ----------
        0x180: all All cores. 
        0x80: this This Core. 
        0x00: this This agent 
        0x40: any Include any agents 
BUS_TRANS_MEM: (counter: all)
        Memory bus transactions (min count: 500) 
        Unit masks (default 0x180)
        ----------
        0x180: all All cores. 
        0x80: this This Core. 
        0x00: this This agent 
        0x40: any Include any agents 
BUS_TRANS_ANY: (counter: all)
        All bus transactions (min count: 500)
        Unit masks (default 0x180)
        ----------
        0x180: all All cores. 
        0x80: this This Core. 
        0x00: this This agent 
        0x40: any Include any agents 
EXT_SNOOP: (counter: all)
        External snoops (min count: 500) 
        Unit masks (default 0x18f)
        ----------
        0x180: all All cores. 
        0x80: this This Core. 
        0x08: modified Counts modified state 
        0x04: exclusive Counts exclusive state 
        0x02: shared Counts shared state 
        0x01: invalid Counts invalid state 
BUS_HIT_DRV: (counter: all)
        HIT signal asserted (min count: 500) 
        Unit masks (default 0x0)
        ----------
        0x00: this This agent 
        0x40: any Include any agents 
BUS_HITM_DRV: (counter: all)
        HITM signal asserted (min count: 500) 
        Unit masks (default 0x0)
        ----------
        0x00: this This agent 
        0x40: any Include any agents 
BUSQ_EMPTY: (counter: all)
        Bus queue is empty (min count: 500) 
        Unit masks (default 0x180)
        ----------
        0x180: all All cores.

        0x80: this This Core. 
SNOOP_STALL_DRV: (counter: all)
        Bus stalled for snoops (min count: 6000) 
        Unit masks (default 0x180)
        ----------
        0x180: all All cores. 
        0x80: this This Core. 
        0x00: this This agent 
        0x40: any Include any agents 
BUS_IO_WAIT: (counter: all)
        IO requests waiting in the bus queue (min count: 6000) 
        Unit masks (default 0x180)
        ----------
        0x180: all All cores. 
        0x80: this This Core. 
ICACHE: (counter: all)
        Instruction cache accesses (min count: 6000) 
        Unit masks (default 0x3)
        ----------
        0x03: accesses Instruction fetches 
        0x02: misses Icache miss 
ITLB: (counter: all)
        ITLB events (min count: 6000) 
        Unit masks (default 0x4)
        ----------
        0x04: flush ITLB flushes 
        0x02: misses ITLB misses 
MACRO_INSTS: (counter: all)
        instructions decoded (min count: 6000) 
        Unit masks (default 0x3)
        ----------
        0x02: cisc_decoded CISC macro instructions decoded 
        0x03: all_decoded All Instructions decoded

SIMD_UOPS_EXEC: (counter: all)
        SIMD micro-ops executed (min count: 6000) 
        Unit masks (default 0x80)
        ----------
        0x00: s SIMD micro-ops executed (excluding stores) 
        0x80: ar SIMD micro-ops retired (excluding stores) 
SIMD_SAT_UOP_EXEC: (counter: all)
        SIMD saturated arithmetic micro-ops executed (min count: 6000) 
        Unit masks (default 0x0)
        ----------
        0x00: s SIMD saturated arithmetic micro-ops executed 
        0x80: ar SIMD saturated arithmetic micro-ops retired 
SIMD_UOP_TYPE_EXEC: (counter: all)
        SIMD packed microops executed (min count: 6000) 
        Unit masks (default 0x1)
        ----------
        0x01: s SIMD packed multiply microops executed 
        0x81: ar SIMD packed multiply microops retired 
        0x02: s SIMD packed shift micro-ops executed 
        0x82: ar SIMD packed shift micro-ops retired 
        0x04: s SIMD pack micro-ops executed 
        0x84: ar SIMD pack micro-ops retired 
        0x08: s SIMD unpack micro-ops executed 
        0x88: ar SIMD unpack micro-ops retired 
        0x10: s SIMD packed logical microops executed 
        0x90: ar SIMD packed logical microops retired 
        0x20: s SIMD packed arithmetic micro-ops executed 
        0xa0: ar SIMD packed arithmetic micro-ops retired 
UOPS_RETIRED: (counter: all)
        Micro-ops retired (min count: 6000) 
        Unit masks (default 0x10)
        ----------
        0x10: any Micro-ops retired

MACHINE_CLEARS: (counter: all)
        Self-Modifying Code detected (min count: 6000) 
        Unit masks (default 0x1)
        ----------
        0x01: No unit mask 
CYCLES_INT_MASKED: (counter: all)
        Cycles during which interrupts are disabled (min count: 6000) 
        Unit masks (default 0x1)
        ----------
        0x01: cycles_int_masked Cycles during which interrupts are disabled 
        0x02: cycles_int_pending_and_masked Cycles during which interrupts are pending and disabled 
SIMD_INST_RETIRED: (counter: all)
        Retired Streaming SIMD Extensions (SSE) instructions (min count: 6000) 
        Unit masks (default 0x1)
        ----------
        0x01: packed_single Retired Streaming SIMD Extensions (SSE) packed-single instructions 
        0x02: scalar_single Retired Streaming SIMD Extensions (SSE) scalar-single instructions 
        0x04: packed_double Retired Streaming SIMD Extensions 2 (SSE2) packed-double instructions 
        0x08: scalar_double Retired Streaming SIMD Extensions 2 (SSE2) scalar-double instructions 
        0x10: vector Retired Streaming SIMD Extensions 2 (SSE2) vector instructions 
        0x1f: any Retired Streaming SIMD instructions 
HW_INT_RCV: (counter: all)
        Hardware interrupts received (min count: 6000) 
SIMD_COMP_INST_RETIRED: (counter: all)
        Retired computational Streaming SIMD Extensions (SSE) instructions. (min count: 6000) 
        Unit masks (default 0x1)
        ----------
        0x01: packed_single Retired computational Streaming SIMD Extensions (SSE) packed-single 
              instructions 
        0x02: scalar_single Retired computational Streaming SIMD Extensions (SSE) scalar-single 
              instructions 
        0x04: packed_double Retired computational Streaming SIMD Extensions 2 (SSE2) packed-double 
              instructions

        Retired computational Streaming SIMD Extensions (SSE) instructions. (min count: 6000) 
        Unit masks (default 0x1)
        ----------
        0x01: packed_single Retired computational Streaming SIMD Extensions (SSE) packed-single 
              instructions 
        0x02: scalar_single Retired computational Streaming SIMD Extensions (SSE) scalar-single 
              instructions 
        0x04: packed_double Retired computational Streaming SIMD Extensions 2 (SSE2) packed-double 
              instructions 
        0x08: scalar_double Retired computational Streaming SIMD Extensions 2 (SSE2) scalar-double 
              instructions 
MEM_LOAD_RETIRED: (counter: all)
        Retired loads (min count: 6000) 
        Unit masks (default 0x1)
        ----------
        0x01: l2_hit Retired loads that hit the L2 cache (precise event) 
        0x02: l2_miss Retired loads that miss the L2 cache (precise event) 
        0x04: dtlb_miss Retired loads that miss the DTLB (precise event) 
SIMD_ASSIST: (counter: all)
        SIMD assists invoked (min count: 6000) 
SIMD_INSTR_RETIRED: (counter: all)
        SIMD Instructions retired (min count: 6000) 
SIMD_SAT_INSTR_RETIRED: (counter: all)
        Saturated arithmetic instructions retired (min count: 6000) 
BR_INST_DECODED: (counter: all)
        Branch instructions decoded (min count: 6000) 
BOGUS_BR: (counter: all)
        Bogus branches (min count: 6000) 
BACLEARS: (counter: all)
        BACLEARS asserted (min count: 6000) 
        Unit masks (default 0x1)
        ----------
        0x01: No unit mask 
```

## Event Data on Atom D525 ##

```
Tue Sep 20 19:16:41 CDT 2011
CPU: Intel Atom, speed 1795.72 MHz (estimated)
Counted CPU_CLK_UNHALTED events (Clock cycles when not halted) with a unit mask of 0x00 (core_p Core cycles when core is not halted) count 10000
CPU_CLK_UNHALT...|
  samples|      %|
------------------
 10044490 94.8466 seti_boinc
	CPU_CLK_UNHALT...|
	  samples|      %|
	------------------
	  9991805 99.4755 seti_boinc
	    52685  0.5245 [vdso] (tgid:6081 range:0x2a3000-0x2a4000)
   372738  3.5196 oprofiled
	CPU_CLK_UNHALT...|
	  samples|      %|
	------------------
	   372629 99.9708 oprofiled
	      109  0.0292 [vdso] (tgid:6351 range:0x2c7000-0x2c8000)
    60232  0.5687 no-vmlinux
    36359  0.3433 libc-2.12.1.so
    12218  0.1154 libglib-2.0.so.0.2600.1
    10386  0.0981 bash
	CPU_CLK_UNHALT...|
	  samples|      %|
	------------------
	    10357 99.7208 bash
	       27  0.2600 [vdso] (tgid:6423 range:0x780000-0x781000)
	        2  0.0193 [vdso] (tgid:6080 range:0x600000-0x601000)
     8743  0.0826 dbus-daemon
	CPU_CLK_UNHALT...|
	  samples|      %|
	------------------
	     8731 99.8627 dbus-daemon
	       12  0.1373 [vdso] (tgid:821 range:0x259000-0x25a000)
     7237  0.0683 ld-2.12.1.so
     6942  0.0656 libgobject-2.0.so.0.2600.1
     6847  0.0647 libdbus-1.so.3.5.2
     5907  0.0558 libcairo.so.2.11000.0
     4624  0.0437 libpthread-2.12.1.so
     4089  0.0386 libgio-2.0.so.0.2600.1
     1576  0.0149 Xorg
	CPU_CLK_UNHALT...|
	  samples|      %|
	------------------
	     1514 96.0660 Xorg
	       62  3.9340 [vdso] (tgid:1265 range:0x78d000-0x78e000)
      708  0.0067 libgdk-x11-2.0.so.0.2200.0
      617  0.0058 nvidia_drv.so
      600  0.0057 libgthread-2.0.so.0.2600.1
      530  0.0050 libX11.so.6.3.0
      469  0.0044 ophelp
      459  0.0043 libeggdbus-1.so.0.0.0
      453  0.0043 libdbus-glib-1.so.2.1.0
      387  0.0037 libpolkit-backend-1.so.0.0.0
      367  0.0035 compiz
	CPU_CLK_UNHALT...|
	  samples|      %|
	------------------
	      356 97.0027 compiz
	       11  2.9973 [vdso] (tgid:1540 range:0xead000-0xeae000)
      338  0.0032 libxcb.so.1.1.0
      183  0.0017 mawk
      177  0.0017 libpolkit-gobject-1.so.0.0.0
      151  0.0014 NetworkManager
	CPU_CLK_UNHALT...|
	  samples|      %|
	------------------
	      141 93.3775 NetworkManager
	       10  6.6225 [vdso] (tgid:828 range:0x422000-0x423000)
      121  0.0011 polkitd
	CPU_CLK_UNHALT...|
	  samples|      %|
	------------------
	      121 100.000 [vdso] (tgid:1331 range:0x672000-0x673000)
      120  0.0011 libgtk-x11-2.0.so.0.2200.0
      105 9.9e-04 irqbalance
	CPU_CLK_UNHALT...|
	  samples|      %|
	------------------
	       87 82.8571 irqbalance
	       18 17.1429 [vdso] (tgid:951 range:0xa83000-0xa84000)
      102 9.6e-04 libpam.so.0.82.2
      100 9.4e-04 libnvidia-glcore.so.260.19.06
       89 8.4e-04 dash
       89 8.4e-04 sudo
       87 8.2e-04 libORBit-2.so.0.1.0
       79 7.5e-04 grep
       68 6.4e-04 libpangoft2-1.0.so.0.2800.2
       62 5.9e-04 libgvfscommon.so.0.0.0
       62 5.9e-04 rsyslogd
       60 5.7e-04 librt-2.12.1.so
       58 5.5e-04 libpango-1.0.so.0.2800.2
       52 4.9e-04 console-kit-daemon
	CPU_CLK_UNHALT...|
	  samples|      %|
	------------------
	       42 80.7692 console-kit-daemon
	       10 19.2308 [vdso] (tgid:1191 range:0x3a6000-0x3a7000)
       49 4.6e-04 libm-2.12.1.so
       49 4.6e-04 libnss_compat-2.12.1.so
       46 4.3e-04 libdl-2.12.1.so
       41 3.9e-04 libusbmuxd.so.1.0.4
       38 3.6e-04 libfade.so
       34 3.2e-04 nm-applet
	CPU_CLK_UNHALT...|
	  samples|      %|
	------------------
	       21 61.7647 nm-applet
	       13 38.2353 [vdso] (tgid:1543 range:0x35d000-0x35e000)
       34 3.2e-04 libnm-glib.so.2.4.1
       27 2.5e-04 gnome-screensaver
	CPU_CLK_UNHALT...|
	  samples|      %|
	------------------
	       15 55.5556 gnome-screensaver
	       12 44.4444 [vdso] (tgid:1619 range:0x853000-0x854000)
       27 2.5e-04 udisks-daemon
	CPU_CLK_UNHALT...|
	  samples|      %|
	------------------
	       19 70.3704 udisks-daemon
	        8 29.6296 [vdso] (tgid:1601 range:0x77a000-0x77b000)
       25 2.4e-04 libstartup-notification-1.so.0.0.0
       25 2.4e-04 libwnck-1.so.22.3.30
       24 2.3e-04 libdecoration.so
       24 2.3e-04 libgconf-2.so.4.1.5
       23 2.2e-04 libxklavier.so.16.0.0
       23 2.2e-04 sshd
	CPU_CLK_UNHALT...|
	  samples|      %|
	------------------
	       22 95.6522 sshd
	        1  4.3478 [vdso] (tgid:3059 range:0x1e3000-0x1e4000)
       21 2.0e-04 evdev_drv.so
       20 1.9e-04 libpulse-mainloop-glib.so.0.0.4
       18 1.7e-04 libncurses.so.5.7
       18 1.7e-04 wpa_supplicant
       18 1.7e-04 libvpswitch.so
       18 1.7e-04 libwall.so
       16 1.5e-04 libpopt.so.0.0.0
       16 1.5e-04 libudev.so.0.9.1
       15 1.4e-04 libexpo.so
       14 1.3e-04 libcompizconfig.so.0.0.0
       13 1.2e-04 libcrypto.so.0.9.8
       13 1.2e-04 libresizeinfo.so
       13 1.2e-04 libstaticswitcher.so
       13 1.2e-04 libXi.so.6.1.0
       12 1.1e-04 libscale.so
       12 1.1e-04 libkeyboard.so
       12 1.1e-04 libnm-util.so.1.6.0
       11 1.0e-04 ls
       11 1.0e-04 libanimation.so
       11 1.0e-04 libccp.so
       11 1.0e-04 gconfd-2
	CPU_CLK_UNHALT...|
	  samples|      %|
	------------------
	       10 90.9091 gconfd-2
	        1  9.0909 [vdso] (tgid:1515 range:0x9a7000-0x9a8000)
       11 1.0e-04 libpangocairo-1.0.so.0.2800.2
       10 9.4e-05 libnss_nis-2.12.1.so
       10 9.4e-05 libsession.so
       10 9.4e-05 libXext.so.6.4.0
        9 8.5e-05 rm
        9 8.5e-05 init
        9 8.5e-05 gnome-panel
	CPU_CLK_UNHALT...|
	  samples|      %|
	------------------
	        5 55.5556 [vdso] (tgid:1549 range:0xac4000-0xac5000)
	        4 44.4444 gnome-panel
        9 8.5e-05 seq
        9 8.5e-05 liba11y-keyboard.so
        9 8.5e-05 gnome-settings-daemon
	CPU_CLK_UNHALT...|
	  samples|      %|
	------------------
	        9 100.000 [vdso] (tgid:1523 range:0x579000-0x57a000)
        9 8.5e-05 libextmod.so
        8 7.6e-05 gnome-terminal
	CPU_CLK_UNHALT...|
	  samples|      %|
	------------------
	        5 62.5000 [vdso] (tgid:3459 range:0x864000-0x865000)
	        3 37.5000 gnome-terminal
        8 7.6e-05 gtk-window-decorator
	CPU_CLK_UNHALT...|
	  samples|      %|
	------------------
	        4 50.0000 gtk-window-decorator
	        4 50.0000 [vdso] (tgid:1621 range:0x387000-0x388000)
        8 7.6e-05 libmove.so
        8 7.6e-05 libplace.so
        8 7.6e-05 libregex.so
        8 7.6e-05 libscaleaddon.so
        8 7.6e-05 gvfs-afc-volume-monitor
	CPU_CLK_UNHALT...|
	  samples|      %|
	------------------
	        8 100.000 [vdso] (tgid:1613 range:0x45d000-0x45e000)
        8 7.6e-05 libpulse.so.0.12.2
        7 6.6e-05 cat
        7 6.6e-05 libresize.so
        7 6.6e-05 libXrender.so.1.3.0
        7 6.6e-05 libpulsecommon-0.9.21.so
        5 4.7e-05 libnss_files-2.12.1.so
        5 4.7e-05 libselinux.so.1
        5 4.7e-05 pam_limits.so
        5 4.7e-05 libsnap.so
        5 4.7e-05 libmurrine.so
        5 4.7e-05 libnl.so.1.1
        5 4.7e-05 libplc4.so
        5 4.7e-05 libwfb.so
        4 3.8e-05 libfuse.so.2.8.4
        4 3.8e-05 gnome-power-manager
	CPU_CLK_UNHALT...|
	  samples|      %|
	------------------
	        3 75.0000 gnome-power-manager
	        1 25.0000 [vdso] (tgid:1522 range:0x298000-0x299000)
        4 3.8e-05 ssh-agent
        4 3.8e-05 libgconf.so
        4 3.8e-05 clock-applet
	CPU_CLK_UNHALT...|
	  samples|      %|
	------------------
	        2 50.0000 clock-applet
	        2 50.0000 [vdso] (tgid:1642 range:0x32d000-0x32e000)
        4 3.8e-05 libavahi-common.so.3.5.2
        4 3.8e-05 libnspr4.so
        4 3.8e-05 libpixman-1.so.0.18.4
        4 3.8e-05 libGL.so.260.19.06
        3 2.8e-05 libz.so.1.2.3.4
        3 2.8e-05 pam_ecryptfs.so
        3 2.8e-05 expr
        3 2.8e-05 gedit
	CPU_CLK_UNHALT...|
	  samples|      %|
	------------------
	        3 100.000 [vdso] (tgid:4336 range:0xe67000-0xe68000)
        3 2.8e-05 libkeybindings.so
        3 2.8e-05 libck-connector.so.0.0.0
        3 2.8e-05 rtkit-daemon
        3 2.8e-05 cron
        2 1.9e-05 mkdir
        2 1.9e-05 libcrypt-2.12.1.so
        2 1.9e-05 libnih.so.1.0.0
        2 1.9e-05 libnsl-2.12.1.so
        2 1.9e-05 libnss_dns-2.12.1.so
        2 1.9e-05 pam_ck_connector.so
        2 1.9e-05 pam_env.so
        2 1.9e-05 mount.ecryptfs_private
        2 1.9e-05 dirname
        2 1.9e-05 id
        2 1.9e-05 libezoom.so
        2 1.9e-05 libworkarounds.so
        2 1.9e-05 wnck-applet
	CPU_CLK_UNHALT...|
	  samples|      %|
	------------------
	        2 100.000 [vdso] (tgid:1627 range:0x5a9000-0x5aa000)
        2 1.9e-05 libhousekeeping.so
        2 1.9e-05 libmedia-keys.so
        2 1.9e-05 libmouse.so
        2 1.9e-05 libxrandr.so
        2 1.9e-05 libavahi-core.so.7.0.0
        2 1.9e-05 libecryptfs.so.0.0.0
        2 1.9e-05 libgnome-desktop-2.so.17.1.4
        2 1.9e-05 libgnome-keyring.so.0.1.1
        2 1.9e-05 libk5crypto.so.3.1
        2 1.9e-05 libnss3.so
        2 1.9e-05 libsmime3.so
        2 1.9e-05 pango-basic-fc.so
        2 1.9e-05 polkit-gnome-authentication-agent-1
        2 1.9e-05 avahi-daemon
	CPU_CLK_UNHALT...|
	  samples|      %|
	------------------
	        1 50.0000 avahi-daemon
	        1 50.0000 [vdso] (tgid:832 range:0xe86000-0xe87000)
        1 9.4e-06 sleep
        1 9.4e-06 libacl.so.1.1.0
        1 9.4e-06 libattr.so.1.1.0
        1 9.4e-06 libgcc_s.so.1
        1 9.4e-06 libkeyutils.so.1.3
        1 9.4e-06 libnss_mdns4.so.2
        1 9.4e-06 libnss_mdns4_minimal.so.2
        1 9.4e-06 libpam_misc.so.0.82.0
        1 9.4e-06 libwrap.so.0.7.6
        1 9.4e-06 pam_gnome_keyring.so
        1 9.4e-06 pam_mail.so
        1 9.4e-06 pam_motd.so
        1 9.4e-06 pam_nologin.so
        1 9.4e-06 bluetooth-applet
	CPU_CLK_UNHALT...|
	  samples|      %|
	------------------
	        1 100.000 [vdso] (tgid:1550 range:0x726000-0x727000)
        1 9.4e-06 opjitconv
        1 9.4e-06 libXfixes.so.3.1.0
        1 9.4e-06 libbonoboui-2.so.0.0.0
        1 9.4e-06 libnssutil3.so
        1 9.4e-06 libpanel-applet-2.so.0.2.68
        1 9.4e-06 libssl3.so
        1 9.4e-06 libglx.so.260.19.06
        1 9.4e-06 libbluetooth-util.so
        1 9.4e-06 imuxsock.so
 
Tue Sep 20 19:18:46 CDT 2011
CPU: Intel Atom, speed 1795.72 MHz (estimated)
Counted INST_RETIRED events (number of instructions retired) with a unit mask of 0x01 (No unit mask) count 10000
INST_RETIRED:1...|
  samples|      %|
------------------
  6536892 96.7327 seti_boinc
   196153  2.9027 oprofiled
     8937  0.1322 libc-2.12.1.so
     5060  0.0749 bash
	INST_RETIRED:1...|
	  samples|      %|
	------------------
	     5059 99.9802 bash
	        1  0.0198 [vdso] (tgid:6918 range:0x483000-0x484000)
     3682  0.0545 libcairo.so.2.11000.0
     2641  0.0391 ld-2.12.1.so
      838  0.0124 dbus-daemon
      623  0.0092 libglib-2.0.so.0.2600.1
      536  0.0079 libdbus-1.so.3.5.2
      355  0.0053 libpthread-2.12.1.so
      321  0.0048 libgobject-2.0.so.0.2600.1
      296  0.0044 Xorg
      270  0.0040 ophelp
      189  0.0028 nvidia_drv.so
      181  0.0027 libORBit-2.so.0.1.0
      143  0.0021 libgconf-2.so.4.1.5
       62 9.2e-04 libpam.so.0.82.2
       45 6.7e-04 libgdk-x11-2.0.so.0.2200.0
       41 6.1e-04 libX11.so.6.3.0
       41 6.1e-04 libpangoft2-1.0.so.0.2800.2
       35 5.2e-04 no-vmlinux
       33 4.9e-04 mawk
       32 4.7e-04 dash
       28 4.1e-04 grep
       25 3.7e-04 libdbus-glib-1.so.2.1.0
       23 3.4e-04 libxcb.so.1.1.0
       16 2.4e-04 NetworkManager
       16 2.4e-04 irqbalance
       14 2.1e-04 sudo
       14 2.1e-04 libgthread-2.0.so.0.2600.1
       13 1.9e-04 libpango-1.0.so.0.2800.2
       11 1.6e-04 compiz
       11 1.6e-04 libnvidia-glcore.so.260.19.06
       11 1.6e-04 rsyslogd
        9 1.3e-04 libgtk-x11-2.0.so.0.2200.0
        8 1.2e-04 libnm-util.so.1.6.0
        5 7.4e-05 libnss_compat-2.12.1.so
        5 7.4e-05 wpa_supplicant
        5 7.4e-05 libgconfbackend-xml.so
        5 7.4e-05 gconfd-2
        5 7.4e-05 libgio-2.0.so.0.2600.1
        4 5.9e-05 libm-2.12.1.so
        3 4.4e-05 libnss_files-2.12.1.so
        3 4.4e-05 nm-applet
        3 4.4e-05 libnm-glib.so.2.4.1
        2 3.0e-05 ls
        2 3.0e-05 libcrypto.so.0.9.8
        2 3.0e-05 libfade.so
        2 3.0e-05 libscale.so
        2 3.0e-05 libpangocairo-1.0.so.0.2800.2
        2 3.0e-05 libxklavier.so.16.0.0
        2 3.0e-05 rtkit-daemon
        2 3.0e-05 udisks-daemon
	INST_RETIRED:1...|
	  samples|      %|
	------------------
	        2 100.000 [vdso] (tgid:1601 range:0x77a000-0x77b000)
        2 3.0e-05 libextmod.so
        2 3.0e-05 sshd
	INST_RETIRED:1...|
	  samples|      %|
	------------------
	        1 50.0000 sshd
	        1 50.0000 [vdso] (tgid:3059 range:0x1e3000-0x1e4000)
        1 1.5e-05 libdl-2.12.1.so
        1 1.5e-05 libpopt.so.0.0.0
        1 1.5e-05 librt-2.12.1.so
        1 1.5e-05 libselinux.so.1
        1 1.5e-05 pam_env.so
        1 1.5e-05 pam_limits.so
        1 1.5e-05 gnome-panel
	INST_RETIRED:1...|
	  samples|      %|
	------------------
	        1 100.000 [vdso] (tgid:1549 range:0xac4000-0xac5000)
        1 1.5e-05 libanimation.so
        1 1.5e-05 libdecoration.so
        1 1.5e-05 libezoom.so
        1 1.5e-05 libmove.so
        1 1.5e-05 libsession.so
        1 1.5e-05 libstaticswitcher.so
        1 1.5e-05 libwall.so
        1 1.5e-05 libgconf.so
        1 1.5e-05 liba11y-keyboard.so
        1 1.5e-05 libmouse.so
        1 1.5e-05 libmurrine.so
        1 1.5e-05 gvfs-afc-volume-monitor
	INST_RETIRED:1...|
	  samples|      %|
	------------------
	        1 100.000 [vdso] (tgid:1613 range:0x45d000-0x45e000)
        1 1.5e-05 libXdamage.so.1.1.0
        1 1.5e-05 libcompizconfig.so.0.0.0
        1 1.5e-05 libgnome-keyring.so.0.1.1
        1 1.5e-05 libpulse-mainloop-glib.so.0.0.4
        1 1.5e-05 libstartup-notification-1.so.0.0.0
        1 1.5e-05 libwnck-1.so.22.3.30
        1 1.5e-05 libwfb.so
 
Tue Sep 20 19:20:50 CDT 2011
CPU: Intel Atom, speed 1795.72 MHz (estimated)
Counted LLC_MISSES events (Last level cache demand requests from this core that missed the LLC) with a unit mask of 0x41 (No unit mask) count 10000
 LLC_MISSES:10000|
  samples|      %|
------------------
    26964 99.6821 seti_boinc
       13  0.0481 libc-2.12.1.so
       11  0.0407 ld-2.12.1.so
        9  0.0333 libglib-2.0.so.0.2600.1
        7  0.0259 bash
        7  0.0259 libdbus-1.so.3.5.2
        7  0.0259 Xorg
        5  0.0185 compiz
        5  0.0185 libgdk-x11-2.0.so.0.2200.0
        3  0.0111 no-vmlinux
        2  0.0074 dbus-daemon
        2  0.0074 libORBit-2.so.0.1.0
        2  0.0074 libX11.so.6.3.0
        2  0.0074 libgobject-2.0.so.0.2600.1
        1  0.0037 grep
        1  0.0037 libpthread-2.12.1.so
        1  0.0037 libvpswitch.so
        1  0.0037 gnome-settings-daemon
	 LLC_MISSES:10000|
	  samples|      %|
	------------------
	        1 100.000 [vdso] (tgid:1523 range:0x579000-0x57a000)
        1  0.0037 libdbus-glib-1.so.2.1.0
        1  0.0037 libgthread-2.0.so.0.2600.1
        1  0.0037 libgvfscommon.so.0.0.0
        1  0.0037 libpixman-1.so.0.18.4
        1  0.0037 libGL.so.260.19.06
        1  0.0037 nvidia_drv.so
        1  0.0037 NetworkManager
 
Tue Sep 20 19:22:53 CDT 2011
CPU: Intel Atom, speed 1795.72 MHz (estimated)
Counted LLC_REFS events (Last level cache demand requests from this core) with a unit mask of 0x4f (No unit mask) count 10000
   LLC_REFS:10000|
  samples|      %|
------------------
   183647 99.7626 seti_boinc
	   LLC_REFS:10000|
	  samples|      %|
	------------------
	   183646 99.9995 seti_boinc
	        1 5.4e-04 [vdso] (tgid:6081 range:0x2a3000-0x2a4000)
       77  0.0418 libc-2.12.1.so
       62  0.0337 ld-2.12.1.so
       51  0.0277 bash
       44  0.0239 libcairo.so.2.11000.0
       30  0.0163 libglib-2.0.so.0.2600.1
       24  0.0130 oprofiled
       23  0.0125 dbus-daemon
       20  0.0109 no-vmlinux
       20  0.0109 Xorg
       13  0.0071 libdbus-1.so.3.5.2
       13  0.0071 libX11.so.6.3.0
       11  0.0060 libgobject-2.0.so.0.2600.1
       10  0.0054 libpthread-2.12.1.so
        8  0.0043 libgdk-x11-2.0.so.0.2200.0
        5  0.0027 compiz
        4  0.0022 libxcb.so.1.1.0
        3  0.0016 mawk
        3  0.0016 nvidia_drv.so
        2  0.0011 libpam.so.0.82.2
        2  0.0011 libgio-2.0.so.0.2600.1
        1 5.4e-04 grep
        1 5.4e-04 libncurses.so.5.7
        1 5.4e-04 libanimation.so
        1 5.4e-04 libscaleaddon.so
        1 5.4e-04 libORBit-2.so.0.1.0
        1 5.4e-04 libdbus-glib-1.so.2.1.0
        1 5.4e-04 libgthread-2.0.so.0.2600.1
        1 5.4e-04 libnm-glib.so.2.4.1
        1 5.4e-04 libstartup-notification-1.so.0.0.0
        1 5.4e-04 libnvidia-glcore.so.260.19.06
        1 5.4e-04 irqbalance
        1 5.4e-04 sshd
 
Tue Sep 20 19:24:57 CDT 2011
CPU: Intel Atom, speed 1795.72 MHz (estimated)
Counted BR_INST_RETIRED events (number of branch instructions retired) with a unit mask of 0x00 (any Retired branch instructions) count 10000
BR_INST_RETIRE...|
  samples|      %|
------------------
   706277 98.1040 seti_boinc
     5451  0.7572 libc-2.12.1.so
     3902  0.5420 oprofiled
     1100  0.1528 bash
      757  0.1051 libcairo.so.2.11000.0
      452  0.0628 ld-2.12.1.so
      421  0.0585 libdbus-1.so.3.5.2
      355  0.0493 dbus-daemon
      324  0.0450 libglib-2.0.so.0.2600.1
      246  0.0342 libgobject-2.0.so.0.2600.1
      177  0.0246 libpthread-2.12.1.so
       64  0.0089 ophelp
       56  0.0078 Xorg
	BR_INST_RETIRE...|
	  samples|      %|
	------------------
	       55 98.2143 Xorg
	        1  1.7857 [vdso] (tgid:1265 range:0x78d000-0x78e000)
       53  0.0074 libdbus-glib-1.so.2.1.0
       53  0.0074 libgdu.so.0.0.0
       48  0.0067 libgconf-2.so.4.1.5
       41  0.0057 libORBit-2.so.0.1.0
       17  0.0024 nvidia_drv.so
       14  0.0019 libX11.so.6.3.0
       12  0.0017 grep
       10  0.0014 libgdk-x11-2.0.so.0.2200.0
        9  0.0013 libpam.so.0.82.2
        8  0.0011 libgthread-2.0.so.0.2600.1
        7 9.7e-04 libxcb.so.1.1.0
        6 8.3e-04 dash
        6 8.3e-04 libudev.so.0.9.1
        5 6.9e-04 libgtk-x11-2.0.so.0.2200.0
        5 6.9e-04 libpangoft2-1.0.so.0.2800.2
        4 5.6e-04 sudo
        4 5.6e-04 libgio-2.0.so.0.2600.1
        4 5.6e-04 libpango-1.0.so.0.2800.2
        3 4.2e-04 no-vmlinux
        3 4.2e-04 mawk
        3 4.2e-04 libgconfbackend-xml.so
        3 4.2e-04 libnvidia-glcore.so.260.19.06
        2 2.8e-04 libatasmart.so.4.0.3
        2 2.8e-04 libm-2.12.1.so
        2 2.8e-04 compiz
        2 2.8e-04 nm-applet
        2 2.8e-04 libnm-util.so.1.6.0
        2 2.8e-04 udisks-daemon
        2 2.8e-04 rsyslogd
        1 1.4e-04 ls
        1 1.4e-04 libnss_compat-2.12.1.so
        1 1.4e-04 libnss_files-2.12.1.so
        1 1.4e-04 librt-2.12.1.so
        1 1.4e-04 tr
        1 1.4e-04 libscale.so
        1 1.4e-04 gvfs-gdu-volume-monitor
        1 1.4e-04 libpangocairo-1.0.so.0.2800.2
        1 1.4e-04 libusbmuxd.so.1.0.4
        1 1.4e-04 libxklavier.so.16.0.0
        1 1.4e-04 NetworkManager
        1 1.4e-04 irqbalance
        1 1.4e-04 sshd
 
Tue Sep 20 19:27:00 CDT 2011
CPU: Intel Atom, speed 1795.72 MHz (estimated)
Counted BR_MISS_PRED_RETIRED events (number of mispredicted branches retired (precise)) with a unit mask of 0x00 (No unit mask) count 10000
BR_MISS_PRED_R...|
  samples|      %|
------------------
    14453 97.8869 seti_boinc
       88  0.5960 bash
       85  0.5757 libc-2.12.1.so
       32  0.2167 ld-2.12.1.so
       25  0.1693 libcairo.so.2.11000.0
       15  0.1016 libdbus-1.so.3.5.2
       13  0.0880 dbus-daemon
	BR_MISS_PRED_R...|
	  samples|      %|
	------------------
	       12 92.3077 dbus-daemon
	        1  7.6923 [vdso] (tgid:821 range:0x259000-0x25a000)
       12  0.0813 libpthread-2.12.1.so
        9  0.0610 libglib-2.0.so.0.2600.1
        9  0.0610 libgobject-2.0.so.0.2600.1
        4  0.0271 Xorg
        4  0.0271 libgdk-x11-2.0.so.0.2200.0
        3  0.0203 mawk
        2  0.0135 ophelp
        2  0.0135 libX11.so.6.3.0
        1  0.0068 dash
        1  0.0068 libgcc_s.so.1
        1  0.0068 libnss_files-2.12.1.so
        1  0.0068 gtk-window-decorator
	BR_MISS_PRED_R...|
	  samples|      %|
	------------------
	        1 100.000 [vdso] (tgid:1621 range:0x387000-0x388000)
        1  0.0068 sudo
        1  0.0068 libdecoration.so
        1  0.0068 libdbus-glib-1.so.2.1.0
        1  0.0068 libgnome-desktop-2.so.17.1.4
        1  0.0068 libxcb.so.1.1.0
```