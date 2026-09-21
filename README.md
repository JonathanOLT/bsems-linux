####################################################################################################
#                                   GUIA DE INSTALAÇÃO BSEMS (PT + EN)                             #
#        Script criado por: https://t.me/thepurgeeee  /  https://www.youtube.com/@ScriptJovem      #
#      Créditos totais ao canal: Jonathan Olt (YouTube) → https://www.youtube.com/@jonathanolt     #
####################################################################################################
#                         Senha para extrair o arquivo (WinRAR): ScriptJovem                       #
####################################################################################################



====================================  🇧🇷 TUTORIAL EM PORTUGUÊS  ====================================

1) Acesse o servidor Debian 12 e faça login como root:
su -

2) Crie uma pasta para armazenar os arquivos do instalador:
mkdir -p /root/bsems
cd /root/bsems

3) Envie para esta pasta os seguintes arquivos:
   • script.sh
   • bsems_V2.3.4_24_07_2023.tgz

4) Verifique se os arquivos estão na pasta:
ls -lh

5) Dê permissão de execução ao script:
chmod +x script.sh

6) Execute o script:
./script.sh

   O script desenvolvido por ScriptJovem fará automaticamente:
   - Ativar NTP temporariamente
   - Remover qualquer instalação antiga do Docker
   - Instalar Docker, containerd, docker compose plugin e dependências
   - Ajustar a data/hora do sistema (necessário para evitar erro de licença)
   - Extrair o arquivo bsems_V2.3.4_24_07_2023.tgz para /etc/bsems
   - Corrigir o arquivo startup.sh (docker compose, tar, permissões)
   - Remover a linha “version:” do docker-compose.yml
   - Iniciar todos os containers do BSEMS
   - Exibir a mensagem final: "### Setup concluído com sucesso!"

IMPORTANTE:
- NÃO renomeie o arquivo .tgz. O script procura exatamente:
  bsems_V2.3.4_24_07_2023.tgz
- O script deve ser executado na mesma pasta onde o arquivo .tgz está.
- ⚠️ Como o script altera a data/hora do servidor, recomenda-se que ESTE SERVIDOR 
  SEJA USADO EXCLUSIVAMENTE para o EMS, evitando problemas com outras aplicações.

7) Após completar a instalação, acesse o EMS no navegador:
https://IP_DO_DEBIAN:6443/emsWebServer/

8) Verifique se os containers estão ativos:
docker ps

Se os serviços do BSEMS aparecerem, a instalação foi concluída.



====================================  🇺🇸 ENGLISH TUTORIAL  ====================================

#        Script created by: https://t.me/thepurgeeee  /  https://www.youtube.com/@ScriptJovem      
#        Full credits to the channel: Jonathan Olt (YouTube) → https://www.youtube.com/@jonathanolt
#        Password to extract the file (WinRAR): ScriptJovem
####################################################################################################

1) Access the Debian 12 server and log in as root:
su -

2) Create a folder to store the installation files:
mkdir -p /root/bsems
cd /root/bsems

3) Upload the following files into this directory:
   • script.sh
   • bsems_V2.3.4_24_07_2023.tgz

4) Confirm the files are present:
ls -lh

5) Make the script executable:
chmod +x script.sh

6) Run the script:
./script.sh

   The script developed by ScriptJovem will automatically:
   - Temporarily enable NTP
   - Remove any previous Docker installation
   - Install Docker, containerd, docker compose plugin and dependencies
   - Adjust the system date/time (required to avoid licensing issues)
   - Extract bsems_V2.3.4_24_07_2023.tgz into /etc/bsems
   - Fix startup.sh (docker compose, tar options, permissions)
   - Remove the “version:” line from docker-compose.yml
   - Start all BSEMS containers
   - Display the message: "### Setup completed successfully!"

IMPORTANT:
- Do NOT rename the .tgz file. The script expects:
  bsems_V2.3.4_24_07_2023.tgz
- The script MUST be executed from the same folder where the .tgz file is located.
- ⚠️ Since the script changes the server’s date/time, it is strongly recommended 
  that this server be dedicated ONLY to the EMS to avoid issues with other systems.

7) After the installation is complete, access the EMS:
https://DEBIAN_IP:6443/emsWebServer/

8) Check if all containers are running:
docker ps

If the BSEMS services appear, the installation is complete.
