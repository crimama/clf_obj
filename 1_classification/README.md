# Classification 
- 해당 Classification 파트는 크게 데이터 수집(+라벨링) - 모델 학습 - Web적용의 순서를 가집니다 

## 1.데이터 수집 
- [데이터수집 노트북](https://github.com/crimama/clf_obj/blob/main/1_classification/1_Data_Collecting.ipynb)
- 해당 노트북에 주석으로 가이드라인 작성 해 두었습니다 

## 2.모델 학습 
```
💡 데이터 학습에선 2_Classification.ipynb 파일을 사용, ❗코랩 환경에서 진행

- 데이터 수집 과정에서 모은 이미지를 이용해 학습을 진행 함
- Pretrained model 로 mobilnet을 사용 함
- Input 이미지가 Up | Down을 분류하는 모델
- **코드 및 과정 설명은 ipynb 노트북 파일에 주석으로 작성 함**
```

## 3.깃허브 업로드 
[html](https://github.com/crimama/clf_obj/tree/main/1_classification/html)<--폴더에 있는 파일들 사용 
```
💡 웹에서 분류 모델을 실행 시키기 위해서는 4개가 필요 함 
- index.html
- 모델 weights 파일 
- 라벨 json 파일 
- 결과 출력 이미지
```
### 1. Github에 빈 Repositary 생성 
### 2. Repositary를 만든 뒤 로컬에서 Clone
### 3. 파일 복사 
    - 위 html 폴더에 있는 파일을 모두 자신이 만든 Repositary 폴더에 넣음 
    
    `** 매우 중요 : 데이터 학습 단계에서 다운 받은 weights 파일을 mobilenet 폴더에 넣음 
        (이 때 model.json 뿐만 아니라 .bin파일 모두 넣어야 함)** `
### 4. Git push         
    - git push를 이용하여 로컬의 파일들을 github에 업로드 함 
   
## 4. Web page 만들기 (gitpage deploy) 
- 깃허브의 pages 기능을 사용하면 index.html로 webpage를 만들 수 있음 
### 1. pages 만들기 
    - 앞서 push 한 git repositary에서 setting -> pages를 들어 감 
![image](https://user-images.githubusercontent.com/92499881/177718930-8b353c2f-09fc-4fab-9563-6a8fe19ee645.png)

### 2. Source 지정 
    - Source 탭에서 main -root로 설정하고 save를 누름 
![image](https://user-images.githubusercontent.com/92499881/177719106-88cb9a9e-dfe2-42e4-8227-d1259c6541fe.png)
### 3. Web page 링크 확인 
    - Save를 누를 경우 자동으로 Webpage 링크가 생성 됨 
    ![image](https://user-images.githubusercontent.com/92499881/177719249-a04d1d49-34e5-4d1e-996a-b851ae4c61a6.png)
    - 다만 웹페이지 링크가 생성 되더라도 바로 보여지지는 않음 (웹페이지 생성을 위한 시간 필요) 
    - 웹 페이지가 생성 완료됬을 경우 code 탭 오른쪽 하단에 다음과 같은 표시가 뜸 
    ![image](https://user-images.githubusercontent.com/92499881/177719476-77bbb1ab-a889-4eff-98de-2764cef6af05.png)
### 4. Web page 실행 
![image](https://user-images.githubusercontent.com/92499881/177719620-2b41e617-7fd2-4641-8e15-4e0090685d67.png)
- 상단에는 웹캠이 실시간으로 실행 되며 Capture를 누르면 사진이 찍힘 
- 왼쪽 하단에 찍힌 사진이 출력 되며 이 사진이 input image가 되어 분류 모델이 실행 됨 
- 분류 결과에 따라 Up 또는 Down 이미지가 출력 됨 
