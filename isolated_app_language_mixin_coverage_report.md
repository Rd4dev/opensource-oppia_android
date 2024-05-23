## Isolating target coverage data

### Note:
- It requires the target name not the file name
- It utilizes the --instrumentation_filter

## Command Sample:
$ **bazel coverage --instrumentation_filter='app/src/main/java/org/oppia/android/app/translation:app_language_watcher_mixin' //app/src/test/java/org/oppia/android/app/translation:AppLanguageWatcherMixinTest**

```sh
rd4dev@DESKTOP-CLN30QH:~/codecoverage/oppia-android$ bazel coverage --instrumentation_filter='app/src/main/java/org/oppia/android/app/translation:app_language_watcher_mixin' //app/src/test/java/org/oppia/android/app/translation:AppLanguageWatcherMixinTest
INFO: Build option --instrumentation_filter has changed, discarding analysis cache.
INFO: Analyzed target //app/src/test/java/org/oppia/android/app/translation:AppLanguageWatcherMixinTest (236 packages loaded, 5989 targets configured).
INFO: Found 1 test target...
Target //app/src/test/java/org/oppia/android/app/translation:AppLanguageWatcherMixinTest up-to-date:
  bazel-bin/app/src/test/java/org/oppia/android/app/translation/AppLanguageWatcherMixinTest.jar
  bazel-bin/app/src/test/java/org/oppia/android/app/translation/AppLanguageWatcherMixinTest
INFO: Elapsed time: 96.097s, Critical Path: 38.56s
INFO: 4 processes: 1 internal, 2 linux-sandbox, 1 worker.
INFO: Build completed successfully, 4 total actions
PASSED: //app/src/test/java/org/oppia/android/app/translation:AppLanguageWatcherMixinTest (see /home/rd4dev/.cache/bazel/_bazel_rd4dev/a059af30b4a45ffc89089e187ccd1d18/execroot/__main__/bazel-out/k8-fastbuild/testlogs/app/src/test/java/org/oppia/android/app/translation/AppLanguageWatcherMixinTest/test.log)
INFO: From Testing //app/src/test/java/org/oppia/android/app/translation:AppLanguageWatcherMixinTest
==================== Test output for //app/src/test/java/org/oppia/android/app/translation:AppLanguageWatcherMixinTest:
JUnit4 Test Runner
.Cleaner.create(android.view.ThreadedRenderer@505f4b3e,android.graphics.HardwareRenderer$DestroyContextRunnable@12e717bd)
.Cleaner.create(android.view.ThreadedRenderer@12f2698b,android.graphics.HardwareRenderer$DestroyContextRunnable@35e72b21)
System.logW: A resource was acquired at attached stack trace but never released. See java.io.Closeable for information on avoiding resource leaks.java.lang.Throwable: Explicit termination method 'dispose' not called
.Cleaner.create(android.view.ThreadedRenderer@45f403da,android.graphics.HardwareRenderer$DestroyContextRunnable@7b1ced70)
System.logW: A resource was acquired at attached stack trace but never released. See java.io.Closeable for information on avoiding resource leaks.java.lang.Throwable: Explicit termination method 'dispose' not called
.Cleaner.create(android.view.ThreadedRenderer@7c943241,android.graphics.HardwareRenderer$DestroyContextRunnable@ddb7c21)
.System.logW: A resource was acquired at attached stack trace but never released. See java.io.Closeable for information on avoiding resource leaks.java.lang.Throwable: Explicit termination method 'dispose' not called
Cleaner.create(android.view.ThreadedRenderer@4da37e13,android.graphics.HardwareRenderer$DestroyContextRunnable@4c9e6178)

Time: 10.231

OK (5 tests)


BazelTestRunner exiting with a return value of 0
JVM shutdown hooks (if any) will run now.
The JVM will exit once they complete.

-- JVM shutdown starting at 2024-05-21 12:40:39 --

May 21, 2024 12:40:40 PM com.google.devtools.coverageoutputgenerator.Main getTracefiles
INFO: Found 1 tracefiles.
May 21, 2024 12:40:40 PM com.google.devtools.coverageoutputgenerator.Main parseFilesSequentially
INFO: Parsing file /home/rd4dev/.cache/bazel/_bazel_rd4dev/a059af30b4a45ffc89089e187ccd1d18/sandbox/linux-sandbox/544/execroot/__main__/bazel-out/k8-fastbuild/testlogs/_coverage/app/src/test/java/org/oppia/android/app/translation/AppLanguageWatcherMixinTest/test/jvcov14428944142765399764.dat
May 21, 2024 12:40:40 PM com.google.devtools.coverageoutputgenerator.Main getGcovInfoFiles
INFO: No gcov info file found.
May 21, 2024 12:40:40 PM com.google.devtools.coverageoutputgenerator.Main getGcovJsonInfoFiles
INFO: No gcov json file found.
May 21, 2024 12:40:40 PM com.google.devtools.coverageoutputgenerator.Main getProfdataFileOrNull
INFO: No .profdata file found.
================================================================================
//app/src/test/java/org/oppia/android/app/translation:AppLanguageWatcherMixinTest (cached) PASSED in 11.7s
  /home/rd4dev/.cache/bazel/_bazel_rd4dev/a059af30b4a45ffc89089e187ccd1d18/execroot/__main__/bazel-out/k8-fastbuild/testlogs/app/src/test/java/org/oppia/android/app/translation/AppLanguageWatcherMixinTest/coverage.dat

Executed 0 out of 1 test: 1 test passes.
There were tests whose specified size is too big. Use the --test_verbose_timeout_warnings command line option to see which ones these are.
rd4dev@DESKTOP-CLN30QH:~/codecoverage/oppia-android$ cat /home/rd4dev/.cache/bazel/_bazel_rd4dev/a059af30b4a45ffc89089e187ccd1d18/execroot/__main__/bazel-out/k8-fastbuild/testlogs/app/src/test/java/org/oppia/android/app/translation/AppLanguageWatcherMixinTest/coverage.dat
SF:app/src/main/java/org/oppia/android/app/translation/AppLanguageWatcherMixin.kt
FN:70,org/oppia/android/app/translation/AppLanguageWatcherMixin$initialize$1::<init> (Lorg/oppia/android/app/translation/AppLanguageWatcherMixin;Landroidx/lifecycle/LiveData;)V
FN:72,org/oppia/android/app/translation/AppLanguageWatcherMixin$initialize$1::onChanged (Lorg/oppia/android/util/data/AsyncResult;)V
FN:20,org/oppia/android/app/translation/AppLanguageWatcherMixin::<init> (Landroidx/appcompat/app/AppCompatActivity;Lorg/oppia/android/domain/translation/TranslationController;Lorg/oppia/android/app/translation/AppLanguageLocaleHandler;Lorg/oppia/android/domain/locale/LocaleController;Lorg/oppia/android/domain/oppialogger/OppiaLogger;Lorg/oppia/android/app/translation/ActivityRecreator;)V
FN:38,org/oppia/android/app/translation/AppLanguageWatcherMixin::initialize ()V
FNDA:1,org/oppia/android/app/translation/AppLanguageWatcherMixin$initialize$1::<init> (Lorg/oppia/android/app/translation/AppLanguageWatcherMixin;Landroidx/lifecycle/LiveData;)V
FNDA:1,org/oppia/android/app/translation/AppLanguageWatcherMixin$initialize$1::onChanged (Lorg/oppia/android/util/data/AsyncResult;)V
FNDA:1,org/oppia/android/app/translation/AppLanguageWatcherMixin::<init> (Landroidx/appcompat/app/AppCompatActivity;Lorg/oppia/android/domain/translation/TranslationController;Lorg/oppia/android/app/translation/AppLanguageLocaleHandler;Lorg/oppia/android/domain/locale/LocaleController;Lorg/oppia/android/domain/oppialogger/OppiaLogger;Lorg/oppia/android/app/translation/ActivityRecreator;)V
FNDA:1,org/oppia/android/app/translation/AppLanguageWatcherMixin::initialize ()V
FNF:4
FNH:4
BRDA:38,0,0,1
BRDA:38,0,1,0
BRDA:73,0,0,1
BRDA:73,0,1,0
BRDA:76,0,0,1
BRDA:76,0,1,1
BRDA:93,0,0,-
BRDA:93,0,1,-
BRDA:99,0,0,-
BRDA:99,0,1,-
BRF:10
BRH:4
DA:20,1
DA:21,1
DA:22,1
DA:23,1
DA:24,1
DA:25,1
DA:26,1
DA:38,1
DA:55,0
DA:56,0
DA:58,0
DA:59,0
DA:61,0
DA:65,1
DA:66,1
DA:67,1
DA:68,1
DA:69,1
DA:70,1
DA:72,1
DA:73,1
DA:76,1
DA:89,1
DA:90,1
DA:93,0
DA:94,0
DA:95,0
DA:96,0
DA:99,0
DA:101,1
DA:104,1
LH:21
LF:31
end_of_record
rd4dev@DESKTOP-CLN30QH:~/codecoverage/oppia-android$
```
