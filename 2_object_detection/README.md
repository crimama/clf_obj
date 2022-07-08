# Object Detection 
```
- Object Detection 은 Web Deploy 방식 + 모델 학습 방식에 따라 3가지로 나뉘어 있습니다 
- 데이터 수집 및 Annotating(라벨링)과정은 동일합니다 
```
# 1. 데이터 수집 및 Annotating 
- [데이터 준비](https://github.com/crimama/clf_obj/tree/main/2_object_detection/Data_Preparing)
- 해당 디렉토리에서 데이터 수집 및 Annotating 가이드라인 작성 되어 있습니다

# 2.모델링 및 Web Deploy 

1. [flask_object_detection](https://github.com/crimama/clf_obj/tree/main/2_object_detection/flask_object_detection)
    - 모델은 Yolov5를 사용했으며 web deploy를 위해 flask 와 ngrok를 사용하였습니다 
2. [tfjs_object_detection](https://github.com/crimama/clf_obj/tree/main/2_object_detection/tfjs_object_detection)
    - 모델은 Tensorflow 의 mobilenet_ssd_v2를 사용했으며 web deploy를 위해 JavaScript를 사용하였습니다. 
    - Tensorflow 가이드라인을 참고하였습니다. 
3. [roboflow_object_detection](https://github.com/crimama/clf_obj/tree/main/2_object_detection/roboflow_object_detection)
    - 이 방법은 코랩에서의 데이터 수집을 제외한 모든 과정을 roboflow 플랫폼에서 진행합니다 
    - 모델 학습 또한 roboflow에서 진행 됩니다 
    - 교육 과정의 취지와는 맞지 않다고 생각 되지만 우선은 정리 및 추가 해 두었습니다. 

