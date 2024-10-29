# roomba_ros_ic
Pacotes ROS do trabalho de iniciação cientifica - Rafael Arueira 

Como utilizar:

1) Para executar o programa no Roomba fisico

- Realizar login no roomba via ssh: 

    ssh -X nuria@roomba.local
    
- Criar a pasta para o workspace de trabalho no diretorio raiz

    mkdir testes_ws
    
- Baixar os arquivos deste repositório
    
    mkdir testes_ws/src
    cd testes_ws/src
    git clone git@github.com:marangoni/roomba_ros_ic.git
    
- Remover o diretório das simulações:

    rm -rf create_simulator
    
- Criar o workspace com os pacotes baixados

    cd ~/testes_ws
    catkin_make
    
- Carregar os arquivos launch do pacote roomba_robot conforme a ação desejada

    roslaunch roomba_robot [tab] [tab]
    roomba_joy.launch OU
    roomba_lidar.launch OU
    roomba_go.launch OU
    roomba_go_lidar.launch OU
    roomba_cam.launch
    
- Orientações sobre os arquivos Launch    
roomba_joy.launch - carrega o roomba para controle via joystick
*** ATENÇAO: Depois de executar o comando roslaunch roomba_robot roomba_joy.launch desconectar e conectar novamente

o dongle do joystick para que ele seja reconhecido.

* roomba_lidar.launch - carrega o roomba com o Lidar para movimentação com o joystick e 
exibição no rviz
*** ATENÇAO: Para poder visualizar a saída do Lidar no Rviz é necessário realizar o acesso
via ssh habilitando a interface grafica com o comando ssh -X nuria@roomba.local

* roomba_go.launch - carrega o roomba para movimento autonomo

* roomba_go_lidar.launch - carrega o roomba para movimento autonomo e lidar com exibição no
rviz
*** ATENÇAO: Para poder visualizar a saída do Lidar no Rviz é necessário realizar o acesso
via ssh habilitando a interface grafica com o comando ssh -X nuria@roomba.local

* roomba_cam.launch - carrega o roomba para controle com o joystick e visualização da 
pela camera IR no Rviz

2) Para executar a simulação no notebook

*** Necessário o ROS noetic e gazebo 11 instalados e configurados ***

- Criar a pasta para o workspace de trabalho no diretorio raiz

    mkdir testes_ws
    
- Baixar os arquivos deste repositório
    
    mkdir testes_ws/src
    cd testes_ws/src
    git clone git@github.com:marangoni/roomba_ros_ic.git
    
- - Criar o workspace com os pacotes baixados

    cd ~/testes_ws
    catkin_make
    
- Seguir as instruções do arquivo para carregar as simulações

    create_simulator/create_gazebo/launch/guia_comandos.txt
    
    

  
    


