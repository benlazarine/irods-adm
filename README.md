# irods-adm

A collection of scripts for administering an iRODS grid


## iRODS Sessions

A session is a group of log messages that occured during a single connection.

The awk script `group-log-by-pid.awk` can be used to group a sequence of log messages by the
connection that generated them.

The bash script `dump-logs.sh` can be used to dump all of the sessions with errors from the CyVerse portion of the CyVerse grid.

The awk script `filter-session-by-cuser.awk` can be combined with `group-log-by-pid.awk` to find all of the sessions for a given user.

The awk script `session-intervals.awk` can be combined with `group-log-by-pid.awk` to find all of the time intervals for each session from a log file.

The bash script `count-sessions.sh` can be combined with `sessions-intervals.awk` to generate a report on the number of concurrent sessions during each second for the time period covered by a log file.


## Resources

The program `resc-create-times` lists all of the root resources sorted by creation time.

The program `check-irods` generates a report on the accessibility of the IES and resources from various locations.


## Generating a histogram of an SQL query for byte-based sizes

The bash script `histgram.sh` can be used to generate a histogram of file sizes.


## Synchronizing data object and file sizes

The bash script `fix-file-size.sh` can be used to set the sizes of a group of data objects with the sizes of their respective files.


## Replication

The program `repl-report` can be used to generate a report on the number and volume of data objects that need to be replicated.

The program `repl` can be used to replicate data objects to the taccCorralRes resource.
