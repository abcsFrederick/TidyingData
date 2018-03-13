Data Tidying: Practice
================
Drs. Sarangan Ravichandran and Randall Johnson
February 26, 2017

### Cleaning up

For the remainder of our time, you may continue to work on this example data set or begin working with your own data. If you would like to continue with this example, open the a copy of this Rmd file and edit it. Include all of your answers in the Rmd file, as well as any other code and relevant discussion. We will stick around for awhile to answer any questions you might have.

Hands-on exercise using Wisconsin Breast Cancer dataset
=======================================================

Now, we will read a slightly complicated Breast Cancer dataset. You may use the import data set drop-down option to read the data in, but be sure to save the code generated by the dialog and record it in the code chunk below.

![](Images/RS-ImportDataset.png) ![](Images/RS-ImportDataset1.png)

The `wdbc` data set has 569 samples and 32 covariates. There are mean, standard error and worst observations for the following measures (see the [wdbc.names](https://github.com/ravichas/TidyingData/blob/master/Data/wdbc.names) file for more details):

-   Texture
-   Perimeter
-   area
-   smoothness
-   compactness
-   concavity
-   concave\_points
-   symmetry
-   fractaldim

Figures showing the raw relationship between diagnosis (benign or metastatic) tumors and some of these measures follows:

![](4-Practice_files/figure-markdown_github/raw%20data-1.png)![](4-Practice_files/figure-markdown_github/raw%20data-2.png)![](4-Practice_files/figure-markdown_github/raw%20data-3.png)![](4-Practice_files/figure-markdown_github/raw%20data-4.png)

The perimter of the cells appears to be fairly consistent within most samples, but 10.5% of the samples had a standard error over 5. Of these, 96.7% were diagnosed as metastatic.

| measure         |        meanB|        meanM|
|:----------------|------------:|------------:|
| Texture         |   17.9147619|   21.6049057|
| Perimeter       |   78.0754062|  115.3653774|
| area            |  462.7901961|  978.3764151|
| smoothness      |    0.0924776|    0.1028985|
| compactness     |    0.0800846|    0.1451878|
| concavity       |    0.0460576|    0.1607747|
| concave\_points |    0.0257174|    0.0879900|
| symmetry        |    0.1741860|    0.1929090|
| fractaldim      |    0.0628674|    0.0626801|