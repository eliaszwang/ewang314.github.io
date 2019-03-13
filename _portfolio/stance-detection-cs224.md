---
title: "Stance Detection for Fake News Identification"
excerpt: ""
collection: portfolio
paperurl: 'https://ewang314.github.io/files/stance-detection-cs224n.pdf'
date: 2017-03-01
citation: 'Mrowca, D., **Wang, E.**, Kosson, A. Stance Detection for Fake News Identification. *Stanford NLP with Deep Learning (CS 224N) Project*, 2017'
---
Abstract
======

The latest election cycle generated sobering examples of the threat that fake news poses to democracy. Primarily disseminated by hyper-partisan media outlets, fake news proved capable of becoming viral sensations that can dominate social media and influence elections. To address this problem, we begin with stance detection, which is a first step towards identifying fake news. The goal of this project is to identify whether given headline-article pairs:  (1)agree, (2)disagree, (3)discuss the same topic, or (4) are not related at all. Our method feeds the headline-article pairs into a bi-directional LSTM which first analyzes the article and then uses the acquired article representation to analyze the headline.  On top of the output of the conditioned bi-directional LSTM, we concatenate global statistical features extracted from the headline-article pairs. We report a 9.7% improvement in the Fake News Challenge evaluation metric and a 22.7% improvement in mean F1 compared to the highest scoring baseline.  We also present qualitative results that show how our method outperforms state-of-the art algorithms on this challenge.
{: .text-justify}
