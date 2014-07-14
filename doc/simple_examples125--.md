##적미분 방정식

  옥타브는 아래의 모양과 같은 비선형 미분 방정식을 풀기위한 기본 함수를 가지고 있습니다.

  	dx
	-- = f (x, t)
	dt

  초기 조건은

  	x(t = t0) = x0

  이런 형식의 적분 방정식을 옥타브에서 사용하기 위해서는, 우선 함수 `f(x,t)`의 정의를 내려야 합니다. 명령줄에 함수식을 그대로 입력하는 것만으로 충분할 수 있습니다. 예를 들어, 아래의 명령문들은 비선형 방정식의 유의미한 부분으로 오른편의 함수를 정의했습니다. 사용자가 함수를 입력하는 동안, 옥타브는 기본 모양과는 다른 프롬프트를 보여줌으로서 입력이 끝나기를 기다리고 있다는 것을 표현합니다.

  	octave:1> function xdot = f (x, t)
	>
	> r = 0.25;
	> k = 1.4;
	> a = 1.5;
	> b = 0.16;
	> c = 0.9;
	> d = 0.8;
	>
	> xdot(1) = r*x(1)*(1 - x(1)/k) - a*x(1)*x(2)/(1 + b*x(1));
	> xdot(2) = c*a*x(1)*x(2)/(1 + b*x(1)) - d*x(2);
	>
	> endfunction

  초기 조건을 주고

  	octave:2> x0 = [1; 2];

  출력 시간을 한개의 열벡터로 만들고 나면 (처음 시간은 위의 초기 조건에 맞는 시간임에 유의)

 	octave:3> t = linspace (0, 50, 200)';

  미분 방정식을 적분하는 것은 매우 쉬워집니다.

  	octave:4> x = lsode ("f", x0, t);

  `lsode`함수는 일반적인 미분방정식을 풀기 위한 Livermore Solver를 사용합니다. Livermore Solver는 A. C. Hindmarsh. ODEPACK, a Systematized Collection of ODE Solvers, in: Scientific Computing, R. S. Stepleman et al. (Eds.), North-Holland, Amsterdam, 1983, pages 55-64를 참조했습니다.
