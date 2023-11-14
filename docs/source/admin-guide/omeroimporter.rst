========================
Setting Up OMEROImporter
========================

1. Download the OmeroImporter_TestPack
======================================

To the machine you want to upload through.

Make sure it’s in the home directory.

2. Place the different features in the correct directories
==========================================================

``OMERO_IMPORT_FOLDER`` and ``OMERO_IMPORT_DONE`` should be located in
the places where the users will be uploading from in the future.

``OmeroImporter.cfg`` should go in a folder called ``OmeroImporter`` in
the user’s home directory — make sure it has the correct paths,
passwords, etc.

You can unzip the ``W-IDM_OmeroDataImporter`` inside that folder as
well.

3. Test the setup manually
==========================

Note: make sure Java is installed on the machine (it has to be a newer
version of Java i.e. 

Since it’s a jar executable, you can run the file manually with the -cfg
option to test the sample upload with the new setup using this command:

``java -jar [PATH-TO-JAR] -cfg``

4. Edit the paths in the config file
====================================

To the folders that the users will actually use now that the test is
done.

5. Clean up
===========
