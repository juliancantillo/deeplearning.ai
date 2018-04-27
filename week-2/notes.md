## Week 2

### Binary Classification

It uses Logistic Regretions. Data, Label = [0,1].

Data: x ∈ _R<sup>n<sub>x</sub></sup>_
Label: y ∈ {0, 1} 

In python it works

> X.shape = (n<sub>x</sub>, m)



### Logistic Regression

Given _x_, want `y = P(y=1 | x)` P stands for Probability or Chance

Parameters: w ∈ _R<sup>n<sub>x</sub></sup>_
            b ∈ _R_

Output: `ŷ = σ(w<sup>T</sup>x + b)`

### Logistic Regression Cost Function

Having:

> ŷ = σ(w<sup>T</sup>x + b)

where

> σ(z) = 1 / 1 + _e_<sup>-z</sup>


#### Loss Function

> L(ŷ,y) = -(y log(ŷ) + (1-y)log(1-ŷ))


If y=1: `L(ŷ,y) = -log(ŷ)` <- Want `log(ŷ)` **large**, Want `ŷ` **large**

If y=0: `L(ŷ,y) = -log(1-ŷ)` <- Want `log(ŷ)` **large**, Want `ŷ` **small**

#### Cost Function

> J(w,b) = 1/m ∑<sup>m</sup><sub>i=1</sub> L(ŷ<sup>i</sup>,y<sup>i</sup>) = - 1/m ∑<sup>m</sup><sub>i=1</sub>[(y<sup>i</sup> log(ŷ<sup>i</sup>) + (1-y<sup>i</sup>)log(1-ŷ<sup>i</sup>))]


