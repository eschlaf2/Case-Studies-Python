# Case-Studies-Python

### Quick start to learning Python for neural data analysis:

- Visit the [web-formatted version of the book](https://mark-kramer.github.io/Case-Studies-Python/intro.html).
- Read and interact with the Python code in your web browser.

### Slow start to learning Python for neural data analysis:

- See [below](#started)

----
This repository is a companion to the textbook [Case Studies in Neural Data Analysis](https://mitpress.mit.edu/books/case-studies-neural-data-analysis), by Mark Kramer and Uri Eden. That textbook used MATLAB to analyze examples of neuronal data. The material here is  similar, except that we use Python.

The intended audience is the *practicing neuroscientist* - e.g., the students, researchers, and clinicians collecting neuronal data in the hospital or lab.  The material can get pretty math-heavy, but we've tried to outline the main concepts as directly as possible, with hands-on implementations of all concepts.  We focus on only two main types of data: spike trains and electric fields (such as the local field potential [LFP], or electroencephalogram [EEG]).  If you're interested in other data (e.g., calcium imaging, or BOLD), you may still find the examples indirectly useful (for example, demonstrations of how to compute and interpret a power spectrum of a signal).

This repository was created by Emily Schlafly and Mark Kramer, with important contributions from Dr. Anthea Cheung.

---

# Getting Started[](#started)

There are multiple ways to interact with these notebooks.

- **Simple**: Visit the [web-formatted version of the notebooks](https://mark-kramer.github.io/Case-Studies-Python/intro.html).

- **Intermediate**  Open a notebook in <a href="https://mybinder.org/v2/gh/Mark-Kramer/Case-Studies-Python.git/master?filepath=content">Binder</a> and interact with the notebooks through a JupyterHub server. Binder provides an easy interface to interact with this material; read about it in [eLife](https://elifesciences.org/labs/a7d53a88/toward-publishing-reproducible-computation-with-binder).

- **Advanced**: Run the notebooks locally on your computer in <a href="https://jupyter.org/">Jupyter</a>. You'll then be able to read, edit and execute the Python code directly in your browser and you can save any changes you make or notes that you want to record. To access and download a notebook, visit the [Contents](#contents). You will need to [install Python](#install-python) and we recommend [configure Python](#configure-python).

---

# Install Python

We assume you have installed Python and can get it running on your computer.  Some useful references to do so include,

- [Python.org](https://www.python.org/)

- [Miniconda](https://docs.conda.io/en/latest/miniconda.html)

- [Anaconda](https://www.anaconda.com/products/individual)

If this is your first time working with Python, using [Anaconda](https://www.anaconda.com/products/individual) is probably a good choice. It provides a simple, graphical interface to start [Jupyter](https://jupyter.org/).

--- 

# Configure Python

Once you have installed Anaconda or Miniconda, we recommend setting up an [environment](https://docs.conda.io/projects/conda/en/latest/user-guide/concepts/environments.html) to run the notebooks. Type the following code into your terminal to create and activate an environment called `csn`. 

```
conda create env --file csn.yml
conda activate csn
```

This will ensure that you have all the packages needed to run the notebooks. If you run a notebook at this point, you may notice that when you generate plots, they look different. If you want to match the formatting in the published version, you can run the following in your terminal:

```
mkdir ~/.jupyter
cp -ir assets/custom ~/.jupyter/
mkdir -p ~/.ipython/profile_default/
cp -ir startup ~/.ipython/profile_default/
```

Note that if you already have files in these directories, you will be prompted to overwrite them. In this case, you may prefer to append the contents to the end of the existing files. You can do this with the following:

```
for f in $(ls assets/custom); do echo $(assets/custom/$f) >> ~/.jupyter/custom/$f; done
for f in $(ls startup); do echo $(startup/$f) >> ~/.ipython/profile_default/startup/$f; done
```

---

# Contents[](#contents) 

1. [Introduction to Python](content/01)
2. [The Event-Related Potential](content/02)
3. [The Power Spectrum (Part 1)](content/03)
4. [The Power Spectrum (Part 2)](content/04)
5. [The Cross Covariance and Coherence](content/05)
6. [Filtering Field Data](content/06)
7. [Cross Frequency Coupling](content/07)
8. [Basic Visualizations and Descriptive Statistics of Spike Train Data](content/08)
9. [Modeling place Fields with Point Process Generalized Linear Models](content/09)
10. [Analysis of Rhythmic Spiking in the Subthalamic Nucleus During a Movement Task](content/10)
11. [Analysis of Spike-Field Coherence](content/11)

# Appendices

1. [Appendix: Backpropagation](content/A01)
1. [Appendix: Hodgkin Huxley Model](content/A02)
1. [Appendix: Integrate and Fire Model](content/A03)
1. [Appendix: Training a Perceptron](content/A04)



