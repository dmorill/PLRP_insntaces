# PLRP_insntaces
 
Here we present a set of instances for the periodic location-routing problem (PLRP) applied to waste collection. New dimensions were added to Cordeau's cases: customer nodes were assigned a "customer type" to introduce the disparity in load size and collection frequency between each customer's recycling needs, which affects the route sequence.

This folder is divided into three sections: "Instances_Originals" contains the 42 unaltered instances from Cordeau, categorized in "Small Size" for each including no more than 60 customer nodes, "Medium Size" for up to 144 customer nodes, and "Large Size" for up to 417 customer nodes. The section "Instances_Modified" is distributed exactly as the previous, with the difference that each instance was modified with the new dimensions, tailored for recycling conditions. Finally, "Instances_12C" includes 13 randomly modified instances, but cropped in node size for up to 12 customer nodes each, in the hope of a better comparison of the Mixed Integer Linear Programming model (exact method) and the novel VNS Metaheuristic when the problem is simplified and easier to run.

Basic Instance Structure

#Customers	#Depots		Depots_Cap.		Vehicles_Cap.
#Type of waste

Node_ID	X_coord	Y_coord	Demand	Frequency  Depot_Bool Waste_ID_assigned / Days
0	1	1	-1	1	   1	      1 2 3		/ 1 5


When the Depot_Bool = 1, it represents that the node is a Depot, and the assigned demand & frequency are -1
