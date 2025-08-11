# Data Related to publication: <br> Optimal Autonomous MLIP Dataset Building
### UK Ministry of Defence © Crown Owned Copyright 2025/AWE

This repository contains all the data produced for the publication titled "Optimal Autonomous MLIP Dataset Building" (DOI when available)  
Contact: vincent.fletcher@warwick.ac.uk

The primary contents are:
1. The nested sampling runs done at each cycle, with the interatomic potential used during that cycle
2. The database constructed through our procedure for that cycle (the `.rdb.extxyz` file)
3. The DFT data, evaluating the `.rdb.extxyz` file
4. The `.edb.extxyz` files which is the `.rdb.extxyz` file with the DFT data
    
In addition to this data I have also provided the DFT benchmark data shown in the paper.

If you would like to use our data for training, the `.edb.extxyz` files contain the nested sampling configurations and the DFT evaluated properties under the keywords: `dft_energy` (eV), `dft_virial` (eV/ $Å^3$), `dft_forces` (eV/ $Å$). The stresses are also saved under the keyword `dft_stress` (GPa) but the units are GPa.

Note: Due to the quantity of nested sampling data collected only a small portion of the configurations are provided in the `.traj.extxyz` files but the full files can be requested from the author.

Files are structured as follows:  
<pre>
|-- cycle_n
    |-- castep_files: The extracted results are in the Evaluated DataBase file (.edb.extxyz)
    |   |- .param files used to evaluate the X GPa database(s)
    |   `- X GPa
    |      `-- These are all the .castep, and .cell, files from evaluating the concatenated .rdb.extxyz file
    |  
    `-- nested_sampling
        |- The interatomic potential used for the sampling
        |- The concatenated (but unevaluated) databases in the Raw DataBase file (.rdb.extxyz)
        `- X GPa
           `-- These are the .traj, .energies, .inp, .out, and .rdb.extxyz files from the X GPa NS run
               If the .rdb.extxyz is not present, the final configuration was used and will be in the concatenated version
               For confirmation of the data used, please consult our publication
</pre>
