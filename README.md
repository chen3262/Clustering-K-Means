# Clustering-K-Means
Clustering protein conformations using different RMSD inputs
<img src ="https://github.com/chen3262/Plot_Sec_Struc/blob/master/sec_struct_horizontal.png" width="1300">

```Plot_sec_struct.py``` is Python script to process and plot the secondary strcutures of a protein, which requires inputs files from VMD Timeline > Cal. Sec. Struc ( [tutorial](https://www.ks.uiuc.edu/Training/Tutorials/science/timeline/tutorial_timeline-html/)).

## Requirements
python modules: ```numpy```, ```pandas```, ```matplotlib```, ```seaborn```

To check if you have these modules installed, you can either do
```bash
conda list | grep "module_name"
pip list | grep "module_name"
```
If nothing is shown, you will need to install the module using either of the following commands
```bash
conda install module_name
pip install module_name
```
## Preparation Steps
Step 1: Obtain a *.tml output from VMD Timeline > Cal. Sec. Struc.

Step 2: provide the path of the .tml file, output folder path, and adjust the dimension of the picture in line 2-6 of the scripts.
```ruby
  2 file = '/path/to/the/timeline.tml' # path of the output from VMD Timeline
  3 DIR = '/path/to/the/output/folder/' # path of the folder to store the pidctures
  4 num_res = 42 # Number of residues of your protein
  5 dim_fig1 = [30, 4] # wiidth and height of the horizontal heatmap
  6 dim_fig2 = [10, 25] # wiidth and height of the vertical heatmap
```

Step 3:
```bash
python Plot_Sec_Struct.py
```
## Download and Testing
- Download:
```bash
git clone https://github.com/chen3262/Plot_Sec_Struc.git
```
- Use the provided ```timeline.tml``` for a test
- If run properly, you will get two pictures, ```sec_struct_horizontal.pdf``` and ```sec_struct_vertical.pdf```
- Sample output of ```sec_struct_horizontal.pdf```, where the populations of different secondary structures for each residues are represented in grey scales.
<img src ="https://github.com/chen3262/Plot_Sec_Struc/blob/master/sec_struct_horizontal.png" width="1000">

- Sample output of ```sec_struct_vertical.pdf```, which is annotated with numerical values of the secondary structure population.
<img src ="https://github.com/chen3262/Plot_Sec_Struc/blob/master/sec_struct_vertical.png" width="500">


## License

Copyright (C) 2019 Si-Han Chen chen.3262@osu.edu
