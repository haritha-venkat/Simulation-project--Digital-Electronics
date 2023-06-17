# TITTLE:
     DESIGN AND SIMULATE SR FF USING NAND GATES WITH NO CLOCK PULSE USING VERILOG.
# THEORY:
     1. An SR Flip Flop is short for Set-Reset Flip Flop. It has two inputs S(Set) and R(Reset) and two outputs Q(normal output) and Q'(inverted output).
     2. As we proceed, we will see how to write Verilog code for SR Flip Flop using different levels of abstraction.
     3. With the assistance of a logic diagram, we will be able to know the essential logic gates needed to build a circuit. Verilog provides us with gate primitives, which help us create a circuit by connecting basic logic gates. Gate level modeling enables us to describe the circuit using these gate primitives.
    4. From the below circuit, it is clear we need to interconnect four NAND gates in a specific fashion to obtain an SR flip flop. Let’s see how we can do that using the gate-level modeling style.



# LOGIC DIAGRAM:

![image](https://github.com/haritha-venkat/Simulation-project--Digital-Electronics/assets/121285701/1713e481-3bee-46d0-966d-98095bca53f2)


# NETLIST DIAGRAM:

![image](https://github.com/haritha-venkat/Simulation-project--Digital-Electronics/assets/121285701/2bc16c4f-6623-44d1-be61-f917a268a123)

# TIMING DIAGRAM:

![image](https://github.com/haritha-venkat/Simulation-project--Digital-Electronics/assets/121285701/d2baa541-f933-4fcc-b0c3-0f0fab808a9e)


# PROGRAM:
developed by: harithashree.v
reg.no.: 212222230046
```python
    module srff_gate(q, qbar, s, r, clk);

input s,r,clk; 
output q, qbar;

wire nand1_out; // output of nand1 
wire nand2_out; // output of nand2 

nand (nand1_out,clk,s); 
nand (nand2_out,clk,r); 
nand (q,nand1_out,qbar);
nand (qbar,nand2_out,q);

endmodule
```
