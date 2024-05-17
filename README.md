## Repository for Python codes, input, and output data sets for the research: Store Fulfillment with Autonomoys Mobile Robots and In-Store Customers


### Variant Change
In the "Dynamic Algorithm with Simulation.ipynb" file, to change the variant of the algorithm go to the comment: "Deciding the variation of the heuristic"

For changing the sequencing variant we need to set "1" and "0" for the following two variables depending on which one we want to use and which one to turn of. "1" represents turning on and "0" represents turning off. In the uploaded version it is currently set as follows:

tsp_based_seq = 0

buypicks_based_seq = 1

To decide on the abandon policy of whether we want to use it or not, we simply set "0" for turning off abandon policy and "1" for turning on for the variable "use_abandon". In the uploaded version it is currently set as follows:

use_abandon = 1


To change the number of allowed reallocations in the heuristic, we set "0" for multiple reallocations and "1" for single reallocation for the variable "limit_to_one_insertion". And if we want to set the algorithm to no reallocations at all then we simply set the "no_update" variable to "1" which overrides anything set in the variable "limit_to_one_insertion", otherwise to activate the "limit_to_one_insertion" variable we set the "no_update" variable to "0". In the uploaded version it is currently set as follows:

limit_to_one_insertion = 1

no_update = 0  

### Number of resources
To change the number of resources in the algorithm we need to look for the following codes right under the "Input Parameters -----> Need to Change for Design of Experiment" comment. In the uploaded version it is currently set as follows:
num_cob = 6      
num_ded = 1          

### Large files
Large data files are stored in the following folders: 

Inputs: https://1drv.ms/f/s!Agvu7NOb4BgTg8Q8taV9Mf8FG0ZRFQ?e=0EIDET

Outputs: 
