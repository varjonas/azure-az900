Olá,

Nesse módulo de introdução, foi realizado um overview da plataforma, onde a explicação foi visual e sobre as funcionalidades do Azure.
O Azure separa por categorias as funções exibidas, como introdutório, a categoria computação contém a área de trabalho virtual do azure e até mesmo as máquinas virtuais.

Com relação a redes, explicado sobre os Bastions, que seria um acesso seguro as máquinas virtuais, explicado pela Valeria que o mesmo operaria como um Jump server.
Toda configuração de rede também é possível ser feita nessa camada, como Firewall, DNS, TCP/IP e Gateway.

De maneira geral, a introdução explicou como funciona o Azure, pra que e por quê utilizar o Azure, as diferenças de um ambiente em Cloud e OnPremise.


------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Criação de máquinas virtuais

Para criar uma máquina virtual, devemos verificar a disponibilidade da região e também o custo ao qual o equipamento irá gerar, o custo pode variar de acordo com o tempo de uso e os recursos a serem utilizados.
A máquina abaixo, foi criada para teste, o acesso é feito via RDP na porta 3389 de forma pública, foi utilizado a imagem do Windows Server 2025.
É possível personalizar a configuração da máquina, sendo para discos, rede ou memória por exemplo, isso também afetará no valor.

Importante verificar a disponibilidade da região e o valor da VM também pode ser alterado de acordo com a região, determinadas configurações/imagens podem não estar disponíveis de acordo com a licença do Azure e também a região.

<img width="1919" height="1029" alt="Captura de tela 2025-09-06 083823" src="https://github.com/user-attachments/assets/831f0327-f7ea-4736-a780-704844a84173" />

O custo dessa VM também foi realizado e ficou em 0,1880USD/hora ou por volta de 137$ por mês;

<img width="1070" height="373" alt="image" src="https://github.com/user-attachments/assets/e4cad87d-4bc8-4853-94de-a73fc72e45b9" />

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Criação de um banco de dados SQL

É possível também fazer essa criação e para isso vamos precisar criar um servidor na aba de criação de banco de dados, esse server não precisa ser acessado, será usado para armazenamento do nosso bd.
Aqui também é necessário verificar a redundância do armazenamento e isso pode ser feito local, por zona, por redundância geográfica ou por zona geográfica. Cada uma das opções escolhidas pode afetar o custo final, e para testes, o bd criado ficou em 0.12USD por GB usado, o banco foi criado com 32GB.
<img width="804" height="358" alt="image" src="https://github.com/user-attachments/assets/17d33c2c-a936-4335-a536-ea8ab6bdbec7" />

O custo estimado para o mês é de 3,68USD.

<img width="1042" height="706" alt="image" src="https://github.com/user-attachments/assets/6a4d2bde-7506-4c00-9c6c-02b8e2fd5d18" />


