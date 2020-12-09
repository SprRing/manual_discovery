# manual_discovery

##### https://blogs.uni-paderborn.de/sse/tools/flowdroid/
Here is what we can see using the very basic settings.
And there are 11 memory leaks.
Input cmd lines:
```
java -jar /Users/yenshou/Downloads/taobao_FlowDroid/soot-infoflow-cmd-jar-with-dependencies.jar \
-a /Users/yenshou/Downloads/taobao_FlowDroid/taobao.apk \
-p /Users/yenshou/Library/Android/sdk/platforms/android-28/android.jar \
-s /Users/yenshou/Downloads/taobao_FlowDroid/SourcesAndSinks.txt
```
```
[main] INFO soot.jimple.infoflow.memory.MemoryWarningSystem - Shutting down the memory warning system...
[main] INFO soot.jimple.infoflow.android.SetupApplication$InPlaceInfoflow - Memory consumption after path building: 280 MB
[main] INFO soot.jimple.infoflow.android.SetupApplication$InPlaceInfoflow - Path reconstruction took 2 seconds
[main] INFO soot.jimple.infoflow.android.SetupApplication$InPlaceInfoflow - The sink virtualinvoke $r4.<java.io.FileOutputStream: void write(byte[])>($r6) in method <com.uc.crashsdk.a.b: boolean a(java.lang.String,java.lang.String)> was called with values from the following sources:
[main] INFO soot.jimple.infoflow.android.SetupApplication$InPlaceInfoflow - - $r16 = virtualinvoke $r13.<java.net.HttpURLConnection: java.io.InputStream getInputStream()>() in method <com.uc.crashsdk.a.c: byte[] a(java.lang.String,byte[])>
[main] INFO soot.jimple.infoflow.android.SetupApplication$InPlaceInfoflow - The sink $r0 = virtualinvoke $r0.<java.lang.String: java.lang.String replace(java.lang.CharSequence,java.lang.CharSequence)>(“&#95;“, “_”) in method <com.alibaba.motu.crashreporter.b: java.lang.String b(java.lang.String)> was called with values from the following sources:
[main] INFO soot.jimple.infoflow.android.SetupApplication$InPlaceInfoflow - - $r2 = virtualinvoke $r4.<android.telephony.TelephonyManager: java.lang.String getSubscriberId()>() in method <tb.ajv: java.lang.String e(android.content.Context)>
[main] INFO soot.jimple.infoflow.android.SetupApplication$InPlaceInfoflow - The sink virtualinvoke $r2.<java.io.OutputStream: void write(byte[],int,int)>($r3, 0, $i0) in method <tb.jxx: void a(java.io.InputStream,java.io.File)> was called with values from the following sources:
[main] INFO soot.jimple.infoflow.android.SetupApplication$InPlaceInfoflow - - $r6 = virtualinvoke $r5.<java.net.HttpURLConnection: java.io.InputStream getInputStream()>() in method <tb.jxx: tb.jxw$b b(java.lang.String,java.io.File)>
[main] INFO soot.jimple.infoflow.android.SetupApplication$InPlaceInfoflow - The sink $r0 = virtualinvoke $r0.<java.lang.String: java.lang.String replace(java.lang.CharSequence,java.lang.CharSequence)>(“_”, “&#95;“) in method <com.alibaba.motu.crashreporter.b: java.lang.String a(java.lang.String)> was called with values from the following sources:
[main] INFO soot.jimple.infoflow.android.SetupApplication$InPlaceInfoflow - - $r2 = virtualinvoke $r4.<android.telephony.TelephonyManager: java.lang.String getSubscriberId()>() in method <tb.ajv: java.lang.String e(android.content.Context)>
[main] INFO soot.jimple.infoflow.android.SetupApplication$InPlaceInfoflow - The sink virtualinvoke $r3.<java.io.ByteArrayOutputStream: void write(byte[],int,int)>($r5, 0, 4) in method <com.ta.utdid2.device.UTUtdid: byte[] generateUtdid()> was called with values from the following sources:
[main] INFO soot.jimple.infoflow.android.SetupApplication$InPlaceInfoflow - - $r5 = virtualinvoke $r4.<android.telephony.TelephonyManager: java.lang.String getDeviceId()>() in method <com.ta.utdid2.android.utils.PhoneInfoUtils: java.lang.String getImei(android.content.Context)>
[main] INFO soot.jimple.infoflow.android.SetupApplication$InPlaceInfoflow - The sink virtualinvoke $r3.<java.io.ByteArrayOutputStream: void write(byte[])>($r5) in method <com.ta.utdid2.device.UTUtdid: byte[] generateUtdid()> was called with values from the following sources:
[main] INFO soot.jimple.infoflow.android.SetupApplication$InPlaceInfoflow - - $r5 = virtualinvoke $r4.<android.telephony.TelephonyManager: java.lang.String getDeviceId()>() in method <com.ta.utdid2.android.utils.PhoneInfoUtils: java.lang.String getImei(android.content.Context)>
[main] INFO soot.jimple.infoflow.android.SetupApplication$InPlaceInfoflow - The sink virtualinvoke $r18.<java.io.ByteArrayOutputStream: void write(byte[],int,int)>($r5, 0, $i0) in method <com.uc.crashsdk.a.c: boolean a(byte[],java.lang.String,java.lang.String)> was called with values from the following sources:
[main] INFO soot.jimple.infoflow.android.SetupApplication$InPlaceInfoflow - - $r17 = virtualinvoke $r13.<java.net.HttpURLConnection: java.io.InputStream getInputStream()>() in method <com.uc.crashsdk.a.c: boolean a(byte[],java.lang.String,java.lang.String)>
[main] INFO soot.jimple.infoflow.android.SetupApplication$InPlaceInfoflow - The sink virtualinvoke $r14.<java.io.OutputStream: void write(byte[])>($r10) in method <com.uc.crashsdk.a.c: byte[] a(java.lang.String,byte[])> was called with values from the following sources:
[main] INFO soot.jimple.infoflow.android.SetupApplication$InPlaceInfoflow - - $r16 = virtualinvoke $r13.<java.net.HttpURLConnection: java.io.InputStream getInputStream()>() in method <com.uc.crashsdk.a.c: byte[] a(java.lang.String,byte[])>
[main] INFO soot.jimple.infoflow.android.SetupApplication$InPlaceInfoflow - The sink staticinvoke <android.util.Log: int e(java.lang.String,java.lang.String)>($r0, $r1) in method <com.taobao.flowcustoms.afc.utils.b: void a(java.lang.String,java.lang.String)> was called with values from the following sources:
[main] INFO soot.jimple.infoflow.android.SetupApplication$InPlaceInfoflow - - $r6 = interfaceinvoke $r4.<android.database.Cursor: java.lang.String getString(int)>(0) in method <com.taobao.linkmanager.afc.utils.TFCCommonUtils: java.lang.String c(android.content.Context)>
[main] INFO soot.jimple.infoflow.android.SetupApplication$InPlaceInfoflow - - $r0 = virtualinvoke $r3.<android.telephony.TelephonyManager: java.lang.String getDeviceId()>() in method <com.taobao.flowcustoms.afc.utils.AfcUtils: java.lang.String a(android.content.Context,boolean)>
[main] INFO soot.jimple.infoflow.android.SetupApplication$InPlaceInfoflow - The sink $r0 = virtualinvoke $r0.<java.lang.String: java.lang.String replace(java.lang.CharSequence,java.lang.CharSequence)>(“.log”, “”) in method <com.alibaba.motu.crashreporter.b: java.lang.String[] c(java.lang.String)> was called with values from the following sources:
[main] INFO soot.jimple.infoflow.android.SetupApplication$InPlaceInfoflow - - $r2 = virtualinvoke $r4.<android.telephony.TelephonyManager: java.lang.String getSubscriberId()>() in method <tb.ajv: java.lang.String e(android.content.Context)>
[main] INFO soot.jimple.infoflow.android.SetupApplication$InPlaceInfoflow - The sink virtualinvoke $r18.<java.io.ByteArrayOutputStream: void write(byte[],int,int)>($r10, 0, $i0) in method <com.uc.crashsdk.a.c: byte[] a(java.lang.String,byte[])> was called with values from the following sources:
[main] INFO soot.jimple.infoflow.android.SetupApplication$InPlaceInfoflow - - $r16 = virtualinvoke $r13.<java.net.HttpURLConnection: java.io.InputStream getInputStream()>() in method <com.uc.crashsdk.a.c: byte[] a(java.lang.String,byte[])>
[main] INFO soot.jimple.infoflow.android.SetupApplication$InPlaceInfoflow - Data flow solver took 17 seconds. Maximum memory consumption: 467 MB
[main] INFO soot.jimple.infoflow.android.SetupApplication - Found 11 leaks
```

