# convert-windowsimage
Scripts for converting Windows images (ISO,WIM) to VHD/VHDX.

This is a fork of Convert-WindowsImage from Nerdhile: https://github.com/nerdile/convert-windowsimage
Which itself was originally forked from the TechNet ScriptCenter: https://gallery.technet.microsoft.com/scriptcenter/Convert-WindowsImageps1-0fe23a8f

This code is owned by Microsoft and licensed under the MS-LPL.  See the LICENSE file for more information.

## Changes from the Nerdhile version:
- .Net classes have changed vastly since originally written. The corrected/update names of the classes and packages needed to be located, then code changed to download them as needed.

## See Article:
https://azuretothemax.net/2025/05/20/building-golden-images-for-hyper-v-lab-testing/

## For Use Instructions:
Look at the code itself. There are many comments from the original authors explaining how to use the script.

To give one example, this is a modern way to use the tool...
```
.\Convert-WindowsImage.ps1 -SourcePath "C:\Hyper-V\WIM\Win_11_24H2.wim" -VHDPath "C:\Hyper-V\Templates\Win11_24H2_test.vhdx" -Edition 1 -VHDFormat VHDX -VHDPartitionStyle GPT -VHDType dynamic -SizeBytes  128GB
```
