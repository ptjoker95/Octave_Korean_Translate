# Diary and Echo Commands

옥타브의 다이어리 기능으로 별도의 파일에 사용자가 입력한 내용과 결과 모두 혹은 일부를  기록할 수 있습니다.

**Command: diary**

**Command: diary *on***

**Command: diary *off***

**Command: diary *filename***

모든 명령어와 그에 따른 결과를 터미널에 나타나는 그대로 기록합니다.

**on**

 현재 작업중인 디렉토리에 `diary`라는 파일을 만들고 세션을 기록합니다.

 **off**

 다이어리 파일에 세션을 기록하는 것을 중지합니다.

 ***filename***

 *filename* 파일에 세션을 기록합니다.

 인수가 없으면 `diary`가 현재 다이어리 상태를 유지합니다.

 **참조: ** [history]()


때로는 함수가 실행되는 도중에 함수에 있는 명령어들을 보는 것이 유용할 때가 있습니다. 특히 디버깅할 때에 매우 유용합니다.

**Command: echo *options***

실행되는 동안에 명령어들을 볼지 말지를 결정합니다. 옵션으로는

**on**

 스크립트 파일에서 실행되는 동안 명령어들을 볼 수 있게 합니다.

**off**

 스크립트 파일에서 실행되는 동안 명령어들을 볼 수 없게 합니다.

**on all**

 스크립트 파일과 함수가 실행되는 동안 명령어들을 볼 수 있게 합니다.

**off all**

 스크립트 파일과 함수가 실행되는 동안 명령어들을 볼 수 있게 합니다.

인수없이 실행되면, `echo`는 현재 상태를 유지합니다.

**Built-in Function: *val* = echo_executing_commands *()***

**Built-in Function: *old_val* = echo_executing_commands *(new_val)***

**Built-in Function: echo_executing_commands *(new_val, "local")***

에코 상태를 정하는 내부 변수를 보여주거나 설정합니다. 그 값은 다음의 합일 수도 있습니다.

**1**

 스크립트 파일에서 읽어오는 명령어들을 보여줍니다.

**2**

 함수의 명령어들을 보여줍니다.

**4**

 명령어 줄의 명령어를 보여줍니다.


한가지 이상의 상태가 동시에 활성화될 수도 있습니다. 예를 들어, 3은 `--echo-commands`와 같습니다.

`echo_executing_commands`의 값은 `echo`명령어나 명령어 옵션 `--echo-commands`로 설정될 수 있습니다.

`"local"`옵션으로 함수 내부에서 호출되면, 그 함수나 호출된 서브루틴에 한해 값이 변합니다. 함수가 종료되면 원래 값으로 되돌아옵니다.
