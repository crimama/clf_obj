# Flask-Yolov5-Object Detection 
Flask 웹 프레임 워크와 Yolov5 Object detection 모델로 만든 simple web deploy 입니다. 

## Requirements ##
```
pip install -r requirements.txt
```

## Running ##
### 1. 학습 모델 
- 이전 단계 Yolov5에서 학습한 `best.pt`모델을 yolov5 폴더 안에 저장 
### 2. 경로 설정 
- 아나콘다 프롬프트를 실행 시킨 후 경로를 flask-video-stream으로 설정 
```
cd clf_obj/2_object_detection/flask_object_detection/flask-video-stream
```
### 3. 실행 
```
python app.py
```
### 4. Webpage에서 확인 
- `app.py`파일을 실행시킬 경우 다음과 같은 ip주소가 나타 남, 이를 아무 웹 브라우저에서 실행 
![image](https://user-images.githubusercontent.com/92499881/177930649-2946251d-79c8-4032-b556-7beca74bf521.png)

