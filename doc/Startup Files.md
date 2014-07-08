#자동 실행 파일

 옥타브가 실행될 때, 다음의 리스트에 있는 파일에 있는 명령문을 읽어옵니다. 이 파일들은 함수의 설정을 포함한 옥타브 명령문을 포함할 수 있습니다.


   ***octave-home*/share/octave/site/m/startup/octaverc**

   *octave-home*은 옥타브가 인스톨된 경로를 의미한다.(기본적으로 `/usr/local`) 이 파일은 인스톨된 옥타브의 모든 버전과 모든 사용자에게 기본 환경의 변화를 적용한다. 모든 사용자에게 적용되기 때문에 이 파일을 변경하는 것은 조심해야 한다. 기본 파일은 환경 변수 `OCTAVE_SITE_INITFILE`에 의해 변경될 수 있다.

   ***octave-home*/share/octave/version/m/startup/octaverc

   i*octave-home*은 옥타브가 인스톨된 경로를 의미한다.(기본적으로 `/usr/local`) 그리고 *version*은 옥타브의 버전을 의미한다. 이 파일은 인스톨된 옥타브의 특정 버전과 모든 사용자에게 기본 환경의 변화를 적용한다. 모든 사용자에게 적용되기 때문에 이 파일을 변경하는 것은 조심해야 한다. 기본 파일은 `OCTAVE_VERSION_INITFILE`에 의해 변경될 수 있다.

   **~/.octaverc**

   이 파일은 기본 옥타브 환경를 자신에 맞게 변경할 때 쓰인다.

   **.octaverc**

   이 파일은 특정 프로젝트를 위한 옥타브 환경 설정에 사용될 수 있다. 옥타브는 `~/.octaverc`를 읽어온 후에 현재 경로에 이 파일이 있는지 찾는다. `~/.octaverc`파일에 있는 `cd`명령어는 `.octaverc`를 옥타브가 찾을 때 영향을 미친다.

   만일 홈 디렉토리에서 옥타브를 실행하면, `~/.octaverc`에 있는 명령문은 한번만 실행된다.


 옥타브를 `--silent` 옵션 없이 `--verbose` 옵션만으로 실행하면 자동 실행 파일에 있는 문구가 표시된다.

 `dump_prefs` 함수는 옥타브를 어떤 커스터마이징이 가능하며 효과가 있는 지 결정할 때 유용하다.


  **Function File: dump_prefs*()***
  **Function File: dump_prefs*(fid)***

    옥타브에 의해 구문분석이 되는 형식의 사용자 지정 변수를 표시합니다. *fid*는 `fopen`으로 받을 수 있는 파일 표시자입니다. 만일 *file*이 생략되면 리스트는 stdout으로 표시됩니다.
