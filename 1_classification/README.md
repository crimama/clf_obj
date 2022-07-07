# Classification 
- 해당 Classification 파트는 크게 데이터 수집(+라벨링) - 모델 학습 - Web적용의 순서를 가집니다 

## 1.데이터 수집 
- Classification 파트 확인 
- [데이터수집](https://github.com/crimama/clf_obj/blob/main/utils/Data_Collecting.md)

## 2.모델 학습 
```
💡 데이터 학습에선 **2_Classification.ipynb** 파일을 사용, **코랩 환경**에서 진행

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
1. Github에 빈 Repositary 생성 
2. Repositary를 만든 뒤 로컬에서 Clone
3. 파일 복사 
    - 위 html 폴더에 있는 파일을 모두 자신이 만든 Repositary 폴더에 넣음 
    - 데이터 학습 단계에서 다운 받은 weights 파일을 mobilenet 폴더에 넣음 
        (이 때 model.json 뿐만 아니라 .bin파일 모두 넣어야 함) 
4. Git push         
    - git push를 이용하여 로컬의 파일들을 github에 업로드 함 
   
## 4. Web page 만들기 (gitpage deploy) 
- 깃허브의 pages 기능을 사용하면 index.html로 webpage를 만들 수 있음 
1. pages 만들기 
    - 앞서 push 한 git repositary에서 setting -> pages를 들어 감 
    -  
