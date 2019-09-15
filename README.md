# miniDSP BEQ

Save files for movie BEQ for the miniDSP 2x4HD. The BEQ settings are entered on both inputs' PEQ filters.  All other filters and settings are for left at a flat house curve for universal use.  

## Save File Use
In the miniDSP HD1 pluggin select the File Menu -> Load -> Load configuration to current slot.  An open dialog will appear. In it select the BEQ file for the movie you wish to load and press the open button.  The BEQ config is now loaded into the currently selected config slot.

Note: Some files include a comment about a positive or negative gain in their name.  This is an adjustment that is made by increasing or decreasing your main volume.  

![Load File](/images/loadFile.png)

## Git Setup
Using git to clone the repositories has the advantage of easily updating the list as new BEQs are added and it will also update existing files if the BEQ for the movie has been updated. 

### Download Github client
Download the Github Desktop client from https://desktop.github.com. A version is available for both Mac and Windows. 

On first launch it will ask you to set-up a GitHub account.  This can be skipped as it's not needed for downloading the files. 

### Clone the repository
In the main window, press the "Clone a Repository" button.

![No repository](/images/norepo.png)


In the configuration window that opens enter https://github.com/bmiller/miniDSPBEQ for the Repository URL.  You can also change the Local Path of where the BEQ files will be saved if you prefer a different location.  

![Repository setup](/images/reposetup.png)

Press the Clone button.  This will download all of the BEQ files to your computer at the location entered for the Local Path and they can then be loaded into your miniDSP 2x4 HD when you view a movie.

### Load Updates

After you clone the repository and when you relaunch GitHub Desktop the main window will open and have the miniDSPBEQ repository selected.  To load any new BEQs or updates to existing ones press the "Fetch origin" button.  This will cause the app to check if any updates are available.  If updates are available the button will change to "Pull origin". Press it again to download the updates.  The folder on your computer with the save files is now updated to the latest BEQs.  

![Fetch Updates](/images/fetchupdates.png)

## Adding New BEQs

Note: only authorized users can directly add to the repository

### Create Branch

First create a new branch called "newBEQs".  This only needs to be done the first time.  Start by selecting the branch selector.

![Branch Switch](/images/branchSwitch.png)

Press the new "New Branch button".  Then in the dialog that opens type in the name "newBEQs" and press the "Create" button.

![New Branch](/images/newBranch.png)

### Committing

Generate the xml save file from either BEQDesigner or from the miniDSP app and save it to the Movie or TV Shows folder of your local copy of the repository. In the GitHub app check the newBEQs branch is selected.  In the Changes tab on the left hand side of the screen it should be showing the xml file(s) that were saved. Check the checkbox next to the filename if it is not already checked.  Then in the Summary text box enter a note on what is being added.  The format I've been using is:

```
Added: \<list of added movies\>
Updated: \<list of updated movies\>
```
	
Once the note is added press the "Commit to newBEQs" button.  

![Commit](/images/commit.png)

Finally, the new commit needs to be pushed to the server.  Press the "Push origin" button in in the window.  

![Push](/images/push.png)