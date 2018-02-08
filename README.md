# Projeto final (2017.2)

Este repositório serve pra descrever o projeto final da disciplina **Práticas de Programação**, no semestre 2017.2. As dúvidas ou ambiguidades sobre a descrição do projeto, devem ser registradas por meio de uma [issue](https://github.com/ads-ifpb-praticas/projeto-20172/issues) com o label `question`.

## Considerações iniciais

O **principal objetivo** do projeto é utilizar todas as ferramentas e técnicas vistas na disciplinas. Este trabalho é **individual**

## Descrição da solução

Deve ser construido uma solução para Salões de Beleza / Barbearias durante este projeto. O principal problema a ser resolvido é o agendamento de horários, evitando que se utilize um sistema por "ordem de chegada", onde os clientes gastam muito tempo esperando para serem atendidos.

## Requisitos

Os requisitos do sistema estão listados abaixo. A grande parte dos requisitos está em aberto, com detalhes que devem ser decididos pela equipe, como por exemplo, quais dados de um cliente devem ser armazenados pelo sistema.

### **RF.01 - Cadastro de clientes**

O sistema deve prover uma maneira dos clientes se cadastrarem para que possam executar as funcionalidades do sistema. É necessário que o cliente informe o **nome completo** obrigatoriamente.

### **RF.02 - Cadastro de atendentes**

O administrador do sistema deve cadastrar os atendentes de um determinado estabelecimento. Neste cadastro deve constar o nome do atendente e uma foto de perfil. Por atendente, entende-se um cabelereiro, um barbeiro, uma manicure, etc.

Os atendentes possuem um ou mais horários de atendimento, levando em conta dia da semana e hora de chegada e saída.

### **RF.03 - Cadastro de serviços**

Ao administrador do sistema, deve ser possível de cadastrar os serviços oferecidos pelo estabelecimento. Exemplos: corte de cabelo masculino, corte de barba comum, desenhada, etc. Estes serviços tem um tempo de duração médio, para que a agenda possa ser preenchida.

Os serviços estão associados a um atendente, uma vez que nem todos os atendentes conseguem executar todos os tipos de serviço.

### **RF.04 - Agendamento de horário**

O agendamento de horários deve ser feito pelos clientes ou pelo administrador do sistema. Deve ser feito de duas maneiras: a partir do serviço a ser feito ou a partir do atendente.

O agendamento por serviço deve mostrar quais os horários de cada atendente que executa aquele serviço, o cliente então deve escolher o horário e o profissional que irá atendê-lo e então confirmar o agendamento.

O agendamento por atendente tem como base apenas os horários disponíveis para o profissional selecionado.

### **RF.05 - Lembrete de agendamentos**

O sistema deve enviar um email para o cliente para informar que o agendamento foi realizado com sucesso, mas apenas para os casos onde o agendamento é feito antecipadamente (mínimo de 1 dia).

### **RF.06 - Controle de fidelidade**

O sistema deve prover funcionalidades básicas para que o administrador possa verificar quem são seus clientes fiéis. As informações que necessitam serem apresentadas são:

- Nomes dos clientes que mais frequentaram o estabelecimento nos últimos meses. A escolha do período deve ser feita pelo administrador, podendo ser no período de 1 mês, de 3 meses ou de 6 meses.

- Nomes dos clientes que mais gastaram com os serviços do estabelecimento nos últimos meses. A escolha do período deve ser feita pelo administrador, podendo ser no período de 1 mês, de 3 meses ou de 6 meses.

### **RF.07 - Confirmação de atendimento**

O administrador do sistema, ao entrar na tela inicial, deve confirmar se os atendimentos que já foram encerrados aconteceram de fato. Apenas os dados dos atendimentos confirmados serão exibidos no controle de fidelidade.

## Entrega

Os artefatos que devem ser entregues obrigatoriamente no dia da apresentação do trabalho (16/04/2018) são:

### 1. Código-fonte do projeto

A versão considerada será a última tag no repositório até a data de entrega. Tags com datas diferentes serão desconsideradas e a nota será zerada.

## Avaliação

O foco da avaliação do projeto estará sobre a utilização correta das ferramentas apresentadas em sala. Uso incorreto/incompleto de alguma ferramenta acarretará perca de pontos.

As ferramentas/técnicas a serem utilizadas são:

- **Git / Github**. Para controlar as versões dos artefatos a serem construídos.
- **Maven**. Para gerenciar o processo de construção dos aplicativos.
- **Log4J**. Para registrar eventos do sistema em logs diversos.
- **Testes**. Será necessário ao menos 50% de cobertura de testes. Os testes a serem verificados serão:
    + **Testes Unitários** (JUnit + Mockito)
    + **Testes de Integração** (DbUnit ou qualquer outro framework a sua escolha)
    + **Testes de Sistema** (Selenium WebDriver)
- **Injeção de Dependências com CDI**.
- **Projeto Arquitetural**.
- **Java Server Faces**. Para a interface gráfica com o usuário
- **Integração Contínua com Jenkins**. As configurações da integração contínua serão feitas em sala de aula.