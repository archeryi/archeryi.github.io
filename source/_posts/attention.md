---
title: Attention的四种形式
date: 2018-09-06 17:20:04
categories:
- nlp
mathjax: true
---
Attention主要用于关联Seq2Seq模型中的encoder states， 也能用于关联序列模型的past states。通过attention，能够基于隐层状态向量$s\_{1},...,s\_{n}$生成一个向量$c\_{i}$，然后用这个向量和当前隐层向量$h\_{i}$进行prediction。向量$c\_{i}$的计算方式如下：
$c\_{i} = \sum\_{j}a\_{ij}s\_{j}$
$a\_{i} = softmax(f\_{att}(h\_{i}, s\_{j}))$
根据$f\_{att}$函数的不同，attention大体有四种主要的形式。 

## Additive attention

$f\_{att}(h\_{i}, s\_{j}) = v\_{a}^{T}tanh(W\_{a}[h\_{i};s\_{j}$
或者：
$f\_{att}(h\_{i}, s\_{j}) = v\_{a}^{T}tanh(W\_{1}h\_{i} + W\_{2}s\_{j})$

## Multoplicative attention


$f\_{att}(h\_{i}, s\_{j}) = h\_{i}^{T}W\_{a}s\_{j}$

## Self-attention


$f\_{att}(h\_{i}, s\_{j}) = h\_{i}^{T}W\_{a}h\_{i}$

## Key-value attention
不想写了


 
