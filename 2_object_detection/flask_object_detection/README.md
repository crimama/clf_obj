# Flask-Object-Detection 
- Yolov5를 이용해 모델을 학습한 뒤 Flask web framework를 활용해 web에서 모델을 출력 함 

# 1. 모델 학습 
- [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/crimama/clf_obj/blob/main/2_object_detection/flask_object_detection/Object_detection_YOLOv5.ipynb)
 [Object_detection_yolov5.ipynb](https://github.com/crimama/clf_obj/blob/main/2_object_detection/flask_object_detection/Object_detection_YOLOv5.ipynb)
```
  - 모델 학습에는 Yolov5 모델이 사용 됨
  - 모델 학습 과정은 노트북에 주석 참고 
  - 아래 노트북을 코랩에서 실행 
  - 💡학습을 마친 뒤 best.pt를 저장해야 함💡 
```

# 2. Web Deployment 
~~~
[flask-video-stream](https://github.com/crimama/clf_obj/tree/main/2_object_detection/flask_object_detection/flask-video-stream)
```
