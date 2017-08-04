# 4주차 튜터링 로그
## 프로젝트 관련
**내가 만들고 싶은걸 만드는 것이 제일 좋다.** (기술적으로 써먹을 알맹이가 있다면)

몇 개의 예제를 올려준 이유는 이 정도는 만들면 괜찮다고 해서 올린 것.
예제 앱은 간단해 보이지만 대부분 2~3인 정도의 팀 분량.

TODO 앱이 진짜 배울 것도 많고 제일 현실적이다. 예제나 연습 프로젝트를 해볼 수 있는 가장 복잡한 앱 중에 하나. 데이터 관리하는 것이 생각보다 쉽지 않다.

어디가서 iOS 얼마나 할 줄 아는가라는 물음에 대해 TODO나 메모장, 일정관리 정도는 할 줄 안다라고 답하면 그렇다면 기본은 할 줄 안다고 생각한다.

### Realm을 꼭 한번 써보고 싶은데 괜찮은가?
개인 앱이면 모를까 실무에서는 Realm을 쓰는 경우가 많지 않다. 실무는 보수적이여서 스타트업이면 모를까 오래되지 않은 기술을 쉽게 사용하지 않는다.

Realm을 얘기하는 친구들이 많아서 Realm에 대한 튜터님들의 토의가 있었는데 튜터님 네 분 전부 Realm을 권장하고 싶지는 않다고 함

Realm을 쓰고 싶어하는 친구가 있을 수는 있다. 꼭 반대하는 건 아니다. 하지만 굳이 쓰라고 하고 싶지는 않다.

Realm을 쓰면 빠르게 데이터베이스를 구축할 수 있는 장점은 있지만 그 라이브러리를 쓰는 방법 정도 밖에 남는 것이 없고 배울 수 있는 것이 없다. 또 지양하는 이유로는 라이브러리 내부가 변경되면 그런 부분에 의존적으로 영향을 받을 수 밖에 없다.

Realm은 우리가 공부하는 과정에 포함된 부분이 아니기 때문에 튜터들이 문제 해결을 도와주기 어려울 수 있다. 내부에서 오류가 발생한 경우라면 더더욱. 그래서 가급적이면 Realm은 지양하고 대체할 수 있는 방향이 있다면 대체하면 좋을 것.

#### 그럼 Core Data를 추천하는가?
Core Data 역시 엄청 권하기가 조심스럽다. 왜냐면 실무에서도 Core Data가 그렇게 많이 쓰이지 않는다.

그럼 뭘 많이 쓰느냐? 로컬 DB를 사용한다 한다면 SQLite를 많이 쓴다. 아니면 Archiving을 하기도 한다.

UserDefaults, document, cache, temporary folder, Realm 같은 데이터베이스 등 여러가지 저장 공간이 있는데 목적이 다 다르다.

Realm을 쓴다고 해서 다 Realm에 저장하는 것도 아니다. 사진 바이너리 등의 데이터는 document 폴더에 따로 저장하고 사진 주소를 갖고 있는 경우도 있다. 굉장히 다양한 경우가 존재한다. 적재적소에 다양한 방법들을 사용해야 한다.

어떤 정보를 어떤 형태로 저장하고 불러와야할까에 대한 고민을 좀 더 해보면 낫지 않을까라는 튜터님의 생각

무조건 요즘 트렌드의 기술을 갖다 쓰는 것이 내가 발전하는 것은 아니다.

실무에 가면 남이 짠 코드를 봐야할 일도 많고 여럿이 프로젝트를 하는 경우도 많고 그렇다면 부딪히는 경우도 생긴다.

프로젝트를 진행하면서 최대한 서로 같이 해보면서 부딪혀보면 좋을 것이다. 그리고 그런 내용들이 면접에서 할 얘기들이 될 것이다.

## GIT 관련
그리고 Git을 잘 다루는 것은 굉장히 중요하다.

branch를 나누고 tag 달고 뭐하고 뭐하고... 이런 것까지 바라지는 않지만 commit 단위와 commit 메시지에 집중했으면 좋겠다.

우리가 버전관리시스템을 사용하려는 이유는 뭘까? 내가 실수한 부분을 갈아치우고 싶어서. commit은 내가 실수한 부분을 갈아치울 수 있는 단위. 내가 commit한 만큼 되돌릴 수 있다.

commit 단위는 너무 커도 안되겠지만 너무 작아도 안된다. 적어도 내가 일을 취소했을 때 후회하지 않을 정도의 단위여야 한다. 또한 내가 한 줄로 이 코드의 변화를 대부분 설명할 수 있을 정도의 분량이 적절한다. 인터넷에 많은 내용이 참고할 것.

commit 메시지도 내가 작성하는 양식이 있으면 좋다. 정해진 법은 없다. 하지만 commit 메시지를 보고서 내가 작업을 취소해도 무리가 없을 정도의 메시지가 담겨야 한다. 그리고 리뷰할 때 스크롤 몇 번으로 코드 리뷰를 끝낼 수 있는 정도.

commit은 이 코드가 동작할 때 해야한다. 코드를 빌드할 수 없는 상태에서는 commit을 하면 안된다. 나머지는 하면서 차차 익히게 될 것이다.

### Git과 Storyboard
storyboard를 같이 사용하면 분명 conflict가 발생할 것이다. **storyboard reference**에 대한 내용을 잘 찾아보고 참고하면 좋을 것.

## 라이브 코딩 관련
여러 명이서 하면 금방 할 수 있을 것 같아도 혼자 하는 것보다 못한 결과가 나올 수 있다. 커뮤니케이션이 어렵다. 팀으로 프로젝트를 하면 이런 경우는 다반사일 것이다.

1+2법칙? 내가 1의 시간을 예상했으면 이것을 고치고 발전시키는데 2의 시간을 더 넣어라. 내가 만약 이걸 만드는데 1시간이 걸릴 것이라 생각이 되면 최소한 3시간 이상은 예상해야 한다.

코딩 중에 방향적인 문제에 대해서 의문이 들었음에도 불구하고 일을 맡긴 사람에게 물어보지 않은 것은 엄연한 커뮤니케이션의 부재. 이게 쌓이고 쌓이면 분명 크게 돌아온다.

사람끼리 하는 일이기 때문에 사람을 대하는 것 먼저 연습할 필요가 있다. 사람들 끼리의 의사소통 방법도 다 다르고, 표현도 다 다르다. 프로젝트를 함에 있어서도 내 생각을 정확하게 전달하고 이것이 명확히 협의된 상태에서 진행되어야 후에 문제가 덜 생긴다.

3주라는 시간 안에 최대한의 결과를 얻기 위해서는 내 의사소통을 명확히 하고 다른 사람에게 명확하게 작성한 것을 공유할 수 있어야 한다. 그리고 의문이 생기면 바로 해결할 수 있어야 하는 자세도 필요하다.

주어진 과제도 혼자했다면 더 잘할 수도 있다. 하지만 어느 순간이 되면 나혼자 하는 것으로는 더이상 발전되는 느낌이 들지 않을 수 있다. 내 생각에 갇혀버리기 때문. 그렇기에 계속해서 다른 사람의 코드를 보고 생각해보아야 한다. 꼭 내 프로젝트가 아니더라도 다른 사람이 어떤 생각을 하고 있나 들여다보면 좋다.

그리고 실제 프로젝트에 들어가기 전에 사전 조사도 많이하고 새로운 기능을 구현할 때 이런 것들이 필요하겠구나 공부하고서는 시작해보는 것도 좋다.