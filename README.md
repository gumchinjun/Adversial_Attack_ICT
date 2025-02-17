# 🚢 적대적 AI 공격에 대한 해양선박 보안 강화 연구
## A Study on Strengthening the Security of Marine Ships against Adversarial AI Attacks

### 📄 논문 정보
학술대회: 한국정보처리학회 ACK 2024 학술발표대회 논문집  <br/>
저자: 전준석, 김희준, 이현화, 윤다영, 박지우, 이규영  <br/>
주제: 자율운항선박 시스템의 보안 강화를 위한 적대적 AI 공격 및 방어 전략 연구  <br/>
프로젝트 지원: 해양수산부 실무형 해상물류 일자리 지원사업 (스마트해상물류 x ICT멘토링)  <br/>

### 🛠 연구 개요 (Overview)
자율운항선박은 점점 발전하고 있지만, 적대적 AI 공격(Adversarial Attacks)에 취약함.  <br/>
본 연구에서는 주요 적대적 공격 기법 5가지를 구현하고, 적대적 훈련(Adversarial Training)을 통한 방어 효과를 분석.  <br/>

### 🔥 주요 연구 내용 (Key Findings)
#### 1️⃣ 적대적 공격 기법 (Adversarial Attack Methods)
다음 5가지 공격 기법을 활용하여 해양선박 AI 모델을 공격.  <br/>
1. FGSM (Fast Gradient Sign Method):	모델의 손실 함수의 기울기를 이용해 작은 노이즈(ε)를 추가하는 단순한 공격  <br/>
2. BIM (Basic Iterative Method):	FGSM을 여러 번 반복하여 더 정교한 적대적 예제를 생성  <br/>
3. PGD (Projected Gradient Descent):	무작위 시작점을 이용하여 더욱 강력한 공격 수행  <br/>
4. DeepFool:	결정 경계를 최소한으로 넘는 미세한 노이즈로 공격  <br/>
5. JSMA (Jacobian-based Saliency Map Attack):	중요도가 높은 픽셀을 조작하여 모델을 속이는 공격  <br/>
#### 2️⃣ 방어 기법: 적대적 훈련 (Defense: Adversarial Training)
적대적 훈련(Adversarial Training)은 공격을 받은 적대적 예제를 학습 데이터에 포함하여 모델이 강인함을 갖도록 하는 기법.  <br/>
실험 결과, 적대적 훈련 적용 후 모델이 높은 정확도를 유지하여 효과적인 방어 기법임을 입증함.  <br/>
#### 3️⃣ 실험 결과 (Experimental Results)
- 데이터셋: Kaggle ‘Game of Deep Learning: Ship Datasets’  <br/>
- CNN 기반 모델을 사용하여 선박(화물선, 군함, 항공모함, 크루즈선, 유조선) 분류  <br/>

#### 적대적 훈련 적용 전/후 성능 비교
| 공격 기법 (Method) | 공격 전 정확도 (Before) | 공격 후 정확도 (After) |
|-------------------|----------------------|----------------------|
| **FGSM**        | 0.1855               | 0.7818               |
| **BIM**         | 0.2137               | 0.6679               |
| **PGD**         | 0.1312               | 0.9168               |
| **DeepFool**    | 0.2398               | 0.8407               |
| **JSMA**        | 0.2400               | 0.8217               |

- PGD 공격이 가장 강력했으며, CNN 모델의 정확도가 **13.12%까지 감소**함  
- 하지만 **적대적 훈련(Adversarial Training) 적용 후**, PGD 공격에서도 **91.68%의 높은 정확도**를 유지하여 방어 성능을 입증함

### 📌 결론 (Conclusion)
✅ 자율운항선박 AI 모델은 적대적 공격에 취약하지만, 적대적 훈련을 통해 보안성을 강화할 수 있음을 입증 <br/>
✅ 다양한 적대적 공격 기법을 적용하여 실제 해양산업에서 발생할 수 있는 위협을 분석  <br/>
✅ 향후 연구에서는 다양한 방어 기법(예: 입력 변환, 모델 앙상블)과 결합하여 보안성을 더욱 향상할 예정 
