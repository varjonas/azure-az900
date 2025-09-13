Realizado a criação de um grupo de recursos no Azure, aqui, optamos por criar o grupo na região East US, porém, a criação da nossa VNET foi feita através da região Brazil South.
Esse passo é simples e busca mostrar que é possível criarmos grupos, onde irão conter os recursos necessários para utilizarmos, tal como uma VM ou uma VNET, é possível adicionar descrição a tudo, garantindo assim, rastreabilidade futura.
Toda edição realizada fica salva na aba log de atividade, ali é possível verificar quem, quando e o que foi criado.

Em visualizador de recursos, temos uma visão aberta de quais recursos possuímos no nosso grupo e abri-los diretamente.
Importante ressaltar que é possível criar bloqueios e gerenciar a permissão de cada usuário, para que edições não autorizadas sejam realizadas.

<img width="948" height="727" alt="image" src="https://github.com/user-attachments/assets/9610b2d2-515f-419f-8328-2a24441b6e86" />

------------------------------------------------------------------------------------------------------------------------------
Neste módulo, estudamos sobre armazenamento e contas de armazenamento do azure

É possível criarmos discos de armazenamentos dentro de uma conta de armazenamento para transferencia de arquivos, eu posso realizar o uso do azcopy para facilitar a transferência dos arquivos. O mapeamento do meu diretório também é possível e é compativel com Windows, Linux e MAC.

Conta de armazenamento criada:
<img width="939" height="903" alt="Captura de tela 2025-09-13 105834" src="https://github.com/user-attachments/assets/5c33bff6-b396-48fc-ab76-557054d5fc51" />

Posso também compartilhar os meus arquivos conforme dito acima, isso é compatível com Linux, MAC e Windows, e para isso usaremos o protocolo SMB e porta 445.

<img width="831" height="511" alt="Captura de tela 2025-09-13 110056" src="https://github.com/user-attachments/assets/31861c64-4678-48b0-962d-5612e10ff28e" />

Ainda assim, eu posso usar o gerenciador de armazenamento do azure para gerenciar meus arquivos via azcopy de uma forma de interface gráfica. O azcopy se torna mais pratico para transferencia de arquivos, também usando o Microsoft Storage Explorer do Azure.

<img width="956" height="551" alt="image" src="https://github.com/user-attachments/assets/e671bd15-6bed-49cc-83ab-3a91b58593c4" />

Ainda falando de armazenamento, vimos que no Azure é possível usar conteineres ou um armazenamento blob do azure.

O Armazenamento de Blobs do Azure (Azure Blob Storage) é um serviço da Microsoft Azure que oferece armazenamento escalonável e econômico para dados não estruturados, como arquivos de texto, binários, imagens e vídeos, sendo ideal para aplicações em nuvem, análise de dados, e arquivamento de informações. Ele funciona com base em "blobs", que são objetos binários grandes armazenados em contêineres, com opções de acesso rápido ou de longo prazo e recursos de segurança avançados, como controle de acesso e criptografia. 

O que é um Blob? 
Um blob é um objeto binário grande que pode armazenar qualquer tipo de dado.

Principais usos do Armazenamento de Blobs do Azure:
Fornecimento de imagens e documentos: Exibir conteúdo diretamente a um navegador. 
Armazenamento de arquivos: Para acesso distribuído e gerenciamento de backups. 
Transmissão de conteúdo: Streaming de áudio e vídeo. 
Armazenamento de dados para análise: Alimentar serviços locais ou na nuvem para obter insights. 
Data Lakes e Machine Learning: Suporta grandes volumes de dados para cargas de trabalho de alto desempenho. 


