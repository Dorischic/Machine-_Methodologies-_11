# Machine-_Methodologies-_11
This project provides a complete exploratory data analysis in Python on a roller coaster dataset
This project is all about a full exploratory data analysis (EDA) in Python, using a dataset of roller coasters. It covers the usual sequence: load the data, understand it, clean and prepare it, look at each variable on its own, look at how variables relate, and then use the data to answer a specific question.
I replicated the whole notebook cell by cell. Instead of just writing the code, I stopped at each block to work out what it was doing and why it sat in that position. This document records that process, and it covers the concepts, the reasoning, my decisions, and the problems I hit.
Concepts and Techniques
Setup: I import pandas, numpy, matplotlib, and seaborn, and set the ggplot style to keep every chart consistent.
Data understanding: head, tail, shape, dtypes, and describe show the structure, data types, and any odd values before I change anything.
Data preparation: I check for irrelevant columns, duplicates, and missing values, then rename columns using a dictionary to keep names consistent.
Single-variable analysis: a bar chart of value counts shows the busiest years. A histogram and KDE show the shape of coaster speeds, and a boxplot would show outliers.
Relationships: a scatterplot compares speed and height. A pairplot compares several variables at once, and a correlation heatmap summarises how strongly they move together. Correlation shows association, not cause.
Asking a question: to find the locations with the fastest coasters, I filter out "other", group by location, calculate mean speed and count, keep locations with at least 10 coasters, sort, and plot a horizontal bar chart. The minimum count matters because averages from very few coasters can mislead.
My Approach
I downloaded the roller coaster dataset from Kaggle, fixed the setup code, loaded the CSV, inspected the data, checked for nulls and duplicates, made the single-variable plots, and then the relationship plots. I built the final query one line at a time, checking the output at each stage.
Setup
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

Key Takeaways
Look at the data before analysing it.
Each chart type answers a different question.
Sample size affects how far an average can be trusted.
Building chained code step by step makes it easier to debug.
