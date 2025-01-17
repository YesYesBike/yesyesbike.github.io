% C, Perl, Linux
% yesyesbike
%
# "나무는 나무로 이루어져 있다." -미상

***

[홈으로](index.html)

[잡다](jobda.html)

[마크다운 소스파일](mdtest.md)

<br>

## 어떻게 마크다운에서 HTML 파일을 만들었는가?

애초에 마크다운 언어가 HTML 파일로 변환되도록 만들어졌다.
마크다운에서 HTML 태그를 사용할 수 있는 것도 이 때문이다.  
일단 [Discount Markdown][DISCOUNT]이 필요하다.
설치하고 나면 `markdown` 명령어로 마크업 파일을 HTML로 변환할 수 있다. `stdout`으로 출력된다.  
하지만 출력에서 body 부분만 있고 나머지는 빠져있다.
그래서 전체 HTML 파일로 출력하는 [프로그램][MD2HTML]을 하나 작성했다.

<br>

## 앞으로의 계획

비록 HTML만으로도 충분히 정보를 전달할 수 있지만 글씨가 너무 작아서 읽기 힘들 때가 있다.
style 태그를 넣는 법은 알고 있으니 이제 무슨 스타일을 적용할지를 공부해야겠다.

[DISCOUNT]: https://www.pell.portland.or.us/~orc/Code/discount/
[MD2HTML]: https://github.com/YesYesBike/.dotfiles/blob/master/util/md2html
