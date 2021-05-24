# CSSL
<body>
  <div>
  <h2>DL 및 자식태그 DT 및 DD태그 연습</h2>
        <dl>
            <dt>HTML</dt>
        
  <dd>
      HTML은 HyperText Markup Language의 약자로
      매우 쉽고
      빠르게 웹 문서를 만들 수 있는 마크업 언어이다.        
  </dd>

  <dt>CSS</dt>

  <dd>
      CSS는 Cascading Style Sheet의 약자로
      HTML문서의
      스타일을 정의하는 규약이다.
  </dd>

  <dt>자바스크립트</dt>

  <dd>
      자바스크립트는 HTML문서에서 사용할 수 있는
      프로그래밍 언어로 HTML문서에 다양한
      효과를 줄때 사용한다.
  </dd>
  </dl>
   <div>
</body>


# HTML

  
1] TextBasic01
---
    
    <br/>  : 엔터키
    &nbsp; : 스페이스바

2] TextBasic02
---
  
    <u> : 밑줄 긋기 
    <s>,<del>,<strike> : 가운데 줄 긋기 
    <i> : 이탤릭체 
    <strong> : 글자 진하게 
    <sup> : 위첨자 
    <sub> : 아래첨자 

    * 중요
        인라인 엘리먼트 안에는 블락 엘리먼트를 넣을 수 없다.
        블락 엘리먼트 안에는 다 가능하다.

3] TextBasic03
---

    &nbsp;  : 스페이스바 한번(빈칸)
    &gt;    : > (greater then)
    &lt;    : < (letter then)
    &amp;   : &
    &quot;  : "(double quotation)
    &apos; 혹은 &# 39 : '&apos;'는 IE에서는 적용 안됨
        
4] Form04_1
---
    
    form태그 : 사용자가 입력한 값 혹은 선택한 값을 서버로 전송할 때 사용하는 태그
        
    주요 속성 
    action : 사용자가 입력한 값을 전송할 서버상에 있는 페이지 경로 지정
           (action생략시 기본값은 자신의 페이지)
    method : get, post(생략시 get)
           get : 데이터 노출 됨, http 요청 헤더에 포함되서 전송됨, 최대 4KB
           post : 데이터 노출 안됨, http 요청 바디에 내용이 포함되서 전송됨, 무한대
    targer : 이 속성은 a태그의 target속성과 같은 기능
    enctype : URL인코딩 박싱 지정

5] Form04_2
---
    form하위 태그
    [1] type 속성
    text : 한 줄 입력상자
    password : 입력시 입력한 값이 노추 안되게
    checkbox : 여러개 선태 가능한 체크 박스 표시
              체크된 상태로 보여주려면 checked  속성 추가
    radio : 하나만 선택 가능한 라디오 박스 표시할 때
            체크된 상태로 보여주려면 checked 속성 추가
    hidden : 값을 웹브라우저에 표시하지 않고 전송하고자 할 때 브라우저에 보이지 않음
    
    [2] name 속성
    [3] value 속성

# CSS

1] Selector01
---

    * { } : 전체 선택자
    
    태그명 { } : 태그 선택자
    
    .클래스명 { } : 클래스 선택자
    
    .클래스명 하위 { } : 하위 선택자 (스페이스로 구분)
    
    .클래스명 > 자식 { } : 자식 선택자 (>로 구분)
    
    .클래스명 , , , { } : 다중 선택자 (,로 구분)
    
    #아이디명 { } : 아이디 선택자
    
    
# 자바스크립트

1] Variable01
---
    var num1=10, num2; 
    var str1="쟈스", str2;
    var date = new Date()
    var nullvar = null;
    var obj{};
    
    num1+num2의 값은 NaN 타입은 Number
    str1+str2의 값은 쟈스undefined 타입은 String
    date의 값은 오늘 날짜, 타입은 object
    nullvar의 값은 null, 타입은 object
    obj의 값은 [object Object], 타입은 object
    
    obj{} 변수, 메서드 모두 obj.으로 값 할당 할 수 있다!
    obj.name="가길동";
    obj.age=20;
    
    var obj2{
        id:"KIM",
        pwd:"1234",
        name:"김길동",
        eat:function(food){
            document.write(this.name+"이 "+food+"를 먹다")
            }
    }
       
    obj2.eat("피자") = KIM이 피자를 먹다


2] Operator02
---

조건식에서 0 or null or false만 false 

나머지 모두 true
  
    document.write("가나다">="가다나"); // 쟈스에서 가능하지만 자바에선 불가능
    // true
    document.write(3 >= 9 == 0); // 3>=9 는 false, 0 은 false 즉 false == false
    // true
    
==(동등연산자-Equality)와 ===(일치연산자 Identity)

==자료형이 다르더라도 내부적 강제 형변환해서 비교

===는 강제 형변환 과정없이 정확히 값하고 자료형이 일치할때만 true

<a href="javascript:history.back()">뒤로 가기</a>

3] Arrays03
---
자바와는 다르게 배열의 크기가 불변이다.
    
      선언방법1
      var arrays = new Array(3);
      arrays[0] = 100;
      arrays[1] = new Date();
      arrays[2] = 3.14;
      
      arrays[3] = true; //3번방은 없지만 크기가 불변이다.
      arrays.push(200);
      
      arrays[1] = new Date();
      arrays[1] = new Date();
