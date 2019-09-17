# Welcome to Doduo!

## Vagrant & Virtual Box
Pentru rulare sunt necesare **[Virtual Box](https://www.virtualbox.org/wiki/Downloads)** , **[Vagrant](https://www.vagrantup.com)** si **[Git](https://git-scm.com/downloads)**.


## Clone repo
Trebuie sa avem **repository-ul** clonat local, iar pentru asta rulati comanda 
```
git clone https://github.com/PirvuDanielCatalin/DoduoProjectDocs.git
```
Dupa care intrati in folderul proiectului cu ajutorul comenzii
```
cd DoduoProjectDocs
```
Rulati masinile virtuale cu ajutorul comenzii
```
vagrant up
```

## Masinile virtuale
Nume Masina         | IP            | Hostname			  | Config 
--------------------| ------------- | ------------------- | -------
VM1.Proiect.Sprint1 | 192.168.56.61 | vm1.proiect.sprint1 | VM1
VM2.Proiect.Sprint1 | 192.168.56.62 | vm2.proiect.sprint1 | VM2
VM3.Proiect.Sprint1 | 192.168.56.63 | vm3.proiect.sprint1 | VM3
 
 #
 
 Nume Masina        | Use           
--------------------| ------------- 
VM1.Proiect.Sprint1 | Ansible Control Node
VM2.Proiect.Sprint1 | Jenkins Master
VM3.Proiect.Sprint1 | Docker, Private Registry, Nexus


## Conectare la masina
Pentru a va conecta pe o masina, fiind pe Windows, rulati comanda:
```
vagrant ssh nume_masina
```
Pentru a va conecta pe o masina, fiind pe oricare masina, rulati:
- ``` ssh vagrant@hostname_masina ```
sau
- ``` ssh config_name ```

## Pentru a rula playbook-urile folosind ansible
- Trebuie sa fim pe masina VM1 , iar pentru asta rulam ``` vagrant ssh VM1.Proiect.Sprint1 ``` daca rulam comanda pe Windows sau ``` ssh VM1 ``` daca suntem pe oricare masina in afara VM1.
- Apoi ne conectam ca root prin comanda ``` su ```, parola fiind **vagrant**.
- Ne mutam in folderul **ansible_playground** din directorul home al root, comanda este
 ``` cd ~/ansible_playground ```
 - Rulam un anume playbook prin comanda ``` ansible-playbook NumePlaybook.yml ```