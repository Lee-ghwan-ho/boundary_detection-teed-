
---
## boundary_detection-teed-
 -  Ranked #1 on Edge Detection on UDED practice(several image dataset 24.01.12)
---
## 24.01.12 

# 연구과제에 필요한 boundary detection 모델을 찾다가, 속도도 빠르고 uded data 1등인 model을 학습시키는 과정진행
- 1.BIPED dataset 학습 
- 2.BIPED + BRIND dataset 학습
- 3~~BIPED DATA 증강~~
- 4~~gray scale data or biomedical image 실험해서 성능 평가~~
- 5~~추가적인 data로 학습~~
- <img src="240112/TEED-main/TEED-main/checkpoints/스크린샷 2024-01-12 184036.png" alt="설명">
---
## 24.01.15
- 1.BIPED dataset 데이터 증강(13:30🕜->18:00🕡끝)
- 2.gray scale로 증강하면 gray scale에서 더 잘 나올까 생각 -> 코드 수정중
- 3.gray scale로 바꾸면 추가해줄수있는 기법이 있는지 찾아보기(ex) color는 감마추가)
- 4.train.lst파일 수정, test.lst파일 수정 후 모델 실행 -> 에러 (3,) 수정필요
---
## 24.01.16
- 1.그냥 실제 사진만(flip,rotate) 넣고 돌려보면 되는지 확인 필요
- 2.gray scale로 만들어서 저장하는 데이터 증강 코드로 수정 
## 24.01.17
- 1.증강 data, model에서 돌아가지 않음(데이터 크기문제 p1 -> 720x720, p1flip -> 720 x 720, rot_19 -> 530 x 530 ,90 -> 720x720)
- 2.나중에 model을 보고 증강한 grayscale data에서 돌아갈수 있도록 모델을 크게 수정해보는것도 좋을것 같음 -> grayscale domain을 예측해야하므로 
---
## 24.01.18
- 1. 481x321(Brind dataset크기)로 수정해서 돌리면 돌아가므로, 증강한 데이터셋을 481x321로 전체 수정해주는 코드 작성
- 2. png,jpg 둘다 만든 데이터셋으로 학습 예정
- 3. 학습결과
![image](https://github.com/Lee-ghwan-ho/boundary_detection-teed-/assets/114568122/11d7d3c4-d03e-4e1a-8af5-fb7eec27f3bb)
- 4. 우리 데이터셋에서도 좋은 성능 보여줌 but 노이즈많은 데이터셋에서는 성능이 좋지않았음 

---
## 24.01.19
- 1. 마무리 (흐린 데이터같은 경우는 인식하지 못하는 결과 -> 이미지 전처리를 통해 다시 수행해 볼 예정)
- 2. 의료 데이터셋에 적용해보고 결과값 도출해보기
