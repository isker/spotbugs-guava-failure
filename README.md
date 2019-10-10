```
λ ./gradlew spotbugsMain --stacktrace
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
Run with --info or --debug option to get more log output. Run with --scan to get full insights.

* Exception is:
org.gradle.api.tasks.TaskExecutionException: Execution failed for task ':spotbugsMain'.
	at org.gradle.api.internal.tasks.execution.ExecuteActionsTaskExecuter$3.accept(ExecuteActionsTaskExecuter.java:166)
	at org.gradle.api.internal.tasks.execution.ExecuteActionsTaskExecuter$3.accept(ExecuteActionsTaskExecuter.java:163)
	at org.gradle.internal.Try$Failure.ifSuccessfulOrElse(Try.java:191)
	at org.gradle.api.internal.tasks.execution.ExecuteActionsTaskExecuter.execute(ExecuteActionsTaskExecuter.java:156)
	at org.gradle.api.internal.tasks.execution.ValidatingTaskExecuter.execute(ValidatingTaskExecuter.java:62)
	at org.gradle.api.internal.tasks.execution.SkipEmptySourceFilesTaskExecuter.execute(SkipEmptySourceFilesTaskExecuter.java:108)
	at org.gradle.api.internal.tasks.execution.ResolveBeforeExecutionOutputsTaskExecuter.execute(ResolveBeforeExecutionOutputsTaskExecuter.java:67)
	at org.gradle.api.internal.tasks.execution.ResolveAfterPreviousExecutionStateTaskExecuter.execute(ResolveAfterPreviousExecutionStateTaskExecuter.java:46)
	at org.gradle.api.internal.tasks.execution.CleanupStaleOutputsExecuter.execute(CleanupStaleOutputsExecuter.java:94)
	at org.gradle.api.internal.tasks.execution.FinalizePropertiesTaskExecuter.execute(FinalizePropertiesTaskExecuter.java:46)
	at org.gradle.api.internal.tasks.execution.ResolveTaskExecutionModeExecuter.execute(ResolveTaskExecutionModeExecuter.java:95)
	at org.gradle.api.internal.tasks.execution.SkipTaskWithNoActionsExecuter.execute(SkipTaskWithNoActionsExecuter.java:57)
	at org.gradle.api.internal.tasks.execution.SkipOnlyIfTaskExecuter.execute(SkipOnlyIfTaskExecuter.java:56)
	at org.gradle.api.internal.tasks.execution.CatchExceptionTaskExecuter.execute(CatchExceptionTaskExecuter.java:36)
	at org.gradle.api.internal.tasks.execution.EventFiringTaskExecuter$1.executeTask(EventFiringTaskExecuter.java:77)
	at org.gradle.api.internal.tasks.execution.EventFiringTaskExecuter$1.call(EventFiringTaskExecuter.java:55)
	at org.gradle.api.internal.tasks.execution.EventFiringTaskExecuter$1.call(EventFiringTaskExecuter.java:52)
	at org.gradle.internal.operations.DefaultBuildOperationExecutor$CallableBuildOperationWorker.execute(DefaultBuildOperationExecutor.java:416)
	at org.gradle.internal.operations.DefaultBuildOperationExecutor$CallableBuildOperationWorker.execute(DefaultBuildOperationExecutor.java:406)
	at org.gradle.internal.operations.DefaultBuildOperationExecutor$1.execute(DefaultBuildOperationExecutor.java:165)
	at org.gradle.internal.operations.DefaultBuildOperationExecutor.execute(DefaultBuildOperationExecutor.java:250)
	at org.gradle.internal.operations.DefaultBuildOperationExecutor.execute(DefaultBuildOperationExecutor.java:158)
	at org.gradle.internal.operations.DefaultBuildOperationExecutor.call(DefaultBuildOperationExecutor.java:102)
	at org.gradle.internal.operations.DelegatingBuildOperationExecutor.call(DelegatingBuildOperationExecutor.java:36)
	at org.gradle.api.internal.tasks.execution.EventFiringTaskExecuter.execute(EventFiringTaskExecuter.java:52)
	at org.gradle.execution.plan.LocalTaskNodeExecutor.execute(LocalTaskNodeExecutor.java:43)
	at org.gradle.execution.taskgraph.DefaultTaskExecutionGraph$InvokeNodeExecutorsAction.execute(DefaultTaskExecutionGraph.java:355)
	at org.gradle.execution.taskgraph.DefaultTaskExecutionGraph$InvokeNodeExecutorsAction.execute(DefaultTaskExecutionGraph.java:343)
	at org.gradle.execution.taskgraph.DefaultTaskExecutionGraph$BuildOperationAwareExecutionAction.execute(DefaultTaskExecutionGraph.java:336)
	at org.gradle.execution.taskgraph.DefaultTaskExecutionGraph$BuildOperationAwareExecutionAction.execute(DefaultTaskExecutionGraph.java:322)
	at org.gradle.execution.plan.DefaultPlanExecutor$ExecutorWorker$1.execute(DefaultPlanExecutor.java:134)
	at org.gradle.execution.plan.DefaultPlanExecutor$ExecutorWorker$1.execute(DefaultPlanExecutor.java:129)
	at org.gradle.execution.plan.DefaultPlanExecutor$ExecutorWorker.execute(DefaultPlanExecutor.java:202)
	at org.gradle.execution.plan.DefaultPlanExecutor$ExecutorWorker.executeNextNode(DefaultPlanExecutor.java:193)
	at org.gradle.execution.plan.DefaultPlanExecutor$ExecutorWorker.run(DefaultPlanExecutor.java:129)
	at org.gradle.internal.concurrent.ExecutorPolicy$CatchAndRecordFailures.onExecute(ExecutorPolicy.java:64)
	at org.gradle.internal.concurrent.ManagedExecutorImpl$1.run(ManagedExecutorImpl.java:48)
	at org.gradle.internal.concurrent.ThreadFactoryImpl$ManagedThreadRunnable.run(ThreadFactoryImpl.java:56)
Caused by: org.gradle.process.internal.worker.WorkerProcessException: Failed to run Gradle SpotBugs Worker
	at org.gradle.process.internal.worker.WorkerProcessException.runFailed(WorkerProcessException.java:29)
	at org.gradle.process.internal.worker.request.Receiver.infrastructureFailed(Receiver.java:88)
	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62)
	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
	at org.gradle.internal.dispatch.ReflectionDispatch.dispatch(ReflectionDispatch.java:36)
	at org.gradle.internal.dispatch.ReflectionDispatch.dispatch(ReflectionDispatch.java:24)
	at org.gradle.internal.remote.internal.hub.MessageHubBackedObjectConnection$DispatchWrapper.dispatch(MessageHubBackedObjectConnection.java:182)
	at org.gradle.internal.remote.internal.hub.MessageHubBackedObjectConnection$DispatchWrapper.dispatch(MessageHubBackedObjectConnection.java:164)
	at org.gradle.internal.remote.internal.hub.MessageHub$Handler.run(MessageHub.java:412)
	... 3 more
Caused by: org.gradle.api.reflect.ObjectInstantiationException: Could not create an instance of type com.github.spotbugs.internal.spotbugs.SpotBugsExecutor.
	at org.gradle.internal.instantiation.DependencyInjectingInstantiator.newInstance(DependencyInjectingInstantiator.java:54)
	at org.gradle.process.internal.worker.request.WorkerAction.execute(WorkerAction.java:68)
	at org.gradle.process.internal.worker.request.WorkerAction.execute(WorkerAction.java:40)
	at org.gradle.process.internal.worker.child.ActionExecutionWorker.execute(ActionExecutionWorker.java:91)
	at org.gradle.process.internal.worker.child.ActionExecutionWorker.execute(ActionExecutionWorker.java:34)
	at org.gradle.process.internal.worker.child.SystemApplicationClassLoaderWorker.call(SystemApplicationClassLoaderWorker.java:133)
	at org.gradle.process.internal.worker.child.SystemApplicationClassLoaderWorker.call(SystemApplicationClassLoaderWorker.java:70)
	at worker.org.gradle.process.internal.worker.GradleWorkerMain.run(GradleWorkerMain.java:68)
	at worker.org.gradle.process.internal.worker.GradleWorkerMain.main(GradleWorkerMain.java:73)
Caused by: java.lang.NoSuchMethodError: com.google.common.collect.ImmutableList.builderWithExpectedSize(I)Lcom/google/common/collect/ImmutableList$Builder;
	at org.gradle.internal.instantiation.AbstractClassGenerator$AbstractInjectedPropertyHandler.getInjectedServices(AbstractClassGenerator.java:1123)
	at org.gradle.internal.instantiation.AbstractClassGenerator.generateUnderLock(AbstractClassGenerator.java:237)
	at org.gradle.internal.instantiation.AbstractClassGenerator.access$000(AbstractClassGenerator.java:93)
	at org.gradle.internal.instantiation.AbstractClassGenerator$1.transform(AbstractClassGenerator.java:111)
	at org.gradle.internal.instantiation.AbstractClassGenerator$1.transform(AbstractClassGenerator.java:108)
	at org.gradle.cache.internal.DefaultCrossBuildInMemoryCacheFactory$AbstractCrossBuildInMemoryCache.get(DefaultCrossBuildInMemoryCacheFactory.java:124)
	at org.gradle.internal.instantiation.AbstractClassGenerator.generate(AbstractClassGenerator.java:150)
	at org.gradle.internal.instantiation.AsmBackedClassGenerator.generate(AsmBackedClassGenerator.java:109)
	at org.gradle.internal.instantiation.Jsr330ConstructorSelector$1.transform(Jsr330ConstructorSelector.java:59)
	at org.gradle.internal.instantiation.Jsr330ConstructorSelector$1.transform(Jsr330ConstructorSelector.java:54)
	at org.gradle.cache.internal.DefaultCrossBuildInMemoryCacheFactory$AbstractCrossBuildInMemoryCache.get(DefaultCrossBuildInMemoryCacheFactory.java:124)
	at org.gradle.internal.instantiation.Jsr330ConstructorSelector.forType(Jsr330ConstructorSelector.java:54)
	at org.gradle.internal.instantiation.Jsr330ConstructorSelector.forParams(Jsr330ConstructorSelector.java:49)
	at org.gradle.internal.instantiation.DependencyInjectingInstantiator.newInstance(DependencyInjectingInstantiator.java:46)
	... 8 more


* Get more help at https://help.gradle.org

BUILD FAILED in 1s
2 actionable tasks: 1 executed, 1 up-to-date
```
