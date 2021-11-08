# OSeMOSYS-SE
This repository contains an OSeMOSYS model of Sweden

To edit and generate a new model, follow these steps:
1. Activate 'myenv' or 'OSeMOSYS' (depending on where otoole is installed).
2. Change directory to this current folder of the README file. Work from here.
3. Edit the input data .csv files.
4. Convert the data files to one single .txt file using this line:
otoole convert datapackage datafile datapackage.json osemosys-se_ref.txt
5. Make a results folder:
mkdir results
6. Generate the results:
glpsol -m osemosys_fast.txt -d osemosys-se_ref.txt
7. If you want to visualize the RES, run this command:
otoole viz res datapackage.json res.png
