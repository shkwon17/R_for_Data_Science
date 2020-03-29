# R_for_Data_Science
library(tidyverse)
ggplot(data = mpg) + 
  geom_point(mapping = aes(x = displ, y = hwy))
# Exercises
#Ex 1
ggplot(data = mpg) 
ggplot(data = mpg) + geom_point(mapping = aes(x = hwy, y = cyl))  
ggplot(data = mpg) + geom_point(mapping = aes(x = class, y = drv))
# Alpha
ggplot(data = mpg) + geom_point(mapping = aes(x = displ, y = hwy, alpha = class))
# Shape
ggplot(data = mpg) + geom_point(mapping = aes(x = displ, y = hwy, shape = class))  
ggplot(data = mpg)  
# Color
ggplot(data = mpg) + geom_point(mapping = aes(x = displ, y = hwy), color = "blue")
ggplot(data = mpg) + geom_point(mapping = aes(x = displ, y = hwy), color = "pink")
#Exercises
#EX1: Wrong parenthesis, which should have capped and compeleted aes ()
ggplot(data = mpg) + geom_point(mapping = aes(x = displ, y = hwy, color = "blue"))
ggplot(data = mpg) + geom_point(mapping = aes(x = displ, y = hwy), color = "blue")
?mpg
# Place + always at the end of a line 
ggplot(data = mpg) 
+ geom_point(mapping = aes(x = displ, y = hwy))
ggplot(data = mpg) 
 + geom_point(mapping = aes(x = displ, y = hwy))
ggplot(data = mpg) + geom_point(mapping = aes(x = displ, y = hwy))
ggplot(data = mpg) + 
geom_point(mapping = aes(x = displ, y = hwy))
#?function_name
?function_ggplot
?help

# Facet
ggplot(data = mpg) + geom_point(mapping = aes(x = displ, y = hwy)) + 
  facet_wrap(~ class, nrow = 2)
  
ggplot(data = mpg) + geom_point(mapping = aes(x = drv, y = cyl))

ggplot(data = mpg) + geom_point(mapping = aes(x = displ, y = hwy)) + facet_grid(drv ~ .)

# geom_smooth
# left
ggplot(data = mpg) + 
  geom_point(mapping = aes(x = displ, y = hwy))

# right
ggplot(data = mpg) + 
  geom_smooth(mapping = aes(x = displ, y = hwy))

ggplot(data = mpg) +
  geom_smooth(mapping = aes(x = displ, y = hwy))
              
ggplot(data = mpg) +
  geom_smooth(mapping = aes(x = displ, y = hwy, group = drv))
    
ggplot(data = mpg) +  geom_smooth(mapping = aes(x = displ, y = hwy, color = drv), show.legend = FALSE)
  
ggplot(data = mpg) +  geom_smooth(mapping = aes(x = displ, y = hwy, color = drv), show.legend = TRUE)

ggplot(data = mpg) + 
  geom_point(mapping = aes(x = displ, y = hwy)) +
  geom_smooth(mapping = aes(x = displ, y = hwy))

ggplot(data = mpg) + 
  geom_point(mapping = aes(x = displ, y = hwy), color = "blue") +
  geom_smooth(mapping = aes(x = displ, y = hwy))
  
  ggplot(data = mpg) + 
  geom_point(mapping = aes(x = displ, y = hwy), color = "blue") +
  geom_smooth(mapping = aes(x = displ, y = hwy, color = class), show.legend = TRUE)
  
ggplot(data = mpg) + geom_point(mapping = aes(x = displ, y = hwy), color = "blue") + geom_smooth(mapping = aes(x = displ, y = hwy, color = drv), show.legend = TRUE)

ggplot(data = mpg, mapping = aes(x = displ, y = hwy)) + geom_point(mapping = aes(color = "blue") 

ggplot(data = mpg, mapping = aes(x = displ, y = hwy)) + 
  geom_point(mapping = aes(color = class)) 
  
ggplot(data = mpg) + 
  geom_point(mapping = aes(x = displ, y = hwy, color = class)) 

ggplot(data = mpg, mapping = aes(x = displ, y = hwy)) + 
  geom_point(mapping = aes(color = class)) + 
  geom_smooth(data = filter(mpg, class == "subcompact"), se = FALSE)  
  
  ggplot(data = mpg, mapping = aes(x = displ, y = hwy)) + 
  geom_point(mapping = aes(color = class)) + 
  geom_smooth(data = filter(mpg, class == "subcompact"), se = TRUE) 
  
  ggplot(data = mpg, mapping = aes(x = displ, y = hwy)) + 
  geom_point(mapping = aes(color = class)) + 
  geom_smooth(data = filter(mpg, class == "subcompact")) 
  
  #Statistical Transformation
  ggplot(data = diamonds) + 
  geom_bar(mapping = aes(x = cut))
  
  ggplot(data = diamonds) + 
  geom_bar(mapping = aes(x = cut, y = stat(prop), group = 1))

ggplot(data = diamonds) + 
  stat_summary(
    mapping = aes(x = cut, y = depth),
    fun.ymin = min,
    fun.ymax = max,
    fun.y = median
  )  
  
  ggplot(data = diamonds) + 
  geom_bar(mapping = aes(x = cut, color = cut))
  
ggplot(data = diamonds) + 
  geom_bar(mapping = aes(x = cut, fill = cut))
  
# Workflow - Basics
x <- 3 * 4
this_is_a_really_long_name <- 2.5

#Data transformation
install.packages("nycflights13")
library(nycflights13)  

?flights  

view (flights)  
