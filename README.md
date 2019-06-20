# openuidataset

The goal of this project is to use automated GUI exploration and TESTAR tool for automatically extracting screenshots and JSON files that describe the widgets, their location on the screenshot, and other properties. This data will be then used for training machine learning algorithms to recognize widgets from the screenshots.

Instructions for installing TESTAR tool and the required environment to run it on VirtualBox image having Windows 10.

1. Install VirtualBox, the latest version should be fine.

2. Download OVA image (virtual machine with Win10) from https://testar.org/download/

3. Run VirtualBox.

4. Select File/Import Appliance and select the OVA image file you just downloaded.

5. Give a name for the virtual machine (VM).

6. Enable "Reinitialize the MAC address..." and select Import.

7. Select the VM you just installed from the VirtualBox and start it (allow access in your firewall if asked).

8. Username for Win10 is "testar" and password is "testar".

9. The OVA image has an older version of TESTAR, it is in C:\testar\

10. Start a web browser in the VM and download the latest TESTAR binaries from https://testar.org/download/

11. Extract the TESTAR binaries .zip file for example into C:\testar\ (you can remove the old bin and lib folders).

12. Start testar.bat from the bin folder of the new TESTAR binaries (if "Windows protected your PC" prevents testar.bat from starting, click "more" and "Run anyway" to allow TESTAR to run).

13. In TESTAR user interface, first select the protocol you want to use, for example desktop_generic_json for random action selection and generating JSON files.

14. Start TESTAR in Generate mode (many-colored arrows).

15. If you want to stop TESTAR execution, press SHIFT + Arrow Down.

16. Check the results from output folder. The JSON files will be generated into output/scrshots/sequence folder.
