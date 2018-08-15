---
  title: "Histogram and Boxplot Construction"
  description: "Using ggplot2 to learn some basics of R."
---

## Investigating the dataset

```yaml
type: NormalExercise 
lang: r
xp: 100 
skills: 1
key: b99a54db27   
```

The dataset that you are working with in these first few exercises contains the percentage of individuals in each state who were born in a foreign country.  We always want to investigate the dataset first to determine what variables are available.  One function that gives you a quick snapshot of this is the `head()` function.   To use this, you simply pass the name of your dataset into the `head()` function and R will show you the first few rows of the dataset coupled with the variable names.  

The `head()` function takes two arguments.  The first argument is the name of the dataset, and the second is how many rows you wish to see.  By default, you will be shown 6 rows, but you can specify how many rows by making use of the 2nd argument:

`head(NAME OF DATA, # OF ROWS)`

`@instructions`
- Use the `head()` function to view the first 10 rows of the dataset. 
- Hit *Run Code* to test your code, and *Submit Answer* when you think you have it right. 

`@hint`
- Remember the `head()` function takes two arguments.  The first is the name of the dataset (which is `state_foreign_born` in this case) and the second is the number of rows you wish to see (if different from 6).


`@pre_exercise_code`

```{r}
# Load datasets and packages here
library(tidyverse)
state_foreign_born<-read_csv("datasets/state_foreign_born.csv")

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
success_msg("Great job!  You are `head`ing in the right direction!")
```

# ---
# 
# ## Which states have the highest percentage of foreign born?
# 
# ```yaml
# type: NormalExercise
# lang: r
# xp: 100
# skills: 1
# key: f0c6a9fb86
# ```
# 
# It may be that you want to learn a bit about which states have the highest percentage of people who are foreign born.   You can do this with the `dplyr` package's `arrange` function. See if you can edit the chunk below to do this. Feel free to reference the **Tidyverse for Beginners** cheat sheet. 
# 
# 
# `@instructions`
# - Use `dplyr`'s `arrange` function to sort the data in `state_foreign_born` from largest to smallest. 
# - Hit *Run Code* to test your code, and *Submit Answer* when you think you have it right. 
# 
# `@hint`
# - Don't forget to put the `percent_foreign_born` variable inside of the arrange function. 
# - Did you remember how to sort it from LARGEST to SMALLEST?  Reference your cheat sheet for help. 
# 
# 
# `@pre_exercise_code`
# 
# ```{r}
# # Load datasets and packages here.
# 
# ```
# 
# `@sample_code`
# 
# ```{r}
# state_foreign_born %>% 
#   ____write something here_____
#   
# ```
# 
# `@solution`
# 
# ```{r}
# state_foreign_born %>% 
#   arrange(desc(percent_foreign_born))
# ```
# 
# `@sct`
# 
# ```{r}
# # Update this to something more informative.
# success_msg("Great job!")
# ```
# 
