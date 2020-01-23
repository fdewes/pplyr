<!--

#################################################
### THIS FILE WAS AUTOGENERATED! DO NOT EDIT! ###
#################################################
# file to edit: index.ipynb
# command to build the docs after a change: nbdev_build_docs

-->

# pplyr

> use the R dplyr package with python

## Install

`pip install pplyr`

## How to use

Create a dplyr command and call pplyr(df, cmd):
<div class="codecell" markdown="1">
<div class="input_area" markdown="1">

```python
df = pd.read_csv("iris.csv", index_col=0)
```

</div>

</div>
<div class="codecell" markdown="1">
<div class="input_area" markdown="1">

```python
cmd = """
df %>% group_by(Sepal.Length, Species) %>% summarize(n = n()) %>% arrange(-n)
"""

df = pplyr(df, cmd)
```

</div>

</div>
