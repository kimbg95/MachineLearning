**[ML-report] 개발자 중 높은 소득을 올리는 사람을 분류하는 데 가장 적합한 기법은 무엇이며, 어떤 특징들이 가장 관련이 있을까?**

**요약**

- 이 프로젝트는 개발자들의 소득 수준을 예측하기 위해 가장 적합한 머신러닝 기법을 분석하고, 고소득 개발자와 관련된 주요 특징들을 파악하는 것을 목표로 했습니다. 설문 조사에 참여한 약 65,000명의 개발자들이 포함된 데이터셋을 사용하여, 이들의 직무, 학력, 경력, 그리고 개인적 가치와 같은 다양한 정보를 분석했습니다.

**데이터셋 개요**

- **참여자 수**: 약 65,000명
- **참여자 구성**: 전문 개발자, 가끔 코딩하는 직장인, 개발자를 준비 중인 학생 등
- **주요 개발자 유형**: 전체의 약 55%는 풀스택 개발자, 약 20%는 모바일 개발자
- **경력 분포**: 30년 이상 코딩 경험이 있는 개발자 약 15%, 1년 이하 경험의 개발자 약 40%
- **학력**: 약 75%가 컴퓨터 과학, 컴퓨터 공학, 또는 소프트웨어 공학 관련 학사 이상의 학위를 보유
- **경력 가치**: 약 65%가 현재 직무에 대해 어느 정도 또는 매우 만족

### 1. 프로젝트 개요

**프로젝트 제목**: Stack Overflow Developer Survey 2020 데이터 분석

**목표**: Stack Overflow Developer Survey 2020 데이터를 분석하여 낮은 소득과 높은 소득에 관련된 주요 특징을 식별하고, 머신러닝 기법을 통해 데이터를 분류하며 통찰을 얻는 것.

**데이터 출처**: Stack Overflow Developer Survey 2020 (186개국, 약 65,000명의 응답자)

### 2. 데이터 이해 및 준비

**데이터셋 설명**:

- **총 행**: 64,461
- **총 열**: 61
- **열의 데이터 타입**: int64(1), float64(4), object(56)
<img width="549" alt="1" src="https://github.com/user-attachments/assets/e4153670-0f08-4cca-8ab5-ca69bfba96e4" />

**데이터셋 구성**:

1. **기본 정보**: 응답자의 기본 정보
2. **교육, 직업 및 경력**: 교육 수준, 직업, 경력 관련 정보
3. **기술 및 기술 문화**: 기술 스택, 기술 사용 관련 정보
4. **Stack Overflow 사용 및 커뮤니티**: Stack Overflow 사용 빈도, 커뮤니티 활동
5. **인구 통계 정보**: 응답자의 인구 통계적 정보
6. **최종 질문**: 추가적인 의견 및 피드백
<img width="572" alt="2" src="https://github.com/user-attachments/assets/176fbb1b-be78-4d17-99c8-b5a4fb5990b6" />

**탐색적 데이터 분석(EDA)**:

- 응답자의 지역, 인종, 성별, 직업 분포 분석
- 소득 분포를 확인하기 위해 'ConvertedComp' 열의 히스토그램 작성
- 교차표를 통해 성별에 따른 소득 차이 분석
<img width="422" alt="3" src="https://github.com/user-attachments/assets/d7e38d19-82e3-4b2a-9076-ebbdfa0c8720" />
<img width="459" alt="4" src="https://github.com/user-attachments/assets/4d2952b2-440b-46e7-8143-1bec64af7dae" />
<img width="440" alt="5" src="https://github.com/user-attachments/assets/557e1dce-f8d6-410a-bb9d-3f75192b7032" />
<img width="513" alt="6" src="https://github.com/user-attachments/assets/2b951972-b245-41b2-80da-7961198abfb0" />
<img width="513" alt="7" src="https://github.com/user-attachments/assets/9060a927-b6fc-4385-b505-87181b7b436e" />


**데이터 전처리**:

- 문자열 값을 숫자 값으로 변환
- 데이터를 0과 1 사이로 정규화
- 결측값 처리 및 이상치 제거

### 3. 분석 및 모델링

**분석 기법**:

1. **클러스터링 분석**:
    - K-Means 클러스터링을 사용하여 데이터를 낮은 소득과 높은 소득으로 그룹화
    - 엘보우 방법을 사용하여 최적의 클러스터 수 결정

<img width="509" alt="8" src="https://github.com/user-attachments/assets/52d1e19a-fd8e-4bdf-9444-7bbbf53f0534" />
<img width="454" alt="9" src="https://github.com/user-attachments/assets/515fc06e-9583-494d-a300-0b665ed9c467" />
<img width="598" alt="10" src="https://github.com/user-attachments/assets/40753510-0373-4c4d-ac93-ffddff1b3e4a" />
<img width="481" alt="11" src="https://github.com/user-attachments/assets/712cf521-96ec-4b0b-ba71-7453f94c73d4" />
<img width="393" alt="12-1" src="https://github.com/user-attachments/assets/36ce5403-8f15-409a-a5ff-9d3bdf028390" />
<img width="490" alt="13-1" src="https://github.com/user-attachments/assets/2d164f9d-f23b-4472-82c3-767f3f681ed1" />
<img width="556" alt="14" src="https://github.com/user-attachments/assets/a93ccd90-3d99-405e-9b00-49c7f11e2706" />
<img width="550" alt="15" src="https://github.com/user-attachments/assets/fc6d7139-2fa8-4e93-a25d-514e2056910e" />


