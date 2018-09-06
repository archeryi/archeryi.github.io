---
title: Attention的四种形式
date: 2018-09-06 17:20:04
tags:
categories: NLP
mathjax: true
---
Attention主要是在seq2seq中将encoder隐层的各个状态通过矩阵相乘作为当前decoder的输入，其基本形式如下，根据$f\_{att}$函数的不同有四种不同的形式。
$c\_{i} = \sum\_{j}a\_{i,j}s\_{j}$
$a\_{i} = softmax(f\_{att}(h\_{i}, s\_{j}))$ 
##
 
