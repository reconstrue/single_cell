# Monocle 3

This directory contains Jupyter notebooks that use
[Monocle 3](https://cole-trapnell-lab.github.io/monocle3/) is "an analysis
toolkit for single-cell RNA-seq." It is
[MIT](https://github.com/cole-trapnell-lab/monocle3/blob/master/LICENSE.md)
code out of Seattle's Seattle Lake Union area.

As with the rest of this repository, these are simply Jupyter
notebooks tuned up to work on Google's
[Colab](https://colab.research.google.com/) free Jupyter hosting
service which comes with optional free GPUs and TPUs. The core of Colab
is simply another Jupyter kernel; the tuning up is for UI and storage issues
specific to Google's front-end. Nonetheless, the
notebooks are tested to run on vanila JupyterLab.

## R Jupyter Notebook

The first notebook written was `monocle3_on_colab_in_r.ipynb` which, as the 
name implies, is an R Jupyter notebook as can been seen by examining the raw 
source of the `.ipynb` file:
```json
{
  "nbformat": 4,
  "nbformat_minor": 0,
  "metadata": {
    "language_info": {
      "codemirror_mode": "r",
      "file_extension": ".r",
      "mimetype": "text/x-r-source",
      "name": "R",
      "pygments_lexer": "r",
      "version": "3.3.1"
    },
    "kernelspec": {
      "display_name": "R",
      "language": "R",
      "name": "ir"
    }
  }...
```

That experiment went well enough that folks were able to perform analyses 
dispite the current UI limitations of R on Colab.

## Python Jupyter Notebook

After banging head against the current limitations of R UI on Colab,
the second notebook, `monocle3_on_colab_in_python.ipynb`, was started
as a Python notebook. Python can call into R code on Colab. In this
notebook, `monocle3` is treated as a non-UI funtion, "Here's some
data, now you give me some data back." The results are then in
Python-land and can be graphically presented to the use via Python
libraries such at Altair and Plotly.



