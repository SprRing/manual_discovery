# manual_discovery
Here is what we can see using the very basic settings.
And there are 11 memory leaks.
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
