# Homelab


Ansible Postinstall:

SSH-Key Erstellen und in Semaphore eintragen:

ssh-keygen #Keine Passphrase vergeben!


Auf Zielsystemen sudoers user einrichten:

adduser semaphore
nano /etc/sudoers.d/semaphore

Inhalt:
semaphore ALL=(ALL) NOPASSWD: ALL

chmod 440 semaphore 

Danach von Ansible Server zu Ziel connecten:
ssh semaphore@192.168.178.97

Und SSH Key auf das Zielsystem legen:
ssh-copy-id -i ~/.ssh/id_ed25519.pub semaphore@192.168.178.97