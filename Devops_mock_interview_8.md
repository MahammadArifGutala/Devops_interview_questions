Unix & Shell 
---
1. Lets say you have a script that will take more than a day to execute, in this case how do you run that script. Also as user you might not able to keep machine in interactive mode for longer period.
3. is it possible to store a commands output, either success or failure to the same file?
----> Yes, i'm trying to do shell command then save the output into variable using shell script. So i use backticks like this :

out=`ls -l`
print $out

4. what is debug mode in shell script?
----->>>
#!/bin/bash
clear
 
# turn on debug mode
set -x
for f in *
do
   file $f
done
# turn OFF debug mode
set +x
ls
# more commands

5. set of commands executed at multiples places in shell script, want to standardize that is it possible something like to define function?
  ------->>>>> Combining the commands – We can use “;“, “&&“, or “||“ to concatenate our commands, 
6. In shell script can we supply parameters to functions? 
             ---> Yes, 
function_name()
{
 echo “hello $1”
 return 1
}
Running the function with a single parameter will echo the value.
$ function_name ram
hello ram

7. what is the use of shift command? 
         ---> The shift command is mostly used when the number of positions that parameters should be shifted to the left. This value can be any non-negative integer. If n is zero (0), no parameter shift will be performed. The default value of n is 1.

10. difference between break and exit 0 in shell script?
        ---> break is a keyword, which causes an immediate exit from the switch or loop ( for , while or do ).   0 exit status means the command was successful without any errors.
11. delete files which are older than 10 days?
                                      ---> find ./my_dir -mtime +10 -type f -delete
12. delete empty files in a given directory?
                                      ---> find .-type f -empty -delete 


Monitoring 
-----
13. what is the importance of monitoring?
14. difference between metrics monitoring and log monitoring, give example for both type of monitoring?
15. how do we configure endpoint in promethus to scrape the data?
16. what is the use of node exporter and alert manager in prometheus?
17. Can we monitor jenkins using prometheus? Also can we send mailer when jenkins is down?
18. what are metric types that prometheus can accept?

kubernetes
----
19. explain any 4 different types of pod statuses and also the reasons that why pod might go into that state?
20. what are operators and give one example where we can use operator?
21. what is the importance of kubeconfig file? Also lets say when you login to kuberenets by default it will pointed to default namespace, if i want list any objects which are other namespace need concate -n option for all the kubectl commands, is there a way we can set the namaspace to aviod -n option in all the commands?
22. given a object how do we find api version and kind with respect to cluster?
23. any work around to bring one pod out of rotation, when multiple replicas has been deployed?

Jenkins
----
24. list of best practices to follow while writing Jenkins pipeline?
25. Is it possible to run each stage on different agaent?
26. Is it possible to change success or error message that we see in console ouput ?
27. Have list of command that has to executed in certain directory in the code, is it possible to do the same?
28. Can we have versioning on Jenkins freestyle job? 

Ansible
---
29. Is it possible to set fact using ansible playbook?
30. can we concate line to exsisting file in remote server, example exporting env variable in bashrc? ( also imporatnt when the playbook runs again if the value exsists then you should not insert)
31. Difference between copy and template module?
32. In one of the template file need to use remote machine ip, how do we read the machine ip value? 

Devops General Interview Questions 
---
- Daily activites of devops engineer 
- challenges that you have faced while working devops 
- what are the envirnments which are there in the organization 
- How the deployents move from one env to other env
