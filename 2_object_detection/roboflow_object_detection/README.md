
# 2. Object Detection

## 파일 구조

<aside>
💡 자세한 파일 설명은 진행 과정에서 설명

</aside>

- html (모델 web 구동 용 폴더)
    - model
    - .atom-live-server.json
    - .tags.
    - index.html
    - scropt.js
    - styles.css
- thumb (학습용 데이터)
- 1_Data_collecting.ipynb (데이터 수집,로컬환경)
- 2_Classification.ipynb (데이터 학습, 코랩환경)

## 진행 과정

### 1. 데이터 수집

<aside>
💡 - 노트북에는 코랩 용, 로컬 용으로 두개의 코드가 있습니다 
- 로컬 용은 참고 용 입니다.

</aside>

- **1_Data_Collecting.ipynb**를 코랩 상에서 실행
- 따로 환경설정은 필요 없으며 **디렉토리 설정** 과 **이미지 캡쳐 - 코랩용**을 실행 시키면 아래와 같은 창이 나타남

![Untitled](%E1%84%80%E1%85%A1%E1%84%8B%E1%85%B5%E1%84%83%E1%85%B3%E1%84%85%E1%85%A1%E1%84%8B%E1%85%B5%E1%86%AB%20d1bde4dd18784d6e8ee2d7ed99a53ef9/Untitled%2010.png)

- Capture 버튼을 누르면 미리 선언한 **file_path** 에 저장 됨

### **2. 데이터 라벨링**

<aside>
💡 Object Detection은 이미지 속 **객체의 라벨링(Annotating)**이 필요 함 
다양한 라벨링 툴이 있으며 이번 과정에서는 **“Roboflow**”를 활용 함

</aside>

1. **Roboflow 가입 및 로그인** 
2. **새 프로젝트 생성** 

![Untitled](%E1%84%80%E1%85%A1%E1%84%8B%E1%85%B5%E1%84%83%E1%85%B3%E1%84%85%E1%85%A1%E1%84%8B%E1%85%B5%E1%86%AB%20d1bde4dd18784d6e8ee2d7ed99a53ef9/Untitled%2011.png)

![Untitled](%E1%84%80%E1%85%A1%E1%84%8B%E1%85%B5%E1%84%83%E1%85%B3%E1%84%85%E1%85%A1%E1%84%8B%E1%85%B5%E1%86%AB%20d1bde4dd18784d6e8ee2d7ed99a53ef9/Untitled%2012.png)

1. **selct folder를 누르고 앞선 과정에서 캡쳐한 이미지 폴더(thumb/cup)선택** 
    
    ![Untitled](%E1%84%80%E1%85%A1%E1%84%8B%E1%85%B5%E1%84%83%E1%85%B3%E1%84%85%E1%85%A1%E1%84%8B%E1%85%B5%E1%86%AB%20d1bde4dd18784d6e8ee2d7ed99a53ef9/Untitled%2013.png)
    
2. **이미지 업로드 후 Finish Uploading 누른 후 Assign Image 선택** 
    
    ![Untitled](%E1%84%80%E1%85%A1%E1%84%8B%E1%85%B5%E1%84%83%E1%85%B3%E1%84%85%E1%85%A1%E1%84%8B%E1%85%B5%E1%86%AB%20d1bde4dd18784d6e8ee2d7ed99a53ef9/Untitled%2014.png)
    
3. **박스 Annotating 진행** 
    - 아래 창에서 이미지를 선택 하면 Annotate할 수 있는 창이 뜸
    - 모든 이미지를 다음과 같이 박스를 그려 줌
    - Annotate를 모두 완료 했으면 **오른쪽 상단의 Add images to Dataset 클릭**
    - Train - Valid - Test 비율 조절한 뒤 **Add Images** 클릭

![Untitled](%E1%84%80%E1%85%A1%E1%84%8B%E1%85%B5%E1%84%83%E1%85%B3%E1%84%85%E1%85%A1%E1%84%8B%E1%85%B5%E1%86%AB%20d1bde4dd18784d6e8ee2d7ed99a53ef9/Untitled%2015.png)

![Untitled](%E1%84%80%E1%85%A1%E1%84%8B%E1%85%B5%E1%84%83%E1%85%B3%E1%84%85%E1%85%A1%E1%84%8B%E1%85%B5%E1%86%AB%20d1bde4dd18784d6e8ee2d7ed99a53ef9/Untitled%2016.png)

1. **Generate Dataset** 
    - Generate 탭에서 전처리 진행할 요소 선택
    - Resize, Augmentation 등 선택 가능

![Untitled](%E1%84%80%E1%85%A1%E1%84%8B%E1%85%B5%E1%84%83%E1%85%B3%E1%84%85%E1%85%A1%E1%84%8B%E1%85%B5%E1%86%AB%20d1bde4dd18784d6e8ee2d7ed99a53ef9/Untitled%2017.png)

![Untitled](%E1%84%80%E1%85%A1%E1%84%8B%E1%85%B5%E1%84%83%E1%85%B3%E1%84%85%E1%85%A1%E1%84%8B%E1%85%B5%E1%86%AB%20d1bde4dd18784d6e8ee2d7ed99a53ef9/Untitled%2018.png)

1. **Export Dataset** 
    - 여기서 만든 이미지와 Annotate를 사용하기 위해선 모델에 맞는 형태로 출력 필요 함
    - 우리가 사용할 형태는 Tensorflow TFRecord
    - Export를 누른 뒤 Format으로 **Tensorflow TFRecord**를 선택, 그 후 Continue 클릭
    - 다운로드 유형은 **show download code** 선택

