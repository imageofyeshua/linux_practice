## user and group

$ /etc/passwd
username:passwd:user_id:group_id:addition_info:home_dir:basic_shell

// user password
$ /etc/shadow

// user group
$ /etc/group
group_name:passwd:group_id:second_user

// add user
$ adduser --gid 1001 user1
$ adduser --gid 1001 user2
$ tail -5 /etc/passwd
$ tail -5 /etc/group
$ ls -l /home >> check newly created users
$ ls -a /home/user1 >> check base files
$ ls -a /etc/skel >> basic files to copy into newly created user's home dir

// change passwd
$ passwd newuser1

// user property change
usermod --groups ubuntu newuser1

// user remove
$ userdel -r newuser1 >> -r : delete all info

// set the password change cycle
$ chage -m 2 newuser1

// current group
$ groups

// create new group
$ groupadd newgroup1

// group property change
groupmod --new-name mygroup1 newgroup1

// group remove
$ groupdel newgroup1

// set group password
$ gpasswd mygroup1
