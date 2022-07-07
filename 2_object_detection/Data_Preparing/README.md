# 데이터 수집 및 Annotating 
```
- Object Detection을 학습하기 위해선 학습용 이미지와 찾고자 하는 Object의 위치를 알려주는 Annotating 작업이 필요 함 
- 이미지 수집은 Classification과 마찬가지로 코랩에서 진행되며 Annotating 은 **Roboflow** 사이트에서 진행 함 
```
# 1. 데이터 수집 
```
💡 - 노트북에는 코랩 용, 로컬 용으로 두개의 코드가 있습니다 
   - 로컬 용은 참고 용 입니다.
   - 코랩에서 이미지 캡쳐가 모두 종료된 뒤 해당 이미지들을 로컬로 저장해야 함 
```
- [1_Data_Collecting.ipynb](https://github.com/crimama/clf_obj/blob/main/2_object_detection/Data_Preparing/1_Data_Collecting.ipynb) 를 코랩에서 실행 
- 따로 환경 설정은 필요 없으며 **디렉토리 설정**과 **이미지 캡쳐-코랩용**을 실행 시키면 아래와 같은 창이 생성 됨 
![image](https://user-images.githubusercontent.com/92499881/177734669-16c8ad45-6305-4206-a49f-56b1d996c15a.png)
- `Capture` 버튼을 누르면 미리 선언한 `file_path`에 저장 됨 

# 2. 데이터 라벨링 (Annotating) 
```
💡 Object Detection은 이미지 속 **객체의 라벨링(Annotating)**이 필요 함 
   다양한 라벨링 툴이 있으며 이번 과정에서는 **“Roboflow**”를 활용 함
```
1. **Roboflow** 가입 및 로그인 
2. 새 프로젝트 생성 
![image](https://user-images.githubusercontent.com/92499881/177735898-93746709-0d3f-4431-8a9e-7ffc041525fa.png)
![image](https://user-images.githubusercontent.com/92499881/177735964-04d0561a-bd7e-4eb5-a559-edf540283716.png)
3. `Select folder`를 누르고 앞선 과정에서 캡쳐한 이미지 폴더(thumb/cup) 선택 
4. 이미지 업로드 후 우측 상단의 `Finish Uploading`누른 후 `Assign Image`선택 
5. 박스 Annotating(라벨링) 진행 
    - 아래 창에서 이미지를 선택 하면 Annotate 할 수 있는 창이 뜸 
    - 모든 이미지를 다음과 같이 박스를 그려 줌 
    - Annotate를 모두 완료 했으면 **오른쪽 상단**의 `Add images to Dataset`를 클릭 
    - Train- Vadli - Test 비율 조절한 뒤 `Add images` 클릭 
![image](https://user-images.githubusercontent.com/92499881/177736874-31cc6a53-135c-4d0c-a49e-1a912d6d4fbb.png)
![image](https://user-images.githubusercontent.com/92499881/177737128-2bd1e78b-3eb5-4f05-9fcc-b49e38e1d525.png)

6.Generate Dataset 
  - `3-Preprocessing` 과 `4-Augmentation`을 통해서 이미지 전처리를 할 수 있음 
  - 모두 기본으로 선택한 뒤 진행 
  - `5-Generate`에서 `Generate`클릭 후 이미지 데이터 셋 생성 
![image](https://user-images.githubusercontent.com/92499881/177737649-d0f9c2de-1c91-4650-b2e3-47ad169d7adf.png)

7. Export Dataset
    - 만들어진 이미지 데이터 셋을 사용하기 위해 모델에 맞는 형태로 출력할 필요가 있음 
    - 
 
