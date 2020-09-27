Team Troubleshooting Deliverable 2
================

install.packages(c(‘tidyverse’,‘devtools’,‘dslabs’,‘gapminder’))
devtools::install\_github(“JoeyBernhardt/singer”) library(singer)
install.packages(‘tidyverse’) install.packages(‘singer’) library(dplyr)
packageVersion(‘dplyr’)

## Attributions

Thanks to Icíar Fernández-Boyano for writing most of this document, and
Diana Lin for her edits.

## Instructions

There are **24 errors** in this Rmd. Will you find them all?

  - *15 errors are marked* (at least the general area in which they are
    located) by \#\# ERROR HERE \#\# in the code chunk.
  - *9 errors are hiding.*

Hint: You should be able to knit the Rmd if all code is working
correctly…but this will only catch the errors in code, and not the
errors in logic or instruction-following\!

**Notes:**

  - Errors may be in the form of **broken code** (e.g. using " "
    inappropriately, which returns an error when running the code), but
    can also be **running code that does not follow the instructions**
    (e.g. the goal of the code was to filter the first 3 rows, but
    instead, the first 3 columns were selected). Read the Rmd commentary
    carefully to find these.

  - A code chunk with multiple errors, whether broken code or wrongly
    followed instructions, **counts as a single error for the purpose of
    grading**. An example:

Exercise A: In the following chunk, I would like to select all columns
of the mtcars dataset from `disp` to `wt` (inclusive), and then, filter
for those with horsepower (`hp`) of at least 100 or greater.

``` r
### ERROR HERE ###
mtcars %>%
  select(disp:wt) %>%
  filter(hp >= 100)
```

    ##                      disp  hp drat    wt
    ## Mazda RX4           160.0 110 3.90 2.620
    ## Mazda RX4 Wag       160.0 110 3.90 2.875
    ## Hornet 4 Drive      258.0 110 3.08 3.215
    ## Hornet Sportabout   360.0 175 3.15 3.440
    ## Valiant             225.0 105 2.76 3.460
    ## Duster 360          360.0 245 3.21 3.570
    ## Merc 280            167.6 123 3.92 3.440
    ## Merc 280C           167.6 123 3.92 3.440
    ## Merc 450SE          275.8 180 3.07 4.070
    ## Merc 450SL          275.8 180 3.07 3.730
    ## Merc 450SLC         275.8 180 3.07 3.780
    ## Cadillac Fleetwood  472.0 205 2.93 5.250
    ## Lincoln Continental 460.0 215 3.00 5.424
    ## Chrysler Imperial   440.0 230 3.23 5.345
    ## Dodge Challenger    318.0 150 2.76 3.520
    ## AMC Javelin         304.0 150 3.15 3.435
    ## Camaro Z28          350.0 245 3.73 3.840
    ## Pontiac Firebird    400.0 175 3.08 3.845
    ## Lotus Europa         95.1 113 3.77 1.513
    ## Ford Pantera L      351.0 264 4.22 3.170
    ## Ferrari Dino        145.0 175 3.62 2.770
    ## Maserati Bora       301.0 335 3.54 3.570
    ## Volvo 142E          121.0 109 4.11 2.780

Notice that the instructions indicate selecting columns `disp` to `wt`,
and the code reads `select(disp:vs)`. There is the error.

In addition to selecting the wrong columns, this exercise encapsulates
the number 100 in between quotes - this is incorrect R syntax. In fact,
if you run the code you will see that the filtering is not working.

While Exercise A has 2 requires two corrections to fix, it counts as
having a *single error*, as you cannot obtain your desired output
without fixing both. Therefore, errors within the *same literal R
markdown code chunk* count as **one error**. For the purposes of
grading, each *corrected* literal R markdown code chunk is considered
**one error** and worth **one point** each, for a total of 25 points.

Solution:

``` r
mtcars %>%
  select(disp:wt) %>%
  filter(hp >= 100)
```

    ##                      disp  hp drat    wt
    ## Mazda RX4           160.0 110 3.90 2.620
    ## Mazda RX4 Wag       160.0 110 3.90 2.875
    ## Hornet 4 Drive      258.0 110 3.08 3.215
    ## Hornet Sportabout   360.0 175 3.15 3.440
    ## Valiant             225.0 105 2.76 3.460
    ## Duster 360          360.0 245 3.21 3.570
    ## Merc 280            167.6 123 3.92 3.440
    ## Merc 280C           167.6 123 3.92 3.440
    ## Merc 450SE          275.8 180 3.07 4.070
    ## Merc 450SL          275.8 180 3.07 3.730
    ## Merc 450SLC         275.8 180 3.07 3.780
    ## Cadillac Fleetwood  472.0 205 2.93 5.250
    ## Lincoln Continental 460.0 215 3.00 5.424
    ## Chrysler Imperial   440.0 230 3.23 5.345
    ## Dodge Challenger    318.0 150 2.76 3.520
    ## AMC Javelin         304.0 150 3.15 3.435
    ## Camaro Z28          350.0 245 3.73 3.840
    ## Pontiac Firebird    400.0 175 3.08 3.845
    ## Lotus Europa         95.1 113 3.77 1.513
    ## Ford Pantera L      351.0 264 4.22 3.170
    ## Ferrari Dino        145.0 175 3.62 2.770
    ## Maserati Bora       301.0 335 3.54 3.570
    ## Volvo 142E          121.0 109 4.11 2.780

## Troubleshooting time\!

There are 24 code chunks in this Rmd with errors. Will you be the one to
find them all? More than 1 error in a single chunk of code counts as a
**single** error.

``` r
### ERROR HERE ###
library(dslabs)
library(singer)
library(tidyverse)
library(stringr)
library(gapminder)
```

    ## 
    ## Attaching package: 'gapminder'

    ## The following object is masked from 'package:dslabs':
    ## 
    ##     gapminder

``` r
install.packages(tidyverse)
```

    ## Error in install.packages(tidyverse): object 'tidyverse' not found

``` r
install.packages(c('tidyverse', 'dslabs', 'gapminder', 'singer'))
```

    ## Warning: packages 'tidyverse', 'dslabs', 'gapminder', 'singer' are in use and
    ## will not be installed

``` r
install.packages(stringer)
```

    ## Error in install.packages(stringer): object 'stringer' not found

