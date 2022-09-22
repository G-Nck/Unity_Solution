### 프로퍼티 이름 해쉬화 혹은 ID화

유니티에선 내부적으로 String 문자열을 사용하여 프로퍼티를 지정하지 않고,
속도를 위해 프로퍼티 ID로 해시되어 사용됨.

프로퍼티를 문자열로 지정하는 방식은 문자열 해싱 수행 이후 정수값 메서드로 전달함.

이때 문자열 해싱으로 인해 성능 저하가 발생할 가능성도 있음.
미리 정수형 해쉬값을 저장해두어 사용하면 문자열을 해싱하는 과정을 반복해서 하지 않아도 됨. 
``` cs
int animPropHash;
animPropHash = Animator.StringToHash("AnimPropName");```

참고:  [일반 최적화 - Unity 메뉴얼](https://docs.unity3d.com/kr/2021.3/Manual/BestPracticeUnderstandingPerformanceInUnity7.html)