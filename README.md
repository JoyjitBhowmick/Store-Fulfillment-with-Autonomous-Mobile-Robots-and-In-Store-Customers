## Repository for Python codes, input, and output data sets for the research: Store Fulfillment with Autonomoys Mobile Robots and In-Store Customers

### Input Data
The set of input data sets for the "Dynamic Algorithm with Simulation" file are as follows:
1. Instacart_Aisle_Buy
2. Distance_Matrix
3. Arrivals100, Arrivals125, Arrivals150, and Arrivals 175 (these can be found in the master branch of this repository)
4. incoming_order_arranged


### Dynamic Algorithm with Simulation
To change the variant of the algorithm (total 12 variants possible) and to set the number of resource pool the following steps are followed:

#### Variant Change
In the "Dynamic Algorithm with Simulation.ipynb" file, to change the variant of the algorithm go to the comment: "Deciding the variation of the heuristic"

For changing the sequencing variant we need to set "1" and "0" for the following two variables depending on which one we want to use and which one to turn of. "1" represents turning on and "0" represents turning off. In the uploaded version it is currently set as follows:

tsp_based_seq = 0

buypicks_based_seq = 1

To decide on the abandon policy of whether we want to use it or not, we simply set "0" for turning off abandon policy and "1" for turning on for the variable "use_abandon". In the uploaded version it is currently set as follows:

use_abandon = 1


To change the number of allowed reallocations in the heuristic, we set "0" for multiple reallocations and "1" for single reallocation for the variable "limit_to_one_insertion". And if we want to set the algorithm to no reallocations at all then we simply set the "no_update" variable to "1" which overrides anything set in the variable "limit_to_one_insertion", otherwise to activate the "limit_to_one_insertion" variable we set the "no_update" variable to "0". In the uploaded version it is currently set as follows:

limit_to_one_insertion = 1

no_update = 0  

#### Number of resources
To change the number of resources in the algorithm we need to look for the following codes right under the "Input Parameters -----> Need to Change for Design of Experiment" comment. In the uploaded version it is currently set as follows:
num_cob = 6      
num_ded = 1        

### Output Files

The following are the files that is the result of merging multiple output files:
1. C3D1 - 12 Variants Merged Results: This file provides outputs after running 12 variants of the algorithm with 3 cobots and 1 dedicated picker. There are some columns that have been created after all the outputs were merged such as: scenario, numPicked, totalPicked, variantName, and custArrInstance.

2. Benchmark Merged: This file provides outputs after running 4 benchmark resource pools (C0D1, C0D2, C0D3, and C0D4) and merging them.
3. C1D1 - RAS.xlsx: This file is generated after setting num_cob=1 and num_ded=1 and changing the variant to RAS
4. C2D1 - RAS.xlsx: This file is generated after setting num_cob=2 and num_ded=1 and changing the variant to RAS
5. C4D1 - RAS.xlsx: This file is generated after setting num_cob=4 and num_ded=1 and changing the variant to RAS 
