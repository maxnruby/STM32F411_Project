## STM32CUBEIDE에서 만든 코드를 C언어로 옮기기

  - 초음파 거리 센서(HC-SR04)의 Echo 신호를 검출하는 STM32 로직을 C언어 환경에 옮긴 테스트 코드
  - 디버그 환경에서 0과 1로 테스트
```
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
```


  - 라이징 에지 검출 / 폴링 에지 검출 코드
```
#define _CRT_SECURE_NO_WARNINGS
#include <stdio.h>

#define HIGH 1
#define LOW 0

int main(void) {
    unsigned int TIM_COUNTER = 0;
    int before = LOW;
    int now = LOW;

    while (1) {
        printf("Signal : ");
        scanf("%d", &now);

        if (before == LOW && now == HIGH) {
            printf("Rising Edge\n");
            TIM_COUNTER = 1;
        }
        else if (before == HIGH && now == HIGH) {
            TIM_COUNTER++;
            printf("Count %u\n", TIM_COUNTER);
        }
        else if (before == HIGH && now == LOW) {
            printf("Falling Edge\n");
            printf("Total : %u\n\n", TIM_COUNTER);
            TIM_COUNTER = 0;
        }

        before = now;
    }

    return 0;
}
```
    
