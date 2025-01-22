% C, Perl, Linux
% yesyesbike
%
# "모든 길은 로마로 통한다. 그리고 오늘은 목요일이다." -미상

***

[홈으로](index.html)

[잡다](jobda.html)

<br>

2024년에 뭘 배웠는지는 이미 기억에서 증발해 2025년에 배운 것부터 기록함.
평소에 기록을 잘하자!  
글쓰기 실력과 코딩 실력의 상관관계가 있는지는 몰라도 내가 긴 글을 잘 못 쓰는 것과
긴 코드를 잘 못 짜는 건 관련이 있는 것 같다.

<br>

## 프로그래밍 언어

### C

### Perl
#### [Perl One-Liners Guide][PERL_ONE]

### Scheme
어떤 프로그래밍 언어든 다 똑같겠지만 Lisp를 배운다면 좋은 텍스트 편집기는 선택이 아닌 필수다.
괄호만으로 프로그램의 구조를 나타내기 때문에 이를 자동으로 정렬해 주는 기능이 없다면 고생이 클 것이다.  
가장 먼저 자동으로 들여쓰기를 맞춰주는 기능이 필요하다.
이것도 `lambda`나 `define` 같은 특수 형태와 일반 프로시저를 구별해야 한다.
일반 프로시저의 인자는 항상 같은 열에 위치하게끔 해야 한다.
반면 특수 형태의 인자는 각각 다른 열에 위치할 수도 있다.
예를 들자면 다음과 같다.

```
(+ (* 2 3)
   (* 3 6))

(lambda (n)
  (* n n))
```

그 다음으로 괄호의 짝을 다른 색으로 표시하는 기능이 있다.
맨 끝에 괄호를 빼먹는 실수를 줄이려면 어느 게 어느 것과 짝인지 알아야 한다.  
웬만한 편집기에 이런 기능은 다 포함되어 있으니 편한 걸 가져다 쓰면 된다.
#### [An Introduction to Scheme and its Implementation][SCHEME_IMPLEMENT]
처음으로 `Scheme`를 공부한다면 이 글을 읽으라고 권하고 싶다. `Scheme` 문법
만 다루는 게 아니라 그게 어떤 식으로 구현되어 있는지 꽤 자세히 설명한다.
리스트의 `car`는 값인데 `cdr`는 또 다른 리스트인 이유를 여기서 알게 되었다.  
`cons`는 값 둘을 받아서 하나의 값을 반환한다. 반환값은 일종의 노드이다.
두 값은 각각 노드의 `car`과 `cdr`에 저장된다. `cdr`에 무슨 값이 들어가느냐에 따라 리스트인지 아닌지 결정된다.
리스트라면 `cdr`는 리스트의 다음 원소에 해당하는 노드를 가리킨다.
리스트가 아니라면 `cdr`에 다른 값이 들어간다.
즉 리스트의 노드는 연결 리스트의 노드처럼 한쪽에는 값이 들어가고 다른 한쪽에는 다음 원소의 노드를 가리키는 포인터가 들어간다
(정확히 포인터인지 아닌지는 구현에 따라 다를 테지만 작동 원리를 이해하기에는 이 비유가 적합하다.
참고로 리스트에 들어가는 값은 모두 값 자체가 아니라 전부 값을 가리키는 포인터다.
하지만 이 비유는 적절한 설명 없이는 혼동만 불러일으키므로 자세한 설명은 직접 읽어보는 게 좋다).
맨 끝 노드의 `cdr`는 빈 리스트(`'()`)다.
이는 C언어의 `NULL`과 상당히 비슷하다. 실제로 빈 리스트는 `null?` 프로시저에서 참을 반환한다.
이제 `cons`의 `cdr`쪽에 리스트를 인자로 주면 또 다른 리스트를 반환하는 이유를 알 수 있을 것이다.  
아무런 배경지식이 없는 상태에서 배우기에는 지금까지 읽은 책 중에서는 이 책이 가장 적합하다.
다만 군데군데 빠져 있는 곳이 많이 있어서 아쉬움이 남는다. 인터프리터를 제작하는 단원에서 이게 잘 드러난다.
책에 있는 예제 코드를 취합해도 빠져 있는 코드 때문에 돌릴 수 없다. 물론 빈 자리를 채우는 게 독자 몫이라면 할 말은 없다.
#### [The Nature of Lisp][LISP_NATURE]

<br>

## 컴퓨터 일반
#### [Structure and Interpretation of Computer Programs][SICP]
마법사 책으로도 잘 알려져 있는 SICP는 프로그래밍의 핵심적인 개념을 다룬다.
하지만 이 책에서 다루는 프로그래밍 언어인 Scheme의 문법을 우선적으로 다루지는 않으므로
Lisp 언어 자체를 먼저 익히고 싶다면 다른 책을 찾아 읽는 게 좋다. 다른 책에 비해 문법에서는 진도가 많이 느리다.
하나의 핵심 원리를 깊이 있게 다루고 나서 다음으로 넘어가기 때문에 그런 것 같다.  
책의 구성은 이론과 연습 문제 둘로 나누어져 있다. 연습 문제를 풀어야 비로소 이론이 어떻게 적용되는지 알 수 있다.
이를 소홀히 하면 앞으로 나오는 문제들도 건너뛰게 될 것이고 점점 이해하기 어려워질 것이다.
이 점에서 수학과 꽤 비슷하다. 다음 절에 설명하는 내용은 결국 전에 나온 내용을 이해했다는 전제 하에 이해할 수 있다.
가장 좋은 건 모든 연습 문제를 풀어보는 것이지만 꽤나 어려운 게 섞여있으므로 안 풀리는 문제는 적당히 넘어가는 게 좋다.
어떤 문제는 문제 자체가 이해가 잘 안된다. 그렇다고 번역기를 돌려봐도 크게 나은 건 없다.  

