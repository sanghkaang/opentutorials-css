# CSS 소개

- HTML은 정보를 표현하기 위한 언어
- 처음엔 디자인적 요소가 없었다
- 디자인적 요소가 필요해 <font>태그와 같은 디자인 담당 태그를 만들었지만 웹이 거대해지면서 난잡해지는 문제가 발생.
- 정보태그와 디자인태그가 혼재하게됨
- 그래서 웹개발자들은 HTML을 정보를 담는 그릇으로서 전념하게 하고 디자인적 요소는 따로 빼내서 하나의 새로운 언어를 만들게 되는데 그것이 CSS.
- CSS를 만들면서 생기는 장점 : HTML의 정보로서의 가치가 올라간다. / 중복의 제거
- 아래 두 코드는 같은 결과를 만들어 내지만 아래 코드가 더 간결(정보와 디자인을 분리)하고 재사용성이 높다.(만약 색깔을 바꾸어야하는 상황이라면 어떤게 더 편할까?)

```html
<li><font color="blue">HTML</font></li>
<li><font color="blue">CSS</font></li>
<li><font color="blue">JavaScript</font></li>
```

```html
<style>
  li {
    color:blue;
  }
</style>

<li>HTML</li>
<li>CSS</li>
<li>JavaScript</li>
```



# HTML과 CSS가 만나는 법

- 어떻게 HTML에 CSS를 삽입하는가?
- HTML에 CSS를 삽입하는 두가지 방식

```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      h2{color: blue}
    </style>
  </head>
  <body>
    <li>HTML에 CSS를 삽입하는 두가지 방식</li>
    <h1 style="color:red">Hello World</h1>
    <h2>Hello World</h2>
  </body>
</html>
```



# 선택자

- 인간의 언어는 주어와 서술어로 이루어져 있습니다. 이 두가지는 언어를 구성하는 양대축입니다. **선택자는 인간의 언어로 치면 주어에 해당하는 매우 중요한 요소입니다.** 주어를 자유롭게 사용하지 않으면 정상적인 언어 생활을 할 수 없는 것처럼 선택자를 자유롭게 사용할 수 없으면 CSS를 정복할 수 없습니다. 후속 수업에서는 선택자가 무엇인지, 어떤 선택자들이 있는지를 알아봅니다


## 선택자와 선언

- CSS 기본적인 문법
  - CSS를 적용하고자 하는 태그(선택자 selector)
  - 선택자에 적용할 디자인(선언 declaration)

```html
<style>
  li(선택자)
    {color:red;}(선언)
</style>
```

*선언하는 내용 끝에 세미콜론 붙이는 것을 습관화하는게 좋다


## 선택자의 종류

- 선택자의 종류
  - 태그 선택자
    - 모든 선택자에 디자인 적용
    - 모든 태그에 적용
    - 그냥 태그 이름 사용
  - 아이디 선택자
    - 고유한 하나의 태그에만 아이디 부여해서 디자인 적용
    - #아이디 이름
    - id는 중복되어선 안되잖아
  - 클래스 선택자
    - 여러 개의 태그를 클래스로 그룹핑해서 디자인 적용
    - .클래스 이름
    - 꼭 같은 이름의 태그일 필요 없음
    - 다른 종류의 태그를 그룹핑해도 됨


## 부모 자식 선택자

- 좀 더 심화된 선택자의 형태
- ul li {...}
  - 상위 태그 띄워쓰고 하위 태그의 형태
  - 상위 태그 밑에 모든 하위 태그들에 디자인 적용
- ul>li {...}
  - 상위 태그 > 하위 태그의 형태
  - 상위 태그 바로 밑 직계 자손 하위 태그에만 디자인 적용
- ul,ol {...}
  - 단순 열거
  - 중복 적용
  - ul에도 적용하고 ol에도 똑같은 디자인 적용


## 선택자 공부 팁

- cheatsheet : 개발자세계에서 언어요약본같은 느낌.
- 구글 이미지 검색으로 찾으면 많이 나온다.
- 개발할 때 하나씩 구비해서 필요할 때 찾아서 쓰면 좋다


## 가상 클래스 선택자

- 가상 클래스 선택자
  - 클래스 선택자처럼 행동하지만 클래스 선택자는 아닌 선택자
  - 엘리먼트의 특성에 따라 클래스 선택자처럼 몇몇 태그를 그룹핑한다
- <style> 태그에서 위에 있는 것이 우선순위가 높다.
- 종류
  - link - 방문한 적이 없는 링크
  - visited - 방문한 적이 있는 링크
  - hover - 마우스를 롤오버 했을 때
  - active - 마우스를 클릭했을 때
  - 위의 선택자는 순서대로 지정하는 것이 좋습니다. 특히 visited의 경우는 보안상의 이유로 아래와 같은 속성만 변경이 가능합니다.
    - color
    - background-color
    - border-color
    - outline-color
    - The color parts of the fill and stroke properties


## 여려가지 선택자들

# 속성을 공부하는 방법
