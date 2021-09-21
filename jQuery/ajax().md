## jQuery.aja()

- 비동기 HTTP 요청을 수행한다.

***

# 형식
```javascript
var formData = $("#dataform").serialize();
//form을 대상으로 serialize()메소드를 사용하면 폼의 객체들을 한 번에 받아올 수 있다.
//id=kjk@naver.com&passwd=1235&...이런식으로 나열된다.

$.ajax({
	data :formData,             //요청과 함께 서버에 보내는 string 또는 json
	type:"POST",                //http 타입
	url : "/asinfo/delete",     //요청 url
	cache : false,              //캐시 처리
	success : delete_Handler    //성공시 호출할 함수
});
```
- cache : Ajax를 사용하다보면, 데이터가 갱신이 안되고, 이전 데이터가 그대로 남아있는 경우가 있다. 이는 브라우저에서 ajax통신을 할 때, 새로 url을 호출하지 않고, 가지고 있는 cache값을 그대로 노출시켜주기 때문이다.
- 이때는 cache옵션을 사용하여, 이런 현상을 방지할 수 있다.
- cache를 false로 주게되면 브라우저 캐쉬를 막아서 현재 값을 호출해 올 수 있다.