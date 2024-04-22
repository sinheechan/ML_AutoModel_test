# ML_AutoModel_test

Custom.model 외 Pycret, Lazy Predict AutoML 모델 세 기법의 인구소득예측 정확도 비교분석
<br/><br/>

<img src="image/income_post.jpeg">
<br/><br/>

## Object

### 1. Model Introduce
<br/>

#### 1.1 Custom ML

> Custom ML 과정에서 데이터 전처리, 모델 선정, 파라미터 조정 등 일련의 과정을 직접 지정하여 학습을 진행합니다.
>
> 본 과정에서는 RandomForest, LGBM, Catboost 세 가지 모델의 성능 비교 및 best.model의 예측 정확도를 기준으로 기술합니다.
<br/><br/>

#### 1.2 PyCaret

> PyCaret은 종합적인 머신 러닝 파이프라인을 제공하는 파이썬 라이브러리입니다.
>
> 다양한 데이터 전처리 기능과 알고리즘 튜닝, 모델 비교, 앙상블 기능 등을 포함합니다.
>
> 사용자 친화적인 API를 통해 머신 러닝 작업을 단순화하고, 코드의 길이를 줄이며, 실험의 반복을 쉽게 만듭니다.
>
> PyCaret은 최신 머신 러닝 알고리즘과 기존의 알고리즘을 지원하며, 다양한 데이터셋에 적용할 수 있습니다.
<br/><br/>

#### 1.3 Lazy Predict
> Lazy Predict는 머신 러닝 모델의 기본 성능을 자동으로 평가하는 Python 라이브러리입니다.
>
> 주어진 데이터에 대해 가능한 모든 일반적인 머신 러닝 모델을 학습하고, 성능 지표를 제공합니다.
>
> 사용자가 일일이 모델을 설정하거나 튜닝할 필요 없이, 간단한 코드로 빠르게 초기 모델 선택을 할 수 있습니다
<br/><br/>

## Dataset

- [Kaggle] 성인 인구조사 소득 예측 Dataset
<br/><br/>

## Libraries used / Version
<br/>

**[PyCaret]**
- pycaret
- sklearn
<br/>

**[Lazypredict]**
- pandas==2.0.3
- numpy>=1.25.0
- autoviz
- scikit-learn==0.23.1
- lazypredict
<br/><br/>

## Result

- 3가지 기법으로 생성한 모델 비교 결과 모델 선정과정에서의 예상 정확도는 LGBM 모델이 best.model로 선정되었습니다.
- 모델 Test 성능 측정 과정 Accuracy의 경우 Custom Model(92%), Pycret(86%), Lazy Predict(0.88)의 성능을 보였습니다.
- 다만, 실제 측정에서는 모든 모델의 예측 정확도가  소폭 감소하는 경향을 보였습니다.
- 앞선 선행자료 분석에서는 Auto 모델을 활용하였을 때 앙상블 모델까지 확장 적용할 때 가장 높은 예측 정확도를 달성하였습니다. 
- 결국 머신러닝 기법에 대한 통찰을 기반으로 학습된 후보 모델을 적합시키는 과정이 모델 성능에 가장 중요한 역할을 할 것으로 판단됩니다.   
