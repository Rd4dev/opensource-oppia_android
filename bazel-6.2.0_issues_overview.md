## Migration to Bazel 6.2.0

### Steps undertaken:

1. **Own implementation of migrating to Bazel 6.2.0**
   
   In addition to migrating to a newer Bazel and Kotlin version, the following upgrades were made:
   - dagger[2.48]
   - kotlin [1.5.32]
   - rules_kotlin [v1.9.0]
   - rules_java [5.3.4]

2. **Used the exact PR #4886 migrate-to-newer-bazel-and-kotlin branch**

   Both implementations yielded the same outputs and issues. For testing, [PR #4886](https://github.com/oppia/oppia-android/pull/4886) - `migrate-to-newer-bazel-and-kotlin` branch was utilized.

   Note: All the following results were from the execution of the migrate-to-newer-bazel-and-kotlin branch.

#### Outcomes:

**Bazel 4.0.0**
- While with Bazel 4.0.0, following the provided [wiki instructions](https://github.com/oppia/oppia-android/wiki/Bazel-Setup-Instructions-for-Windows), the following commands were executable:
  - `bazel build :target`
  - `bazel test :target`

**Bazel 6.2.0**
##### Bazel build:

###### Issues:

Encountered error while attempting to build oppia with Bazel 6.2.0, using migrate-to-newer-bazel-and-kotlin execution.

Error Encountered:
![Screenshot (971)](https://github.com/Rd4dev/opensource-oppia_android/assets/122200035/cd1f8729-d5a7-46a7-afc6-bede36e8297b)

This error was observed with both migrate-to-newer-bazel-and-kotlin execution and the own implementation. It seems like there might be environmental issues or missing build tools. Further investigation is needed to identify and rectify any missing dependencies. 

_Additionally, I'm interested in understanding whether the PR represents a functional version. If it does, I'd appreciate knowing if there are any extra tools needed to ensure a successful build, given that I managed to build successfully with Bazel 4.0.0. I also raised inquiries within the [comments section](https://github.com/oppia/oppia-android/pull/4886#issuecomment-2094666282)._

**Installed SDK Manager Tools:**
  Path                                                                              | Version           | Description                        | Location
  -------                                                                           | -------           | -------                            | -------
  add-ons;addon-google_apis-google-23                                               | 1                 | Google APIs                        | add-ons/addon-google_apis-google-23
  build-tools;29.0.2                                                                | 29.0.2            | Android SDK Build-Tools 29.0.2     | build-tools/29.0.2
  build-tools;30.0.0                                                                | 30.0.0            | Android SDK Build-Tools 30         | build-tools/30.0.0
  build-tools;30.0.1                                                                | 30.0.1            | Android SDK Build-Tools 30.0.1     | build-tools/30.0.1
  build-tools;30.0.3                                                                | 30.0.3            | Android SDK Build-Tools 30.0.3     | build-tools/30.0.3
  build-tools;31.0.0                                                                | 31.0.0            | Android SDK Build-Tools 31         | build-tools/31.0.0
  build-tools;32.0.0                                                                | 32.0.0            | Android SDK Build-Tools 32         | build-tools/32.0.0
  build-tools;33.0.0                                                                | 33.0.0            | Android SDK Build-Tools 33         | build-tools/33.0.0
  emulator                                                                          | 34.1.19           | Android Emulator                   | emulator
  extras;m2repository;com;android;...1.0.1                                          | 1                 | Solver for ConstraintLayout 1.0.1  | extras/m2repository/com/android/.../1.0.1
  extras;m2repository;com;android;...1.0.1                                          | 1                 | ConstraintLayout for Android 1.0.1 | extras/m2repository/com/android/.../1.0.1
  ndk;26.1.10909125                                                                 | 26.1.10909125     | NDK (Side by side) 26.1.10909125   | ndk/26.1.10909125
  ndk;27.0.11718014                                                                 | 27.0.11718014 rc1 | NDK (Side by side) 27.0.11718014   | ndk/27.0.11718014
  platform-tools                                                                    | 35.0.1            | Android SDK Platform-Tools         | platform-tools
  platforms;android-31                                                              | 1                 | Android SDK Platform 31            | platforms/android-31
  platforms;android-32                                                              | 1                 | Android SDK Platform 32            | platforms/android-32
  platforms;android-33                                                              | 3                 | Android SDK Platform 33            | platforms/android-33


Tried with both JDK 8 and JDK 11.

###### Solutions Attempted:

- Upgraded build tools to versions 30.0.0, 30.0.1, 30.0.3, 31.0.0, and 32.0.0 as per the [comment](https://github.com/google/mediapipe/issues/3481#issuecomment-1239010710).
- Added repositories as per the following [thread suggestion](https://github.com/google/mediapipe/issues/3365#issuecomment-1135883896).
- Upgraded the following dependencies:
  - dagger[2.48]
  - kotlin [1.5.32]
  - rules_kotlin [v1.9.0]
  - rules_java [5.3.4]
  - moshi [1.15.0]

However, the same issue persisted.

##### Bazel test:

But more importantly `bazel test` works as expected. Coverage support is enabled with Bazel 6.2.0, allowing for the generation of coverage reports in `.dat` files.

Tested the execution with the math module test file, resulting in PASSED tests and coverage generation. Video samples and images were attached for reference.

**Screen Recording of running bazel test with bazel 6.2.0, jdk - 11:**

https://github.com/Rd4dev/opensource-oppia_android/assets/122200035/84994b06-c878-447a-8c82-43d8de2a4bfd

**Screenshots:**

Test Passing:
![Screenshot (691)](https://github.com/Rd4dev/opensource-oppia_android/assets/122200035/ca5647ce-cdd6-4e9e-8dae-f7975fbaf8e0)

Coverage Report:
![Screenshot (970)](https://github.com/Rd4dev/opensource-oppia_android/assets/122200035/f33290b2-d5b2-4fde-9a56-45eee28f5562)

#### Will this hinder the 4.1 project implementation?

### No!

The project primarily focuses on generating tests with migration to Bazel 6.2.0 for the test targets. Since the _test execution and coverage report generation are functioning properly_, **it shouldn't hinder the project workflow**. However, resolving the issue with `bazel build` could be crucial. Ensuring all environmental dependencies are met and staying updated with PR #4886 will be essential to address any hindrances in building Bazel targets.

Currently, there are no hindrances to the project implementation, but efforts are directed towards resolving the `bazel build` issue. A prototype will be developed once the proposal is set to ensure smooth project implementation. During the Community Bonding Period (CBP), focus will be on getting `bazel build` working seamlessly (under mandatory conditions) and testing out a prototype so there are no unexpected hindrances in the actual coding phase.
