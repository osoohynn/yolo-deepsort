# yolo-deepsort
yolo-deepsort object tracking


## 2025.1.1 기준 수정사항
<br>

### 1. tensorflow version
requirement 설치 후
```
!pip install tensorflow-gpu==2.8.0
```

### 2. protobuf version
```
!pip install protobuf==3.20.3
```

### 3. numpy 자료형
numpy 1.20 부터는 np.int, np.float 이 쓰이지 않고 파이썬 내장 int, float을 사용해야한다.<br>
따라서 아래 코드를 실행하기 전에
```
!python object_tracker.py --video ./data/video/test.mp4 --output ./outputs/tracker.avi --model yolov4 --dont_show --info
```

np.int -> int

np.float -> float
