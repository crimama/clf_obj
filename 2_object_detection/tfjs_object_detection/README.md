# TFJS Object Detection 
- 해당 파일들은 TFJS 프레임워크 형태로 모델을 web에 deploy하는 것들 입니다
- 과정 역시 다른 것과 마찬가지로 데이터 수집 - 학습 - web deploy 의 과정을 거치며 학습 이후 tfjs 모델로 변형하는 과정이 추가되어 있습니다 
- 학습 파일은 두가지가 있습니다. 첫번째 `tfjs_object_detection`은 Tensorflow 공식 블로그에서 제공하는 코드로 web deploy까지 나타나 있습니다. 
  - 하지만 어떠한 문제 때문인지 정상적으로 동작하지 않았습니다 
- 두번째 `roboflow_tfjs_object_detection`은 roboflow 사이트에서 제공하는 일종의 template 형태의 코드입니다. 모델은 `mobilenet_v2_ssd`를 사용했으며 inference 까지 동작 하는 것은 확인 했습니다. 
