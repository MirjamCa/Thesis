# The Dynamic Patient Admission Scheduling with Operating Room Constraints, Flexible Horizon, and Patient Delays

This repository contains instances, generator, solutions, and validator for the problem defined in the paper *The Dynamic Patient Admission Scheduling with Operating Room Constraints, Flexible Horizon, and Patient Delays. Submitted for publication* by Sara Ceschia and Andrea Schaerf, currently under revision. 

## Generator

The generator OrPasXMLGenerator.php generates instances of any size by running:

	$ ./OrPasXMLGenerator.php <departments> <rooms> <features> <patients> <days> <or_rooms>

The files `HC_classes.php` and `HC_Data.php` are necessary to run the generator.

##Instances

Generated instances are stored in folder `Instances`. Each instance is validated again the `OrPasInstance.xsd` XML schema. 
They are split into 6 families with the following main features:

| Family | Rooms | Departiments | Operating Rooms | Specialisms | Treatments | Patients | Days
| :------| ------:| ------:| ------:| ------:| ------:| ------:| 
| Short1 | 25 | 2 | 2 | 9 | 15 | 391-439 | 14
| Short2 | 50 | 4 | 4 | 18 | 25 | 574-644 | 14
| Short3 | 75 | 6 | 5 | 23 | 35 | 821-925 | 14
| Long1 | 25 | 2 | 2 | 9 | 15 | 693-762 | 28
| Long2 | 50 | 4 | 4 | 18 | 25 | 1089-1169 | 28
| Long3 | 75 | 6 | 5 | 23 | 35 | 1488-1602 | 28

## Results

### Results of the dynamic (regular) solver in its best parameter configuration


| Instance | Avg     | Dev     | Med     | Best    
| :--------  | ---:|  ---:|  ---:|  ----: | 
| or_pas_dept2_short00 | 84743.13 | 434.93 | 84697	| 83750	
| or_pas_dept2_short01 | 76421.17 | 672.82 | 76413	| 75185	
| or_pas_dept2_short02 | 85644.67  | 451.86 | 85614	| 84743	
| or_pas_dept2_short03 | 85578.17  | 694.82 | 85734	| 84041	
| or_pas_dept2_short04 | 80065.43  |  542.35 | 80110 | 78979	
| or_pas_dept4_short00 | 162431.33  | 736.19 | 162445 | 160908	
| or_pas_dept4_short01 | 131807.20 | 829.73 | 131874 | 130417	
| or_pas_dept4_short02 | 130755.77 | 794.25 | 130598 | 129365	
| or_pas_dept4_short03 | 132371.20 | 1066.50 | 132471 | 130044	
| or_pas_dept4_short04 | 118835.60 | 809.96 | 118975 | 116781	
| or_pas_dept6_short00 | 211538.80 | 1186.79 | 211655 | 209289	
| or_pas_dept6_short01 | 231615.80 | 1395.02 | 232004 | 229258	
| or_pas_dept6_short02 | 227800.30 | 1732.82 | 227598 | 223933	
| or_pas_dept6_short03 | 189188.20 | 1033.87 | 189196 | 186491	
| or_pas_dept6_short04 | 211278.67 | 906.75 | 211612 | 208996	
| or_pas_dept2_long00 | 175608.50 | 1778.51 | 175958 | 172398	
| or_pas_dept2_long01 | 185516.37 | 1351.85 | 185570 | 183134	
| or_pas_dept2_long02 | 162102.70 | 1237.24 | 162007 | 159459	
| or_pas_dept2_long03 | 141373.47 | 1221.96 | 141613 | 139098	
| or_pas_dept2_long04 | 181073.43 | 861.35 | 181237 | 179153	
| or_pas_dept4_long00 | 229260.90 | 1605.24 | 229615 | 225738	
| or_pas_dept4_long01 | 256394.27 | 1802.09 | 256616 | 253143	
| or_pas_dept4_long02 | 283645.53 | 1917.39 | 283635 | 279354	
| or_pas_dept4_long03 | 390986.00 | 2366.04 | 391276 | 385649	
| or_pas_dept4_long04 | 303337.23 | 2711.70 | 303173 | 298670	
| or_pas_dept6_long00 | 521369.50 | 4009.90 | 521248 | 514810	
| or_pas_dept6_long01 | 551616.71 | 5718.19 | 553391 | 541950	
| or_pas_dept6_long02 | 455385.47 | 3625.85 | 455504 | 447008	
| or_pas_dept6_long03 | 470707.24 | 2898.82 | 470723 | 465630	
| or_pas_dept6_long04 | 340457.53 | 2140.44 | 340116 | 336353	


