# 객체지향의 사실과 오해 : PART 4

### 책임

객체의 책임은 *‘객체가 무엇을 알고 있는가 (knonwing)’* 와 *‘무엇을 할 수 있는가(doing)’* 로 구성된다.

- *하는 것 (doing)*
    - 객체를 생성하거나 계산 하는 등의 스스로 하는 것
    - 다른 객체의 행동을 시작시키는 것
    - 다른 객체의 활동을 제어하고 조절하는 것
- *아는 것 (knowing)*
    - 개인적인 정보에 관해 아는 것
    - 관련된 객체에 관해 아는 것
    - 자신이 유도하거나 계산할 수 있는 것에 관해 아는 것

객체의 책임을 이야기할 때는 일반적으로 외부에서 접근 가능한 공용 서비스의 관점에서 얘기한다. 즉, 책임은 객체의 외부에 제공해줄 수 있는 정보(knowing) 와 외부에 제공해줄 수 있는 서비스(doing)의 목록이다. 따라서 책임은 **객체의 공용 인터페이스(public interface)를 구성**한다.

객체가 다른 객체에게 주어진 책임을 수행하도록 요청을 보내는 것을 **메시지 전송(message-send)** 라고 한다. 책임과 메시지의 수준이 같진 않다. 책임은 단지 객체가 협력에 참여하기 위해 수행해야 하는 행위를 상위 수준에서 개략적으로 서술한 것일 뿐이고, 협력을 정제할 때 **책임은 여러 메시지로 분할**된다.

---

### 역할

어떤 객체가 어떤 책임의 집합을 수행하는 것을 우린 **역할**이라고 한다. 역할은 재사용이 가능하며 객제치향 설계를 낳는 매우 중요한 구성요소이다. 

역할은 협력 내에서 다른 객체로 대체할 수 있음을 나타내는 일종의 표식이다. 즉 협력 안에서의 역할은 *“이 자리는 해당 역할을 수행할 수 있다면 어떤 객체라도 대신할 수 있습니다”* 라는 말과 같다.

물론 해당 역할을 수헹할 수 있는지에 대한 여부는 각 역할이 수신할 수 있는 메시지를 동일한 방식으로 이해할  수 있는지에 달렸다. 동일한 역할을 수행하는 객체들이 동일한 메시지를 수신할 수 있고 이에 맞는 동일한 책임을 수행할 수 있기 때문이다.

역할은 협력 안에서 구체적인 객체로 대체될 수 있는 추상적인 협력자로써, **본질적으로 다른 객체에 의해 대체 가능함**을 의미한다. 

---

### 객체의 모양을 결정하는 협력

시스템에 필요한 데이터를 저장하기 위해 객체가 존재한다는 선입견은 옳지 않다. 객체가 갖는 상태의 일부는 행위를 수행하기 위한 재료일 뿐이며, 존재 이유는 **행위를 수행하며 협력에 참여하는 행동(책임)**에 있다.

올바른 객체 설계를 위헤서는 무엇보다 먼저 견고하고 깔끔한 협력을 설계해야 한다. 이는 설계에 참여하는 객체들이 주고 받을 요청과 응답의 흐름을 결정하는 것을 의미하고, 이들은 객체가 협력에 참여하기 위한 책임이 된다.

---

### 객체지향 설계 기법

> **책임-주도 설계(Responsibility-Driven Design)**
> 

협력에 필요한 책임들을 식별하고 적합한 객체에 책임을 할당하는 방식

> **디자인 패턴(Design Pattern)**
> 

반복적으로 사용하는 해결 방법을 정의해놓은 설계 템플릿의 모음

> **테스트-주도 개발(Test-Driven Development)**
> 

테스트를 먼저 작성하고 테스트를 통과하는 구체적인 코드를 추가하는 방식