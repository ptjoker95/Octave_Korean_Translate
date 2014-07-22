# `readline` 바꾸기

옥타브는 명령어 입력 편집과 히스토리를 위해 GNU Readline 라이브러리를 사용합니다. Readline은 모두 유연하고 명령어 형식 파일을 통해 수정될 수 있습니다.(보다 정확한 명령어 형식을 알고 싶으면 GNU Readline 라이브러리를 참고하십시요.) 기본 형식 파일은 일반적으로 `~/.inputrc`입니다.

옥타브는 Readline을 초기화하는 두가지 명령어를 제공하고 그에 따라 명령어 입력 양태가 바뀝니다.

**Built-in Function: readline_read_init_file *(file)***

readline 라이브러라 초기화 파일인 *file*을 읽어옵니다. *file*이 생략되면, 기본 초기화 파일(일반적으로 `~/.inputrc`)을 읽어옵니다.

보다 자세한 내용은 GNU Readline 라이브러리에 있는 [Readline Init File](http://cnswww.cns.cwru.edu/php/chet/readline/readline.html#Readline-Init-File)을 참고하십시요.

**참고: ** [readline_re_read_init_file]()

**Built-in Function: readline_re_read_init_file *()***

마지막으로 읽어온 readline 라이브러리 초기화 파일을 다시 읽어옵니다. 보다 자세한 내용은 GNU Readline 라이브러리에 있는 [Readline Init File](http://cnswww.cns.cwru.edu/php/chet/readline/readline.html#Readline-Init-File)을 참고하십시요.

**참고: ** [readline_read_init_file]()
