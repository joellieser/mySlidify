---
 title    : Developing Data Products 
 substitle: Slidify Portion of Class Project
 author   : Joel Lieser
 framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
 highlighter : highlight.js  # {highlight.js, prettify, highlight}
 hitheme     : tomorrow      # 
 widgets     : []            # {mathjax, quiz, bootstrap}
 mode        : selfcontained # {standalone, draft, selfcontained}
---

This is the Slidify portion of the class Project.

<div style='text-align: center;'>
    <img height='560' src='../assets/img/ddp.PNG' />
</div>

I chose to attempt to use the lyrics to identify the genre of songs

--- 

The project took the lyrics of 1383 songs from various locations, including:

- http://www.rollingstone.com/music/lists/the-500-greatest-songs-of-all-time-20110407

- http://www.stereogum.com/24391/vh1s_100_greatest_hiphop_songs-2/list/

- http://tasteofcountry.com/top-100-country-songs/

(amongst others)

Then downloaded the lyrics from the api at http://www.chartlyrics.com/api.aspx

--- 

A number of "standard" words were identified and filtered out:


```
##   [1] "a"         "about"     "after"     "all"       "also"     
##   [6] "an"        "and"       "another"   "any"       "are"      
##  [11] "as"        "at"        "be"        "because"   "been"     
##  [16] "before"    "being"     "between"   "both"      "but"      
##  [21] "by"        "came"      "can"       "come"      "could"    
##  [26] "did"       "do"        "does"      "each"      "else"     
##  [31] "for"       "from"      "get"       "got"       "had"      
##  [36] "has"       "have"      "he"        "his"       "her"      
##  [41] "hers"      "here"      "how"       "we"        "ll"       
##  [46] "my"        "s"         "m"         "n"         "t"        
##  [51] "d"         "i"         "if"        "in"        "into"     
##  [56] "is"        "it"        "its"       "just"      "like"     
##  [61] "me"        "make"      "many"      "might"     "of"       
##  [66] "on"        "only"      "or"        "other"     "our"      
##  [71] "out"       "over"      "re"        "same"      "should"   
##  [76] "since"     "so"        "some"      "still"     "such"     
##  [81] "take"      "than"      "that"      "the"       "then"     
##  [86] "there"     "these"     "they"      "them"      "this"     
##  [91] "those"     "through"   "to"        "too"       "up"       
##  [96] "use"       "way"       "well"      "went"      "were"     
## [101] "what"      "when"      "where"     "which"     "while"    
## [106] "will"      "wont"      "baby"      "back"      "cause"    
## [111] "don"       "down"      "ever"      "every"     "go"       
## [116] "gonna"     "good"      "hey"       "him"       "know"     
## [121] "let"       "love"      "no"        "not"       "now"      
## [126] "oh"        "one"       "said"      "say"       "she"      
## [131] "thing"     "ve"        "was"       "yeah"      "again"    
## [136] "ain"       "am"        "around"    "away"      "day"      
## [141] "everybody" "feel"      "keep"      "life"      "little"   
## [146] "long"      "look"      "man"       "never"     "night"    
## [151] "ooh"       "right"     "see"       "time"      "want"     
## [156] "who"       "woman"     "yes"       "with"      "would"    
## [161] "you"       "your"
```

--- 

Then through extensive data cleansing, identified the top 40 words from each genre and chose 72 total from them identifying words per genre, and then applied a random forest, which isn't very accurate at all. 
<br>
Overall Statistics
                                          
               Accuracy : 0.2678          
                 95% CI : (0.2222, 0.3174)
    No Information Rate : 0.2678          
    P-Value [Acc > NIR] : 0.5203          
    
--- 

The Shiny App that illustrates this model and the associated github directory containing the full code are:

http://joellieser.shinyapps.io/developingDataProducts

https://github.com/joellieser/DevelopingDataProducts/

