# 📈데이터로 말하겠습니다. 안녕하세요, 데이터 분석가 고성빈입니다.
##### <br>

- 📫 contect : sbinhigher@naver.com
- notion : https://www.notion.so/o-17589b3f2b2d80e389f7c5ad9ffb55d5?source=copy_link
- velog : https://velog.io/@tjdqls3324/posts
- Github : https://github.com/sbinhigher

## Contents
1. [프로젝트](#프로젝트)
---

## 프로젝트
###### <br>
### **풍력발전기 블레이드 결함 탐지 솔루션 개발**

### 🔍 프로젝트 분류  
`이미지 처리(Image Processing)` · `이미지 객체 탐지(Object Detection)` · `데이터 라벨링(Data Labeling)`
### 🙋 역할  
- 이미지 객체 탐지 모델링 및 프로젝트 매니징 총괄  
- 현장성과 정확도를 모두 반영한 진단 기준 수립 주도
### 📂 프로젝트 배경
- 드론으로 촬영된 블레이드 이미지를 **전사 수작업 검수**하느라 시간이 과도하게 소요됨  
- **엔지니어별 결함 판단 기준 상이**로 인해 검사 정확도와 신뢰도에 문제 발생
### 💡 문제 해결 방법
1. **결함 유형 및 위험도 레벨에 대한 기준 정립**  
2. **자율주행 드론**을 활용해 블레이드 전면 이미지 수집  
3. 이미지 기반 **객체 탐지 모델(YOLOv7)** 구축으로 자동 진단 시스템화  
4. Ground Truth를 기반으로 한 평가체계로 진단 정확도 정량화
### 🚀 목표 및 성과
| 항목 | 기존 | 개선 | 성과 |
|------|-----------|------------|------|
| ⏱️ 진단 소요 시간 | 이미지당 평균 96.42초 | 이미지당 평균 5.99초 | **진단 시간 93.8% 단축** |
| 📏 위험도 기준 | 주관적・불일치 기준 | 정량 기준 수립 | **표준화된 위험도 분류체계 확립** |
| 🎯 진단 정확도 | 측정 불가 | Ground Truth 기반 평가 | **재현율(Recall) 0.9 달성** |
### 🛠️ 사용기술 및 툴(tool)

<p>
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=flat&logo=opencv&logoColor=white"/>
  <img src="https://img.shields.io/badge/YOLOv7-black?style=flat&logo=github&logoColor=white"/>
  <img src="https://img.shields.io/badge/NumPy-013243?style=flat&logo=numpy&logoColor=white"/>
  <img src="https://img.shields.io/badge/Labelme-FFB000?style=flat&logo=OpenCV&logoColor=white"/>
  <img src="https://img.shields.io/badge/GCP-4285F4?style=flat&logo=googlecloud&logoColor=white"/>
</p>

## 🔗 관련 링크

- 📂 **Repository**: [View on GitHub](https://github.com/sbinhigher/image_labeling_project)
- 📝 **Model Training Summary**: *(작성 중 또는 노션 링크 가능)*

## 📌 Pain Point & 개선 방안
> - ## 프로젝트 Pain Point 및 해결 방법

##### Pain Point 1: 대용량 고해상도 이미지 데이터 처리 어려움
- 48MP 고해상도 이미지로 인해 데이터 처리 및 저장이 무거웠음  
- 라벨링 작업에 소요되는 시간과 검수 부담이 큼

**해결 방법**  
- 최적화된 이미지 리사이징 (0.5~0.8배, 0.75배 최종 선정) 및 정방형 크기로 데이터 경량화  
- Instance Segmentation 방식 채택으로 결함 특성 세분화 및 라벨링 품질 향상  
- 외부 인력과 엔지니어의 3회 검수 및 피드백 체계 구축

##### Pain Point 2: 일부 결함 신뢰도 저하 및 결함 예측 데이터 부재
- 다발성 결함 탐지 시 신뢰도가 낮음  
- SCADA 로그 데이터 권한 문제로 결함 발생 예측에 어려움 존재

**해결 방법**  
- ‘다발성 결함’ 카테고리 신설로 기준 명확화  
- SCADA 데이터 협조 불가에 따라 이미지 기반 탐지 솔루션 고도화에 집중  
- YOLOv7-seg 모델 기반 하이퍼파라미터 튜닝 및 이미지 증강 적용

##### Pain Point 3: 비라벨링 이미지 데이터 활용 및 데이터 분할 문제
- 라벨링 되지 않은 이미지 데이터의 활용 방안 마련 필요  
- 효율적인 Train-Validation-Test 데이터셋 분할 필요

**해결 방법**  
- 비라벨링 이미지셋에서 20% 샘플링 활용해 모델 성능 개선 시도  
- 각 호기 및 파트별로 균등하게 샘플링하여 데이터셋 분할 (8:1.5:0.5)

---
## Skills
### 🖥️ Languages & Environment
> ![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![R](https://img.shields.io/badge/R-276DC3?style=for-the-badge&logo=r&logoColor=white)
>>#### Data Handling & Preprocessing
>>![pandas](https://img.shields.io/badge/pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![numpy](https://img.shields.io/badge/numpy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
>>
>>#### Data Crawling
>>![requests](https://img.shields.io/badge/requests-2e6b73?style=for-the-badge&logo=python&logoColor=white)
![selenium](https://img.shields.io/badge/selenium-43B02A?style=for-the-badge&logo=selenium&logoColor=white)
>>
>>#### Image Processing
>>![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white)
![Pillow](https://img.shields.io/badge/Pillow-FFD343?style=for-the-badge&logo=python&logoColor=white)
![ImageAI](https://img.shields.io/badge/Image-2B3E50?style=for-the-badge&logo=python&logoColor=white)
![YOLO](https://img.shields.io/badge/YOLOv7-FF6600?style=for-the-badge&logo=python&logoColor=white)
>
> ![JupyterLab](https://img.shields.io/badge/JupyterLab-F37626?style=for-the-badge&logo=jupyter&logoColor=white)
![VS Code](https://img.shields.io/badge/VS%20Code-007ACC?style=for-the-badge&logo=visualstudiocode&logoColor=white)
![Colab](https://img.shields.io/badge/Colab-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=white)
### 💾 Database & Querying
> ![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)

### 📊 Visualization & Tool
>![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
>> #### Libraries
>>![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=for-the-badge&logo=matplotlib&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-49A2A6?style=for-the-badge&logo=python&logoColor=white)
![Plotly](https://img.shields.io/badge/Plotly-3F4F75?style=for-the-badge&logo=plotly&logoColor=white)
>
>![Tableau](https://img.shields.io/badge/Tableau-00539F?style=for-the-badge&logo=tableau&logoColor=E97627)
### 🛠️ Team Collaboration Tool
> ![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)
![Notion](https://img.shields.io/badge/Notion-000000?style=for-the-badge&logo=notion&logoColor=white)
![Slack](https://img.shields.io/badge/Slack-4A154B?style=for-the-badge&logo=slack&logoColor=white)
![Asana](https://img.shields.io/badge/Asana-E51C23?style=for-the-badge&logo=asana&logoColor=white)