### Results of the static (crystal-ball) solver in its best parameter configuration

| Instance | Avg     | Dev     | Med     | Best    
| :--------  | ---:|  ---:|  ---:|  ----: | 
| or_pas_dept2_short00 | 86969.97 | 371.27	 | 86947 | 86415
| or_pas_dept2_short01 | 76610.17 | 726.20	 | 76878 | 75165
| or_pas_dept2_short02 | 85724.30 | 241.64	 | 85723 | 85092
| or_pas_dept2_short03 | 84421.83 | 401.52	 | 84450 | 83689
| or_pas_dept2_short04 | 80257.10 | 265.52	 | 80306 | 79739
| or_pas_dept4_short00 | 162274.10 | 632.75 | 162383 | 161023
| or_pas_dept4_short01 | 128330.63 | 689.96 | 128340 | 126844
| or_pas_dept4_short02 | 132575.83 | 723.07 | 132687 | 131031
| or_pas_dept4_short03 | 131414.23 | 624.61 | 131541 | 130236
| or_pas_dept4_short04 | 118685.07 | 465.52 | 118776 | 117767
| or_pas_dept6_short00 | 209519.80 | 520.71 | 209520 | 208408
| or_pas_dept6_short01 | 229400.30 | 848.78 | 229318 | 228126
| or_pas_dept6_short02 | 219940.23 | 1091.77 | 220135 | 217641
| or_pas_dept6_short03 | 187157.43 | 786.63 | 187121 | 185379
| or_pas_dept6_short04 | 213279.27 | 648.66 | 213187 | 211735
| or_pas_dept2_long00 | 166753.43 | 927.98 | 166935 | 165043
| or_pas_dept2_long01 | 184473.77 | 878.19 | 184515 | 182704
| or_pas_dept2_long02 | 154540.87 | 862.10 | 154476 | 152948
| or_pas_dept2_long03 | 139857.17 | 912.99 | 139735 | 138120
| or_pas_dept2_long04 | 182489.73 | 380.84 | 182475 | 181918
| or_pas_dept4_long00 | 226703.83 | 1029.53 | 226981 | 224403
| or_pas_dept4_long01 | 255247.37 | 1063.52 | 255400 | 253048
| or_pas_dept4_long02 | 277658.17 | 762.86 | 277606 | 275849
| or_pas_dept4_long03 | 375461.07 | 1732.87 | 375615 | 371729
| or_pas_dept4_long04 | 289296.03 | 1586.19 | 289651 | 286014
| or_pas_dept6_long00 | 495248.93 | 1405.87 | 495013 | 492893
| or_pas_dept6_long01 | 534763.67 | 1652.99 | 535394 | 532499
| or_pas_dept6_long02 | 430484.60 | 1696.84 | 430695 | 426626
| or_pas_dept6_long03 | 462507.63 | 1599.33 | 462225 | 459018
| or_pas_dept6_long04 | 340267.20 | 1138.79 | 340102 | 337876


## Solutions

Best solutions are available in the folders `DynamicSolutions` and `StaticSolutions` for the two solvers, respectively.
Each solution is validated against the `OrPasSolution.xsd` XML schema.

## Validator

The solution validator is available as the C++ source file `or_pas_validator.cc`. The compilation command is provided on top of the file as a comment. The library `libxml++` needs to be installed.