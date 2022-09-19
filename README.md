# Matplotlib_tutorial_for_Beginners

This repository is all about Matplotlib, the basic data visualization tool of Python programming language. I have covered Matplotlib object hierarchy, various plot types with Matplotlib and customization techniques associated with Matplotlib.

This repository is divided into various sections based on contents which are listed below:-

<a class="anchor" id="0.1"></a>
# **Table of Contents**

1. [Introduction](#1)
2. [Overview of Python Data Visualization Tools](#2)
3. [Introduction to Matplotlib](#3)
4. [Import Matplotlib](#4)
5. [Displaying Plots in Matplotlib](#5)
6. [Matplotlib Object Hierarchy](#6)
7. [Matplotlib interfaces](#7)
8. [Pyplot API](#8)
9. [Object-Oriented API](#9)
10. [Figure and Subplots](#10)
11. [First plot with Matplotlib](#11)
12. [Multiline Plots](#12)
13. [Parts of a Plot](#13)
14. [Saving the Plot](#14)
15. [Line Plot](#15)
16. [Scatter Plot](#16)
17. [Histogram](#17)
18. [Bar Chart](#18)
19. [Horizontal Bar Chart](#19)
20. [Error Bar Chart](#20)
21. [Stacked Bar Chart](#21)
22. [Pie Chart](#22)
23. [Box Plot](#23)
24. [Area Chart](#24)
25. [Contour Plot](#25)
26. [Styles with Matplotlib Plots](#26)
27. [Adding a grid](#27)
28. [Handling axes](#28)
29. [Handling X and Y ticks](#29)
30. [Adding labels](#30)
31. [Adding a title](#31)
32. [Adding a legend](#32)
33. [Control colours](#33)
34. [Control line styles](#34)
35. [Summary](#35)

## **1. Introduction** <a class="anchor" id="1"></a>
[Table of Contents](#0.1)

When we want to convey some information to others, there are several ways to do so. The process of conveying the information with the help of plots and graphics is called **Data Visualization**. The plots and graphics take numerical data as input and display output in the form of charts, figures and tables. It helps to analyze and visualize the data clearly and make concrete decisions. It makes complex data more accessible and understandable. The goal of data visualization is to communicate information in a clear and efficient manner.

In this project, I shed some light on **Matplotlib**, which is the basic data visualization tool of Python programming language. Python has different data visualization tools available which are suitable for different purposes. First of all, I will list these data visualization tools and then I will discuss Matplotlib.

## **2. Overview of Python Visualization Tools**<a class="anchor" id="2"></a>
[Table of Contents](#0.1)

Python is the preferred language of choice for data scientists. Python have multiple options for data visualization. It has several tools which can help us to visualize the data more effectively. These Python data visualization tools are as follows:-

- Matplotlib
- Seaborn
- pandas
- Bokeh
- Plotly
- ggplot
- pygal

In the following sections, I discuss Matplotlib as the data visualization tool. 

## **3. Introduction to Matplotlib**<a class="anchor" id="3"></a>
[Table of Contents](#0.1)

**Matplotlib** is the basic plotting library of Python programming language. It is the most prominent tool among Python visualization packages. Matplotlib is highly efficient in performing wide range of tasks. It can produce publication quality figures in a variety of formats.  It can export visualizations to all of the common formats like PDF, SVG, JPG, PNG, BMP and GIF. It can create popular visualization types – line plot, scatter plot, histogram, bar chart, error charts, pie chart, box plot, and many more types of plot. Matplotlib also supports 3D plotting. Many Python libraries are built on top of Matplotlib. For example, pandas and Seaborn are built on Matplotlib. They allow to access Matplotlib’s methods with less code. 

The project **Matplotlib** was started by John Hunter in 2002. Matplotlib was originally started to visualize Electrocorticography (ECoG) data of epilepsy patients during post-doctoral research in Neurobiology. The open-source tool Matplotlib emerged as the most widely used plotting library for the Python programming language. It was used for data visualization during landing of the Phoenix spacecraft in 2008.

## **4. Import Matplotlib**<a class="anchor" id="4"></a>
[Table of Contents](#0.1)

Most of the time, we have to work with **pyplot** interface of Matplotlib. So, I will import **pyplot** interface of Matplotlib as follows:-

`import matplotlib.pyplot`

To make things even simpler, we will use standard shorthand for Matplotlib imports as follows:-

`import matplotlib.pyplot as plt`

## **5. Displaying Plots in Matplotlib**<a class="anchor" id="5"></a>
[Table of Contents](#0.1)

Viewing the Matplotlib plot is context based. The best usage of Matplotlib differs depending on how we are using it. There are three applicable contexts for viewing the plots. The three applicable contexts are using plotting from a script, plotting from an IPython shell or plotting from a Jupyter notebook.

1. ### Plotting from a script

    - If we are using Matplotlib from within a script, then the **plt.show()** command is of great use. It starts an event loop, 
looks for all currently active figure objects, and opens one or more interactive windows that display the figure or figures.

    - The **plt.show()** command should be used only once per Python session. It should be used only at the end of the script. Multiple **plt.show()** commands can lead to unpredictable results and should mostly be avoided.

2. ### Plotting from an IPython shell

    - We can use Matplotlib interactively within an IPython shell. IPython works well with Matplotlib if we specify Matplotlib mode. To enable this mode, we can use the **%matplotlib** magic command after starting ipython. Any plt plot command will cause a figure window to open and further commands can be run to update the plot.

3. ### Plotting from a Jupyter notebook

    - The Jupyter Notebook (formerly known as the IPython Notebook) is a data analysis and visualization tool that provides multiple tools under one roof.  It provides code execution, graphical plots, rich text and media display, mathematics formula and much more facilities into a single executable document.

    - Interactive plotting within a Jupyter Notebook can be done with the **%matplotlib** command. There are two possible options to work with graphics in Jupyter Notebook. These are as follows:-

      - **%matplotlib notebook** – This command will produce interactive plots embedded within the notebook.

      - **%matplotlib inline** – It will output static images of the plot embedded in the notebook.

    After this command (it needs to be done only once per kernel per session), any cell within the notebook that creates a plot will embed a PNG image of the graphic.

## **6. Matplotlib Object Hierarchy**<a class="anchor" id="6"></a>
[Table of Contents](#0.1)

There is an Object Hierarchy within Matplotlib. In Matplotlib, a plot is a hierarchy of nested Python objects. A **hierarch** means that there is a tree-like structure of Matplotlib objects underlying each plot.

A **Figure** object is the outermost container for a Matplotlib plot. The **Figure** object contain multiple **Axes** objects. So, the **Figure** is the final graphic that may contain one or more **Axes**. The **Axes** represent an individual plot.

So, we can think of the **Figure** object as a box-like container containing one or more **Axes**. The **Axes** object contain smaller objects such as tick marks, lines, legends, title and text-boxes.

## **7.	Matplotlib API Overview**<a class="anchor" id="7"></a>
[Table of Contents](#0.1)

Matplotlib has two APIs to work with. A MATLAB-style state-based interface and a more powerful object-oriented (OO) interface. 
The former MATLAB-style state-based interface is called **pyplot interface** and the latter is called **Object-Oriented** interface.

There is a third interface also called **pylab** interface. It merges pyplot (for plotting) and NumPy (for mathematical functions) together in an environment closer to MATLAB. This is considered bad practice nowadays. So, the use of **pylab** is strongly discouraged and hence, I will not discuss it any further.

## **8. Pyplot API** <a class="anchor" id="8"></a>
[Table of Contents](#0.1)

**Matplotlib.pyplot** provides a MATLAB-style, procedural, state-machine interface to the underlying object-oriented library in Matplotlib. **Pyplot** is a collection of command style functions that make Matplotlib work like MATLAB. Each pyplot function makes some change to a figure - e.g., creates a figure, creates a plotting area in a figure etc. 

**Matplotlib.pyplot** is stateful because the underlying engine keeps track of the current figure and plotting area information and plotting functions change that information. To make it clearer, we did not use any object references during our plotting we just issued a pyplot command, and the changes appeared in the figure.

We can get a reference to the current figure and axes using the following commands-

`plt.gcf ( )`    *get current figure*

`plt.gca ( )`   *get current axes* 

**Matplotlib.pyplot** is a collection of commands and functions that make Matplotlib behave like MATLAB (for plotting). The MATLAB-style tools are contained in the pyplot (plt) interface. 

This is really helpful for interactive plotting, because we can issue a command and see the result immediately. But, it is not suitable for more complicated cases. For these cases, we have another interface called **Object-Oriented** interface, described later.
