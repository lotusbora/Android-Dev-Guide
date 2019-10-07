# CodeStyle 
- Java 에서 Kotlin에 따라 차이가 발생할 수 있는 점 참고! 
- Ktlint를 통해서 formatting 습관화! 이후에 ktlint로 수동으로 수정 : https://ktlint.github.io/

## Line
- 코드간의 간격은 1줄 이상 넘어가지 않도록 한다.
- 한 라인이 스튜디오 라인을 최대한 넘지 않도록 한다

## Variables 
### Order
1. Class TAG 정의
2. Key and Constants 정의
3. 각종 Object 정의 
4. Views 정의
5. General Variables 정의

### Key 
| Prefix | 설명 |
| ------------- | ------------- |
| `EXTRA_` | Intent |
| `PREF_` | SharedPreferences |
| `ARGUMENT_` | Fragment Arguments |
| `REQUEST` | Activity Request Code |
| `RESULT` | Activity Result Code 

### 기존자바의 m Prefix 코틀린에서는?
- Kotlin을 전환하기 때문에 멤버변수 앞에 m은 붙이지 않는다. 

## Parameter
1. 메서드갯수가 스튜디오 라인을 최대한 넘지 않도록 한다.
2. 안드로이드 관련 (Contexnt, Activity, Fragment, View 등은 가장 먼저 선언한다.)
3. 파라미터 ,다음에는 한 칸 띄고 다음 파라미터 선언을 한다.

```kotlin (1번, 2번, 3번 포함)
fun startActivity(context: Context, requestCode: Int, resultCode: Int,
                   data: Any, type: Int, tag: String) {  
  ...  
}
```

```kotlin (2번, 3번 포함)
fun startActivity(context: Context, requestCode: Int) {  
  ...  
}
```

### Fragment 
- Fragment에 `ARGUMENT_`를 넣어주는 경우, 해당 Fragment에 `newInstance()`를 구현하고 이를 사용한다.
(참조:https://m.blog.naver.com/PostView.nhn?blogId=tpgns8488&logNo=220989078813&proxyReferer=https%3A%2F%2Fwww.google.co.kr%2F)
- Fragment 생성자의 Parameter로 넘기지 않는다.
```kotlin
fun newInstance(index: Int): FavoriteFragment{
	val fragment = new UserFragment();
	Bundle().apply{
  	  args.putParcelable(ARGUMENT_INDEX, index);
	  fragment.setArguments(this)
 	}
	return fragment;
}
```

## 주석
- 주석은 최대한 지양하는 방향으로! 대신 코드 리팩토링 및 구조 개선 시에 필요에 따라 주석처리는 필요..
