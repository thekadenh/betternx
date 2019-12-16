# betternx
A python package that makes NetworkX better

This package is full of simple improvements to NetworkX. I have included documentation here that hopefully makes everything easy to understand and implement for your own projects.

# Documentation

This next section is the documentation for the functions in my project. All of them can be found in FinalProject.ipynb or FinalProject.py.

## CCDF

`def CCDF(G, gType='loglog', fmt = '', xlabel = 'Degree, k', ylabel = 'Pr(K>=k)', title = None, **kwargs):`

`G` is the graph you give to the CCDF function (some networkx graph object).

`gType` can be one of four values: `'loglog'` (both x and y axis are log scales), `'semilogx'` (only x axis is log scale), `'semilogy'` (only y axis is log scale), or `'linear'` (neither axis is log scale). 

`fmt` is a string that formats your graph the way you want it really easily. More info can be found here: https://matplotlib.org/3.1.1/api/_as_gen/matplotlib.pyplot.plot.html

`xlabel` and `ylabel` are strings that alter the axis labels.

`title` is optionally a string that controls the title for the graph.

You can also pass in any other keyword arguments to the plt.plot() function. Here are some notable ones:

`basex` and `basey` control the bases of logarithmic axes.

#### This function doesn't return anything. It outputs a plot.

## Feedback loop count

`def fbl_count(G):`

`G` is the graph over which you want to count the number of feedback loops.

#### This function returns the number of feedback loops in G.

## Feed-forward loop count

`def ffl_count(G):`

`G` is the graph over which you want to count the number of feed-forward loops.

#### This function returns the number of feed-forward loops in G.

## Are nodes connected

`def nodes_connected(G, u, v):`

`G` is the graph which contains `u` and `v`

`u` is the name of a node in `G`.

`v` is the name of a node in `G`.

#### This function returns True if an edge exists from u to v, and False otherwise.

## Motif counting function

`def motif_count_3d(G, motif, rtype = 'list'):`

`G` is the graph over which you want to count the motifs.

`motif` is a graph with 3 nodes depicting a motif.

`rtype` can be `'list'`, which makes the function return a list of all triplets of nodes for which the motif exists. If `rtype` is anything other than `'list'`, the function will return an integer count of how many motifs there are. This does not account for subgraph isomorphisms. Caution: this algorithm is very slow and takes a long time to run.

#### This function returns a list of all triplets of nodes for which the motif exists, or an integer count of how many motifs there are in G (depending on return type specified).

## drawGz

`def drawGz(G,z, colors=None, nsize = 600, flabel = True, orderthresh = 50, orderthreshsize = 100, width = 2, **kwargs):`

`G` is the graph to draw.

`z` is the partition vector of G. For example, if node 0 in G was in category 3, and node 1 was in category 1, and node 2 was in category 5, z = [3, 1, 5]. 

`colors` is an optional array of color values that you want your partitions to be.

`flabel` is a value that determines whether or not the nodes are labeled. Can be True or False.

`orderthresh` is the threshold over which `flabel` = False by default and the node size changes.

`orderthreshsize` is the size that nodes change to once they reach a certain threshold.

`width` is the line width of edges. 

You can also pass in any other keyword arguments to nx.draw_networkx(). 

#### This function outputs a plot and does not return anything.

## DCSBM

`def DCSBM(G, reps = 20, groups = 2, maxphase = 30, output = 'all'):`

## Mean Degree

`def mean_degree(G, out = True):`

## Plague Simulator

`def Plague(G = None, Gtype = 'erdos', erdosval = 0.15, node_num = 50, mode = 'Game', ethics = 'Good', difficulty = 'Brutal', starttype = 'random', starters = None, numstarters = 4, vaccines = 'on', quarantines = 'on', antivax = 0.1, vaxcost = 100, startermoney = 500, allowance = 200, quarantinecost = 300, beta = 0.6, gamma = 0.3, curechance = 0.3, icost = 50, dcost = 50, ccost = 300, zcost = 400, betainc = 0.02, gammadec = 0.02, campchance = 0.1): `


A huge thank you goes out to Dr. Aaron Clauset for making this project possible, and for providing ideas and some of the code for this project. 
