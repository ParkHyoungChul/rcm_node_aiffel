
<img width="387" height="202" alt="image" src="https://github.com/user-attachments/assets/bd9b1d89-2258-4d19-849d-9e7f7830abf9" />

## 가상환경 설정

* 새로운 가상환경을 생성한 뒤, 아래 버전으로 진행해 주세요.
  (권장: `Python 3.11`, `TensorFlow 2.15.0`)

```bash
pip install tensorflow
pip install streamlit numpy pandas joblib scikit-learn tqdm
```

## 실행 방법

* 프로젝트 폴더 안에서 다음 명령어로 실행해 주세요.

  * `show_st.py`: Lecture 모델(AutoInt) 스트림릿 실행 코드
  * `show_st_plus.py`: Project 모델(AutoInt_MLP) 스트림릿 실행 코드

```bash
streamlit run show_st.py
```

## 노트북 코드 설명


* `model_load_test.ipynb` **모델이 정상적으로 로드되는지 확인**하는 코드입니다.

  > 바로 Streamlit으로 실행하면 에러가 생겼을 때 디버깅이 번거로울 수 있으므로, 먼저 이 코드로 확인하세요.

* `autoint_mlp_train.ipynb` **AutoInt_MLP 모델을 학습시키고 가중치를 저장하는 코드**입니다.

  > 이미 학습된 가중치 파일도 함께 전달드렸지만, 새 모델을 만들고 아키텍쳐를 바꾸며 학습할때는 해당 코드를 참고하시기 바랍니다.
  > !주의! : 이 학습파일에서 모델 아키텍쳐를 변경했다면 `autointmlp.py`이 파일에서도 같은 형태로 변경을 해주셔야합니다

## 추가로 진행해야 할 작업

* 모델의 **성능 향상을 위한 다양한 시도**를 자유롭게 해보세요!

## 주의사항 및 참고

* **TensorFlow 버전에 따라** 가중치 파일의 확장자가 다를 수 있습니다. (제공되는 코드는 .weights 가 하나씩 더 붙어있습니다)참고해주세요
* 코드 내 `dtype.longlong` 부분은 `int64` 또는 `int32`로 변경되어야 할 수 있습니다. 참고해주세요
* 다양한 오류가 발생하지만 참고 해주세요. 😄
