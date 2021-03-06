# 히스토리를 유용하게 사용할 수 있는 명령어들

옥타브는 이전의 명령어를 다시 불러와서 수정하거나 다시 실행할 수 있도록 입력한 명령어들을 저장해놓습니다. 옥타브를 종료하더라도 `history_size` 환경 변수에 정해진 숫자만큼 파일에 저장을 합니다. 옥타브가 실행되면, `history_file` 변수에 정해져있는 파일로부터 명령어 리스트를 읽어옵니다.

다음은 히스토리 리스트를 보거나 찾는데 사용되는 명령어입니다.

**LFD**
**RET**

커서가 어디있던 지 상관없이 현재 줄을 입력합니다. 만일 줄이 비어있지 않으면, 히스토리 리스트에 저장합니다. 만일 그 줄이 히스토리에 있으면, 원래 상태로 히스토리에 재저장합니다.

**C-p**

 히스토리 리스트 '위'로 올라갑니다.

**C-n**

 히스토리 리스트 '아래'로 내려갑니다.

**M-<**

 히스토리의 첫번째 줄로 갑니다.

**M->**

 히스토리 기록의 마지막 으로 갑니다. 즉, 현재 입력하고 있는 줄입니다.

**C-r**

 현재 줄을 시작으로 아래에서부터 히스토리에 있는 내용을 검색합니다. 중복 검색을 합니다.

**C-s**

 현재 줄을 시작으로 위에서부터 히스토리에 있는 내용을 검색합니다.

대부분의 터미널에서, 히스토리 리스트를 옮길 때 `C-p`와 `C-n`대신에 화살키의 위아래도 사용할 수 있습니다.

옥타브는 히스토리 리스트에 있는 명령어를 보고, 수정하고 다시 실행할 수 있는 명령어도 제공합니다.

**Command: history**
**Command: history *opt1 ...***
**Built-in Function: *h = * history *()***
**Built-in Function: *h = * history *(opt1, ...)***

아무 옵션없이 `history` 명령어를 실행하면 실행한 명령어의 리스트를 보여줍니다. 가능한 옵션은 다음과 같습니다.

**n**
**-n**

 히스토리에서 가장 최근의 n 라인만 보여줍니다.

**-c**

 히스토리 리스트를 지웁니다.

**-q**

 히스토리 리스트의 앞의 숫자를 보여주지 않습니다. X 윈도우 시스템에서 복사할 때 유용합니다.

**-f *file***

 *file*을 읽고 그 내용을 현재의 히스토리 리스트에 더합니다. 만일 이름이 생략되면, 기본 히스토리 파일(일반적으로 `~/.octave_hist`)을 읽어옵니다.

**-w *file***

 현재의 히스토리를 *file*에 저장합니다. 만일 이름이 생략되면, 기본 히스토리 파일(일반적으로 `~/.octave_hist`)에 저장합니다.


예를 들어, 최근의 히스토리 중에서 5라인을 번호없이 보고 싶으면, `history -q 5`를 하면 됩니다.

단일 출력 인수로 실행되면, 히스토리는 인수를 셀 문자열로 기록하고 화면에 출력하지 않습니다.

**Command: edit_history**

**Command: edit_history *com_number***

**Command: edit_history *first last***

`EDITOR`변수에 지정되어 있는 편집기로 히스토리 리스트를 편집합니다.

편집할 명령어는 임시 파일에 우선 복사됩니다. 에디터를 종료하게 되면, 옥타브는 파일에 있는 명령어들을 실행합니다. 때로는 명령줄에 명령어들을 다시 입력하는 것보다 `edit_history`를 이용하는 게 더 편리할 수 있습니다. 명령어들을 다시 실행하지 않기 위해서는 에디터를 종료시키기 전에 모든 줄을 지우면 됩니다.

 아무 지정어 없이 실행되었을 때, 이전에 실행된 명령어를 편집합니다. 지정어가 하나일 경우 *cmd_number*로 지정된 명령어를 편집합니다. 지정어가 2개이면, *first*와 *last* 사이에 있는 명령어 리스트를 편집합니다. 명령어 번호 식별자는 음수도 가능하며, -1은 가장 최근에 호출된 명령어입니다. 다음의 명령어는 가장 최근에 실행된 명령어를 편집하는 같은 기능을 합니다.

 `edit_history`
 `edit_history -1`

범위를 지정할 때, 앞의 숫자를 뒤의 숫자보다 크게 하면, 편집하기 위해 버퍼에 넣을 때 명령어 리스트를 거꾸로 넣습니다.

**참조:** [run_history]()

**Command: run_history**

**Command: run_history *cmd_number***

**Command: run_history *first last***

히스토리 리스트에 있는 명령어들을 실행합니다.

매개 변수 없이 실행되면, 이전에 실행된 명령어를 실행합니다. 매개 변수가 하나면 *cmd_number*의 명령어를 실행합니다. 매개 변수가 두개면 *first*와 *last* 사이의 명령어 리스트를 실행합니다. 매개 변수가 01이면 가장 최근에 실행된 명령어를 실행합니다. 예를 들어

