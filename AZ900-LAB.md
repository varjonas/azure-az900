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

-----------------------------------------------------------------------------------------------------------------------------

Agora no módulo de segurança e identidade na Azure, vimos temas como o Entra ID e também o Microsoft Defender for Cloud, para garantirmos a segurança do nosso ambiente Cloud, as ferramentas devem ser fornecidas pelo provider e o cuidado com a segurança é de nossa parte.

O Entra ID é possível sincronizar com a conta OnPrimese ou não e as permissões que esses usuários irão ter dentro do nosso ambiente, temos os logs das contas também para rastreabilidade das ações realizadas.
<img width="935" height="900" alt="image" src="https://github.com/user-attachments/assets/e1194f13-652d-49b7-aa4a-efee29e44bc2" />

Obs: Quantos dias conseguimos restaurar a conta de um usuário excluído? Os usuários são automaticamente delestados 30 dias após a exclusão.

<img width="951" height="550" alt="image" src="https://github.com/user-attachments/assets/d25e17dc-7c9d-44e5-ab3f-511e17cde10d" />

É possível ativar a funcionalidade para reset de senha, onde o próprio usuário consegue realizar o seu reset, economizando em tempo/chamados, porém é uma função premium e terá um custo.

<img width="935" height="908" alt="image" src="https://github.com/user-attachments/assets/e7dd8755-01f0-49a9-adeb-cca040eeb8d5" />

Funções que podemos criar/alterar
- Nome de dominio personalizado
- Regras e administradores
- Usuários

Também conseguimos consultar o Health, ali mostra a indisponibilidade do serviço Entra ID, conseguimos monitorar o tempo em que nosso serviço ficou ou não indisponível.

<img width="953" height="700" alt="image" src="https://github.com/user-attachments/assets/a21607b4-2365-45e3-99bb-94f398035499" />

Obs: RBAC, esse termo é importante para nossa administração e porque?

RBAC é a sigla para Role-Based Access Control (Controle de Acesso Baseado em Função), uma abordagem para gerenciar permissões em sistemas de TI, na qual o acesso é atribuído a funções, e não a usuários individuais. As funções, como "financeiro" ou "desenvolvedor", representam cargos e conjuntos de permissões, e os usuários são designados a essas funções para determinar o que podem ver e fazer no sistema. 

Como funciona
1. Definição de Funções:
A organização define funções que correspondem aos cargos ou responsabilidades dentro da empresa, como administrador, usuário de vendas, analista financeiro, etc. 
2. Atribuição de Permissões:
Cada função é associada a um conjunto específico de permissões, como "visualizar", "editar" ou "excluir" dados, e acesso a determinados recursos ou funcionalidades do sistema. 
3. Atribuição de Usuários a Funções:
Usuários são designados a uma ou mais funções, herdando as permissões associadas a essas funções. 

Vantagens do RBAC
Segurança Aprimorada:
Garante que os usuários só tenham acesso às informações e funcionalidades necessárias para suas funções, seguindo o princípio do privilégio mínimo e reduzindo riscos de segurança. 

Gerenciamento Simplificado:
Em vez de configurar permissões para cada usuário individualmente, os administradores gerenciam permissões através das funções, o que facilita a administração em ambientes com muitos usuários. 

Hierarquia Clara:
Reflete a estrutura de uma empresa, definindo níveis de acesso distintos para diferentes cargos.

Defender for Cloud

Eu consigo através do Defender for Cloud no Azure, configurar minhas contas de outros Cloud Provider para monitorar e proteger.

<img width="939" height="896" alt="image" src="https://github.com/user-attachments/assets/cac3dc60-804b-4913-b901-2d5420a82db0" />

Podemos também conectar a conta do Devops, Github, Gitlab e o Defender for cloud irá monitorar os códigos executados, temos um painel de alertas e podemos configura-los para envio de e-mail, notificações no teams, o que fizer sentido para minha empresa.

<img width="950" height="896" alt="image" src="https://github.com/user-attachments/assets/1bcfe723-1746-4ba2-88fb-019c903c6e7a" />

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------

O tema da vez foi o Azure Pricing Calculator

Com a calculadora do Azure, é possível simular cenários e comparar o ambiente Onpremise com o ambiente cloud e ter uma estimativa de valor, aproximado do custo real. A ideia é poder ter um valor X para estimativa de custo.

<img width="1271" height="943" alt="image" src="https://github.com/user-attachments/assets/aead6449-7fc7-42b3-98ae-7ec94c187b18" />

Abaixo está um exemplo de simulação de uma máquina virtual.

<img width="1270" height="944" alt="image" src="https://github.com/user-attachments/assets/0ddb86da-198e-4cf4-8237-e6e6a0c5bedf" />

O que eu posso simular custos?
- Produtos
- Cenários de exemplo
- Posso salvar estimativas

Existe também a aba de FAQ onde há perguntas frequentes sobre a calculadora.

Obs:
- Se eu reservar minha máquina por 1 a 3 anos o valor será alterado
- Caso eu altere de licença para Azure Hybrid, o valor é alterado também
- Economizar horas de uso na opção pague conforme o uso, gera também economia

<img width="1238" height="816" alt="image" src="https://github.com/user-attachments/assets/ef2c7e3a-d02e-4b23-8292-e269d375fa30" />


Obs: Inserir tags para marcar os recursos e o resources groups, os recursos não herdam as tags dos resources groups.
Isso serve para organização e definir centro de custos para na hora do pagamento identificar com facilidade da onde esses custos sairam.

----------------------------------------------------------------------------------------------------------------------------

O foco agora é a governança, então, o objetivo é a criação de politicas, que é aplicada para gestão de recursos e ela depende de quem está tentando manipular esses recursos, idependente de quem seja, administrador ou não.

