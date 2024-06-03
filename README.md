# ml-decision-tree-proj

:::::::::::::: columns
::: {.column width="50%"}
![](figs/explain.png){width=100%}
:::

::: {.column width="50%"}
- Two things need to be determined at each node: feature and threshold. 
- Thresholds can be values of training samples on a feature. 
- Exhaustive search. Complexity: O(NM), $N$: number of features, $M$: number of samples. 
:::
::::::::::::::

- Intuition: Each node cuts the plane into two halves. It's better to have less mixture of two classes on each half. 
- Given a Boolean condition $S$, Gini impurity is $g(S) =  \sum_{c=\pm1} 
Pr(class=c| S) \cdot (1-Pr(class=c| S)) = 1 - \sum_{c=\pm1} Pr^2(class=c| S)$. If all samples belong to one class, then $g(S)=0$ thus least impure and hence most pure. 

title: | 
         CS 474/574 Machine Learning \
         3. Decision Trees
author: |
          Prof. Dr. Forrest Sheng Bao
