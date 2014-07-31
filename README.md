csdir
=====

create shared directory

This script creates a directory with proper permissions for sharing files
between local users and creates symbolic links on every user's desktop.

Requirements:

   * ACL enabled (permissions must be inherited from shared directory)
   * sudo

Default settings:

   * shared directory is /home/shared
   * permissions are based on group "users"
   * each member of that group with a home directory in /home will get a link
     $HOME/Desktop/shared to /home/shared
   * xdg subdirectories will be created in the shared directory (Pictures,
     Videos, Documents, ...) using the language settings of the user who's
     calling this script; so if the user's documents directory is called
     "Dokumente" csdir will create /home/shared/Dokumente
   * the file owner attribute of files in /home/shared is fyi only; he can
     chmod the file as he likes, but still everyone in the group "users" can
     read/write/delete the file

Suggestions?

   * Should this script get a GUI?
   * Should it also work w/o ACL?
   * Will it blend?
   * Please raise a GitHub issue or - even better - fork & implement your
     favourite feature yourself. This is free software.

