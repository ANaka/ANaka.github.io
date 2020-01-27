---
title: "Pandas dummies to categorical trick"
layout: post
date: 2020-01-15
image: /assets/images/
headerImage: false
tag:
- Pandas
- python
- learning
category: blog
author: naka
description:
hidden: True
---

```python
import pandas as pd
df = sns.load_dataset('exercise',index_col=0)
dummies = pd.get_dummies(df['diet'])
dummies.idxmax(axis=1)
```



Being able to convert a matrix of dummy variables into a single categorical column comes in handy in a lot of situations
