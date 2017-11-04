# ammoSave
Enables Ammo to be Saved to the Databse for Exile servers.
Reverse Engineered from Rod Serlings excellent AVS Script http://www.exilemod.com/topic/7268-avs-advanced-vehicle-system/
All credit to Rod for the original work. 
Currently works with extDB2, haven't done anything with ExtDB3 but feel free to do try and edit yourself, should be pretty easy to work out.

Install:
1. Stop your server.
2. Run the enclosed SQL script on your database.
3. Replace the exile.ini file (exilsever\extDB) on your server with the provided one, or merge if you have changed it for other scripts.
4. Download your mission file from the server and un-PBO it.
5. Create a folder called Custom\ammoSave in your mission PBO (you can change the location but will need to redo all the scripts to use the new location).
6. Open config.cpp in your mission file and add the following under "class CfgExileCustomCode"
	ExileServer_object_vehicle_database_update = "Custom\ammoSave\ExileServer_object_vehicle_database_update.sqf";
	ExileServer_object_vehicle_database_load = "Custom\ammoSave\ExileServer_object_vehicle_database_load.sqf";
	ExileServer_object_vehicle_database_insert = "Custom\ammoSave\ExileServer_object_vehicle_database_insert.sqf";
	ExileServer_object_vehicle_carefulCreateVehicle = "Custom\ammoSave\ExileServer_object_vehicle_carefulCreateVehicle.sqf";
7. If you don't have an init.sqf file in your mission copy the provided one into the root fold of the mission. If you do copy the contents of the provided file and add it.  
8. re-PBO and push edited mission file to your server.
9. Restart the server.... profit!!
