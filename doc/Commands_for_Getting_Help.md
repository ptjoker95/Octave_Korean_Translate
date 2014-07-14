#Commands for Getting Help

 이 매뉴얼에 있는 모든 텍스트는 *`doc`* 명령어를 통해 옥타브의 프롬프트에서 볼 수 있습니다. 더불어, 개인 사용자가 만든 함수와 변수에 관한 문서도 *`help`*명령어를 통해서 사용가능합니다. 이 섹션에서는 매뉴얼과 사용자가 만든 함수와 변수들을 위한 문서를 읽는데 사용되는 명령어에 대해 설명합니다. 직접 제작한 함수에 관한 문서를 어떻게 만드는 지에 대해서는 [Function Files](Function\ Files.md)을 참고하십시요.


 #####Command: help *name*

 **Command: help *`--list`***

 **Command: help .**

  *name*에 관한 도움말을 보여줍니다. 예를 들어, *`help help`* 명령문은 `help`명령어에 관한 짧은 메세지를 표시합니다.

  `--list` 옵션은, 현재 옥타브에서 사용할 수 있는 연산자, 키워드, 기본 함수들, 읽어올 수 있는 함수들의 리스트를 보여줍니다.

  `.` 옵션은, 현재 옥타브에서 사용할 수 있는 연산자들의 리스트를 보여줍니다.

  아무 내용없이 `help`를 사용하면, 명령문에서 어떻게 help를 사용하는 지 알려줍니다.

  help 명령어는 연산자들에 대한 정보를 알려주지만, 명령어 구분자로 사용되는 콤마나 세미콜론 등에 관한 정보는 주지 않습니다. 이런 정보를 알기 위해서는, `help comma`나 `help semicolon`을 사용해야 합니다.

  **참조:** [doc](Getting\ Help.md), [lookfor](Getting\ Help.md), [which]()


#####Command: doc *function_name*

  *function_name*에 관한 문서를 GNU Info 브라우저를 이용해 온라인 버전 매뉴얼을 그대로 보여줍니다. 아무 내용없이 실행하면, 매뉴얼의 처음을 보여줍니다.

  예를 들어, `doc rand` 명령문은 `rand`에 관한 온라인 버전의 매뉴얼을 GNU Info 브라우저를 실행합니다.

  GNU Info 브라우저를 실행하면, `C-h`명령어로 도움말을 사용할 수 있습니다.

  **참조:** []


**Command: lookfor *str***

**Command: lookfor *-all str***

**Function File: *[func, helpstring]* = lookfor *(str)**

