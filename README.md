# abc
#Logic to check for empty variable in the Group and Owner fields and add error handling 
#-z = if variable is empty 
# -n = if variable is not empty

set -x 
if [ -z "$frmGroup" ]; 
then 
  echo "Group Empty" 
elif [ -n "$frmGroup" ]; 
then 
  chgrp $frmGroup $frmPath$frmDirName 
fi

if [ -z "$frmChgOwn" ]; 
  then 
  echo "Change Owner Empty" 
elif [ -n "$frmChgOwn" ]; 
then 
  chown $frmChgOwn $frmPath$frmDirName 
fi
