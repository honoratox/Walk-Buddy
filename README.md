# Walk-Buddy

## Especificação dos Requisitos do Software - ERSw "Walk Buddy"

## Histórico de Revisões do Documento

| Versão | Data       | Descrição                         | Autores                             |
| ------ | ---------- | --------------------------------- | ------------------------------------|
| 1.0    | 31/09/2022 | Criação do documento              | Alexandre, Leonardo, Vinícius      |
| 1.0    | 02/10/2023 | Introdução descrição requisitos   | Alexandre, Leonardo, Vinícius, Pedro|
| 1.0    | 03/10/2023 | Regras de negócio, Stakeholders, Caso de uso, Histórias de Usuários | Alexandre, Leonardo, Vinícius, Pedro|
| 1.0    | 05/10/2023 | Revisão final, Diagrama de Classe | Alexandre, Leonardo, Vinícius      |
| 1.1    | 09/12/2023 | Correção dos erros, Diagrama de atividades | Alexandre, Leonardo, Pedro, Vinícius|

## Sumário

1. [Introdução](#introdução)
    1.1 [Propósito do documento de requisitos](#propósito-do-documento-de-requisitos)
    1.2 [Público-alvo](#público-alvo)
   
3. [Descrição Geral](#descrição-geral)
    2.1 [Situação Atual](#situação-atual)
    2.2 [Restrições de Hardware e Software](#restrições-de-hardware-e-software)
   
5. [Requisitos](#requisitos)
    3.1 [Requisitos Funcionais - RF](#requisitos-funcionais---rf)
    3.2 [Requisitos Não Funcionais - RNF](#requisitos-não-funcionais---rnf)
   
7. [Regras de Negócio](#regras-de-negócio)
    4.1 [Regras de Negócio (RN)](#regras-de-negócio-rn)
8. [Stakeholders](#stakeholders)
    5.1 [Usuários](#usuários)
        5.1.1 [Responsabilidades](#responsabilidades)
    5.2 [Equipe de TI](#equipe-de-ti)
9. [Casos de Uso (CSU)](#casos-de-uso-csu)
    6.1 [Diagrama de Casos de Uso (Use Case Diagram)](#diagrama-de-casos-de-uso-use-case-diagram)
    6.2 [Descrição dos Casos de Uso](#descrição-dos-casos-de-uso)
10. [Diagrama de Classes](#diagrama-de-classes)
    7.1 [Diagrama de classes](#diagrama-de-classes-1)
    7.2 [Descrição das classes](#descrição-das-classes)
11. [Diagrama de Atividades](#diagrama-de-atividades)
12. [Prototipação](#prototipação)
13. [Estimativas de Software](#estimativas-de-software)
    10.1 [Análise Ponto de Função (APF)](#análise-ponto-de-função-apf)
    10.2 [Estimativas](#estimativas-1)

## Introdução

### 1.1 Propósito do documento de requisitos

O documento de requisitos tem como objetivo definir e descrever os requisitos do software "Walk Buddy". Ele serve como guia para o desenvolvimento do aplicativo, proporcionando uma compreensão clara das funcionalidades e restrições associadas.

### 1.2 Público-alvo

O público-alvo deste documento inclui desenvolvedores, analistas de sistemas, testadores, e demais membros da equipe envolvida no desenvolvimento, bem como stakeholders externos interessados nas funcionalidades e características do aplicativo.

## Descrição Geral

### 2.1 Situação Atual

O aplicativo Walk Buddy visa atender à necessidade de donos de pets que buscam passeadores para seus animais de estimação. Proporcionando uma interação entre donos e passeadores, o aplicativo permite agendar passeios, manter comunicação instantânea, rastrear o pet durante o passeio, e avaliar a experiência.

### 2.2 Restrições de Hardware e Software

O aplicativo requer smartphones modernos com capacidade para executar versões IOS-17 ou Android 13 ou superiores.

## Requisitos

### 3.1 Requisitos Funcionais - RF

| Código | Nome                     | Descrição                                                                                                                                                                                                                   |
| ------ | ------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| RF01   | Cadastro do dono         | O usuário deve poder se cadastrar no app com informações básicas, como nome, e-mail, telefone e endereço. Também deve ser possível adicionar informações sobre o cachorro, como raça, tamanho, idade e necessidades especiais.         |
| RF02   | Pesquisa de passeadores  | O usuário deve poder pesquisar passeadores por localização, preço, horário e outros critérios. Os resultados da pesquisa devem ser exibidos de forma clara e concisa.                                                          |
| RF03   | Registro de passeio       | O usuário deve poder agendar passeios com passeadores diretamente pelo app, escolhendo data, hora e duração. O usuário deve receber uma confirmação do agendamento.                                                             |
| RF04   | Realizar pagamento         | Pagamento virtual via Pix ou cartão de crédito.                                                                                                                                                                             |
| RF05   | Avaliação de passeadores | Os donos de pet devem avaliar os passeadores após o pagamento, em um prazo de 4 dias.                                                                                                                                       |
| RF06   | Cadastro de pet           | Informações detalhadas sobre o pet, incluindo nome, idade, vacinação, doenças e perfil comportamental.                                                                                                                       |
| RF07   | Cadastro do passeador     | Cada passeador deve possuir em seu cadastro nome, idade, região de atuação.                                                                                                                                                  |
| RF08   | Chat entre passeador      | Chat instantâneo entre dono de pet e passeador, iniciado após a confirmação do passeio.                                                                                                                                      |
| RF09   | Exibir notificações       | Notificações para eventos, acionadas pelo passeador ou dono do pet.                                                                                                                                                          |
| RF10   | Exibir mapa de passeios    | Mostrar o itinerário do passeio para o dono do pet.                                                                                                                                                                         |
| RF11   | Rastreamento do pet        | Ativação da localização durante o passeio para rastrear o pet. Notificação se o pet sair da rota do itinerário.                                                                                                              |
| RF12   | Visualizar cachorro        | O passeador pode visualizar o perfil do cachorro com o qual irá passear.                                                                                                                                                     |
| RF13   | Alterar status do passeio | Confirmação de início, finalização ou cancelamento do passeio pelo passeador.                                                                                                                                                |

### 3.2 Requisitos Não Funcionais - RNF

| Código | Classificação        | Descrição                                                                                                    |
| ------ | -------------------- | ------------------------------------------------------------------------------------------------------------ |
| RNF01  | Interoperabilidade    | Integração do sistema de pagamento com a Stripe.                                                             |
| RNF02  | Portabilidade         | Disponibilidade do aplicativo para iOS e Android.                                                            |
| RNF03  | Implementação         | Desenvolvimento do sistema em Flutter.                                                                        |
| RNF04  | Desempenho            | Tempo de resposta da API.                                                                                    |
| RNF05  | Confiabilidade        | Disponibilidade do sistema 24/7.                                                                             |

## Regras de Negócio

### 4.1 Regras de Negócio (RN)

| Código | Descrição                                                                                                                         |
| ------ | ----------------------------------------------------------------------------------------------------------------------------------- |
| RN01   | A senha para autenticação deve ter entre 6 e 10 dígitos, contendo pelo menos 1 número, 1 letra minúscula, 1 letra maiúscula e 1 caractere especial. |
| RN02   | Após 3 tentativas mal sucedidas de acesso, a funcionalidade é bloqueada por 2 horas, e um e-mail é enviado ao responsável pela conta.   |
| RN03   | O tempo de passeio requisitado pelo dono do pet não pode ultrapassar 10 minutos do tempo estipulado.                             |
| RN04   | O passeador deve realizar autenticação através de reconhecimento facial e RG.                                                      |
| RN05   | O passeador deve submeter o itinerário antes da confirmação do passeio.                                                            |

## Stakeholders

### 5.1 Usuários

#### 5.1.1 Responsabilidades

- **Donos de Pet (Vinícius)**
  - Responsável por cadastrar seu perfil e o perfil do seu pet.
  - Realizar pesquisas e agendar passeios.
  - Efetuar pagamentos e avaliações.

- **Passeador (Leonardo)**
  - Cadastrar seu perfil e habilidades.
  - Disponibilizar horários para passeios.
  - Manter o aplicativo ativo durante os passeios.
  - Responder a mensagens via chat.
  - Confirmar início, finalização ou cancelamento do passeio.

### 5.2 Equipe de TI
- **Designer (Pedro Honorato)**
 - Responsável pelo design visual e usabilidade do aplicativo.

- **Analista (Vinícius Tavares)**
  - Responsável pela análise e especificação de requisitos.
  - Colaborar na definição de casos de uso e regras de negócio.

- **Programador (Alexandre Jurka e Pedro Honorato)**
  - Responsável pelo desenvolvimento do aplicativo.
  - Implementar os requisitos e funcionalidades especificados.

- **Tester (Leonardo Buldrini)**
  - Responsável por testes de qualidade.
  - Identificar e relatar bugs e problemas de usabilidade.

### 5.3 Demais Stakeholders

| Nome                | Descrição                 | Contato          |
| ------------------- | ------------------------- | ----------------- |
| Petz                | Petshop                   | 37 3234-2001     |
| Impressora Cupom    | Fiscal                    | 37 3333-3333     |

## Casos de Uso (CSU)

### 6.1 Diagrama de Casos de Uso (Use Case Diagram)

[Inserir imagem do diagrama de casos de uso aqui]

### 6.2 Descrição dos Casos de Uso

#### CSU 01: Cadastro do Dono

Como dono de pet, quero me cadastrar no aplicativo para encontrar um passeador para meu pet.

**Ator(es):**
  - Primário: Dono
  - Secundário:

**Pré-condições:**
  - O usuário deve possuir o aplicativo baixado e uma conexão com a internet.

**Prioridade:**
  - Alta

**Fluxo Principal:**
1. O usuário baixa a aplicação.
2. Clica no botão CADASTRO.
3. Seleciona a opção dono de pet.
4. Preenche os dados necessários para criação do usuário.
5. Clica no botão FINALIZAR.

**Fluxo Alternativo:**
- Cadastrar com outra plataforma:
  - O usuário clica no botão cadastrar com outra plataforma.
  - O usuário escolhe a conta para realizar o cadastro e login.
  - O usuário preenche algum campo que não é fornecido pelo método.
  - O usuário clica em FINALIZAR.

**Fluxo de Exceção:**
- Dados inconsistentes:
  - Usuário recebe a notificação que já existe uma conta com o e-mail escolhido ou que algum campo não está condizente com a regra de negócio 01.
  - Usuário tem a opção de mudar o e-mail no cadastro ou realizar o login com aquele e-mail.

**Regras de Negócio:**
- RN 01, RN 02

**Pós-condições:**
  - O usuário foi cadastrado com sucesso.

...

