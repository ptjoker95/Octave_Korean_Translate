#커서 움직이기

다음의 명령어로 커서를 움직일 수 있습니다.

**C-b**

한칸 뒤로 움직입니다.

**C-f**

한칸 앞으로 움직입니다.

**BACKSPACE**

커서 왼쪽의 문자를 지웁니다.

**DEL**

커서가 있는 곳의 문자를 지웁니다.

**C-d**

커서가 있는 곳의 문자를 지웁니다.

**M-f**

한 단어 앞으로 움직입니다.

**M-b**

한 단어 뒤로 움직입니다.

**C-a**

줄의 맨 앞으로 움직입니다.

**C-e**

줄의 맨 뒤로 움직입니다.

**C-l**

화면을 지우고, 현재의 줄을 맨 위에 다시 씁니다.

**C-_**

**C-/**

마지막 동작을 취소합니다. 줄이 빌 때까지 취소할 수 있습니다.

**M-r**

현재 줄의 모든 변동을 취소합니다. 'undo'명령어와 같습니다.

위의 명령어들은 입력줄을 편집하기 위해 필요한 기본적인 키입력입니다. 대부분의 터미널에서, 커서를 왼쪽이나 오른쪽으로 움직이기 위해 `C-f`나 `C-b`대신 왼쪽 오른쪽 화살표를 쓸 수도 있습니다.

`C-f`가 한 문자 단위로 움직이는 반면에 `M-f`는 한 단어 단위로 움직이는 데 주목하시기 바랍니다. meta키는 단어단위로, control키는 문자 단위로 작동하기에 편리합니다.

`clc`함수는 옥타브 프로그램에서 화면을 지우는 데 사용될 수 있습니다.

**Built-in Function: clc *()***

**Built-in Function: home *()***