MATLAB code to perform a wide analysis on network topological measures.

### REFERENCE ###

"Can local-community-paradigm and epitopological learning enhance
our understanding of how local brain connectivity is able to process,
learn and memorize chronic pain?"
Vaibhav Narula et al., Applied Network Science, 2017, 2:28
https://doi.org/10.1007/s41109-017-0048-x

for each measure, the support function reports the original source,
please cite the proper reference if you use it.


### INPUT ###
x - adjacency matrix of the network
    the network is considered unweighted, undirected and zero-diagonal

request - cell array with the names of the required measures among:
          N - nodes
          E - edges
          avgdeg - average degree
          density - density
          clustering - clustering coefficient
          char_path - characteristic path length
          efficiency_glob - global efficiency
          efficiency_loc - local efficiency
          closeness - closeness centrality
          EBC - edge betweenness centrality
          BC - node betweenness centrality
          radiality - radiality
          LCPcorr - Local Community Paradigm correlation
          assortativity - assortativity
          modularity - modularity
          struct_cons - structural consistency
          powerlaw_p - pvalue for power-lawness
          powerlaw_gamma - fitted exponent of power-law degree distribution
          smallworld_omega - small worldness omega
          smallworld_sigma - small worldness sigma
          smallworld_omega_eff - small worldness omega (efficiency)
          smallworld_sigma_eff - small worldness sigma (efficiency)
          richclub_p - pvalue for rich-clubness

          NB: if the input is not provided or an empty array [] is given,
              all the measures are computed

par - 1 or 0 to indicate whether the function should use parallel computation or not.
      if the input is not provided, parallel computation is used
			  
iters - structure containing for the stochastic measures
        the number of iterations.
        if the input is not provided, the default values are:
        iters.modularity = 100;
        iters.struct_cons = 100;
        iters.powerlaw_p = 1000;
        iters.smallworld = 10;
        iters.richclub_p = 1000;

### OUTPUT ###
tm - structure array containing the topological measures.
     the names of the structure fields correspond to the names
     in the input variable "request"
     NB: if a single measure is requested, the output is directly its value
	 
	 
### CONTACT ###

For any problem, please contact:
Alessandro Muscoloni: alessandro.muscoloni@gmail.com
Carlo Vittorio Cannistraci: kalokagathos.agon@gmail.com