# Collaborative Filtering(협업필터링)
### 협업필터링이란?
    - 많은 사용자들로부터 얻은 기호정보에 따라 사용자들의 관심사들을 자동적으로 예측하게 해주는 방법

### Neighborhood-based Collaborative Filtering
    - Memory-based Collaborative Filtering라고도 부름
    - User-Item간의 평점 등 주어진 데이터로 새로운 아이템을 예측
    - Model-based CF에 비해 계산량이 적음
    - 새로운 user, item이 추가되더라도 비교적 안정적
    - 새로운 content(user 또는 item)를 추천할 수 있음

    📌 User-based Collaborative Filtering
        - 취향이 비슷한 사용자끼리의 데이터를 바탕으로 추천
        - SNS 친구 추천 등에서 활용
        - Regression vs Classification
            - 평점 등 점수 분포가 연속일 때와 이산형일 때 나눠서 적용
            - 평점 등 점수를 정규화하여 추천알고리즘에 적용(Mean-Centering, Z-score normalization)

    📌 Item-based Collaborative Filtering
        - 아이템과 아이템 사이의 유사도 계산
        - 여러 사용자의 과거 선호도 데이터로 연관성이 높은 아이템을 찾고, 해당 아이템을 사용자에게 추천함
        - 아마존, 넷플 등

    📌 User-based vs Item-based Collaborative Filtering
        - 정확도
            - User 수 < Item 수 : User-based
            - User 수 > Item 수 : Item-based
        - 모델 Robustness
            - 유저와 아이템이 얼마나 자주 많이 변하는지에 따라 다름
            - 아이템 수가 크게 변하지 x -> Item-based
        - 설명력
            - Item-based는 비슷한 item과 가중치로 함께 설명 o
            - User-based는 특정 user와 비슷한 user로 분류된 user의 실제 취향을 알 수가 없기 때문에 어려움
        - 새로운 추천 가능
            - Item-based는 과거 아이템 데이터에 의존하기 때문에 어려움
            - USer-based는 여러 유저의 데이터를 보기 때문에 더 새로운 추천이 가능함
        - Cold-start 문제 -> 딥러닝 기반 추천알고리즘
            - 충분한 데이터가 없다면 좋은 추천 불가능
            - 유저에 대한 기록이 x or 새로운 아이템 정보 x -> 추천 불가능
        - 계산량
            - 데이터가 많아질수록 유사도 계싼이 많아지지만 추천 품질이 좋아짐
        - Long-Tail Economy -> 모델 기반 협업필터링
            - 대부분의 사용자가 관심 갖는 소수 아이템으로 쏠림 현상
            - 관심이 상대적으로 부족한 아이템은 추천x

### 유사도
    📌 자카드 유사도(Jaccard Similarity)
        - 집합의 개념을 이용한 유사도 계산
        - 집합 A와 B 사이의 유사도는 교집합으로 판단
    
    📌 피어슨 유사도(Pearson Similarity)
        - Vector X, Y 사이의 상관관계 계산
        - 각 Vector의 표본평균으로 각 vector를 정규화하고, 코사인 유사도를 구함

---------------


#### 📖 참고 사이트 및 강의
- 패스트캠퍼스 : 딥러닝을 활용한 추천시스템 구현 올인원 패키지 Online.  
- [협업 필터링](https://ko.wikipedia.org/wiki/%ED%98%91%EC%97%85_%ED%95%84%ED%84%B0%EB%A7%81)

---------------