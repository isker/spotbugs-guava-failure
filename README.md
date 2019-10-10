```
λ ./gradlew spotbugsMain
> Task :compileJava UP-TO-DATE
> Task :processResources NO-SOURCE
> Task :classes UP-TO-DATE
> Task :spotbugsMain FAILED

FAILURE: Build failed with an exception.

* What went wrong:
Execution failed for task ':spotbugsMain'.
> Failed to run Gradle SpotBugs Worker
   > Could not create an instance of type com.github.spotbugs.internal.spotbugs.SpotBugsExecutor.
      > com.google.common.collect.ImmutableList.builderWithExpectedSize(I)Lcom/google/common/collect/ImmutableList$Builder;

* Try:
Run with --stacktrace option to get the stack trace. Run with --info or --debug option to get more log output. Run with --scan to get full insights.

* Get more help at https://help.gradle.org

BUILD FAILED in 1s
2 actionable tasks: 1 executed, 1 up-to-date
```
