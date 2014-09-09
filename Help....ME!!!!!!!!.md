hi, my name is michael and i am having a problem with the emulator, open emu, ds. i am trying to go to some certain areas in the game "pokemon black 2" but my only problem is, when i try to enter 1 or 2 certain places, i get a black screen, the music stops, and i get a error report saying, "Could not Communicate with Helper application. i have no idea what this means, this has been a major problem for me and because of this, i cannot proceed in this game, and i am really loving it, so i would very much appreciate it if you could help me out with this, thank you and here is the full error report:

Process:         OpenEmuHelperApp [274]
Path:            /Users/USER/Desktop/OpenEmu.app/Contents/Resources/OpenEmuHelperApp
Identifier:      OpenEmuHelperApp
Version:         1.0 (1.0.3)
Code Type:       X86-64 (Native)
Parent Process:  OpenEmu [268]
Responsible:     OpenEmu [268]
User ID:         501

Date/Time:       2014-08-09 20:56:47.434 -0700
OS Version:      Mac OS X 10.9.4 (13E28)
Report Version:  11
Anonymous UUID:  EBF7B1C6-BBF9-4B31-4148-90FCB473F824

Sleep/Wake UUID: E4378B0F-9ABD-4A25-A889-C065E86CF1EB

Crashed Thread:  15

Exception Type:  EXC_BAD_ACCESS (SIGSEGV)
Exception Codes: KERN_INVALID_ADDRESS at 0x00000006e772b024

VM Regions Near 0x6e772b024:
    CG shared images       00000001c871f000-00000001c8727000 [   32K] r--/r-- SM=SHM  
--> 
    __TEXT                 0000123400000000-000012340047c000 [ 4592K] r-x/rwx SM=COW  /System/Library/Extensions/AppleIntelHD4000GraphicsGLDriver.bundle/Contents/MacOS/AppleIntelHD4000GraphicsGLDriver

Thread 0:: Dispatch queue: com.apple.main-thread
0   libsystem_kernel.dylib        	0x00007fff914faa1a mach_msg_trap + 10
1   libsystem_kernel.dylib        	0x00007fff914f9d18 mach_msg + 64
2   com.apple.CoreFoundation      	0x00007fff8bed9f15 __CFRunLoopServiceMachPort + 181
3   com.apple.CoreFoundation      	0x00007fff8bed9539 __CFRunLoopRun + 1161
4   com.apple.CoreFoundation      	0x00007fff8bed8e75 CFRunLoopRunSpecific + 309
5   com.apple.HIToolbox           	0x00007fff8aa3fa0d RunCurrentEventLoopInMode + 226
6   com.apple.HIToolbox           	0x00007fff8aa3f7b7 ReceiveNextEventCommon + 479
7   com.apple.HIToolbox           	0x00007fff8aa3f5bc _BlockUntilNextEventMatchingListInModeWithFilter + 65
8   com.apple.AppKit              	0x00007fff8df8524e _DPSNextEvent + 1434
9   com.apple.AppKit              	0x00007fff8df8489b -[NSApplication nextEventMatchingMask:untilDate:inMode:dequeue:] + 122
10  com.apple.AppKit              	0x00007fff8df7899c -[NSApplication run] + 553
11  OpenEmuHelperApp              	0x000000010b13babd -[OpenEmuXPCHelperApp launchApplication] + 77
12  OpenEmuHelperApp              	0x000000010b13b3d6 main + 99
13  OpenEmuHelperApp              	0x000000010b132f34 start + 52

Thread 1:
0   libsystem_kernel.dylib        	0x00007fff914fee6a __workq_kernreturn + 10
1   libsystem_pthread.dylib       	0x00007fff8d33bf08 _pthread_wqthread + 330
2   libsystem_pthread.dylib       	0x00007fff8d33efb9 start_wqthread + 13

Thread 2:: Dispatch queue: com.apple.libdispatch-manager
0   libsystem_kernel.dylib        	0x00007fff914ff662 kevent64 + 10
1   libdispatch.dylib             	0x00007fff91e3c421 _dispatch_mgr_invoke + 239
2   libdispatch.dylib             	0x00007fff91e3c136 _dispatch_mgr_thread + 52

Thread 3:
0   libsystem_kernel.dylib        	0x00007fff914fee6a __workq_kernreturn + 10
1   libsystem_pthread.dylib       	0x00007fff8d33bf08 _pthread_wqthread + 330
2   libsystem_pthread.dylib       	0x00007fff8d33efb9 start_wqthread + 13

Thread 4:
0   libsystem_kernel.dylib        	0x00007fff914fee6a __workq_kernreturn + 10
1   libsystem_pthread.dylib       	0x00007fff8d33bf08 _pthread_wqthread + 330
2   libsystem_pthread.dylib       	0x00007fff8d33efb9 start_wqthread + 13

Thread 5:
0   libsystem_kernel.dylib        	0x00007fff914faa1a mach_msg_trap + 10
1   libsystem_kernel.dylib        	0x00007fff914f9d18 mach_msg + 64
2   com.apple.CoreFoundation      	0x00007fff8bed9f15 __CFRunLoopServiceMachPort + 181
3   com.apple.CoreFoundation      	0x00007fff8bed9539 __CFRunLoopRun + 1161
4   com.apple.CoreFoundation      	0x00007fff8bed8e75 CFRunLoopRunSpecific + 309
5   com.apple.AppKit              	0x00007fff8e12505e _NSEventThread + 144
6   libsystem_pthread.dylib       	0x00007fff8d33a899 _pthread_body + 138
7   libsystem_pthread.dylib       	0x00007fff8d33a72a _pthread_start + 137
8   libsystem_pthread.dylib       	0x00007fff8d33efc9 thread_start + 13

Thread 6:
0   libsystem_kernel.dylib        	0x00007fff914fe716 __psynch_cvwait + 10
1   libsystem_pthread.dylib       	0x00007fff8d33cc3b _pthread_cond_wait + 727
2   org.openemu.desmume           	0x000000010f0cb09b taskProc(void*) + 59
3   libsystem_pthread.dylib       	0x00007fff8d33a899 _pthread_body + 138
4   libsystem_pthread.dylib       	0x00007fff8d33a72a _pthread_start + 137
5   libsystem_pthread.dylib       	0x00007fff8d33efc9 thread_start + 13

Thread 7:
0   libsystem_kernel.dylib        	0x00007fff914fe716 __psynch_cvwait + 10
1   libsystem_pthread.dylib       	0x00007fff8d33cc3b _pthread_cond_wait + 727
2   org.openemu.desmume           	0x000000010f0cb09b taskProc(void*) + 59
3   libsystem_pthread.dylib       	0x00007fff8d33a899 _pthread_body + 138
4   libsystem_pthread.dylib       	0x00007fff8d33a72a _pthread_start + 137
5   libsystem_pthread.dylib       	0x00007fff8d33efc9 thread_start + 13

Thread 8:
0   libsystem_kernel.dylib        	0x00007fff914fe716 __psynch_cvwait + 10
1   libsystem_pthread.dylib       	0x00007fff8d33cc3b _pthread_cond_wait + 727
2   org.openemu.desmume           	0x000000010f0cb09b taskProc(void*) + 59
3   libsystem_pthread.dylib       	0x00007fff8d33a899 _pthread_body + 138
4   libsystem_pthread.dylib       	0x00007fff8d33a72a _pthread_start + 137
5   libsystem_pthread.dylib       	0x00007fff8d33efc9 thread_start + 13

Thread 9:
0   libsystem_kernel.dylib        	0x00007fff914fe716 __psynch_cvwait + 10
1   libsystem_pthread.dylib       	0x00007fff8d33cc3b _pthread_cond_wait + 727
2   org.openemu.desmume           	0x000000010f0cb09b taskProc(void*) + 59
3   libsystem_pthread.dylib       	0x00007fff8d33a899 _pthread_body + 138
4   libsystem_pthread.dylib       	0x00007fff8d33a72a _pthread_start + 137
5   libsystem_pthread.dylib       	0x00007fff8d33efc9 thread_start + 13

Thread 10:
0   libsystem_kernel.dylib        	0x00007fff914fe716 __psynch_cvwait + 10
1   libsystem_pthread.dylib       	0x00007fff8d33cc3b _pthread_cond_wait + 727
2   org.openemu.desmume           	0x000000010f0cb09b taskProc(void*) + 59
3   libsystem_pthread.dylib       	0x00007fff8d33a899 _pthread_body + 138
4   libsystem_pthread.dylib       	0x00007fff8d33a72a _pthread_start + 137
5   libsystem_pthread.dylib       	0x00007fff8d33efc9 thread_start + 13

Thread 11:
0   libsystem_kernel.dylib        	0x00007fff914fe716 __psynch_cvwait + 10
1   libsystem_pthread.dylib       	0x00007fff8d33cc3b _pthread_cond_wait + 727
2   org.openemu.desmume           	0x000000010f0cb09b taskProc(void*) + 59
3   libsystem_pthread.dylib       	0x00007fff8d33a899 _pthread_body + 138
4   libsystem_pthread.dylib       	0x00007fff8d33a72a _pthread_start + 137
5   libsystem_pthread.dylib       	0x00007fff8d33efc9 thread_start + 13

