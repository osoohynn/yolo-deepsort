# yolo-deepsort
yolo-deepsort object tracking


<br>

## 2025.1.1 기준 수정사항

### 1. 각종 라이브러리 version
requirement 설치 후
```
!pip install tensorflow-gpu==2.8.0
```
```
!pip install protobuf==3.20.3
```

### 2. numpy 자료형
numpy 1.20 부터는 np.int, np.float 이 쓰이지 않고 파이썬 내장 int, float을 사용해야한다.<br>
따라서 아래 코드를 실행하기 전에 해당 자료형들을 변경해주어야 한다. (3개)
```
!python object_tracker.py --video ./data/video/test.mp4 --output ./outputs/tracker.avi --model yolov4 --dont_show --info
```

### 2-1.
1. 코랩 파일의 ```/content/yolov4-deepsort/tools/generate_detections.py``` 를 찾아서 엽니다.
2. ```63``` 번째 줄의 ```np.int```를 ```int``` 로 바꿔줍니다.
3. 파일을 저장합니다. (command + S)

<img width="291" alt="Screenshot 2025-01-01 at 22 24 58" src="https://github.com/user-attachments/assets/13ed2e1b-ac8b-4503-a5ab-39780beb4222" /> ➡️
<img width="265" alt="Screenshot 2025-01-01 at 22 25 21" src="https://github.com/user-attachments/assets/1f501524-4e8a-4dac-b378-595342978ab4" />

### 2-2.
1. 코랩 파일의 ```/content/yolov4-deepsort/deep_sort/detection.py``` 를 찾아서 엽니다.
2. ```32``` 번째 줄의 ```np.float```를 ```float``` 로 바꿔줍니다.
3. 파일을 저장합니다. (command + S)

<img width="475" alt="Screenshot 2025-01-01 at 22 31 55" src="https://github.com/user-attachments/assets/7cd563d6-1f39-4ade-ba1c-9f6d03fe9e3c" /> ➡️
<img width="448" alt="Screenshot 2025-01-01 at 22 32 12" src="https://github.com/user-attachments/assets/4373571f-e544-4b67-a455-9f4d1150d4bf" />

### 2-3.
1. 코랩 파일의 ```/content/yolov4-deepsort/deep_sort/preprocessing.py``` 를 찾아서 엽니다.
2. ```32``` 번째 줄의 ```np.float```를 ```float``` 로 바꿔줍니다.
3. 파일을 저장합니다. (command + S)

<img width="327" alt="Screenshot 2025-01-01 at 22 34 30" src="https://github.com/user-attachments/assets/ff5edb3d-b3fe-4a39-9f56-8fc57945e312" /> ➡️
<img width="293" alt="Screenshot 2025-01-01 at 22 34 47" src="https://github.com/user-attachments/assets/a66c2a17-7b74-482a-904e-6a95da92e532" />


모두 변경 후 코드 실행 진행.