For "AndroidCallbacks.txt"
```
java -jar /Users/yenshou/Downloads/taobao_FlowDroid/soot-infoflow-cmd-jar-with-dependencies.jar \
-a /Users/yenshou/Downloads/taobao_FlowDroid/taobao.apk \
-p /Users/yenshou/Library/Android/sdk/platforms/android-28/android.jar \
-s /Users/yenshou/Downloads/taobao_FlowDroid/AndroidCallbacks.txt
```
```
[main] INFO soot.jimple.infoflow.cmd.MainClass - Analyzing app /Users/yenshou/Downloads/taobao_FlowDroid/taobao.apk (1 of 1)...
[main] INFO soot.jimple.infoflow.android.SetupApplication - Initializing Soot...
[main] INFO soot.jimple.infoflow.android.SetupApplication - Loading dex files...
[main] WARN soot.dexpler.DexFileProvider - Multiple dex files detected, only processing 'classes.dex'. Use '-process-multiple-dex' option to process them all.
[main] INFO soot.jimple.infoflow.android.SetupApplication - ARSC file parsing took 0.076652005 seconds
[main] INFO soot.jimple.infoflow.memory.MemoryWarningSystem - Registered a memory warning system for 3,686.4 MiB
[main] INFO soot.jimple.infoflow.android.entryPointCreators.AndroidEntryPointCreator - Creating Android entry point for 834 components...
[main] INFO soot.jimple.infoflow.android.SetupApplication - Constructing the callgraph...
[main] INFO soot.jimple.infoflow.android.callbacks.DefaultCallbackAnalyzer - Collecting callbacks in DEFAULT mode...
[main] INFO soot.jimple.infoflow.android.callbacks.DefaultCallbackAnalyzer - Callback analysis done.
[main] WARN soot.jimple.infoflow.android.resources.LayoutFileParser - Fragment without class name or id detected
[main] WARN soot.jimple.infoflow.android.resources.LayoutFileParser - Fragment without class name or id detected
[main] INFO soot.jimple.infoflow.android.entryPointCreators.AndroidEntryPointCreator - Creating Android entry point for 834 components...
[main] INFO soot.jimple.infoflow.android.SetupApplication - Constructing the callgraph...
[main] INFO soot.jimple.infoflow.android.callbacks.DefaultCallbackAnalyzer - Running incremental callback analysis for 13 components...
[main] INFO soot.jimple.infoflow.android.callbacks.DefaultCallbackAnalyzer - Incremental callback analysis done.
[main] INFO soot.jimple.infoflow.android.entryPointCreators.AndroidEntryPointCreator - Creating Android entry point for 835 components...
[main] WARN soot.jimple.infoflow.android.entryPointCreators.AndroidEntryPointCreator - Cannot create valid constructor for com.taobao.android.compat.ApplicationCompat$ActivityLifecycleCallbacksCompat, because it is an interface and cannot substitute with subclass
[main] INFO soot.jimple.infoflow.android.SetupApplication - Constructing the callgraph...
[main] INFO soot.jimple.infoflow.android.callbacks.DefaultCallbackAnalyzer - Running incremental callback analysis for 1 components...
[main] INFO soot.jimple.infoflow.android.callbacks.DefaultCallbackAnalyzer - Incremental callback analysis done.
[main] INFO soot.jimple.infoflow.android.entryPointCreators.AndroidEntryPointCreator - Creating Android entry point for 835 components...
[main] INFO soot.jimple.infoflow.android.SetupApplication - Constructing the callgraph...
[main] INFO soot.jimple.infoflow.android.callbacks.DefaultCallbackAnalyzer - Running incremental callback analysis for 0 components...
[main] INFO soot.jimple.infoflow.android.callbacks.DefaultCallbackAnalyzer - Incremental callback analysis done.
[main] INFO soot.jimple.infoflow.memory.MemoryWarningSystem - Shutting down the memory warning system...
[main] INFO soot.jimple.infoflow.android.SetupApplication - Callback analysis terminated normally
[main] INFO soot.jimple.infoflow.android.SetupApplication - Entry point calculation done.
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.accounts.OnAccountsUpdateListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.animation.Animator$AnimatorListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.animation.LayoutTransition$TransitionListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.animation.TimeAnimator$TimeListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.animation.ValueAnimator$AnimatorUpdateListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.app.ActionBar$OnMenuVisibilityListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.app.ActionBar$OnNavigationListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.app.ActionBar$TabListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.app.Application$ActivityLifecycleCallbacks
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.app.DatePickerDialog$OnDateSetListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.app.FragmentBreadCrumbs$OnBreadCrumbClickListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.app.FragmentManager$OnBackStackChangedListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.app.KeyguardManager$OnKeyguardExitResult
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.app.LoaderManager$LoaderCallbacks
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.app.PendingIntent$OnFinished
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.app.SearchManager$OnCancelListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.app.SearchManager$OnDismissListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.app.TimePickerDialog$OnTimeSetListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.bluetooth.BluetoothProfile$ServiceListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.content.ClipboardManager$OnPrimaryClipChangedListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.content.ComponentCallbacks
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.content.ComponentCallbacks2
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.content.DialogInterface$OnCancelListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.content.DialogInterface$OnClickListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.content.DialogInterface$OnDismissListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.content.DialogInterface$OnKeyListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.content.DialogInterface$OnMultiChoiceClickListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.content.DialogInterface$OnShowListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.content.IntentSender$OnFinished
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.content.Loader$OnLoadCanceledListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.content.Loader$OnLoadCompleteListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.content.SharedPreferences$OnSharedPreferenceChangeListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.content.SyncStatusObserver
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.database.sqlite.SQLiteTransactionListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.drm.DrmManagerClient$OnErrorListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.drm.DrmManagerClient$OnEventListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.drm.DrmManagerClient$OnInfoListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.gesture.GestureOverlayView$OnGestureListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.gesture.GestureOverlayView$OnGesturePerformedListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.gesture.GestureOverlayView$OnGesturingListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.graphics.SurfaceTexture$OnFrameAvailableListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.hardware.Camera$AutoFocusCallback
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.hardware.Camera$AutoFocusMoveCallback
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.hardware.Camera$ErrorCallback
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.hardware.Camera$FaceDetectionListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.hardware.Camera$OnZoomChangeListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.hardware.Camera$PictureCallback
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.hardware.Camera$PreviewCallback
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.hardware.Camera$ShutterCallback
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.hardware.SensorEventListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.hardware.display.DisplayManager$DisplayListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.hardware.input.InputManager$InputDeviceListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.inputmethodservice.KeyboardView$OnKeyboardActionListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.location.GpsStatus$Listener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.location.GpsStatus$NmeaListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.location.LocationListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.media.AudioManager$OnAudioFocusChangeListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.media.AudioRecord$OnRecordPositionUpdateListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.media.JetPlayer$OnJetEventListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.media.MediaPlayer$OnBufferingUpdateListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.media.MediaPlayer$OnCompletionListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.media.MediaPlayer$OnErrorListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.media.MediaPlayer$OnInfoListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.media.MediaPlayer$OnPreparedListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.media.MediaPlayer$OnSeekCompleteListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.media.MediaPlayer$OnTimedTextListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.media.MediaPlayer$OnVideoSizeChangedListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.media.MediaRecorder$OnErrorListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.media.MediaRecorder$OnInfoListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.media.MediaScannerConnection$MediaScannerConnectionClient
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.media.MediaScannerConnection$OnScanCompletedListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.media.SoundPool$OnLoadCompleteListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.media.audiofx.AudioEffect$OnControlStatusChangeListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.media.audiofx.AudioEffect$OnEnableStatusChangeListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.media.audiofx.BassBoost$OnParameterChangeListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.media.audiofx.EnvironmentalReverb$OnParameterChangeListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.media.audiofx.Equalizer$OnParameterChangeListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.media.audiofx.PresetReverb$OnParameterChangeListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.media.audiofx.Virtualizer$OnParameterChangeListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.media.audiofx.Visualizer$OnDataCaptureListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.media.effect$EffectUpdateListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.net.nsd.NsdManager$DiscoveryListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.net.nsd.NsdManager$RegistrationListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.net.nsd.NsdManager$ResolveListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.net.sip.SipRegistrationListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.net.wifi.p2p.WifiP2pManager$ActionListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.net.wifi.p2p.WifiP2pManager$ChannelListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.net.wifi.p2p.WifiP2pManager$ConnectionInfoListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.net.wifi.p2p.WifiP2pManager$DnsSdServiceResponseListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.net.wifi.p2p.WifiP2pManager$DnsSdTxtRecordListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.net.wifi.p2p.WifiP2pManager$GroupInfoListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.net.wifi.p2p.WifiP2pManager$PeerListListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.net.wifi.p2p.WifiP2pManager$ServiceResponseListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.net.wifi.p2p.WifiP2pManager$UpnpServiceResponseListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.os.CancellationSignal$OnCancelListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.os.IBinder$DeathRecipient
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.os.MessageQueue$IdleHandler
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.os.RecoverySystem$ProgressListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.preference.Preference$OnPreferenceChangeListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.preference.Preference$OnPreferenceClickListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.preference.PreferenceFragment$OnPreferenceStartFragmentCallback
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.preference.PreferenceManager$OnActivityDestroyListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.preference.PreferenceManager$OnActivityResultListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.preference.PreferenceManager$OnActivityStopListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.security.KeyChainAliasCallback
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.speech.RecognitionListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.speech.tts.TextToSpeech$OnInitListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.speech.tts.TextToSpeech$OnUtteranceCompletedListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.view.ActionMode$Callback
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.view.ActionProvider$VisibilityListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.view.GestureDetector$OnDoubleTapListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.view.GestureDetector$OnGestureListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.view.InputQueue$Callback
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.view.KeyEvent$Callback
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.view.MenuItem$OnActionExpandListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.view.MenuItem$OnMenuItemClickListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.view.ScaleGestureDetector$OnScaleGestureListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.view.SurfaceHolder$Callback
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.view.SurfaceHolder$Callback2
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.view.TextureView$SurfaceTextureListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.view.View$OnAttachStateChangeListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.view.View$OnClickListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.view.View$OnCreateContextMenuListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.view.View$OnDragListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.view.View$OnFocusChangeListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.view.View$OnGenericMotionListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.view.View$OnHoverListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.view.View$OnKeyListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.view.View$OnLayoutChangeListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.view.View$OnLongClickListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.view.View$OnSystemUiVisibilityChangeListener�
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.view.View$OnTouchListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.view.ViewGroup$OnHierarchyChangeListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.view.ViewStub$OnInflateListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.view.ViewTreeObserver$OnDrawListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.view.ViewTreeObserver$OnGlobalFocusChangeListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.view.ViewTreeObserver$OnGlobalLayoutListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.view.ViewTreeObserver$OnPreDrawListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.view.ViewTreeObserver$OnScrollChangedListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.view.ViewTreeObserver$OnTouchModeChangeListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.view.accessibility.AccessibilityManager$AccessibilityStateChangeListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.view.animation.Animation$AnimationListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.view.inputmethod.InputMethod$SessionCallback
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.view.inputmethod.InputMethodSession$EventCallback
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.view.textservice.SpellCheckerSession$SpellCheckerSessionListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.webkit.DownloadListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.widget.AbsListView$MultiChoiceModeListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.widget.AbsListView$OnScrollListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.widget.AbsListView$RecyclerListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.widget.AdapterView$OnItemClickListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.widget.AdapterView$OnItemLongClickListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.widget.AdapterView.OnItemSelectedListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.widget.AutoCompleteTextView$OnDismissListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.widget.CalendarView$OnDateChangeListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.widget.Chronometer$OnChronometerTickListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.widget.CompoundButton$OnCheckedChangeListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.widget.DatePicker$OnDateChangedListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.widget.ExpandableListView$OnChildClickListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.widget.ExpandableListView$OnGroupClickListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.widget.ExpandableListView$OnGroupCollapseListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.widget.ExpandableListView$OnGroupExpandListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.widget.Filter$FilterListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.widget.NumberPicker$OnScrollListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.widget.NumberPicker$OnValueChangeListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.widget.NumberPicker$OnDismissListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.widget.PopupMenu$OnMenuItemClickListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.widget.PopupWindow$OnDismissListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.widget.RadioGroup$OnCheckedChangeListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.widget.RatingBar$OnRatingBarChangeListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.widget.SearchView$OnCloseListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.widget.SearchView$OnQueryTextListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.widget.SearchView$OnSuggestionListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.widget.SeekBar$OnSeekBarChangeListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.widget.ShareActionProvider$OnShareTargetSelectedListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.widget.SlidingDrawer$OnDrawerCloseListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.widget.SlidingDrawer$OnDrawerOpenListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.widget.SlidingDrawer$OnDrawerScrollListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.widget.TabHost$OnTabChangeListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.widget.TextView$OnEditorActionListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.widget.TimePicker$OnTimeChangedListener
[main] WARN soot.jimple.infoflow.android.data.parsers.PermissionMethodParser - Line does not match: android.widget.ZoomButtonsController$OnZoomListener 
[main] INFO soot.jimple.infoflow.android.source.AccessPathBasedSourceSinkManager - Created a SourceSinkManager with 0 sources, 0 sinks, and 48 callback methods.
[main] INFO soot.jimple.infoflow.android.SetupApplication - Collecting callbacks and building a callgraph took 30 seconds
[main] INFO soot.jimple.infoflow.android.SetupApplication - Running data flow analysis on /Users/yenshou/Downloads/taobao_FlowDroid/taobao.apk with 0 sources and 0 sinks...
[main] INFO soot.jimple.infoflow.InfoflowConfiguration - Implicit flow tracking is NOT enabled
[main] INFO soot.jimple.infoflow.InfoflowConfiguration - Exceptional flow tracking is enabled
[main] INFO soot.jimple.infoflow.InfoflowConfiguration - Running with a maximum access path length of 5
[main] INFO soot.jimple.infoflow.InfoflowConfiguration - Using path-agnostic result collection
[main] INFO soot.jimple.infoflow.InfoflowConfiguration - Recursive access path shortening is enabled
[main] INFO soot.jimple.infoflow.InfoflowConfiguration - Taint analysis enabled: true
[main] INFO soot.jimple.infoflow.InfoflowConfiguration - Using alias algorithm FlowSensitive
[main] INFO soot.jimple.infoflow.memory.MemoryWarningSystem - Registered a memory warning system for 3,686.4 MiB
[main] INFO soot.jimple.infoflow.android.SetupApplication$InPlaceInfoflow - Callgraph construction took 0 seconds
[main] INFO soot.jimple.infoflow.codeOptimization.InterproceduralConstantValuePropagator - Removing side-effect free methods is disabled
[main] INFO soot.jimple.infoflow.android.SetupApplication$InPlaceInfoflow - Dead code elimination took 0.787327344 seconds
[main] INFO soot.jimple.infoflow.android.SetupApplication$InPlaceInfoflow - Callgraph has 17477 edges
[main] INFO soot.jimple.infoflow.android.SetupApplication$InPlaceInfoflow - Starting Taint Analysis
[main] INFO soot.jimple.infoflow.android.SetupApplication$InPlaceInfoflow - Using context- and flow-sensitive solver
[main] INFO soot.jimple.infoflow.android.SetupApplication$InPlaceInfoflow - Using context- and flow-sensitive solver
[main] WARN soot.jimple.infoflow.android.SetupApplication$InPlaceInfoflow - Running with limited join point abstractions can break context-sensitive path builders
[main] INFO soot.jimple.infoflow.android.SetupApplication$InPlaceInfoflow - Looking for sources and sinks...
[main] ERROR soot.jimple.infoflow.android.SetupApplication$InPlaceInfoflow - No sources found, aborting analysis
[main] INFO soot.jimple.infoflow.memory.MemoryWarningSystem - Shutting down the memory warning system...
[main] WARN soot.jimple.infoflow.android.SetupApplication$InPlaceInfoflow - No results found.
[main] INFO soot.jimple.infoflow.android.SetupApplication$InPlaceInfoflow - Data flow solver took 1 seconds. Maximum memory consumption: 383 MB
[main] INFO soot.jimple.infoflow.android.SetupApplication - Found 0 leaks
```

Something we need to test further...
```
java -Xmx4g -cp sootclasses-trunk-jar-with-dependencies.jar:soot-infoflow.jar:soot-infoflow-android.jar:slf4j-api-1.7.5.jar:slf4j-simple-1.7.5.jar:axml-2.0.jar /Users/yenshou/Downloads/taobao_FlowDroid/AndroidCallbacks.txt “/Users/yenshou/Downloads/taobao_FlowDroid/taobao.apk" /Users/yenshou/Library/Android/sdk/platforms/android-28/android.jar
```
