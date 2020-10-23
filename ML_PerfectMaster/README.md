## ML_PerfectMaster
  

  1. Basic 
      - numpy
      - pandas
  2. Scikit learn
      - scikitlearn Iris Data
      - scikitlearn API & Datasets
        - ⭐️ Estimator (fit, predict) > Classifier, Regressor
          - scikitlearn 에선 Estimator 라는 부모 클래스에서 classifier, regressor 를 만들기 때문에 BaseEstimator 라는 클래스를 상속받아 dummyclassifier, dummyregressor 만들 수 있음
      - scikitlearn model selection
        - train_test_split
        - 교차 검증 (KFold, Stratified KFold)
          - ⭐️분류 모델은 Stratified KFold로!
          - ⭐️불균형한 분포를 가진 레이블 데이터 집합을 위한 K-fold 
        - 교차 검증 성능 평가 (cross_val_score, GridSearchCV)
          - CV 결과 vs 테스트 데이터 정확도
            1. 학습 데이터와는 중요 피처의 분포도를 달리하여 테스트 데이터를 만들었을 때 얼마나 성능이 일관성 있게 나타나는가?
            2. 동시에 학습 데이터와 비슷한 유형으로 테스트 데이터를 생성해서 검증(validation) 결과와는 얼마나 달라지는가?
            
            *이런 요소들을 감안해서 여러번 테스트 데이터로 테스트를 수행합니다. 즉 테스트 데이터를 어떻게 만들었느냐에 따라서 결과가 달라질 수 있고, 최적 하이퍼 파라미터가 또 달라질 수 있습니다.*
            *하지만 일반적으로는 CV 결과를 Baseline으로 생각하여, 최적으로 튜닝이 된것으로 간주합니다. 이 기반에서 테스트 데이터 세트의 유형에 따라서 모델 성능이 어느정도 변동성을 가지는지를 확인하는 것 역시 중요한 평가 지표 입니다.*
  3. Evaluation
    - Accuracy, Confusion Matrix, Precision, Recall, ROC Curve
      - ⭐️ 불균형한 레이블 클래스를 가지는 이진 분류 모델에서는 많은 데이터 중에서 중점적으로 찾아야 하는 매우 적은 수의 결괏값에 Positive를 설정해 1값을 부여함!
      - ex) 스팸메일 : 스팸인 경우 1, 정상 메일인 경우 0
      - 정밀도 또는 재현율이 특별히 강조돼야 할 경우, Binarizer를 이용하여 분류의 결정 임계값(Threshold)을 조정해 정밀도 또는 재현율의 수치를 높일 수 있음
      
  4. Classification
  5. Regression
  6. Dimension Reduction
  7. Clustering
  8. Text Analysis
  9. Recommendation

  Reference
  * 파이썬 머신러닝 완벽 가이드
  
***
