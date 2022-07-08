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


# 외부 호스팅 
- 컴퓨터가 아닌 외부 디바이스(폰, 태블릿 등)에서 접속하고 싶은 경우 외부에서 로컬로 접속할 수 있도록 해 주어야 함 
- 이를 위해 `ngrok`을 사용 함 
### 1. 구글에서 `ngrok`을 검색 하고 공식 사이트에서 `download`선택, windows(64-bit)용 zip 파일을 다운 받음 
### 2. `ngrok-v3-stable-windows-amd64.zip`의 이름으로 파일이 다운받아 지며 압축을 품 
### 3.압축을 풀게 되면 `ngrok.exe` 파일이 생겨나며 이를 실행
  - 이 파일을 실행 시키면 아래와 같은 화면이 나오는데 `추가정보` -> `실행`을 누르게 되면 그 다음 화면이 나타나게 됨 
![image](https://user-images.githubusercontent.com/92499881/177932166-3508ff1d-2d27-41cd-aa75-bd896519313d.png)![image](https://user-images.githubusercontent.com/92499881/177932241-54731e51-3ef6-4278-832c-238066226762.png)

### 4. 외부 호스팅 
```
ngrok http 5000 
```
ngrok 창에서 위 코드를 입력하게 될 경우 외부에서 접속할 수 있는 링크가 생성 됨 

`Forwarding` 에 있는 `https://1256-115-143-94-231.jp.ngrok.io`의 형태의 링크로 접속을 하게 되면 어떤 디바이스에서도 해당 로컬 호스트로 접속할 수 있음 

