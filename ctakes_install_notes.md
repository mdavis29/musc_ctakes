# CTAKES Instruction guide.
For a more detailed instruction guide, go to the official instruction guide at https://cwiki.apache.org/confluence/display/CTAKES/cTAKES+4.0+User+Install+Guide. This markdown will contain the steps for the Windows OS portion of the installation.

## Requirements
    + Request your [UMLS Licence](https://uts.nlm.nih.gov//license.html). This process can take several days.
    + Java Version 1.8+

## Installation Instructions (Windows OS):
These installation instructions are for Windows OS and were simply transcribed from the official instruction guide. For a more detailed account
of the instructions, or if you are using a linux OS, please use the guide in the link above. This guide also has example uses of ctakes at the bottom of the guide.

    * First make sure that java version 1.8+
        + C:\>java -version
        + java version "1.8.0_201" Java(TM) SE Runtime Environment ...
    * Download the User Installation package on the cTAKES [downloads page](http://ctakes.apache.org/downloads.html)
        + Unzip the files into the folder 'C:\apache-ctakes-4.0.0'. This will be your <cTAKES_HOME> directory
    * [Download the cTAKES resources](https://sourceforge.net/projects/ctakesresources/files/)
        + Unzip to temporary location (downloads will work)
    * Copy the contents of the temporary resources directory (and all sub-directories) to <cTAKES_HOME>/resources. There may be conflicts while doing this, we want to overwrite the cTAKES_HOME files with those in the resources downloads.
        + xcopy /s C:\temp\ctakes-resources-4.0-bin\resources C:\apache-ctakes-4.0.0\resources
    * Add UMLS access rights. At this step we will need to modify two files to include our UMLS username and password. The two files that need to be modified are <cTAKES_HOME>/bin/runctakesCVD.bat and <cTAKES_HOME>/bin/runctakesCPE.bat.
        + Use any text edit to modify <cTAKES_HOME>/bin/runctakesCVD.bat
            - Find the line that reads 'java -Dctakes.umlsuser=<YOUR_UMLS_ID_HERE> -Dctakes.umlspw=<YOUR_UMLS_PASSSWORD_HERE> -cp ...'
            - Modify that line to read 'java -Dctakes.umlsuser="myuser!!!!"  -Dctakes.umlspw="mypass!!!!"  -cp ...',
            - Notice everything from -cp ... should remain untouched
        + Perform this same procedure on <cTAKES_HOME>/bin/runctakesCPE.bat

    *Installation complete

