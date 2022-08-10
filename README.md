# SVCvsLOGREG_tradingalgorithm
trading algorithm testing support vector machines and logistic regression

Tuning of the training data time frame, and moving average windows(time). 

Original Inputs:

-short_window = 4 days 
-long_window = 100 days 
![DD7E473A-5AA2-4F54-82C0-4789BC25AF91_4_5005_c](https://user-images.githubusercontent.com/98767273/183766532-0f2639f5-916e-4f10-8a93-bd0b72b97510.jpeg)

-'months=3' as parameter in DateOffset()
![3930F424-6288-4B62-87BA-018AD44224D8_4_5005_c](https://user-images.githubusercontent.com/98767273/183766688-bdec5e03-7c4e-4303-9615-408a7e76854f.jpeg)

Original Output(Predictions):
![0A916BD2-F7D7-4968-849D-39EDBC33C308](https://user-images.githubusercontent.com/98767273/183767508-f4508ecd-e0e6-4058-9e5a-8ba58bc57980.jpeg)

Input Change #0:

-short_window = 4 days 
-long_window = 100 days 
![DD7E473A-5AA2-4F54-82C0-4789BC25AF91_4_5005_c](https://user-images.githubusercontent.com/98767273/183776493-9305b18c-46cf-4605-8bc8-ed5e8526ef03.jpeg)

-'months=6' as parameter in DateOffset()
![5FEBFB29-A933-413D-9404-1E6DD8ACA7E6_4_5005_c](https://user-images.githubusercontent.com/98767273/183776597-dd2894a7-1d60-4a2d-b7e9-edda6f3a8b70.jpeg)

Output #0:
![B463AB7B-615E-408E-A70A-82345D8D6BBC](https://user-images.githubusercontent.com/98767273/183776669-a6290349-4107-4335-a30e-ee91d429660a.jpeg)

Change Occured #0:
Changing the Offset of the training period from 3, to 6 months caused the Algorithm to over-predict the trend reversals; meaning between 2018-2020 when the trend became bearish it predicted the returns lower than the actual returns, and when the market trend revered to a bullish trend it predicted returns over the actual returns. Where before it was predicting a higher return then the actual return for bullish and bearish trend reverals.

Input change #1:

-short_window = 4 days 
-long_window = 100 days 
![DD7E473A-5AA2-4F54-82C0-4789BC25AF91_4_5005_c](https://user-images.githubusercontent.com/98767273/183766532-0f2639f5-916e-4f10-8a93-bd0b72b97510.jpeg)

-'months=1' as parameter in DateOffset()
![BA7DBBE9-B886-41B7-A440-E479D010E95E_4_5005_c](https://user-images.githubusercontent.com/98767273/183777940-03d7b8cd-2281-4abd-95b0-31c0cfbbb46d.jpeg)

Output #1:
![4CF11DD2-5D2D-43EE-8462-7F59C79FAEC2](https://user-images.githubusercontent.com/98767273/183778025-e02dff97-b0b9-466a-a079-b1a8b878faad.jpeg)

Change Occured #1:
Changing the Offset of the training period to 1 month caused for the algorithm to overpredict the returns when the the chart was trading sideways from 2016-2018 to where when the offset was 3, and 6 the algorithm predicted 2016-2018 nearly perfectly.  With the offset of 1 month the algorithm overpredicted every return from 2016-2021 (.1%)-(1%) over the actual returns.

Input Change #2:

-short_window = 4 days 
-long_window = 100 days 
![DD7E473A-5AA2-4F54-82C0-4789BC25AF91_4_5005_c](https://user-images.githubusercontent.com/98767273/184022776-a23c0397-a49f-4383-ba79-2801c85f9528.jpeg)

-'month=2' as parameter in DateOffset()
![AF6BC40E-649C-4723-B393-CC9A08342EDF_4_5005_c](https://user-images.githubusercontent.com/98767273/184023191-fc183b46-f685-4cb3-a7bf-7cee82bf77d9.jpeg)

Output #2:
![E1BDEC4A-7AA5-4536-B200-0661F519422E](https://user-images.githubusercontent.com/98767273/184023259-6029a997-5164-4b44-8443-98487d31202c.jpeg)

Change Occured #2:
