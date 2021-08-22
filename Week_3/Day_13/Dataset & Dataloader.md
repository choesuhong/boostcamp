# Dataset & Dataloader

---------------------

## 목표

--------------

- [ ] Dataset, Dataloader의 사용하는 방법 알기
- [ ] Batch 단위로 데이터를 로딩하는 방법 알기
- [ ] 각 sampler들을 언제 사용하면 좋을까?
- [ ] 데이터의 크기가 너무 커서 메모리에 한번에 올릴수 없을 경우  어떤식으로 데이터를 불러오는게 좋을까?



## 모델에 데이터를 먹이는 방법

------------

![image-20210823025315754](https://raw.githubusercontent.com/choesuhong/save-image-repo/image/img/image-20210823025315754.png)

1. 초기 데이터 생성 방법을 지정
2. 데이터의 전체 길이
3. index 값을 주었을 때 반환되는 데이터의 형태 (X, y)



## Dataset 클래스 생성시 유의점

---------------

- 데이터 형태에 따라 각 함수를 다르게 정의
- 모든 것을 데이터 생성 시점에 처리할 필요x (ex : **image의 Tensor 변화는 학습에 필요한 시점에 변환**)
- 데이터 셋에 대한 표준화된 처리방법 제공 필요 -> 후속 연구자 또는 동료에게는 빛과 같다
- HuggingFace등 표준화된 라이버러리 사용



## DataLoader 클래스

-------------------------

- Data의 Batch를 생성해준다
- 학습직전(GPU feed전) 데이터의 변환을 책임
- Tensor로 변환 + Batch 처리


