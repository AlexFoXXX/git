# git
1. Установите Jenkins

2. Создайте задачу, которая будет делать следующее:

Клонировать проект https://github.com/vitalliuss/helloci
Запускать тесты из проекта в директори Java с помощью цели mvn test
3. Настройте билд триггеры таким образом, чтобы задача выполнялась раз в 5 минут

Started by user Alex Fox
Running as SYSTEM
[EnvInject] - Loading node environment variables.
Building on master in workspace C:\Windows\system32\config\systemprofile\AppData\Local\Jenkins\.jenkins\workspace\Github job
The recommended git tool is: NONE
No credentials specified
 > C:\Program Files\Git\cmd\git.exe rev-parse --is-inside-work-tree # timeout=10
Fetching changes from the remote Git repository
 > C:\Program Files\Git\cmd\git.exe config remote.origin.url https://github.com/vitalliuss/helloci # timeout=10
Fetching upstream changes from https://github.com/vitalliuss/helloci
 > C:\Program Files\Git\cmd\git.exe --version # timeout=10
 > git --version # 'git version 2.29.2.windows.3'
 > C:\Program Files\Git\cmd\git.exe fetch --tags --force --progress -- https://github.com/vitalliuss/helloci +refs/heads/*:refs/remotes/origin/* # timeout=10
Seen branch in repository origin/I1234
Seen branch in repository origin/demobranch
Seen branch in repository origin/dependabot/maven/Java/junit-junit-4.13.1
Seen branch in repository origin/develop
Seen branch in repository origin/feature
Seen branch in repository origin/main
Seen branch in repository origin/master
Seen branch in repository origin/minskbranch
Seen branch in repository origin/trainingbranch
Seen 9 remote branches
 > C:\Program Files\Git\cmd\git.exe show-ref --tags -d # timeout=10
Multiple candidate revisions
Scheduling another build to catch up with Github job
Checking out Revision 904af05dec9a5818276ac39c6faf97fe5a5e13ba (origin/master)
 > C:\Program Files\Git\cmd\git.exe config core.sparsecheckout # timeout=10
 > C:\Program Files\Git\cmd\git.exe checkout -f 904af05dec9a5818276ac39c6faf97fe5a5e13ba # timeout=10
Commit message: "Merge pull request #15 from Molnix888/dotnet-update"
First time build. Skipping changelog.
[Github job] $ cmd.exe /C "C:\apache-maven-3.6.3\bin\mvn.cmd -f Java/pom.xml test && exit %%ERRORLEVEL%%"
[INFO] Scanning for projects...
[INFO] 
[INFO] ---------------< com.github.vitalliuss.helloci:hello-ci >---------------
[INFO] Building hello-ci 1.0-SNAPSHOT
[INFO] --------------------------------[ jar ]---------------------------------
[INFO] 
[INFO] --- maven-resources-plugin:2.6:resources (default-resources) @ hello-ci ---
[WARNING] Using platform encoding (Cp1251 actually) to copy filtered resources, i.e. build is platform dependent!
[INFO] skip non existing resourceDirectory C:\Windows\System32\config\systemprofile\AppData\Local\Jenkins\.jenkins\workspace\Github job\Java\src\main\resources
[INFO] 
[INFO] --- maven-compiler-plugin:3.1:compile (default-compile) @ hello-ci ---
[INFO] Changes detected - recompiling the module!
[WARNING] File encoding has not been set, using platform encoding Cp1251, i.e. build is platform dependent!
[INFO] Compiling 2 source files to C:\Windows\System32\config\systemprofile\AppData\Local\Jenkins\.jenkins\workspace\Github job\Java\target\classes
[INFO] 
[INFO] --- maven-resources-plugin:2.6:testResources (default-testResources) @ hello-ci ---
[WARNING] Using platform encoding (Cp1251 actually) to copy filtered resources, i.e. build is platform dependent!
[INFO] skip non existing resourceDirectory C:\Windows\System32\config\systemprofile\AppData\Local\Jenkins\.jenkins\workspace\Github job\Java\src\test\resources
[INFO] 
[INFO] --- maven-compiler-plugin:3.1:testCompile (default-testCompile) @ hello-ci ---
[INFO] Changes detected - recompiling the module!
[WARNING] File encoding has not been set, using platform encoding Cp1251, i.e. build is platform dependent!
[INFO] Compiling 1 source file to C:\Windows\System32\config\systemprofile\AppData\Local\Jenkins\.jenkins\workspace\Github job\Java\target\test-classes
[INFO] 
[INFO] --- maven-surefire-plugin:3.0.0-M1:test (default-test) @ hello-ci ---
[INFO] 
[INFO] -------------------------------------------------------
[INFO]  T E S T S
[INFO] -------------------------------------------------------
[INFO] Running com.github.vitalliuss.helloci.AppTest
[ERROR] Tests run: 5, Failures: 1, Errors: 0, Skipped: 1, Time elapsed: 0.503 s <<< FAILURE! - in com.github.vitalliuss.helloci.AppTest
[ERROR] testShouldBeFailed(com.github.vitalliuss.helloci.AppTest)  Time elapsed: 0.082 s  <<< FAILURE!
java.lang.AssertionError
	at com.github.vitalliuss.helloci.AppTest.testShouldBeFailed(AppTest.java:21)

