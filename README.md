# CEBD1160-Big-Data
=============

Synopsis
=============
CEBD1160 - Big Data Project
This repository is the first step of a journey in the Big Data diploma at Concordia University.

Motivation
=============

The repository contains the Final project for class CEBD1160. 
In the course we were taught how to use Docker for Linux, Gnuplot, R programming language, and Python programming language.

It contains 3 different folders:

1) Data - contains the .csv file of the dataset that was used
2) Gnuplot - contains 4 files the code (codefile.txt) and the 3 different outputs (outputx.png, outputy.png, outputxy.png)
3) r - contains 4 files the code (rcode.txt) and the 3 different outputs (xplot.pdf, yplot.pdf, xyplot.pdf)

Code
=============

The class used Docker for Linux to run Gnuplot.
We first used Gnuplot commands to create the visuals on the datset and then we uploaded them to github.

Example of Gnuplot Code to plot variable x:
#start GNUPlot
root@c1652435b0bd:/CEBD1160-Big-Data/GNUPLOT# gnuplot
#set terminal
gnuplot> set terminal png
#set the output file name
gnuplot> set output 'outputx.png'
#set dimensions
gnuplot> set samples 50, 50
#set title name
gnuplot> set title "X Plot"
#plot x
gnuplot> bin_width = 3000
gnuplot> bin_number(x) = floor(x/bin_width)
gnuplot> rounded(x) = bin_width * ( bin_number(x) + 0.5 )
#output the graph
gnuplot> plot 'datafilex.csv' using (rounded($1)):(1) smooth frequency with boxes


We then replicated the Gnuplot exercise by using the R programming language

Example of R code to plot variable x:
#read the data file into JK
> JK <- read.csv("https://raw.githubusercontent.com/jkooner44/CEBD1160-Big-Data/master/data/datafile.csv")
#plot a histogram on Total Population field
> hist(JK[,2], main="X Plot", xlab="Population")


GITHUB
=============

For all folders the results were uploaded to Github using Docker for Linux
The steps were:

1. Start docker and start new container
2. Find and write down filepath of container
3. Download github repository
4. Change directory into local copy of github repo
5. Find and write down filepath of github repo
6. Copy local repo into Docker container
7. Create directory within local repo called “Linux”
8. Download data and copy into new “Linux” directory


