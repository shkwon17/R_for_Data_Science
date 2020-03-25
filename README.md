# R_for_Data_Science
library(tidyverse)
ggplot(data = mpg) + 
  geom_point(mapping = aes(x = displ, y = hwy))
# Exercises
#Ex 1
ggplot(data = mpg) 
ggplot(data = mpg) + geom_point(mapping = aes(x = hwy, y = cyl))  
ggplot(data = mpg) + geom_point(mapping = aes(x = class, y = drv))
  
  