README

In the instructions below Project refers to a series of similar experiments that are aimed to answer the same scientific question. Dataset refers to an individual experiment and it's corresponding image acquisition session. 
Typically one Project will contain multiple Datasets while a Dataset will contain multiple images.

Instructions for PC
===================

Before starting:
----------------

1. On your <NETWORK DRIVE> user folder, create a folder called "Your_Name_OMERO_IMPORT_FOLDER". 
2. In this folder keep a copy of the "Pazour_OMERO_import_template_wMacros_v05.xlsm" that was provided to you.

When you are ready to import your first images to OMERO:
--------------------------------------------------------

1. In "Your_Name_OMERO_IMPORT_FOLDER" create the following import structure:

"Project-Name_CONTAINER" (folder)
	-"Project-Name" (folder)
		- "Dataset_Name" (folder)

    * Use a unique name or identifier for "Project-Name" and make sure to use the same name for <Project_ID>
    * Use a unique name or identifier for "Dataset_Name" and make sure to use the same name for <Dataset_ID>

2. When you are done with image acquisition, move the image files to be imported in the corresponding Dataset-folder as follows:

"Project-Name_CONTAINER" (folder)
	-"Project-Name" (folder)
		- "Dataset_Name" (folder)
			- "Image-file_1"
			- "Image-file_2"
			- "Image-file_3"
            - ...

3. Launch "Pazour_OMERO_import_template_wMacros_v05.xlsm".
4. Follow the instructions that you will find in each of the three metadata tabs.
5. Move "Project_Name.csv" to the "Project_Name_CONTAINER" folder.
6. Move "Dataset_Name.csv" to the "Project_Name" folder.
7. Move "Image-List.csv" to the "Dataset_Name" folder.
7. Copy and Paste the "Pazour_OMERO_import_template_wMacros_v05.xlsm" to the "Project_Name" folder and rename it "Project_Name-Dataset_Name.xlsm".
8. As a result the structure in your file system should look as follows:

"Project-Name_CONTAINER" (folder)
	- Project-Name.csv
	-"Project-Name" (folder)
		- Project_Name-Dataset_Name.xlsm
		- Dataset_Name.csv
		- "Dataset_Name" (folder)
			- Image-List.csv
			- "Image-file_1"
			- "Image-file_2"
			- "Image-file_3"
            - ...

9. The next day inspect OMERO to verify the import has occurred as expected.


--------

Project TAB
-----------
1. Fill in relevant metadata in the Value column (leave empty the ones you do not need)
2. In "Your_Name_OMERO_IMPORT_FOLDER" create reate a Project_CONTAINER  folder entitled "Project_Name_CONTAINER"
3. In the Project_CONTAINER  folder create a Project folder entitled "Project_Name"
4. <Save filled data to CSV> using "Project_Name" as file name
4.1 If you are on MacOS, you will be prompted to "Save As...". Please make sure to choose the "Comma Separated Values (.csv)" option
5. Move Project_Name.csv  to Project_CONTAINER folder 
6. Jump to  allowable value lists to view and edit


Dataset TAB
-----------
1. Fill in relevant metadata in the Value column (leave empty the ones you do not need)
2. <Save filled data to CSV> using "Dataset_Name" as file name
2.1 If you are on MacOS, you will be prompted to "Save As...". Please make sure to choose the "Comma Separated Values (.csv)" option
3. Move Dataset_Name.csv  to Project_Name folder 
4. In the Project_Name  folder create a Dataset folder entitled "Dataset_Name"
5. Jump to  allowable value lists to view and edit


Image-List TAB
-----------
1. Fill in relevant metadata in the Value column (leave empty the ones you do not need)
2. <Save filled data to CSV> using "Image-List" as file name
2.1 If you are on MacOS, you will be prompted to "Save As...". Please make sure to choose the "Comma Separated Values (.csv)" option
3. Move Image-List.csv  to Dataset_Name folder 
4. Move to Dataset_Name folder all images described in the limage list 
5. If available move to Dataset_Name folder the Microscope.JSON file and the Settings.JSON files created with Micro-Meta App
6. Jump to  allowable value lists to view and edit


