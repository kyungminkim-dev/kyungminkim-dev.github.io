# day15 학습정리

## [DLBasic] Generative Model

* Learning a Generative Model
    * Suppose we are given images of dogs.

    * We want to learn a probability distribution $p(x)$ such that

        * Generation : If we sample $x_{new} \sim p(x), x_{new}$ should look like a dog(sampling)

        * Density estimation : $p(x)$ should be high if $x$ looks like a dog, and low otherwise (anomaly detection) (Also known as, explicit models).

            ```
            explicit model : 단순히 generation만 하는 모델이 아닌 이미지가 주어졌을 때, 
            어떤 것인지 확률까지 구해주는 모델. 
            단순히 generation만하는 모델은 implicit model.
            ```


            * *density estimation 이란?*

                ```
                In probability and statistics, density estimation is the construction of an estimate, 
                based on observed data, 
                of an unobservable underlying probability density function.   (wikipedia)
                ```
            
            * *Anomaly detection 이란?*
                ```
                In data analysis, 
                anomaly detection(outlier detection) is the identification of rare items, 
                events or observations which raise suspicions by differing significantly from the majority of the data. (wikipedia)
                ```
                

        * Unsupervised representation learning : We should be able to learn what these images have in common, e.g, ears, tail, etc (featuer learning).

        * Then, how can we represent $p(x)$?

* Basic Dscrete Distribution 

    * Bernoulli distribution : (biased) coin flip

        * D = { Heads, Tails}

        * specify $P(X=heads) = p$. Then $P(X=Tails) = 1-p$

        * Write : $X \sim Ber(p)$

        
    * Categorical distribution : (biased) m-sided dice

        * D = {1,...,m}

        * Specify $P(Y=i) = p_i, such\space that \sum_{i=1}^{m}=1$

        * Writhe : $Y \sim Cat(p_1,...,p_m)$

    *확률을 표현하는데 parameter는 확률변수의 값은 n-1개가 필요. 전체 1에서 나머지를 빼주면 확률이 나오니까*

    
