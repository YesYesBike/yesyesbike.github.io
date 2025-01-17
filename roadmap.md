% C, Perl, Linux
% yesyesbike
%
# "모든 길은 로마로 통한다. 그리고 오늘은 목요일이다." -미상

***

[홈으로](index.html)

[잡다](jobda.html)

<br>

2024년에 뭘 배웠는지는 이미 기억에서 증발해서 2025년에 배운 것부터 기록함.
평소에 기록을 잘하자!  
글쓰기 실력과 코딩 실력의 상관관계가 있는지는 몰라도 내가 긴 글을 잘 못 쓰는 것과
긴 코드를 잘 못 짜는 건 관련이 있는 것 같다.

<br>

* 프로그래밍 언어
    * C
        * [Flex][FLEX]
        * [Bison][BISON]
    * Perl
        * [Perl One-Liners Guide][PERL_ONE]
    * Scheme
        * [An Introduction to Scheme and its Implementation][SCHEME_IMPLEMENT]  
        처음으로 `Scheme`를 공부한다면 이 글을 읽으라고 권하고 싶다. `Scheme` 문법
        만 다루는 게 아니라 그게 어떤 식으로 구현되어 있는지 꽤 자세히 설명한다.
		리스트의 `car`는 값인데 `cdr`는 또 다른 리스트인 이유를 여기서 알게 되었다.  
		`Scheme`에서 리스트는 연결 리스트로 구현되어 있다.
		`cons`는 연결 리스트의 노드를 만든다. `car`는 노드의 데이터에 해당하고 `cdr`는 다음 노드를 가리킨다.
		이런 원리를 깨우치니 공부하는 동안 의문으로 남았던 게 말끔히 씻겨나갔다.
		Pair도 어떻게 구현된 건지도 알게 되었다. `cdr`는 다음 노드를 가리키는 게 아니라 또 다른 값을 가리킨다.  
        다만 군데군데 빠져 있는 곳이 많이 있어서 아쉬움이 남는다.
        * [The Nature of Lisp][LISP_NATURE]

* 컴퓨터 일반
    * 컴퓨터 구조
    * 운영체제
    * 시스템 프로그래밍
    * 알고리즘
    * 네트워킹

* 생산성
    * Unix
    * Vim
        * [Learn Vimscript the Hard Way][VIMHARDWAY]  
        편집기에서 터미널로 코드를 전송하는 함수를 작성하려면 그걸 수행하는 Vim API를 알아야 한다.
		아직까지도 변수를 다루는 법도 모르니 이번 기회에 잘 공부해서 플러그인도 짜봐야겠다.

* 하드웨어
    * MCU

* 해커 정신
    * [The Art of Unix Programming][TAOUP]  
	유닉스 철학에 대한 글은 많지만 이렇게 한 권의 책으로 구성된 건 흔치 않다.
	몇 쪽이나 될지는 잘 모르겠지만 수백 쪽은 족히 될 것 같다.  
    유닉스가 그토록 오랜 세월 동안 살아남은 건 무엇 때문인가?
    물론 정식으로 인증받은 유닉스는 거의 없지만 그 정신은 전 세계 해커들에게 퍼져 있다.
    내가 유닉스를 좋아하는 이유는 내가 윈도우를 싫어하는 이유와 정반대이다.
        1. 유닉스는 삶을 편리하게 하지만 윈도우의 GUI는 그걸 불가능하게 한다.
        1. 유닉스에서는 자유롭게 작업 환경을 자기 입맛대로 뜯어 고치기 쉽지만 윈도우는 그게 매우 힘들고 제한적이다.
        1. 유닉스의 인터페이스는 투명하지만 윈도우는 모든 게 안개에 둘러싸여 있다.
        1. 유닉스에서는 쉘을 중심으로 작업을 자동화하기 편하지만 윈도우에서는... 안 해봐서 모르겠다.
        1. 유닉스는 공부한 만큼 보상이 돌아오지만 윈도우는 공부하는 보람이 적다.
        1. 유닉스는 프로그래밍을 하기 위한 환경을 구축하기 쉽지만 윈도우는 걸리적거리는 게 많다.
    * [How To Become A Hacker][HACKER]

[BISON]: https://www.gnu.org/software/bison/manual/bison.html
[FLEX]: https://westes.github.io/flex/manual/
[HACKER]: http://www.catb.org/~esr/faqs/hacker-howto.html
[LISP_NATURE]: https://www.defmacro.org/ramblings/lisp.html
[PERL_ONE]: https://learnbyexample.github.io/learn_perl_oneliners/preface.html
[SCHEME_IMPLEMENT]: https://docs.scheme.org/schintro/schintro_toc.html
[TAOUP]: http://www.catb.org/esr/writings/taoup/html/
[VIMHARDWAY]: https://learnvimscriptthehardway.stevelosh.com/