2. **분류 모델**:
- **로지스틱 회귀**: 이진 분류 문제 해결을 위한 기준 모델
![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/73cbe43b-3974-4a7c-9f52-2f9eb1ebdbb3/13609468-cce3-416e-87f5-bd77fb156a54/image.png)

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/73cbe43b-3974-4a7c-9f52-2f9eb1ebdbb3/11915179-993f-4dd7-916b-9b13b7e689cc/image.png)

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/73cbe43b-3974-4a7c-9f52-2f9eb1ebdbb3/178b1577-e03d-4e91-8f7a-309d16b7007c/image.png)

**인공 신경망: 데이터 패턴 인식 및 예측**

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/73cbe43b-3974-4a7c-9f52-2f9eb1ebdbb3/5436b1db-7a9b-4453-a3f0-baec43b0257b/image.png)

**서포트 벡터 머신(SVM): 데이터 분류를 위한 초평면 찾기**
![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/73cbe43b-3974-4a7c-9f52-2f9eb1ebdbb3/cec19f2a-a2e1-4dbf-9cfb-7efdd1792d91/image.png)

**모델 평가**:

- 각 모델의 정확도, 혼동 행렬, ROC 곡선 등 성능 평가
- 모델의 하이퍼파라미터 조정 및 교차 검증

### 4. 주요 결과

- **클러스터링 결과**: 데이터는 명확하게 두 개의 클러스터로 나누어졌으며, 낮은 소득 클러스터와 높은 소득 클러스터가 식별되었습니다.
- **분류 모델 성능**:
    - 로지스틱 회귀: 정확도 80%, AUC 0.78
 
![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/73cbe43b-3974-4a7c-9f52-2f9eb1ebdbb3/978e29ac-29ff-4950-b790-bd3756952fbf/image.png)

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/73cbe43b-3974-4a7c-9f52-2f9eb1ebdbb3/39843eac-9582-4a09-8c12-dc6ab76b0a43/image.png)

- 인공 신경망: 정확도 85%, AUC 0.82
![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/73cbe43b-3974-4a7c-9f52-2f9eb1ebdbb3/4f2a0e4e-7c2c-4eb9-bc06-e692cc1f0bbd/image.png)

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/73cbe43b-3974-4a7c-9f52-2f9eb1ebdbb3/780c2bd1-a1d0-48f2-a142-d7f9503a23ce/image.png)

- 서포트 벡터 머신: 정확도 83%, AUC 0.80
![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/73cbe43b-3974-4a7c-9f52-2f9eb1ebdbb3/c07b7b3e-515e-4f33-a684-940211b768e4/image.png)

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/73cbe43b-3974-4a7c-9f52-2f9eb1ebdbb3/21212818-b4c3-4802-86df-1e98543225ca/image.png)

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/73cbe43b-3974-4a7c-9f52-2f9eb1ebdbb3/c3e96c80-7709-4e87-af89-7fef5ac92a35/image.png)

- **특징 중요도**: 높은 소득 클러스터는 주로 특정 지역, 경력, 교육 수준과 관련이 깊음

### 5. 통찰 및 결론

- 높은 소득과 관련된 주요 특징은 고급 기술 사용, 경력 수준, 특정 지역에 집중되어 있음.
- 성별과 지역에 따른 소득 격차가 존재하며, 이러한 인사이트는 채용, 교육 프로그램, 정책 수립에 유용할 수 있음.

![12.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/73cbe43b-3974-4a7c-9f52-2f9eb1ebdbb3/52345a98-1f40-42e7-a550-5e8e15410c54/12.png)

![13.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/73cbe43b-3974-4a7c-9f52-2f9eb1ebdbb3/d742ff9a-934b-4fa2-af3e-6bc3b4503817/13.png)

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/73cbe43b-3974-4a7c-9f52-2f9eb1ebdbb3/af318f1c-464d-480a-9718-ec811a3db1b1/Untitled.png)

### 6. 배운 점 및 향후 개선 사항

- **배운 점**:
    - 데이터 전처리와 탐색적 데이터 분석(EDA)의 중요성
    - 다양한 머신러닝 모델의 장단점 이해
    - 클러스터링 기법을 통해 데이터의 구조를 파악하는 방법
- **향후 개선 사항**:
    - 추가적인 데이터 변수 포함하여 분석의 깊이와 정확도 향상
    - 최신 데이터셋을 사용하여 결과 검증 및 업데이트
    - 모델 성능을 향상시키기 위한 추가적인 하이퍼파라미터 조정 및 기능 엔지니어링
