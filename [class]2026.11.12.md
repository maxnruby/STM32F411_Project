## HC_SR04(초음파센서) 활용

  초음파센서는 초음파를 송신(Trigger)한 뒤 메아리가 돌아올 때(Echo)까지의 시간을 정확하게 측정함<br>

  이를 위해 타이머 인터럽트를 설정<br><br>
  

  - Timer 설정<br>
<img width="485" height="629" alt="image" src="https://github.com/user-attachments/assets/2f844e7d-52bc-476b-bcd7-98895859b400" wide=30% />
<br><br>

  - 핀설정<br>

<img width="555" height="498" alt="image" src="https://github.com/user-attachments/assets/e94c14c9-cf60-4f28-9803-e75e1c5c0208" />
<br><br>

#### 오실로스코프로 신호측정하기

  - 설정한 타이머 주기에 맞춰 트리거 펄스가 제대로 나가는지 오실로스코프 파형으로 확인

  - HAL_Delay(1);
      
<img width="445" height="149" alt="image" src="https://github.com/user-attachments/assets/4f36fb18-3d83-4b9c-af1c-48884101893c" />
<br><br>
<img width="787" height="739" alt="image" src="https://github.com/user-attachments/assets/c7c318ff-2336-4a1b-aaa0-224130d32ce0" />
<br><br>

  - delay_us(200);
  - 정확하게 200us 측정됨
       
<img width="396" height="112" alt="image" src="https://github.com/user-attachments/assets/6b3a5e35-6277-4234-86d9-73bc34c613ca" />
<br><br>
<img width="781" height="732" alt="image" src="https://github.com/user-attachments/assets/eec92de9-659c-4406-8154-aaa81e6ee5c5" />
<br><br>
 
