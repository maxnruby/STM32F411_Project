## C언어 배우기

  - 초음파 거리 센서(HC-SR04)의 Echo 신호를 검출하는 STM32 로직을 C언어 환경에 옮긴 테스트 코드
  - 디버그 환경에서 0과 1로 테스트

#include <stdio.h>
#include <windows.h>

#define HIGH 1
#define LOW 0

long unsigned int echo(void)
{
    long unsigned int echo_val = 0;
    unsigned char HAL_GPIO_ReadPin = 0;
    unsigned int TIM_COUNTER = 0;

    while (HAL_GPIO_ReadPin == LOW) {}   /* 1) 상승(HIGH) 대기 */
    TIM_COUNTER = 0;                        /* 2) 카운터 0 */
    while (HAL_GPIO_ReadPin == HIGH) {    /* 3) 하강(LOW)까지 카운트 */
        TIM_COUNTER++;
    }
    echo_val = TIM_COUNTER;                 /* 4) HIGH 유지 시간(us) */

    if (echo_val >= 240 && echo_val <= 23000) return echo_val;
    return 0;
}
int main(void)
{
    while (1)
    {
        echo();    
    //    Sleep(1000);
    }

}

