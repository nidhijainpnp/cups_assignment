#Printing Comments in Log Files
This file describes the approach of adding the comments in log files (access_log and error_log).

There were two log files, access_log and error_log. I captured some of the keywords in access_log and used grep command to find relevant files that could generate them.

##For access_log file
I searched the keyword "localhost" and found a file log.c located in scheduler folder and there, found a function cupsFilePrintf();The function accepted two arguments,i.e.file name and the text to be written in that file.

##For error_log file
I searched the keyword "Using keychain" and found a file conf.c located in scheduler folder and there, found a function cupsdLogMessage();The function accepted two arguments,i.e.debug level and the message to be written.

I added the following text "custom debug by Nidhi" in the above two log files.