# ORG TERMINAL
### Um guia de instalação do WSL no windows e utilização do terminal do windows com o OH MY ZSH e algumas configurações que tornam o terminal mais produtivo

## INSTALAÇÃO DO WSL NO WINDOWS 

* executar o comando
~~~~terminal do shell
wsl --install
~~~~
* Caso venha o texto de ajuda do WSL ao executar o comando acima tente executar o comando abaixo, que irá listar todos as distribuições disponíveis 
~~~~terminal do shell
wsl --list --online 
~~~~
* Execute o comando a seguir para instalar uma distribuição da sua preferência
~~~~terminal do shell
wsl --install -d <DistroName>
~~~~
Obs: Execute o shell em modo administrador

* Agora é só baixar o windows terminal diretamente na loja da Microsoft
* Após instalação, abra o temrinal e acesse o menu de configurações do windows terminal ou aperte 'Ctrl' + ','.
* Na janela que abrir procure por perfil padrão e no canto direito mude de windows PowerShell para A ditricuição instalada por você.
* A partir deste momento o sistema irá pedir o nome de usuário e uma senha para a distribuição instalada.
* Sugiro como boas práticas executar os comando abaixo para fazer um update no pacotes 
~~~~bash
sudo apt update && sudo apt upgrade
~~~~

## INSTALAÇÃO DO ZSH
* Primeiramente é necessário instalar o ZSH com o comando 
~~~~bash
sudo apt install zsh
~~~~
* Instalando o Oh My Zsh
  * Ferramenta para gerenciar sua configuração do Zsh. Inclui mais de 200 plug-ins opcionais (rails, git, OSX, hub, capistrano, cerveja, formiga, php, python, etc), mais de 140 temas e uma ferramenta de atualização automática.
~~~~bash
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
~~~~
* A partir de agora todas configurações que você quer fazer como adicionar variáveis ambientes ou configurar seu terminal de qualquer forma utilize o arquivo ~/.zshrc e não mais o ~/.bash_profile ou derivados.
  
