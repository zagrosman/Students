## Visualizing protein-protein interactions using UCSF Chimera
1. Go to UCSF Chimera homepage and download the favorable source codes (https://www.cgl.ucsf.edu/chimera/download.html)
2. Install UCSF Chimera.
3. Extract the pdb complex from Gromacs trajectory files.
4. Open the complex in UCSF Chimera. 
5. Go to Chimera [presets] menu and select [Publication 5 flat ribbon) to change the represention as shown below:

![image](https://user-images.githubusercontent.com/17006122/205597944-9615818d-d71b-4fda-88d9-83f62bc81cba.png)

6. Go to [Tools] menu and then select [surface/binding analysis] and then select [FindHBond] as the below:

![image](https://user-images.githubusercontent.com/17006122/205598349-c10ad17a-d2e9-4ace-9592-49ffcb7ecf92.png)

Next, you should see the following window after selecting the above-mentioned options:

![image](https://user-images.githubusercontent.com/17006122/205599479-27df3b20-551b-447c-925c-10c607844e0b.png)

Then subject the following settings to the appeared window:
a. Select **both** in **Find these bonds box**

b. Select **Relax Hbonds constrains** and change its value to 0.5 angstroms to 30 degree as depicted in the previous image. 

c. Select **Color H-bonds not meeting precise criteria differently:** You can click on the colorful box to select another color for showing H-bonds:

![image](https://user-images.githubusercontent.com/17006122/205600854-a61a0f28-ed91-41f1-bd7e-9d365cf2893b.png)

