## class 4

installing and using R packages

\- for installation, you need internet

-   install a package once

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

#alternatively use

```{r}
install.packages("tidyverse")
```

```{r}
glimpse(d1)
```

```{r}
#dimension
dim(d1)
```

```{r}
#data types
typeof(d1$minutes_to_nearest_facility)
```

```{r}
#attributes
attributes(d1)
```

```{r}
#summary

summary(d1)

```

```{r}
table(d1$residence)
```

#look at the smoke status per residence

```{r}
table(d1$county,d1$residence,d1$smoker)
```

```{r}
install.packages("arsenal")
d3 <- tableby(county_residence+smoker+mode_transport_to_nearest_facility,data=d1)
summary(d3)

```

```{r}
class(as.factor(d1$residence))
```

```{r}
#we are changing/ recoding column residence; rural to be 1 and urban to be 2 and changing back
d1$residence <- ifelse(d1$residence == "rural", 1, 2)

d1$residence <- ifelse(d1$residence == 1, "rural", "urban")

View(d1)

table(d1$residence)
```

-   select() - in package dplyr, helps us to select columns in a data frame
-   pipe ( \|\> ) - control+shift+m

```{r}
library(tidyverse)

d2 <- d1 |> 
  select(county, residence, smoker)

dim(d2)
```

```{r}
d3 <- d1 |> 
  select(-c(residence, smoker))

dim(d3)
```

-   Merge data, d2 and d3.
-   We use the function merge()
-   To join the two data sets, we need to have common column name

```{r}
d4 <- merge(d2, d3, by.x = "county", by.y = "county", all.x = TRUE)

dim(d4)
```

# mutate() - which is used to create new columns

#rename()

#visualization #statistical modeling
