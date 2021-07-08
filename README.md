# Anomaly Detector API

The Anomaly Detector API enables you to monitor and detect abnormalities in your time series data without having to know machine learning. The Anomaly Detector API's algorithms adapt by automatically identifying and applying the best-fitting models to your data, regardless of industry, scenario, or data volume. Using your time series data, the API determines boundaries for anomaly detection, expected values, and which data points are anomalies.

**Capabilities**
* Detect anomalies in data stream by using previously seen data points to determine if the latest one is an anomaly.
* Use time series to detect any anomalies that might exist throughout the data.

**Prerequisites**
* Azure subscription

**Set-up**
* Log in to the azure portal
* Create an “Anomaly Detector” resource by using the link - [Anomaly detector setup](https://portal.azure.com/#create/Microsoft.CognitiveServicesAnomalyDetector).
* Select Free Tier (F0) for “Pricing tier” while creating the resource.
* Once setup and deployed, get keys and endpoint information by going to the “Keys and Endpoint” menu in the left navigation bar.

**Data**

The Anomaly Detector API accepts time series data formatted into a JSON request object. A time series can be any numerical data recorded over time in sequential order.

**Important terms**
* **Granularity**: rate that the data is sampled at. Refer - [Granularity](https://docs.microsoft.com/en-us/dotnet/api/microsoft.azure.cognitiveservices.anomalydetector.models.granularity?view=azure-dotnet-preview)
* **Sensitivity**: the lower the value is, the larger the margin value will be which means less anomalies will be accepted. Can be number between 0 - 99
* **Custom Interval**: Custom Interval is used to set non-standard time interval, for example, if the series is 5 minutes, request can be set as {"granularity":"minutely", "customInterval":5}.
* **PositiveAnomaly**: A positive anomaly means the point is detected as an anomaly and its real value is larger than the expected one.
* **Negative Anomaly**: A negative anomaly means the point is detected as an anomaly and its real value is smaller than the expected one.

**Important numbers**
* Minimum number of points required: **12**
* Maximum number of points possible: **8640**
* Missing data points: **<10%**
