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

## 시각화

## 평가


## 결과
1.마포구
2.영등포구
3.송파구
4.동작구

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
