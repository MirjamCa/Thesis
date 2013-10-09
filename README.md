# The Dynamic Patient Admission Scheduling with Operating Room Constraints, Flexible Horizon, and Patient Delays

This repository contains instances, generator, solutions, and validator for the problem defined in the paper *The Dynamic Patient Admission Scheduling with Operating Room Constraints, Flexible Horizon, and Patient Delays. Submitted for publication* by Sara Ceschia and Andrea Schaerf, currently under revision. 

This is a temporary version of the file, meant for reviewers' use only.

## Generator

The generator OrPasXMLGenerator.php generates instances of any size by running:
    $ ./OrPasXMLGenerator.php <departments> <rooms> <features> <patients> <days> <or_rooms>

The files `HC_classes.php` and `HC_Data.php` are necessary to run the generator.

##Instances

Generated instances are stored in folder Instances. They are split into 5 families with the following main features:

| Family |	Rooms	| Departments	| Patients	| Days |
| :------| ------:  | ------:| ------:| ------:| 
| Short1 |	25 |	2 |	440 	| 14 |
| Short2 |	50 |	4 |	640 	| 14 |
| Short3 |	75 |	6 |	1400 	| 14 |
| Long1 |	25 |	2 |	748 	| 28 |
| Long2 |	50 |	4 |	1088 	| 28 |
| Long3 |	75 |	6 |	1564 	| 28 |

## Results

### Results of the dynamic (regular) solver in its best configuration

| Instance | Avg     | Dev     | Med     | Best    |
| :------  | ------: | ------: | ------: | ------: |
| or-dept2_short00 | 63470.0  | 552.2 | 63371 | 62503 | 
| or-dept2_short01 | 95704.0  | 630.3 | 95707 | 94660 |
| or-dept2_short02 | 55218.1  | 287.4 | 55218 | 54380 |
| or-dept2_short03 | 74491.7  | 633.6 | 74701 | 73291 |
| or-dept2_short04 | 72711.1  | 487.6 | 72761 | 71686 |
| or-dept4_short00 | 126509.9 |1019.1    | 126451 | 124079 |
| or-dept4_short01 | 141902.3 | 704.6 | 141944 | 140520 |
| or-dept4_short02 | 113988.2 | 640.7  | 114074 | 112753  |
| or-dept4_short03 | 121690.3 |  1167.4  | 121789 | 119716 |
| or-dept4_short04 | 115830.4 | 630.6 | 115770 | 114523 |
| or-dept6_short00 | 177036.0 |1151.8  | 177484 | 175023 |
| or-dept6_short01 | 206101.  | 995.4 | 205915 | 203881  |
| or-dept6_short02 | 198402.2 | 847.7 | 198415 | 196399 |
| or-dept6_short03 | 164359.9 | 615.5 | 164524 | 163123 |
| or-dept6_short04 | 189961.6 |1326.8  | 190262 | 187470 |
| or-dept2_mid00 | 223533.5 | 1474.2  | 223648 | 220142 |
| or-dept2_mid01 | 130859.2 |  999.7 | 131114 | 128336 |
| or-dept2_mid02 | 143599.7 |  608.5 | 143614 | 142669 |
| or-dept2_mid03 | 229154.8 | 1410.7  | 229164 | 226574 |
| or-dept2_mid04 | 173789.2 |  902.5 | 173808 | 172134 |
| or-dept4_mid00 | 262804.9 | 1655.1  | 262897 | 259207 |
| or-dept4_mid01 | 213411.6 |  988.8 | 213677 | 210752 |
| or-dept4_mid02 | 247530.3 |  976.9 | 247347 | 245905 |
| or-dept4_mid03 | 300126.5 | 1393.8  | 299752 | 297032 |
| or-dept4_mid04 | 254056.7 | 1223.3   | 253800 | 252312  |
| or-dept6_mid00 | 474375.4 | 2313.2  | 474189 | 468343 |
| or-dept6_mid01 | 390235.4 | 2306.2  | 390042 | 386435 |
| or-dept6_mid02 | 411998.8 | 1558.9  | 412192 | 408250 |
| or-dept6_mid03 | 409788.8 | 2972.7  | 410153 | 399418 |
| or-dept6_mid04 | 449136.2 | 2290.0  | 449158 | 445640 |


### Results of the static (crystal-ball) solver in its best configuration

| Instance | Avg     | Dev     | Med     | Best    |
| :------  | ------: | ------: | ------: | ------: |
| or-dept2_short00 | 63170.7  | 457.3 | 63519 | 62662 |
| or-dept2_short01 | 95553.2  | 582.0 | 95906 | 94928 |
| or-dept2_short02 | 53463.2  | 137.2 | 53466 | 53289 |
| or-dept2_short03 | 75823.5  | 622.1 | 76207 | 74757 |
| or-dept2_short04 | 71260.2  | 257.6 | 71466 | 70981 |
| or-dept4_short00 | 127363.2 |1322.9   | 127981 | 125170 |
| or-dept4_short01 | 141656.7 | 308.5 | 141795 | 141187 |
| or-dept4_short02 | 111109.5 | 503.1 | 111203 | 110387 |
| or-dept4_short03 | 120126.2 | 621.9 | 120236 | 119210 |
| or-dept4_short04 | 115144.2 | 863.9 | 115655 | 113691 |
| or-dept6_short00 | 182120.7 |1027.1  | 182462 | 180656 |
| or-dept6_short01 | 213307   | 485.6 | 213692 | 212505 |
| or-dept6_short02 | 196149.7 | 258.2 | 196151 | 195935 |
| or-dept6_short03 | 161543.2 | 721.4 | 161565 | 160803 |
| or-dept6_short04 | 199718.2 | 449.4 | 199874 | 199084 |
| or-dept2_mid00 | 231435.2 | 1323.6  | 232555 | 229783 |
| or-dept2_mid01 | 131134.7 |  369.7 | 131309 | 130642 |
| or-dept2_mid02 | 143572.2 |  498.5 | 143804 | 142853 |
| or-dept2_mid03 | 249361.2 | 1358.0  | 250067 | 247433 |
| or-dept2_mid04 | 180366.2 | 2125.5  | 181911 | 177544 |
| or-dept4_mid00 | 281974.0   | 1163.2   | 281869 | 280473 |
| or-dept4_mid01 | 217340.0   | 1360.3   | 218116 | 215100 |
| or-dept4_mid02 | 258798.2 |  896.7 | 259039 | 257416 |
| or-dept4_mid03 | 318309.5 | 2304.4  | 320063 | 315077 |
| or-dept4_mid04 | 265911.7 | 1106.2  | 266694 | 264033 |
| or-dept6_mid00 | 521038.7 | 2986.7  | 521715 | 516683 |
| or-dept6_mid01 | 427752.5 | 1929.7   | 428286 | 425093 |
| or-dept6_mid02 | 435685.7 | 1266.4  | 436549 | 433549 |
| or-dept6_mid03 | 473744.5 | 3335.7  | 473472 | 469470 |
| or-dept6_mid04 | 477363.5 | 1830.3  | 478106 | 474887 |


## Solutions

Best solutions are available from the folders DynamicSolutions and StaticSolutions for the two solvers, respectively.

## Validator

The solution validator is available as a C++ source file in `or_pas_validator`. The compilation command is provided on top of the file as a comment. The library libxml++ needs to be installed.