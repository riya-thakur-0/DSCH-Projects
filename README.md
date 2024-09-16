# DSCH-Projects
In this there are some performed dsch projects

Verilog Code for 4:1 mux:

// DSCH 3.5
// 17-09-2024 00:05:40
// example

module example ( A, B, S, R, Q, P, out1); input A, B, S, R, Q, P;
output outl;
wire w5, w6, w7, w8, w9, w10,wll,w12;
wire;
not #(1) inv_1(w5,A);
not #(1) inv_2 (w6, B);
or #(2) or2_3 (out1, w7, w8); 
or #(2) or2_4(w8, w9, w10); 
or #(2) or2_5 (w7, wll,w12); 
and # (2) and3_6 (w11, P,w5, w6); 
and # (2) and3_7 (w12,Q,w5,B);
and # (2) and3_8 (w9, R, A, w6);
and # (2) and3_9 (w10,S,A,B);
endmodule

// Simulation parameters in Verilog Format
always
#200 A=~A;
#400 B=~B;
#800 S=~S;
#1600 R=~R;
#3200 Q=~Q;
#6400 P=~P;

// Simulation parameters
// A CLK 1 1
// B CLK 2 2
// S CLK 4 4
// R CLK 8 8
// Q CLK 16 16
// P CLK 32 32
