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

## 3.Web browser demo 
```

💡 웹에서 분류 모델을 실행 시키기 위해서는 4개가 필요 함 
- index.html
- 모델 weights 파일 
- 라벨 json 파일 
- 결과 출력 이미지

```
