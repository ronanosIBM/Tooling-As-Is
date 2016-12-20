Pre-requisites:
- Pluglet support must be enabled in IDA (may not be by default)

To enable pluglet support in IDA, open IBM Installation Manager, and select Modify Packages. Modify the IDA installation to include pluglet support
- A view of this is available here: http://www-01.ibm.com/support/docview.wss?uid=swg24040705

To use the Clone Entities Pluglet, first import the pluglet into your IDA workspace
1. Download the com.ibm.ima.pluglets.samples.data.zip file and note the location of the download
2. Open IDA and select File > Import from the main menu
3. In the import wizard, navigate to General > Existing Projects into Workspace
4. Use the Select Archive File section on the second line and hit the Browse button
5. Navigate to the zip file you have downloaded
6. Complete the import

Steps 3-6 must be completed for each individual workspace you use. Pluglets are not installed into the IDA workbench, rather they are registered and run in real time.

To register IDA pluglets (complete this once per session to use pluglets)
1. Open a Logical or Physical Data Model
2. Right click on a Package/Entity/Attribute/Relationship etc
3. In the context menu select Run Pluglet > Register Pluglets
4. You should get a message to say "<n> pluglets registered"
5. You can now use the Clone Entities Pluglet

To run the Clone Entities Pluglet
1. Ensure the target model for the cloned entities is open
2. Select a set of Entities in the Data Project Explorer
3. Right-click on the selection and select Run Pluglet > Custom Tasks > Clone Selected Entities
4. In the dialog popup, you will be presented with open Logical Data Models. Select a package as the target and hit OK
5. The entities should be cloned into the selected package

Note: The following default settings are currently assumed
1. Non-persistent Entities, Attributes, Relationships WILL NOT be cloned
2. FK attributes, which are part of relationships with a parent Entity not in the selection, WILL NOT be cloned
3. Inherited PK attributes (via a generalization) WILL be cloned, regardless of whether or not the supertype is in the selection
