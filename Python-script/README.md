# Installing Python and How to use the script

# For Windows users:

* Check the python version of you computer: “python –V”
    
* If not installed:

      * Go to https://www.python.org/downloads.
      
      * Choose your version. For new users who do not have python installed on their PCs, use the latest one.
      	At the time of producing this document, the latest version was 3.6.5.
      
      * Download the installer file. While installing, remember to select “Add python 3.6 to your path”.
      
      * Now check the python version again to confirm python installation on your pc.
     
* The python scrip uses the libraries: “openpyxl, texttable, warnings, telnetlib, socket, sys”.

* The first two libraries are third party libraries available under: https://pypi.org. 
  To install them, open your command promt and run the commands below:
    * “pip install openpyxl” 
    * “pip install texttable”
    
* If it does not work, try updating “pip” by running: “python -m pip install --upgrade pip” command and then try the commands above.

# For Mac Users: 

* MacBook already has python 2.7.10 installed. To download third-party library, it requires “pip”.

* If "pip" is not installed:

     * Install by running:
     	* "sudo easy_install pip" or, "sudo python -m ensurepip”. 
	 	This will install pip version 6.1.1

     * Then run: pip install {{name of the package}} 
     
	        * "pip install openpyxl"
	        * "pip install texttable" 

* If it does not work, then:

     * Download https://bootstrap.pypa.io/get-pip.py, by running:
     
 	        * "curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py”
		
     * And run:	
	        
		* "python get-pip.py –user” : This will install pip version 10.0.1. 
		* "python -m pip install openpyxl --user"
		* "python -m pip install texttable –user”


* Or, if “Homebrew” is not installed,

	* First install it by running: 
		ruby -e "$(curl –fsSL  https://raw.githubusercontent.com/Homebrew/install/master/install)"
	 
	* Then run:
	
		* "brew install python2" : This will upgrade the python for 2.7.15.
		* "sudo easy_install pip" : This will install pip version 10.0.1. 
		* "pip install openpyxl".
		* "pip install texttable". 
           
 # Run the script
 
 * Now, your python script is ready to go. Open command prompt/terminal. Run the script like this:
      * python <name of the script .py> <name of the excel file .xlsx>. As an example:
      
      	<I>	python TDM_to_IP_On_Ramp_ASIC.py InputDataTest.xlsx	<I>


![Alt text](../images/exampleScreenShot.png?raw=true "ExampleScreenShot")
 
  
