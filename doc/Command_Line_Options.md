#명령문 옵션

 옥타브에서 사용가능한 전체 명령문 옵션입니다.

 `--built-in-docstrings-file filename`

   옥타브의 기본 함수를 위한 문서 파일의 이름을 지정합니다. 이 값은 정확해야 하며, 매우 특별한 상황에서만 필요합니다.

 `--debug`
 `-d`

   구문 해석 디버깅 모드로 들어갑니다. 이 옵션을 사용하게 되면 명령문에 대한 많은 정보를 출력하는 옥타브의 구문 해석기가 작동하고, 구문 해석기를 디버깅할 때 매우 유용할 것입니다.

 `--debug-jit`

   JIT 컴파일러의 디버깅과 트레이싱을 가능하게 합니다.

 `--doc-cache-file **filename**`

   캐쉬 파일로 사용할 파일명을 지정합니다. `OCTAVE_DOC_CACHE_FILE` 설정에 지정된 값은 명령문에서 **filename**으로 지정된 값으로 대체됩니다. 캐쉬 파일은 `doc_cache_file` 함수를 이용해서 시스템이나 사용자가 확인 및 수정할 수 있습니다.

 `--echo-commands`
 `-x`

   실행된 명령어를 보여줍니다.

 `--eval *code*`

   *code*를 실행하고 종료합니다. `--persist`옵션이 있으면 종료되지 않습니다.

 `--exec-path *path*`

   프로그램이 실행될 경로를 지정합니다. 명령줄에서 지정된 *path*의 값은 기본적으로 지정된 `OCTAVE_EXEC_PATH`값을 대체합니다. 경로값은 기본 변수 `EXEC_PATH` 값으로 시스템이나 사용자가 확인 및 수정할 수 있습니다.

 `--force-gui`

   그래픽 유저 인터페이스(GUI) 로 옥타브를 실행합니다.

 `--help`
 `-h`
 `-?`

   짧은 도움말 메세지를 출력합니다.

 `--image-path **path**`

   이미지를 찾는 경로를 추가합니다. 명령줄에서 지정된 **path**의 값은 기본적으로 지정된 `OCTAVE_IMAGE_PATH`값을 대체합니다. 경로값은 기본 변수 `IMAGE_PATH` 값으로 시스템이나 사용자가 확인 및 수정할 수 있습니다.

 `--info-file **filename**`

   사용할 info 파일의 이름을 지정합니다. 명령줄에서 지정된 **filename**의 값은 기본적으로 지정된 `OCTAVE_INFO_FILE`값을 대체합니다. Info 파일은 기본 함수 `info_file`으로 시스템이나 사용자가 확인 및 수정할 수 있습니다.

 `--info-program **program**`

   사용할 info 프로그램의 이름을 지정합니다. 명령줄에서 지정된 **program**의 값은 기본적으로 지정된 `OCTAVE_INFO_PROGRAM`값을 대체합니다. Info 프로그램은 기본 함수 `info_program`으로 시스템이나 사용자가 확인 및 수정할 수 있습니다.

 `--interactive`
 `-i`

   대화식 환경을 지정합니다. 이 옵션은 리모트 쉘이나 Emacs 쉘 버퍼에서 옥타브를 실행할 때 유용합니다. Emacs에서 옥타브를 실행하는 다른 방법은 [Emacs Octave Support](Emacs\ Octave\ Support.md)를 참고하십시요.

 `--jit-compiler`

   액설러레이팅 루프를 사용할 때 JIT 컴파일러를 사용합니다.

 `--line-editing`

   Force readline use for command-line editing (번역 필요)

 `--no-gui`

   그래픽 유저 인터페이스(GUI) 대신 커맨드 라인 인터페이스(CLI)를 사용합니다.

 `--no-history`
 `-H`

   명령문 기록을 하지 않습니다.

 `--no-init-file`

   초기설정 파일 `~/.octaverc`와 `.octaverc`을 읽지 않습니다.

 `--no-init-path`

   기본 경로를 포함한 검색 경로를 초기화하지 않습니다.

 `--no-line-editing`

   명령문 수정을 하지 않습니다.

 `--no-site-file`

   초기설정 파일 `octaverc`를 읽지 않습니다.

 `--no-window-system`
 `-W`

   그래픽을 포함한 윈도우 시스템을 사용하지 않습니다. 터미널 환경만 사용하도록 합니다.

 `--norc`
 `-f`

   시작할 때에 시스템이나 사용자의 어떤 초기설정 파일도 읽어오지 않습니다. 이것은 `--no-init-file`과 `--no-site-file`을 같이 사용한 것과 같습니다.

 `--path **path**`
 `-p **path**`

   함수 파일을 찾는 검색 경로의 헤드를 추가합니다. **path**의 값은 기본적으로 지정된 `OCTAVE_PATH`값을 대체합니다. 경로 지정 함수 중에 하나로 시스템이나 사용자가 별도로 경로를 지정할 수 있습니다.

 `--persist`

   `--eval` 옵션이 실행된 뒤나 명령줄에서 지정된 파일을 읽은 후에 대화형 모드로 진행됩니다.

 `--silent`
 `--quiet`
 `-q`

   시작할 때 표시되는 문구나 버전 메세지를 표시하지 않습니다.

 `--texi-macros-file **filename**`

   makeinfo에서 사용되는 Texinfo 매크로를 포함한 파일의 이름을 지정합니다.

 `--traditional`
 `--braindead`

   `MATLAB`과 같이 사용자 설정 초기값을 다음과 같이 지정합니다.

	PS1										=	">> "
	PS2										=	""
	allow_noninteger_range_as_index			=	true
	beep_on_error							=	true
	confirm_recursive_rmdir					=	false
	crash_dumps_octave_core					=	false
	save_default_options					=	"-mat-binary"
	do_braindead_shortcircuit_evaluation	=	true
	fixed_point_format						=	true
	history_timestamp_format_string			=	"%%-- %D %I:%M %p --%%"
	page_screen_output						=	false
	print_empty_dimensions					=	false

   그리고 다음의 경고를 끕니다.

   	Octave:abbreviated-property-match
	Octave:fopen-file-in-path
	Octave:function-name-clash
	Octave:load-file-in-path

   이 옵션은 작성한 코드가 옥타브에서는 작동하지만 `MATLAB`에서는 작동하지 않는다는 걸 알려주는, `Octave:matlab-incompatible` 경고를 끄지 않습니다. ([warning](Issuing\ Warnings.md), [warning_ids](Issuing\ Warnings.md) 를 참고하십시요.)

 `--verbose`
 `-V`

   상세한 설명이 출력되는 모드입니다.

 `--version`
 `v`

   현재 사용 중인 옥타브의 버전을 출력하고 종료합니다.

 *`file`*

   *file*에 있는 명령문을 실행합니다. `--persist` 옵션이 없으면 종료합니다.


 옥타브는 실행시에 추가된 옵션과 조건들을 포함하는 정보를 출력하는 몇가지 함수를 가지고 있습니다.

 **기본함수: argv()**

   옥타브실행시에 추가된 조건을 알려줍니다. 예를 들어, 다음과 같이 옥타브를 실행했을 때,

   	`octave --no-line-editing --silent`

   `argv` 함수는 `--no-line-editing`과 `--silent`를 출력할 것입니다.

   옥타브 스크립트 실행문을 쓰고 싶을 때, `argv` 는 스크립트에 전해진 조건의 리스트를 출력할 것입니다. 옥타브 스크립트 실행문을 만드는 예제는 [Executable Octave Programs](Executable\ Octave\ Programs.md)를 참고하십시요.

