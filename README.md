# Data Analysis Capstone Design
Kyung-Hee University Software Convergence (Jun Yong Lee, Tae Kyoung Lee)

### Vertiport Location Optimization
#### 1. What is UAM?
- UAM은 기체, 운항, 서비스를 총칭하는 개념
- 도심화 + 수도권 집중 지상교통 혼잡에 도시당 UAM터미널(Vertiport) 30여개와 300여대의 기체가 비행할 것으로 전망함
- UAM은 도시인구 증가에 따른 도시교통 수요의 야기된 문제의 여러 문제(대기오염, 교통소음, 지구온난화, 교통스트레스)를 해결할 미래 대안으로 평가!

#### 2. UAM과 관련된 연구의 필요성
- UAM의 대량생산과 대중화를 극복하기 위해 자동차 산업의 경험과 노하우를 활용할 필요 있음
- UAM의 산업 선장의 핵심, 도심 대중의 수용성이 최대관건
- UAM의 핵심 인프라인 버티포트 네트워크의 종합적인 교통망 체계 개편이 필수적

#### 3. Research Idea
![image](https://github.com/user-attachments/assets/79e69214-8971-4088-9471-6dcabaeb0a1e)

#### 4. Model & Objective Function
\documentclass{article}
\usepackage{amsmath}

\begin{document}

\section*{Optimization Problem}

\textbf{Minimize}
\[
Z = \sum_{i} \sum_{j} d_{ij} \cdot x_{ij}
\]

\textbf{Subject to:}

\begin{align*}
\sum_{i} y_i &= k \\
\sum_{j} P_j \cdot x_{ij} &\leq 8400 \cdot y_i & \text{if } k \leq 4 \\
\sum_{j} P_j \cdot x_{ij} &\leq 14600 \cdot y_i & \text{if } k \geq 5 \\
\sum_{j} x_{ij} &\geq y_i & \forall i \\
d_{ij} &\geq 10 & \forall i, j \text{ with } y_i = y_j = 1, i \neq j \\
\sum_{j} x_{ij} &\geq y_i & \forall i \\
y_i &= 0 & \text{(if 후보지가 산지)} \\
y_i &= 0 & \text{(if 후보지가 하천)} \\
y_i &= 0 & \text{(if 후보지가 자연환경보전지역)} \\
d_{i,건물} &\geq 2 & \forall i \text{ with } y_i = 1 \\
d_{i,기타시설} &\geq 1 & \forall i \text{ with } y_i = 1 \\
d_{i,학교} &\geq 1 & \forall i \text{ with } y_i = 1
\end{align*}

\textbf{Variables:}
\begin{itemize}
\item $x_{ij}$: 이진 변수로, 후보지 $i$가 수요지 $j$에 할당되었는지를 나타냅니다.
\item $x_{ij} = 1$이면 할당되었음을 의미.
\item $x_{ij} = 0$이면 할당되지 않음.
\item $y_i$: 이진 변수로, 후보지 $i$가 버티포트 위치로 선택되었는지를 나타냅니다.
\item $y_i = 1$이면 버티포트로 선택됨.
\item $y_i = 0$이면 선택되지 않음.
\item $P_j$: 수요지 $j$의 인구 수를 나타내는 변수.
\item 각 수요지의 인구 크기는 나타내며, 후보지에 할당된 수요지들의 인구 총합을 계산하는 데 사용됨.
\end{itemize}

\end{document}

#### 6. Reference
- 도시의 하늘을 여는 한국형 도심항공교통(K-UAM) 로드맵 (관계부처합동, 2020)
