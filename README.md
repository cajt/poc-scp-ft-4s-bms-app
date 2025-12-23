# poc-scp-ft-4s-bms-app
Proof of concept fault tolerant SCP with a BMS Application.

# Fault Tolerance Concept

Fail-safe in a 2-out-of-2 configuration. BMS is implemented in split parts. Both halves have to error 
free for the battery/BMS to operate nominally. 
If an error is detected the whole system stops and the electronics disconnects the battery cells from 
the rest of the system, protecting the cells from leaving their safe operating area in the presence 
of BMS error.

In the error-free operation simple cell safety limits are checked: Cell voltages, Current and Temperatures.

# Simplifications for the PoC

- Power supply: Non-redundant and externally supplied.
- Wake-up and power boot-strap: None, the system can't wake up without an external power source. 
- Only 4 cells. (But it should moderately obvious how to extend this by a few more cells. Conceptually this is also compatible with stacking the BMS for higher cells counts.)

# Motivation

Li based cells have some nasty failure-modes, and require some attention to avoid entering dangerous operating areas. This is a good application for fault-tolerance and fail-safe circuitry


# Disclaimer, Liabilities and Guarantees

No Guarantees. The risk is yours alone. If you don't understand this method, mitigation and risks involved you should really not touch this. 
Published in the hope that it might be inspiration or food for thought, not a ready to use module or product.  
