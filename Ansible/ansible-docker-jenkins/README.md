#            Ansible-Docker-Jenkins
 * This ansible role is used to deploy jenkins 

## PreReq's

* Install following dependencies 

### Ansible 

  ```
  # become root user
  sudo -i
  adduser ansible
  vi /etc/ssh/sshd_config
  # change passwordAuthentication from no to yes & save the file
  service sshd restart
  visudo
  # scroll to the line where you see %sudo or wheel
  # and add the below line
  ansible ALL=(ALL:ALL) NOPASSWD:ALL
  ```
  * Install python & Ansible [click here](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html#latest-releases-via-apt-ubuntu)

  * Configure nodes for ansible access

     * Give no password access
     * Create a key pair
      ```
      ssh-keygen
      ```
     * copy public to nodes
     ```
     ssh-copy-id ansible@<node-ip>
     ```
### Docker
  
  * To install docker on Linux
  ```
  curl -fsSL https://get.docker.com -o get-docker.sh
  sh get-docker.sh
  sudo usermod -aG docker <username>
  docker info
  ```


  