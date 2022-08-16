# Sass_
  ### ✍️ Learning Sass


- link href="style/main.css" rel="stylesheet" /

  
- 빌드업 명령어 
  - sass style/main.scss:style/main.css
  - sass --watch ... (실시간 반영)
    - 확장형 (extend) / 압축형 
      - 압축형 : sass sass --watch --style compressed ...
      
- 주석
  - /**/ (0), // (x) -> 빌드 시에 반영 안됨

- 중첩 (nesting), 이중 중첩
  - div { p { } span {} }
  
- 네임스페이스 속성 중첩 + 의사 클래스
  - font : { family: ; size: ; weight: ;}
  - & (엠퍼샌드)
  
- 변수 
  - 스타일시트에서 재사용할 정보를 저장한다 
    - ex. $main-color : ...;
- 믹스인
  - 재사용 할 스타일"그룹"을 정의한다
  - 정의 : @mixin my-font { font-family: ; font-syle: ; font-size: ; font-color: ; }
  - 호출 : h1 { @include my-font; }

    - 믹스인 인자 
      - 인자를 취한다 (여러 인자 활용)
      - ex. 정의 : @mixin my-font ($font-color) {color: $font-color;}
          호출 : h1 {@include my-font(red)}
