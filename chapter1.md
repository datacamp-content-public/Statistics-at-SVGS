---
  title: "Unit 1:  Data Visualization"
  description: "This is a template chapter."
---

## Exploring ggplot2

```yaml
type: NormalExercise 
lang: r
xp: 100 
skills: 1
key: b99a54db27   
```


Use the `tidyverse` cheatsheet to replace the scatterplot below with one that draws boxplots.   Try your best guess. 

![](https://svgsstats.github.io/forDataCamp/mpg_scatter_class_hwy.png)
```{r}
library(ggplot2)
ggplot(mpg) +
  geom_point(aes(x=class,y=hwy))
```

`@instructions`
- Load the `ggplot2` package using a `library()` call. 
- Use the `ggplot()` function to construct a graph similar to the one pictured, but with boxplots instead.
- Hit *Run Code* to test your code, and *Submit Answer* when you think you have it right. 

`@hint`
- Reference the `tidyverse` cheatsheet to find what the boxplot geom is called. 
- The x-axis should be `class` and the y-axis should have the `hwy` variable.
- Don't forget to put the `x=class` inside of the `aes()` function.


`@pre_exercise_code`

```{r}
# Load datasets and packages here.

```

`@sample_code`

```{r}
# Load the ggplot2 package first

# Put your ggplot() function below this line.
```

`@solution`

```{r}
# Load the ggplot2 package first
library(ggplot2)
# Put your ggplot() function below this line. 
ggplot(mpg) + 
  geom_boxplot(aes(x=class,y=hwy))
```

`@sct`

```{r}
# Update this to something more informative.
success_msg("Great job!  The tidyverse cheatsheet is a great reference tool for finding the right function for a particular graph.")
```
