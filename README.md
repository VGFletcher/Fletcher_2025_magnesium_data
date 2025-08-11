# Data Related to publication: Optimal Autonomous MLIP Dataset Building
### UK Ministry of Defence © Crown Owned Copyright 2025/AWE

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
           `-- These are all the .traj, .energies, .inp, .out, and .rdb.extxyz files from the X GPa NS run
               If the .rdb.extxyz is not present, the final configuration was used and will be in the concatenated version
               For confirmation, please consult our publication
</pre>
