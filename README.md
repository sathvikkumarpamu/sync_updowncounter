# 3-Bit Synchronous Up/Down Counter

## Aim
To design and verify a 3-bit synchronous up/down counter using IC 7473 and JK flip-flops.

## Apparatus Required
- Electronic circuit design kit  
- IC 7473 (Dual JK Flip-Flop)  
- Patch cords  

## Theory
A 3-bit synchronous up/down counter is a sequential logic circuit that counts in binary sequence from 0 to 7 and can be configured to count **up** or **down** depending on the control input.  

All flip-flops are clocked **simultaneously** (synchronous operation), which avoids delay problems associated with asynchronous counters. The IC 7473 provides two JK flip-flops; an additional JK flip-flop is used to achieve the 3-bit design.

### Key Concepts
- **Synchronous Operation:** All flip-flops share the same clock signal, ensuring simultaneous state transition.  
- **Up/Down Control:** A mode control signal (M) determines direction:
  - M = 1 → Count up  
  - M = 0 → Count down  
- **Clock and Clear:** The clock signal drives all flip-flops, and the clear input resets the counter to zero.

## Procedure
1. **Determine Flip-Flops:**  
   A 3-bit counter requires three JK flip-flops. The states range from 000 to 111—all valid with no don’t-care conditions.

2. **Mode Control Signal (M):**  
   Used to switch between up and down counting modes.

3. **Draw State Diagrams:**  
   Represent transitions for both up and down modes showing the binary count sequence.

4. **Select Flip-Flop Type and Derive Excitation Table:**  
   Choose JK flip-flops and derive the excitation table for state transitions.

5. **Derive Minimal Expressions:**  
   Using K-Maps, obtain simplified expressions:
   - J1 = 1, K1 = 1  
   - Expressions are derived for J2, K2, J3, and K3 based on excitation conditions.

6. **Design Logic Diagram:**  
   Implement the logical connections using AND/OR gates as per minimal expressions.

## Result
The 3-bit synchronous up/down counter was successfully designed and verified. The truth table and logic operation were found to be correct as per theoretical expectations.

## Notes
- The counter design can be extended for more bits by cascading additional JK flip-flops.
- The synchronous nature ensures minimal propagation delay as all flip-flops are triggered by the same clock pulse.


### Example Output States (for M=1, Up Counting)
| Decimal | Binary Output (Q3 Q2 Q1) |
|----------|--------------------------|
| 0 | 000 |
| 1 | 001 |
| 2 | 010 |
| 3 | 011 |
| 4 | 100 |
| 5 | 101 |
| 6 | 110 |
| 7 | 111 |

### Example Output States (for M=0, Down Counting)
| Decimal | Binary Output (Q3 Q2 Q1) |
|----------|--------------------------|
| 7 | 111 |
| 6 | 110 |
| 5 | 101 |
| 4 | 100 |
| 3 | 011 |
| 2 | 010 |
| 1 | 001 |
| 0 | 000 |