Thread 12:
0   libsystem_kernel.dylib        	0x00007fff914fe716 __psynch_cvwait + 10
1   libsystem_pthread.dylib       	0x00007fff8d33cc3b _pthread_cond_wait + 727
2   org.openemu.desmume           	0x000000010f0cb09b taskProc(void*) + 59
3   libsystem_pthread.dylib       	0x00007fff8d33a899 _pthread_body + 138
4   libsystem_pthread.dylib       	0x00007fff8d33a72a _pthread_start + 137
5   libsystem_pthread.dylib       	0x00007fff8d33efc9 thread_start + 13

Thread 13:
0   libsystem_kernel.dylib        	0x00007fff914fe716 __psynch_cvwait + 10
1   libsystem_pthread.dylib       	0x00007fff8d33cc3b _pthread_cond_wait + 727
2   org.openemu.desmume           	0x000000010f0cb09b taskProc(void*) + 59
3   libsystem_pthread.dylib       	0x00007fff8d33a899 _pthread_body + 138
4   libsystem_pthread.dylib       	0x00007fff8d33a72a _pthread_start + 137
5   libsystem_pthread.dylib       	0x00007fff8d33efc9 thread_start + 13

Thread 14:
0   libsystem_kernel.dylib        	0x00007fff914fee6a __workq_kernreturn + 10
1   libsystem_pthread.dylib       	0x00007fff8d33bf08 _pthread_wqthread + 330
2   libsystem_pthread.dylib       	0x00007fff8d33efb9 start_wqthread + 13

Thread 15 Crashed:
0   org.openemu.desmume           	0x000000010f1420a0 void std::__final_insertion_sort<int*, bool (*)(int, int)>(int*, int*, bool (*)(int, int)) + 464
1   org.openemu.desmume           	0x000000010f186f85 Sequencer::execHardware() + 1925
2   org.openemu.desmume           	0x000000010f18cfd7 void NDS_exec<false>(int) + 6039
3   org.openemu.desmume           	0x000000010f042e1b -[NDSGameCore executeFrame] + 107
4   org.openemu.OpenEmuBase       	0x000000010b33da76 -[OEGameCore frameRefreshThread:] + 370
5   com.apple.Foundation          	0x00007fff91fa2cb7 __NSFireDelayedPerform + 333
6   com.apple.CoreFoundation      	0x00007fff8bf1e3e4 __CFRUNLOOP_IS_CALLING_OUT_TO_A_TIMER_CALLBACK_FUNCTION__ + 20
7   com.apple.CoreFoundation      	0x00007fff8bf1df1f __CFRunLoopDoTimer + 1151
8   com.apple.CoreFoundation      	0x00007fff8bf8f5aa __CFRunLoopDoTimers + 298
9   com.apple.CoreFoundation      	0x00007fff8bed96a5 __CFRunLoopRun + 1525
10  com.apple.CoreFoundation      	0x00007fff8bed8e75 CFRunLoopRunSpecific + 309
11  com.apple.CoreFoundation      	0x00007fff8bf8e811 CFRunLoopRun + 97
12  OpenEmuHelperApp              	0x000000010b139c76 -[OpenEmuHelperApp OE_gameCoreThread:] + 207
13  com.apple.Foundation          	0x00007fff91fa576b __NSThread__main__ + 1318
14  libsystem_pthread.dylib       	0x00007fff8d33a899 _pthread_body + 138
15  libsystem_pthread.dylib       	0x00007fff8d33a72a _pthread_start + 137
16  libsystem_pthread.dylib       	0x00007fff8d33efc9 thread_start + 13

Thread 16:
0   libsystem_kernel.dylib        	0x00007fff914fee6a __workq_kernreturn + 10
1   libsystem_pthread.dylib       	0x00007fff8d33bf08 _pthread_wqthread + 330
2   libsystem_pthread.dylib       	0x00007fff8d33efb9 start_wqthread + 13

Thread 17:
0   libsystem_kernel.dylib        	0x00007fff914fee6a __workq_kernreturn + 10
1   libsystem_pthread.dylib       	0x00007fff8d33bf08 _pthread_wqthread + 330
2   libsystem_pthread.dylib       	0x00007fff8d33efb9 start_wqthread + 13

Thread 18:: com.apple.audio.IOThread.client
0   libsystem_kernel.dylib        	0x00007fff914faa1a mach_msg_trap + 10
1   libsystem_kernel.dylib        	0x00007fff914f9d18 mach_msg + 64
2   com.apple.audio.CoreAudio     	0x00007fff8a2af828 HALB_MachPort::SendMessageWithReply(unsigned int, unsigned int, unsigned int, unsigned int, mach_msg_header_t*, bool, unsigned int) + 98
3   com.apple.audio.CoreAudio     	0x00007fff8a2af7b6 HALB_MachPort::SendSimpleMessageWithSimpleReply(unsigned int, unsigned int, int, int&, bool, unsigned int) + 42
4   com.apple.audio.CoreAudio     	0x00007fff8a2adf3e HALC_ProxyIOContext::IOWorkLoop() + 950
5   com.apple.audio.CoreAudio     	0x00007fff8a2adadd HALC_ProxyIOContext::IOThreadEntry(void*) + 97
6   com.apple.audio.CoreAudio     	0x00007fff8a2ad99d HALB_IOThread::Entry(void*) + 75
7   libsystem_pthread.dylib       	0x00007fff8d33a899 _pthread_body + 138
8   libsystem_pthread.dylib       	0x00007fff8d33a72a _pthread_start + 137
9   libsystem_pthread.dylib       	0x00007fff8d33efc9 thread_start + 13

Thread 19:
0   libsystem_kernel.dylib        	0x00007fff914fee6a __workq_kernreturn + 10
1   libsystem_pthread.dylib       	0x00007fff8d33bf08 _pthread_wqthread + 330
2   libsystem_pthread.dylib       	0x00007fff8d33efb9 start_wqthread + 13

Thread 15 crashed with X86 Thread State (64-bit):
  rax: 0x00000000b8619000  rbx: 0x0000000124663000  rcx: 0x0000000024e05000  rdx: 0x000000012466e240
  rdi: 0x0000000000001644  rsi: 0x000000010f48b898  rbp: 0x000000012d238f10  rsp: 0x000000012d238ee0
   r8: 0x0000000000000474   r9: 0x000000010f48ccf8  r10: 0x000000010f48b9a0  r11: 0x0000000000000004
  r12: 0x000000010f48c928  r13: 0x000000010f48b8d4  r14: 0x000000000000002c  r15: 0x000000010f48b898
  rip: 0x000000010f1420a0  rfl: 0x0000000000010213  cr2: 0x00000006e772b024
  
Logical CPU:     3
Error Code:      0x00000004
Trap Number:     14


