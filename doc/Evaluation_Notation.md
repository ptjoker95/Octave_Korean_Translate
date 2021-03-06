#1.3.2 결과값 표시방법

 이 매뉴얼의 예제에서 명령문의 결과는 '⇒ '로 표시됩니다. 예를 들어,

  sqrt (2)
  	⇒ 1.4142

  이것을 "`sqrt(2)`은 1.4142 값을 내놓는다"라고 할 수 있씁니다.

  어떤 경우에 명령문에 의해 값이 나오는 행렬은 다음과 같이 표시될 수 있습니다.

  	[1. 2; 3, 4] == [1, 3; 2, 4]
		⇒ [ 1, 0; 0, 1]

  다른 경우에는 결과의 구조를 명확히 보여주기 위해 다음과 같이 표시될 것입니다.

  	eye (3)
		⇒ 1 0 0
		  0 1 0
		  0 0 1

  때로는 한가지 명령문이 다른 명령문에 의한 값과 같다는 걸 보여줘야 할 때도 있을 것입니다.
  명령문이 서로 같다는 것을 보여줄 때에는 '≡ '을 이용할 것입니다. 예를 들어,

  	rot90 ([1, 2; 3, 4], -1)
	≡
	rot90 ([1, 2; 3, 4], 3)
	≡
	rot90 ([1, 2; 3, 4], 7)

  와 같이 표현될 것입니다.