<img width="953" height="896" alt="image" src="https://github.com/user-attachments/assets/8dc16060-35a2-43d4-8b3f-23b315f4e785" />

É possível usar templates de politicas e modifica-las conforme a minha necessidade.

Um resource group, quando criamos uma politica para ele, essa politica é herdada pelos meus itens do grupo de recursos, porém caso o eu movimente esse recurso, a politica não seguirá junto com a movimentação.

<img width="940" height="890" alt="image" src="https://github.com/user-attachments/assets/7b9ceafa-6165-4121-a48c-ef042b2140cd" />

Também falamos aqui sobre o Purview, que em conjunto com o 365, é um conjunto de ferramentas, uma switch de aplicações, com foco em compliansive e governança.
Focado em administrar dados não só o Azure, mas de recursos fora do Azure também, temos várias soluções agrupadas por plataformas.

<img width="940" height="682" alt="image" src="https://github.com/user-attachments/assets/567f4182-3b37-4528-aabe-2387550dca17" />

- Capturar mensagens impróprias pra mitigar riscos
- Compliance Manager
- Records Management (Valida se existe gravações de dados, em reuniões, eventos)
Para esse caso em especifico, é necessário uma licença E5 para uma experiência mais completa. 

Priva
Parceria com o Purview, o Priva ajuda com o regulatório, dizendo aonde não está atendo os requisitos, como por exemplo a LGPD, ajudando e apoiando aonde a minha empresa não está cumprindo com os requisitos.

----------------------------------------------------------------------------------------------------------------------------

Ferramentas para interagir com o Azure

- Portal do Azure
- Azure PowerShell
- Azure Cloud Shell
- Interface de linha de comando (CLI)
 
<img width="951" height="557" alt="image" src="https://github.com/user-attachments/assets/e5b776f3-9dc4-4b04-9dd7-975d423a27b0" />

Posso usar qualquer uma delas, depende de qual estou mais familiarizado, todas vão ter a mesma função de ajuda.

Azure ARC
Uma ferramenta disponível no Azure, idependente da assinatura, ele tem modelos peculiares, ele segue um modo de boot cloud, para gerenciar recursos que não estão dentro do Azure.
Nesse necessário, é possível executar um script nas minhas máquinas, para fazer a gestão do equipamento via Nuvem, abrindo possíbilidade de trabalhar fora do ambiente OnPremise, possibilidade de gerenciar tudo em um unico portal, painel unico de gerenciamento e uma visualização de segurança e conformidade.

<img width="932" height="903" alt="image" src="https://github.com/user-attachments/assets/1afdb71c-66f8-4b79-bf69-ae53b0746fd1" />

É possível adicionar uma máquina AWS e aplicar policias nativas da Microsoft, o ARC é para administrar o que está fora do Azure, até o momento, não temos outra aplicação equivalente em outros providers.

ARM Azure Resource Manager
Cria uma camada de gerenciamento que permite criar, atualizar e excluir recursos da assinatura do Azure.
Arquivos JSON.

Bicep
Linguagem exclusiva da Microsoft, para criação de recursos no Azure, voltados a automação de recursos, ele vem pra facilitar a vida de quem está aprendendo a automatizar recursos, e funciona em conjunto com o ARM.
É uma linguagem específica de domínio (DSL) que usa sintaxe declarativa para implantar recursos apenas dentro do Azure.

Em automação da VNET como exemplo, ele me trás o modelo de comando de acordo com o modo que eu selecionar, CLI ou PS, ele muda a sintaxe, mas o resultado é o mesmo, a mesma estratégia.
Temos mais de uma forma de fazer a mesma coisa.

<img width="827" height="233" alt="image" src="https://github.com/user-attachments/assets/bb30eff2-486e-4c9e-96e4-a6b08e361a25" />

Modelo JSON de criação de uma VNET.
<img width="683" height="520" alt="image" src="https://github.com/user-attachments/assets/79518c68-a2d4-48b2-9d3a-9cf0a33e40a4" />

---------------------------------------------------------------------------------------------------------------------------

Ferramentas de monitoramento

- Assistente do Azure
- Integridade do Serviço do Azure
- Azure Monitor

O Assistente do Azure, Advisor é uma ferramenta Cloud Native, que nos ajuda a gerenciar nossos recursos, ele faz recomendações de custo, entre outras, com base nas práticas recomendadas para otimizar as implantações do Azure.
5 tópicos importantes:
- Confiabilidade
- Segurança
- Desempenho
- Custo
- Excelência operacional
<img width="954" height="903" alt="image" src="https://github.com/user-attachments/assets/64d871aa-995b-47e1-ad46-5872680113e9" />

A integridade do serviço Azure é uma coleção de servições que te mantêm informado sobre o status geral do Azure, de serviços que podem afetar você e o status do recurso específico que está te afetando.
Como exemplo, uma movimentação de rack para manutenção da Microsoft, onde ela te comunica antes e recomenda que você movimente os recursos para que não tenha uma indisponibilidade.
<img width="1919" height="902" alt="image" src="https://github.com/user-attachments/assets/a49b26dc-6815-46d6-bdb6-bde7618aac99" />

Azure Monitor maximiza a disponibilidade e o desempenho de aplicativos e serviços, coletando, analisando e tomando decisões com base na telemetria da nuvem e de ambientes locais.

<img width="949" height="896" alt="image" src="https://github.com/user-attachments/assets/2f3c97d9-9bc2-46a2-a4a3-bb58f05e3402" />
<img width="951" height="903" alt="image" src="https://github.com/user-attachments/assets/a56b3597-a1b0-4bba-a8b0-922c3e14c11c" />






