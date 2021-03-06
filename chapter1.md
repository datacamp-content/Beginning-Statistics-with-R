---
  title: "Template Chapter 1"
  description: "This is a template chapter."
---

## Recognize a statistical question

```yaml
type: PureMultipleChoiceExercise 
xp: 50 
key: 5e51bfcb9d   
```

A statistical question is a question that can be answered by collecting data. Almost all data has some variability. Variability means that repeated measurements of similar items give different numbers (the numbers vary).

A deterministic question is a question with one exact answer. The number never changes.

Example of a statistical question:
How much time do students at  my school spend on math homework each week?

Example of a deterministic question:
How many pennies are in a dime?

Abby went to the store a bought a bag of jelly beans, and has not opened it yet. Which of the following is not a statistical question about jelly beans?


`@hint`
If there is only one possible correct answer to the question, it is deterministic.
If there are multiple possible correct answers, or the correct answer could change, then it is a statistical question.

`@possible_answers`
- What is a typical number of jelly beans in a bag?
 - [How much does Abby's bag weigh?]
 - Which color is the most frequent?
 - If Abby closed her eyes, shook up the bag, reached in and grabbed a jelly bean, how likely will it be red?
 - What is the typical weight of a jelly bean?
 - How are the jelly beans distributed according to color?

`@feedbacks`
 - Since different bags can have different numbers of jelly beans, this is a statistical question.
 - Good job! Since there is only one possible answer, this is a deterministic question.
 - Since there are multiple colors of jelly beans, this is a statistical question.
 - Since Abby could grab any color of jelly bean, this is a statistical question.
 - Some jelly beans will be bigger than others, this is a statistical question.
 - Since there are multiple colors of jelly beans, this is a statistical question.

---

## Maximum and minimum values

```yaml
type: BulletExercise 
xp: 100 
key: 8fb45ad353   
```

* max(data): the maximum value will be returned
* which.max(data): the entry with the maximum value will be returned
* min(data): the minimum value will be returned
* which.min(data): the entry with the minimum value will be returned

The dataset Electorial_Votes is loaded for you.
* Find the largest number of electorial votes
* Find which state/district that has the most electorial votes
* Find the smallest number of electorial votes
* Find which state/district that has the fewest electorial votes

`@pre_exercise_code`

```{r}
Electorial_Votes <- matrix(c(9,3,11,6,55,9,7,3,3,29,16,4,4,20,11,6,6,8,8,4,10,11,16,10,6,10,3,5,6,4,14,5,29,15,3,18,7,7,20,4,9,3,11,38,6,3,13,12,5,10,3),ncol = 1)
rownames(Electorial_Votes) <- c(
  "Alabama","Alaska","Arizona","Arkansas","California","Colorado","Connecticut","Delaware","District of Columbia","Florida","Georgia","Hawaii","Idaho","Illinois","Indiana","Iowa","Kansas","Kentucky","Louisiana","Maine","Maryland","Massachusetts","Michigan","Minnesota","Mississippi","Missouri","Montana","Nebraska","Nevada","New Hampshire","New Jersey","New Mexico","New York","North Carolina","North Dakota","Ohio","Oklahoma","Oregon","Pennsylvania","Rhode Island","South Carolina","South Dakota","Tennessee","Texas","Utah","Vermont","Virginia","Washington","West Virginia","Wisconsin","Wyoming"
)
colnames(Electorial_Votes) <- "Electorial_Votes"
print(Electorial_Votes)
Electorial_Votes <- c(9,3,11,6,55,9,7,3,3,29,16,4,4,20,11,6,6,8,8,4,10,11,16,10,6,10,3,5,6,4,14,5,29,15,3,18,7,7,20,4,9,3,11,38,6,3,13,12,5,10,3)
names(Electorial_Votes) <- c(
  "Alabama","Alaska","Arizona","Arkansas","California","Colorado","Connecticut","Delaware","District of Columbia","Florida","Georgia","Hawaii","Idaho","Illinois","Indiana","Iowa","Kansas","Kentucky","Louisiana","Maine","Maryland","Massachusetts","Michigan","Minnesota","Mississippi","Missouri","Montana","Nebraska","Nevada","New Hampshire","New Jersey","New Mexico","New York","North Carolina","North Dakota","Ohio","Oklahoma","Oregon","Pennsylvania","Rhode Island","South Carolina","South Dakota","Tennessee","Texas","Utah","Vermont","Virginia","Washington","West Virginia","Wisconsin","Wyoming"
)
```

***

## Find the largest number of electorial votes

```yaml
type: NormalExercise
xp: 25
key: dd03b69684
```

`@instructions`
Find the largest number of electorial votes

`@hint`
Type max(Electorial_Votes), then press the submit button

`@solution`
```{r}
max(Electorial_Votes)
```

***

## Find which state/district has the largest number of electorial votes

```yaml
type: NormalExercise
xp: 25
key: 7bcc0658f6
```

`@instructions`
Find which state/district has the largest number of electorial votes

`@hint`
Type which.max(Electorial_Votes), then press the submit button

`@solution`
```{r}
which.max(Electorial_Votes)
```

***

## Find the least number of electorial votes of state/districts that have a vote

```yaml
type: NormalExercise
xp: 25
key: 0038ca9110
```

`@instructions`
Find the least number of electorial votes

`@hint`
Type min(Electorial_Votes), then press the submit button

`@solution`
```{r}
min(Electorial_Votes)
```

***

## Find which state/district has the least number of electorial votes
## Note: There are multiple states with the minimum number of electorial colleges, the which.min() function will grab the first one

```yaml
type: NormalExercise
xp: 25
key: e83e873522
```

`@instructions`
Find which state/district has the least number of electorial votes

`@hint`
Type which.min(Electorial_Votes), then press the submit button

`@solution`
```{r}
which.max(Electorial_Votes)
```

---

## Using dotplots to see your data

```yaml
type: BulletExercise
lang: r
xp: 100
key: 47fc948fb1
```

Dotplots are visual representations of data enabling quick insights into the numbers.

The `dotplot()` function creates dotplots.

The mean and median are ways to describe the center of data using only one number.
The mean of a dataset is the sum of all the numbers divided by the number of observations.
The median is the middle value, or the average of the middle two values.

The median is better than the mean when the data is skewed.

`mean()` computes the mean.
`median()` computes the median.

`@pre_exercise_code`

```{r}
Electorial_Votes <- c(
  9,3,11,6,55,9,7,3,3,29,16,4,4,20,11,6,6,8,8,4,10,11,16,10,6,10,3,5,6,4,14,5,29,15,3,18,7,7,20,4,9,3,11,38,6,3,13,12,5,10,3
)
names(Electorial_Votes) <- c(
  "Alabama","Alaska","Arizona","Arkansas","California","Colorado","Connecticut","Delaware","District of Columbia","Florida","Georgia","Hawaii","Idaho","Illinois","Indiana","Iowa","Kansas","Kentucky","Louisiana","Maine","Maryland","Massachusetts","Michigan","Minnesota","Mississippi","Missouri","Montana","Nebraska","Nevada","New Hampshire","New Jersey","New Mexico","New York","North Carolina","North Dakota","Ohio","Oklahoma","Oregon","Pennsylvania","Rhode Island","South Carolina","South Dakota","Tennessee","Texas","Utah","Vermont","Virginia","Washington","West Virginia","Wisconsin","Wyoming"
)
dotplot <- function(x){
  stripchart(x,xaxt = "n",method = "stack",pch = 19,offset = 1)
  axis(1,at = x,pos = 0.9)
}
```

***

## Create a dotplot/stripchart for the electorial votes dataset

```yaml
type: NormalExercise
xp: 34
key: 39553e98c0
```

`@instructions`

Use the `dotplot()` function to create a dotplot of the electorial college votes

`@hint`

Type `dotplot(Electorial_Votes)`, then press the submit button.

`@solution`

```{r}
dotplot(Electorial_Votes)
```

***

## Compute the mean electorial college

```yaml
type: NormalExercise
xp: 33
key: 44ff981299
```

`@instructions`

Use the `mean()` function to find the average number of electorial college votes

`@hint`

Type `mean(Electorial_Votes)`, then press the submit button.

`@solution`

```{r}
mean(Electorial_Votes)
```

***

## Compute the median electorial college

```yaml
type: NormalExercise
xp: 33
key: 2e83ffdda5
```

`@instructions`

Use the `median()` function to find the typical number of electorial college votes

`@hint`

Type `median(Electorial_Votes)`, then press the submit button.

`@solution`

```{r}
median(Electorial_Votes)
```

---

## Use a dotplot to determine skew

```yaml
type: MultipleChoiceExercise 
lang: r
xp: 25
key: 6d4cc518f0
```

Data is called skewwed if to one side there is a lot more variability than on the other side.
Symmetric data has approximately equal variance on the left and on the right.

* Dotplots of skewed right data have a tail going to the right.
* Dotplots of skewed left data have a tail going to the left.
* Symmetric data has approximately the same shape on the left and on the right.

Look at the dotplot and decide if the electorial vote numbers are skew left, skew right or symmetric.

`@pre_exercise_code`

```{r}
Electorial_Votes <- c(
  9,3,11,6,55,9,7,3,3,29,16,4,4,20,11,6,6,8,8,4,10,11,16,10,6,10,3,5,6,4,14,5,29,15,3,18,7,7,20,4,9,3,11,38,6,3,13,12,5,10,3
)
names(Electorial_Votes) <- c(
  "Alabama","Alaska","Arizona","Arkansas","California","Colorado","Connecticut","Delaware","District of Columbia","Florida","Georgia","Hawaii","Idaho","Illinois","Indiana","Iowa","Kansas","Kentucky","Louisiana","Maine","Maryland","Massachusetts","Michigan","Minnesota","Mississippi","Missouri","Montana","Nebraska","Nevada","New Hampshire","New Jersey","New Mexico","New York","North Carolina","North Dakota","Ohio","Oklahoma","Oregon","Pennsylvania","Rhode Island","South Carolina","South Dakota","Tennessee","Texas","Utah","Vermont","Virginia","Washington","West Virginia","Wisconsin","Wyoming"
)
par(mar = c(0,0,0,0),oma = c(0,0,0,0))
dotplot <- function(x){
  stripchart(x,xaxt = "n",method = "stack",pch = 19,offset = 1)
  axis(1,at = x,pos = 0.9)
}
dotplot(Electorial_Votes)
```

`@possible_answers`

- skew left
 - [skew right]
 - symmetric
 - neither skewed nor symmetric
 
`@feedbacks`

 - Look at the dotplot again, the tail is going to the right.
 - Good!
 - Look at the dotplot again, the left side and the right sides of the dotplot look different.
 - Look at the dotplot again, most of the data is on the left but there are a few points trailing to the right.
 
---

## Use a dotplot to select the measure of central tendency

```yaml
type: MultipleChoiceExercise
lang: r
xp: 25
key: 0fd6e00cc0
```

* The median is a better description of the central tendency when the data is skewed.
* The mean is a better description of the central tendency when there are few distinct observations.
* In general, the mean is preferred.

Look at the dotplot and decide if the mean or median is a better description of the data' central tendency.

`@pre_exercise_code`

```{r}
Electorial_Votes <- c(
  9,3,11,6,55,9,7,3,3,29,16,4,4,20,11,6,6,8,8,4,10,11,16,10,6,10,3,5,6,4,14,5,29,15,3,18,7,7,20,4,9,3,11,38,6,3,13,12,5,10,3
)
names(Electorial_Votes) <- c(
  "Alabama","Alaska","Arizona","Arkansas","California","Colorado","Connecticut","Delaware","District of Columbia","Florida","Georgia","Hawaii","Idaho","Illinois","Indiana","Iowa","Kansas","Kentucky","Louisiana","Maine","Maryland","Massachusetts","Michigan","Minnesota","Mississippi","Missouri","Montana","Nebraska","Nevada","New Hampshire","New Jersey","New Mexico","New York","North Carolina","North Dakota","Ohio","Oklahoma","Oregon","Pennsylvania","Rhode Island","South Carolina","South Dakota","Tennessee","Texas","Utah","Vermont","Virginia","Washington","West Virginia","Wisconsin","Wyoming"
)
par(mar = c(0,0,0,0),oma = c(0,0,0,0))
dotplot <- function(x){
  stripchart(x,xaxt = "n",method = "stack",pch = 19,offset = 1)
  axis(1,at = x,pos = 0.9)
}
dotplot(Electorial_Votes)
```

`@possible_answers`

- mean
- [median]
 
`@feedbacks`

- the data is skewed right
- Good!

---
## See the shape, center and variability of the data

```yaml
type: BulletExercise
key: ea46221337
lang: r
xp: 100
```

Graphs and plots can help you quickly see the shape, central tendency and variability of data.

* Histograms use bars to show which ranges of values are more common (`hist()`).
* Boxplots give a visual summary of the data; showing the maximum, minimum, median, and interquartiles (`boxplot()`).

Interquartiles are the middle values between the median and the most extreme values.
* Q1 is the median value of the data between the minimum and the median.
* Q3 is the median value of the data between the median and the maximum value.

Two of the easiest ways to compute variability by hand are interquartile range (`IQR()`), and median absolute deviation (`mad()`).
* IQR = Q3 - Q1
* mad: the median of the difference between values and the median

`@instructions`

For each planet in our solar system, the acceleration due to gravity is in the `gravity` dataset.
* Create a histogram of gravity acceleration
* Create a boxplot of gravity acceleration
* Compute the `IQR()` of gravity acceleration
* Compute the `mad()` of gravity acceleration

`@pre_exercise_code`
```{r}
# data from https://nssdc.gsfc.nasa.gov/planetary/factsheet/ 2018-07-21
gravity <- matrix(c(3.7,8.9,9.8,3.7,23.1,9,8.7,11),ncol = 1)
rownames(gravity) <- c("MERCURY","VENUS","EARTH","MARS","JUPITER","SATURN","URANUS","NEPTUNE")
colnames(gravity) <- "gravity (m/s^2)"
print(gravity)

gravity <- c(3.7,8.9,9.8,3.7,23.1,9,8.7,11)
names(gravity) <- c("MERCURY","VENUS","EARTH","MARS","JUPITER","SATURN","URANUS","NEPTUNE")
```

***

### Create a histogram

```yaml
type: NormalExercise
xp: 100
key: da77794e1d
```

`@instructions`
Create a histogram of the gravity data
`@hint`
Use the `hist()` function.
`@solution`
```{r}
hist(gravity)
```

`@sct`
```{r}
hist(gravity)
```

***

### Create a boxplot

```yaml
type: NormalExercise
xp: 100
key: 5c7addef87
```

`@instructions`
Create a boxplot of the gravity data
`@hint`
Use the `boxplot()` function.
`@solution`
```{r}
boxplot(gravity)
```

`@sct`
```{r}
boxplot(gravity)
```

***

### Compute the interquartile range

```yaml
type: NormalExercise
xp: 100
key: e0185daf00
```

`@instructions`
Compute the interquartile range of the gravity data
`@hint`
Use the `IQR()` function.
`@solution`
```{r}
IQR(gravity)
```

`@sct`
```{r}
IQR(gravity)
```

***

### Compute the median absolute deviation

```yaml
type: NormalExercise
xp: 100
key: 605632c37f
```

`@instructions`
Compute the median absolute deviation of the gravity data
`@hint`
Use the `mad()` function.
`@solution`
```{r}
mad(gravity)
```

`@sct`
```{r}
mad(gravity)
```


---
## What if it is not a bunch of numbers?

```yaml
type: NormalExercise
key: 553da7c84a
lang: r
xp: 100
skills: 1
```


`@instructions`

`@hint`

`@pre_exercise_code`
```{r}
# https://www.teamusa.org/road-to-rio-2016/team-usa/athletes 2018-07-21
Rio<-c(

"DC","DC","DC","DC","AL","AK","AK","AZ","AZ","AZ","AZ","AZ","AZ","AZ","AZ","AZ","AR","AR","AR","AR","AR","AR",
"CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA","CA",
"CO","CO","CO","CO","CO","CO","CO","CO","CO","CO","CO","CO","CO","CO","CO","CO","CO","CO","CO",
"Conn","Conn","Conn","Conn","Conn","Conn","Conn","Conn","Del","Del",
"Fla","Fla","Fla","Fla","Fla","Fla","Fla","Fla","Fla","Fla","Fla","Fla","Fla","Fla","Fla","Fla","Fla","Fla","Fla","Fla","Fla","Fla","Fla","Fla","Fla","Fla","Fla","Fla","Fla","Fla","Fla","Fla","Fla","Fla","Fla","Fla","Fla","Fla","Fla",
"Ga","Ga","Ga","Ga","Ga","Ga","Ga","Ga","Ga","Ga","Ga","Ga","Ga","Ga","Hawaii","Hawaii","Hawaii","Hawaii","Hawaii","Idaho","Idaho",
"Ill","Ill","Ill","Ill","Ill","Ill","Ill","Ill","Ill","Ill","Ill","Ill","Ill","Ill","Ill","Ill","Ill",
"Ind","Ind","Ind","Ind","Ind","Ind","Ind","Ind","Ind","Ind","Ind","Ind","Ind","Iowa","Iowa","Iowa","Kan","Kan","Kan","Ky","Ky","La",
"La","La","Maine","Mass","Mass","Mass","Mass","Mass","Mass","Mass","Mass","Mass","Mass","Mass","Mass","Mass",
"Md","Md","Md","Md","Md","Md","Md","Md","Md","Md","Md","Mich","Mich","Mich","Mich","Mich","Mich","Mich","Mich","Mich","Mich",
"Minn","Minn","Minn","Minn","Minn","Minn","Minn","Minn","Minn","Minn","Minn","Miss","Miss","Miss","Miss",
"Mo","Mo","Mo","Mo","Mo","Mo","Mo","Mo","Mo","Mo","Mo","NC","NC","NC","NC","NH","NH","NH","NH",
"NJ","NJ","NJ","NJ","NJ","NJ","NJ","NJ","NJ","NJ","NJ","NJ","NJ","NJ","NJ","NJ","NJ","NJ","NJ","NJ","NJ","NJ","NJ","NJ","NJ","NJ","NJ","NJ","NJ","NJ",
"NM","NM","NY","NY","NY","NY","NY","NY","NY","NY","NY","NY","NY","NY","NY","NY","NY","NY","NY","NY","NY","NY","NY","NY","NY","NY","NY","NY","NY","NY","NY","NY","NY",
"Neb","Neb","Neb","Neb","Nev","Nev","Nev","Nev","Ohio","Ohio","Ohio","Ohio","Ohio","Ohio","Ohio","Ohio","Ohio","Ohio","Ohio","Ohio","Ohio","Okla",
"Ore","Ore","Ore","Ore","Ore","Ore","Ore","Ore","Ore","Ore","Ore","Ore","Ore","Ore",
"Pa","Pa","Pa","Pa","Pa","Pa","Pa","Pa","Pa","Pa","Pa","Pa","Pa","Pa","Pa","Pa","Pa","Pa","Pa","Pa","Pa","Pa","Pa","Pa","Pa","Pa","Pa","Pa","Pa","Pa","Pa",
"RI","RI","RI","RI","SC","SC","SD","Tenn","Tenn",
"Texas","Texas","Texas","Texas","Texas","Texas","Texas","Texas","Texas","Texas","Texas","Texas","Texas","Texas","Texas","Texas","Texas","Texas","Texas","Texas","Texas","Texas","Texas","Texas","Texas","Texas","Texas","Texas","Texas","Texas","Texas","Texas","Texas",
"Utah","Utah","Utah","Utah","Va","Va","Va","Va","Va","Va","Va","Va","Va","Va","Va","Va","Va","Va","Vt",
"Wash","Wash","Wash","Wash","Wash","Wash","Wash","Wash","Wash","Wash","Wash","Wash","Wash","Wash","Wash","Wash","Wis","Wis","Wis","Wis","Wis"

)
```

`@sample_code`
```{r}

```

`@solution`
```{r}

```

`@sct`
```{r}

```