**Function File: *[func, helpstring]* = lookfor *("-all", str)***

 현재의 함수 찾기 경로에 있는 모든 함수에서 **str** 문자열을 검색합니다. 기본적으로, `lookfor`는 각각의 함수에서 찾을 수 있는 도움말의 처음 문장에서 *str*을 검색합니다. `"-all"` 옵션은 각 함수의 도움말 전체에서 검색하도록 합니다. 모든 검색어는 대소문자를 가리지 않습니다.

 옵션없이 사용되면, `lookfor`는 터미널에 비슷한 함수의 리스트를 보여줍니다. 반면, **func**와 **helpstring** 옵션은 비슷한 함수를 찾고, 그 함수의 도움말의 첫번째 문장을 보여줍니다.

 `lookfor`를 이용해 도움말의 첫번째 문장을 정확하게 찾는건 그 함수의 도움말의 형식에 좌우됩니다. 모든 옥타브의 핵심적인 함수들은 정확한 형식을 따르고 있지만, 외부 패키지나 다른 사용자가 제공하는 함수에 대해서도 같은지는 보장할 수 없습니다. 따라서, 옥타브에서 제공하지 않는 함수에 대해서는 `"-all"` 옵션을 사용하는 것이 필요할 수 있습니다.

 **참조:** [help](), [doc](), [which]()



 옥타브의 현재 버전에 대해서 새로운 정보는, `news` 함수를 이용하면 됩니다.

 **Command: news**

 **Command: news *package***

  옥타브느 설치된 패키지의 현재 NEWS 파일을 보여줍니다.

  옵션없이 호출되면, 옥타브에 관한 NEWS 파일을 보여줍니다. *package*의 이름이 주어지면, 그 패키지에 관한 현재의 NEWS 파일을 보여줍니다.

 **Function File: info *()***

  GNU Octave 커뮤니티에 관한 정보를 보여줍니다.

 **Built-in Function: warranty *()***

  옥타브에 관한 저작권과 배포 조건을 보여줍니다.



 다음의 함수는 문서를 보여줄 때 사용되는 프로그램이나 찾은 문서를 바꿀 때 사용될 수 있습니다.

 **Built-in Function: *val* = info_file *()***

 **Built-in Function: *old_val* = info_file *(new_val)***

 **Built-in Function: info_file *(new_val, "local")***

  옥타브 info파일의 이름을 지정하는 내부 변수를 찾거나 지정합니다. 기본값은 `octave-home/info/octave.info`이고, *octave-home*은 옥타브가 설치된 루트 디렉토리를 의미합니다. 기본값은 환경변수 `OCTAVE_INFO_FILE`이나 명령문 옵션 `'--info-file FNAME'`으로 변경될 수 있습니다.

  `"local"`옵션으로 호출되게 되면, 변수는 불려진 함수와 서브루틴에 국한되게 됩니다. 함수가 종료되면 원래 값으로 되돌아오게 됩니다.

  **참조:** [info_program](), [doc](), [help](), [makeinfo_program]()


 **Built-in Function: *val* = info_program *()***

 **Built-in Function: *old_val* = info_program *(new_val)***

 **Built-in Function: info_program *(new_val, "local")***

  실행되고 있는 info 프로그램의 이름을 지정하는 내부 변수를 찾거나 지정합니다. 기본값은 `octave-home/libexec/octave/version/exec/arch/info`이고, *octave-home*은 옥타브가 설치된 루트 디렉토리를, *version*은 옥타브 버전, *arch*는 시스템 타입 (예를 들어, `i686-pc-linux-gnu`) 을 의미합니다. 기본값은 환경 변수 `OCTAVE_INFO_PROGRAM`이나 명령문 옵션 `'--info-program NAME'`으로 변경될 수 있습니다.

  `"local"`옵션으로 호출되게 되면, 변수는 불려진 함수와 서브루틴에 국한되게 됩니다. 함수가 종료되면 원래 값으로 되돌아오게 됩니다.

  **참조:** [info_file](), [doc](), [help](), [makeinfo_program]()

 
 **Built-in Function: *val* = makeinfo_program *()***

 **Built-in Function: *old_val* = makeinfo_program *(new_val)***

 **Built-in Function: makeinfo_program *(new_val, "local")***

  Texinfo 마크업 명령어를 포함하는 도움말을 만드는 옥타브의 프로그램의 이름을 지정하는 내부 변수를 찾거나 지정합니다. 기본값은 `makeinfo`입니다.

 `"local"`옵션으로 호출되게 되면, 변수는 불려진 함수와 서브루틴에 국한되게 됩니다. 함수가 종료되면 원래 값으로 되돌아오게 됩니다.

  **참조:** [taxi_macros_file](), [info_file](), [info_program](), [doc](), [help]()


 **Built-in Function: *val* = texi_macros_file *()***

 **Built-in Function: *old_val* = texi_macros_file *(new_val)***

 **Built-in Function: texi_macros_file *(new_val, "local")***

  makeinfo로 넘겨지기 전에 문서열 앞에 넣어지는 Texinfo 매크로을 가지고 있는 파일의 이름을 지정한 내부 변수를 찾거나 지정합니다. 기본값은 `octave-home/share/octave/version/etc/macros.texi`이고, *octave-home*은 옥타브가 설치된 루트 디렉토리를, *version*은 옥타브 버전을 의미합니다. 기본값은 환경변수 `OCTAVE_TEXI_MACROS_FILE`이나 명령문 옵션 `'--texi-macros-file FNAME'`으로 변경될 수 있습니다.

  `"local"`옵션으로 호출되게 되면, 변수는 불려진 함수와 서브루틴에 국한되게 됩니다. 함수가 종료되면 원래 값으로 되돌아오게 됩니다.

   **참조:** [makeinfo_program]()

 
 **Built-in Function: *val* = doc_cache_fiile*()***

 **Built-in Function: *old_val* = doc_cache_file*(new_val)***

 **Built-in Function: doc_cache_file *(new_val, "local")***

   옥타브 문서 캐쉬 파일의 이름을 지정한 내부 변수를 찾거나 지정합니다. 캐쉬파일은 `lookfor` 명령어의 실행을 눈에 띄게 향상시킵니다. 기본값은 `octave-home/share/octave/version/etc/doc-cache`이고, *octave-home*은 옥타브가 설치된 루트 디렉토리를, *version*은 옥타브 버전을 의미합니다.