[INFO] 
[INFO] Results:
[INFO] 
[ERROR] Failures: 
[ERROR]   AppTest.testShouldBeFailed:21
[INFO] 
[ERROR] Tests run: 5, Failures: 1, Errors: 0, Skipped: 1
[INFO] 
[INFO] ------------------------------------------------------------------------
[INFO] BUILD FAILURE
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  22.017 s
[INFO] Finished at: 2020-12-21T02:17:49+03:00
[INFO] ------------------------------------------------------------------------
[ERROR] Failed to execute goal org.apache.maven.plugins:maven-surefire-plugin:3.0.0-M1:test (default-test) on project hello-ci: There are test failures.
[ERROR] 
[ERROR] Please refer to C:\Windows\System32\config\systemprofile\AppData\Local\Jenkins\.jenkins\workspace\Github job\Java\target\surefire-reports for the individual test results.
[ERROR] Please refer to dump files (if any exist) [date].dump, [date]-jvmRun[N].dump and [date].dumpstream.
[ERROR] -> [Help 1]
[ERROR] 
[ERROR] To see the full stack trace of the errors, re-run Maven with the -e switch.
[ERROR] Re-run Maven using the -X switch to enable full debug logging.
[ERROR] 
[ERROR] For more information about the errors and possible solutions, please read the following articles:
[ERROR] [Help 1] http://cwiki.apache.org/confluence/display/MAVEN/MojoFailureException
Build step 'Вызвать цели Maven верхнего уровня  ' marked build as failure
Finished: FAILURE







Bring It On 
1. Установите Jenkins

2. Создайте задачу которая будет делать следующее:

Клонировать проект https://github.com/vitalliuss/helloci
Запускать тесты из проекта в директори Java с помощью цели mvn test
3. Настройте билд триггеры:

Запуск тестов не позднее чем через 5 минут после коммита в git
Каждый будний день в полночь
4. Опубликуйте файл “Java\target\surefire-reports\com.github.vitalliuss.helloci.AppTest.txt” как артефакт

Started by user Alex Fox
Running as SYSTEM
[EnvInject] - Loading node environment variables.
Building on master in workspace C:\Windows\system32\config\systemprofile\AppData\Local\Jenkins\.jenkins\workspace\Github job Bring it on
The recommended git tool is: NONE
No credentials specified
 > C:\Program Files\Git\cmd\git.exe rev-parse --is-inside-work-tree # timeout=10
Fetching changes from the remote Git repository
 > C:\Program Files\Git\cmd\git.exe config remote.origin.url https://github.com/vitalliuss/helloci # timeout=10
Fetching upstream changes from https://github.com/vitalliuss/helloci
 > C:\Program Files\Git\cmd\git.exe --version # timeout=10
 > git --version # 'git version 2.29.2.windows.3'
 > C:\Program Files\Git\cmd\git.exe fetch --tags --force --progress -- https://github.com/vitalliuss/helloci +refs/heads/*:refs/remotes/origin/* # timeout=10
Seen branch in repository origin/I1234
Seen branch in repository origin/demobranch
Seen branch in repository origin/dependabot/maven/Java/junit-junit-4.13.1
Seen branch in repository origin/develop
Seen branch in repository origin/feature
Seen branch in repository origin/master
Seen branch in repository origin/minskbranch
Seen branch in repository origin/trainingbranch
Seen 8 remote branches
 > C:\Program Files\Git\cmd\git.exe show-ref --tags -d # timeout=10
