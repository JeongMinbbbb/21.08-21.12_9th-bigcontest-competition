# 21.08-21.12_BigContest_1st
## 주제 : KBO 배럴 정의 및 타자 성적 예측
- 2021 빅콘테스트 공모전 데이터분석분야 챔피언리그 스포츠테크
- 데이터 분석 경진대회 최대 규모(전체 1307개 팀 참가)

### **분석 목적**

- 목표 1 : 미국 리그에서 파생된 배럴 지표(좋은 타구의 생산 빈도)의 국내 도입 적합성 검토
- 목표 2 : 한국형 배럴을 정의하고, 이를 활용하여 타자의 시즌 잔여 경기 성적을 예측
- 목표 3 : 성적 예측 모델을 기반의 활용 인사이트 도출

*** 
### **분석 과정**
1. 한국형 배럴 지표 정의
- 기존 배럴 지표의 국내 도입 적합성 검토
- 두 리그 간 타율 및 장타율 차이를 추정하여 한국형 배럴 지표에 반영
   - 8년치 데이터를 통해 추정된 신뢰구간들이 공통적으로 포함하는 범위를 계산
   - 해당 범위의 중앙값인 0.026을 타율 차이의 대표값으로 채택
- 한국형 배럴의 선별 기준점을 타율 0.526, 장타율 1.5로 정의
- 야구장의 비거리와 담장 높이를 계산하여 물리적인 가능성을 추가로 반영
2. 성적 예측 모델링
- 야구 데이터의 특성을 반영한 통계 기법인 지수평활법을 활용하여, 미래 시점의 잔여 경기를 대표하는 데이터셋을 생성
- 최적의 변수들을 선정하여 XGBoost와 Random Forest로 기존 데이터를 예측 모델에 학습시킴
- 생성한 잔여 경기 데이터셋을 모델에 입력하여 최종 성적 예측치를 도출
3. 활용방안 모색
- 선수 예시를 들어 전략에 활용하는 방법 제안
   - 저평가 선수 발굴 : ex)노시환과 페르난데스 비교

*** 
### **분석 결과 및 성과**
1. 타자 성적 예측 모델의 성능
   - 출루율의 R-squared는 0.896, MAE는 0.0141
   - OPS의  R-square는 0.971, MAE는 0.0211
2. 성과 : 252개 팀 중 상위 6% 달성, 모델의 설명력이 30%p 향상

***
***
***
### Team Project

#### Teaming   (팀장)배정민, 이한재, 조용민 ,김해인 ***(in Dongguk_University_Stat)***
