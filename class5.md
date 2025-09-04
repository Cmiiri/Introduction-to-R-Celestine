```{r}
ideal <- read.csv("https://raw.githubusercontent.com/ThumbiMwangi/R_sources/master/ideal3a.csv")
```

```{r}
colnames(ideal$CalfSex)
```

```{r}
piping operator
control+shift+r
```

```{r}

```

# selecting

install the pacakages

```{r}
View(ideal)

select.list(calfsex)

```

## Session 5 Visualization

ggplot2 package used for plotting

```{r}
#load required pacakages
install.packages("ggplot2")
#then call
library(ggplot2)


```

datasets

coordinate system

geometry

```{r}

```

bar graph

geom_bar() only takes one variable

geom_col() takes more than one variable

```{r}
ggplot(data=ideal,)
```

count/tally how many

```{r}
df <- ideal
select(sublocation)
group_by
```
