- Why shell script over tools?

the tools are rstricted in my organization somehow so i used to write the shell scripts to check the server helath of 500 vms
with custom parameters and also i dont this the perameters are available defaulty in the tools.


- date | echo "Monday" whats the output?

here Monday is output cause date is a fdefault command that always writes to systemin which doesn't return any output from the first command date.
so pipe property is to take the previous command output but previous one is not returning any output so it just execute the next one without depending on
the first one or independtly it gets executed.

- what you will do as a devops eng on failing an application from your 100 apps?

i will go to the logfile and check for the errors first. to read that the log files are very very very huge to read from all the log levels
TRACE level INFO level and ERROR level i check for filtering of ERRORS.

Usually logs are stored in a seperate external storages not on VM directly like in github, amazon s3, azure blob, google cloud services so i will
gather the end point of the logs using curl command the filter it out by errors

curl log/url/endpoint | grep error

