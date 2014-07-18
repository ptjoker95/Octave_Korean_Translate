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