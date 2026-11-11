## STM32F411 GPIO 및 오실로스코프 사용

  - 디버그 익스프레션 창에서 GPIOA 찾아 보기
<img width="1920" height="1032" alt="image" src="https://github.com/user-attachments/assets/ecc37bd2-6e8d-4921-b585-7417b39c18bb" />
<br><br>

  - Extension connectors
<img width="1597" height="751" alt="image" src="https://github.com/user-attachments/assets/556381a9-e949-484e-a463-62796873b99c" />
<br><br>

  - Expression Value
<img width="1054" height="790" alt="image" src="https://github.com/user-attachments/assets/717ce2dd-ee5b-4768-b8c2-2abc44a6ded2" />
<br><br>

---

#### PA6 ON 해보기
 
MODER 계산

00 01 00 00 00 00 00 00

 1      0     0     0

<img width="626" height="380" alt="image" src="https://github.com/user-attachments/assets/366b16bf-155c-4f03-8a59-ef03cd19890c" />
<br><br>

OUTPUT DATA RESITER 계산

0000 0000 0100 0000

 0     0    4   0

<img width="633" height="298" alt="image" src="https://github.com/user-attachments/assets/902358c0-3d78-4dec-88e8-cc7967e068a1" />
<br><br>

  - 값 입력해주기
<img width="393" height="390" alt="image" src="https://github.com/user-attachments/assets/075ef9c1-2277-4a94-8efc-01aaff32e677" />
<br><br>

 - GPIO A 관련 레지스터 및 주소 옵셋 확인
<img width="807" height="379" alt="image" src="https://github.com/user-attachments/assets/f9828233-3c43-47c5-a861-c3ff8cc3463e" />
<br><br>

  - 오실로스코프로 측정하기

<img width="543" height="621" alt="image" src="https://github.com/user-attachments/assets/c7aabeea-8721-4739-a6f2-eb145f0b1d0f" />
<br><br>

  - Trig로 상승신호 확인함
<img width="899" height="745" alt="image" src="https://github.com/user-attachments/assets/e8c19f51-0d9e-4a04-9e90-338406c59753" />
<br><br>


