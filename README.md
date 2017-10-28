# CEBD1160-Big-Data
=============

Synopsis
=============
CEBD1160 - Big Data Project
This repository is the first step of a journey in the Big Data diploma at Concordia University.

Motivation
=============

The repository contains the Final project for class CEBD1160. 
In the course we were taught how to use Docker, Linux, Gnuplot, R programming language, and Python programming language.

It contains 3 different folders:

1) Data - contains the .csv file of the dataset that was used
2) Gnuplot - contains 4 files the code (codefile.txt) and the different outputs (outputx.png, outputy.png, outputxy.png)
3) r - contains 4 files the code (rcode.txt) and the different outputs (xplot.pdf, yplot.pdf, xyplot.pdf)

Code
=============

The class used Linux to upload the data results to Gnuplot.
We first used Gnuplot commands to create the visuals on the datset and then we uploaded them to github.

Example of basic code:
set terminal png
set output 'test.png'
bin_width = .1

bin_number(x) = floor(x/bin_width)

rounded(x) = bin_width * ( bin_number(x) + 0.5 )
set yrange [0:10]
plot 'gaussian.csv' using (rounded($1)):(1) smooth frequency with boxes

We then replicated the Gnuplot exercise by using the R programming language

Example of R code:
install.packages(“RCurl”)
library(RCurl)
y <- read.csv("https://raw.github.com/aronlindberg/latent_growth_classes/master/LGC_data.csv")

