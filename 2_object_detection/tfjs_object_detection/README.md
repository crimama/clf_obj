# TFJS Object Detection 
- 해당 파일들은 TFJS 프레임워크 형태로 모델을 web에 deploy하는 것들 입니다
- 과정 역시 다른 것과 마찬가지로 데이터 수집 - 학습 - web deploy 의 과정을 거치며 학습 이후 tfjs 모델로 변형하는 과정이 추가되어 있습니다 
- 학습 파일은 두가지가 있습니다. 첫번째 `tfjs_object_detection`은 Tensorflow 공식 블로그에서 제공하는 코드로 web deploy까지 나타나 있습니다. 
  - 하지만 어떠한 문제 때문인지 정상적으로 동작하지 않았습니다 
- 두번째 `roboflow_tfjs_object_detection`은 roboflow 사이트에서 제공하는 일종의 template 형태의 코드입니다. 모델은 `mobilenet_v2_ssd`를 사용했으며 inference 까지 동작 하는 것은 확인 했습니다. 


# 텐서플로우 공식 블로그 object detection 
  [레퍼런스블로그](https://blog.tensorflow.org/2021/01/custom-object-detection-in-browser.html)
  [깃허브](https://github.com/hugozanini/TFJS-object-detection)
  [코드](https://github.com/crimama/clf_obj/blob/main/2_object_detection/tfjs_object_detection/TFJS-object-detection.ipynb)
  

# Roboflow 
  [깃허브](https://github.com/roboflow-ai/tensorflow-object-detection-faster-rcnn)
  [코드](https://github.com/crimama/clf_obj/blob/main/2_object_detection/tfjs_object_detection/roboflow_tfjs_object_detection.ipynb)

# 기타 레퍼런스 
- 구글링을 통해서 찾은 다른 레퍼런스도 아래 추가 해 두었습니다 

[레퍼런스1](https://www.analyticsvidhya.com/blog/2021/12/custom-object-detection-on-the-browser-using-tensorflow-js/)

[레퍼런스2](https://codelabs.developers.google.com/codelabs/tensorflowjs-object-detection#0)

[레퍼런스3](https://medium.com/swlh/build-custom-object-detection-web-application-using-tensorflow-js-d1664f96a18b)
