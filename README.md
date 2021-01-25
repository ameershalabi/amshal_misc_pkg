# amshal_misc
This repository is intended to a collection of generic (except the encoder) components written in the VHDL language. All the files included are written and verified by Ameer Shalabi. The functionality of the components were tested using ModelSim and synthasized using Synopsys Design Vision. 
The repository contains the following generic components:
* A decoder (DEC_generic)
* A multiplexer (MUX_generic)
* An Incrementor (incr_generic)
* A Decrementor (decr_generic)
* An enabler (en_and)
The repository contains the following generic registers:
* Lenear-FeedBack Shift Regsiter (LFSR_RAND, LFSR_generic)
* A counter (counter_generic)
* A register with forced re-set (triggered) (REG_generic_f_rst)
* A register (triggered) (REG_generic)
* Direction-controlled Serial-In Serial-Out shift register (SISO_rl_shift_reg_generic)
* Direction-controlled Serial-In Parallel-Out shift register (SIPO_rl_shift_reg_generic)
* Direction-controlled Serial-In Serial- /Parallel-Out register (SI_SPO_rl_shift_reg_generic)
* First-In First-Out register (FIFO_generic)
Other generic components
* A dual read RAM(RAM_dual_R)
Other non-generic
* A package with useful and necessary functions for the above components (amshal_misc_pkg)
* A 32x5 OR-Gate encoder (OR_ARRAY_32x5_Enc)
* A 16x4 OR-Gate encoder (OR_ARRAY_16x4_Enc)
* A 8x3 OR-Gate encoder (OR_ARRAY_8x3_Enc)

