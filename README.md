# 5주차 1차시 강의내용 정리 — 상태변수와 상태방정식
작성자: 2021732074 김용현

---

## 상태변수의 개념

시스템이 시간에 따라 어떻게 변화하는지 나타내는 내부 변수  
초기조건을 자연스럽게 반영할 수 있어 실제 시스템을 더 현실적으로 표현할 수 있음  
전달함수에서는 알 수 없는 **시스템 내부 동작**을 분석할 수 있다는 장점이 있음

---

## 질량-스프링-댐퍼 시스템 예시

![사진1](https://drive.google.com/uc?export=view&id=1_DZeEbuKGcGpN1eKPpRm2gmB3p8S8VS9)

외력 r(t)에 의한 진동 시스템  
상태변수 선택  
- 위치: \(x_1 = y(t)\)
- 속도: \(x_2 = \dot{y}(t)\)

상태방정식  
\[
\dot{x}_1 = x_2
\]
\[
\dot{x}_2 = -\frac{b}{M}x_2 - \frac{k}{M}x_1 + \frac{1}{M}r
\]

→ 위치와 속도가 시간에 따라 변하는 것을 직접 계산할 수 있음

---

## RLC 회로 예시

![사진2](https://drive.google.com/uc?export=view&id=149l7Yw8pT-bPmZ70V2W34bytzy5dsUj2)

상태변수  
- 커패시터 전압: \(x_1 = v_c\)
- 인덕터 전류: \(x_2 = i_L\)

행렬 형태 표현  
\[
\dot{x} = Ax + Bu,\quad y = Cx + Du
\]

→ 전기회로도 기계시스템처럼 상태공간 표현으로 분석할 수 있음

---

## 상태방정식의 기본 구조

![사진3](https://drive.google.com/uc?export=view&id=1cPp5oI1pGbRHw6Ulgl4PEN-C-Dh-lk8O)

행렬의 의미를 정리하면  
- A : 상태가 스스로 변화하는 방식  
- B : 입력의 영향  
- C : 출력과 상태의 관계  
- D : 입력이 직접 출력으로 전달되는 비율  

---

## 상태방정식의 해석

![사진4](https://drive.google.com/uc?export=view&id=1mjWnKeGogvKt5TJIy9FVAqNiMsIhsn4b)

해의 구성  
\[
x(t)=e^{At}x(0)+\int_0^t e^{A(t-\tau)}Bu(\tau)d\tau
\]

- 첫 항: **초기조건**이 시스템에 미치는 영향  
- 두 번째 항: **입력**이 시스템에 미치는 영향  

---

## 상태천이행렬

![사진5](https://drive.google.com/uc?export=view&id=1bLar4SZ621N-bjnCQJmvBEQrAfsCk1t6)

\[
\Phi(t)=e^{At}
\]

→ 시간에 따른 상태 변화 비율  
→ MATLAB에서 자동 계산 가능

---

## 두 질량 시스템 예시

![사진6](https://drive.google.com/uc?export=view&id=1rJiyNsRoO57WLUjqdayFnt4VROX0vh1A)

상태변수 예시  
\[
x=[p, q, \dot{p}, \dot{q}]^T
\]

MATLAB 시뮬레이션 예시 코드

```matlab
sys = ss(A,B,C,D);
x0 = [0.1, 0, 0, 0];
initial(sys, x0, [0, 5]);
