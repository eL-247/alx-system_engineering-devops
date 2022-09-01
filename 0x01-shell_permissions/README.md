This are what the above scripts does



- 0-iam_betty : prints the effective username of the current user.
~~~~
su betty
~~~~



- 1-who_am_i : prints all the groups the current user is part of.
~~~~
whoami
~~~~

- 2-groups : prints all the groups the current user is part of.

~~~~
id -Gn
~~~~


- 3-new_owner : changes the owner of the file hello to the user betty.

~~~~
chown betty hello
~~~~



- 4-empty : creates an empty file called hello.

~~~~
touch hello
~~~~



- 5-execute : adds execute permission to the owner of the file hello.

~~~~
chmod u+x hello
~~~~



- 6-multiple_permissions : adds execute permission to the owner and the group owner, and read permission to other users, to the file hello.

~~~~
chmod ug+x o+r hello
~~~~



- 7-everybody : adds execution permission to the owner, the group owner and the other users, to the file hello

~~~~
chmod ugo+x hello
~~~~



- 8-James_Bond : sets the permission to the file hello as follows

	- Owner: no permission at all

	- Group: no permission at all

	- Other users: all the permissions

~~~~
chmod 007 hello
~~~~



- 9-John_Doe : sets the mode of the file hello to this:

	- The file hello will be in the working directory

	- You are not allowed to use commas for this script


~~~
chmod 753 hello
~~~~



- 10-mirror_permissions : sets the mode of the file hello the same as olleh’s mode.



	- The file hello will be in the working directory

	- The file olleh will be in the working directory


~~~~
chmod --reference=olleh hello
~~~~



- 11-directories_permissions : adds execute permission to all subdirectories of the current directory for the owner, the group owner and all other users. Regular files should not be changed.

~~~~
chmod -R +X
~~~~


- 12-directory_permissions : creates a directory called my_dir with permissions 751 in the working directory.

~~~~
mkdir -m 751 my_dir
~~~~



- 13-change_group : changes the group owner to school for the file hello

~~~~
chgrp school hello
~~~~



- 100-change_owner_and_group : changes the owner to vincent and the group owner to staff for all the files and directories in the working directory.

~~~~
chown vincent:staff
~~~~



- 101-symbolic_link_permissions : changes the owner and the group owner of _hello to vincent and staff respectively *The file ~_hello~ is a symbolic link*.

~~~~
chown -h vincent:staff _hello
~~~~



- 102-if_only : Write a script that changes the owner of the file hello to betty only if it is owned by the user guillaume.

~~~~
chown --from=guillaume betty hello
~~~~












