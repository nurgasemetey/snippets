###  Disable CPU Power Saving Management in BIOS 


[Disable CPU Power Saving Management in BIOS - Thomas-Krenn-Wiki](https://www.thomas-krenn.com/en/wiki/Disable_CPU_Power_Saving_Management_in_BIOS "Disable CPU Power Saving Management in BIOS - Thomas-Krenn-Wiki")


 

```shell
Disable CPU Power Management
During the boot process, press the Delete or Entf button (depending on your keyboard layout) to enter the BIOS
Switch to -> Advanced CPU Configuration -> Advanced Power Management Configuration
Change Power Technology to Custom and Energy Efficient Turbo to Disable.
Switch to CPU P State Control, deactivate EIST (P-States) and Turbo Mode.
Then switch to CPU C State Control, change Package C State Limit to C0/C1 state and deactivate CPU C3 Report, CPU C6 Report and Enhanced Halt State (C1E).

```
