## OS

- 기본적으로는 Linux 권장되지만, MS Windows용으로 컴파일된 배포본도 제공됨
- 다만 Arch Linux의 경우 시도해 본 결과 : [MUMPS](https://mumps-solver.org) 빌드가 안되어 직접 컴파일 실패, 설치본을 다운로드 받아서 사용 가능
- Ubuntu Linux의 경우에는 문제 빌드에 문제 없을 것으로 보임
- 본 문서에서는 MS WIndows 기준으로 가장 쉬운 방법을 서술


## 적합한 해석 종류

- Explicit Nonlinear Transient (명시적 비선형 천이해석)
- 접촉 비선형, 재료 비선형, 대변위
- Explicit (명시적,외연적,양적법,양해법) vs Implicit (암시적,내연적,음해법) 방법 비교

| **항목**                     | **Explicit**                           | **Implicit**                                     |
| ---------------------------- | -------------------------------------- | ------------------------------------------------ |
| 안정조건 (Stability)         | Conditionsal stability                 | Always stable                                    |
| 시간증분 ( $\Delta t$ )      | Small : [us]                           | Large : [ms]                                     |
| 정밀도 (Precision)           | $\theta = ( \Delta t )^2$              | $\theta = ( \Delta t )^2$                        |
| 행렬형태 (Matrix)            | Diagonal : $M^{-1}$                    | Non-diagonal : $[M + \alpha K]^{-1}$             |
| 메모리 소요량 (Memory)       | Low : 10 MW                            | High : 6000 MW                                   |
| 방법론 (Method)              | Element by element(Local Treatment)    | Global resolution(Need convergence at each step) |
| 강건성 (Robustness)          | Good(Hige and coupled non-linearities) | Bad(Null pivots, Divergence …)                   |
| 하드웨어 비용 (Cost:CPU,RAM) | Low                                    | High                                             |
| 병렬화 (Parallelisation)     | O                                      | X                                                |
| 동적문제 (Dynamic Problem)   | O                                      | O                                                |
| 정적문제 (Static Problem)    | X                                      | O                                                |
| 충격문제 (Shock Problem)     | O                                      | X                                                |
