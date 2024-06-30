## Capstone Project : Temperature Forecast for Five Asian Cities in the Year 2100
### latest version : 2024/06/30 by JuYeon

### 📌 Description
- 아시아 5개 도시(Seoul, Shanghai, Tokyo, Bangkok, Jakarta)의 2100년 기온 예측
- Time Series Forecasting을 위해 고안된 Deep Learning 모델 사용
- Data from **Berkely Earth**(https://berkeleyearth.org/data/)
    - Use **local temperature**
- Data from **Our World in Data**(https://ourworldindata.org/grapher/global-primary-energy)
    - Use **SSP scenario**
- Framework : **PyTorch**
- model type : Temporal Fusion Transfomer(TFT) / N-BEATS / Transformer / Prophet
- Flow Chart
<img src="./plot/FlowChart.png">

### 📌 Result
- TFT 모델과 N-BEATS 모델이 테스트 기간 5년에 대하여 가장 납득할 만한 성능을 보여줌
<img src="./plot/MAPE_compare.png">
- 따라서, TFT 모델과 N-BEATS 모델로 2100년 기온 예측 진행
<img src="./plot/nbeats_total_plot.png">
<img src="./plot/tft_total_plot.png">


### 📌 Directorys & Files
- DATA/RAW : raw data (**.mat** files)
- DATA/DataFrame : extracted charge and capacity data ( **.csv** files )

- Train_SCModels : training Models using B0006/B0007/B0018's voltage data only & Predict B0005's capacity (single-channel)
- Train_MCModels : training Models using B0006/B0007/B0018's voltage, current, temperature & Predict B0005's capacity (multi-channel)
- Train_Other_MCModels : Predict Other Cells (EX: train B0005/B0007/B0018 & Predict B0006)

- BEST_MODEL : parameters of best models ( **.pt** files)
- PREDICT_B0005 : prediction of B0005's capacity
- PREDICTION_PLOP : B0005, B0006, B0007, B0018에 대한 모든 예측 시각화


### 📌 Conclusion
<img src="./PREDICTION_PLOT/B0005_plot.png">
<img src="./PREDICTION_PLOT/B0006_plot.png">
<img src="./PREDICTION_PLOT/B0007_plot.png">
<img src="./PREDICTION_PLOT/B0018_plot.png">
