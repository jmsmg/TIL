# OpenCV

## 이미지 읽기

- cv2.imread(file_name, flag) : 이미지를 읽어서 Numpy 객체로 반환
  - file_name : 이미지파일
  - flag : 이미지를 읽는 방법 설정
    - IMREAD_COLOR : 이미지를 Color로 읽고 투명한 부분 무시
    - IMREAD_GRAYSCALE : 이미지를 Grayscale로 읽기
    - IMREAD_UNCHANGED : 이미지를 Color로 읽고, 투명한 부분도 읽음(alpha)

- cv2.imshow(title, image) : 이미지 화면에 출력 (코랩은 matplotlib으로 써야 윈도우에 띄울 수 있음)
  - title : 윈도우 창의 제목
  - image : 출력할 이미지 객체

- cv2.imwrite(file_name, image) : 특정한 이미지를 파일로 저장
  - file_name : 저장할 이미지 파일 이름
  - image : 저장할 이미지 객체

- cv2.waitKey(time) : 키보드 입력을 처리 (입력한 ascii code 반환)
  - time : 입력 대기시간 (무한대기 : 0)

- cv2.destroyAllWindows() : 화면의 모든 윈도우 닫기 (colab은 필요 없음)