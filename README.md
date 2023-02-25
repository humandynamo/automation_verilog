# automation_verilog
Question: 
Design an Automatic Library Evaluation Framework that automates the synthesis flow of the Xilinx Vivado Tool.
The Script Should Take Verilog Files as Input and Synthesis All of them.
The area, power, and delay report should be generated for all the designs.
All the results should be combined in the form of a CSV file 
The components of the area, delay, and power should be as shown in the CSV file attached.

Answer:
To design an Automatic Library Evaluation Framework that automates the synthesis and implementation flow of the Xilinx Vivado Tool, we are following the steps below:

1. Install Xilinx Vivado Tool and ensure it is added to the system path.
2. Write a script that takes Verilog files as input and generates a project for each of them using the Vivado Tool's batch mode. The script should also set
   the appropriate synthesis and optimization settings and run the synthesis process.
3. Once the synthesis process is complete, the script should extract the area, power, and delay data from the synthesis report files for each design.
4. Using python script we are running the vivado operations in batch mode and we combine the area, power, and delay data into a single CSV file.
5. The script should provide the option to run the synthesis process in parallel for multiple designs to improve efficiency.

Initially we have created a module folder which contains all verilog (.v) files which follows the nomenclature of top_module name. 
In the script folder which contains two text files (.txt) which functionals on the adding the verilog files (.v) over the vivado (which opens in batch mode) and another text file for running synthesis and implementation of the added files.

During automation:

The script assumes the Vivado Tool is installed and added to the system path. It also assumes the existence of two TCL scripts, create_project.tcl (craete project and 
adds verilog project files to the created project) and run_synth.tcl, which are used to create a new Vivado project and run synthesis for a given project, respectively. 

We are automating the entire synthesis and implementaion process using python script (Automation.ipynb).
Also we are storing each individual project processed data into the folder files.
For creating nested folders we are using the python script.
Finally we are extracting important data from the synthesised files and storing data in the csv file (results.csv).


Theory reference:
Automation in Verilog refers to the use of scripts or tools to automate the design, verification, and testing of Verilog hardware designs. Verilog is a popular hardware description language used for designing digital circuits and systems. It is essential to ensure that the design is correct and meets the required specifications. Automating the design process using scripts or tools can help save time and reduce errors.

Design Automation: This involves automating the design process, which includes tasks like creating modules, instantiating modules, connecting modules, and generating 
a netlist. Tools like HDL Designer, Verilog-XL, and Synopsys Design Compiler can help automate the design process. Here we have used python script running tcl files over vivado in batch mode.

Scripts are used to perform a sequence of tasks, such as compiling Verilog files, running simulations, and generating reports. Makefiles are used to automate the build
process, where a set of rules are defined to generate the output files based on the input files.

Automation in Verilog can help increase productivity, reduce errors, and improve the quality of the design. It is an essential skill for Verilog engineers, and mastering it can make you a more efficient and effective designer.
