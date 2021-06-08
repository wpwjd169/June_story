# June_story
6월의 이야기 -  final 프로젝트 관련


-----------------------------------------------
6월 1일<br>
<br>
두 달의 파이널 테스트가 이제 진행되어가고 있다. 물론 저번주부터 계획을 하고 진행하고 있지만 연결해주는 역할을 주로 맡다보니 아직은 준비하는 기간이 생겼다.<br>
우선적으로 DB와 Java를 연결하는 로직 부분을 모두 구성해야 하고 동시에 servlet을 이용해서 웹과도 연결을 해줘야 하기 때문에<br>
지금은 업무가 확실히 시작하기 전에 탄탄히 어떤 방식으로 진행되는지 알아야한다.<br>

- 우선은 순수자바(POJO) 방식으로 servlet과 jsp를 연결 시키는 방법 + mybatis도 직접관리하는 방법을 뜯어보자 (이걸 POJO 1-1 과정이라고 하자.)<br>
- 두 번째는 순수자바(POJO) 형식에서 뿌려주는 controller를 하나 더 만들어서 각각의 필요한 것을 조건에 맞게 진행하도록 연결하자(POJO 1-2 과정)<br>
- 세 번째는 이 과정에서 @(어노테이션)으로 연결해서 더욱 간추려서 진행해보도록 하자.(POJO 1-3 과정)<br>
- 마지막은 Mybatis에서 VO가 아닌 Map으로 집어 넣어서 가져올 때 조건값을 가져오는 방법(물론 cursor의 방향이 중요)으로 만들어보자.
```
순수자바가 익숙해지면 바로 Spring의 방식으로 연결하는(Dispatcher 방식) 과정을 진행하자.
```
*현재 생각하는 6월 첫째 주 예상 복습 과정*

------------------------------------------------
6월 2일<br>
현재까지 Pojo방식을 mybatis를 이용해서 쿼리를 읽어서 값을 받아오는 것을 다시 만들고 뜯어서 확인해보았다. 프로젝트 과정에서 나중에는 Spring으로 이관작업하지만 <br>
우선 mybatis를 제대로 사용하지 않았다보니 방식을 몰랐다. 가장 중요한 점은 mapper를 통해서 mybatis를 찾아서 그 쿼리를 진행하는 방식이고 그 이전에 properties 등에 <br>
정보를 등록하고 읽어오는 방식으로 전개되야 하는 점이다. 확실히 DB에서 간단히 시스템 시간을 읽어오도록 하는 것을 봤지만, 프로젝트에서 객체 방식으로 값을 받는 것이<br>
아니라 Map을 통해서 특정 값만 받도록 해야하는데 아직 Map에 put하기 위해 어떤 틀로 만들어야 하는지 모르겠다. getter,setter 방식으로 한다면 vo클래스를 하나 만들어서<br>
간단히 받을 수 있지만 내일은 Map으로 받는 법을 찾아봐야 할 듯하다.
```
 -가정 1 : Mybatis를 호출하는 공통 클래스에서 Map을 리턴타입으로 하는 메소드로 진행해야 할까?
 -가정 2 : Mybatis를 실행하는 mapper에서 hashMap으로 returnType을 선언해서 이를 받아오는 클래스를 인식시켜야 하나?
 -가정 3 : 받을 수 있는 클래스를 만들고 이를 Map으로 그냥 선언하고 파라미터로 dao에서 리턴값을 받고 db에 맞는 것을 put(key, value)형식으로 만들까?
```
이후에 jsp에 따로 스크립트 시트에 호출해야 하는데... 없어도 되는걸까?
만약에 이게 적용이 된다면 Logic을 보내주는 경로를 편리하게 보내 줄거 같은데?? (물론 많아서 답이 없겠지만)

------------------------------------------------
6월 3일
위에 가정에서 말하는 것처럼 결국은 Mybatis에서 연결하는 과정에서 Map을 사용하고 동시에 VO같이 Map으로 받는 java를 하나 만들어서 이걸 Map에 넣는 방식으로 진행하는 것이<br>
맞았다. 그래도 아직은 적응이 되지 않아서 내부를 좀 더 작성하는 법이 안타깝다. 오늘은 문서작업을 진행했다. PM,PL들이 고생하는거에 숟가락 얻는 느낌이 들어서 미안하지만<br>
도움을 요청했고 최대한 도와줘야지 프로젝트가 진행되니까 잠시 멈추고 명세서에 예외처리를 작성했다. 어떤 작동하는 과정에서 반증되어 나타는 오류를 모두 가정해서 적는<br>
것이기에 경험, 스토리를 모두 적었다. 적어서 만족한다는 이야기를 들었으니 몫을 했다는거 아닐까?<br>
수업을 들으면서 슬금슬금 mybatis와 spring의 연결이 이어지기 시작했다. 이제 UI구성도 나타나기 시작했고 연결하는 방법도 점점 늘어날 것으로 감이 오기 시작했다<br>
이제 작성하는 일이 다가오니 더 빨리 기본 베이스를 만들어 놓아야 할 듯하다.

------------------------------------------------
6월 4일 ~ 6월 7일
아주 아팠다.. 아주 많이 먹어서 그런건지 아니면 아주 허겁지겁 먹어서 그런건지 제대로 몸이 아팠다....<br>
잘려고 할 때마다 양팔과 양다리가 찌르는 듯한 느낌으로 계속 건들어서 잠도 제대로 못잤다...<br>
괜찮아지면 다른 부위가 아프니까 정신이 없다.. 몽롱한 기분이 많이 든다..<br>
계속 작업하고 일정 관리 잘해야하는데 어질어질하니까.. 잘 버틸지..
