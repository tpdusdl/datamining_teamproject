# datamining_teamproject
데이터마이닝 팀프로젝트 

## 주제 : 전동 킥보드 불법주차 장소 분석 및 주차장 입지선정


## 주제 선정 배경 및 필요성
<img src="https://github.com/tpdusdl/datamining_teamproject/assets/134132939/c193b36f-4d23-452d-98b1-1828d3f62f7a" width="350" height="300">
<img src="https://github.com/tpdusdl/datamining_teamproject/assets/134132939/3dd89d38-891f-47c8-abaa-07d19ae44648" width="350" height="300">
<img src="https://github.com/tpdusdl/datamining_teamproject/assets/134132939/187dc226-f1cc-4ff1-9c3a-30f07b70a540" width="300" height="300">
<img src="https://github.com/tpdusdl/datamining_teamproject/assets/134132939/6da922ee-43f0-4565-a2e6-249deb8c118d" width="1000" height="200">
<기사출처> https://skyedaily.com/news/news_view.html?ID=185976   


최근 전동 킥보드에 대한 수요가 계속해서 증가함과 동시에 불법주차로 인한 신고 및 안전사고에 대한 우려 또한 증가하는 추세이고 불편함을 표하는 시민들의 목소리도 점점 커지고 있다. 이에 따라 각 지자체에서 대응 방안을 내놓았지만 당장 눈앞에 있는 문제를 해결하기에 급급해 보인다.
이러한 전동 킥보드 불법주차는 통행방해, 보행자 안전 문제, 인력 낭비, 안전사고 등 여러 문제점을 야기하기에 근본적으로 문제를 해결할 필요가 있다.
<br/><br/><br/>
![image](https://github.com/tpdusdl/datamining_teamproject/assets/74286434/e832d98b-20f4-4e6a-8e13-183cc66177dd)
 <br/>또한, 현재 전동킥보드 주차장 위치는 불법주차문제를 반영하지 못하고 있음을 확인하였다.
따라서 주차 문제를 해결할 수 있는 알맞은 장소에 주차장을 설치해야한다.
```
Give examples
```

## 분석 목적
전동 킥보드의 불법 주차 문제를 수요에 충족하지 못하는 주차 스테이션의 수로 보고 전동 킥보드 주차장 증설을 제안함과 동시에 주차장이 필요한 입지를 구체적으로 선정해 주는 것을 분석 목적으로 한다.
불법주차가 많은 지역은 어떤 특징을 가지고 있는지 파악하고, 파악한 지역의 특징을 반영하여 최적의 주차장 입지를 선정하고자 한다.



```
Give the example
```

And repeat

```
until finished
```

End with an example of getting some data out of the system or using it for a little demo

## 데이터

### 변수설정
서울시 자치구 중 견인신고 수가 많은 상위 4개 구(마포구, 송파구, 동작구, 영등포구)를 선정해 각 구마다 법정동을 기준으로 나눠 동마다 아래 변수에 해당하는 사건 혹은 장소의 수를 획득한 데이터를 통해 할당해주었다.   
-견인수  
-pc방수  
-카페수  
-따릉이대여소 수  
-기숙사/고시원 수  
-독서실 수  
-약국 수  
-편의점 수  
-숙박업 수  
-학원 수  
-병원 수  
-부동산 수  
-양식집 수  
-한식집 수  
-중식집 수  
-일식집 수  
-음식점 전체수  
-동물병원 수  
-아파트 수  
-버스정류장 수  

총 20개의 feature 사용


### 데이터 획득
*[서울시 전동 킥보드 견인현황]( https://data.seoul.go.kr/dataList/OA-21304/S/1/datasetView.do)   
*[서울시 버스 정류소 위치 정보]( http://data.seoul.go.kr/dataList/OA-15067/S/1/datasetView.do)  
*[서울시 고등학교 기본정보]( http://data.seoul.go.kr/dataList/OA-20557/S/1/datasetView.do)  
*[서울시 대학 및 전문대학 DB정보 (한국어)](http://data.seoul.go.kr/dataList/OA-12974/S/1/datasetView.do)  
*[공공자전거 대여소 정보](http://data.seoul.go.kr/dataList/OA-13252/F/1/datasetView.do)  
*[서울교통공사 1_8호선 역사 좌표(위경도) 정보]( https://www.data.go.kr/data/15099316/fileData.do)     
*[소상공인시장진흥공단 상가(상권)정보 - 서울 ](https://www.data.go.kr/data/15083033/fileData.do )  



# 분석

## 
## EDA
<img src="https://github.com/tpdusdl/datamining_teamproject/assets/134132939/909a4f7f-0306-4fe2-a6cf-13f00efab5e0">
<img src="https://github.com/tpdusdl/datamining_teamproject/assets/134132939/795c2346-c2ec-4834-83f9-46812c63e226" width="700" height="300">
<img src="https://github.com/tpdusdl/datamining_teamproject/assets/134132939/c26ec7a8-98e2-488b-9753-0f03d5065b8b" width="300" height="300">
<img src="https://github.com/tpdusdl/datamining_teamproject/assets/134132939/85bc0b3b-61df-46e1-afb9-679bf8811d69">
<img src="https://github.com/tpdusdl/datamining_teamproject/assets/134132939/aa091706-9b00-4d6f-ab67-09a53c4e3b28">
<img src="https://github.com/tpdusdl/datamining_teamproject/assets/134132939/558c3542-cd12-4ba7-ba86-41eb60d57fcb">   


대표적으로 마포구에 저장된 데이터를 확인해보겠다.   
결측치 여부를 확인해 본 결과 모든 feature에 대해 존재하지 않음을 확인했다.   
feature의 type은 모두 int로 구성되어 있음을 알 수 있다.   
feature 간의 수치 차이가 다소 존재하기 때문에 뒤이어 분석할 clustring을 위해 scaling이 필요함을 확인했다.   
<img src="https://github.com/tpdusdl/datamining_teamproject/assets/134132939/48d61f38-b7f5-4b7d-97bf-cd5baac4fecf">   


각 feature들의 histogram을 확인해 보았다.   

<img src="https://github.com/tpdusdl/datamining_teamproject/assets/134132939/363d3bba-f945-46e4-b0d6-4666abd59349">   
견인수와 다른 변수들간의 상관계수를 확인해 본 결과, 상관계수가 0.6 이하인경우 분석에 악영향을 미칠 것으로 파악하여 버스정류장수, 아파트수, 약국수, 따릉이대여소수 변수들은 삭제했다.   
<img src="https://github.com/tpdusdl/datamining_teamproject/assets/134132939/e0005fcd-68a5-40c4-a2b0-5ad6e22ca4d5">   
3개 feature을 삭제한 후의 상관관계를 다시 확인해 보았다.   
모든 feature가 견인수와의 상관관계가 0.6이상임을 확인하고 clustering을 진행하겠다.

## 전처리
견인수, 카페수, 음식점수 feature 들이 다른 나머지 feature 들의 data 분포보다 큰 것으로 확인되어 k-means와 같은 알고리즘에서 거리 기반의 연산에 영향을 줄이기 위해 scaler = StandardScaler()을 사용하였다.   

## 모델링
### k-means
<img src="https://github.com/tpdusdl/datamining_teamproject/assets/134132939/6e434e57-aa16-42fa-aa48-64df7fa9c800">   
<img src="https://github.com/tpdusdl/datamining_teamproject/assets/134132939/6fa93596-1d2c-4a90-8af2-47dec20f6757">   

종합적으로 결과를 참고하였을때 n_cluster=4, algorithm=elkan 을 사용하기로 했다.   

kmeans = KMeans(n_clusters=4, algorithm= 'elkan', random_state=0)   
kmeans.fit(scaled_data)
<img src="https://github.com/tpdusdl/datamining_teamproject/assets/134132939/c1c1c9a6-4a13-43a8-a646-b391dab25419">   
k-means 결과 4개의 클러스터들의 특징은 다음과 같다.   

cluster1 : 독서실, 기숙사,고시원이 많은 지역   

cluster2 : 특징이 없음.   

cluster3 : 일식집, 편의점이 많은 지역   

cluster4 : 숙박업, 양식집이 많은 지역   


### agglomerative
<img src="https://github.com/tpdusdl/datamining_teamproject/assets/134132939/2489d175-77ff-42e8-bec1-1694a13d69d2">   

silhouette score를 고려해 n_clusters=4, linkage='average' 를 사용하기로 했다.   

agg = AgglomerativeClustering(n_clusters=4, linkage='average')   
labels=agg.fit_predict(scaled_data)   
<img src="https://github.com/tpdusdl/datamining_teamproject/assets/134132939/a6683b36-9052-499e-bd8c-2e466d8bb129">   

Agglomerative 결과 4개의 클러스터들의 특징은 다음과 같다.   

cluster1 : pc방수, 독서실 수, 동물병원수가 많은 지역   

cluster2 : 숙박업, 양식집, 카페수가 많은 지역   

cluster3 : 특징이 없다.   

cluster4 : 기숙사/고시원수, 한식집이 많은 지역   

### dbscan
<img src="https://github.com/tpdusdl/datamining_teamproject/assets/134132939/8af719bb-961c-4b21-9dce-22bbb732aa4b">   
Best Silhouette Score는 'eps': 1.5, 'min_samples': 3일 때, Silhouette Score: 0.20374381429350133로 나왔다.   
cluster label 출력 결과, Cluster Labels: [-1  0 -1  0 -1 -1 -1  0 -1 -1 -1 -1 -1  0 -1 -1 -1 -1 -1 -1  0 -1  0  0  -1  0]   
위와 같이 나왔고 이는 noise가 매우 많고 clustering이 잘 되었다고 판단하기 어려워 해당 방법론을 기각했다.   

뒤이어 후술할 3개 구(송파구, 동작구, 영등포구)에 대해서는 마포구 분석과정과 매우 유사하게 진행되었다.
## 송파구
### EDA
<img src="https://github.com/tpdusdl/datamining_teamproject/assets/134132939/3b5aea96-bcfc-4b8c-81be-c7646ce79fbf">   
송파구 feature들의 데이터 분포를 확인해본 결과, 데이터 scaling이 필요하다고 판단했다.   
<img src="https://github.com/tpdusdl/datamining_teamproject/assets/134132939/57c558d0-e832-4893-9152-8c44e0035c78">   
견인수와 다른 변수들간의 상관계수를 확인해 본 결과, 상관계수가 0.5 이하인경우인 약국수, 동물병원수, 지하철역수, 숙박업소수, 고등학교수, 병원 수 는 삭제했다.   
<img src="https://github.com/tpdusdl/datamining_teamproject/assets/134132939/7417db26-8020-4df0-87f2-0b3f763cee76">   
삭제 후 상관계수에 이상이 없음을 확인하고 clustering을 진행했다.   

### 전처리
scaler = StandardScaler()   
df_scaled = scaler.fit_transform(df)   

### k-means
<img src="https://github.com/tpdusdl/datamining_teamproject/assets/134132939/657e5f7d-c0fb-4a68-8749-c6bd589dd0c6">   
<img src="https://github.com/tpdusdl/datamining_teamproject/assets/134132939/53bc6e38-86ba-48e5-a85a-08b929f364eb">   

종합적으로 결과를 참고하였을 때 n_cluster=3, algorithm=elkan 을 사용하기로 했다.   
kmeans = KMeans(n_clusters=3, algorithm= 'elkan', random_state=0)   
kmeans.fit(df_scaled)   

### agglomerative
<img src="https://github.com/tpdusdl/datamining_teamproject/assets/134132939/1d2bae85-8c93-4a99-80a4-5d6405fc2aa6">   

agg = AgglomerativeClustering(n_clusters=3)    
agg.fit(df_scaled)   

### dbscan
<img src="https://github.com/tpdusdl/datamining_teamproject/assets/134132939/ab231329-d5e2-4786-9d57-8b0e3b8649e2">   

전부 이상치로 분류되어 의미 없는 결과가 나왔으므로 분석 알고리즘에서 제외했다.

## 동작구
### EDA
<img src="https://github.com/tpdusdl/datamining_teamproject/assets/134132939/3b5aea96-bcfc-4b8c-81be-c7646ce79fbf">   
동작구 feature들의 데이터 분포를 확인해본 결과, 데이터 scaling이 필요하다고 판단했다.   
<img src="https://github.com/tpdusdl/datamining_teamproject/assets/134132939/57c558d0-e832-4893-9152-8c44e0035c78">   
견인수와 다른 변수들간의 상관계수를 확인해 본 결과, 상관계수가 0.7 이하인경우인 기숙사,학교,pc방 은 삭제했다.    

### 전처리
scaler = StandardScaler()   
df1_scaled = scaler.fit_transform(df1)   

### k-means
<img src="https://github.com/tpdusdl/datamining_teamproject/assets/134132939/657e5f7d-c0fb-4a68-8749-c6bd589dd0c6">   
<img src="https://github.com/tpdusdl/datamining_teamproject/assets/134132939/53bc6e38-86ba-48e5-a85a-08b929f364eb">   

종합적으로 결과를 참고하였을 때 n_cluster=3, algorithm=elkan 을 사용하기로 했다.   
n_clusters = 3   
kmeans =KMeans(n_clusters = n_clusters, algorithm= 'elkan')   
kmeans.fit(df1_scaled)   

### agglomerative
<img src="https://github.com/tpdusdl/datamining_teamproject/assets/134132939/1d2bae85-8c93-4a99-80a4-5d6405fc2aa6">   

agg = AgglomerativeClustering(n_clusters=3, linkage='ward')   
agg_labels=agg.fit_predict(df1_scaled)    

### dbscan
<img src="https://github.com/tpdusdl/datamining_teamproject/assets/134132939/ab231329-d5e2-4786-9d57-8b0e3b8649e2">   

Cluster Labels: [ 0 -1  0 -1 -1  0 -1 -1 -1]   
dbscan결과 위와 같이 나왔고 이는 noise가 많고 clustering이 잘 되었다고 판단하기 어려워 해당 방법론을 기각했다.   


## 결론
### 마포구
전체적으로 실루엣 점수를 비교하였을 때, agglomerative 의 결과가 가장 좋다고 판단하였다.   
best algorithm: agglomerative n_clusters:4, linkage: average, 실루엣 점수:0.4011545610076085   
cluster1 : pc방수, 독서실 수, 동물병원수가 많은 지역   

cluster2 : 숙박업, 양식집, 카페수가 많은 지역   

cluster3 : 특징이 없다.   

cluster4 : 기숙사/고시원수, 한식집이 많은 지역   

이러한 특징들을 가진 cluster들에 할당된 법정동들을 분류해봤다.   
cluster1 : 동교동, 망원동, 상암동, 성산동   

cluster2 : 연남동   

cluster3 : 공덕동, 구수동, 노고산동, 당인동, 대흥동, 도화동, 마포동,상수동, 신공덕동, 신수동, 신정동, 아현동, 염리동, 용강동, 중동 ,창전동, 토정동, 하중동, 합정동, 현석동   

cluster4 : 서교동   

이를 통해 각각의 법정동별로 전동 킥보드 주차장 입지를 새로 선정함에 있어 우선적으로 고려해야 할 feature 선정을 했고,   
특징이 없는 cluster라 함은 주변 상권 혹은 대중교통 시설의 위치와는 별개로 견인 신고가 많이 들어오는 위치가 주차장 입지를 선정할 때 여전히 중요한 고려 사항 중 하나라는 것을 다시 한번 상기시키는 데에 의미가 있었다.   


### 송파구
분석의 논리적인 과정은 이하 마포구와 동일하게 진행하였고 그에 따른 결과는 다음과 같다.   
best algorithm: agglomerative   
n_clusters= 3, linkage = single, Silhouette Score: 0.4661810701236094   
<img src="https://github.com/tpdusdl/datamining_teamproject/assets/134132939/bb4dd39a-5cbf-4ba3-a490-2f8d984f473e">   

cluster1 : 특징이 없다.   

cluster2 : 카페수, 편의점 수, 음식점 수 가 많은지역   

cluster3 : pc방수, 기숙사 수가 많은 지역   

이러한 특징들을 가진 cluster들에 할당된 법정동들을 분류해봤다.   
cluster1 : 풍납동, 거여동, 마천동, 오금동,송파동,석촌동,삼전동, 장지동, 신천동   

cluster2 : 문정동   

cluster3 : 방이동, 가락동, 잠실동   

### 동작구
best algorithm: kmeans
n_clusters= 3, algorithm= 'elkan', Silhouette Score: 0.464784226978624   
<img src="https://github.com/tpdusdl/datamining_teamproject/assets/134132939/ed312298-bff3-4909-8b95-8f893e5fdaf6">   

클러스터 1 : 지하철 역, 병원많음   

클러스터 2 : 학원, 음식점 많음   

클러스터 3 : 특징 없음   

이러한 특징들을 가진 cluster들에 할당된 법정동들을 분류해봤다.   
클러스터 1 : 본동, 상도 1동, 동작동   

클러스터 2 : 상도동, 사당동   

클러스터 3 : 노량진동, 흑석동,대방동, 신대방   

### 영등포구
best algorithm: kmeans   
n_clusters= 5, algorithm: 'elkan', Silhouette Score: 0.2808630292848594   
<img src="https://github.com/tpdusdl/datamining_teamproject/assets/134132939/f7e92489-055d-41f6-8194-7761a46a5eac">   

클러스터 1 : 따릉이 대여소   

클러스터 2 : 특징이 없음   

클러스터 3 : 카페, 학원, 양식, 일식   

클러스터 4 : 특징이 없음   

클러스터 5 : 편의점, 음식점, 한식   

이러한 특징들을 가진 cluster들에 할당된 법정동들을 분류해봤다.   
클러스터 1 : 양평동 4가, 영등포동 3가, 영등포동 4가   

클러스터 2 : 당산동 2가, 문래동 1가, 문래동 5가, 문래동 6가, 양평동 6가, 양화동, 영등포동 1가, 영등포동 2가, 영등포동 6가, 영등포동 7가   

클러스터 3 : 당산동 4가, 도림동, 양평동 3가, 영등포동   

클러스터 4 : 당산동, 당산동 1가, 당산동 5가, 당산동 6가, 문래동 2가, 신길동, 양평동 1가, 양평동 2가, 양평동 5가, 영등포동 7가, 영등포동 8가   

클러스터 5 : 당산동 3가, 문래동 4가   

## 기대효과
추후 전동 킥보드의 수요에 맞춰 전용 주차장을 증설함에 있어 수요가 분명한 입지 주변 설치를 통해 전동 킥보드의 무분별한 주차로 인한 안전사고 문제 및 불필요한 노동력을 줄일 수 있을 것으로 기대된다.   
주차장에 주차돼있는 전동 킥보드를 통해서는 올바른 인식을 심어줄 것을 기대함으로써 전체적인 시민의식을 올려 거시적으로는 후속 분석을 진행할 때, 무분별한 주차로 인한 데이터가 줄고 확실한 수요에 의한 데이터를 통해 진행해볼 수 있다는 점에서 향상된 분석 효과를 기대할 수 있다.

## 한계점 및 추후 개선 방안
1. 대부분의 데이터들이 동 단위가 아닌 구 단위로 취합돼있는 형태라 서울시에 위치한 모든 자치구의 특징을 분석해보지 못해 해당 방법론을 통해 모든 구에 적용이 가능한 지 확인해보지 못한 점에 대한 분명한 한계점이 존재한다.
2. 분석에 쓴 feature들이 불법주차의 원인을 다 설명하지 못한다. 따라서 불법 주차에 영향을 미치는 다른 특징들을 추가하여 분석의 설명력을 높일 계획이다.



Explain what these tests test and why

```
Give an example
```

### And coding style tests

Explain what these tests test and why

```
Give an example
```



## 데이터 출처

* [Dropwizard](http://www.dropwizard.io/1.0.2/docs/) - The web framework used
* [Maven](https://maven.apache.org/) - Dependency Management
* [ROME](https://rometools.github.io/rome/) - Used to generate RSS Feeds

## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags). 

## Authors

* **Billie Thompson** - *Initial work* - [PurpleBooth](https://github.com/PurpleBooth)

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Hat tip to anyone whose code was used
* Inspiration
* etc
