## File Ownership

$ touch sample.txt
$ ls -l sample.txt
file_type:file_permission:link_count:file_owner:file_group:file_size:last_modified:file_name

// file permission
User:Group:Others

// file permission change
$ chmod 777 sample.txt
$ mv sample.txt ~user1 >> move file to user1's home directory
$ su - user1

// file | group ownership change
$ chown ubuntu:ubuntu sample.txt == chown ubuntu sample.txt || chgrp ubuntu sample.txt
