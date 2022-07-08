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
### 5. 확인 
- 웹브라우저에 IP주소를 입력하게 되면 아래와 같은 화면이 뜸 
- `stream`버튼을 누를 경우 웹캠이 켜지면서 실시간으로 object detection이 실행 됨 


`❗다만 현재 구조 상의 문제로 다소 느림, 추후 보정할 예정` 
![image](https://user-images.githubusercontent.com/92499881/177930753-fc54c71f-ca1e-47d0-835e-78af684530a9.png)

