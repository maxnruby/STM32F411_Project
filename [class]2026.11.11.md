오실로스코 사용법

STM32F411 보드 LED 켜보기->오실로스코프 연결

STM32Cube IDE Debeg 하면서 Trigger 어쩌구

상승 & 하강 trig

커서 > 종류 > 진폭 > 가로 > 왼쪽 위를 돌려돌려
              시간 > 1ms 까지 재보기 커서 누르고 왼쪽 위 돌려돌려 커서2 눌러서.... 

디버그에서 익스프레션 창에서 GPIOA 찾아서 보기
<img width="1920" height="1032" alt="image" src="https://github.com/user-attachments/assets/ecc37bd2-6e8d-4921-b585-7417b39c18bb" />

Extension connectors
<img width="1597" height="751" alt="image" src="https://github.com/user-attachments/assets/556381a9-e949-484e-a463-62796873b99c" />

Expression Value
<img width="1054" height="790" alt="image" src="https://github.com/user-attachments/assets/717ce2dd-ee5b-4768-b8c2-2abc44a6ded2" />

  - PA6 ON 
MODER

00 01 00 00 00 00 00 00
1    0    0    0

OUTPUT DATA RESITER 

0000 0000 0100 0000
0   0    4   0

<img width="393" height="390" alt="image" src="https://github.com/user-attachments/assets/075ef9c1-2277-4a94-8efc-01aaff32e677" />
  오실로스코프로 측정하기
<img width="899" height="745" alt="image" src="https://github.com/user-attachments/assets/e8c19f51-0d9e-4a04-9e90-338406c59753" />

