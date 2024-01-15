![image](https://github.com/Lee-ghwan-ho/boundary_detection-teed-/assets/114568122/5ef41a5e-211a-49a8-b1e5-9d4ac37c6f22)---
## 24.01.15
- 1.BIPED dataset 데이터 증강
---


  1. cv_imshow: 이미지를 화면에 표시합니다.
  2. make_dirs: 주어진 경로에 디렉토리를 만듭니다.
  3. image_normalization: 이미지를 정규화합니다.(엡실론으로 이미지의 최소값과 최대값이 동일한 경우 0으로 나누는 오류를 방지)
  4. gamma_data: 감마 보정을 통해 데이터를 증강합니다.
  5. rotate할때 520x520 정사각형으로 만듦(이미지 크기가 1280 x 720이라서 가로&세로:100~(720-100),)or 회전 하는 각도에 따라 가로세로 달라질수 있음
  6. 1280 x 720 img 2개로 분리 (왼쪽 이미지, 오른쪽 이미지)
  7. flip, gamma처리하면 데이터 증강 완료 


![image](https://github.com/Lee-ghwan-ho/boundary_detection-teed-/assets/114568122/286604d4-06f6-468d-a968-719e016d392c)
![image](https://github.com/Lee-ghwan-ho/boundary_detection-teed-/assets/114568122/27500bac-35ca-4af2-a731-be57c96b635e)
![image](https://github.com/Lee-ghwan-ho/boundary_detection-teed-/assets/114568122/ea7293db-c991-41bc-896a-2d431aa014cb)

---
