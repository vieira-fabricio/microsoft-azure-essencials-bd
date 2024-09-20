# Resumo do Lab - Configurando uma Instância de Banco de Dados na Azure
#### Neste lab, aprendemos a criar e configurar uma instância de banco de dados no Microsoft Azure. Este desafio tem como objetivo proporcionar uma experiência prática no uso do Azure SQL Database, uma solução gerenciada de banco de dados em nuvem.


### O que é o Azure SQL Database?

O **Azure SQL Database** é um serviço de banco de dados relacional oferecido pela Microsoft Azure, que utiliza o mecanismo do Microsoft SQL Server. Trata-se de um serviço gerenciado na nuvem, no qual o Azure cuida da manutenção de hardware, atualizações, backups automáticos, escalabilidade e recuperação de desastres, permitindo que você se concentre no desenvolvimento de suas aplicações sem se preocupar com a infraestrutura subjacente.

Ele oferece alta disponibilidade, segurança integrada e suporte a diferentes cargas de trabalho, desde aplicativos pequenos a grandes sistemas empresariais. Também possui recursos de otimização de desempenho e análise inteligente, tornando-o ideal para aplicações modernas e escaláveis.

---

### Passo a Passo para Configurar uma Instância do Azure SQL Database

#### 1. **Acessar o Portal do Azure**
   - Acesse o [Portal do Azure](https://portal.azure.com/).
   - Faça login com suas credenciais.

#### 2. **Iniciar a Criação do Banco de Dados**
   - No painel de navegação à esquerda, clique em **Criar um recurso**.
   - Na barra de pesquisa, digite **SQL Database** e selecione a opção **SQL Database** nos resultados.
   - Clique no botão **Criar**.

#### 3. **Configurar os Detalhes do Banco de Dados**
   - **Assinatura**: Escolha a assinatura do Azure que você deseja usar.
   - **Grupo de Recursos**: Selecione um grupo de recursos existente ou crie um novo, para organizar seus recursos do Azure.
   - **Nome do Banco de Dados**: Defina um nome único para o banco de dados.
   - **Servidor**: 
     - Se você já tem um servidor SQL no Azure, pode usá-lo.
     - Caso contrário, clique em **Criar novo servidor** e configure os seguintes parâmetros:
       - **Nome do Servidor**: Defina um nome exclusivo para o servidor SQL.
       - **Login de Administrador**: Insira o nome de usuário do administrador.
       - **Senha do Administrador**: Defina uma senha forte para o administrador.
       - **Região**: Escolha a região geográfica onde o servidor será hospedado.

#### 4. **Selecionar o Nível de Desempenho**
   - Escolha o plano de desempenho e escalabilidade do banco de dados. As principais opções são:
     - **Serviço baseado em DTU** (Database Transaction Unit): Com foco em cargas de trabalho previsíveis.
     - **Serviço baseado em vCore**: Flexível para ajustar o número de CPUs virtuais e a quantidade de memória conforme suas necessidades.
   - Escolha o tamanho de armazenamento que deseja alocar para o banco de dados.

#### 5. **Configurar a Redundância de Backup**
   - Selecione a opção de redundância do backup:
     - **Redundância Local**: Mantém os backups em uma única região.
     - **Redundância Geográfica**: Replica os backups em múltiplas regiões para maior resiliência.

#### 6. **Configurar Opções Adicionais (Opcional)**
   - **Segurança e Rede**: Defina se o banco de dados poderá ser acessado pela internet pública ou apenas de redes privadas, como através de uma **Rede Virtual**.
   - **Auditoria e Segurança Avançada**: Ative o **Auditing** e a **Proteção contra Ameaças** para monitorar e proteger seu banco de dados contra acessos maliciosos.

#### 7. **Revisar e Criar**
   - Revise todas as configurações na página final.
   - Clique em **Criar** para iniciar a implementação da instância do banco de dados.
   - A criação da instância pode levar alguns minutos.

#### 8. **Conectar ao Banco de Dados**
   - Após a implantação, vá até o painel do **SQL Database** e selecione o banco de dados criado.
   - Clique em **Configurações de Conexão** e permita o acesso de endereços IP que precisarão se conectar ao banco de dados.
   - Utilize ferramentas como **SQL Server Management Studio (SSMS)** ou **Azure Data Studio** para conectar-se ao banco de dados. Para isso, você precisará:
     - Nome do servidor (disponível no portal do Azure).
     - Nome de usuário e senha do administrador SQL configurados anteriormente.

---

#### Conclusão
Durante este lab, aprendemos a configurar uma instância de banco de dados no Azure SQL Database, cobrindo desde a criação do banco até a configuração de segurança e conexão. Esse serviço é essencial para quem deseja hospedar bancos de dados relacionais de forma gerenciada e escalável na nuvem.
