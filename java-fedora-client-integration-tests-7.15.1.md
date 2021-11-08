[INFO] -------------------------------------------------------------
[ERROR] COMPILATION ERROR : 
[INFO] -------------------------------------------------------------
[ERROR] /Users/usingh/Desktop/OA-PASS/java-fedora-client/pass-data-client/src/main/java/org/dataconservancy/pass/client/elasticsearch/ElasticsearchPassClient.java:[271,51] method search in class org.elasticsearch.client.RestHighLevelClient cannot be applied to given types;
  required: org.elasticsearch.action.search.SearchRequest,org.elasticsearch.client.RequestOptions
  found: org.elasticsearch.action.search.SearchRequest
  reason: actual and formal argument lists differ in length
[INFO] 1 error
[INFO] -------------------------------------------------------------
[INFO] ------------------------------------------------------------------------
[INFO] Reactor Summary:
[INFO] 
[INFO] PASS Client Tool ................................... SUCCESS [  1.305 s]
[INFO] PASS Test Data ..................................... SUCCESS [  2.789 s]
[INFO] PASS Core Data Model ............................... SUCCESS [  4.582 s]
[INFO] pass-client-api .................................... SUCCESS [  1.419 s]
[INFO] pass-client-util ................................... SUCCESS [  1.714 s]
[INFO] pass-json-adapter .................................. SUCCESS [  2.150 s]
[INFO] PASS Data Client ................................... FAILURE [  0.659 s]
[INFO] PASS Status Utility ................................ SKIPPED
[INFO] pass-client-shaded-v2_3 ............................ SKIPPED
[INFO] pass-client-integration ............................ SKIPPED
[INFO] ------------------------------------------------------------------------
[INFO] BUILD FAILURE
[INFO] ------------------------------------------------------------------------
[INFO] Total time: 14.788 s
[INFO] Finished at: 2021-11-08T09:53:00-05:00
[INFO] Final Memory: 41M/530M
[INFO] ------------------------------------------------------------------------
[ERROR] Failed to execute goal org.apache.maven.plugins:maven-compiler-plugin:3.8.1:compile (default-compile) on project pass-data-client: Compilation failure
[ERROR] /Users/usingh/Desktop/OA-PASS/java-fedora-client/pass-data-client/src/main/java/org/dataconservancy/pass/client/elasticsearch/ElasticsearchPassClient.java:[271,51] method search in class org.elasticsearch.client.RestHighLevelClient cannot be applied to given types;
[ERROR] required: org.elasticsearch.action.search.SearchRequest,org.elasticsearch.client.RequestOptions
[ERROR] found: org.elasticsearch.action.search.SearchRequest
[ERROR] reason: actual and formal argument lists differ in length
[ERROR] -> [Help 1]
org.apache.maven.lifecycle.LifecycleExecutionException: Failed to execute goal org.apache.maven.plugins:maven-compiler-plugin:3.8.1:compile (default-compile) on project pass-data-client: Compilation failure
/Users/usingh/Desktop/OA-PASS/java-fedora-client/pass-data-client/src/main/java/org/dataconservancy/pass/client/elasticsearch/ElasticsearchPassClient.java:[271,51] method search in class org.elasticsearch.client.RestHighLevelClient cannot be applied to given types;
  required: org.elasticsearch.action.search.SearchRequest,org.elasticsearch.client.RequestOptions
  found: org.elasticsearch.action.search.SearchRequest
  reason: actual and formal argument lists differ in length

	at org.apache.maven.lifecycle.internal.MojoExecutor.execute(MojoExecutor.java:212)
	at org.apache.maven.lifecycle.internal.MojoExecutor.execute(MojoExecutor.java:153)
	at org.apache.maven.lifecycle.internal.MojoExecutor.execute(MojoExecutor.java:145)
	at org.apache.maven.lifecycle.internal.LifecycleModuleBuilder.buildProject(LifecycleModuleBuilder.java:116)
	at org.apache.maven.lifecycle.internal.LifecycleModuleBuilder.buildProject(LifecycleModuleBuilder.java:80)
	at org.apache.maven.lifecycle.internal.builder.singlethreaded.SingleThreadedBuilder.build(SingleThreadedBuilder.java:51)
	at org.apache.maven.lifecycle.internal.LifecycleStarter.execute(LifecycleStarter.java:128)
	at org.apache.maven.DefaultMaven.doExecute(DefaultMaven.java:307)
	at org.apache.maven.DefaultMaven.doExecute(DefaultMaven.java:193)
	at org.apache.maven.DefaultMaven.execute(DefaultMaven.java:106)
	at org.apache.maven.cli.MavenCli.execute(MavenCli.java:863)
	at org.apache.maven.cli.MavenCli.doMain(MavenCli.java:288)
	at org.apache.maven.cli.MavenCli.main(MavenCli.java:199)
	at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
	at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62)
	at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
	at java.lang.reflect.Method.invoke(Method.java:497)
	at org.codehaus.plexus.classworlds.launcher.Launcher.launchEnhanced(Launcher.java:289)
	at org.codehaus.plexus.classworlds.launcher.Launcher.launch(Launcher.java:229)
	at org.codehaus.plexus.classworlds.launcher.Launcher.mainWithExitCode(Launcher.java:415)
	at org.codehaus.plexus.classworlds.launcher.Launcher.main(Launcher.java:356)
Caused by: org.apache.maven.plugin.compiler.CompilationFailureException: Compilation failure
/Users/usingh/Desktop/OA-PASS/java-fedora-client/pass-data-client/src/main/java/org/dataconservancy/pass/client/elasticsearch/ElasticsearchPassClient.java:[271,51] method search in class org.elasticsearch.client.RestHighLevelClient cannot be applied to given types;
  required: org.elasticsearch.action.search.SearchRequest,org.elasticsearch.client.RequestOptions
  found: org.elasticsearch.action.search.SearchRequest
  reason: actual and formal argument lists differ in length

	at org.apache.maven.plugin.compiler.AbstractCompilerMojo.execute(AbstractCompilerMojo.java:1220)
	at org.apache.maven.plugin.compiler.CompilerMojo.execute(CompilerMojo.java:187)
	at org.apache.maven.plugin.DefaultBuildPluginManager.executeMojo(DefaultBuildPluginManager.java:134)
	at org.apache.maven.lifecycle.internal.MojoExecutor.execute(MojoExecutor.java:207)
	... 20 more
[ERROR] 
[ERROR] Re-run Maven using the -X switch to enable full debug logging.
[ERROR] 
[ERROR] For more information about the errors and possible solutions, please read the following articles:
[ERROR] [Help 1] http://cwiki.apache.org/confluence/display/MAVEN/MojoFailureException
[ERROR] 
[ERROR] After correcting the problems, you can resume the build with the command
[ERROR]   mvn <goals> -rf :pass-data-client
