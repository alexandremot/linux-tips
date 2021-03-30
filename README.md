## linux-tips
#### // mysql
----
###### ERROR 1698 (28000): Access denied for user 'root'@'localhost'
###### https://stackoverflow.com/questions/39281594/error-1698-28000-access-denied-for-user-rootlocalhost
----
#### // ssh

###### gerar chave ssh (ssh-keygen)

    ssh-keygen -t rsa

----

###### problema:
    [user@hostname ~]$ ssh root@pong
    @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
    @    WARNING: REMOTE HOST IDENTIFICATION HAS CHANGED!     @
    @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
    
###### solução:   
    ssh-keygen -R <host>
      where host: destination machine

----
#### // helpful hints
----
###### desabilitar desligamento do note quando fechada a tampa

    1. Open the file /etc/systemd/logind.conf as root.
    2. Find this: HandleLidSwitch
    3. If it's commented, uncomment and change the value to ignore. The line after editing should be:

    HandleLidSwitch=ignore

    4. Restart computer and your problem should be gone. Or better restart logind service:

    sudo service systemd-logind restart

----