1장에서 다루는 핵심 개념은 다음과 같다.

* 프로시저 선언
* 재귀와 반복
* 간단한 프로시저를 엮어 또 다른 프로시저 구성하기
* 프로시저들의 공통점을 모아 하나의 프로시저로 일반화하기

간단한 것을 모아 복합적인 것을 이루고 그것들 사이에서 하나의 공통된 표현 방법을 이끌어내는 것은 매우 중요하다.
Lisp의 프로시저는 일급이기 때문에 그 자체를 다른 프로시저의 전달인자로 줄 수 있다.
이 때문에 훨씬 더 강력한 표현력을 가진다. 다른 프로그래밍 언어에서는 자료형 같은 제약 때문에 불가능한 것도 쉽게 할 수 있다.  
재귀는 Lisp에서 루프를 구현할 수 있는 유일한 방법이다. Lisp를 쓴다면 좋으나 싫으나 재귀에 익숙해져야 한다.
재귀는 시간과 공간 두 측면 모두에서 반복문보다 비효율적이지만 프로시저의 맨 끝 구문에서만 재귀를 사용한다면 쉽게 최적화할 수 있다(Tail Call).
공간 측면에서는 새로운 스택을 할당할 필요 없이 최초 스택 안에서 모든 걸 처리할 수 있어서 반복문만큼 좋다.
스택 할당에 드는 시간을 아끼면서, 동시에 재귀 호출을 `goto` 문처럼 사용하면서 시간 측면에서도 이득을 볼 수 있다.

아직 1장도 다 못 읽었기 때문에 책 전체를 평가하기는 이르다.

<br>

## 생산성
### Vim
#### [Learn Vimscript the Hard Way][VIMHARDWAY]  
편집기에서 터미널로 코드를 전송하는 함수를 작성하려면 그걸 수행하는 Vim API를 알아야 한다.
아직까지도 변수 다루는 법을 모르니 이번 기회에 잘 공부해서 플러그인도 짜봐야겠다.

<br>

## 하드웨어

<br>

## 해커 정신
#### [The Art of Unix Programming][TAOUP]  
유닉스 철학에 대한 글은 많지만 이렇게 한 권의 책으로 구성된 건 흔치 않다.
몇 쪽이나 될지는 잘 모르겠지만 수백 쪽은 족히 될 것 같다.  
유닉스가 그토록 오랜 세월 동안 살아남은 건 무엇 때문인가?
물론 정식으로 인증받은 유닉스는 거의 남아있지 않지만 그 정신은 전 세계 해커들에게 퍼져 있다.
내가 유닉스를 좋아하는 이유는 윈도우를 싫어하는 이유와 정반대이다.

1. 유닉스는 삶을 편리하게 하지만 윈도우의 GUI는 그걸 불가능하게 한다.
1. 유닉스에서는 자유롭게 작업 환경을 자기 입맛대로 뜯어 고치기 쉽지만 윈도우는 그게 매우 힘들고 제한적이다.
1. 유닉스의 인터페이스는 투명하지만 윈도우는 모든 게 안개에 둘러싸여 있다.
1. 유닉스에서는 쉘을 중심으로 작업을 자동화하기 편하지만 윈도우에서는... 안 해봐서 모르겠다.
1. 유닉스는 공부한 만큼 보상이 돌아오지만 윈도우는 공부하는 보람이 적다.
1. 유닉스는 프로그래밍을 하기 위한 환경을 구축하기 쉽지만 윈도우는 걸리적거리는 게 많다.
1. 유닉스는 원한다면 최소한의 것만 사용할 수 있지만 윈도우의 끼워팔기는 혀를 내두르게 한다.

#### [How To Become A Hacker][HACKER]

[BISON]: https://www.gnu.org/software/bison/manual/bison.html
[FLEX]: https://westes.github.io/flex/manual/
[HACKER]: http://www.catb.org/~esr/faqs/hacker-howto.html
[LISP_NATURE]: https://www.defmacro.org/ramblings/lisp.html
[PERL_ONE]: https://learnbyexample.github.io/learn_perl_oneliners/preface.html
[SCHEME_IMPLEMENT]: https://docs.scheme.org/schintro/schintro_toc.html
[TAOUP]: http://www.catb.org/esr/writings/taoup/html/
[VIMHARDWAY]: https://learnvimscriptthehardway.stevelosh.com/
[SICP]: https://mitp-content-server.mit.edu/books/content/sectbyfn/books_pres_0/6515/sicp.zip/full-text/book/book-Z-H-1.html#titlepage