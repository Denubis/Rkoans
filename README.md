RKoans
======

Rkoans is an interactive tutorial for learning R in a Unit-testing framework with added cod-Zen fluff.  No previous knowledge of R is required.

As well as being a fun way to learn R, it is also a good way to get an idea of Test-driven development.
## Getting started

First, you need to clone the Rkoans repo and change into the Rkoans directory:

```
git clone
cd Rkoans
```

Then, either fire up R in this directory or start RStudio and create a new project from the Rkoans directory. Then you can load Rkoans  `devtools` package:


```r
# Make sure you are in the Rkoans directory
require(devtools)
load_all(".")
```


## Studying the koans

To start learning R through the Rkoans, first load Rkoans (see above), then enter:


```r
study_koans()
```


and you should see something similar to:

```
...
f. Failure: What is true, is true ------------------------------------------------------------------------------------
TRUE == 0 isn't true

g. Failure: What is true, is true ------------------------------------------------------------------------------------
TRUE == 2 isn't true
what_is_true.R is damaging your karma.
Study this koan to gain new insight...
```

This is telling you that you have failing tests in the file what_is_true.R.  The koans are all found in the `koans` directory within Rkoans.  Go to that file in your text editor or RStudio and start editing the tests in order to make them pass.  You will need to fill in the blanks (`_`) so that the test statement is true.  When you save the file, the koan reader will update your progress.  If all the tests pass on your file, you will then move on to the next one.
If an answer is not immediately evident, drop out of the koan reader (escape in RStudio or C-C if you are running R from the console) and test the expressions or look for help on the R console.

Remember, to ask for help in R, enter `?` and the function you want to know about:


```r
# e.g.
`?`(sign)
```


## Unit testing with testthat

Rkoans uses the [testthat](https://github.com/hadley/testthat) unit testing framework.  Tests are built from expectations which read almost like English:


```r
# testthat expectation example.
expect_that(1 + 1, equals(2))
```


For a test to pass, the expectation must be met.

For more on using the testthat framework, see this [paper](http://journal.r-project.org/archive/2011-1/RJournal_2011-1_Wickham.pdf).

## Stability

So far, I have only tested Rkoans on Linux.  Other platforms (particularly Windows) may have problems.

## Contributing

Patches are encouraged! Send me a pull request with a new or revised koan file.  Look here for lots of ideas for new koans to start, or things to add to existing koans. So write some fun exercises, add your koans to R/koans.R and your answers to answers/koans.R, check that the tests pass using the koan_tester.R functions and I'll include them!

Feel free to contact me if you have any questions or want more information before you start contributing.

## Contributors

TBC

## Credits

This project would not have been possible without Hadley wickham's [testthat](https://github.com/hadley/testthat) package.

Using the koans metaphor as a tool for learning a programming language started with the [Ruby Koans](https://github.com/neo/ruby_koans) by EdgeCase.  This package was directly influenced by the [Clojure Koans](https://github.com/functional-koans/clojure-koans) and [Python Koans](https://github.com/gregmalcolm/python_koans).


