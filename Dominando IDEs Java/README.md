# Dominando IDEs Java

 ▪️ Instalação e configuração Java no MacOS
 
  :white_check_mark: Instalação JDK 17 LTS
  
  :white_check_mark: Configuração de variável de ambiente
  
  :white_check_mark: Instalação do Eclipse
  
  :white_check_mark: Configurando o ícone no Dock
  
  :white_check_mark: Instalação do IntelliJ

:apple: MACOS

🔺 Instalação JDK Oracle
O **JDK 17 LTS** é a última versao de longo suporte cujos binários são de uso gratuito sendo (https://www.oracle.com/downloads/licenses/no-fee-license.html)

🔸 1. Abra o terminal e vamos verificar se temos o Java instalado:

java -version

🔸 2. Para instalar o JDK 17, acesse o link (https://www.oracle.com/java/technologies/downloads/#jdk17-mac), e escolha a versão para a respectiva arquitetura do seu Mac.

Executar o arquivo de extensão .dmg e seguir com NEXT até o final da instalação.

🔸 3. Confirme se realmente foi instalado com sucesso:

java -version

🔸 4. Vamos configurar o ambiente JAVA_HOME:

4.1. Verificar o caminho da instalação do Java:

/usr/libexec/java_home

4.2. Copie o caminho que aparecerá no terminal, no meu caso:

/Library/Java/JavaVirtualMachines/jdk-17.jdk/Contents/Home

4.3. Descubra qual o tipo de Shell do seu MacOS:

echo $SHELL
No meu caso: /bin/zsh

4.3.1. Se o seu SHELL for o zsh, Abra o ~/.zshenv:

nano ~/.zshenv 

4.3.2. Se o seu SHELL for o bash, Abra o ~/.bash_profile:

nano ~/.bash_profile

4.4. Copie o código abaixo e cole no final do arquivo:
export JAVA_HOME=$(/usr/libexec/java_home)

4.5. Salve o arquivo

4.6. Source the arquivo e escreva $JAVA_HOME:

source ~/.zshenv _OU_ source ~/.bash_profile

% echo $JAVA_HOME
/Library/Java/JavaVirtualMachines/jdk-17.jdk/Contents/Home

🔸 5. Feche o terminal e abra novamente

🔸 6. Vamos conferir mais uma vez se o Java está instalado na nossa máquina

java --version
