##선형 방정식 풀이 시스템


  선형 방정식 문제는 수치 분석에서 언제나 등장합니다. 선형 방정식 `Ax = b`을 풀기 위해서, 역슬래시 '\'를 이용합니다.

  	x = A \ b

  이것은 `inv(a) * b'와 개념적으로 같습니다만, 가역행렬을 직접 계산하는 것을 피할 수 있습니다.

  계수행렬이 단일이라면, 옥타브는 경고 메세지를 보여주고 최소 norm solution을 계산합니다.

  간단한 예로는 화학에서 볼 수 있으며, 화학 방정식의 등치 (Balanced Chemical Equations) 를 확인할 수 있습니다. 수소와 산소가 물을 만드는 것을 생각해봅시다.

  	H2 + O2 --> H20

  위의 식을 정확하지 않습니다. 질량 보존의 법칙에 의해 식의 왼쪽과 오른쪽에 있는 각각의 분자 수는 같아야 합니다. 수소와 산소 각각에 대한 전체적인 반응식은

  	x1*H2   + x2*O2  --> H2O
	H: 2*x1 + 0*x2   --> 2
	O: 0*x1 + 2*x2   --> 1

  와 같습니다. 옥타브에서는 단 3줄만에 값을 구할 수 있습니다.

  	octave:1> A = [ 2, 0; 0, 2 ];
	octave:2> b = [ 2; 1 ];
	octave:3> x = A \ b
