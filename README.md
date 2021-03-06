# 3SDSetup

https://rikumax25.github.io/3SDSetup/

For use with https://3ds.guide/

Thread: https://gbatemp.net/threads/plailects-guides-file-downloaders-web-3sdsetup-wiiusetup.478176/



-----------------------------------------------------------------------------------------------------------------------------------------------------------
**Usage**

SD card setup for...
- stock to boot9strap install
- arm9loaderhax to boot9strap
- boot9strap updating
- wiped SD card

-----------------------------------------------------------------------------------------------------------------------------------------------------------
**Documentation**

getFileBuffer_url(url, name) -> Gets file from URL and stores it with a name to identify it
Example: getFileBuffer_url ("http://3sdsetup.net/index.html","index")


getLatestRelease(author,repo,filename,step) -> gets the URL from a file that contains "filename" from the latest release of a repository, step is a name to                                                identify the step is used to (must be shared between the actions related to the corresponding step)
Example: getLatestRelease("TiniVi","safehax","3dsx", "Safehax") -> Gets the 3dsx file from the safehax repository for the step "Safehax"


notLatestRelease(author,repo,filename,step) -> same as getLatestRelease but used in repositories that don't use the "Latest" tag


getFileBuffer_zip(bufferName,original_name,new_name,path) -> Extracts the "original_name" file from an already downloaded zip file and extracts it to a                                                                specified "path"


extractFolder(bufferName,folder,path) -> extracts a whole "folder" from an already downloaded zip file into an specified "path"


extractZip(bufferName,path,remove_path) -> extracts all the contents from an already downloaded file on a specified "folder"
Example: extractZip("Starter Homebrew Kit","","starter"); -> Extracts content of the starter folder
         extractZip("Starter Homebrew Kit","",""); -> Extracts starter folder
         
         
 addFile(name,path,filename,origin) -> Adds an already downloaded file to a specified "path" with a specified "filename"
 Example: addFile("Fasthax","3ds","fasthax.3dsx","list"); -> Adds the Fasthax file to the 3ds folder
