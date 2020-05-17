## Tutorial

### ARIMA 와 PROPHET
<pre>
ARIMA
    AR(autoregression):
        자기 자신의 과거 정보로 사용하는 개념.'현재의 상태는 이전의 상태를 참고해서 계산된다.'라는 아이디어를 전제로 한다.
    MA(moving average):
        이전 항에서의 오차를 이용하여 현재 항의 상태를 추론 하겠다.
        AR,MA 를 합친것이 ARMA 모델이라고하며, 조금 더 발전된 ARIMA(integrated) 모델은 ARMA 모델에 추세 변동의 경향성(momentum) 까지 반영한 방법이다. 

PROPHET
    ARIMA 보다 좀 더 정확한 트렌드 예측 분석을 제공하는 PROPHET
    additive 모델이라는 모델링 방법에 기반한 시계열 예측 모델로서, 
    시계열 데이터의 트렌드성(연간/월간/일간) 을 예측하는 것에 초점을 맞추어져 있다.

    seasonality_mode: 연간,월간,주간,일간 등의 트렌드성을 반영하는것을 의미
    changepoint_prior_scale:트렌드가 변경되는 문맥을 반영하는 파라미터,
        수치가 높을수록 모델은 과적합에 가까워진다.
</pre>

### Google colab 사용
<pre>
1. 구글 드라이브에서 새로 만들기 -> colab 파일 생성
2. 런타임 -> 런타임 유형 -> GPU , python3
3. 구글 드라이브 마운트:
	from google.colab import drive
	drive.mount('/drive')
	//위코드 실행시 인증코드 입력창과, 인증 링크가 생성됨
	//생성된 리크를 클릭하여 계정을 선택하고, 허용을 해주면 인증코드를 발급 받는다.
	//해당 인증은 유효 기간이 있기 때문에 유효기간이 끝나면 다시 발급 해주어야 한다.

4. 드라이브 파일 리스트 보기
!ls '/drive/My Drive'

//'/drive/My Drive/<원하는 디렉토리 혹은 파일>
!ls '/drive/My Drive/study/deeplearning'

5. colab 에서 패키지 설치
!pip install fbprophet
</pre>
