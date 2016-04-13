TimeShift for Linux is an application that provides functionality similar to the System Restore feature in Windows and the Time Machine tool in Mac OS. TimeShift protects your system by taking incremental snapshots of the file system at regular intervals. These snapshots can be restored at a later date to undo all changes to the system.

Snapshots are taken using rsync and hard-links. Common files are shared between snapshots which saves disk space. Each snapshot is a full system backup that can be browsed with a file manager.

http://www.teejeetech.in/p/timeshift.html

Install: kcp -i timeshift

Needed packages: kcp -di libgee


