# 추천 시스템(Recommendation System)
### 추천 시스템이란?
    - 사용자(User)와 상품(Item)으로 구성된 시스템으로 특정 사용자가 관심을 가질만한 정보를 추천하는 것
    - 사용자가 정보를 수집하고 찾는 시간을 줄여주는 것을 목적으로 함
    - 온라인 쇼핑몰, 뉴스 추천, 유튜브, 넷플릭스 등에서 사용하고 있음

### 추천 알고리즘의 종류
    📌 Contents-based Filtering(컨텐츠 기반 추천 시스템)
        - 사용자가 과거에 좋아했던 것과 비슷한 아이템을 추천

    📌 Collaborative Filtering(협업필터링)
        - 비슷한 성향 또는 취향을 갖는 다른 유저가 좋아한 아이템을 현재 유저에게 추천
        - Linkedin, facebook과 같은 SNS는 collaboprative filtering을 친구 추천 등에 사용함
        - 간단하면서 정확도가 높은 알고리즘

    📌 Hybrid Recommender System
        - Contents-based Filtering과 Collaborative Filtering의 장단점을 상호보완
        - Cold start(충분한 정보가 없어서 필요한 정보를 얻지 못하는 것)등의 문제를 해결할 수 있음

### 추천 시스템의 평가
    ✔ RMSE(Root Mean Square Error)
        - 평균 제곱근 오차
        - 추정 값 또는 모델이 예측한 값과 실제 환경에서 관찰되는 값의 차이를 다룰 때 흔히 사용하는 측도
        - 예측 대상 값에 영향을 받음
        - 추천 시스템에서 평점 예측을 평가할 때 사용하는 정량적 지표
        - RMSE가 낮다고 해서 추천 시스템이 무조건 좋은 것은 아님

    ✔ NDCG(Normalized Discounted Cumulative Gain)
        - 랭킹 문제에 많이 사용하는 평가 지표
        - Top-N 랭킹 리스트를 만들고, 더 관심있거나 관련성 높은 아이템을 포함하고 있는지 평가
        - 순위에 가중치를 줌, 단순한 랭킹이 아닌 데이터의 성향을 반영하기 위한 지표
        - 1에 가까울수록 좋은 랭킹
        - 연속형 변수, 이산형 변수 모두 계산 가능
        - CG : 관련성 점수(사용자가 추천된 각 아이템을 얼마나 선호하는지)를 합한 값(동일한 비중으로)
        - DCG : 랭킹에 따라 비중을 discount해서 관련성을 계산, 하위권에 penalty 부여
        - NDCG : DGG / IDCG
        (Ideal DCG : 선택된 결과로 가질 수 있는 가장 큰 DCG 값 - rel가 큰 순서대로 재배열한 것에 대해서 DCG를 계산)
        ex) TV나 영화 프로그램 K개를 랭킹순으로 추천

    ✔ Precision at K
        - Top K개의 결과로 Precision(정밀도)를 계산
        - 추천된 결과의 관련 여부에 따라 0 또는 1로 평가
    
    ✔ MAP(Mean Average Precision)
        - 추천 랭킹 또는 검색 결과에 대한 average precision의 평균값 계산
        - 전체 Precision at K에 대한 평균 값
    
    ✔ Recall at K
        - K개 추천했을때, 추천됐어야 하는 item이 몇개 추천되어져 있느냐를 나타내는 값


---------------


#### 📖 참고 사이트 및 강의
- 패스트캠퍼스 : 딥러닝을 활용한 추천시스템 구현 올인원 패키지 Online.  
- NDCG : [갈아먹는 추천 알고리즘[6] 추천 엔진 성능 지표](https://yeomko.tistory.com/32), [Normalized Discounted Cumulative Gain (nDCG) 예제와 코드](https://ride-or-die.info/normalized-discounted-cumulative-gain/)  
- Recall at K : [precision at K, MAP, recall at K](https://ddiri01.tistory.com/321)
- 위키백과 : [추천 시스템](https://ko.wikipedia.org/wiki/%EC%B6%94%EC%B2%9C_%EC%8B%9C%EC%8A%A4%ED%85%9C)


---------------
추천 시스템에 대한 공부 및 다양한 예제, 프로젝트를 진행할 예정임  
20210222 ~ 