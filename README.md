# 🏆 Gestor de Clube Desportivo (Web App Universal)

Esta é uma aplicação web completa (HTML, CSS, JS puro) para gerir um grupo desportivo amador. É totalmente adaptável a qualquer desporto e clube, permitindo a gestão de jogadores, estatísticas avançadas de desempenho, formação automática de equipas (sorteios) e tesouraria completa.

A aplicação funciona inteiramente no browser e guarda a base de dados no armazenamento local do teu dispositivo (`localStorage`), garantindo rapidez extrema e total privacidade (offline-first).

## 📂 Estrutura de Ficheiros Necessária
Para que a aplicação funcione corretamente no teu computador ou quando a alojares na internet (ex: num servidor ou GitHub Pages), a pasta do projeto deve ter a seguinte estrutura:

```text
/a-tua-pasta-do-projeto
│
├── index.html               # O código principal da aplicação
├── logo.jpg                 # O logotipo do teu clube (aparece no topo da app)
├── elementos_clube.xlsx     # A base de dados Excel inicial com os atletas
│
└── /fotos                   # Pasta (opcional) com as fotos dos jogadores
    ├── joao.jpg
    ├── mario.png
    └── …



⚙️ 1. O Ficheiro Excel (elementos_clube.xlsx)
O ficheiro Excel serve para carregar a base de dados de atletas inicial para a aplicação. A aplicação requer que as colunas tenham os seguintes cabeçalhos exatos na primeira linha:

NOME: Nome do atleta (Ex: João Silva).

DATA NASCIMENTO: Data de nascimento (Ex: 01/05/1990) - A app calcula a idade automaticamente.

ESTATUTO: Define o tipo de pagamento. Ex: Mensalidade, Por Jogo ou Convidado.

CONTACTO: Número de telemóvel para os atalhos automáticos do WhatsApp (Ex: 912345678).

NÍVEL: Número de 1 a 5 (onde 5 é o melhor). Este número fica invisível na aplicação e serve apenas para o algoritmo equilibrar as equipas no Sorteio Automático.

FOTO (Opcional): O nome do ficheiro da foto que guardaste na pasta /fotos (Ex: joao.jpg). Se deixares em branco, a app gera um avatar com a inicial do jogador.

🚀 2. Como Inicializar a App
Abre o index.html no teu browser (Safari, Chrome, Firefox).

Na primeira utilização, a aplicação vai pedir-te o Nome do Clube. Este nome vai personalizar toda a interface, os relatórios em PDF e as mensagens automáticas de WhatsApp, tornando a app tua.

No separador "Equipa", clica em "+ Atualizar Tabela Excel" e seleciona o teu ficheiro elementos_clube.xlsx. Os jogadores aparecem imediatamente no ecrã.

📊 3. Funcionalidades Principais
Aba: Equipa (Estatísticas Avançadas e Desempenho)
Cada atleta possui um cartão individual onde podes ver o seu saldo financeiro e as suas estatísticas de época calculadas em tempo real:

Presenças, Golos e AG (Auto Golos).

Pts/Rank: Sistema de Ranking competitivo (Vitória = 3 pontos, Empate = 1 ponto, Derrota = 0 pontos).

IF (Índice de Frequência): Percentagem de assiduidade do jogador face ao total de jogos oficiais que o clube realizou na época.

IV (Índice de Vitórias): Percentagem de sucesso (vitórias) face aos jogos em que o atleta efetivamente participou.

Exportação: Gera e descarrega um PDF com o Ranking da equipa (ordenado por Pontos), ou partilha a classificação automaticamente via WhatsApp.

Aba: Sorteio & Jogo (Gestão de Plantel)
Sorteio Inteligente: A aplicação cruza o nível invisível de cada atleta selecionado e gera equipas ("Azul" e "Vermelha") perfeitamente equilibradas, listadas por ordem alfabética.

Drag & Drop e Bancada: Arrasta jogadores de uma equipa para a outra ou coloca-os nos "Ausentes (Bancada)" se faltarem à última da hora.

Convidados Extra: Adiciona convidados (com nível personalizado) a qualquer momento.

Registo de Jogo: Inseres o resultado global (Ex: Azul 4 - 3 Vermelha) e os golos/auto golos individuais. A app valida as contas e atualiza as estatísticas globais e índices de toda a gente com 1 clique.

Máquina do Tempo (Edição/Rollback): Inseriste um resultado ou golos errados? Podes "Editar" um jogo passado ou "Apagar" (❌). A aplicação vai reverter toda a matemática e retirar as presenças, vitórias, derrotas e golos que tinha atribuído aos jogadores nesse dia.

Aba: Finanças (Tesouraria Global)
Painel central "Conta Corrente" com subdivisão de dinheiro físico (Caixa), MB Way e Transferências.

Saldo Inicial (🏦): Permite inserir o dinheiro que o clube já tinha em caixa ou no banco antes de começar a usar a aplicação (Transporte de exercício anterior).

Cobranças: Nos cartões de atleta, podes lançar dívidas. Ao registares o pagamento, a app envia automaticamente um Recibo via WhatsApp para o jogador com a referência do mês/jogo e o saldo final atualizado.

Conta Corrente em PDF: Regista despesas/receitas extra e exporta o extrato de um determinado período.

💾 4. Sistema, Segurança e Backups
Privacidade Total: Os dados vivem apenas no teu browser. Não há servidores externos, logo, não há custos de alojamento nem riscos de partilha de dados.

Backup e Restauro (Muito Importante): Como os dados estão no dispositivo, se limpares a cache do browser ou mudares de telemóvel, perdes o histórico. Para evitar isso, no fundo da aba "Finanças" tens uma secção de Segurança:

Clica em "📥 Fazer Backup" para descarregares um ficheiro .json com todos os teus dados, jogos e finanças.

Para recuperar ou mudar de telemóvel, abre a app no telemóvel novo e clica em "📤 Restaurar" enviando esse ficheiro .json.

Formatação Total: O botão "🗑️ Formatar Tudo" apaga completamente a memória da app. Ideal para limpar a casa e começar uma nova época de raiz com toda a equipa a zeros.
