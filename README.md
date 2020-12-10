# G16_coarse_to_fine

# 결론

## 평가문항	상세기준

### 1. mean-shift를 활용하여 눈동자 검출 라벨링 추가작업을 원활히 진행하였다.

- 눈이미지-라벨이미지 쌍의 추가데이터셋을 10000건 이상 충분히 확보하였다.

- 이전 스텝에서 다룬 눈동자 검출 방법을 LFW 데이터셋에 적용하여 필요한 만큼의 데이터셋을 생성해 보았다. 

- 데이터셋을 생성하는 코드 prepare_eye_dataset.py를 실행하면 아래 사용할 데이터셋이 LFW 데이터셋으로부터 가공 생성했다. 


### 2. 눈동자 키포인트 검출 딥러닝 모델이 구현되어 안정적으로 학습이 진행되었다. 

- pretrained model 기반의 딥러닝 모델의 트레이닝 loss가 안정적으로 감소함을 확인하였다.
    - mse = 0.012285141274333 
    - mae = 0.05068657919764519

![learning_result](https://user-images.githubusercontent.com/39249809/101793943-b299b000-3b49-11eb-8448-6d95e494d906.png)

### 3. 모델이 검출한 눈 위치에 당황한 표정효과 눈 이미지를 합성한 이미지를 생성하였다. 

- 사람 얼굴 이미지에서 딥러닝 모델로 눈동자 키포인트를 검출하여 눈 이미지를 자연스럽게 합성한 결과이미지를 생성하였다.

- G14에서 학습한 카메라 앱의 눈에 위치에 ***당황한 표정효과 눈 이미지를 합성*** 해 보았다. 
    - 결과 화일: ./images/***surprise_eye_result.mp4***

- 결과 이미지 2장은 아래에 캡쳐함 

![surprise_eye1](https://user-images.githubusercontent.com/39249809/101793952-b3cadd00-3b49-11eb-9cb8-fb573598f463.png)

![surprise_eye2](https://user-images.githubusercontent.com/39249809/101793953-b4637380-3b49-11eb-8886-a9459c856d9d.png)