![Untitled](%E1%84%80%E1%85%A1%E1%84%8B%E1%85%B5%E1%84%83%E1%85%B3%E1%84%85%E1%85%A1%E1%84%8B%E1%85%B5%E1%86%AB%20d1bde4dd18784d6e8ee2d7ed99a53ef9/Untitled%2019.png)

![Untitled](%E1%84%80%E1%85%A1%E1%84%8B%E1%85%B5%E1%84%83%E1%85%B3%E1%84%85%E1%85%A1%E1%84%8B%E1%85%B5%E1%86%AB%20d1bde4dd18784d6e8ee2d7ed99a53ef9/Untitled%2020.png)

![Untitled](%E1%84%80%E1%85%A1%E1%84%8B%E1%85%B5%E1%84%83%E1%85%B3%E1%84%85%E1%85%A1%E1%84%8B%E1%85%B5%E1%86%AB%20d1bde4dd18784d6e8ee2d7ed99a53ef9/Untitled%2021.png)

- ~~위 이미지와 같은 형태로 Raw URL 링크가 생성 되며 학습 과정 중 이를 사용할 것임~~
- Roboflow 자체 Training tool을 사용할 것이므로 따로 저장하지 않고 바로 다음으로 진행

### 3**. 데이터 학습**

<aside>
💡 - Roboflow의 자체 Training 기능을 사용 함

</aside>

1. **Training**                                                                                                                                       
    - 업로드 한 이미지의 Annotating (라벨링)이 모두 종료가 되면 아래와 같이 **Start Training**버튼이 활성화 됨, 해당 버튼을 클릭
2. **Fast or Accurate 중 원하는 것 선택**                                                                                                

![Untitled](%E1%84%80%E1%85%A1%E1%84%8B%E1%85%B5%E1%84%83%E1%85%B3%E1%84%85%E1%85%A1%E1%84%8B%E1%85%B5%E1%86%AB%20d1bde4dd18784d6e8ee2d7ed99a53ef9/Untitled%2022.png)

![Untitled](%E1%84%80%E1%85%A1%E1%84%8B%E1%85%B5%E1%84%83%E1%85%B3%E1%84%85%E1%85%A1%E1%84%8B%E1%85%B5%E1%86%AB%20d1bde4dd18784d6e8ee2d7ed99a53ef9/Untitled%2023.png)

1. **Train 방법 선택** 
    - 해당 항목은 학습을 처음부터 진행할 지 혹은 기존에 학습된 것을 이용해 학습할 지를 선택하는 항목
    - **Start from a Checkpoint -COCOv6n** 을 선택 후 **Start Training** 선택
    
    ![Untitled](%E1%84%80%E1%85%A1%E1%84%8B%E1%85%B5%E1%84%83%E1%85%B3%E1%84%85%E1%85%A1%E1%84%8B%E1%85%B5%E1%86%AB%20d1bde4dd18784d6e8ee2d7ed99a53ef9/Untitled%2024.png)
    
- Start Training을 선택하게 되면 자동으로 학습이 진행 됨

### 4. Web browser 구동

- Roboflow 상에서 모델이 학습 종료되면 아래 이미지 처럼 학습 된 모델을 사용할 수 있는 선택지가 나타남
- 여기서 **Use your webcam 선택**
    
    ![Untitled](%E1%84%80%E1%85%A1%E1%84%8B%E1%85%B5%E1%84%83%E1%85%B3%E1%84%85%E1%85%A1%E1%84%8B%E1%85%B5%E1%86%AB%20d1bde4dd18784d6e8ee2d7ed99a53ef9/Untitled%2025.png)
    
- **Use your Webcam** 선택 시 아래 창 처럼 나타나며 web에서 바로 Object Detection이 구동 됨

![Untitled](%E1%84%80%E1%85%A1%E1%84%8B%E1%85%B5%E1%84%83%E1%85%B3%E1%84%85%E1%85%A1%E1%84%8B%E1%85%B5%E1%86%AB%20d1bde4dd18784d6e8ee2d7ed99a53ef9/Untitled%2026.png)

![Untitled](%E1%84%80%E1%85%A1%E1%84%8B%E1%85%B5%E1%84%83%E1%85%B3%E1%84%85%E1%85%A1%E1%84%8B%E1%85%B5%E1%86%AB%20d1bde4dd18784d6e8ee2d7ed99a53ef9/Untitled%2027.png)

- 이를 javascript 와 html 파일로 저장할 수 있음
- 오른쪽 상단에 보면 **Get Code** 버튼을 누르게 되면 창이 뜨고 **Download Sample App** 버튼이 활성화 됨
- 이를 클릭하게 되면 html, css, js 파일이 압축되어 있는 파일이 다운로드 됨

### 5. Publishing (Github page 이용)

- html 파일을 publishing 하기 위해 github의 page 기능을 활용 함
- 아래 과정은 Classification에 있는 과정과 동일

### 이슈 사항

- 웹캠으로 촬영한 이미지로 Object Detection 모델을 만들고 이를 Web browser에서 구동하는 방법을 찾았습니다.
- 하지만 이는 직접 코랩에서 학습하지 않고 roboflow 사이트의 자동 학습 기능을 사용합니다
    
    > **Object Detection - 진행 과정 - 3.데이터 학습 참고**
    > 
    
    해당 학습이 종료된 후 web browser deploy 기능을 사용하면 html-js-css 파일을 다운 받을 수 있고 이를 이용해 Web browser 에서 구동시킬 수 있습니다. 
    
- 원래 기획은 코랩에서 모델을 학습 시키고 이를 html 과 js를 이용해 웹에서 구동하는 것이었습니다
- 그래서 roboflow 사이트에서 다운 받은 js 코드를 확인했고 roboflow 서버에서 api 형태로 모델을 읽어오는 형태를 갖고 있습니다.
- roboflow 서버에서 모델 파일을 읽어오는 것이 아니라
