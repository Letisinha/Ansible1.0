# Ansible1.0
Aqui descrevo meus testes com Ansible em máquinas virtuais criadas na plataforma AWS utilizando isntâncias EC2:

Nesse teste primário subi 3 instâncias AWS, uma controller node e duas worker nodes.

![image](https://github.com/Letisinha/Ansible1.0/assets/87834617/ce576f13-cdba-4416-94ce-5355e3f44dee)

Fiz a instalação do ansible na instância controller e a conexão entre a controller as workers com a chave SSH. 

O próximo passo foi definir o inventário com os IPs privados das máquinas workers e testar a conexão. 

![image](https://github.com/Letisinha/Ansible1.0/assets/87834617/1192090a-3fa2-4acc-9020-50708d8f0a75)

Com a conexão testada, pude criar minha pasta playbooks onde coloquei meu código yml (presente no repositório) que faz a instalação do apache nas worker nodes e inicia um HTML bastante simples.

Rodando o playbook nas worker nodes, o código html deve ser exibido na pasta de destino definida no playbook:

![image](https://github.com/Letisinha/Ansible1.0/assets/87834617/417747f4-ba33-45d9-a0e0-278292a667cc)

Assim, colocando o IP público de cada worker node no navegador, o HTML deve ser apresentado:

Máquina worker1:

![image](https://github.com/Letisinha/Ansible1.0/assets/87834617/fec108b3-df47-450d-82ed-fbf113d4797d)

Máquina worker2:

![image](https://github.com/Letisinha/Ansible1.0/assets/87834617/b36da34e-fc85-4b9b-ad34-2796a18befaa)

----- fim do teste -----
