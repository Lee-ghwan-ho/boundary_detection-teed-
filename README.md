
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
---
## 24.01.18
- 1. 481x321(Brind dataset크기)로 수정해서 돌리면 돌아가므로, 증강한 데이터셋을 481x321로 전체 수정해주는 코드 작성
  2. png,jpg 둘다 만든 데이터셋으로 학습 예정
---
