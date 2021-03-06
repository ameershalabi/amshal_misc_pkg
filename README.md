# amshal_misc
This repository is intended to be a collection of components written in the VHDL language. All the files included are written and verified by Ameer Shalabi. The functionality and behavioral of the components were verified using ModelSim and synthesized using Synopsys Design Vision. 

* `amshal_misc_pkg` A package with useful and necessary functions for the above components
* The repository contains the following generic components:

| Component 	| file name 	| usage 		|
| ------------- | ------------- |------------- 	|
| A decoder  	| `DEC_generic`  	| A generic combinational decoder |
| A multiplexer  | `MUX_generic`  | A generic mux with array of inputs|
| An Incrementor | `incr_generic` | A generic combinational Incrementor |
| A Decrementor | `decr_generic` | A generic combinational Decrementor |
| An enabler| `en_and` | Attaches tri-state buffers to the input to control output |
| An edge detecion circuit| `edgeDet_generic.vhdl` | Generates three vectors indicating signal event, rising edge, and falling edge at each bit of input vector |

* The repository contains the following generic registers:

| Component 	| file name 	| usage 		|
| ------------- | ------------- |------------- 	|
| Lenear-FeedBack Shift Regsiters | `RAND_LFSR_generic`, `LFSR_generic` | Generates an LFSR using a vector imported from the amshal_misc package file|
| A counter | `counter_generic` | A generic counter circuit|
| Rigesters| `REG_generic`, `REG_generic_f_rst` | Generic register circuits |
| Shift Registers | `SISO_rl_shift_reg_generic` , `SIPO_rl_shift_reg_generi`, `SI_SPO_rl_shift_reg_generic` | Generic shift registers with multi directional control|
| First-In First-Out register | `FIFO_generic` |  A generic FIFO |

* The repository contains the following non-generic Encoders:

| Component 	| file name 	| usage 		|
| ------------- | ------------- |------------- 	|
| A 32x5 OR-Gate encoder| `OR_ARRAY_32x5_Enc` | Fully parallel 32x5 encoder |
| A 16x4 OR-Gate encoder | `OR_ARRAY_16x4_Enc` | Fully parallel 16x4 encoder |
| A 8x3 OR-Gate encoder | `OR_ARRAY_8x3_Enc` | Fully parallel 8x3 encoder |

* Other generic components
1. A dual read RAM (`RAM_dual_R`)
2. A single read RAM (`RAM_single_R`)
* Other non-generic
1. A 4x4 parallel multiplier (`multiplier_4x4`):
* the multiplier is devided into three components that must be compiled before the multiplier can be used `multiplier_4x4_lv_last`, `multiplier_4x4_lv_mid`, and `multiplier_4x4_lv_up`. `multiplier_4x4_lv_up` represents the lowest level of multiplication and produces the LSB of the product. `multiplier_4x4_lv_last` is the last level of the multiplication and produces the most significant half of the product. The rest of the product is generated by the middle level `multiplier_4x4_lv_mid`. A generic version of the multiplier is in the works.

## TO DO LIST:
1. A generic multiplier (ongoing, 22/02/2021)
3. A generic Logic-Gate Binary Tree generator (On the list!)
