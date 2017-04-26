Thread: https://gbatemp.net/threads/3sdsetup-web-sd-setup-release.457604/

**3SDSetup**

For use with https://3ds.guide/


-----------------------------------------------------------------------------------------------------------------------------------------------------------
**Usage**

Sets up SD card for new installations of arm9loaderhax+Luma3DS with magnet links to neccessary torrents.

**Documentation**

getFileBuffer_url(url, name) -> Gets file from URL and stores it with a name to identify it
Example: getFileBuffer_url ("http://3sdsetup.tk/index.html","index")


getLatestRelease(author,repo,filename,step) -> gets the URL from a file that contains "filename" from the latest release of a repository, step is a name to                                                identify the step is used to (must be shared between the actions related to the corresponding step)
Example: getLatestRelease("TiniVi","safehax","3dsx", "Safehax") -> Gets the 3dsx file from the safehax repository for the step "Safehax"


notLatestRelease(author,repo,filename,step) -> same that getLatestRelease but its used in repositories that dont use the "Latest" tag


getFileBuffer_zip(bufferName,original_name,new_name,path) -> Extracts the "original_name" file from an already downloaded zip file and extracts it to an                                                                specified "path"


extractFolder(bufferName,folder,path) -> extracts a whole "folder" from an already downloaded zip file into an specified "path"


extractZip(bufferName,path,remove_path) -> extracts all the contents from an already downloaded file on a specified "folder"
Example: extractZip("Starter Homebrew Kit","","starter"); -> Extracts content of the starter folder
         extractZip("Starter Homebrew Kit","",""); -> Extracts starter folder
         
         
 addFile(name,path,filename,origin) -> Adds an already downloaded file to an specified "path" with and specified "filename"
 Example: addFile("Fasthax","3ds","fasthax.3dsx","list"); -> Adds the Fasthax file to the 3ds folder
