## Protein Ligand docking using Chimera software

![image](https://user-images.githubusercontent.com/17006122/207009540-cfa190b5-aab1-476f-b469-71c1d9184891.png)


**Requirements:**
1. Receptor file: in pdb format. 
2. Ligand file: in 3D sdf format. 
3. UCSF Chimera: latest vesrion. 
4. ChimeraX: an advanced rendering software to show protein ligand interactions. 
5. Protein Imager: An online web interface to illustrate 3D conformation of bio-macromolecules. 

**Traget receptor and ligand for this tutorial:**
1. Receptor: Human pancreatic alpha amylase: PDB id: 1HNY
2. Ligand: Quercetin


## Docking steps using UCSF Chimera
**Step 1**: Receptor preparation
1. Fetch or open the target pdb file. 

![image](https://user-images.githubusercontent.com/17006122/207010253-2bb1a78e-8260-470b-893a-bfc9c3bd36dc.png)

Now, you can see:

![image](https://user-images.githubusercontent.com/17006122/207010518-5532ff51-aa95-44ba-88cf-b2a55da5c2a4.png)

2.  Click on Tools> Structure Editing > Dock Prep as shown:

![image](https://user-images.githubusercontent.com/17006122/207011162-7c1292fc-31b0-4f66-bfca-a546bcf8b76c.png)
 
 Now you can see:
 
![image](https://user-images.githubusercontent.com/17006122/207011833-204fe198-73ce-4578-8247-386353d4245a.png)

 3.  Select  all  options  except  “**Delete non-complexed ions**” and click **OK** as shown above. 
 4.  In **Add hydrogens panel** tick all indicated options and then click on **OK** as shown below.
![image](https://user-images.githubusercontent.com/17006122/207012653-9cb2b2ad-4ee6-41ee-9367-36ffcf0ddebd.png)

 5. In **Assign charges for Dock Prep panel**, click on **OK**. The given options should be selected before running this step. 

![image](https://user-images.githubusercontent.com/17006122/207013336-032bdd02-be88-468b-8d1d-c110ad8f2df8.png)
 
 6. In **Specify net charges**, select the displayed options and then click on **OK**:

![image](https://user-images.githubusercontent.com/17006122/207013899-aaad3ee9-b51e-4b90-ab09-2fbf6ceeb821.png)

 7. In **Save menu**, select a name for prepared receptor and then click on **Save** to save your prepared receptor in [.mol2] format. 

![image](https://user-images.githubusercontent.com/17006122/207014655-8b250cd6-7850-4dfb-b761-1cf544aad2fc.png)


Now, close the Chimera interface and repeat the above mentioned steps for your ligand.


**Step 2**: Ligand preparation

1. Download or fetch the 3D conformation of your ligand from PubChem, Chemspider or other relevant chemical ligand databases. 
2. Open the ligand in Chimera and repeat the above mentioned options to prepare your ligand. 
3. After ligand preparation, save the ligand in mol2 formation in your workfolder path. So, follow the below steps to prepare your ligands:

**Steps:**
1. Download the 3D sdf conformation of your target ligand in PubChem database as shown. 

![image](https://user-images.githubusercontent.com/17006122/207018905-c6054cf0-eb8e-4535-81c6-18b0aa27e422.png)

2. Insert the downloaded file into your workfolder and change its name. 

![image](https://user-images.githubusercontent.com/17006122/207018835-e599b97e-07f5-48ca-a74c-bc0a48af3b37.png)

3. Open the file in Chimera as shown:

![image](https://user-images.githubusercontent.com/17006122/207019091-91b842d6-a3f2-49ac-9db8-b9f847091f7d.png)

4. Prepare the ligand using [Dock prep] options in tools menu and then save the ligand in mol2 format. 

![image](https://user-images.githubusercontent.com/17006122/207020235-aefbd1b8-a3d5-4eb6-8a88-91ef52dc9835.png)


## Docking
To dock ligand into target receptor, you should first install autodock vina, autodock and mgltools on your operating system. You can download the source files of these tools from developer websites. Chimera has its own interface docking options. Therefore, when the user run Chimera, he/she should orient the chimera to where the autodock vina installed on your system. You should specify its path and then run its docking interface. 

1. Open both ligand and receptor in mol2 format in Chimera. You formerly prepared these molecules using chimera docking preparation module. 

![image](https://user-images.githubusercontent.com/17006122/207021878-8ad8c8c4-5dc3-4b6d-8162-5567bc351773.png)

2. Open the chimera docking module:

![image](https://user-images.githubusercontent.com/17006122/207022120-35fb75b4-ed8b-46ab-841c-9c97a08c962b.png)

3. You should specify docking parameters in the appeared window on your Chimera visualization interface:

![image](https://user-images.githubusercontent.com/17006122/207022661-1c3e2ef9-1785-46eb-9a68-5e05c37d5711.png)

**First:** Open the autodock to set a grid box for your receptor.

![image](https://user-images.githubusercontent.com/17006122/207026413-32d9c7b9-6057-4d3e-9b21-203eed955da0.png)

**Second:** Set the grid box to where the protein active site is. You should read the receptor-related crystallography details to find the active site details. 

![image](https://user-images.githubusercontent.com/17006122/207028517-3316a589-450a-4ae1-b5bd-0b231bc5a069.png)

**Third:** When you prepared the grid box information, now the numerical values for grid box coordinations should add to Chimera grid box. 

![image](https://user-images.githubusercontent.com/17006122/207029762-87a195a1-099f-4e9a-88d8-1367aa0e9434.png)

Now close the ADT, and follow the rest of settings in Chimera. 

4. Using Chimera grid box options, you can resize the coordination of your docking box. To do this, you can change numerical value in each xyz boxes. Please note that you can set up the grid box using box ADT or chimera alone. 

![image](https://user-images.githubusercontent.com/17006122/207031088-e854731a-e8ce-4041-b3a4-88e78fbd6647.png)

5. Assign receptor and ligand molecules to their own boxes:

![image](https://user-images.githubusercontent.com/17006122/207032018-cb5af1d2-935e-47cc-b0b0-bffda330a806.png)

6. Set receptor options to [true]



