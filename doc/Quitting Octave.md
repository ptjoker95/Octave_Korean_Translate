#옥타브 종료하기

 **Built-in Function: exit *(status)***
 
 **Built-in Function: quit *(status)***

   옥타브 세션을 종료합니다. 정수 *status*가 설정되면, 옥타브 종료 상태로 OS에 그 값을 리턴합니다. 기본값은 0입니다.
 

 **Built-in Function: atexit *(fcn)***

 **Built-in Function: atexit *(fcn, flag)***

   옥타브가 종료될 때 호출되는 함수를 저장합니다.

   		function last_words ()
	        disp ("Bye bye");
    	endfunction
		atexit ("last_words");
	
	의 식은 옥타브가 종료될 때 `"Bye bye"`라는 메세지를 출력합니다.

    *flag* 옵션은 옥타브가 종료될 때 호출될 함수의 목록에서 *fcn* 함수를 저장하거나 삭제할 때 사용됩니다. *flag* 옵션이 true이면 저장하고, *flag* 옵션이 false이면 삭제합니다. 예를 들어, 위에서 저장한 `last_words` 함수를 저장한 후에,

		atexit ("last_words", false);
	
	를 하게 되면 리스트에서 저 함수를 삭제하고, 옥타브가 종료될 때 `last_words`를 호출하지 않습니다.

	`atexit`는 리스트에 있는 함수 중에서 첫번째 것만을 삭제합니다. 따라서 어떤 함수가 `atext`에 의해서 여러번 저장되어 있으면, 리스트에서 그 함수를 지우기 위해서는 여러번 호출되어야 합니다.
