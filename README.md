# projeto_integrador_ti05
Projeto de encerramento do curso técnico de informática da turma 0523, cursado na unidade Tatuapé Cel. Luís Americano.

Projeto Integrador

Participantes:
Kaylane - https://github.com/kaycout
Laís - https://github.com/laisnf
Marcos - https://github.com/Marcos-Kim

Proposta:
Criar um site que receba nomes, com equipe e supervisão, e liste todos esses nomes em uma tabela e faça uma reordenação dessa lista de nomes. O intuito é atender à necessidade de, principalmente, equipes de vendas, que necessitam fazer uma roleta para decidir a ordem de atendimento de seus colaboradores.

Exigências:
•	Deve constar no topo das listas EMPRESA, EMPREENDIMENTO/LOJA/DEPARTAMENTO, a DATA, o PERÍODO (manhã, tarde ou integral) e o botão CRIAR ROLETA;
•	Campos para preenchimento com NOME, EQUIPE e SUPERVISÃO/DIRETORIA;
•	Após clicar no botão ADICIONAR o cursor deve retornar ao campo NOME;
•	Deve ser obrigatório o preenchimento dos campos EMPRESA, EMPREENDIMENTO, DATA e PERÍODO antes de poder seguir adiante;
•	Após a etapa acima, é gerado um QR Code para que outros usuários possam inserir, via smartphone, apenas UM NOME, sua EQUIPE e sua SUPERVISÃO, evitando assim a inserção de participantes não presentes;
•	Para o usuário de QR Code, será apresentada uma tela simples, indicando de qual roleta se trata e os campos para inserir os dados solicitados. Após o envio desses dados, recebe uma confirmação do envio e um aviso para que mantenha a tela aberta, para receber o resultado do sorteio;
•	Deve ser obrigatório o preenchimento dos campos NOME e EQUIPE para ser adicionado à lista;
•	Nenhum NOME pode ser repetido. O sistema deve ignorar diferenciar um NOME em razão de acentuação, letras maiúsculas ou minúsculas e caracteres especiais, como ç e Ç;
•	Caso tentem inserir um NOME que já conste na tabela, o sistema deve informar que já consta tal NOME;
•	Deve ser possível apagar qualquer nome da tabela, sem apagar os demais;
•	Cada linha da tabela deve ser numerada, a fim de contabilizar o número total de participantes da roleta;
•	Deve haver um botão SORTEAR, disponível apenas na tela do usuário administrador/criador da roleta, preferencialmente no desktop;
•	Ao clicar em SORTEAR, deve haver algum tipo de animação por um período de alguns segundos antes da entrega do resultado do sorteio;
•	O resultado deve ser exibido em uma nova tabela, enquanto a tabela original deve ser mantida;
•	Deve ser possível salvar ambas as tabelas em um arquivo PDF, sendo que cada tabela deve estar em uma página diferente, cada uma com linhas e grades separando cada NOME, a fim de facilitar a visualização;
•	Cada participante que inseriu seu nome via QR Code deve receber um aviso com o seu resultado. Também deve haver a opção de baixar as listas em seu smartphone;
•	Na tela do administrador/criador da roleta, deve haver um banner no rodapé da página, destinado a espaço publicitário;
•	Na tela do usuário do QR Code, um espaço publicitário deve ser reservado entre o envio dos dados e a confirmação do recebimento dos dados na lista. Outro espaço publicitário será reservado para antes do download das listas do resultado.

Front-End:

#Tecnologias utilizadas:

Na criação do FRONT-END foram utilizadas apenas as linguagens HTML5, CSS3, JAVASCRIPT e BOOTSTRAP 5.3.2.

#Tela do desktop:

