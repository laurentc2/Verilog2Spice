# Verilog to Spice in Python

Simple strutured VERILOG netlist to SPICE netlist translator

usage example assuming : 
 * the verilog netlist to be converted called : final.v  
 * a reference stdcells library spice netlist : stdcells.cdl
 * a reference memory block spice netlist : memory.cdl
 * the target spice netlist output : final.sp  

python verilog2spice.py -spice stdcells.cdl -spice memory.cdl -verilog final.v -output final.sp -pos_pwr VDD -neg_pwr VSS -delimiter

 * under Linux, the command python can be avoided or replaced by python3
 * if pos_pwr and neg_pwr are not specified, they are by default VDD and VSS
 * if -delimiter is used, the busses delimiter will be changed from [:] in the verilog netlist to <:> in the spice netlist
