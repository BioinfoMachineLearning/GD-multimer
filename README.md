# GD-multimer
Stochastic gradient descent method for reconstructing protein multimer structures from inter-chain contacts/distances



** Download GD-Multimer package (short path is recommended)**

```
git clone git@github.com:BioinfoMachineLearning/GD-multimer.git

(If fail, try username) git clone https://github.com/BioinfoMachineLearning/GD-multimer.git

cd GFOLD
```

** How to run the code:**

```
For dimers using contact:

python ./scripts/docking_new.py target_name first_chain second_chain res_file output_dir weight_file top_num

example:

python ./scripts/docking_new.py T0965A_T0965B GD_tools/pdb_homo/chains/T0965A.pdb GD_tools/pdb_homo/chains/T0965B.pdb ../output_distance/T0965A_T0965B_con.rr ./ ./talaris2013.wts all
```

```
For dimers using distance:

python ./scripts/docking_new_dist.py target_name first_chain second_chain res_file output_dir weight_file thre 

example:

python ./scripts/docking_new_dist.py T0965A_T0965B GD_tools/pdb_homo/chains/T0965A.pdb GD_tools/pdb_homo/chains/T0965B.pdb ../output_distance/T0965A_T0965B_dist.rr ./ ./talaris2013.wts 6
```

```
For multimers using contact:


python ./scripts/docking_gd_parallel_multi.py target_name num_of_chains first_chain second_chain third_chain ... nth_chain res_file output_dir weight_file top_num


example:

python ./scripts/docking_gd_parallel_multi.py T1034 4 /home/esdft/Downloads/pdbs/initial_start_multi/T1034A.pdb /home/esdft/Downloads/pdbs/initial_start_multi/T1034B.pdb /home/esdft/Downloads/pdbs/initial_start_multi/T1034C.pdb /home/esdft/Downloads/pdbs/initial_start_multi/T1034D.pdb /home/esdft/Downloads/output_distance/T1034o.rr /home/esdft/Downloads/pdbs/ ./talaris2013.wts all
```

```
For multimers using distance:


python ./scripts/docking_gd_parallel_multi_dist.py target_name num_of_chains first_chain second_chain third_chain ... nth_chain res_file output_dir weight_file thre


example:

python ./scripts/docking_gd_parallel_multi_dist.py T1034 4 /home/esdft/Downloads/pdbs/initial_start_multi/T1034A.pdb /home/esdft/Downloads/pdbs/initial_start_multi/T1034B.pdb /home/esdft/Downloads/pdbs/initial_start_multi/T1034C.pdb /home/esdft/Downloads/pdbs/initial_start_multi/T1034D.pdb /home/esdft/Downloads/output_distance/T1034o.rr /home/esdft/Downloads/pdbs/ ./talaris2013.wts 36
```

