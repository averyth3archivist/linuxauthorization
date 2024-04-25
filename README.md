# linuxauthorization
## Managing File Permissions using Linux (Portfolio Project from Google Cybersecurity Professional Certificate)

### Project Description

As a security professional at a fictitious large organization, I am tasked with ensuring members of the research team are authorized with the appropriate permissions on the system. In this project, I examined the existing permissions and made modifications if they did not match the authorization that should be provided, using Linux commands.


### Check file and directory details

First, it is necessary to examine the existing file and directory permissions to see what needs to be modified. I used the ```ls -la``` command to list permissions to files, and directories, including hidden files. Figure 1 shows the commands use to navigate to the ~/projects folder to then list the file and directory permissions.

![alt text][figure1]

[figure1]: https://github.com/averyth3archivist/linuxauthorization/blob/30e8698a45ddd086d7f6819894e896590617726a/LinuxAuthorization_Figure1.png "Figure 1"
***Figure 1.** - Demonstration of the ls -la Linux command.*


### Describe the permissions string

Permissions string output: 
```-rw-rw-r-- 1 researcher2 research_team   46 Apr  1 18:17 project_r.txtp```

**Figure 1** shows the output for the file "project_r.txt." This 10 character string at the beginning represents the file permission both the user and group owner types have read and write permissions, while the other group type has only read permissions. 


### Change file permissions

Provided that the organization does not allow other to have write access to any files, permissions need to be modified for the file "project_k.txt." As demonstrated in Figure 2, I used the chmod command to modify the write permissions for the other owner type. In the first argument, I specify that I would like to take away write permissions from the other owner type, using ```o-w```. In the second argument, I specify that I would like to make the modification for "project_k.txt."

![alt text][figure2]

[figure2]: https://github.com/averyth3archivist/linuxauthorization/blob/30e8698a45ddd086d7f6819894e896590617726a/LinuxAuthorization_Figure2.png "Figure 2"

***Figure 2.** - Demonstration of the use of the chmod command to change the write permissions on the "project_k.txt" file for the other owner type and the ls -la command to display the output.*

### Change file permissions on a hidden file

The file .project_x.txt is an archived, hidden file, only available to be read by the user and group owner types. Therefore, I modified permissions using the chmod command.

![alt text][figure3]

[figure3]: https://github.com/averyth3archivist/linuxauthorization/blob/30e8698a45ddd086d7f6819894e896590617726a/LinuxAuthorization_Figure3.png "Figure 3"

***Figure 3.** - Demonstration of modifying permissions on the hidden file (.project_x.txt) to read-only for the user and group owner types.*

### Change directory permissions

Only researcher2 or the user owner type should have access to the drafts directory, therefore I used the chmod command to get rid of the execute permissions for the group owner type.

![alt text][figure4]

[figure4]: https://github.com/averyth3archivist/linuxauthorization/blob/30e8698a45ddd086d7f6819894e896590617726a/LinuxAuthorization_Figure4.png "Figure 4"

***Figure 4.** Demonstration of modifying the execute permissions for the group owner type to ensure that only the user owner type has access.*

### Summary

In this project, I used Linux commands to manage file permissions to match the appropriate level of authorization set by my organization. In the projects directory, I used ```ls -la``` to examine the existing permissions. Then, I modified permissions on files and directories using the ```chmod``` command.
