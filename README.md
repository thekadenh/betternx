# betternx
A python package that makes NetworkX better

This package is full of simple improvements to NetworkX. I have included documentation here that hopefully makes everything easy to understand and implement for your own projects.

# Documentation

This next section is the documentation for the functions in my project. All of them can be found in FinalProject.ipynb or FinalProject.py.

## CCDF

def CCDF(G, gType='loglog', fmt = '', xlabel = 'Degree, k', ylabel = 'Pr(K>=k)', title = None, **kwargs):

G is the graph you give to the CCDF function (some networkx graph object).
gType can be one of four values: 'loglog' (both x and y axis are log scales), 'semilogx' (only x axis is log scale), 'semilogy' (only y axis is log scale), or 'linear' (neither axis is log scale). 
fmt is a string that formats your graph the way you want it really easily. More info can be found here: https://matplotlib.org/3.1.1/api/_as_gen/matplotlib.pyplot.plot.html
xlabel and ylabel are strings that alter the axis labels.
title is optionally a string that controls the title for the graph.
You can also pass in any other keyword arguments to the plt.plot() function. Here are some notable ones:
basex and basey control the bases of logarithmic axes.

## 


A huge thank you goes out to Dr. Aaron Clauset for making this project possible, and for providing ideas and some of the code for this project. 
