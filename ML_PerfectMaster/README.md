## ML_PerfectMaster
  

 ### 1. Basic 
  - numpy
  - pandas
  
  ### 2. Scikit learn
  - scikitlearn Iris Data
  - scikitlearn API & Datasets
    - **⭐️ `Estimator (fit, predict)` > Classifier, Regressor**
      - scikitlearn 에선 Estimator 라는 부모 클래스에서 classifier, regressor 를 만들기 때문에 `BaseEstimator` 라는 클래스를 상속받아 dummyclassifier, dummyregressor 만들 수 있음
  - scikitlearn model selection
    - train_test_split
    - 교차 검증 (KFold, Stratified KFold)
      - **⭐️분류 모델은 Stratified KFold로!**
      - **⭐️불균형한 분포를 가진 레이블 데이터 집합을 위한 K-fold**
    - 교차 검증 성능 평가 (cross_val_score, GridSearchCV)
      - CV 결과 vs 테스트 데이터 정확도
        1. 학습 데이터와는 중요 피처의 분포도를 달리하여 테스트 데이터를 만들었을 때 얼마나 성능이 일관성 있게 나타나는가?
        2. 동시에 학습 데이터와 비슷한 유형으로 테스트 데이터를 생성해서 검증(validation) 결과와는 얼마나 달라지는가?

        *이런 요소들을 감안해서 여러번 테스트 데이터로 테스트를 수행합니다. 즉 테스트 데이터를 어떻게 만들었느냐에 따라서 결과가 달라질 수 있고, 최적 하이퍼 파라미터가 또 달라질 수 있습니다.*
        *하지만 일반적으로는 CV 결과를 Baseline으로 생각하여, 최적으로 튜닝이 된것으로 간주합니다. 이 기반에서 테스트 데이터 세트의 유형에 따라서 모델 성능이 어느정도 변동성을 가지는지를 확인하는 것 역시 중요한 평가 지표 입니다.*
  
  ### 3. Evaluation
  - Accuracy, Confusion Matrix, Precision, Recall, ROC Curve
    - **⭐️ 불균형한 레이블 클래스를 가지는 이진 분류 모델에서는 많은 데이터 중에서 중점적으로 찾아야 하는 매우 적은 수의 결괏값에 Positive를 설정해 1값을 부여함!**
    - ex) 스팸메일 : 스팸인 경우 1, 정상 메일인 경우 0
    - 정밀도 또는 재현율이 특별히 강조돼야 할 경우, `Binarizer`를 이용하여 분류의 결정 임계값(Threshold)을 조정해 정밀도 또는 재현율의 수치를 높일 수 있음
      
  ### 4. Classification
  - DecisionTree
    - 과적합 방지를 위한 hyperparameter : max_depth, min_samples_split, min_samples_leaf
    - max_features : default = none(전체 feature 수)
  - Ensemble : 여러개의 weak learner 를 결합
    - Voting : 서로 다른 알고리즘의 여러 개의 분류기(weak learner)를 결합
    - Bagging : 동일한 여러개의 분류기(weak learner)를 결합 
      - ex. RandomForest (여러 개의 Decision Tree 결합)
        - n_estinators : weak learner의 개수
        - max_features : default = `sqrt(전체 feature 수)`

    - Boosting: 여러 개의 학습기를 "순차"적으로 학습 & 예측하여 잘못 예측한 데이터에 가중치 부여를 통해 오류를 개선해 나가면서 학습
      - GradientBoosting : 경사하강법을 이용해서 가중치 업데이트 (⭐️`learning_rate`)
      - XGBoost (eXtra Gradient Boost) : Regularization, Tree Pruning, Early Stopping, Cross validation, Null 값 처리 등 지원
      - LightGBM : `Leaf Wise` (계속 같은 방향성을 갖고 Leaf node 를 늘려감)
  - Stacking (CV 기반 Stacking): 앙상블과 유사하나, 기반 모델들이 예측한 값들을 stacking 형태로 만들어 "메타 모델"이 이를 학습하고 예측하는 모델
      
  
  ### 5. Regression
  ### 6. Dimension Reduction
  ### 7. Clustering
  ### 8. Text Analysis
  ### 9. Recommendation

  Reference
  * 파이썬 머신러닝 완벽 가이드
  
***
