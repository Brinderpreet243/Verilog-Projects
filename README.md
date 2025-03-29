# Verilog-Projects
A collection of Verilog-based digital designs and simulations. Includes basic and advanced circuits such as a 4-bit ALU, Johnson counter, D flip-flop, and more. Implemented and tested using simulation tools like Icarus Verilog and Vivado.

## RISC-V Processor Schematic
The following schematic represents the architecture of our RISC-V processor design.
![Screenshot 2025-03-29 091358](https://github.com/user-attachments/assets/316daecd-4144-4e23-a685-dcedabe53e0c)
## **🖥️ RISC-V Processor Simulation Waveform**

## Individual Components

### 1. Instruction Fetch Unit (IFU)
![Screenshot 2025-03-29 091853](https://github.com/user-attachments/assets/01448556-92de-4331-a8ba-be3c2fe7c580)


### 2. Control Unit
![Screenshot 2025-03-29 091912](https://github.com/user-attachments/assets/826e3ce1-ace7-41f7-9667-63e82bc47475)


### 3. Datapath Unit

![Screenshot 2025-03-29 091942](https://github.com/user-attachments/assets/d7fe546a-13c0-45fd-a48a-9a5b2cf0bd53)

Below is the simulation waveform for the **RISC-V processor**, showing instruction execution, register file updates, ALU operations, and control signals.
![Screenshot 2025-03-29 091455](https://github.com/user-attachments/assets/fe6f9845-6ad7-4617-a573-813423a27957)
## Individual Components



## **📌 4-Bit Johnson Counter using D Flip-Flops**  

### **📜 Schematic**  
The following schematic represents the architecture of the **4-bit Johnson Counter** using **D Flip-Flops**.  

  ![Screenshot 2025-03-29 090300](https://github.com/user-attachments/assets/4e71a191-8663-4e1f-a93c-6089ba502e2d)

  ## **📊 Waveform Simulation Results**  

Below are the simulation results of the **4-bit Johnson Counter**.

### **1️⃣ Johnson Counter Output**

![Screenshot 2025-03-29 090348](https://github.com/user-attachments/assets/3b11210b-b981-4d26-b62d-db64cfca5c33)

### **💻 Verilog Code**  
The Verilog implementation of the **4-bit Johnson Counter**.  

```verilog
module johnson_counter(clk, reset, Q3, Q2, Q1, Q0);
    input clk, reset;
    output Q3, Q2, Q1, Q0;  

   Dflip_flop Dflip_flop_3(
                         .D(~Q0),  
                         .clk(clk),
                         .reset(reset),
                         .q(Q3)
   );
   Dflip_flop Dflip_flop_2(
                          .D(Q3),
                          .clk(clk),
                          .reset(reset),
                          .q(Q2)
   );
   Dflip_flop Dflip_flop_1(  
                          .D(Q2),
                          .clk(clk),
                          .reset(reset),
                          .q(Q1)    
   );
   Dflip_flop Dflip_flop_0(  
                          .D(Q1),  
                          .clk(clk),
                          .reset(reset),
                          .q(Q0)
   );

endmodule


## ALU Simulation Result
![ALU Simulation](alu_sim1.png)

## ALU Verilog Code
![ALU Code](alu_sim2.png)
