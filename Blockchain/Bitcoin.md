# bitcoin

"bitcoin은 **탈 중앙화** 디지털 화폐이다"

- 순수한P2P 기반의 전자현금은 **금융기관을 거칠 필요** 없이 개인간의 **직접적인 화폐전송**을 통한 온라인 결제가 가능하게 한다

 

중앙화 || 탈 중앙화  

## Bank

1. 계좌 및 신원 관리

 2. 입출금&송금 중계		 // 은행을 신뢰하기 때문에

 3. 장부관리				//거래장부를 은행에서 어떻게 관리를 하는가//은행의 데이터베이스에 장부가 저장 되어있다.

    - 위의 세가지가 있어 
``` 
  - 화폐 가치에 대한 신뢰성(국가에 의해 보장)
    
  - 사용자에 대한 신뢰성(계좌에 대체적으로 본인만 접근 및 운용)
    
  - 거래&장부 에 대한 신뢰성
```



## Bitcoin

"기술이 보장하는 통화 시스템 "

1. 화폐 가치

   * Bitcoin 취득 방법
     * 트랜잭션인증에 대한 대가로 Bitcoin을 받는가.
     * 거래소 등을 통해 실물화폐를 주고 Bitcoin을 구매한다
     * Bitcoin 소유자에게 현물을 판매하고 그에 대한 대가로 상응하는 Bitcoin을 받는다  //희소성을 갖게 된다.정확한 근거가 되지 못함
   * Bitcoin 총 발행양의 제한
     * 생성된 블록번호에 맞춰 발행된 Bitcoin의 수가 정확하게 제한된다.
     *  모든 채굴이 다 끝났다면, 채굴에 대한 보상은 받을 수 없게 된다 . 
     * 마이닝 속도 제한
     * 발행 차수에 따른 보상 감소
     * 모든 발행 이후부터는 수수료로 마이닝 보상 지급
     * 가격이 높게 측정 되는 이유
       * 이용자 수가 많다

2. 사용자 인증

   

   ### Bitcoin 의 사용자 접근

   : 계좌는 본인만 접근 및 운용할 수 있다.

- 개인키(private Key)

  - 쉽게 생성이 가능하지만 현실적으로 중복된 개인키를 가질 확률은 거의 존재하지 않는다.
  - 공개된 public key를 통해 역추적이 불가하다. (hash함수의 비가역성)

- 공개키(Public Key)

- 주소(address)

- 주소(wallet) : 개인키를 관리하기 위해 사용

  

3. 거래&장부 신뢰

   

- 특정 트랜잭션(송금 내용)을 자신 개인키로 해싱한다 그러면 특정한 값(암호화된 값)이 나온다 // UTXO(Unspent Transaction Output : UTXO에 남은 잔금 이상의 금액은 송금이 불가하다.)

  이것이 여러 사람에게 퍼진다(인증 노드들에게 공표).

  - 노드들은 트랜잭션 풀 내에서 인증가능한 트랜잭션들을 선별해 블록화 하여 공표한다.

  *  Node들은 코인 거래 내용의 처음부터 끝까지 하나하나 맞는건지 검증한다.

  이 값을 잡아서 공개키로 디크립터 해서 나에게 맞는지 확인한다(해싱을 하게 되면 데이터가 떨어진다) 그럼 그 데이터가 나와 동일한지 확인한다..

- 블록체인의 내부 구조상 각 블록은 이전블록의 거래내역을 가지고 있고 모든 인증 노드가 같은 정보를 가지고 있기 때문에 위.변조가 힘들다

- Bitcoin = 내가 거래한 기록이 모두 정확하게 기록된다. 

  -  개수가 정해져 있고 다 이어져 있어서 허위발행 자체가 되지 않는다
  - 다른 사람의 Bitcoin 사용 = 다른 사람의 개인키를 알아야 하는데 알 수 없으니 안된다

- POW : 거래 내역 조작을 통해 중복사용을 하려면 검증하는 컴퓨터를 내 편으로 만들어야 한다.

    랜덤 한 수를 만들다가 타겟 값보다 현 블록 해시 값이 더 작아야 한다

  - 작업을 증명하기 위해서 높은 컴퓨팅 파워가 필요하고 현실적.물리적인 장벽이 생긴 것 이다.
  - **유적존재**: 많은 사람들이 모여 신적이라고 부르기 때문에 많은 사람들이 모여 있다면 더욱 높은 수준이 된다

- 이중지불 

  - 생성속도가 미묘하게 차이 나기도 하지만 The longest chain wins 라고 가장 긴 체인이 이기는 걸로..			
  - 뭐가 맞는지 상관 안 한다. 가장 긴 걸 맞는 거라고 할거야!

 

### issues



#### 수수료란?

채굴자들이 채굴하는 이유는 (작업증명을 하는 이유는) Bitcoin이 리워드로 나오기 때문이고 채굴할 수 있는 양이 정해져 있어서.

#### Bitcoin의 정체성

  채굴 뿐만 아니라 돈을 주고 산다면 정체성에 있어 맞지 않다. 700만원이라는 가치가 있는 것 인가..?

#### 여러 Bitcoin 회사가 있는데 hash함수를 다같이 사용하니까

  비트코인을 갖고 비지니스 하는 경우 - 채굴장, 거래소의 수수료, 하드월넷이라고 지갑이 있다, 

#### Bitcoin은 다수보다 적은 사람들의 많은 돈으로 가치가 올라간게 아닌가.. 

시장논리에 적할수 있다. 구매자는 많고 물주는 있기 때문에 화폐의 가치를 보장할 수 없다

#### 해시함수에 대해...



## Reference

``` 
https://bitcoin.org/bitcoin.pdf

https://bitcoin.org/en/developer-documentation

https://drive.google.com/file/d/1UEWKg2BQcO5jLCwf7U7LGYfkkcTNf4F-/view

https://steemit.com/kr/@loum/kt  
```
