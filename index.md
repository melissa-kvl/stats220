# My Meme
## *Made in RStudio, about RStudio - A beginner student's outlet for frustration*

![my_meme](https://user-images.githubusercontent.com/100824050/158041988-f2eecf52-2018-42be-b75f-464dbc15b977.png)

*I made this meme using the code below*
```
library(magick)
caption <- image_blank(width = 600,
                      height = 300,
                      color = "#cce6ff") %>%
           image_annotate(text = "When RStudio sends you an error message",
                         color = "#000000",
                         size = 30,
                         font = "Impact",
                         gravity = "center")

shocked_dog <- image_read("https://media.istockphoto.com/photos/guilty-or-intrigued-siberian-husky-dog-looking-up-isolated-on-white-picture-id1311639548?b=1&k=20&m=1311639548&s=170667a&w=0&h=M6sOY-04cQ7wilahV66Fr6CHhOTJaoXyJqLUoDxohQ0=") %>%
  image_scale(250)

dismayed_dog <- image_read("https://media.istockphoto.com/photos/what-a-shame-picture-id172161240?b=1&k=20&m=172161240&s=170667a&w=0&h=HruhX36pjpogzp20Pekm5bLnUwDX9A5VONTDP13DGHE=") %>%
  image_scale(350)

first_row <- caption 

second_row <- c(shocked_dog, dismayed_dog) %>%
  image_append()

meme <- c(first_row, second_row) %>%
  image_append(stack = TRUE)
```

**What was the motivation for creating my meme?**
1. I was inspired to make a meme about RStudio given that I use the platform in two courses
2. I wanted to make a meme that anyone who has or is starting out in R can relate to 
3. I wanted to have some fun with the meme because it is not often that we get an assignment this awesome!

**How is my meme original?**
* I based the meme format off the popular one (pictured below) however I changed the puppet to dogs because I love big dogs :)
* I also made the meme about a subject which I have never seen a meme about before

![Meme inspiration](https://imgflip.com/s/meme/Monkey-Puppet.jpg)
