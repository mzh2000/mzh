# mzh
#!/bin/sh
#sorting following array
echo "please input a number list:"
read -a arr
for (( i=0 ; i<${#arr[@]} ; i++ ))
do
  for (( j=${#arr[@]} - 1 ; j>i ; j-- ))
  do
    #echo $j
    if  [[ ${arr[j]} -lt ${arr[j-1]} ]]
    then
       t=${arr[j]}
       arr[j]=${arr[j-1]}
       arr[j-1]=$t
    fi
  done
done
echo "after sorting:"
