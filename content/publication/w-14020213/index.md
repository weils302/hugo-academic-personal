---
title: Investigation of Hyperparameter Setting of a Long Short-Term Memory Model
  Applied for Imputation of Missing Discharge Data of the Daihachiga River
subtitle: ""
publication_types:
  - "2"
authors:
  - " Weilisi"
  - Toshiharu Kojima
doi: 10.3390/w14020213
publication: "*Water*"
abstract: "Missing observational data pose an unavoidable problem in the
  hydrological field. Deep learning technology has recently been developing
  rapidly, and has started to be applied in the hydrological field. Being one of
  the network architectures used in deep learning, Long Short-Term Memory (LSTM)
  has been applied largely in related research, such as flood forecasting and
  discharge prediction, and the performance of an LSTM model has been compared
  with other deep learning models. Although the tuning of hyperparameters, which
  influences the performance of an LSTM model, is necessary, no sufficient
  knowledge has been obtained. In this study, we tuned the hyperparameters of an
  LSTM model to investigate the influence on the model performance, and tried to
  obtain a more suitable hyperparameter combination for the imputation of
  missing discharge data of the Daihachiga River. A traditional method, linear
  regression with an accuracy of 0.903 in Nash&ndash;Sutcliffe Efficiency (NSE),
  was chosen as the comparison target of the accuracy. The results of most of
  the trainings that used the discharge data of both neighboring and estimation
  points had better accuracy than the regression. Imputation of 7 days of the
  missing period had a minimum value of 0.904 in NSE, and 1 day of the missing
  period had a lower quartile of 0.922 in NSE. Dropout value indicated a
  negative correlation with the accuracy. Setting dropout as 0 had the best
  accuracy, 0.917 in the lower quartile of NSE. When the missing period was 1
  day and the number of hidden layers were more than 100, all the compared
  results had an accuracy of 0.907&ndash;0.959 in NSE. Consequently, the case,
  which used discharge data with backtracked time considering the missing period
  of 1 day and 7 days and discharge data of adjacent points as input data,
  indicated better accuracy than other input data combinations. Moreover, the
  following information is obtained for this LSTM model: 100 hidden layers are
  better, and dropout and recurrent dropout levels equaling 0 are also better.
  The obtained optimal combination of hyperparameters exceeded the accuracy of
  the traditional method of regression analysis."
draft: false
featured: true
tags: []
image:
  caption: ""
  focal_point: ""
  preview_only: false
summary: ""
lastmod: 2022-09-28T14:47:03+09:00
date: 2022-09-28T05:53:35.988Z
links:
  - name: URL
    url: https://www.mdpi.com/2073-4441/14/2/213
categories: []
projects: []
publishDate: 2022-09-28T05:47:01.196188Z
---
