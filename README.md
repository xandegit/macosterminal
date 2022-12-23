# macosterminal

## Busy port
lsof -i: <port number>

lsof -i:5001
and kill the process number

kill -9 <process number>

Busy port by node

lsof -i:3000 -t | xargs kill

or

killall -9 node


#Search files containing text and add them to bash file to remove
find . | xargs grep -l '//TOREMOVE' | awk '{print "rm "$1}' > doit.sh
Execute it
source doit.sh

#show lines number in file
cat doit.sh | wc -l

#Search files containing text
grep -lr '//TOREMOVE'

find . | grep -lr '//TOREMOVE'