No topo da tela temos o cabeçalho, onde o usuário deve inserir os dados necessários para abrir a roleta e gerar seu ID. Isso evita que participantes de outros sorteios simultâneos sejam erroneamente adicionados a outros sorteios.
![Captura de Tela (80)](https://github.com/user-attachments/assets/814118d1-7630-4956-b634-5f184e3af575)

Após clicar em CRIAR ROLETA, é gerado um ID e também um QR Code que direciona os usuários mobile para a página de participação correspondente a esse sorteio.
O corpo principal da página foi dividido em 3 colunas; a primeira é para listar os participantes, a segunda é para adicionar os participantes e a terceira é para o resultado do sorteio.
Por fim, no rodapé da página fixamos uma área para banners publicitários, através dos quais vamos monetizar a ferramenta, pois ela é gratuita para os usuários.
 ![Captura de Tela (86)](https://github.com/user-attachments/assets/f4a7e172-7d63-4e63-9eaa-7808713fc5ab)


#Telas do celular:

•	A primeira tela deve exibir EMPRESA, EMPREENDIMENTO, DATA e ROLETA (com o período já selecionado. E logo abaixo os campos NOME, EQUIPE e SUPERVISÃO para serem preenchidos, além do botão ENVIAR;
![mob1](https://github.com/user-attachments/assets/6ab01bbf-23b6-4015-b55f-7482162ef27f)

•	No caso de duplicidade de participante, haverá uma tela informando que não foi possível inserir o participante em razão dessa duplicidade;
![mob2](https://github.com/user-attachments/assets/7589889c-9e26-4de8-85a9-eef40902bf72)

•	Estando tudo ok, entra uma tela de anúncio e sequencialmente entra uma nova tela;
•	Após a tela de publicidade, é carregada uma tela de espera, que informa ao participante para aguardar o resultado do sorteio; 
![Imagem1](https://github.com/user-attachments/assets/23449392-687d-4155-aed5-aa6bbb82b02c)

•	Após o sorteio, cada participante que entrou pelo QR Code deve receber uma mensagem em uma nova tela indicando sua posição sorteada (“Parabéns! Você está na XX posição. Boa sorte!”). Logo abaixo, perguntamos “Gostaria de salvar uma cópia da lista sorteada?” e oferecemos 2 botões: SALVAR e outro botão SAIR;
![mob4](https://github.com/user-attachments/assets/35b96f14-8c89-4849-9b1b-f0dd7e70c266)

•	Se o usuário clicar em sair, a janela muda para “Obrigado” e acabou. Mas se clicar em SALVAR, uma nova tela de anúncio se abre e depois o arquivo em formato PDF com as listas é enviado, encerrando a operação de nossa parte.
![mob3](https://github.com/user-attachments/assets/7a4ac668-c52d-471e-8e1b-3ac113869625)


CRIAÇÃO DO BANCO DE DADOS DA ROLETA – P.I

# Contexto

• Para o nosso Projeto Integrador, cujo tema trata-se de uma roleta para ser usada em estabelecimentos, foi criado um banco de dados chamado roletadb.
• Logo em seguida, para a estrutura do banco de dados da roleta, foi pensado e definido algumas das identidades principais, sendo elas;
1. Empresa
2. Participante
3. Participante Mobile
4. Participante sorteio
5. Sorteio
6. Resultado
7. Uploads
8. QR Code
9. Publicidade - Para anúncios que serão exibidos no site.
10. Arquivos
11.Configuração do sorteio - Caso haja alguma alteração da roleta.
12.Caso haja necessidade – Configurações do Sorteio (para futuras personalizações e novas animações) essa entidade ajuda.
                                                                          
# Modelo Conceitual

Definição das entidades do banco de dados.
![modelo-conceitual-roleta-atualizada](https://github.com/user-attachments/assets/ab2203cd-dc35-4891-a426-e0f2e0892ab6)

## MODELAGEM BANCO DE DADOS

A modelagem do banco de dados foi feita a partir da definição das entidades, pensando nisso, foi realizado o modelo lógico juntamente com as normalizações, sendo eles todos os atributos necessários para o banco de dados.

# Modelo Lógico com as normalizações
![normalizacao-livre-atualizada2 0](https://github.com/user-attachments/assets/869cd9d3-6216-41e6-8d99-28b13149e351)

## 1 Normalização
![primeira-normalizacao-atualizada2 0 (1)](https://github.com/user-attachments/assets/45a239c1-dce6-40e9-9c1e-a7b064c1214d)

## 2 Normalização
![segunda-normalizacao-atualizada2 0 (1)](https://github.com/user-attachments/assets/025eed28-5265-4bc1-bc3c-08790eff953d)

## 3 Normalização-a
![terceira-normalizacao1](https://github.com/user-attachments/assets/6e5fd212-779d-44b0-be60-36387db0600a)

## 3 Normalização-b
![terceira-normalizacao2](https://github.com/user-attachments/assets/77666d44-0dd3-48dd-a999-a390ce0754f6)

## 3 Normalização-c
![terceira-normalizacao3](https://github.com/user-attachments/assets/443ad1a9-9f63-4fa2-8b44-a3f8a510b0b3)


# MODELO FISICO - Banco de dados
### Código escrito em sql
![Captura de Tela (62)](https://github.com/user-attachments/assets/01893156-33c1-4cf2-9cee-80365e3c6efb)


## Modelo de Entidade Relacional

#### Diagrama do relacionamento - ROLETA
![modelo-relacional-atualizado2 0](https://github.com/user-attachments/assets/caf71fe4-a76b-4eba-9357-9c784b1af1ed)

# API Roleta de Equipes
API back-end desenvolvida utilizando **Node.js**, **Express** e **MySQL** para gerenciar dados de participantes, empresas e sorteios. O objetivo principal é automatizar, facilitar e organizar o processo de sorteio de equipes de vendas.

## Tecnologias Utilizadas

- **Node.js**: Ambiente de execução JavaScript.
- **Express**: Framework para Node.js para construção de APIs.
- **MySQL**: Banco de dados relacional.
- **Multer**: Middleware para manipulação de uploads de arquivos.
- **Bcrypt**: Biblioteca para criptografia de senhas.
- **PDFKit**: Biblioteca para geração de arquivos PDF.
- **csv-parser**: Leitor de arquivos CSV.
- **xlsx**: Manipulação de arquivos Excel.

Funcionalidades / Como utilizar o sistema:
1.	Deve-se preencher todos os campos do cabeçalho e então clicar em CRIAR ROLETA;
2.	Insira os participantes através da coluna do meio ou;
3.	Escaneie o QR Code com um celular e adicione um participante através da página mobile;
4.	Após todos os participantes do sorteio terem sido adicionados (verifique através da coluna da esquerda), clique em SORTEAR;
5.	Aguarde pelo resultado;
6.	O resultado geral será apresentado na coluna da direita no desktop;
7.	O resultado individual de cada participante via mobile será informado em uma nova tela;
8.	Se desejar, uma cópia em PDF poderá ser baixada em ambas as plataformas.
