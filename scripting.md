## Sheban part

- `#!/bin/bash`

script executor we have to decalre and make sure it is correct otherwise the script trwos deffrent errors.
we have to choose dash or bash or sh among them mostly.
---
## Metadata information part

that contains the autor, date, version, script description like what it does in the comments.

###########################

# #Author: prasanth kumar kankati

# #Date: 05-11-2025

# #version: V1

###########################
---
## Set Debug mode / use echo to segeregate the outputs of commands while it is printing to console:

- `set -x`
free
prints memory 
df -h
prints disk file
ncpus
---
- `set-e`
if any comand is failed the script, execution will gets break to execute further. So on a right time when the error occurs it stops execution.

create a folder , add user, add permission is there in case if the mkdirr command failed whats the point in executing further so it stops at right time.

---
- `set-o pipefail`
we should use set -e & set -o pipefail together to avoid pipe fail errors depends on previous command false error input to next command.

for example 

asasasas | echo 

first command failed but without set-o echo still exectes feeling that the first command still giving the input to the next so execution goes 
so keeping them together will still breaks the execution even there are pipes on a error.

some people simply right and we can alao write 

`set -exo pipefail`

but for modifications and easiness we can define them individially is the best practice.

----

if not used debug mode all the outputs gets mixed up.


---
pf -ef | grep "amazon"

grepping from the list of processes amzon related processes are filtered out. piping takes the input from first command output and takes as input.












