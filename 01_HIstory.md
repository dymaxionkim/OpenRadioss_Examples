## Brief History

### [KRASH](https://www.slideshare.net/altairhtcus/radioss-27-years-of-past-evolution-and-future)

- 1973 : 록히드사에서 군용 가젤 헬리콥터의 충돌 시뮬레이션 구현 (세계최초)
             노드 16개, 빔요소 22개, CDC7600 컴퓨터로 1개월 동안 계산, 전후처리는 수작업 (천공카드)

### [DYNA3D](https://www.osti.gov/servlets/purl/10139227)

- 1973 : 로렌스리버모어연구소([LLNL](https://www.llnl.gov/)) 소속 [홀퀴스트(Hallquist) 박사](https://www.youtube.com/watch?v=3kzwsjA00xg&t=2s)가 최초개발
             (폭격기 투발 지상충돌형 핵폭탄 3D 시뮬레이션 목적, 1인 개발)
- 1978 : 오픈소스 공개 (공유 요청을 받으면 자기테잎 미디어에 복사해서 나눠줌)
- 1982 : 메이저 업데이트
- 1984 : 벤슨(Benson) 박사 합류 (2인 개발 체제)
- 1986 : 메이저 업데이트 (일반화된 표면접촉 해석이 가능한 최초의 소프트웨어)
- 1987 : 금속 성형 모사 기능 추가
- 1988 : LSTC사(리버모어 소프트웨어 주식회사) 설립 (오픈소스 개발종료)
- 현재 : 로렌스리버모어연구소에서는 DYNA3D에서 발전시킨 병렬연산 대응 [ParaDyn ](https://www.osti.gov/servlets/purl/15004769)코드를 계속 개발하고 있음
           라그랑지안 지배방정식, 오일러 유체역학(SPH), 70종 이상의 재료모델, 멀티피직스, 
           고도화된 접촉 알고리즘, Meshless, 초거대 규모 연산 등의 신기술이 적용되어 있는 것으로 알려져 있음
           (로렌스리버모어연구소, 미국방부 관련 과제 종사 엔지니어들만 사용 가능)

### [LS-DYNA](https://en.wikipedia.org/wiki/LS-DYNA)

- 1988 : LSTC사에서 DYNA3D를 LS-DYNA로 개선하여 상용화
- 2007 : [The History of LS-DYNA, by 벤슨(Benson) 박사](http://blog.d3view.com/wp-content/uploads/2007/06/benson.pdf)
- 2019 : LSTC사가 ANSYS에 합병됨

### [RADIOSS](https://en.wikipedia.org/wiki/Radioss)

- 1985 : Altair사 설립 (엔지니어링 컨설팅)
- 1986 : 프랑스 Mecalog Group에서 Radioss 개발 (폭발 해석에 주력, DYNA3D에서 출발)
              창업자 [Francis Arnaudeau](https://www.linkedin.com/in/francis-arnaudeau-52948625/?originalSubdomain=fr)
- 1989 : Radioss CRASH (최초의 차량 충돌 시뮬레이션 성공, 애니메이션화 성공)
             슈퍼컴퓨터에서 운용, 병렬연산, 7천개 요소망, 계산시간 10시간, 1us 시간간격
             Radioss 3D (벙커버스터 미사일 콘크리트 충돌 해석)
- 1992 : Fortran90 으로 컨버젼
- 1995 : 포드자동차 실무적용 (3~6만개 요소망, 자동차 충돌)
- 1996 : 분산형 메모리 기능 지원 (대규모 해석에 필요)
- 2000 : 1~2백만개 요소망 도달, Implicit 기능 추가
- 2006 : Altair가 Mecalog Group을 합병, Hyperworks에 Radioss 통합
              Francis Arnaudeau는 Altair의 전무이사(CTO)로 이동, Mecalog Group의 모든 임직원은 그대로 고용승계
- 2010 : 2~4백만개 요소망 도달, 접촉 해석 기능 대폭 개선, X-FEM 기능 추가 (크랙), 에어백 해석 기능 추
- 2021 : 입력파일 형식으로 (1) Radioss Block  (2) LS-DYNA key 형식 모두 지원 시작
- 2022 : OpenRadioss 오픈소스 공개
- 향후계획
  추가재료모델/최적화/다중물리학/외부솔버협업/GPU지원/2차ALE/Meshless/지능형접촉해석 등

### ETC

- [PAM-CRASH](https://en.m.wikipedia.org/wiki/Pam-Crash) (독일), ESI Group, from 1985
- [DyTran](https://hexagon.com/ko/products/dytran) (독일), HEXAGON사
- [Abaqus Explicit](https://www.3ds.com/products-services/simulia/products/abaqus/abaqusexplicit/) (프랑스), Dassault사

### Radioss는 왜 오픈소스화 했는가?

- LS-DYNA 등의 기존 선발업체 대비 후발주자로서 패널티가 계속 있어왔음
  (신규추가된 기능이 상대적으로 부족하다던가, 실무 성공 사례가 상대적으로 적은 편이라던가, 사용자집단이 작다던가 등)
- Altair사는 Hyperworks 플랫폼의 시장점유율을 끌어올리는데 관심이 있고, 그 구성요소 중의 작은 한 부분에 불과한 Radioss는 전략적으로 독점 코드를 유지할 이유가 적은 편임
- 따라서 주력제품인 Hyperworks의 판매를 촉진하기 위한 촉매로서 OpenRadioss의 존재가 더 유리하다고 판단