``` r
library(dslabs)
library(singer)
library(tidyverse)
library(gapminder)
library(stringr)
```

[MovieLens](https://dl.acm.org/doi/10.1145/2827872) are a series of
datasets widely used in education, that describe movie ratings from the
MovieLens [website](https://movielens.org/). There are several MovieLens
datasets, collected by the [GroupLens Research
Project](https://grouplens.org/datasets/movielens/) at the University of
Minnesota. Here, we load the MovieLens 100K dataset from Rafael Irizarry
and Amy Gill’s R package,
[DSLabs](https://cran.r-project.org/web/packages/dslabs/dslabs.pdf),
which contains datasets useful for data analysis practice, homework, and
projects in data science courses and workshops.

### Exercise 1

Let’s have a look at the dataset\! My goal is to:

  - Find out the “class” of the dataset.
  - If it isn’t a tibble already, coerce it into a tibble and store it
    in the variable “movieLens”.
  - Have a quick look at the rows and columns, using a *dplyr function*.

Before

``` r
### ERROR HERE ###
#class(dslabs::movielens)
#movieLens <- as_tibble(dslabs::movielens)
#dim(movieLens)
```

After

``` r
### ERROR HERE ###
class(movielens)
```

    ## [1] "data.frame"

``` r
movieLens <- as_tibble(movielens)
dim(movieLens)
```

    ## [1] 100004      7

### Exercise 2

Now that we’ve had a quick look at the dataset, it would be interesting
to explore the rows (observations) in some more detail. I’d like to know
how many movie entries…

  - Belong to the genre *“Drama”*?
  - Don’t belong to the genre *“Drama”*?
  - Were filmed *after* the year 2000?
  - Have a rating of *4.5 or greater*?
  - Were filmed in 1999 *or* 2000?
  - Correspond to the movie *“Little Women”*?
  - Have *more than* 4.5 stars, and were released *before* 1995?

<!-- end list -->

``` r
filter(movieLens, genres == "Drama")
```

    ## # A tibble: 7,757 x 7
    ##    movieId title                             year genres userId rating timestamp
    ##      <int> <chr>                            <int> <fct>   <int>  <dbl>     <int>
    ##  1      31 Dangerous Minds                   1995 Drama       1    2.5    1.26e9
    ##  2    1172 Cinema Paradiso (Nuovo cinema P~  1989 Drama       1    4      1.26e9
    ##  3    1293 Gandhi                            1982 Drama       1    2      1.26e9
    ##  4      62 Mr. Holland's Opus                1995 Drama       2    3      8.35e8
    ##  5     261 Little Women                      1994 Drama       2    4      8.35e8
    ##  6     300 Quiz Show                         1994 Drama       2    3      8.35e8
    ##  7     508 Philadelphia                      1993 Drama       2    4      8.35e8
    ##  8     537 Sirens                            1994 Drama       2    4      8.35e8
    ##  9    2702 Summer of Sam                     1999 Drama       3    3.5    1.30e9
    ## 10    3949 Requiem for a Dream               2000 Drama       3    5      1.30e9
    ## # ... with 7,747 more rows

``` r
filter(movieLens, !genres == "Drama")
```

    ## # A tibble: 92,247 x 7
    ##    movieId title                year genres              userId rating timestamp
    ##      <int> <chr>               <int> <fct>                <int>  <dbl>     <int>
    ##  1    1029 Dumbo                1941 Animation|Children~      1    3      1.26e9
    ##  2    1061 Sleepers             1996 Thriller                 1    3      1.26e9
    ##  3    1129 Escape from New Yo~  1981 Action|Adventure|S~      1    2      1.26e9
    ##  4    1263 Deer Hunter, The     1978 Drama|War                1    2      1.26e9
    ##  5    1287 Ben-Hur              1959 Action|Adventure|D~      1    2      1.26e9
    ##  6    1339 Dracula (Bram Stok~  1992 Fantasy|Horror|Rom~      1    3.5    1.26e9
    ##  7    1343 Cape Fear            1991 Thriller                 1    2      1.26e9
    ##  8    1371 Star Trek: The Mot~  1979 Adventure|Sci-Fi         1    2.5    1.26e9
    ##  9    1405 Beavis and Butt-He~  1996 Adventure|Animatio~      1    1      1.26e9
    ## 10    1953 French Connection,~  1971 Action|Crime|Thril~      1    4      1.26e9
    ## # ... with 92,237 more rows

``` r
filter(movieLens, year > 2000)
```

    ## # A tibble: 25,481 x 7
    ##    movieId title                  year genres            userId rating timestamp
    ##      <int> <chr>                 <int> <fct>              <int>  <dbl>     <int>
    ##  1    5349 Spider-Man             2002 Action|Adventure~      3    3      1.30e9
    ##  2    5669 Bowling for Columbine  2002 Documentary            3    3.5    1.30e9
    ##  3    6377 Finding Nemo           2003 Adventure|Animat~      3    3      1.30e9
    ##  4    7153 Lord of the Rings: T~  2003 Action|Adventure~      3    2.5    1.30e9
    ##  5    7361 Eternal Sunshine of ~  2004 Drama|Romance|Sc~      3    3      1.30e9
    ##  6    8622 Fahrenheit 9/11        2004 Documentary            3    3.5    1.30e9
    ##  7    8636 Spider-Man 2           2004 Action|Adventure~      3    3      1.30e9
    ##  8   44191 V for Vendetta         2006 Action|Sci-Fi|Th~      3    3.5    1.30e9
    ##  9   48783 Flags of Our Fathers   2006 Drama|War              3    4.5    1.30e9
    ## 10   50068 Letters from Iwo Jima  2006 Drama|War              3    4.5    1.30e9
    ## # ... with 25,471 more rows

``` r
filter(movieLens, rating < 4.5)
```

    ## # A tibble: 77,186 x 7
    ##    movieId title                  year genres            userId rating timestamp
    ##      <int> <chr>                 <int> <fct>              <int>  <dbl>     <int>
    ##  1      31 Dangerous Minds        1995 Drama                  1    2.5    1.26e9
    ##  2    1029 Dumbo                  1941 Animation|Childr~      1    3      1.26e9
    ##  3    1061 Sleepers               1996 Thriller               1    3      1.26e9
    ##  4    1129 Escape from New York   1981 Action|Adventure~      1    2      1.26e9
    ##  5    1172 Cinema Paradiso (Nuo~  1989 Drama                  1    4      1.26e9
    ##  6    1263 Deer Hunter, The       1978 Drama|War              1    2      1.26e9
    ##  7    1287 Ben-Hur                1959 Action|Adventure~      1    2      1.26e9
    ##  8    1293 Gandhi                 1982 Drama                  1    2      1.26e9
    ##  9    1339 Dracula (Bram Stoker~  1992 Fantasy|Horror|R~      1    3.5    1.26e9
    ## 10    1343 Cape Fear              1991 Thriller               1    2      1.26e9
    ## # ... with 77,176 more rows

``` r
filter(movieLens, year == 1999 |year == 2000)
```

    ## # A tibble: 9,088 x 7
    ##    movieId title                   year genres           userId rating timestamp
    ##      <int> <chr>                  <int> <fct>             <int>  <dbl>     <int>
    ##  1    2694 Big Daddy               1999 Comedy                3    3      1.30e9
    ##  2    2702 Summer of Sam           1999 Drama                 3    3.5    1.30e9
    ##  3    2762 Sixth Sense, The        1999 Drama|Horror|My~      3    3.5    1.30e9
    ##  4    2841 Stir of Echoes          1999 Horror|Mystery|~      3    4      1.30e9
    ##  5    2858 American Beauty         1999 Drama|Romance         3    4      1.30e9
    ##  6    2959 Fight Club              1999 Action|Crime|Dr~      3    5      1.30e9
    ##  7    3510 Frequency               2000 Drama|Thriller        3    4      1.30e9
    ##  8    3949 Requiem for a Dream     2000 Drama                 3    5      1.30e9
    ##  9   27369 Daria: Is It Fall Yet?  2000 Animation|Comedy      3    3.5    1.30e9
    ## 10    2628 Star Wars: Episode I ~  1999 Action|Adventur~      4    5      9.50e8
    ## # ... with 9,078 more rows

``` r
filter(movieLens, title == "Little Women")
```

    ## # A tibble: 54 x 7
    ##    movieId title         year genres userId rating  timestamp
    ##      <int> <chr>        <int> <fct>   <int>  <dbl>      <int>
    ##  1     261 Little Women  1994 Drama       2    4    835355681
    ##  2     261 Little Women  1994 Drama      19    4    855194216
    ##  3     261 Little Women  1994 Drama      30    4    951008613
    ##  4     261 Little Women  1994 Drama      32    4    834828302
    ##  5     261 Little Women  1994 Drama      36    4    847057120
    ##  6     261 Little Women  1994 Drama      85    1    837513012
    ##  7     261 Little Women  1994 Drama      86    3    848161454
    ##  8     261 Little Women  1994 Drama      88    3.5 1239755456
    ##  9     261 Little Women  1994 Drama      95    5   1016317793
    ## 10     261 Little Women  1994 Drama     102    3    957894400
    ## # ... with 44 more rows

``` r
filter(movieLens, rating > 4.5, year < 1995)
```

    ## # A tibble: 8,386 x 7
    ##    movieId title                  year genres            userId rating timestamp
    ##      <int> <chr>                 <int> <fct>              <int>  <dbl>     <int>
    ##  1     265 Like Water for Choco~  1992 Drama|Fantasy|Ro~      2      5    8.35e8
    ##  2     266 Legends of the Fall    1994 Drama|Romance|Wa~      2      5    8.35e8
    ##  3     551 Nightmare Before Chr~  1993 Animation|Childr~      2      5    8.35e8
    ##  4     589 Terminator 2: Judgme~  1991 Action|Sci-Fi          2      5    8.35e8
    ##  5     590 Dances with Wolves     1990 Adventure|Drama|~      2      5    8.35e8
    ##  6     592 Batman                 1989 Action|Crime|Thr~      2      5    8.35e8
    ##  7     318 Shawshank Redemption~  1994 Crime|Drama            3      5    1.30e9
    ##  8     356 Forrest Gump           1994 Comedy|Drama|Rom~      3      5    1.30e9
    ##  9    1197 Princess Bride, The    1987 Action|Adventure~      3      5    1.30e9
    ## 10     260 Star Wars: Episode I~  1977 Action|Adventure~      4      5    9.50e8
    ## # ... with 8,376 more rows

### Exercise 3

While filtering for *all movies that do not belong to the genre drama*
above, I noticed something interesting. I want to filter for the same
thing again, this time selecting variables **title and genres first,**
and then *everything else*. Hint: there is a function to select
“everything else”…

``` r
### ERROR HERE ###
#movieLens %>%
#  filter(!genres == "Drama") %>%
#  select(title, genres, year, rating, timestamp)
```

Notice that some movies appear to have several genres, instead of a
single one. If we filter for the movie “Dumbo” and select the genres
column, we see that “Animation|Children|Drama|Musical” appear as genres.

``` r
movieLens %>%
  title == "Dumbo" %>%
  select(genres)
```

    ## Error in title(.): plot.new has not been called yet

This means that when we filter for “Drama”, we are only filtering for
those movies that are classified as *exclusively* Drama. What if we want
to see all movies that *contain* “Drama” in their genres, even if they
are a Romance-Drama, or a Comedy-Drama? Here is a handy, **error-free**
expression that can help you do that. No errors, only for learning.

``` r
movieLens %>%
  filter(str_detect(genres, "Drama"))
```

    ## # A tibble: 44,752 x 7
    ##    movieId title                  year genres            userId rating timestamp
    ##      <int> <chr>                 <int> <fct>              <int>  <dbl>     <int>
    ##  1      31 Dangerous Minds        1995 Drama                  1    2.5    1.26e9
    ##  2    1029 Dumbo                  1941 Animation|Childr~      1    3      1.26e9
    ##  3    1172 Cinema Paradiso (Nuo~  1989 Drama                  1    4      1.26e9
    ##  4    1263 Deer Hunter, The       1978 Drama|War              1    2      1.26e9
    ##  5    1287 Ben-Hur                1959 Action|Adventure~      1    2      1.26e9
    ##  6    1293 Gandhi                 1982 Drama                  1    2      1.26e9
    ##  7    2455 Fly, The               1986 Drama|Horror|Sci~      1    2.5    1.26e9
    ##  8      17 Sense and Sensibility  1995 Drama|Romance          2    5      8.35e8
    ##  9      52 Mighty Aphrodite       1995 Comedy|Drama|Rom~      2    3      8.35e8
    ## 10      62 Mr. Holland's Opus     1995 Drama                  2    3      8.35e8
    ## # ... with 44,742 more rows

Now that you know that, select (and filter, where required\!):

  - All colums *except* those from userId to timestamp (inclusive)
  - Columns year, title, and genres (in that order) *only* for movies
    classified *exclusively* as “Romance”
  - Columns rating, title, and year (in that order) followed by
    everything else (all other columns), only for movies *containing*
    the genre “Comedy”

<!-- end list -->

``` r
### ERROR HERE ###
select(movieLens, -(userId:timestamp))
```

    ## # A tibble: 100,004 x 4
    ##    movieId title                               year genres                      
    ##      <int> <chr>                              <int> <fct>                       
    ##  1      31 Dangerous Minds                     1995 Drama                       
    ##  2    1029 Dumbo                               1941 Animation|Children|Drama|Mu~
    ##  3    1061 Sleepers                            1996 Thriller                    
    ##  4    1129 Escape from New York                1981 Action|Adventure|Sci-Fi|Thr~
    ##  5    1172 Cinema Paradiso (Nuovo cinema Par~  1989 Drama                       
    ##  6    1263 Deer Hunter, The                    1978 Drama|War                   
    ##  7    1287 Ben-Hur                             1959 Action|Adventure|Drama      
    ##  8    1293 Gandhi                              1982 Drama                       
    ##  9    1339 Dracula (Bram Stoker's Dracula)     1992 Fantasy|Horror|Romance|Thri~
    ## 10    1343 Cape Fear                           1991 Thriller                    
    ## # ... with 99,994 more rows

``` r
movieLens %>%
  filter(genres == "Romance") %>%
  select(year, title, genres)
```

    ## # A tibble: 63 x 3
    ##     year title                    genres 
    ##    <int> <chr>                    <fct>  
    ##  1  1998 Meet Joe Black           Romance
    ##  2  1998 Meet Joe Black           Romance
    ##  3  1984 Against All Odds         Romance
    ##  4  1988 Everybody's All-American Romance
    ##  5  1998 Meet Joe Black           Romance
    ##  6  1998 Meet Joe Black           Romance
    ##  7  1998 Meet Joe Black           Romance
    ##  8  2004 Raise Your Voice         Romance
    ##  9  1998 Meet Joe Black           Romance
    ## 10  1998 Meet Joe Black           Romance
    ## # ... with 53 more rows

``` r
movieLens %>%
  filter(str_select(genres, Romance)) %>%
  select(year, title, genres)
```

    ## Error: Problem with `filter()` input `..1`.
    ## x could not find function "str_select"
    ## i Input `..1` is `str_select(genres, Romance)`.

### Exercise 4

Some of our variables are currently in *camelCase* (in fact, *movieLens*
is in camelCase). Let’s clean these two variables to be *snake\_case*
instead, and assign our post-rename object back to “movieLens”.

``` r
movieLens <- movieLens %>%
  rename(user_id = userId,
         movie_id = movieId)
movieLens
```

    ## # A tibble: 100,004 x 7
    ##    movie_id title                year genres            user_id rating timestamp
    ##       <int> <chr>               <int> <fct>               <int>  <dbl>     <int>
    ##  1       31 Dangerous Minds      1995 Drama                   1    2.5    1.26e9
    ##  2     1029 Dumbo                1941 Animation|Childr~       1    3      1.26e9
    ##  3     1061 Sleepers             1996 Thriller                1    3      1.26e9
    ##  4     1129 Escape from New Yo~  1981 Action|Adventure~       1    2      1.26e9
    ##  5     1172 Cinema Paradiso (N~  1989 Drama                   1    4      1.26e9
    ##  6     1263 Deer Hunter, The     1978 Drama|War               1    2      1.26e9
    ##  7     1287 Ben-Hur              1959 Action|Adventure~       1    2      1.26e9
    ##  8     1293 Gandhi               1982 Drama                   1    2      1.26e9
    ##  9     1339 Dracula (Bram Stok~  1992 Fantasy|Horror|R~       1    3.5    1.26e9
    ## 10     1343 Cape Fear            1991 Thriller                1    2      1.26e9
    ## # ... with 99,994 more rows

As you already know, `mutate()` defines and inserts new variables into a
tibble. There is *another mystery function* that you’ve seen already
that adds the new variable, and drops existing ones. I wanted to create
an average\_rating column that takes the mean(rating) across all
entries, and I only want to see that variable (i.e drop all others\!)
but I forgot what that mystery function is. Can you remember?

``` r
transmute(movieLens,
       average_rating = mean(rating))
```

    ## # A tibble: 100,004 x 1
    ##    average_rating
    ##             <dbl>
    ##  1           3.54
    ##  2           3.54
    ##  3           3.54
    ##  4           3.54
    ##  5           3.54
    ##  6           3.54
    ##  7           3.54
    ##  8           3.54
    ##  9           3.54
    ## 10           3.54
    ## # ... with 99,994 more rows

### Exercise 5

I’m interested in arranging movies from the year 1998 by their
descending rating. Then, I would like to rearrange the columns to show
`rating` followed by `title`, and then followed by everything else.

``` r
movieLens %>%
  filter(year == 1998) %>%
  arrange(desc(rating)) %>%
  select(rating, title, everything())
```

    ## # A tibble: 4,019 x 7
    ##    rating title             movie_id  year genres              user_id timestamp
    ##     <dbl> <chr>                <int> <int> <fct>                 <int>     <int>
    ##  1      5 Wedding Singer, ~     1777  1998 Comedy|Romance            8    1.15e9
    ##  2      5 American History~     2329  1998 Crime|Drama               8    1.15e9
    ##  3      5 Truman Show, The      1682  1998 Comedy|Drama|Sci-Fi       9    9.39e8
    ##  4      5 There's Somethin~     1923  1998 Comedy|Romance           10    9.43e8
    ##  5      5 Out of Sight          1912  1998 Comedy|Crime|Drama~      15    1.03e9
    ##  6      5 Rushmore              2395  1998 Comedy|Drama             15    9.98e8
    ##  7      5 Fear and Loathin~     1884  1998 Adventure|Comedy|D~      17    1.13e9
    ##  8      5 Pi                    1921  1998 Drama|Sci-Fi|Thril~      17    1.13e9
    ##  9      5 Following             2579  1998 Crime|Mystery|Thri~      17    1.13e9
    ## 10      5 Sliding Doors         1680  1998 Drama|Romance            20    1.22e9
    ## # ... with 4,009 more rows

Instead of filtering to a specific year, group the movies by year, and
then arrange by ascending rating. Lastly, select only the year, title,
and rating, in that order.

*Hint:* Grouped arrange needs one more argument…

``` r
movieLens %>%
  group_by(year) %>%
  arrange(rating, .by_group = TRUE) %>%
  select(year, title, rating)
```

    ## # A tibble: 100,004 x 3
    ## # Groups:   year [104]
    ##     year title                                         rating
    ##    <int> <chr>                                          <dbl>
    ##  1  1902 Trip to the Moon, A (Voyage dans la lune, Le)    3  
    ##  2  1902 Trip to the Moon, A (Voyage dans la lune, Le)    4  
    ##  3  1902 Trip to the Moon, A (Voyage dans la lune, Le)    4.5
    ##  4  1902 Trip to the Moon, A (Voyage dans la lune, Le)    4.5
    ##  5  1902 Trip to the Moon, A (Voyage dans la lune, Le)    5  
    ##  6  1902 Trip to the Moon, A (Voyage dans la lune, Le)    5  
    ##  7  1915 Birth of a Nation, The                           2.5
    ##  8  1915 Birth of a Nation, The                           3.5
    ##  9  1916 20,000 Leagues Under the Sea                     3.5
    ## 10  1917 Immigrant, The                                   4  
    ## # ... with 99,994 more rows

### Exercise 6

Alone, `tally()` is a short form of `summarise()`. `count()` is
short-hand for `group_by()` and `tally()`.

  - Each entry of the movieLens table corresponds to a movie rating by a
    user. Therefore, if more than one user rated the same movie, there
    will be several entries for the same movie. I want to find out how
    many times each movie has been reviewed, or in other words, how many
    times each movie title appears in the dataset.

<!-- end list -->

``` r
movieLens %>%
  group_by(title) %>%
  tally()
```

    ## # A tibble: 8,832 x 2
    ##    title                                  n
    ##    <chr>                              <int>
    ##  1 "'burbs, The"                         19
    ##  2 "'Hellboy': The Seeds of Creation"     1
    ##  3 "'Neath the Arizona Skies"             1
    ##  4 "'night Mother"                        3
    ##  5 "'Round Midnight"                      2
    ##  6 "'Salem's Lot"                         1
    ##  7 "'Til There Was You"                   4
    ##  8 "\"Great Performances\" Cats"          2
    ##  9 "$9.99"                                3
    ## 10 "(500) Days of Summer"                45
    ## # ... with 8,822 more rows

  - Without using `group_by()`, I want to find out how many movie
    reviews there have been by year.

<!-- end list -->

``` r
movieLens %>%
  count(year)
```

    ## # A tibble: 104 x 2
    ##     year     n
    ##    <int> <int>
    ##  1  1902     6
    ##  2  1915     2
    ##  3  1916     1
    ##  4  1917     2
    ##  5  1918     2
    ##  6  1919     1
    ##  7  1920    15
    ##  8  1921    12
    ##  9  1922    28
    ## 10  1923     3
    ## # ... with 94 more rows

  - Both `count()` and `tally()` can be called repeatedly, each time
    adding up a level of detail. Below, I want to count the number of
    movie reviews by title and rating, and sort the results.

<!-- end list -->

``` r
movieLens %>%
  count(title, rating)
```

    ## # A tibble: 28,297 x 3
    ##    title                            rating     n
    ##    <chr>                             <dbl> <int>
    ##  1 'burbs, The                         1.5     1
    ##  2 'burbs, The                         2       4
    ##  3 'burbs, The                         2.5     1
    ##  4 'burbs, The                         3       5
    ##  5 'burbs, The                         3.5     3
    ##  6 'burbs, The                         4       4
    ##  7 'burbs, The                         4.5     1
    ##  8 'Hellboy': The Seeds of Creation    2       1
    ##  9 'Neath the Arizona Skies            0.5     1
    ## 10 'night Mother                       5       3
    ## # ... with 28,287 more rows

Not only do `count()` and `tally()` quickly allow you to count items
within your dataset, `add_tally()` and `add_count()` are handy shortcuts
that add an additional columns to your tibble, rather than collapsing
each group.

  - Suppose that I am interested in finding movies that have very few
    reviews, very few being under 5. Without using `group_by()`, add a
    column that counts the *number of reviews per movie title*, and then
    filter to those that have 5 reviews or under. Rename the column `n`
    to `n_reviews`.

<!-- end list -->

``` r
movieLens %>%
  add_count(title, name = 'n') %>%
filter(n <= 5) %>%
mutate(n_reviews = n)
```

    ## # A tibble: 11,543 x 9
    ##    movie_id title         year genres   user_id rating timestamp     n n_reviews
    ##       <int> <chr>        <int> <fct>      <int>  <dbl>     <int> <int>     <int>
    ##  1    27369 Daria: Is I~  2000 Animati~       3    3.5    1.30e9     2         2
    ##  2    48783 Flags of Ou~  2006 Drama|W~       3    4.5    1.30e9     4         4
    ##  3    84236 White Strip~  2009 Documen~       3    4      1.30e9     1         1
    ##  4     2086 One Magic C~  1985 Drama|F~       4    5      9.50e8     1         1
    ##  5     2091 Return from~  1978 Childre~       4    5      9.50e8     3         3
    ##  6     2659 It Came fro~  1982 Comedy|~       4    3      9.50e8     3         3
    ##  7     2902 Psycho II     1983 Horror|~       4    2      9.50e8     4         4
    ##  8     2903 Psycho III    1986 Horror|~       4    1      9.50e8     3         3
    ##  9    42007 Rumor Has I~  2005 Comedy|~       8    2      1.15e9     3         3
    ## 10    43556 Annapolis     2006 Drama          8    3.5    1.15e9     1         1
    ## # ... with 11,533 more rows

### Exercise 7

  - Calculate the mean rating by title and store it in a new variable
    `avg_rating`.

<!-- end list -->

``` r
movieLens %>%
  group_by(title) %>%
  summarize(avg_rating = mean(rating))
```

    ## `summarise()` ungrouping output (override with `.groups` argument)

    ## # A tibble: 8,832 x 2
    ##    title                              avg_rating
    ##    <chr>                                   <dbl>
    ##  1 "'burbs, The"                            3.05
    ##  2 "'Hellboy': The Seeds of Creation"       2   
    ##  3 "'Neath the Arizona Skies"               0.5 
    ##  4 "'night Mother"                          5   
    ##  5 "'Round Midnight"                        2.25
    ##  6 "'Salem's Lot"                           3.5 
    ##  7 "'Til There Was You"                     2.62
    ##  8 "\"Great Performances\" Cats"            1.75
    ##  9 "$9.99"                                  3.83
    ## 10 "(500) Days of Summer"                   3.76
    ## # ... with 8,822 more rows

  - Calculate the mean rating by year and store it in a new variable
    `avg_rating`.

<!-- end list -->

``` r
movieLens %>%
  group_by(year) %>%
  summarize(avg_rating = mean(rating))
```

    ## `summarise()` ungrouping output (override with `.groups` argument)

    ## # A tibble: 104 x 2
    ##     year avg_rating
    ##    <int>      <dbl>
    ##  1  1902       4.33
    ##  2  1915       3   
    ##  3  1916       3.5 
    ##  4  1917       4.25
    ##  5  1918       4.25
    ##  6  1919       3   
    ##  7  1920       3.7 
    ##  8  1921       4.42
    ##  9  1922       3.80
    ## 10  1923       4.17
    ## # ... with 94 more rows

  - Using `summarize()`, find the minimum and the maximum rating by
    title, and store these new variables under `min_rating`, and
    `max_rating`, respectively.

<!-- end list -->

``` r
movieLens %>%
  group_by(title)%>%
  summarize(min_rating = min(rating), max_rating = max(rating))
```

    ## `summarise()` ungrouping output (override with `.groups` argument)

    ## # A tibble: 8,832 x 3
    ##    title                              min_rating max_rating
    ##    <chr>                                   <dbl>      <dbl>
    ##  1 "'burbs, The"                             1.5        4.5
    ##  2 "'Hellboy': The Seeds of Creation"        2          2  
    ##  3 "'Neath the Arizona Skies"                0.5        0.5
    ##  4 "'night Mother"                           5          5  
    ##  5 "'Round Midnight"                         0.5        4  
    ##  6 "'Salem's Lot"                            3.5        3.5
    ##  7 "'Til There Was You"                      0.5        4  
    ##  8 "\"Great Performances\" Cats"             0.5        3  
    ##  9 "$9.99"                                   2.5        4.5
    ## 10 "(500) Days of Summer"                    0.5        5  
    ## # ... with 8,822 more rows

  - Using `group_by()` and `summarize()`, find the number of reviews per
    movie title, and arrange in order of descending number of reviews.
    Notice that we achieved the same result in the previous exercise
    using `tally()`.

<!-- end list -->

``` r
movieLens %>%
    group_by(title) %>%
    summarise(n_reviews = n()) %>%
    arrange(desc(n_reviews))
```

    ## `summarise()` ungrouping output (override with `.groups` argument)

    ## # A tibble: 8,832 x 2
    ##    title                              n_reviews
    ##    <chr>                                  <int>
    ##  1 Forrest Gump                             341
    ##  2 Pulp Fiction                             324
    ##  3 Shawshank Redemption, The                311
    ##  4 Silence of the Lambs, The                304
    ##  5 Star Wars: Episode IV - A New Hope       291
    ##  6 Jurassic Park                            274
    ##  7 Matrix, The                              259
    ##  8 Toy Story                                247
    ##  9 Schindler's List                         244
    ## 10 Terminator 2: Judgment Day               237
    ## # ... with 8,822 more rows

### Exercise 8

`across()` is a new dplyr function (`dplyr` 1.0.0) that allows you to
apply a transformation to multiple variables selected with the
`select()` and `rename()` syntax. For this section, we will use the
`starwars` dataset, which is built into R. First, let’s transform it
into a tibble and store it under the variable `starWars`.

``` r
starWars <- as_tibble(starwars)
```

  - Find the mean for all columns that are numeric.

<!-- end list -->

``` r
starWars %>%
  drop_na() %>%
  summarise(across(where(is.numeric), mean))
```

    ## # A tibble: 1 x 3
    ##   height  mass birth_year
    ##    <dbl> <dbl>      <dbl>
    ## 1   186.  84.5       65.5

  - Find the minimum height and weight within each species.

<!-- end list -->

``` r
starWars %>%
  group_by(species) %>%
  summarise(height = min(height), weight = min(mass*9.8)) %>%
  drop_na()
```

    ## `summarise()` ungrouping output (override with `.groups` argument)

    ## # A tibble: 25 x 3
    ##    species   height weight
    ##    <chr>      <int>  <dbl>
    ##  1 Aleena        79   147 
    ##  2 Besalisk     198   999.
    ##  3 Cerean       198   804.
    ##  4 Clawdite     168   539 
    ##  5 Dug          112   392 
    ##  6 Ewok          88   196 
    ##  7 Geonosian    183   784 
    ##  8 Hutt         175 13308.
    ##  9 Kaleesh      216  1558.
    ## 10 Kel Dor      188   784 
    ## # ... with 15 more rows

  - Find the number of distinct names and homeworlds by each species.

<!-- end list -->

``` r
starWars %>%
  group_by(species) %>%
  filter(n() > 0) %>%
  summarise(across(c(name, homeworld), n_distinct))
```

    ## `summarise()` ungrouping output (override with `.groups` argument)

    ## # A tibble: 38 x 3
    ##    species    name homeworld
    ##    <chr>     <int>     <int>
    ##  1 Aleena        1         1
    ##  2 Besalisk      1         1
    ##  3 Cerean        1         1
    ##  4 Chagrian      1         1
    ##  5 Clawdite      1         1
    ##  6 Droid         6         3
    ##  7 Dug           1         1
    ##  8 Ewok          1         1
    ##  9 Geonosian     1         1
    ## 10 Gungan        3         1
    ## # ... with 28 more rows

``` r
  #drop_na()
```

### Exercise 9

The `singer` package was created by Joey Bernhardt, and it contains 3
datasets that are excerpts from the Million Songs Dataset. The `songs`
and the `locations` package will be used here. These two datasets have
the columns `artist_name` and `title` in common.

  - The R `merge()` function automatically joins the frames by common
    variable names. Merge `songs` and `locations` using one of the join
    family of functions (`inner_join()`, `outer_join()`, `right_join()`,
    etc…), without specifying the key variable.

<!-- end list -->

``` r
inner_join(songs, locations)
```

    ## Joining, by = c("title", "artist_name")

    ## # A tibble: 13 x 5
    ##    title                      artist_name    year city       release            
    ##    <chr>                      <chr>         <int> <chr>      <chr>              
    ##  1 "Grievance"                Pearl Jam      2000 Seattle, ~ Binaural           
    ##  2 "Stupidmop"                Pearl Jam      1994 Seattle, ~ Vitalogy           
    ##  3 "Present Tense"            Pearl Jam      1996 Seattle, ~ No Code            
    ##  4 "MFC"                      Pearl Jam      1998 Seattle, ~ Live On Two Legs   
    ##  5 "Lukin"                    Pearl Jam      1996 Seattle, ~ Seattle Washington~
    ##  6 "It's Lulu"                The Boo Radl~  1995 Liverpool~ Best Of            
    ##  7 "Sparrow"                  The Boo Radl~  1992 Liverpool~ Everything's Alrig~
    ##  8 "High as Monkeys"          The Boo Radl~  1998 Liverpool~ Kingsize           
    ##  9 "Butterfly McQueen"        The Boo Radl~  1993 Liverpool~ Giant Steps        
    ## 10 "My One and Only Love"     Carly Simon    2005 New York,~ Moonlight Serenade 
    ## 11 "It Was So Easy  (LP Vers~ Carly Simon    1972 New York,~ No Secrets         
    ## 12 "I've Got A Crush On You"  Carly Simon    1994 New York,~ Clouds In My Coffe~
    ## 13 "Manha De Carnaval (Theme~ Carly Simon    2007 New York,~ Into White

  - Join `songs` and `locations` in a way that drops all observations
    from `songs` that *do not* have a match in `locations`.

<!-- end list -->

``` r
right_join(songs, locations, by = 'title')
```

    ## # A tibble: 14 x 6
    ##    title              artist_name.x   year artist_name.y city     release       
    ##    <chr>              <chr>          <int> <chr>         <chr>    <chr>         
    ##  1 "Grievance"        Pearl Jam       2000 Pearl Jam     Seattle~ Binaural      
    ##  2 "Stupidmop"        Pearl Jam       1994 Pearl Jam     Seattle~ Vitalogy      
    ##  3 "Present Tense"    Pearl Jam       1996 Pearl Jam     Seattle~ No Code       
    ##  4 "MFC"              Pearl Jam       1998 Pearl Jam     Seattle~ Live On Two L~
    ##  5 "Lukin"            Pearl Jam       1996 Pearl Jam     Seattle~ Seattle Washi~
    ##  6 "It's Lulu"        The Boo Radle~  1995 The Boo Radl~ Liverpo~ Best Of       
    ##  7 "Sparrow"          The Boo Radle~  1992 The Boo Radl~ Liverpo~ Everything's ~
    ##  8 "High as Monkeys"  The Boo Radle~  1998 The Boo Radl~ Liverpo~ Kingsize      
    ##  9 "Butterfly McQuee~ The Boo Radle~  1993 The Boo Radl~ Liverpo~ Giant Steps   
    ## 10 "My One and Only ~ Carly Simon     2005 Carly Simon   New Yor~ Moonlight Ser~
    ## 11 "It Was So Easy  ~ Carly Simon     1972 Carly Simon   New Yor~ No Secrets    
    ## 12 "I've Got A Crush~ Carly Simon     1994 Carly Simon   New Yor~ Clouds In My ~
    ## 13 "Manha De Carnava~ Carly Simon     2007 Carly Simon   New Yor~ Into White    
    ## 14 "Stuck On Amber"   <NA>              NA The Boo Radl~ Liverpo~ Wake Up!

  - Combine `locations` and `songs` to find only the entries that
    correspond to song titles in the `locations` dataset.

<!-- end list -->

``` r
left_join(locations, songs)
```

    ## Joining, by = c("artist_name", "title")

    ## # A tibble: 14 x 5
    ##    artist_name   city        release             title                      year
    ##    <chr>         <chr>       <chr>               <chr>                     <int>
    ##  1 Pearl Jam     Seattle, WA Binaural            "Grievance"                2000
    ##  2 Pearl Jam     Seattle, WA Vitalogy            "Stupidmop"                1994
    ##  3 Pearl Jam     Seattle, WA No Code             "Present Tense"            1996
    ##  4 Pearl Jam     Seattle, WA Live On Two Legs    "MFC"                      1998
    ##  5 Pearl Jam     Seattle, WA Seattle Washington~ "Lukin"                    1996
    ##  6 The Boo Radl~ Liverpool,~ Wake Up!            "Stuck On Amber"             NA
    ##  7 The Boo Radl~ Liverpool,~ Best Of             "It's Lulu"                1995
    ##  8 The Boo Radl~ Liverpool,~ Everything's Alrig~ "Sparrow"                  1992
    ##  9 The Boo Radl~ Liverpool,~ Kingsize            "High as Monkeys"          1998
    ## 10 The Boo Radl~ Liverpool,~ Giant Steps         "Butterfly McQueen"        1993
    ## 11 Carly Simon   New York, ~ Moonlight Serenade  "My One and Only Love"     2005
    ## 12 Carly Simon   New York, ~ No Secrets          "It Was So Easy  (LP Ver~  1972
    ## 13 Carly Simon   New York, ~ Clouds In My Coffe~ "I've Got A Crush On You"  1994
    ## 14 Carly Simon   New York, ~ Into White          "Manha De Carnaval (Them~  2007

  - Merge `songs` and `locations` so that *all information* from both
    datasets is combined.

<!-- end list -->

``` r
full_join(songs, locations)
```

    ## Joining, by = c("title", "artist_name")

    ## # A tibble: 23 x 5
    ##    title                 artist_name    year city         release               
    ##    <chr>                 <chr>         <int> <chr>        <chr>                 
    ##  1 Corduroy              Pearl Jam      1994 <NA>         <NA>                  
    ##  2 Grievance             Pearl Jam      2000 Seattle, WA  Binaural              
    ##  3 Stupidmop             Pearl Jam      1994 Seattle, WA  Vitalogy              
    ##  4 Present Tense         Pearl Jam      1996 Seattle, WA  No Code               
    ##  5 MFC                   Pearl Jam      1998 Seattle, WA  Live On Two Legs      
    ##  6 Lukin                 Pearl Jam      1996 Seattle, WA  Seattle Washington No~
    ##  7 It's Lulu             The Boo Radl~  1995 Liverpool, ~ Best Of               
    ##  8 Sparrow               The Boo Radl~  1992 Liverpool, ~ Everything's Alright ~
    ##  9 Martin_ Doom! It's S~ The Boo Radl~  1995 <NA>         <NA>                  
    ## 10 Leaves And Sand       The Boo Radl~  1993 <NA>         <NA>                  
    ## # ... with 13 more rows

### Exercise 10

Time for reviewing… and tibbles\!

  - Create a tibble with 4 columns, `birth_year`, `name`,
    `birth_weight`, and `birth_location`. `birth_year` should contain
    years 1998 to 2005 (inclusive), `name` should contain the first 8
    names in the `starWars` dataset `name` column, and `birth_weight`
    should take the `year` column, subtract 1995, and multiply by 0.45.
    `birth_location` should contain 8 randomly sampled locations in the
    `locations` dataset `city` column.

  - This tibble should be stored in the variable `fakeStarWars`.

<!-- end list -->

``` r
fakeStarWars <-
tibble(birth_year = 1998:2005,
       name = starWars$name[1:8],
       birth_weight = (birth_year - 1995) * 0.45,
       birth_location = sample(locations$city, size = 8))
```

Let’s look at this new tibble.

``` r
fakeStarWars
```

    ## # A tibble: 8 x 4
    ##   birth_year name               birth_weight birth_location    
    ##        <int> <chr>                     <dbl> <chr>             
    ## 1       1998 Luke Skywalker             1.35 New York, NY      
    ## 2       1999 C-3PO                      1.8  Seattle, WA       
    ## 3       2000 R2-D2                      2.25 Seattle, WA       
    ## 4       2001 Darth Vader                2.7  Seattle, WA       
    ## 5       2002 Leia Organa                3.15 Liverpool, England
    ## 6       2003 Owen Lars                  3.6  Liverpool, England
    ## 7       2004 Beru Whitesun lars         4.05 Seattle, WA       
    ## 8       2005 R5-D4                      4.5  New York, NY

  - Without assigning it to any variables, define the same tibble
    row-by-row with `tribble()`, with the columns in the following
    order: `name`, `birth_weight`, `birth_year`, `birth_location`.

<!-- end list -->

``` r
tribble(
  ~name,            ~birth_year,  ~birth_weight, ~location,
  "Luke Skywalker",  1.35      ,   1998        ,  "Liverpool, England",
  "C-3PO"         ,  1.80      ,   1999        ,  "Liverpool, England",
  "R2-D2"         ,  2.25      ,   2000        ,  "Seattle, WA",
  "Darth Vader"   ,  2.70      ,   2001        ,  "Liverpool, England",
  "Leia Organa"   ,  3.15      ,   2002        ,  "New York, NY",
  "Owen Lars"     ,  3.60      ,   2003        ,  "Seattle, WA",
  "Beru Whitesun Iars", 4.05   ,   2004        ,  "Liverpool, England",
  "R5-D4"         ,  4.50      ,   2005        ,  "New York, NY",
)
```

    ## # A tibble: 8 x 4
    ##   name               birth_year birth_weight location          
    ##   <chr>                   <dbl>        <dbl> <chr>             
    ## 1 Luke Skywalker           1.35         1998 Liverpool, England
    ## 2 C-3PO                    1.8          1999 Liverpool, England
    ## 3 R2-D2                    2.25         2000 Seattle, WA       
    ## 4 Darth Vader              2.7          2001 Liverpool, England
    ## 5 Leia Organa              3.15         2002 New York, NY      
    ## 6 Owen Lars                3.6          2003 Seattle, WA       
    ## 7 Beru Whitesun Iars       4.05         2004 Liverpool, England
    ## 8 R5-D4                    4.5          2005 New York, NY

Now, for the grand finale\!

``` r
gapminder_almost <- gapminder %>% filter(continent == "Europe") %>% distinct(year, .keep_all = TRUE)
```

  - Rearrange variables from the `fakeStarWars` dataset to be in the
    following order: `name`, `birth_year`, `birth_weight`,
    `birth_location`.
  - Rename `birth_year` to `year`.
  - Combine `fakeStarWars` to `gapminder_almost` by `year`, so that only
    those entries with a year that is present in `fakeStarWars` are
    merged.
  - Drop variables `country`, `continent`, `pop`, and `gdpPercap`.
  - Add a column that summarizes the number of times that
    `birth_location` entries are repeated, and name it “n\_location”.
  - Filter out locations repeated under 4 times.
  - Arrange by descending birth weight.
  - Drop any rows with NA values in any variable.
  - Join with the `starwars` dataset so that only those rows that are
    *present in `fakeStarWars`* are combined.
  - Calculate BMI (body mass index) by dividing weight (`mass`) by
    squared `height` *in meters*. Store it in a column with the name
    `bmi`.

<!-- end list -->

``` r
fakeStarWars %>%
  select(name, birth_year,birth_weight,birth_location) %>%
  rename(year = birth_year) %>%
  left_join(gapminder_almost, by = 'year') %>%
  select(-c(country, continent, population, gdp)) %>%
  add_count(birth_location, name = "n_location") %>%
  filter(n_location < 4) %>%
  arrange(desc(birth_weight)) %>%
  drop_na() %>%
  left_join(starwars) %>%
  mutate(bmi = mass / height / 100 ^ 2)
```

    ## Note: Using an external vector in selections is ambiguous.
    ## i Use `all_of(population)` instead of `population` to silence this message.
    ## i See <https://tidyselect.r-lib.org/reference/faq-external-vector.html>.
    ## This message is displayed once per session.

    ## Error: Must subset columns with a valid subscript vector.
    ## [31mx[39m Subscript has the wrong type `tbl_df<
    ##   country   : character
    ##   year      : integer
    ##   population: integer
    ## >`.
    ## [34mi[39m It must be numeric or character.