```
run_history
    OR
run_history -1
```
가장 최근의 명령어를 다시 실행합니다. 명령어
```
run_history 13 169
```
는 13번부터 169번까지의 명령어를 실행합니다.

앞의 숫자가 마지막 숫자보다 클 경우에는 실행될 명령어를 역순으로 실행합니다. 즉,
```
disp (1)
disp (2)
run_history -1 -2
⇒
2
1
```

**참조:** [edit_history]()

옥타브는 히스토리를 언제, 어디에 어떻게 저장할 지도 지정할 수 있씁니다.

**Built-in Function: *val* = history_save*()**

**Built-in Function: *old_val* = history_save *(new_val)***

**Built-in Function: history_save *(new_val, "local")***

명령줄에 입력된 명령어를 히스토리 파일에 저장할지 말지를 정하는 내부 변수를 보여주거나, 설정합니다.

`"local"` 옵션으로 함수 내부에서 호출되면, 변수값은 함수와 그 서브루틴에 한해서 변합니다. 함수가 종료되면 원래값으로 되돌아 옵니다.

**참조:** [history_control](), [history_file](), [history_size](), [history_timestamp_format_string]()

**Builit-in Function: *val* = history_control *()***

**Built-in Function: *old_val* = history_control *(new_val)***

명령어들을 어떻게 히스토리 리스트에 저장할 지를 결정하는 내부 변수를 보여주거나 설정합니다. 기본 값은 비어있는 문서열이지만, 환경변수 `OCTAVE_HISTCONTROL`에 겹쳐질 수 있습니다.

`history_control`은 히스토리 리스트에 명령어를 어떻게 저장할 지를 지정하는 값들을 콜론으로 분리한 리스트입니다. 만일 리스트에 `ignorespace`가 있으면, 히스토리 리스트에 빈칸으로 시작하는 명령문은 저장하지 않습니다. `ignoredups`는 히스토리에 같은 명령문이 있으면 저장하지 않습니다. `ignoreboth`는 `ignorespace`와 `ignoredups`를 모두 실행합니다. `erasedups`는 현재의 명령문과 같은 것이 히스토리에 있으면, 히스토리에 있는 명령문들을 모두 지운 후 현재의 명령문을 저장합니다. 위의 값들이 아닌 값은 무시합니다. `history_control`이 빈 문자열이면, 모든 명령어들은 `history_save`의 값이 붙어서 히스토리 리스트에 저장됩니다.

**참조:** [history_file](), [history_size](), [history_timestamp_format_string](), [history_save]().

**Built-in Function: *val* = history_file *()***

**Built-in Function: *old_val* = history_file *(new_val)***

명령어 히스토리를 저장하는 파일의 이름을 지정하는 내부 변수를 보여주거나 설정합니다. 기본값은 `~/.octave_hist`이지만, 환경변수 `OCTAVE_HISTFILE`에 겹쳐질 수 있습니다.

**참조: ** [history_size](), [history_save](), [history_timestamp_format_string]()

**Built-in Function: *val* = history_size *()***

**Built-in Function: *old_val* = history_size *(new_val)***

히스토리 파일에 저장할 갯수를 정하는 내부 변수를 보여주거나 설정합니다. 기본값은 `1000`이자만, 환경변수 `OCTAVE_HISTSIZE`로 겹쳐질 수 있습니다.

**참조: ** [history_file](), [history_timestamp_format_string](), [history_save]()

**Built-in Function: *val* = history_timestamp_format_string *()***

**Built-in Function: *old_val* = history_timestamp_format_string *(new_val)***

**Built-in Function: history_timestamp_format_string *(new_val, "local")***

옥타브가 종료될 때 히스토리 파일에 쓰여질 주석의 형식을 지정하는 내부 변수를 보여주거나 설정합니다. 형식 문자열은 `strftime`에 넘겨집니다. 기본값은
```
    "# Octave VERSION, %a %b %d %H:%M:%S %Y %Z <USER@HOST>"
```
입니다.

`"local"` 옵션을 가진 함수 내부에서 호출되었을 경우, 그 함수와 그 함수에 의해 호출된 서브루틴에 국한되어 값이 변합니다. 그 함수가 종료되면 원래 값으로 되돌아갑니다.

**참조: ** [strftime](), [history_file](), [history_size](), [history_save]()

**Built-in Function: *val* = EDITOR *()***

**Built-in Function: *old_val* = EDITOR *(new_val)***

**Built-in Function: EDITOR *(new_val, "local")***

기본 문서편집기를 정하는 내부 변수를 보거나 지정합니다.

기본값은 옥타브가 시작될 때 환경변수 `EDITOR`에 의해 정해집니다. 만일 환경변수가 초기화되지 않으면, `EDITOR`는 `"emacs"`로 정해집니다.

`"local"`옵션으로 함수 내부에서 호출되면, 그 함수와 그 함수에 의해 호출된 서브루틴에 국한되어 값이 변합니다. 그 함수가 종료되면 원래 값으로 되돌아갑니다.

**참조: ** [edit](), [edit_history]()
