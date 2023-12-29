# Ansible_Project2
Ansible Practice

- Step 1
  - Create 3 Instances in AWS
    Name: ansible_control , ansible2, ansible3
    OS: Ubuntu
    t2 micro
    Authentication: .pem access key
    15 GB

  - Use Mobaxterm to log into instances via ssh
    Click session - ssh - input ip of target instance - username "ubuntu" - advanced ssh settings - input .pem file - connect
    Use command "sudo nano /etc/hostname" to change each hostname to the matching instance name then restart server "sudo init 6"
    Enter commands "sudo apt update" "sudo apt upgrade" on each server

  - Run "sudo apt install" on ansible_control server
    cd .ansible/
    vi inventory
        [linux]
        ...
        [linux:vars]
        ansible_user=
        ansible_password=
    esc - :wq - enter | this will save the file
        vi ansible.cfg
        host_key_checking = False
    esc - :wq - enter
    ansible linux -m ping




    
