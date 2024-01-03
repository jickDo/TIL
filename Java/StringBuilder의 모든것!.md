# StringBuilder 톺아보기 

---

오늘 공부한 내용은 StringBuilder에 대한 내용이다. 최근 String의 메서드나 String그 자체의 불변성, String constant pool같은 메모리 사용 부분에 대해서
공부를 했었다. 알고리즘을 공부를 하다보면 문자열을 사용할 경우가 많고, 그러다 보면 의도치 않게 메모리를 많이 잡아 먹는데 그것을 해결해줄 대안으로 StringBuilder를 공부하게 되었다.


<br><br>

## StringBuilder란?

---

>A mutable sequence of characters.
>This class provides an API compatible with StringBuffer, but with no guarantee of synchronization.
>This class is designed for use as a drop-in replacement for StringBuffer in places where the string buffer was being used by a single thread (as is generally the case).
>Where possible, it is recommended that this class be used in preference to StringBuffer as it will be faster under most implementations.

위 문장은 StringBuilder.java의 공식문서의 가장 최상단 설명이며, 그 설명은 
> '문장은 변경가능 하며, 동기화가 보장되지 않는 StringBuffer이다'
> 
> 또한, 단일 스레드 에서 StringBuffer의 대체 목적으로 설계 되어 대부분의 경우는 StringBuffer보다 빠르다는 점을 말한다.

쉽게 요약하자면 String클래스를 변경가능 하고 추가 데이터를 잡아먹지 않는 방식의 변경을 가할수 있으며, StringBuffer의 멀티스레드 환경에서
대채제로 개발되어 왠만한 환경은 StringBuilder가 빠르다는 점을 말하고 있다.

**알고리즘 문제는 속도와 메모리 사용의 중요성이 있기 때문에 왠만해서는 String을 변경하게 된다면 StringBuilder를 사용해야 할것같다.**


<br>

또한 한가지 특징으로

> Every string builder has a capacity.
>As long as the length of the character sequence contained in the string builder does not exceed the capacity, it is not necessary to allocate a new internal buffer. 
> If the internal buffer overflows, it is automatically made larger.

위 문장은 스트링 빌더의 용량이 정해져있고, 이를 초과하면 그때서야 추가 용량을 자동으로 할당받는 점을 말하고 있다.

<br><br>

##







