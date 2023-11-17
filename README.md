# Semana 5
## Primeiro desafio: Instalar uma VM com OL8, instalar o ANSIBLE e criar um YAML de ping para o IP do seu desktop (Criar documentação do passo a passo)
<br> Podemos começar nosso desafio dando um update em nosso dnf da seguinte forma:

    sudo dnf install ansible  
<br> Agora podemos instalar o ansible com 

    sudo dnf install ansible
<br> Podemos tanmbem instalar o ansible atraves do comando pip que é o instalador de pacotes do python com os comandos

    sudo yum install python3-pip
    pip3 install ansible    
<br> Podemos conferir se tudo deu certo digitando em nosso console: ansible --version

<br> Com nosso ansible instalado podemos começar nossas configurações, primeiramente vamos criar um diretorio para criação dos nossos arquivos necessarios

    mkdir ~/teste_ansible
    cd ~/teste_ansible
<br> Agora ja dentro de nosso diretorio podemos criar um arquivo geralmente chamado de inventory.ini, dentro deste arquivo iremos colocar 2 linhas uma sendo especificando uma especie de grupo para o processo e na segunda o ip que pretendemos pingar futuramente, sendo assim criamos e escrevemos o ip no arquivo com os seguintes comandos: 

    echo "[desktop]" > inventory.ini
    echo "192.168.2.100" >> inventory.ini
<br> Pronto! Nosso arquivo está do jeito que precisamos, agora precisamos criar nosso arquivo .yaml que sera responsavel por "ler" o nosso arquivo .ini, podemos cria-lo da seguinte forma: 

    touch ping_desktop.yml    
<br> Agora posso entrar em meu arquivo com o editor de texto da minha preferencia:

    sudo nano ping_desktop.yml
<br> Dentro de nosso arquivo podemos escrever algumas linhas dando name ao nosso processo e especificando o grupo que ele irá executar no caso as linhas que iremos adicionar são as seguintes:
<br> . "name": Ping Desktop: Este é um comentário que descreve o que o playbook está fazendo, usado apenas para identificar o processo
<br> . "hosts": desktop: Especifica em quais hosts ou grupos de hosts as tarefas devem ser executadas. No nossocaso, criamos um grupo chamado desktop no arquivo de inventário (inventory.ini). Os hosts pertencentes a esse grupo serão os destinatários das tarefas neste playbook.
<br> . "tasks": Aqui você lista as tarefas que deseja realizar nos hosts especificados.
<br> . "name": Ping the desktop: Mais uma vez, é um comentário para descrever a tarefa que está sendo executada.
<br> . "ping": Esta é uma tarefa específica do Ansible chamada "ping". Ela não executa um ping de rede como o comando de ping tradicional, mas verifica se os hosts podem se comunicar com o servidor Ansible.

<br> Em suma devemos ter um arquivo parecido com essa saida:

      ---
      - name: Ping Desktop
      hosts: desktop
      tasks:
        - name: Ping the desktop
          ping:

<br> Agora podemos salvar e sair de nosso arquivo e podemos executar o playbook

      ansible-playbook -i inventory.ini ping_desktop.yml


## Segundo desafio: 
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
