# Boom Bikes Demand Analysis  
> Analyzing factors affecting shared bike demand to optimize business strategy and boost revenue.  

---

## Table of Contents  
* [General Info](#general-information)  
* [Technologies Used](#technologies-used)  
* [Conclusions](#conclusions)  
* [Acknowledgements](#acknowledgements)  

---

## General Information  

**Problem Statement**:  
BoomBikes, a US-based bike-sharing provider, has faced significant revenue dips during the COVID-19 pandemic. To recover, they aim to understand the factors influencing bike-sharing demand post-lockdown, allowing them to align their business strategy with customer needs.  

**Business Goal**:  
The primary goals are:  
1. Build a predictive model to accurately forecast bike-sharing demand.  
2. Identify significant factors affecting demand to help the management adjust strategies accordingly.  

**Dataset**:  
The dataset contains daily bike demand figures across the US, influenced by meteorological data and people's behavioral patterns.  

**Approach**:  
The analysis uses **Multiple Linear Regression** with the following steps:  
- **Feature Selection**: Combined algorithmic and manual selection to determine the 10 most significant predictors using Recursive Feature Elimination (RFE), multicollinearity checks, and statistical significance testing.  
- **Model Building**: The final model explains **84% of variability in training data** and achieves **81% accuracy on test data**.  
- **Validation**: Residual analysis, multicollinearity verification, and cross-validation ensure model reliability.  

---

## Conclusions  

- **Key Predictors**:  
  The most significant factors affecting bike-sharing demand are:  
  1. Year (`yr`): Demand has increased over time.  
  2. Temperature (`temp`): Higher temperatures positively correlate with demand.  
  3. Humidity (`hum`): High humidity negatively affects demand.  
  4. Windspeed (`windspeed`): Higher wind speeds reduce demand.  
  5. Seasonal Effects: Demand spikes in winter and weekends (e.g., Saturdays).  
  6. Working Day: Demand is higher on working days compared to holidays.  
  7. Precipitation: Light snow/rain has a negative impact on demand.  

- **Model Performance**:  
  - Training R²: 84%  
  - Testing R²: 81%  
  - Stability: ±14% at 95% confidence interval (validated through cross-validation).  

- **Insights for Business Strategy**:  
  - Focus marketing efforts during winter and weekends when demand peaks.  
  - Offer discounts or incentives during adverse weather conditions to sustain demand.  
  - Optimize bike availability on working days to cater to commuting needs.  

---

## Technologies Used  

- **Python**  
  - pandas - version 1.3.3  
  - numpy - version 1.21.2  
  - matplotlib - version 3.4.3  
  - seaborn - version 0.11.2  
  - statsmodels - version 0.13.0  
  - scikit-learn - version 1.0  

---

## Acknowledgements  

- **Inspiration**:  
  This project was inspired by the challenges posed by the pandemic to small and mid-sized businesses.  
- **References**:  
  - Dataset provided by BoomBikes.  
  - [Linear Regression Tutorial](https://www.statsmodels.org/stable/examples/index.html)  

---

## Contact  
Created by [@NavutheAgarwal] - feel free to reach out!  

---

### Notes on Model Assumptions and Validation:  

- **Residual Analysis**: Residuals follow a normal distribution, satisfying the assumptions of linear regression.  
- **Multicollinearity**: Verified using VIF values. Non-significant predictors were removed.  
- **Cross-validation**: Ensures model stability and generalizability.  


