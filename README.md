# hackerrank

Note: this playbook supports only ubuntu distribution and will require sudo access. 

1. Clone the repository on the system where you want to deploy the stack

2. Install ansible using install_ansible.sh script
   
   cd hackerrank && sudo sh install_ansible.sh

3. run playbook
   
   cd hackerrank/apache-tomcat-app 
   
   ansible-playbook -i "localhost," -c local setup.yml     ( if sudo doesn't require password )
   
   OR
   
   ansible-playbook -i "localhost," -c local -K setup.yml  ( if sudo require password )

4. Once deployment has been finished you can check the load balancing using sample application http://localhost/LoginWebApp/ .

5. Additionaly you can also check the  load balancer status using http://localhost/balancer-manager .

