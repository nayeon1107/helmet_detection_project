# CNN 알고리즘을 활용한 건설 현장 근로자 안전모 착용여부 인식 모델 개발

### 📂 프로젝트 개요
- 딥러닝 팀 프로젝트
- 인원 : 3명
- 2022.04 ~ 2022.06 (2개월) 진행


  
### 📌 주제 도출 배경
- 산업현장의 재해율이 지속적으로 감소하는 데에 반해 건설현장의 재해율은 점진적으로 증가하는 추세
- 특히 건설업 내 사망재해 심각
- 상해 부위 중 두부 손상으로 인한 경우가 전체의 43% 차지
- 딥러닝을 기반으로 한 안전모 착용 여부 인식 모델을 개발하여 안전모 착용을 검사하는 서비스를 제공하고자 함


![image](https://github.com/nayeon1107/helmet_detection_project/assets/88521667/053cb36f-79fc-4e71-8090-1d3b6f83b6e0)


### 📃 활용 데이터
[AI Hub 공사현장 안전 장비 인식 이미지 소개](https://aihub.or.kr/aidata/33921)

![image](https://github.com/nayeon1107/helmet_detection_project/assets/88521667/d0229e9c-eca7-4426-af3c-f189b349700f)
&nbsp; &nbsp; 전체 데이터 > 안전 보호구 관련 데이터 > 안전모 착용/미착용 이미지만 선별하여 사용

&nbsp; &nbsp; Colab Pro 환경에서 처리할 수 있도록 전체 데이터 Random downsampling 을 통한 개수 조정


### 📊 적용 모델 및 모델별 결과
- CNN
  - Simple CNN
- Pretained Model
  - VGG 16
  - ResNet 50
  - MobileNet 
 ![image](https://github.com/nayeon1107/helmet_detection_project/assets/88521667/be5af3be-9f18-480b-b957-af3072a44a32)

&nbsp; &nbsp; ➡ 정확도 **98.25%** 의 **MobileNet** 채택



### 😀 최종 결과
1) YOLOv5 를 이용하여 전체 사진 중 사람의 머리만을 인식하는 모델을 학습시킨 후
2) MobileNet 모델을 이용하여 안전모 착용 여부를 인식

0 : 안전모 미착용
1 : 안전모 착용
![image](https://github.com/nayeon1107/helmet_detection_project/assets/88521667/908398b5-7898-41d5-9120-31393e31c314)
![image](https://github.com/nayeon1107/helmet_detection_project/assets/88521667/66df6cc2-cd0c-499d-820a-382b9515a873)


### 🔎 개선 및 보완점
- 데이터의 불균형이나 데이터의 잘못된 라벨링 등이 문제점이라 생각
- 이미지 크기에 비해 현저히 작은 사람 머리 인식 크기
- Detection을 보완하여 건설현장에 적용한다면 유의미한 성과가 있을 것
  

### 📚 참고 자료
- Identity Mappings in Deep Residual Networks (Kaiming He 외 3명 , 2016)
- MobileNets: Efficient Convolutional Neural Networks for Mobile Vision Applications (Andrew G. Howard, 외 7명 , 2017)
- VERY DEEP CONVOLUTIONAL NETWORKS FOR LARGE-SCALE IMAGE RECOGNITION (Karen Simonyan ∗ & Andrew Zisserman , 2015)