#####기본함수: program_name()

   `program_invocation_name`에서 반환된 값의 마지막 구성을 출력합니다.

   참고: [Program_invocation_name](Command%20Line%20Options.md#%EA%B8%B0%EB%B3%B8%ED%95%A8%EC%88%98-program_invocation_name)

#####기본함수: program_invocation_name()

   옥타브를 실행할 때, 프롬프트 상에서 쓰여진 이름을 반환합니다.

   명령줄에서 스크립트를 실행(예: `octave foo.m`)하거나 옥타브 스크립트를 실행할 때, 프로그램의 이름은 스크립트의 이름으로 정해집니다. 옥타브 스크립트를 만드는 예는 [Executable Octave Programs](Executable\ Octave\ Programs.md)를 참고하십시요.

   참고: [program_name](Command%20Line%20Options.md#%EA%B8%B0%EB%B3%B8%ED%95%A8%EC%88%98-program_name)


   위의 함수를 이용해  옥타브를 실행할 때 사용된 옵션을 보여주는 예입니다.

     printf ("%s", program_name())
	 arg_list = argv ();
	 for i = 1:nargin
	   printf ( " %s", arg_list{i})
	 endfor
	 printf ("\n")

   셀 어레이에서 객체들을 찾는 설명은 [Indexing Cell Arrays](Indexing\ Cell\ Arrays.md)을 참고하십시요. 그리고 `nargin` 변수에 관한 정보는 [Defining Functions](Defining\ Functions.md)를 참고하십시요.
