# openuidataset

The goal of this project is to use automated GUI exploration and TESTAR tool for automatically extracting screenshots and JSON files that describe the widgets, their location on the screenshot, and other properties. This data will be then used for training machine learning algorithms to recognize widgets from the screenshots.



## Instructions for installing TESTAR tool and the required environment to run it on VirtualBox image having Windows 10.

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



## openuidataset upload instructions

In order to upload data to the openUiData set, you have to do a pull request with your new data in it. The new data has to conform to the folder structure of the existing data in the data set to preserve its integrity. The data format contains the screenshots and the JSON for each image. For each software version the folder should contain the <hash>.jpeg and <hash>.json files. The fiels should be named as the hash of the image file and the .JSON file should also have an identical name which relatest to the image which data the JSON file contains.

The folder structure is as follows:

./<operating system>/<software name>/<software version>/12hakfna12.jpeg
./<operating system>/<software name>/<software version>/12hakfna12.JSON

## Instructions for upload

1. Clone the OpenUiData project to your local environment

2. Create a new branch n the repo to use as the base for a pull request

3. Create the aforementioned folder path that matches the software that you ran in the repo. For example: Windows10/microsoftWord/1.2/

4. Under this folder copy the output scrnshots folder contents from Testar including the .jpeg and .hash files

5. Commit the nef files into the new branch and Push the changes to github

6. Create a new pull request with the name in the following format: "New data: <operating system>/<software name>/<software version>"
  
7.  Wait for your pull request to be approved or to be commented upon.
