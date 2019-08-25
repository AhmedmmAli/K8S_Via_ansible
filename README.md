# K8S_Via_ansible
build a web server serving anything of your choice deployed on a Kubernetes cluster.

# Prerequisites

1- To run this task first you will need two machines, one will work as a master node and the other one will work as the worker node
2- You will need to trust your public key on those two machines.
*********************************************************************************************************************
 				Installation
*********************************************************************************************************************

1- You need to replace the IPs in the var file and the host file with the new IPs you got for the two machine.

2- Run this command " ansible-playbook  -i hosts plays/kubernetes.yml --extra-vars "created_user=ubuntu"  ".

3- Wait a few minutes for the installation is done.

4- SSH to the master machine and swich to user "ubuntu".

5- Run command "kubectl get nodes" to verify that everything is working fine.

6- Run command "kubectl get po" to see the 3 replicas of nginx running.

7- Run command "kubectl get svc" to see the service file that belong to nginx.

8- To access nginx from the browser you must write: IP_OF_THE_MASTER_MACHINE:NodePort.

