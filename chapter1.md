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

![](https://www.w3schools.com/w3css/img_lights.jpg)


`@instructions`
- Instruction 1
- Instruction 2
- Instruction 3
- Instruction 4

`@hint`
- Here is the hint for this setup problem. 
- It should get students 50% of the way to the correct answer.
- So don't provide the answer, but don't just reiterate the instructions.
- Typically one hint per instruction is a sensible amount.

`@pre_exercise_code`

```{r}
# Load datasets and packages here.


```

`@sample_code`

```{r}
# Don't forget to load the ggplot2 library.



```

`@solution`

```{r}
# Don't forget to load the ggplot2 library.
library(ggplot2)

ggplot(mpg, aes(x=class,y=hwy)) + 
  geom_boxplot()
```

`@sct`

```{r}
# Update this to something more informative.
success_msg("Great job!  You nailed it.")
```