Checking out Revision 904af05dec9a5818276ac39c6faf97fe5a5e13ba (origin/master)
 > C:\Program Files\Git\cmd\git.exe config core.sparsecheckout # timeout=10
 > C:\Program Files\Git\cmd\git.exe checkout -f 904af05dec9a5818276ac39c6faf97fe5a5e13ba # timeout=10
Commit message: "Merge pull request #15 from Molnix888/dotnet-update"
 > C:\Program Files\Git\cmd\git.exe rev-list --no-walk 904af05dec9a5818276ac39c6faf97fe5a5e13ba # timeout=10
[Github job Bring it on] $ cmd.exe /C "C:\apache-maven-3.6.3\bin\mvn.cmd -f Java/pom.xml test && exit %%ERRORLEVEL%%"
[INFO] Scanning for projects...
[INFO] 
[INFO] ---------------< com.github.vitalliuss.helloci:hello-ci >---------------
[INFO] Building hello-ci 1.0-SNAPSHOT
[INFO] --------------------------------[ jar ]---------------------------------
[INFO] 
[INFO] --- maven-resources-plugin:2.6:resources (default-resources) @ hello-ci ---
[WARNING] Using platform encoding (Cp1251 actually) to copy filtered resources, i.e. build is platform dependent!
[INFO] skip non existing resourceDirectory C:\Windows\System32\config\systemprofile\AppData\Local\Jenkins\.jenkins\workspace\Github job Bring it on\Java\src\main\resources
[INFO] 
[INFO] --- maven-compiler-plugin:3.1:compile (default-compile) @ hello-ci ---
[INFO] Nothing to compile - all classes are up to date
[INFO] 
[INFO] --- maven-resources-plugin:2.6:testResources (default-testResources) @ hello-ci ---
[WARNING] Using platform encoding (Cp1251 actually) to copy filtered resources, i.e. build is platform dependent!
[INFO] skip non existing resourceDirectory C:\Windows\System32\config\systemprofile\AppData\Local\Jenkins\.jenkins\workspace\Github job Bring it on\Java\src\test\resources
[INFO] 
[INFO] --- maven-compiler-plugin:3.1:testCompile (default-testCompile) @ hello-ci ---
[INFO] Nothing to compile - all classes are up to date
[INFO] 
[INFO] --- maven-surefire-plugin:3.0.0-M1:test (default-test) @ hello-ci ---
[INFO] 
[INFO] -------------------------------------------------------
[INFO]  T E S T S
[INFO] -------------------------------------------------------
[INFO] Running com.github.vitalliuss.helloci.AppTest
[ERROR] Tests run: 5, Failures: 1, Errors: 0, Skipped: 1, Time elapsed: 0.397 s <<< FAILURE! - in com.github.vitalliuss.helloci.AppTest
[ERROR] testShouldBeFailed(com.github.vitalliuss.helloci.AppTest)  Time elapsed: 0.055 s  <<< FAILURE!
java.lang.AssertionError
	at com.github.vitalliuss.helloci.AppTest.testShouldBeFailed(AppTest.java:21)

[INFO] 
[INFO] Results:
[INFO] 
[ERROR] Failures: 
[ERROR]   AppTest.testShouldBeFailed:21
[INFO] 
[ERROR] Tests run: 5, Failures: 1, Errors: 0, Skipped: 1
[INFO] 
[INFO] ------------------------------------------------------------------------
[INFO] BUILD FAILURE
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  14.046 s
[INFO] Finished at: 2020-12-21T02:37:35+03:00
[INFO] ------------------------------------------------------------------------
[ERROR] Failed to execute goal org.apache.maven.plugins:maven-surefire-plugin:3.0.0-M1:test (default-test) on project hello-ci: There are test failures.
[ERROR] 
[ERROR] Please refer to C:\Windows\System32\config\systemprofile\AppData\Local\Jenkins\.jenkins\workspace\Github job Bring it on\Java\target\surefire-reports for the individual test results.
[ERROR] Please refer to dump files (if any exist) [date].dump, [date]-jvmRun[N].dump and [date].dumpstream.
[ERROR] -> [Help 1]
[ERROR] 
[ERROR] To see the full stack trace of the errors, re-run Maven with the -e switch.
[ERROR] Re-run Maven using the -X switch to enable full debug logging.
[ERROR] 
[ERROR] For more information about the errors and possible solutions, please read the following articles:
[ERROR] [Help 1] http://cwiki.apache.org/confluence/display/MAVEN/MojoFailureException
Build step 'Вызвать цели Maven верхнего уровня  ' marked build as failure
Archiving artifacts
Finished: FAILURE
