---
  title: "Contingency Table Construction Construction"
  description: "Using ggplot2 to learn some basics of R."
---
## Constructing a Contingency Table

```yaml
type: NormalExercise 
lang: r
xp: 100 
skills: 1
key: b99a54db27   
```

Using the `janitor` package, we can construct a contingency table showing the relationships between categorical variables.  In the `janitor` package, the function that does this is called [`tabyl`](https://www.rdocumentation.org/packages/janitor/versions/1.0.0/topics/tabyl).  The first argument it takes is the name of the dataset.  The next two arguments are the row and column variable names respectively.   


`@instructions`
The dataset has been loaded into your workspace as `census_at_school`. It represents survey results from two questions on a random sample of USA high school students.  One question about what superpower they wish they had and another about gender. 

- Load the `janitor` library into your workspace.
- Use the `tabyl()` function to make a contingency table of Superpower versus Gender.  Put Superpower as the rows and Gender as the columns. 

`@hint`
- Remember to put the name of the dataset in your `library()` statement. 
- Simply pass the dataset, `Superpower`, and `Gender` variable into the `tabyl()` function to make your contingency table. 

`@pre_exercise_code`
```{r}
# load datasets and packages here

```


`@sample_code`

```{r}
# Load your library first

# Construct the contingency table

```

`@solution`

```{r}
# Load your library first
library(dplyr)
```

`@sct`

```{r}
# Update this to something more informative.
success_msg("Great job!  You are heading in the right direction!")
```



---
## Investigating the dataset

```yaml
type: NormalExercise
lang: r
xp: 100
skills: 1
key: f8cecbd925
```
The dataset that you are working with is called `state_foreign_born`.  It contains the percentage of individuals in each state who were born in a foreign country.  The `head()` function will help us *investigate* the data set to see what variables are available.   Pass the name of your dataset into the `head()` function and you will see the first 6 rows of the dataset with variable names. 

The `head()` function takes two arguments.  The first argument is the name of the dataset, and the second is how many rows you wish to see.  


`@instructions`
- Use the `head()` function to view the first 10 rows of the dataset. 
- Hit *Run Code* to test your code, and *Submit Answer* when you think you have it right. 

`@hint`
- Remember the `head()` function takes two arguments.  The first is the name of the dataset (which is `state_foreign_born` in this case) and the second is the number of rows you wish to see (if different from 6).


`@pre_exercise_code`

```{r}
# Load datasets and packages here
state_foreign_born<-read.csv("http://s3.amazonaws.com/assets.datacamp.com/production/repositories/3374/datasets/9e5e6297329fe3304830bf454bc9445bd16f9621/state_foreign_born.csv")

```

`@sample_code`

```{r}
# Type your code below this line

```

`@solution`

```{r}
head(state_foreign_born,10)
```

`@sct`

```{r}
# Update this to something more informative.
success_msg("Great job!  You are heading in the right direction!")
```

---

## Which states have the highest percentage of foreign born?

```yaml
type: NormalExercise
lang: r
xp: 100
skills: 1
key: f0c6a9fb86
```

It may be that you want to learn a bit about which states have the highest percentage of people who are foreign born.   You can do this with the `dplyr` package's `arrange` function. See if you can edit the chunk below to do this. Feel free to reference the **Tidyverse for Beginners** cheat sheet.


`@instructions`
- Use `dplyr`'s `arrange` function to sort the `percent_foreign_born` variable in `state_foreign_born` from largest to smallest.
- Hit *Run Code* to test your code, and *Submit Answer* when you think you have it right.

`@hint`
- Don't forget to put the `percent_foreign_born` variable inside of the arrange function.
- Did you remember how to sort it from LARGEST to SMALLEST?  Reference your cheat sheet for help.


`@pre_exercise_code`

```{r}
# Load datasets and packages here.
library(dplyr,warn.conflicts=FALSE)
state_foreign_born<-read.csv("http://s3.amazonaws.com/assets.datacamp.com/production/repositories/3374/datasets/9e5e6297329fe3304830bf454bc9445bd16f9621/state_foreign_born.csv")
```

`@sample_code`

```{r}
state_foreign_born %>%
  ____write something here_____

```

`@solution`

```{r}
state_foreign_born %>%
  arrange(desc(percent_foreign_born))
```

`@sct`

```{r}
# Update this to something more informative.
success_msg("Great job!")
```

