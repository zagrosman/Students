# How to run ADTvina?

![image](https://user-images.githubusercontent.com/17006122/219967848-58850fc7-9d56-475a-a2fd-366ba0a09cb1.png)


To run AutoDock Vina for docking, you can follow these steps:

1. Install AutoDock Vina on your computer. You can download the installer from the AutoDock Vina website and follow the instructions provided to install it.

2. Prepare your input files. AutoDock Vina uses two input files: a protein structure file in PDBQT format and a ligand structure file in PDBQT format. You can create these files using a molecular visualization software, such as PyMOL or Chimera, or using the AutoDockTools software.

3. Create a configuration file. AutoDock Vina uses a configuration file to specify the docking parameters, such as the grid box size and the number of docking runs. You can create a configuration file using a text editor and save it in a file with a ".conf" extension.

4. Run AutoDock Vina. To do this, type "vina --config config_file" in the command prompt or terminal, where "config_file" is the name of your configuration file. This will start the docking process.

5. Wait for the docking to finish. AutoDock Vina will perform multiple docking runs and output the results in a file with a ".dlg" extension. Depending on the size and complexity of the ligand and protein, this step can take some time.

6. Analyze the docking results. Once the docking is complete, you can analyze the output file using a text editor or specialized software, such as PyMOL or Chimera.

**For example, to run AutoDock Vina with a configuration file named "myconfig.conf", you would type the following command:**
```
vina --config myconfig.conf
```

It's important to note that AutoDock Vina is a powerful software that requires a good understanding of molecular docking principles and parameters. It's recommended to read the documentation and experiment with different options to optimize the docking results for your specific use case.

👉🏻 [ADTvina main-page](https://vina.scripps.edu/)
