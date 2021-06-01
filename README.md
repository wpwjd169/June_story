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
