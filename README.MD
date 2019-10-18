Built with Bazel version 1.0.0

`bazel build //...` results in the following

```
changd-mbp:issue_maven_repository_rules changd$ bazel build //...
Starting local Bazel server and connecting to it...
INFO: Writing tracer profile to '/private/var/tmp/_bazel_changd/f1f23cd09bac1bdb00d47ab2bacdce11/command.profile.gz'
INFO: Analyzed 3 targets (104 packages loaded, 958 targets configured).
INFO: Found 3 targets...
INFO: Deleting stale sandbox base /private/var/tmp/_bazel_changd/f1f23cd09bac1bdb00d47ab2bacdce11/sandbox
ERROR: /Users/changd/dev/issue_maven_repository_rules/oxygen/BUILD:5:1: Compiling Kotlin to JVM //oxygen:oxygen_kt { kt: 1, java: 0, srcjars: 0 } failed: Worker process did not return a WorkResponse:

---8<---8<--- Start of log, file at /private/var/tmp/_bazel_changd/f1f23cd09bac1bdb00d47ab2bacdce11/bazel-workers/worker-1-KotlinCompile.log ---8<---8<---
Exception in thread "main" java.lang.reflect.InvocationTargetException
	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62)
	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
	at java.base/java.lang.reflect.Method.invoke(Method.java:566)
	at io.bazel.kotlin.builder.toolchain.KotlinToolchain$JDepsInvoker.run(KotlinToolchain.kt:99)
	at io.bazel.kotlin.builder.tasks.jvm.JDepsGenerator.generateJDeps(JDepsGenerator.kt:56)
	at io.bazel.kotlin.builder.tasks.jvm.KotlinJvmTaskExecutor$execute$4.invoke(KotlinJvmTaskExecutor.kt:43)
	at io.bazel.kotlin.builder.tasks.jvm.KotlinJvmTaskExecutor$execute$4.invoke(KotlinJvmTaskExecutor.kt:32)
	at io.bazel.kotlin.builder.utils.CompilationTaskContext.execute(CompilationTaskContext.kt:140)
	at io.bazel.kotlin.builder.utils.CompilationTaskContext.execute(CompilationTaskContext.kt:132)
	at io.bazel.kotlin.builder.tasks.jvm.KotlinJvmTaskExecutor.execute(KotlinJvmTaskExecutor.kt:43)
	at io.bazel.kotlin.builder.tasks.KotlinBuilder.executeJvmTask(KotlinBuilder.kt:186)
	at io.bazel.kotlin.builder.tasks.KotlinBuilder.apply(KotlinBuilder.kt:51)
	at io.bazel.kotlin.builder.tasks.BazelWorker.runAsPersistentWorker(BazelWorker.kt:88)
	at io.bazel.kotlin.builder.tasks.BazelWorker.apply(BazelWorker.kt:67)
	at io.bazel.kotlin.builder.KotlinBuilderMain.main(KotlinBuilderMain.java:30)
Caused by: java.io.UncheckedIOException: java.util.zip.ZipException: zip END header not found
	at jdk.jdeps/com.sun.tools.jdeps.Archive.getInstance(Archive.java:52)
	at jdk.jdeps/com.sun.tools.jdeps.JdepsConfiguration.<init>(JdepsConfiguration.java:132)
	at jdk.jdeps/com.sun.tools.jdeps.JdepsConfiguration$Builder.build(JdepsConfiguration.java:563)
	at jdk.jdeps/com.sun.tools.jdeps.JdepsTask.buildConfig(JdepsTask.java:589)
	at jdk.jdeps/com.sun.tools.jdeps.JdepsTask.run(JdepsTask.java:543)
	at jdk.jdeps/com.sun.tools.jdeps.JdepsTask.run(JdepsTask.java:519)
	at jdk.jdeps/com.sun.tools.jdeps.Main.run(Main.java:64)
	... 16 more
Caused by: java.util.zip.ZipException: zip END header not found
	at java.base/java.util.zip.ZipFile$Source.zerror(ZipFile.java:1529)
	at java.base/java.util.zip.ZipFile$Source.findEND(ZipFile.java:1430)
	at java.base/java.util.zip.ZipFile$Source.initCEN(ZipFile.java:1437)
	at java.base/java.util.zip.ZipFile$Source.<init>(ZipFile.java:1268)
	at java.base/java.util.zip.ZipFile$Source.get(ZipFile.java:1231)
	at java.base/java.util.zip.ZipFile$CleanableResource.<init>(ZipFile.java:726)
	at java.base/java.util.zip.ZipFile$CleanableResource.get(ZipFile.java:843)
	at java.base/java.util.zip.ZipFile.<init>(ZipFile.java:246)
	at java.base/java.util.zip.ZipFile.<init>(ZipFile.java:176)
	at java.base/java.util.jar.JarFile.<init>(JarFile.java:346)
	at java.base/java.util.jar.JarFile.<init>(JarFile.java:317)
	at java.base/java.util.jar.JarFile.<init>(JarFile.java:297)
	at jdk.jdeps/com.sun.tools.jdeps.ClassFileReader$JarFileReader.openJarFile(ClassFileReader.java:322)
	at jdk.jdeps/com.sun.tools.jdeps.ClassFileReader$JarFileReader.<init>(ClassFileReader.java:304)
	at jdk.jdeps/com.sun.tools.jdeps.ClassFileReader.newInstance(ClassFileReader.java:79)
	at jdk.jdeps/com.sun.tools.jdeps.Archive.getInstance(Archive.java:50)
	... 22 more
---8<---8<--- End of log ---8<---8<---
INFO: Elapsed time: 12.694s, Critical Path: 3.94s
INFO: 1 process: 1 worker.
FAILED: Build did NOT complete successfullychangd-mbp:issue_maven_repository_rules changd$ bazel build //...
Starting local Bazel server and connecting to it...
INFO: Writing tracer profile to '/private/var/tmp/_bazel_changd/f1f23cd09bac1bdb00d47ab2bacdce11/command.profile.gz'
INFO: Analyzed 3 targets (104 packages loaded, 958 targets configured).
INFO: Found 3 targets...
INFO: Deleting stale sandbox base /private/var/tmp/_bazel_changd/f1f23cd09bac1bdb00d47ab2bacdce11/sandbox
ERROR: /Users/changd/dev/issue_maven_repository_rules/oxygen/BUILD:5:1: Compiling Kotlin to JVM //oxygen:oxygen_kt { kt: 1, java: 0, srcjars: 0 } failed: Worker process did not return a WorkResponse:

---8<---8<--- Start of log, file at /private/var/tmp/_bazel_changd/f1f23cd09bac1bdb00d47ab2bacdce11/bazel-workers/worker-1-KotlinCompile.log ---8<---8<---
Exception in thread "main" java.lang.reflect.InvocationTargetException
	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62)
	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
	at java.base/java.lang.reflect.Method.invoke(Method.java:566)
	at io.bazel.kotlin.builder.toolchain.KotlinToolchain$JDepsInvoker.run(KotlinToolchain.kt:99)
	at io.bazel.kotlin.builder.tasks.jvm.JDepsGenerator.generateJDeps(JDepsGenerator.kt:56)
	at io.bazel.kotlin.builder.tasks.jvm.KotlinJvmTaskExecutor$execute$4.invoke(KotlinJvmTaskExecutor.kt:43)
	at io.bazel.kotlin.builder.tasks.jvm.KotlinJvmTaskExecutor$execute$4.invoke(KotlinJvmTaskExecutor.kt:32)
	at io.bazel.kotlin.builder.utils.CompilationTaskContext.execute(CompilationTaskContext.kt:140)
	at io.bazel.kotlin.builder.utils.CompilationTaskContext.execute(CompilationTaskContext.kt:132)
	at io.bazel.kotlin.builder.tasks.jvm.KotlinJvmTaskExecutor.execute(KotlinJvmTaskExecutor.kt:43)
	at io.bazel.kotlin.builder.tasks.KotlinBuilder.executeJvmTask(KotlinBuilder.kt:186)
	at io.bazel.kotlin.builder.tasks.KotlinBuilder.apply(KotlinBuilder.kt:51)
	at io.bazel.kotlin.builder.tasks.BazelWorker.runAsPersistentWorker(BazelWorker.kt:88)
	at io.bazel.kotlin.builder.tasks.BazelWorker.apply(BazelWorker.kt:67)
	at io.bazel.kotlin.builder.KotlinBuilderMain.main(KotlinBuilderMain.java:30)
Caused by: java.io.UncheckedIOException: java.util.zip.ZipException: zip END header not found
	at jdk.jdeps/com.sun.tools.jdeps.Archive.getInstance(Archive.java:52)
	at jdk.jdeps/com.sun.tools.jdeps.JdepsConfiguration.<init>(JdepsConfiguration.java:132)
	at jdk.jdeps/com.sun.tools.jdeps.JdepsConfiguration$Builder.build(JdepsConfiguration.java:563)
	at jdk.jdeps/com.sun.tools.jdeps.JdepsTask.buildConfig(JdepsTask.java:589)
	at jdk.jdeps/com.sun.tools.jdeps.JdepsTask.run(JdepsTask.java:543)
	at jdk.jdeps/com.sun.tools.jdeps.JdepsTask.run(JdepsTask.java:519)
	at jdk.jdeps/com.sun.tools.jdeps.Main.run(Main.java:64)
	... 16 more
Caused by: java.util.zip.ZipException: zip END header not found
	at java.base/java.util.zip.ZipFile$Source.zerror(ZipFile.java:1529)
	at java.base/java.util.zip.ZipFile$Source.findEND(ZipFile.java:1430)
	at java.base/java.util.zip.ZipFile$Source.initCEN(ZipFile.java:1437)
	at java.base/java.util.zip.ZipFile$Source.<init>(ZipFile.java:1268)
	at java.base/java.util.zip.ZipFile$Source.get(ZipFile.java:1231)
	at java.base/java.util.zip.ZipFile$CleanableResource.<init>(ZipFile.java:726)
	at java.base/java.util.zip.ZipFile$CleanableResource.get(ZipFile.java:843)
	at java.base/java.util.zip.ZipFile.<init>(ZipFile.java:246)
	at java.base/java.util.zip.ZipFile.<init>(ZipFile.java:176)
	at java.base/java.util.jar.JarFile.<init>(JarFile.java:346)
	at java.base/java.util.jar.JarFile.<init>(JarFile.java:317)
	at java.base/java.util.jar.JarFile.<init>(JarFile.java:297)
	at jdk.jdeps/com.sun.tools.jdeps.ClassFileReader$JarFileReader.openJarFile(ClassFileReader.java:322)
	at jdk.jdeps/com.sun.tools.jdeps.ClassFileReader$JarFileReader.<init>(ClassFileReader.java:304)
	at jdk.jdeps/com.sun.tools.jdeps.ClassFileReader.newInstance(ClassFileReader.java:79)
	at jdk.jdeps/com.sun.tools.jdeps.Archive.getInstance(Archive.java:50)
	... 22 more
---8<---8<--- End of log ---8<---8<---
INFO: Elapsed time: 12.694s, Critical Path: 3.94s
INFO: 1 process: 1 worker.
FAILED: Build did NOT complete successfully
```