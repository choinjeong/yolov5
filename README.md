# yolov5

### YOLO
- YOLO는 “You Only Look Once” 약자로, 객체 감지(Object Detection)를 위한 딥러닝 기반 알고리즘입니다.
- 이미지나 비디오에서 여러 객체의 위치와 클래스를 실시간으로 감지할 수 있는 모델로 2016년에 처음 소개되었고  2023년 최근까지 v8까지 나오기도 했습니다. 

### YOLOv5
- 2020년에 나온 버전으로 기존 YOLO 알고리즘에 대해 크게 개선되었습니다.
- pytorch 기반으로 구현되었으며, 커뮤니티와 개발자에 의해 활발하게 사용되고 개선되고 있습니다.

### 데이터 소스
- roboflow(****Thermal Dogs and People Dataset)****
[Computer Vision Datasets](https://public.roboflow.com/)

```python
!python train.py --img 640 --batch 16 --epochs 20 --data custom/data.yaml --cfg models/custom_yolov5s.yaml --weights yolov5s.pt --name yolov5_coco  --cache
```

- image : 이미지 크기
- batch : 배치 크기
- epochs : epoch 크기
- data : 데이터 파일(클래스명, 클래스개수 및 데이터 경로를 담고 있음)
- cfg : 모델 크기, 구조에 대한 정보를 담고 있음. (YOLOv5s, YOLOv5m, YOLOv5l, YOLOv5x 순으로 크기가 커질수록 복잡해지고 정확성이 높아지는 대신 시간이 오래 걸림) yaml 파일 형식으로 저장되어 있음
- weights : 모델의 가중치를 담고 있는 파일
- name : 학습된 모델 이름
- cache : 캐시 이미지

### 예측 결과

(시각화1-성능지표 그래프)

(시각화2-예측 사진)

### 실행환경
python : 3.9.17
numpy : 1.23.5
opencv : 4.8.0

### 참고
[1] https://github.com/ultralytics/yolov5
