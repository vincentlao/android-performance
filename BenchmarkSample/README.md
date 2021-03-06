Benchmark Sample
===================================

This sample project shows how to use the Jetpack Benchmark library.

It includes multiple simple benchmark samples:

* [AutoBoxingBenchmark](benchmark/src/androidTest/java/com/example/benchmark/AutoBoxingBenchmark.kt)
measures the cost of allocating Integer() objects.

* [BitmapBenchmark](benchmark/src/androidTest/java/com/example/benchmark/BitmapBenchmark.kt)
measures the cost of accessing Bitmap pixels, showing the overhead of many JNI
calls versus one in the underlying Android platform code.

As well as one more complex UI benchmark:

* [RecyclerViewBenchmark](benchmark/src/androidTest/java/com/example/benchmark/RecyclerViewBenchmark.kt)
measures the cost of scrolling a RecyclerView UI defined in another UI library
module.

### Running

Open the project in Android Studio 3.4 or later, and run benchmarks as you
usually would run tests: Ctrl-Shift-F10 (Mac: Ctrl-Shift-R)


### Locking Clocks

If you have a rooted device you can benchmark on, use `./gradlew lockClocks` to
lock the CPU clocks of the device to stable values. To unlock clocks, use
`./gradlew unlockClocks`, or reboot your device. This feature is provided by the
`androidx.benchmark` gradle plugin.

License
-------

Copyright 2019 The Android Open Source Project, Inc.

Licensed to the Apache Software Foundation (ASF) under one or more contributor
license agreements.  See the NOTICE file distributed with this work for
additional information regarding copyright ownership.  The ASF licenses this
file to you under the Apache License, Version 2.0 (the "License"); you may not
use this file except in compliance with the License.  You may obtain a copy of
the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS, WITHOUT
WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.  See the
License for the specific language governing permissions and limitations under
the License.