Binary Images:
       0x10b131000 -        0x10b146ff7 +OpenEmuHelperApp (1.0 - 1.0.3) <374A6458-37C0-3FBB-9383-D8E2E164B320> /Users/USER/Desktop/OpenEmu.app/Contents/Resources/OpenEmuHelperApp
       0x10b165000 -        0x10b267ff7 +de.dstoecker.xadmaster (3.3 [libxad 13.0, modified]) <2E573080-75D7-3705-9E0F-369F91CE9D2B> /Users/USER/Desktop/OpenEmu.app/Contents/Frameworks/XADMaster.framework/Versions/A/XADMaster
       0x10b33c000 -        0x10b343ff7 +org.openemu.OpenEmuBase (1.0 - 1) <0E6503B6-96F7-3679-81F2-275014850C68> /Users/USER/Desktop/OpenEmu.app/Contents/Frameworks/OpenEmuBase.framework/Versions/A/OpenEmuBase
       0x10b352000 -        0x10b391fff +org.openemu.OpenEmuSystem (1.0 - 1) <F4EFE891-77C1-3A1A-873C-DD0475B33D4D> /Users/USER/Desktop/OpenEmu.app/Contents/Frameworks/OpenEmuSystem.framework/Versions/A/OpenEmuSystem
       0x10b3e0000 -        0x10b3e4ff7 +org.openemu.OpenEmuXPCCommunicator (1.0 - 1) <91941FAB-889B-37C1-BBB9-59DB7B578AF6> /Users/USER/Desktop/OpenEmu.app/Contents/Frameworks/OpenEmuXPCCommunicator.framework/Versions/A/OpenEmuXPCCommunicator
       0x10b3ee000 -        0x10b400fff +org.mozilla.universalchardet (1.1) <08F9A88E-917F-3C09-B479-EB7C1A9D2CB6> /Users/USER/Desktop/OpenEmu.app/Contents/Frameworks/UniversalDetector.framework/Versions/A/UniversalDetector
       0x10b415000 -        0x10b417fff  com.apple.ForceFeedback (1.0.6 - 1.0.6) <D21AD43F-147B-3B50-89AB-26695EB89998> /System/Library/Frameworks/ForceFeedback.framework/Versions/A/ForceFeedback
       0x10b5ec000 -        0x10b5eefff +org.openemu.NDS (1.0 - 1) <74651C60-2220-397B-A300-8EF203F3673C> /Users/USER/Desktop/OpenEmu.app/Contents/PlugIns/Systems/NDS.oesystemplugin/Contents/MacOS/NDS
       0x10f041000 -        0x10f349fff +org.openemu.desmume (v0.9.10 [OpenEmu Plug-in] - 0.9.10.2) <43B255AA-0040-3C66-A385-8A42F8A29F65> /Users/USER/Library/Application Support/OpenEmu/*/DeSmuME
       0x12d57d000 -        0x12d74efff  com.apple.audio.units.Components (1.10 - 1.10) <F74A9407-DDB5-3C4F-A051-47643871ED93> /System/Library/Components/CoreAudio.component/Contents/MacOS/CoreAudio
       0x12d809000 -        0x12d80dffd  com.apple.audio.AppleHDAHALPlugIn (2.6.3 - 2.6.3f4) <2EB88B27-FA19-3C0C-AA06-7FB8BC56694E> /System/Library/Extensions/AppleHDA.kext/Contents/PlugIns/AppleHDAHALPlugIn.bundle/Contents/MacOS/AppleHDAHALPlugIn
    0x123400000000 -     0x12340047bff7  com.apple.driver.AppleIntelHD4000GraphicsGLDriver (8.28.30 - 8.2.8) <348EFC98-A497-36C3-8AEB-6E33BA34EEB5> /System/Library/Extensions/AppleIntelHD4000GraphicsGLDriver.bundle/Contents/MacOS/AppleIntelHD4000GraphicsGLDriver
    0x123440000000 -     0x123440882ff7  com.apple.GeForceGLDriver (8.26.26 - 8.2.6) <5CF90B2D-22CB-360C-9B0B-DC15A4B9CE8B> /System/Library/Extensions/GeForceGLDriver.bundle/Contents/MacOS/GeForceGLDriver
    0x7fff6f909000 -     0x7fff6f93c817  dyld (239.4) <042C4CED-6FB2-3B1C-948B-CAF2EE3B9F7A> /usr/lib/dyld
    0x7fff885df000 -     0x7fff885e5fff  com.apple.AOSNotification (1.7.0 - 760.3) <7901B867-60F7-3645-BB3E-18C51A6FBCC6> /System/Library/PrivateFrameworks/AOSNotification.framework/Versions/A/AOSNotification
    0x7fff885e6000 -     0x7fff885eeff3  libCGCMS.A.dylib (599.25.10.1) <9A4FAAD7-1C16-33F8-A615-1DCAB0546E31> /System/Library/Frameworks/CoreGraphics.framework/Versions/A/Resources/libCGCMS.A.dylib
    0x7fff885f0000 -     0x7fff885fbfff  libGL.dylib (9.6.1) <4B65BF9F-F34A-3CD1-94E8-DB26DAA0A59D> /System/Library/Frameworks/OpenGL.framework/Versions/A/Libraries/libGL.dylib
    0x7fff88650000 -     0x7fff88677ffb  libsystem_info.dylib (449.1.3) <7D41A156-D285-3849-A2C3-C04ADE797D98> /usr/lib/system/libsystem_info.dylib
    0x7fff88678000 -     0x7fff88f9832b  com.apple.CoreGraphics (1.600.0 - 599.25.10.1) <EC14B831-96BB-3A50-A451-E36BDC8F59FB> /System/Library/Frameworks/CoreGraphics.framework/Versions/A/CoreGraphics
    0x7fff88fc8000 -     0x7fff89015ff2  com.apple.print.framework.PrintCore (9.0 - 428) <8D8253E3-302F-3DB2-9C5C-572CB974E8B3> /System/Library/Frameworks/ApplicationServices.framework/Versions/A/Frameworks/PrintCore.framework/Versions/A/PrintCore
    0x7fff8901f000 -     0x7fff8901ffff  com.apple.CoreServices (59 - 59) <7A697B5E-F179-30DF-93F2-8B503CEEEFD5> /System/Library/Frameworks/CoreServices.framework/Versions/A/CoreServices
    0x7fff89020000 -     0x7fff89062ff7  libauto.dylib (185.5) <F45C36E8-B606-3886-B5B1-B6745E757CA8> /usr/lib/libauto.dylib
    0x7fff890b6000 -     0x7fff890fdfff  libFontRegistry.dylib (127) <A77A0480-AA5D-3CC8-8B68-69985CD546DC> /System/Library/Frameworks/ApplicationServices.framework/Versions/A/Frameworks/ATS.framework/Versions/A/Resources/libFontRegistry.dylib
    0x7fff890fe000 -     0x7fff89106fff  libsystem_dnssd.dylib (522.92.1) <17B03FFD-92C5-3282-9981-EBB28B456207> /usr/lib/system/libsystem_dnssd.dylib
    0x7fff89107000 -     0x7fff89116ff8  com.apple.LangAnalysis (1.7.0 - 1.7.0) <8FE131B6-1180-3892-98F5-C9C9B79072D4> /System/Library/Frameworks/ApplicationServices.framework/Versions/A/Frameworks/LangAnalysis.framework/Versions/A/LangAnalysis
    0x7fff89117000 -     0x7fff8911affc  com.apple.IOSurface (91.1 - 91.1) <D00EEB0C-8AA8-3986-90C1-C97B2486E8FA> /System/Library/Frameworks/IOSurface.framework/Versions/A/IOSurface
    0x7fff8927c000 -     0x7fff89297ff7  libsystem_malloc.dylib (23.10.1) <A695B4E4-38E9-332E-A772-29D31E3F1385> /usr/lib/system/libsystem_malloc.dylib
    0x7fff896bf000 -     0x7fff896c8ff7  libcldcpuengine.dylib (2.3.58) <E3A84FEC-4060-39C2-A469-159A443D2B6D> /System/Library/Frameworks/OpenCL.framework/Versions/A/Libraries/libcldcpuengine.dylib
    0x7fff89714000 -     0x7fff89714ff7  libkeymgr.dylib (28) <3AA8D85D-CF00-3BD3-A5A0-E28E1A32A6D8> /usr/lib/system/libkeymgr.dylib
    0x7fff89737000 -     0x7fff898d7ff7  GLEngine (9.6.1) <28300FBD-E3B2-35D2-BB54-77DCE62FC371> /System/Library/Frameworks/OpenGL.framework/Versions/A/Resources/GLEngine.bundle/GLEngine
    0x7fff89b6a000 -     0x7fff89bc2ff7  com.apple.Symbolication (1.4 - 129.0.2) <B1F008C4-184D-36A2-922F-4A67A075D512> /System/Library/PrivateFrameworks/Symbolication.framework/Versions/A/Symbolication
    0x7fff89bd0000 -     0x7fff89bebff7  libPng.dylib (1043) <23D2DAB7-C9A9-392F-989A-871E89E7751D> /System/Library/Frameworks/ImageIO.framework/Versions/A/Resources/libPng.dylib
    0x7fff89c1d000 -     0x7fff89c21fff  com.apple.CommonPanels (1.2.6 - 96) <6B434AFD-50F8-37C7-9A56-162C17E375B3> /System/Library/Frameworks/Carbon.framework/Versions/A/Frameworks/CommonPanels.framework/Versions/A/CommonPanels
    0x7fff89c22000 -     0x7fff89c2bfff  com.apple.speech.synthesis.framework (4.7.1 - 4.7.1) <383FB557-E88E-3239-82B8-15F9F885B702> /System/Library/Frameworks/ApplicationServices.framework/Versions/A/Frameworks/SpeechSynthesis.framework/Versions/A/SpeechSynthesis
    0x7fff89c2c000 -     0x7fff89c37fff  libGPUSupportMercury.dylib (9.6.1) <A34D5C51-28E0-398A-881D-552B47D2DD3C> /System/Library/PrivateFrameworks/GPUSupport.framework/Versions/A/Libraries/libGPUSupportMercury.dylib
    0x7fff89c42000 -     0x7fff89db0ff7  libBLAS.dylib (1094.5) <DE93A590-5FA5-32A2-A16C-5D7D7361769F> /System/Library/Frameworks/Accelerate.framework/Versions/A/Frameworks/vecLib.framework/Versions/A/libBLAS.dylib
    0x7fff89e11000 -     0x7fff89e2cff7  libCRFSuite.dylib (34) <FFAE75FA-C54E-398B-AA97-18164CD9789D> /usr/lib/libCRFSuite.dylib
    0x7fff89e2d000 -     0x7fff89e62ffc  com.apple.LDAPFramework (2.4.28 - 194.5) <4ADD0595-25B9-3F09-897E-3FB790AD2C5A> /System/Library/Frameworks/LDAP.framework/Versions/A/LDAP
    0x7fff89e70000 -     0x7fff89e74ff7  libsystem_stats.dylib (93.90.3) <4E51D5B0-92A0-3D0D-B90E-495A1ED3E391> /usr/lib/system/libsystem_stats.dylib
    0x7fff89e75000 -     0x7fff8a15ffff  com.apple.CoreServices.CarbonCore (1077.17 - 1077.17) <3A2E92FD-DEE2-3D45-9619-11500801A61C> /System/Library/Frameworks/CoreServices.framework/Versions/A/Frameworks/CarbonCore.framework/Versions/A/CarbonCore
    0x7fff8a185000 -     0x7fff8a189ff7  libcache.dylib (62) <BDC1E65B-72A1-3DA3-A57C-B23159CAAD0B> /usr/lib/system/libcache.dylib
    0x7fff8a287000 -     0x7fff8a2d8ff7  com.apple.audio.CoreAudio (4.2.1 - 4.2.1) <BE13E840-FB45-3BC2-BCF5-031629754FD5> /System/Library/Frameworks/CoreAudio.framework/Versions/A/CoreAudio
    0x7fff8a2d9000 -     0x7fff8a2e4ff7  com.apple.NetAuth (5.0 - 5.0) <C811E662-9EC3-3B74-808A-A75D624F326B> /System/Library/PrivateFrameworks/NetAuth.framework/Versions/A/NetAuth
    0x7fff8a335000 -     0x7fff8a3e5ff7  libvMisc.dylib (423.32) <049C0735-1808-39B9-943F-76CB8021744F> /System/Library/Frameworks/Accelerate.framework/Versions/A/Frameworks/vecLib.framework/Versions/A/libvMisc.dylib
    0x7fff8a8ac000 -     0x7fff8a8adfff  libsystem_sandbox.dylib (278.11.1) <0D0B13EA-6B7A-3AC8-BE60-B548543BEB77> /usr/lib/system/libsystem_sandbox.dylib
    0x7fff8a8de000 -     0x7fff8a94afff  com.apple.framework.IOKit (2.0.1 - 907.100.13) <057FDBA3-56D6-3903-8C0B-849214BF1985> /System/Library/Frameworks/IOKit.framework/Versions/A/IOKit
    0x7fff8a94b000 -     0x7fff8a97ffff  libssl.0.9.8.dylib (50) <B15F967C-B002-36C2-9621-3456D8509F50> /usr/lib/libssl.0.9.8.dylib
    0x7fff8aa03000 -     0x7fff8aa10ff7  libxar.1.dylib (202) <5572AA71-E98D-3FE1-9402-BB4A84E0E71E> /usr/lib/libxar.1.dylib
    0x7fff8aa11000 -     0x7fff8acbbff5  com.apple.HIToolbox (2.1.1 - 698) <A388E773-AE7B-3FD1-8662-A98E6E24EA16> /System/Library/Frameworks/Carbon.framework/Versions/A/Frameworks/HIToolbox.framework/Versions/A/HIToolbox
    0x7fff8acbc000 -     0x7fff8acd5ff7  com.apple.Kerberos (3.0 - 1) <F108AFEB-198A-3BAF-BCA5-9DFCE55EFF92> /System/Library/Frameworks/Kerberos.framework/Versions/A/Kerberos
    0x7fff8acd6000 -     0x7fff8acd8ffb  libutil.dylib (34) <DAC4A6CF-A1BB-3874-9569-A919316D30E8> /usr/lib/libutil.dylib
    0x7fff8ad72000 -     0x7fff8adb0ff7  libGLImage.dylib (9.6.1) <5E02B38C-9F36-39BE-8746-724F0D8BBFC0> /System/Library/Frameworks/OpenGL.framework/Versions/A/Libraries/libGLImage.dylib
    0x7fff8adb1000 -     0x7fff8adb2ff7  libDiagnosticMessagesClient.dylib (100) <4CDB0F7B-C0AF-3424-BC39-495696F0DB1E> /usr/lib/libDiagnosticMessagesClient.dylib
    0x7fff8adb3000 -     0x7fff8ae92fff  libcrypto.0.9.8.dylib (50) <B95B9DBA-39D3-3EEF-AF43-44608B28894E> /usr/lib/libcrypto.0.9.8.dylib
    0x7fff8ae93000 -     0x7fff8aebbffb  libxslt.1.dylib (13) <C9794936-633C-3F0C-9E71-30190B9B41C1> /usr/lib/libxslt.1.dylib
    0x7fff8aebc000 -     0x7fff8af01fff  libcurl.4.dylib (78.94.1) <88F27F9B-052E-3375-938D-2603E90D8AD5> /usr/lib/libcurl.4.dylib
    0x7fff8af17000 -     0x7fff8af17ffd  com.apple.audio.units.AudioUnit (1.10 - 1.10) <68B21135-55A6-3563-A3D6-3E692A7DEB7F> /System/Library/Frameworks/AudioUnit.framework/Versions/A/AudioUnit
    0x7fff8af18000 -     0x7fff8afffff7  libxml2.2.dylib (26) <A1DADD11-89E5-3DE4-8802-07186225967F> /usr/lib/libxml2.2.dylib
    0x7fff8b03a000 -     0x7fff8b07fff6  com.apple.HIServices (1.23 - 468) <5970AF5C-F5BD-3B6A-97C9-95B2CA98D71D> /System/Library/Frameworks/ApplicationServices.framework/Versions/A/Frameworks/HIServices.framework/Versions/A/HIServices
    0x7fff8b080000 -     0x7fff8b351ff4  com.apple.CoreImage (9.4.0) <2C636ECD-0F1A-357C-9EFF-0452476FDDF5> /System/Library/Frameworks/QuartzCore.framework/Versions/A/Frameworks/CoreImage.framework/Versions/A/CoreImage
    0x7fff8b358000 -     0x7fff8b35ffff  com.apple.NetFS (6.0 - 4.0) <8E26C099-CE9D-3819-91A2-64EA929C6137> /System/Library/Frameworks/NetFS.framework/Versions/A/NetFS
    0x7fff8b4de000 -     0x7fff8b542fff  com.apple.datadetectorscore (5.0 - 354.5) <0AE9749A-6BFC-3032-B802-210DF59AEDB0> /System/Library/PrivateFrameworks/DataDetectorsCore.framework/Versions/A/DataDetectorsCore
    0x7fff8b8e5000 -     0x7fff8b8e8fff  com.apple.TCC (1.0 - 1) <32A075D9-47FD-3E71-95BC-BFB0D583F41C> /System/Library/PrivateFrameworks/TCC.framework/Versions/A/TCC
    0x7fff8bd05000 -     0x7fff8bd2cff7  libsystem_network.dylib (241.3) <8B1E1F1D-A5CC-3BAE-8B1E-ABC84337A364> /usr/lib/system/libsystem_network.dylib
    0x7fff8bd45000 -     0x7fff8bd76fff  com.apple.MediaKit (15 - 709) <23E33409-5C39-3F93-9E73-2B0E9EE8883E> /System/Library/PrivateFrameworks/MediaKit.framework/Versions/A/MediaKit
    0x7fff8bda0000 -     0x7fff8bdb7ff7  com.apple.CFOpenDirectory (10.9 - 173.90.1) <EBC0A1F2-9054-3D39-99AE-A3F655E55D6A> /System/Library/Frameworks/OpenDirectory.framework/Versions/A/Frameworks/CFOpenDirectory.framework/Versions/A/CFOpenDirectory
    0x7fff8be3c000 -     0x7fff8be49ff0  libbz2.1.0.dylib (29) <0B98AC35-B138-349C-8063-2B987A75D24C> /usr/lib/libbz2.1.0.dylib
    0x7fff8be4a000 -     0x7fff8be4bffb  libremovefile.dylib (33) <3543F917-928E-3DB2-A2F4-7AB73B4970EF> /usr/lib/system/libremovefile.dylib
    0x7fff8be69000 -     0x7fff8c04efff  com.apple.CoreFoundation (6.9 - 855.17) <729BD6DA-1F63-3E72-A148-26F21EBF52BB> /System/Library/Frameworks/CoreFoundation.framework/Versions/A/CoreFoundation
    0x7fff8c04f000 -     0x7fff8c087ff7  com.apple.RemoteViewServices (2.0 - 94) <3F34D630-3DDB-3411-BC28-A56A9B55EBDA> /System/Library/PrivateFrameworks/RemoteViewServices.framework/Versions/A/RemoteViewServices
    0x7fff8c093000 -     0x7fff8c4c6ffb  com.apple.vision.FaceCore (3.0.0 - 3.0.0) <F42BFC9C-0B16-35EF-9A07-91B7FDAB7FC5> /System/Library/PrivateFrameworks/FaceCore.framework/Versions/A/FaceCore
    0x7fff8c4c7000 -     0x7fff8c4f0fff  GLRendererFloat (9.6.1) <23A2C705-F932-335D-B27B-565A30333460> /System/Library/Frameworks/OpenGL.framework/Versions/A/Resources/GLRendererFloat.bundle/GLRendererFloat
    0x7fff8c63b000 -     0x7fff8c640fff  libmacho.dylib (845) <1D2910DF-C036-3A82-A3FD-44FF73B5FF9B> /usr/lib/system/libmacho.dylib
    0x7fff8c641000 -     0x7fff8c642ff7  com.apple.print.framework.Print (9.0 - 260) <EE00FAE1-DA03-3EC2-8571-562518C46994> /System/Library/Frameworks/Carbon.framework/Versions/A/Frameworks/Print.framework/Versions/A/Print
    0x7fff8c6a5000 -     0x7fff8c6bdff7  com.apple.GenerationalStorage (2.0 - 160.3) <64749B08-0212-3AC8-9B49-73D662B09304> /System/Library/PrivateFrameworks/GenerationalStorage.framework/Versions/A/GenerationalStorage
    0x7fff8c6be000 -     0x7fff8c7a8fff  libsqlite3.dylib (158) <00269BF9-43BE-39E0-9C85-24585B9923C8> /usr/lib/libsqlite3.dylib
    0x7fff8c7a9000 -     0x7fff8c7aefff  com.apple.DiskArbitration (2.6 - 2.6) <A4165553-770E-3D27-B217-01FC1F852B87> /System/Library/Frameworks/DiskArbitration.framework/Versions/A/DiskArbitration
    0x7fff8c7af000 -     0x7fff8c879fff  com.apple.LaunchServices (572.28 - 572.28) <FDED4724-4CB6-3DE5-B785-AE6D4C261CF6> /System/Library/Frameworks/CoreServices.framework/Versions/A/Frameworks/LaunchServices.framework/Versions/A/LaunchServices
    0x7fff8c87a000 -     0x7fff8c9aaff7  com.apple.desktopservices (1.8.3 - 1.8.3) <225BEC20-F8E0-3F22-9560-890A1A5B9050> /System/Library/PrivateFrameworks/DesktopServicesPriv.framework/Versions/A/DesktopServicesPriv
    0x7fff8c9ab000 -     0x7fff8cb11fff  libGLProgrammability.dylib (9.6.1) <07700B99-8542-32D7-BB96-29472EFE75EF> /System/Library/Frameworks/OpenGL.framework/Versions/A/Libraries/libGLProgrammability.dylib
    0x7fff8cb12000 -     0x7fff8cb3bff7  libc++abi.dylib (49.1) <21A807D3-6732-3455-B77F-743E9F916DF0> /usr/lib/libc++abi.dylib
    0x7fff8cb3c000 -     0x7fff8cb3cfff  com.apple.Carbon (154 - 157) <EFC1A1C0-CB07-395A-B038-CFA2E71D3E69> /System/Library/Frameworks/Carbon.framework/Versions/A/Carbon
    0x7fff8ccac000 -     0x7fff8ccacfff  com.apple.Accelerate (1.9 - Accelerate 1.9) <509BB27A-AE62-366D-86D8-0B06D217CF56> /System/Library/Frameworks/Accelerate.framework/Versions/A/Accelerate
    0x7fff8ccad000 -     0x7fff8ccbfff7  com.apple.MultitouchSupport.framework (245.13 - 245.13) <E51DE5CA-9859-3C13-A24F-37EF4385C1D6> /System/Library/PrivateFrameworks/MultitouchSupport.framework/Versions/A/MultitouchSupport
    0x7fff8ccc0000 -     0x7fff8ccc0fff  com.apple.Accelerate.vecLib (3.9 - vecLib 3.9) <F8D0CC77-98AC-3B58-9FE6-0C25421827B6> /System/Library/Frameworks/Accelerate.framework/Versions/A/Frameworks/vecLib.framework/Versions/A/vecLib
    0x7fff8ccc1000 -     0x7fff8ccc8ffb  libcopyfile.dylib (103.92.1) <CF29DFF6-0589-3590-834C-82E2316612E8> /usr/lib/system/libcopyfile.dylib
    0x7fff8cd1f000 -     0x7fff8cd4bfff  com.apple.CoreServicesInternal (184.9 - 184.9) <4DEA54F9-81D6-3EDB-AA3C-1F9C497B3379> /System/Library/PrivateFrameworks/CoreServicesInternal.framework/Versions/A/CoreServicesInternal
    0x7fff8ce3a000 -     0x7fff8ce41fff  libcompiler_rt.dylib (35) <4CD916B2-1B17-362A-B403-EF24A1DAC141> /usr/lib/system/libcompiler_rt.dylib
    0x7fff8ce8e000 -     0x7fff8ce93ff7  libunwind.dylib (35.3) <78DCC358-2FC1-302E-B395-0155B47CB547> /usr/lib/system/libunwind.dylib
    0x7fff8ce94000 -     0x7fff8ce94fff  com.apple.ApplicationServices (48 - 48) <3E3F01A8-314D-378F-835E-9CC4F8820031> /System/Library/Frameworks/ApplicationServices.framework/Versions/A/ApplicationServices
    0x7fff8d1f6000 -     0x7fff8d249fff  com.apple.ScalableUserInterface (1.0 - 1) <CF745298-7373-38D2-B3B1-727D5A569E48> /System/Library/Frameworks/QuartzCore.framework/Versions/A/Frameworks/ScalableUserInterface.framework/Versions/A/ScalableUserInterface
    0x7fff8d24a000 -     0x7fff8d25cff7  com.apple.CoreBluetooth (1.0 - 1) <67A00F44-563E-3C55-9187-34D502D84DDE> /System/Library/Frameworks/IOBluetooth.framework/Versions/A/Frameworks/CoreBluetooth.framework/Versions/A/CoreBluetooth
    0x7fff8d25d000 -     0x7fff8d321ff7  com.apple.backup.framework (1.5.4 - 1.5.4) <195DA868-47A5-37E6-8CF0-9BCF11846899> /System/Library/PrivateFrameworks/Backup.framework/Versions/A/Backup
    0x7fff8d339000 -     0x7fff8d340ff7  libsystem_pthread.dylib (53.1.4) <AB498556-B555-310E-9041-F67EC9E00E2C> /usr/lib/system/libsystem_pthread.dylib
    0x7fff8d3b3000 -     0x7fff8d447ff7  com.apple.Bluetooth (4.2.6 - 4.2.6f1) <15E6C1AE-647C-3E43-8BDC-286BC02845E3> /System/Library/Frameworks/IOBluetooth.framework/Versions/A/IOBluetooth
    0x7fff8d492000 -     0x7fff8d5e6ff3  com.apple.audio.toolbox.AudioToolbox (1.10 - 1.10) <69B273E8-5A8E-3FC7-B807-C16B657662FE> /System/Library/Frameworks/AudioToolbox.framework/Versions/A/AudioToolbox
    0x7fff8dac0000 -     0x7fff8dac8ff7  com.apple.speech.recognition.framework (4.2.4 - 4.2.4) <98BBB3E4-6239-3EF1-90B2-84EA0D3B8D61> /System/Library/Frameworks/Carbon.framework/Versions/A/Frameworks/SpeechRecognition.framework/Versions/A/SpeechRecognition
    0x7fff8dae3000 -     0x7fff8db08ff7  com.apple.CoreVideo (1.8 - 117.2) <4674339E-26D0-35FA-9958-422832B39B12> /System/Library/Frameworks/CoreVideo.framework/Versions/A/CoreVideo
    0x7fff8db09000 -     0x7fff8db21ff7  com.apple.openscripting (1.4 - 157) <B3B037D7-1019-31E6-9D17-08E699AF3701> /System/Library/Frameworks/Carbon.framework/Versions/A/Frameworks/OpenScripting.framework/Versions/A/OpenScripting
    0x7fff8db23000 -     0x7fff8ddf7fc7  com.apple.vImage (7.0 - 7.0) <D241DBFA-AC49-31E2-893D-EAAC31890C90> /System/Library/Frameworks/Accelerate.framework/Versions/A/Frameworks/vImage.framework/Versions/A/vImage
    0x7fff8ddf8000 -     0x7fff8de1cff7  libJPEG.dylib (1043) <25723F3F-48A6-3AC5-A7A3-58E418FEBF3F> /System/Library/Frameworks/ImageIO.framework/Versions/A/Resources/libJPEG.dylib
    0x7fff8de1d000 -     0x7fff8de21ff7  libGIF.dylib (1043) <AF0FE71A-27AB-31E0-8CEA-BC0BF2091FA8> /System/Library/Frameworks/ImageIO.framework/Versions/A/Resources/libGIF.dylib
    0x7fff8de22000 -     0x7fff8de70fff  libcorecrypto.dylib (161.1) <F3973C28-14B6-3006-BB2B-00DD7F09ABC7> /usr/lib/system/libcorecrypto.dylib
    0x7fff8de71000 -     0x7fff8df60fff  libFontParser.dylib (111.1) <835A8253-6AB9-3AAB-9CBF-171440DEC486> /System/Library/Frameworks/ApplicationServices.framework/Versions/A/Frameworks/ATS.framework/Versions/A/Resources/libFontParser.dylib
    0x7fff8df61000 -     0x7fff8ead7ff7  com.apple.AppKit (6.9 - 1265.21) <9DC13B27-841D-3839-93B2-3EDE66157BDE> /System/Library/Frameworks/AppKit.framework/Versions/C/AppKit
    0x7fff8eaf8000 -     0x7fff8eb46ff9  libstdc++.6.dylib (60) <0241E6A4-1368-33BE-950B-D0A175C41F54> /usr/lib/libstdc++.6.dylib
    0x7fff8eb86000 -     0x7fff8eb90ff7  com.apple.bsd.ServiceManagement (2.0 - 2.0) <2D27B498-BB9C-3D88-B05A-76908A8A26F3> /System/Library/Frameworks/ServiceManagement.framework/Versions/A/ServiceManagement
    0x7fff8eb91000 -     0x7fff8ec12fff  com.apple.CoreSymbolication (3.0.1 - 141.0.5) <20E484C4-9F0E-3DF6-BB27-D509859FF57A> /System/Library/PrivateFrameworks/CoreSymbolication.framework/Versions/A/CoreSymbolication
    0x7fff8ec47000 -     0x7fff8ecacffb  com.apple.Heimdal (4.0 - 2.0) <F34D6627-9F80-3823-8B57-DB629307DF87> /System/Library/PrivateFrameworks/Heimdal.framework/Versions/A/Heimdal
    0x7fff8ecad000 -     0x7fff8ecdcfff  com.apple.DebugSymbols (106 - 106) <E1BDED08-523A-36F4-B2DA-9D5C712F0AC7> /System/Library/PrivateFrameworks/DebugSymbols.framework/Versions/A/DebugSymbols
    0x7fff8ed40000 -     0x7fff8ed47ff8  liblaunch.dylib (842.92.1) <A40A0C7B-3216-39B4-8AE0-B5D3BAF1DA8A> /usr/lib/system/liblaunch.dylib
    0x7fff8ed48000 -     0x7fff8ed53fff  libkxld.dylib (2422.110.17) <B6140BAB-0EAF-3E4F-B055-314068056BB4> /usr/lib/system/libkxld.dylib
    0x7fff8ed54000 -     0x7fff8f4a3fff  libclh.dylib (4.0.3 - 4.0.3) <19932A17-7823-37F3-B2D9-FD5D40E54637> /System/Library/Extensions/GeForceGLDriver.bundle/Contents/MacOS/libclh.dylib
    0x7fff8f9c8000 -     0x7fff8fa51ff7  libsystem_c.dylib (997.90.3) <6FD3A400-4BB2-3B95-B90C-BE6E9D0D78FA> /usr/lib/system/libsystem_c.dylib
    0x7fff8fa52000 -     0x7fff8fc0affb  libicucore.A.dylib (511.34) <616A65D6-3F20-3EAB-8CA8-273AD890261C> /usr/lib/libicucore.A.dylib
    0x7fff8fc4a000 -     0x7fff8fc5bff7  libz.1.dylib (53) <42E0C8C6-CA38-3CA4-8619-D24ED5DD492E> /usr/lib/libz.1.dylib
    0x7fff8fc65000 -     0x7fff8fc67ff7  com.apple.securityhi (9.0 - 55005) <18C42525-688C-3D47-B9C9-1E0F8F58FA64> /System/Library/Frameworks/Carbon.framework/Versions/A/Frameworks/SecurityHI.framework/Versions/A/SecurityHI
    0x7fff8fcc8000 -     0x7fff8fe64ff3  com.apple.QuartzCore (1.8 - 332.3) <72003E51-1287-395B-BCBC-331597D45C5E> /System/Library/Frameworks/QuartzCore.framework/Versions/A/QuartzCore
    0x7fff8fe65000 -     0x7fff8fe66fff  com.apple.TrustEvaluationAgent (2.0 - 25) <334A82F4-4AE4-3719-A511-86D0B0723E2B> /System/Library/PrivateFrameworks/TrustEvaluationAgent.framework/Versions/A/TrustEvaluationAgent
    0x7fff8fe67000 -     0x7fff8feb9fff  libc++.1.dylib (120) <4F68DFC5-2077-39A8-A449-CAC5FDEE7BDE> /usr/lib/libc++.1.dylib
    0x7fff8feba000 -     0x7fff8ff27fff  com.apple.SearchKit (1.4.0 - 1.4.0) <B9B8D510-A27E-36B0-93E9-17146D9E9045> /System/Library/Frameworks/CoreServices.framework/Versions/A/Frameworks/SearchKit.framework/Versions/A/SearchKit
    0x7fff90380000 -     0x7fff90399ff7  com.apple.Ubiquity (1.3 - 289) <C7F1B734-CE81-334D-BE41-8B20D95A1F9B> /System/Library/PrivateFrameworks/Ubiquity.framework/Versions/A/Ubiquity
    0x7fff90b17000 -     0x7fff90b58fff  com.apple.PerformanceAnalysis (1.47 - 47) <7B73DFF4-75DB-3403-80D2-0F3FE48764C3> /System/Library/PrivateFrameworks/PerformanceAnalysis.framework/Versions/A/PerformanceAnalysis
    0x7fff90b80000 -     0x7fff90b8dff4  com.apple.Librarian (1.2 - 1) <F1A2744D-8536-32C7-8218-9972C6300DAE> /System/Library/PrivateFrameworks/Librarian.framework/Versions/A/Librarian
    0x7fff90f9c000 -     0x7fff91025fff  com.apple.ColorSync (4.9.0 - 4.9.0) <B756B908-9AD1-3F5D-83F9-7A0B068387D2> /System/Library/Frameworks/ApplicationServices.framework/Versions/A/Frameworks/ColorSync.framework/Versions/A/ColorSync
    0x7fff91026000 -     0x7fff91027ff7  libSystem.B.dylib (1197.1.1) <E303F2F8-A8CF-3DF3-84B3-F2D0EE41CCF6> /usr/lib/libSystem.B.dylib
    0x7fff9102c000 -     0x7fff9107aff7  com.apple.opencl (2.3.59 - 2.3.59) <044485A4-A50C-34CE-A1F9-35A50CC68313> /System/Library/Frameworks/OpenCL.framework/Versions/A/OpenCL
    0x7fff9107b000 -     0x7fff9109ffff  libxpc.dylib (300.90.2) <AB40CD57-F454-3FD4-B415-63B3C0D5C624> /usr/lib/system/libxpc.dylib
    0x7fff911d0000 -     0x7fff912d6ff7  com.apple.ImageIO.framework (3.3.0 - 1043) <C4ADE5B1-A540-34E1-A043-118185489C9D> /System/Library/Frameworks/ImageIO.framework/Versions/A/ImageIO
    0x7fff912d7000 -     0x7fff912dfffc  libGFXShared.dylib (9.6.1) <25BBF325-AC57-3BAA-9427-2D14CC243AE6> /System/Library/Frameworks/OpenGL.framework/Versions/A/Libraries/libGFXShared.dylib
    0x7fff91453000 -     0x7fff9145dff7  com.apple.CrashReporterSupport (10.9 - 539) <B25A09EC-A021-32EC-86F8-05B4837E0EDE> /System/Library/PrivateFrameworks/CrashReporterSupport.framework/Versions/A/CrashReporterSupport
    0x7fff91468000 -     0x7fff91472fff  libcommonCrypto.dylib (60049) <8C4F0CA0-389C-3EDC-B155-E62DD2187E1D> /usr/lib/system/libcommonCrypto.dylib
    0x7fff91473000 -     0x7fff914a2ff9  com.apple.GSS (4.0 - 2.0) <44E914BE-B0D0-3E05-9451-CA9E539AFA52> /System/Library/Frameworks/GSS.framework/Versions/A/GSS
    0x7fff914e9000 -     0x7fff91505ff7  libsystem_kernel.dylib (2422.110.17) <873931CE-D1AF-3596-AADB-D2E63C9AB29F> /usr/lib/system/libsystem_kernel.dylib
    0x7fff9151e000 -     0x7fff9151ffff  liblangid.dylib (117) <9546E641-F730-3AB0-B3CD-E0E2FDD173D9> /usr/lib/liblangid.dylib
    0x7fff91547000 -     0x7fff91609ff5  com.apple.CoreText (367.20 - 367.20) <B80D086D-93A9-3C35-860E-9C3FDD027F3B> /System/Library/Frameworks/CoreText.framework/Versions/A/CoreText
    0x7fff9160d000 -     0x7fff916c5ff7  com.apple.DiscRecording (8.0 - 8000.4.6) <CDAAAD04-A1D0-3C67-ABCC-EFC9E8D44E7E> /System/Library/Frameworks/DiscRecording.framework/Versions/A/DiscRecording
    0x7fff91731000 -     0x7fff91734fff  libCoreVMClient.dylib (58.1) <EBC36C69-C896-3C3D-8589-3E9023E7E56F> /System/Library/Frameworks/OpenGL.framework/Versions/A/Libraries/libCoreVMClient.dylib
    0x7fff91735000 -     0x7fff9177cff7  libcups.2.dylib (372.4) <36EA4350-43B4-3A5C-9904-10685BFDA7D4> /usr/lib/libcups.2.dylib
    0x7fff91788000 -     0x7fff917ebffb  com.apple.SystemConfiguration (1.13.1 - 1.13.1) <2C8E1A73-5AD6-3A7D-8ED8-D6755555A993> /System/Library/Frameworks/SystemConfiguration.framework/Versions/A/SystemConfiguration
    0x7fff917ee000 -     0x7fff91847fff  libTIFF.dylib (1043) <D7CAE68F-6087-3B40-9CB8-EC6DB47BF877> /System/Library/Frameworks/ImageIO.framework/Versions/A/Resources/libTIFF.dylib
    0x7fff91848000 -     0x7fff9184aff3  libsystem_configuration.dylib (596.15) <4998CB6A-9D54-390A-9F57-5D1AC53C135C> /usr/lib/system/libsystem_configuration.dylib
    0x7fff9191c000 -     0x7fff9191dff7  libsystem_blocks.dylib (63) <FB856CD1-2AEA-3907-8E9B-1E54B6827F82> /usr/lib/system/libsystem_blocks.dylib
    0x7fff9191e000 -     0x7fff91924ff7  libsystem_platform.dylib (24.90.1) <3C3D3DA8-32B9-3243-98EC-D89B9A1670B3> /usr/lib/system/libsystem_platform.dylib
    0x7fff91925000 -     0x7fff91933fff  com.apple.opengl (9.6.1 - 9.6.1) <B22FA400-5824-36AF-9945-5FEC31995A0E> /System/Library/Frameworks/OpenGL.framework/Versions/A/OpenGL
    0x7fff91934000 -     0x7fff91936fff  libRadiance.dylib (1043) <9813995C-DEAA-3992-8DF8-320E4E4E288B> /System/Library/Frameworks/ImageIO.framework/Versions/A/Resources/libRadiance.dylib
    0x7fff91937000 -     0x7fff91947ffb  libsasl2.2.dylib (170) <C8E25710-68B6-368A-BF3E-48EC7273177B> /usr/lib/libsasl2.2.dylib
    0x7fff91b3f000 -     0x7fff91b42ff7  libdyld.dylib (239.4) <7C9EC3B7-DDE3-33FF-953F-4067C743951D> /usr/lib/system/libdyld.dylib
    0x7fff91b43000 -     0x7fff91c0efff  libvDSP.dylib (423.32) <3BF732BE-DDE0-38EB-8C54-E4E3C64F77A7> /System/Library/Frameworks/Accelerate.framework/Versions/A/Frameworks/vecLib.framework/Versions/A/libvDSP.dylib
    0x7fff91c51000 -     0x7fff91c55fff  com.apple.IOAccelerator (98.22 - 98.22) <AB1F2662-330B-3D88-8E30-A8343203CD38> /System/Library/PrivateFrameworks/IOAccelerator.framework/Versions/A/IOAccelerator
    0x7fff91d98000 -     0x7fff91d9afff  libCVMSPluginSupport.dylib (9.6.1) <FB37F4C4-1E84-3349-BB03-92CA0A5F6837> /System/Library/Frameworks/OpenGL.framework/Versions/A/Libraries/libCVMSPluginSupport.dylib
    0x7fff91df9000 -     0x7fff91e29fff  com.apple.IconServices (25 - 25.17) <4751127E-FBD5-3ED5-8510-08D4E4166EFE> /System/Library/PrivateFrameworks/IconServices.framework/Versions/A/IconServices
    0x7fff91e39000 -     0x7fff91e53fff  libdispatch.dylib (339.92.1) <C4E4A18D-3C3B-3C9C-8709-A4270D998DE7> /usr/lib/system/libdispatch.dylib
    0x7fff91e54000 -     0x7fff91e60ffb  com.apple.AppleFSCompression (56.92.1 - 1.0) <066255FD-DBD1-3041-8DDA-7AFC41C9096D> /System/Library/PrivateFrameworks/AppleFSCompression.framework/Versions/A/AppleFSCompression
    0x7fff91e61000 -     0x7fff91e6aff3  libsystem_notify.dylib (121) <52571EC3-6894-37E4-946E-064B021ED44E> /usr/lib/system/libsystem_notify.dylib
    0x7fff91e84000 -     0x7fff91edfffb  com.apple.AE (665.5 - 665.5) <BBA230F9-144C-3CAB-A77A-0621719244CD> /System/Library/Frameworks/CoreServices.framework/Versions/A/Frameworks/AE.framework/Versions/A/AE
    0x7fff91ee0000 -     0x7fff91ee1fff  libunc.dylib (28) <62682455-1862-36FE-8A04-7A6B91256438> /usr/lib/system/libunc.dylib
    0x7fff91f3a000 -     0x7fff91f3efff  libpam.2.dylib (20) <B93CE8F5-DAA8-30A1-B1F6-F890509513CB> /usr/lib/libpam.2.dylib
    0x7fff91f3f000 -     0x7fff9223dfff  com.apple.Foundation (6.9 - 1056.13) <2EE9AB07-3EA0-37D3-B407-4A520F2CB497> /System/Library/Frameworks/Foundation.framework/Versions/C/Foundation
    0x7fff922d1000 -     0x7fff922defff  com.apple.Sharing (132.2 - 132.2) <F983394A-226D-3244-B511-FA51FDB6ADDA> /System/Library/PrivateFrameworks/Sharing.framework/Versions/A/Sharing
    0x7fff93133000 -     0x7fff93135fff  com.apple.EFILogin (2.0 - 2) <C360E8AF-E9BB-3BBA-9DF0-57A92CEF00D4> /System/Library/PrivateFrameworks/EFILogin.framework/Versions/A/EFILogin
    0x7fff932c8000 -     0x7fff932d9ff7  libsystem_asl.dylib (217.1.4) <655FB343-52CF-3E2F-B14D-BEBF5AAEF94D> /usr/lib/system/libsystem_asl.dylib
    0x7fff9334a000 -     0x7fff935a4ff9  com.apple.security (7.0 - 55471.14.8) <EA03E140-2509-3A07-8440-2DC97C0D478B> /System/Library/Frameworks/Security.framework/Versions/A/Security
    0x7fff935a5000 -     0x7fff93839ff7  com.apple.RawCamera.bundle (5.06 - 751) <A8B1EEDB-FDCB-3EDC-9728-E3FAA644A499> /System/Library/CoreServices/RawCamera.bundle/Contents/MacOS/RawCamera
    0x7fff9383a000 -     0x7fff9383afff  com.apple.Cocoa (6.8 - 20) <E90E99D7-A425-3301-A025-D9E0CD11918E> /System/Library/Frameworks/Cocoa.framework/Versions/A/Cocoa
    0x7fff93a5c000 -     0x7fff93b4afff  libJP2.dylib (1043) <C4031D64-6C57-3FB4-9D87-874D387381DB> /System/Library/Frameworks/ImageIO.framework/Versions/A/Resources/libJP2.dylib
    0x7fff93b75000 -     0x7fff93b81ff7  com.apple.OpenDirectory (10.9 - 173.90.1) <256C265B-7FA6-326D-9F60-18DADF5F3A0E> /System/Library/Frameworks/OpenDirectory.framework/Versions/A/OpenDirectory
    0x7fff93b82000 -     0x7fff93c73ff9  libiconv.2.dylib (41) <BB44B115-AC32-3877-A0ED-AEC6232A4563> /usr/lib/libiconv.2.dylib
    0x7fff93c74000 -     0x7fff93cebfff  com.apple.CoreServices.OSServices (600.4 - 600.4) <C63562F5-6DF5-3EE9-8897-FF61A44C8251> /System/Library/Frameworks/CoreServices.framework/Versions/A/Frameworks/OSServices.framework/Versions/A/OSServices
    0x7fff93d6d000 -     0x7fff93da8fff  com.apple.bom (14.0 - 193.1) <EF24A562-6D3C-379E-8B9B-FAE0E4A0EF7C> /System/Library/PrivateFrameworks/Bom.framework/Versions/A/Bom
    0x7fff93da9000 -     0x7fff93db3ff7  libcsfde.dylib (380) <A5CF6F85-0537-399F-968B-1536B1235E65> /usr/lib/libcsfde.dylib
    0x7fff93db4000 -     0x7fff93e85ff1  com.apple.DiskImagesFramework (10.9 - 371.1) <D85430A6-1410-3B5F-9D11-17E2440B786E> /System/Library/PrivateFrameworks/DiskImages.framework/Versions/A/DiskImages
    0x7fff93f50000 -     0x7fff93fdbfff  libCoreStorage.dylib (380) <DE9B3F8C-045C-3010-9A25-C8CD72F1066B> /usr/lib/libCoreStorage.dylib
    0x7fff93ff6000 -     0x7fff943d7ffe  libLAPACK.dylib (1094.5) <7E7A9B8D-1638-3914-BAE0-663B69865986> /System/Library/Frameworks/Accelerate.framework/Versions/A/Frameworks/vecLib.framework/Versions/A/libLAPACK.dylib
    0x7fff94c9c000 -     0x7fff94cb8fff  libresolv.9.dylib (54) <11C2C826-F1C6-39C6-B4E8-6E0C41D4FA95> /usr/lib/libresolv.9.dylib
    0x7fff94cb9000 -     0x7fff94ce2fff  com.apple.DictionaryServices (1.2 - 208) <A539A058-BA57-35EE-AA08-D0B0E835127D> /System/Library/Frameworks/CoreServices.framework/Versions/A/Frameworks/DictionaryServices.framework/Versions/A/DictionaryServices
    0x7fff94db5000 -     0x7fff94dc7fff  com.apple.ImageCapture (9.0 - 9.0) <BE0B65DA-3031-359B-8BBA-B9803D4ADBF4> /System/Library/Frameworks/Carbon.framework/Versions/A/Frameworks/ImageCapture.framework/Versions/A/ImageCapture
    0x7fff94dc8000 -     0x7fff95010ff7  com.apple.CoreData (107 - 481.3) <E78734AA-E3D0-33CB-A014-620BBCAB2E96> /System/Library/Frameworks/CoreData.framework/Versions/A/CoreData
    0x7fff95011000 -     0x7fff95181ff4  com.apple.CFNetwork (673.4 - 673.4) <F3BF6020-99BE-3844-A7B8-352B93AD02F3> /System/Library/Frameworks/CFNetwork.framework/Versions/A/CFNetwork
    0x7fff95182000 -     0x7fff951bbff7  com.apple.QD (3.50 - 298) <C1F20764-DEF0-34CF-B3AB-AB5480D64E66> /System/Library/Frameworks/ApplicationServices.framework/Versions/A/Frameworks/QD.framework/Versions/A/QD
    0x7fff951d8000 -     0x7fff951dcff7  libheimdal-asn1.dylib (323.92.1) <CAE21FFF-5763-399C-B7C5-EEBFFEEF2242> /usr/lib/libheimdal-asn1.dylib
    0x7fff95204000 -     0x7fff95208ff7  com.apple.ServerInformation (2.1.1 - 1) <7FAF2B82-FE90-3398-98D8-0F84C6FE6A4A> /System/Library/PrivateFrameworks/ServerInformation.framework/Versions/A/ServerInformation
    0x7fff95270000 -     0x7fff95273fff  com.apple.help (1.3.3 - 46) <AE763646-D07A-3F9A-ACD4-F5CBD734EE36> /System/Library/Frameworks/Carbon.framework/Versions/A/Frameworks/Help.framework/Versions/A/Help
    0x7fff9529f000 -     0x7fff9530eff1  com.apple.ApplicationServices.ATS (360 - 363.3) <546E89D9-2AE7-3111-B2B8-2366650D22F0> /System/Library/Frameworks/ApplicationServices.framework/Versions/A/Frameworks/ATS.framework/Versions/A/ATS
    0x7fff953ab000 -     0x7fff953dafd2  libsystem_m.dylib (3047.16) <B7F0E2E4-2777-33FC-A787-D6430B630D54> /usr/lib/system/libsystem_m.dylib
    0x7fff953db000 -     0x7fff953dbffd  libOpenScriptingUtil.dylib (157) <19F0E769-0989-3062-9AFB-8976E90E9759> /usr/lib/libOpenScriptingUtil.dylib
    0x7fff953dc000 -     0x7fff953e5ffd  com.apple.CommonAuth (4.0 - 2.0) <32BA436F-6319-3A0B-B5D2-2EB75FF36B5B> /System/Library/PrivateFrameworks/CommonAuth.framework/Versions/A/CommonAuth
    0x7fff956c9000 -     0x7fff95708fff  libGLU.dylib (9.6.1) <AE032555-3E2F-3DBF-A26D-EA4576061605> /System/Library/Frameworks/OpenGL.framework/Versions/A/Libraries/libGLU.dylib
    0x7fff957af000 -     0x7fff95822fff  com.apple.securityfoundation (6.0 - 55122.3) <8575DF7A-EC79-3FCE-A737-7512363A5B12> /System/Library/Frameworks/SecurityFoundation.framework/Versions/A/SecurityFoundation
    0x7fff95823000 -     0x7fff959d0f27  libobjc.A.dylib (551.1) <AD7FD984-271E-30F4-A361-6B20319EC73B> /usr/lib/libobjc.A.dylib
    0x7fff959d1000 -     0x7fff959f6ff7  com.apple.ChunkingLibrary (2.0 - 155.1) <B845DC7A-D1EA-31E2-967C-D1FE0C628036> /System/Library/PrivateFrameworks/ChunkingLibrary.framework/Versions/A/ChunkingLibrary
    0x7fff959f7000 -     0x7fff959f9ff7  libquarantine.dylib (71) <7A1A2BCB-C03D-3A25-BFA4-3E569B2D2C38> /usr/lib/system/libquarantine.dylib
    0x7fff960af000 -     0x7fff9613fff7  com.apple.Metadata (10.7.0 - 800.28) <E85AEB1B-CB17-38BC-B5C6-AAB50B47AF05> /System/Library/Frameworks/CoreServices.framework/Versions/A/Frameworks/Metadata.framework/Versions/A/Metadata
    0x7fff96140000 -     0x7fff961ccff7  com.apple.ink.framework (10.9 - 207) <8A50B893-AD03-3826-8555-A54FEAF08F47> /System/Library/Frameworks/Carbon.framework/Versions/A/Frameworks/Ink.framework/Versions/A/Ink
    0x7fff961cd000 -     0x7fff962b1fff  com.apple.coreui (2.1 - 231) <432DB40C-6B7E-39C8-9FB5-B95917930056> /System/Library/PrivateFrameworks/CoreUI.framework/Versions/A/CoreUI
    0x7fff962b7000 -     0x7fff962c7fff  libbsm.0.dylib (33) <2CAC00A2-1352-302A-88FA-C567D4D69179> /usr/lib/libbsm.0.dylib

External Modification Summary:
  Calls made by other processes targeting this process:
    task_for_pid: 9
    thread_create: 0
    thread_set_state: 0
  Calls made by this process:
    task_for_pid: 0
    thread_create: 0
    thread_set_state: 0
  Calls made by all processes on this machine:
    task_for_pid: 1166
    thread_create: 0
    thread_set_state: 0

VM Region Summary:
ReadOnly portion of Libraries: Total=194.4M resident=97.3M(50%) swapped_out_or_unallocated=97.0M(50%)
Writable regions: Total=812.8M written=205.4M(25%) resident=353.3M(43%) swapped_out=0K(0%) unallocated=459.5M(57%)
 
REGION TYPE                      VIRTUAL
===========                      =======
CG shared images                    140K
Dispatch continuations             80.0M
IOKit                              14.8M
IOKit (reserved)                      4K        reserved VM address space (unallocated)
Kernel Alloc Once                     8K
MALLOC                            481.3M
MALLOC (admin)                       32K
MALLOC_LARGE (reserved)            61.2M        reserved VM address space (unallocated)
Memory Tag 242                       12K
STACK GUARD                        56.1M
Stack                              17.2M
VM_ALLOCATE                        20.6M
VM_ALLOCATE (reserved)              148K        reserved VM address space (unallocated)
__DATA                            185.9M
__IMAGE                             528K
__LINKEDIT                         69.4M
__TEXT                            125.0M
__UNICODE                           544K
mapped file                        25.3M
shared memory                        68K
===========                      =======
TOTAL                               1.1G
TOTAL, minus reserved VM space      1.1G
 


System Profile:
Model: MacBookPro10,1, BootROM MBP101.00EE.B02, 4 processors, Intel Core i7, 2.6 GHz, 16 GB, SMC 2.3f36
Graphics: Intel HD Graphics 4000, Intel HD Graphics 4000, Built-In
Graphics: NVIDIA GeForce GT 650M, NVIDIA GeForce GT 650M, PCIe, 1024 MB
Memory Module: BANK 0/DIMM0, 8 GB, DDR3, 1600 MHz, 0x80AD, 0x484D5434314753364D465238432D50422020
Memory Module: BANK 1/DIMM0, 8 GB, DDR3, 1600 MHz, 0x80AD, 0x484D5434314753364D465238432D50422020
AirPort: spairport_wireless_card_type_airport_extreme (0x14E4, 0xEF), Broadcom BCM43xx 1.0 (5.106.98.100.22)
Bluetooth: Version 4.2.6f1 14216, 3 services, 23 devices, 1 incoming serial ports
Network Service: Wi-Fi, AirPort, en0
Serial ATA Device: APPLE SSD SM256E, 251 GB
USB Device: Hub
USB Device: FaceTime HD Camera (Built-in)
USB Device: Hub
USB Device: Hub
USB Device: Apple Internal Keyboard / Trackpad
USB Device: BRCM20702 Hub
USB Device: Bluetooth USB Host Controller
USB Device: Logitech Dual Action
Thunderbolt Bus: MacBook Pro, Apple Inc., 23.4
 