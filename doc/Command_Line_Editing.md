# 명령줄 편집

 옥타브는 명령줄 편집과 기록 형식의 확장성을 제공하는 라이브러리로 GNU Readline 라이브러리를 사용합니다. 본 매뉴얼에는 주로 사용되는 형식만 설명되어 있습니다. 편집 기능들은 사용자 편의에 맞게 다른 키로 변경될 수 있습니다. 본 매뉴얼에서는 기본 Emacs에 변경사항이 없는 것으로 간주합니다. Readlne을 변경하거나 더 많은 형식 리스트를 위해서는 GNU Readline 라이브러리 매뉴얼을 참고하십시요.

 글자(문자, 숫자, 심볼 등)를 입력하기 위해서는 그 글자를 치면됩니다. 옥타브는 커서의 위치에 글자를 입력하고 커서를 앞으로 이동시킵니다.

 명령줄 편집 기능 중 많은 것들은 컨트롤 키를 사용해서 작동됩니다. 예를 들어, `Control-a`는 줄의 맨 앞으로 커서를 이동시킵니다. `C-a`는 `CTRL`을 누른상태로 `a`를 누르는 것을 의미합니다. 이후부터는 `Control-a`를 `C-a`로 표시합니다.

 또다른 명령줄 편집 기능은 Meta키를 사용합니다. `M-u`는 `META`키를 누른 상태에서 `u`를 누르는 것을 의미합니다. 키보드에 따라서, `META`키는 `ALT`나 `WINDOWS`로 표시되어 있습니다. 터미널에 `META`키가 없다면, `ESC`로 시작하는 두키의 조합을 Meta키로 쓸 수 있습니다. 즉, `M-u`를 치려면 `ESC u`로 대체할 수 있습니다. *`ESC`*키 조합은 반대로 Meta키로서 터미널에서 사용될 수 있습니다. 이후부터는 `Meta-u`를 `M-u`로 표시합니다.


[Cursor Motion:](Cursor_Motion.md)
[Killing and Yanking:](Killing_and_Yanking.md)
[Commands for Text:](Commands_for_Text.md)
[Commands For Completion:](Commands_For_Completion.md)
[Commands For History:](Commands_for_History.md)
[Customizing readline:](Customizing_readline.md)
[Customizing the Prompt:](Customizing_the_Prompt.md)
[Diary and Echo Commands:](Diary_and_Echo_Commands.md)
