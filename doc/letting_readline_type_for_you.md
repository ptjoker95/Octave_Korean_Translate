#사용자의 입력을 용이하게 하기 위한 명령어들

다음의 명령어들은 사용자가 입력하는 명령어나 변수명들을 완성하는 데 도움이 됩니다.

**TAB**

 커서 앞에 있는 문자를 완성하도록 합니다. 옥타브는 명령어나 변수명을 완성시킬 수 있습니다.

**M-?**

 커서 앞에 있는 문자열이 가능한 리스트를 보여줍니다.


**Built-in Function: val = completion_append_char *()***

**Built-in Function: *old_val* = completion_append_char *(new_val)***

**Built-in Function: completion_append_char *(new_val, "local")***

완성된 명령줄에 붙는 내부 문자변수를 불러오거나 지정합니다.

`"local"` 옵션으로 함수 내부에서 호출되면, 반수는 함수와 그 서브루틴에 한정되어 변합니다. 함수가 종료되면 원래 값으로 돌아옵니다.

**Built-in Function: completion_matches *(hint)***

*hint*에 해당되는 것들을 보여줍니다.

이 함수는 옥타브를 컨트롤하거나 사용자 입력을 조작할 때 Emacs와 같은 프로그램에 도움을 줍니다. 함수가 호출되어도 현재 명령어 번호는 증가하지 않습니다. 즉, 버그가 아닙니다.
