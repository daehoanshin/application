Java 최신 버젼으로 프로그래밍 할거 아니면....

2018.3.6을 추천드림.....여기로...

매번 업데이트 하는것도 귀찬을 겁니다.







How to crack Jetbrains Intellij IDEA 2019.3.1






jetbrains products 아래 버젼 모두 같은 방법으로 가능합니다.

Jetbrains 2019.3.1 이하 전 제품 크랙가능.


Intellij IDEA 2019.3.1 ultimate과 webstorm 2019.3.1 버젼의 크랙 방법을 설명합니다.





- 이전버젼이 설치되어 있으면, 완전히 삭제하고, trial 버전으로 다운 받아서 설치하시기 바래요.

(완젼삭제 방법은 여기를 참조....)



아래는 Intellij IDEA 중심으로 설명하나, webstorm 도 같은 방법입니다.

윈도우, 맥 모두 같은 방법입니다.





0. Intellij idea 2019.3.1 를 다운로드 받아서, 일단 trial 버전으로 실행하세요.

이전버젼 여기로.

    그리고 첨부파일을 다운로드 받으세요. 압축을 풀면 두개 파일이 있을 겁니다.

   (ACTIVATION_CODE.txt, jetbrains-agent 2019.3.1.jar)




1. 설치된 Intellij idea 실행 후, Intellij idea의 상단메뉴.....Help ->Edit Custom vm options... 를 실행하세요. (대화상자가 나오면 Create를 선택합니다.)

    실행하면 아래파일이 열립니다.

    마자막 라인에 javaagent:jebrains-agent 2019.3.1.jar 를 타이핑합니다.





# custom IntelliJ IDEA VM options

-Xms128m
-Xmx750m
-XX:ReservedCodeCacheSize=240m
-XX:+UseCompressedOops
-Dfile.encoding=UTF-8
-XX:+UseConcMarkSweepGC
-XX:SoftRefLRUPolicyMSPerMB=50
-ea
-Dsun.io.useCanonCaches=false
-Djava.net.preferIPv4Stack=true
-Djdk.http.auth.tunneling.disabledSchemes=""
-XX:+HeapDumpOnOutOfMemoryError
-XX:-OmitStackTraceInFastThrow
-Xverify:none

-XX:ErrorFile=$USER_HOME/java_error_in_idea_%p.log
-XX:HeapDumpPath=$USER_HOME/java_error_in_idea.hprof

-javaagent:jetbrains-agent2019.3.1.jar  <--이부분 추가. 마지막 라인에 넣으면 됩니다.(첨부 파일이름과 같아야 함.윈도우환경은 절대경로.)

저장하시고 문서를 닫으세요.



( 참고로 ..저장되는 파일의 경로는....

-64bit

C:\Program Files\JetBrains\IntelliJ IDEA 2019.3.1\bin\idea64.exe.vmoptions

-32bit

C:\Program Files\JetBrains\IntelliJ IDEA 2019.3.1\bin\idea.exe.vmoptions )


※맥의 경로는 application 폴더에서 IntelliJ idea.app를 마우스 오른쪽 클릭해서

  패키지 내용보기 -> contents -> bin -> idea.vmoptions으로 찾아 가시면됩니다.







2. 첨부된 jetbrains-agent2019.3.1.jar 을 복사해 넣으세요.

설치된 경로  C:\Program Files\JetBrains\IntelliJ IDEA 2019.3.1\bin\

 (맥은 IntelliJ idea.app 아이콘... 오른쪽클릭 ..패키지 내용보기 -> contents -> bin 에.. 복사)




3. Intellij idea를 닫고, 다시 실행합니다.

첨부된   ACTIVATION_CODE.txt 파일을 열고, 내용을 복사하세요

Intellij idea의 상단메뉴.....Help -> Register... -> Activation code 에 붙여 넣고, ok 버튼 클릭 해주시면 끝입니다.



사서 씁니다. 헝그리 코더들이면.. 어쩔수 없지만....



순서가 잘못되면, 좀 이상해져요.

요약하자면...

1.trial로 실행..한번하고 닫기.
2.다시 실행후 설정파일 수정, 설정파일 닫기, bin폴더에 crack jar 붙여넣기
3.프로그램 닫기.
4.다시 실행 후 activation code 붙여넣기. 끝.
순서를 잘 지켜서 해보세요.



Good luck!!!
