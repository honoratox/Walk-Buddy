# Walk Buddy - Especificação dos Requisitos do Software

## Introdução

O Walk Buddy é um aplicativo desenvolvido para facilitar a vida de donos de pets que desejam passear com seus animais, mas enfrentam limitações de tempo. A interação acontece entre usuários cadastrados como passeadores e donos de pets.

## Figma

Acesse o [protótipo do aplicativo no Figma]([https://www.figma.com/file/fX998ysTIxmYx8jaSuDbZk/Walk-Buddy?type=design&node-id=0-1&mode=design&t=Alj65H2E1sFbetOa-0]).

## Requisitos Funcionais (RFs)

| Código | Nome               | Descrição |
|--------|--------------------|-----------|
| RF01   | Cadastro do dono   | O usuário deve poder se cadastrar no app com informações básicas, como nome, e-mail, telefone e endereço. |
| RF02   | Pesquisa de passeadores | O usuário deve poder pesquisar passeadores por localização, preço, horário e outros critérios. |
| RF03   | Registro de passeio | O usuário deve poder agendar passeios com passeadores diretamente pelo app. |
| RF04   | Realizar pagamento | Pagamento de forma virtual, por Pix ou cartão de crédito. |
| RF05   | Avaliação de passeadores | Deverá ser feita pelo dono do pet após o pagamento, num prazo de 4 dias. |
| RF06   | Cadastro de pet | Para cada pet, deve-se submeter informações como nome, idade, vacinação, doenças e perfil comportamental. |
| RF07   | Cadastro do passeador | Cada passeador deve possuir em seu cadastro: nome, idade, região de atuação. |
| RF08   | Chat entre passeador | Deverá ser feito após a confirmação do passeio. |
| RF09   | Exibir notificações | Deverá notificar qualquer tipo de evento, tanto engatilhado pelo passeador quanto pelo dono do pet. |
| RF10   | Exibir mapa de passeios | O itinerário do passeio fica à disposição do dono do pet. |
| RF11   | Rastreamento do pet | O passeador deve ativar a localização durante o passeio, para o dono poder rastrear seu pet. |
| RF12   | Visualizar cachorro | O passeador pode visualizar o perfil do cachorro com o qual irá passear. |
| RF13   | Alterar status do passeio | O passeador confirma que iniciou, finalizou ou cancelou o passeio. |

## Requisitos Não Funcionais (RNFs)

| Código | Classificação | Descrição |
|--------|---------------|-----------|
| RNF01  | Externo       | O sistema de pagamento será integrado com a stripe. |
| RNF02  | Produto       | Disponível para iOS e Android. |
| RNF03  | Organizacional | O sistema vai ser desenvolvido em Flutter. |
| RNF04  | Produto       | Tempo de resposta da API. |
| RNF05  | Produto       | O sistema deve possuir disponibilidade 24/7. |
