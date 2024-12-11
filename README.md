# Data Analysis Capstone Design


### Vertiport Location Optimization
##### Kyung-Hee University Software Convergence (Jun Yong Lee, Tae Kyoung Lee)
------------------------------------------------------------------------------
#### 1. What is UAM?
- UAM (Urban Air Mobility) is a comprehensive concept encompassing aircraft, operations, and services.
- With urbanization and congestion in ground transportation due to population concentration in metropolitan areas, it is expected that each city will have around 30 UAM terminals (vertiports) and approximately 300 aircraft in operation.
- UAM is considered a future alternative to address various urban transportation issues caused by increasing urban populations, including air pollution, traffic noise, global warming, and traffic-induced stress.

#### 2. Research Needs
- To overcome the challenges of mass production and popularization of UAM, it is essential to leverage the experience and expertise of the automotive industry.
- The key to the growth of the UAM industry lies in public acceptance within urban areas.
- A comprehensive reorganization of the transportation network system, including the core infrastructure of UAM—vertiport networks—is crucial.
  
#### 3. Project Summary

Experts in various fields emphasize that numerous factors must be addressed for urban air mobility (UAM) to become a viable and widely accepted future mode of transportation. Among these, we aim to tackle a specific issue highlighted by a domestic telecommunications company’s pilot project team. This team underlined the necessity of a comprehensive reorganization of the transportation network system centered around vertiport networks, the core infrastructure of UAM. Before addressing the broader transportation network, this study focuses on optimizing vertiport locations, as their placement is critical to the success of UAM.

The primary goal of this research is to resolve this issue with a particular focus on the southern Gyeonggi region. Several reasons justify this regional focus. Currently, UAM operation plans are limited to mid-range routes with a maximum distance of approximately 40 km. This operational range suggests that considering the entirety of Gyeonggi Province would exceed the scope of the problem at hand. Additionally, while exploring options for the capital city of Seoul may seem logical, numerous existing studies have already examined this area. These studies have proposed demonstration routes and identified optimal locations for vertiports based on factors such as noise levels. The abundance of prior research on Seoul indicates that further studies in this region would likely focus on addressing the limitations of previous work.

Although complementing prior research is valuable, this study seeks to take on a more challenging and exploratory approach by focusing on a different region. The southern Gyeonggi area was chosen for its proximity to the researchers’ academic institution, enabling deeper contextual understanding and practical engagement. Thus, this study focuses on key cities in southern Gyeonggi, including Suwon, Yongin, Osan, and Hwaseong, to identify optimal vertiport locations and contribute to the successful deployment of UAM in the region.

#### 4. Project Idea
![image](https://github.com/user-attachments/assets/79e69214-8971-4088-9471-6dcabaeb0a1e)

![image](https://github.com/user-attachments/assets/182d6d62-3574-4390-b966-488b09086b1c)
![image](https://github.com/user-attachments/assets/76728de8-3937-40a3-a16e-563a6322c569)

#### 5. Tools
- Language : Python 3.11.7
- Enviroment : VSCode
- Libraries : numpy, pandas, geopandas, folium, PuLP


#### 6. Code Instruction
```
git clone https://github.com/https://github.com/taekyounglee1224/Data_Capstone.git
```
```
capstone.ipynb
```
```
import geopandas as gpd
import folium
from IPython.display import display
import pandas as pd
from sklearn.preprocessing import MinMaxScaler
from folium import Choropleth
from folium import LayerControl, FeatureGroup
import matplotlib.pyplot as plt
import matplotlib.lines as mlines
import matplotlib.patches as mpatches
import numpy as np
import matplotlib.colors as mcolors
from shapely.geometry import Polygon, box
from pyproj import CRS
from pulp import LpProblem, LpMinimize, LpVariable, lpSum, LpBinary, PULP_CBC_CMD
from shapely.geometry import Point
```

- Place the dataset in the data/ directory



#### 7. Demo

<img width="450" alt="image" src="https://github.com/user-attachments/assets/fe901b1d-2bee-4ddc-932b-fc7fce2bc15a">
<a href = "file:///Users/taekyounglee/Documents/projects/DA_Capstone/vertiport_map.html">Link to Map</a>


#### 8. Conclusion and Future work

![image](https://github.com/user-attachments/assets/e620377b-e48b-4bf6-838f-03660d88251c)

1. Expanding the Scope of Data to a National Scale
Developing a more universal and generalized model by expanding the dataset to include national-level data could contribute to the formulation of logistics and mobility improvement strategies at the country level.

2. Incorporating Dynamic Data for Temporal Trends
Utilizing dynamic data to capture temporal trends would enable the development of models that reflect changes over time. This could be achieved by integrating machine learning or artificial intelligence techniques to design more adaptive and flexible models.

3. Building Multi-Objective Optimization Models
Expanding the research to include additional factors such as environmental considerations and policy constraints could result in a multi-objective optimization model that balances environmental protection and community acceptance. This would extend the utility of the study beyond theoretical exploration, making it applicable to practical policy-making and implementation stages.



#### 9. References
- 도시의 하늘을 여는 한국형 도심항공교통(K-UAM) 로드맵 (관계부처합동, 2020)
- 성유진, 김새벽, 최윤수, 조성길. (2023-06-02). 도심항공교통(UAM) 버티포트(Vertiport) 최적입지 선정 및 경로선정을 통한 이동시간 효용성 분석. 대한공간정보학회 학술대회, 대전.
- 박정원, 강나연, 송병덕. (2023-05-31). 다차원적 도심 물류 네트워크 설계: UAM vertiport 및 지상물류허브 동시 입지 선정 최적화. 대한산업공학회 춘계공동학술대회 논문집, 여수.
- 김원진, 박재홍. (2022). 도심항공교통(UAM) 버티포트(Vertiport) 입지 선정 영향요인 연구 . 도시부동산연구, 13(2), 119-137.
- 김민지, 박세연, 김동규. (2023-04-26). UAM 버티포트 입지유형 사례연구를 통한 입지선정요인 고찰. 대한건축학회 학술발표대회 논문집, 부산.
