# RV32I ALU REQUIREMENTS QUESTIONNAIRE

**Instructions:** Please fill out all sections below with your specific requirements. Replace the blank lines (___) with your values and check the appropriate boxes [x]. This questionnaire will guide the complete ALU implementation from RTL to verification.

## 1. Functional Requirements

**Primary Function:** RV32I Arithmetic Logic Unit (ALU)

**Detailed Description:** 
The ALU will implement all arithmetic and logical operations required by the RISC-V RV32I base integer instruction set. This includes arithmetic operations (ADD, SUB), logical operations (AND, OR, XOR), shift operations (SLL, SRL, SRA), and comparison operations (SLT, SLTU).

**Key Features Required:**
- [x] Arithmetic Operations: ADD, SUB
- [x] Logical Operations: AND, OR, XOR
- [x] Shift Operations: SLL (Shift Left Logical), SRL (Shift Right Logical), SRA (Shift Right Arithmetic)
- [x] Comparison Operations: SLT (Set Less Than), SLTU (Set Less Than Unsigned)
- [ ] Additional Feature A: _______________
- [ ] Additional Feature B: _______________
- [ ] Additional Feature C: _______________

**RV32I ALU Operations to Support:**
- [x] ADD/ADDI - Addition
- [x] SUB - Subtraction  
- [x] AND/ANDI - Bitwise AND
- [x] OR/ORI - Bitwise OR
- [x] XOR/XORI - Bitwise XOR
- [x] SLL/SLLI - Shift Left Logical
- [x] SRL/SRLI - Shift Right Logical
- [x] SRA/SRAI - Shift Right Arithmetic
- [x] SLT/SLTI - Set Less Than (signed)
- [x] SLTU/SLTIU - Set Less Than Unsigned
- [ ] LUI - Load Upper Immediate (if needed): _______________
- [ ] AUIPC - Add Upper Immediate to PC (if needed): _______________

## 2. Technical Specifications

**Target Technology:** 
- [ ] FPGA 
- [x] ASIC (Sky130)
- [ ] Generic

**Clock Frequency:** _____ MHz (Please specify target frequency)

**Interface Type:** 
- [ ] AXI 
- [ ] APB 
- [ ] AHB 
- [x] Custom: Simple combinational interface with control signals

**Data Width:** 32 bits (RV32I standard)

**ALU Control Signal Width:** _____ bits (Please specify how many bits for ALU operation selection)

**Pipeline Requirements:**
- [x] Combinational (single cycle)
- [ ] Pipelined (specify stages): _______________

## 3. Interface Specifications

**Input Ports Required:**
- [x] operand_a[31:0] - First operand
- [x] operand_b[31:0] - Second operand  
- [x] alu_op[N:0] - ALU operation select (specify N: _____)
- [ ] Additional inputs: _______________

**Output Ports Required:**
- [x] result[31:0] - ALU result
- [x] zero_flag - Result is zero
- [ ] Additional flags needed:
  - [ ] carry_flag - Carry out
  - [ ] overflow_flag - Signed overflow
  - [ ] negative_flag - Result is negative
  - [ ] Other: _______________

**Clock/Reset Requirements:**
- [ ] Synchronous (clocked) design
- [x] Combinational (no clock required)
- [ ] Reset required: _______________

## 4. Performance Requirements

**Critical Path Target:** _____ ns (Please specify maximum combinational delay)

**Area Constraints:** 
- [ ] Minimize area
- [x] Balanced area/performance
- [ ] Performance priority
- [ ] Specific area target: _____ μm²

**Power Constraints:**
- [x] Standard power optimization
- [ ] Low power priority
- [ ] Specific power target: _____ mW

## 5. Verification Requirements

**Coverage Target:** _____% (Recommended: 95%+)

**Test Scenarios Required:**
- [x] Directed tests for each operation
- [x] Random instruction testing
- [x] Corner cases (overflow, underflow, zero operands)
- [x] All combinations of operand values
- [ ] Additional scenarios: _______________

**Verification Methodology:**
- [x] cocotb/pyuvm testbench
- [ ] SystemVerilog UVM
- [ ] Simple Verilog testbench

## 6. Implementation Strategy

**Number of Development Sprints:** _____ (Recommended: 2-3)

**Sprint Breakdown Preference:**
- Sprint 1: Basic arithmetic and logical operations (ADD, SUB, AND, OR, XOR)
- Sprint 2: Shift operations and comparisons (SLL, SRL, SRA, SLT, SLTU)
- Sprint 3: Optimization and full verification (if needed)

**Priority Ranking (1=highest, 3=lowest):**
___ Performance (Speed/Timing)
___ Area (Silicon area)
___ Power (Energy consumption)
___ Features (Operation completeness)

## 7. Integration Requirements

**CPU Integration:**
- [x] Standalone ALU module
- [ ] Integrated with CPU datapath
- [ ] Part of execution unit

**Interface Protocol:**
- [x] Simple combinational interface
- [ ] Handshake protocol required
- [ ] Pipeline interface required

**Testing Integration:**
- [x] Standalone ALU testing
- [ ] Integration with CPU model
- [ ] System-level testing

## 8. Documentation Requirements

**Documentation Needed:**
- [x] ALU operation encoding table
- [x] Interface specification
- [x] Timing characteristics
- [x] Integration guide
- [x] Verification report
- [ ] Additional docs: _______________

## 9. Special Requirements

**Synthesis Constraints:**
- [ ] Specific synthesis tool requirements: _______________
- [x] Open-source tool compatibility (Yosys)
- [ ] Timing constraints: _______________

**Physical Implementation:**
- [ ] Floorplan requirements: _______________
- [ ] Pin placement constraints: _______________
- [x] Standard cell library: Sky130

**Additional Notes:**
_______________________________________________________________________________
_______________________________________________________________________________
_______________________________________________________________________________

---

**COMPLETION CHECKLIST:**
- [ ] All functional requirements specified
- [ ] Technical specifications filled
- [ ] Interface requirements defined
- [ ] Performance targets set
- [ ] Verification strategy chosen
- [ ] Implementation plan agreed
- [ ] Integration requirements clear
- [ ] Documentation scope defined

**Please save this file and notify me once you have completed filling out all the requirements. I will then proceed with the complete ALU implementation following the agile sprint methodology.**