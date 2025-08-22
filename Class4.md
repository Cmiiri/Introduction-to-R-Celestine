## class 4

installing and using R packages

\- for installation, you need internet

 - install a package once

```{r}
#install.packages("tidyverse")
library(tidyverse)


#install package AMR

install.packages("AMR")
library(AMR)
```

#DATA

we have in built data

\>we can load our own datasets

we use data() to access in built data

```{r}
data()
```

\>some data need packages to access

```{r}
#accessing iris
DNase
```

#Loading from the computer

\>First set your working directory using setwd() or get your working directory using getwd()

\>we can have data in .csv or .xls

#Load .csv

```{r}
d1 <- read.csv("dataset_class4.csv")
```

#manipulate data

we can view the contents of d1

```{r}
View(d1)

colnames(d1)
```

```{r}
#first six rows of data
head(d1)
```

```{r}
#last six rows of data
tail(d1)
```

```{r}
library(tidyverse)
```
