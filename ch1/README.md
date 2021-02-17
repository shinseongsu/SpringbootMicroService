# Spring boot MSA 적용해보기 

---

1. gradle에 멀티 프로젝트 빌드 설정 하기

#### root의 settings.gradle 주목.


![CreatePlan](./images/settings.png)



#### 각각의 모듈에도 settings.gradle로 name을 정해준다.


![CreatePlan](./images/name_settings.png)


다른 모듈의 service단이나 util을 사용하고 싶으면 build.gradle에서 추가해준다.


![CreatePlan](./images/module_dependencies_추가.png)


잘 적용이 되었는지 확인해본다.
참고로 저는 터미널에서 curl 을 사용하여 요청을 보내보았습니다.

> `` curl http://localhost:7001/product/123  `` 요청 (밑에 결과 화면)

![CreatePlan](./images/product_rest.png)


> `` curl http://localhost:7000/product-composite/1 `` 요청 (밑에 결과 화면)
>
![CreatePlan](./images/product_composite%20결과.png)

