The benchmarks and optimized results for the work: 

**Three-Input Gates for Logic Synthesis** by  D. S. Marakkalage, E. Testa, H. Riener, A. Mishchenko, M. Soeken and G. De Micheli, in IEEE Transactions on Computer-Aided Design of Integrated Circuits and Systems. (https://ieeexplore.ieee.org/document/9233431)


The verilog files in `benchmarks/` are the original benchmarks used in the experiments (https://github.com/lsils/benchmarks) and the `.blif` files in `optimized/` are the optimized dot-inverter graphs. 

To reproduce results in Table VII of the paper, please use the branch `tig` in the repository https://github.com/mdsudara/mockturtle.

After cloning and checking out the branch, execute the following commands to build the experiment. 

```
mkdir build 
cd build
cmake -DMOCKTURTLE_EXPERIMENTS=ON ..
make tig
```


Then, to reproduce the results for **And-Inverter Graphs (AIG)**, use the following command.

```
./experiments/tig aig benchmark_name.v output_name.blif
```

Similarly, to reproduce results for **Majority-Inverter Graphs (MIG)**, use
```
./experiments/tig mig benchmark_name.v output_name.blif
```

To reproduce results for **Dot-Inverter Graphs (DIG)**, use
```
./experiments/tig dig benchmark_name.v output_name.blif
```

