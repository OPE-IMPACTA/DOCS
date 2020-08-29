# Lista de Características
### (Priorizada x Esforço x Risc x Baseline)

Legenda:

    (P): Prioridade da característica definida pelo cliente.
        C: Crítica (não tem sentido desenvolver esta versão do sistema sem esta característica)
        I: Importante (podemos conviver sem esta característica nesta versão do sistema)
        U: Útil (esta característica pode ser útil, mas não fará falta nesta versão do sistema)
    
    (E): Esforço da característica definido pela equipe de desenvolvimento.
        A: Alto
        M: Médio
        B: Baixo

    (R) Risco da característica não ser implementada dentro do prazo e custo definido pela equipe de desenvolvimento.
        A: Alto
        M: Médio
        B: Baixo

    (B): Baseline
        1: Primeira versão do sistema (contém todas as características críticas, podendo ter algumas características importantes e úteis).
        2: Segunda versão do sistema (contém todas as características Importantes, podendo ter algumas características úteis).
        3: Terceira versão do sistema (contém todas as características úteis).
        4: Quarta versão do sistema (contém todas as características úteis).
        
| # | Nome | Descrição | (P) | (E) | (R) | (B)
|:----:|:-----|:----|:----:|:----:|:----:|:----:|
| 01 | Login | Controle de acesso do usuário. | C | M | A | 1 |
| 02 | Logout | Saída de acesso do usuário. | C | M | B | 1 |
| 03 | Registrar Entrada | Registros de entrada do funcionário. | I | M | B | 1 |
| 04 | Registrar Pausa | Registros de entrada/sáida de pausa dos funcionários. | I | M | B | 1 |
| 05 | Registrar Saída | Registros sáida dos funcionários. | I | M | B | 1 |
| 06 | Selecionar projeto | Selecionar projeto da atividade. | C | M | B | 1 |
| 07 | Criar atividades | Criar uma nova atividade. | | | | |
| 08 | Clientes | Registro de todos os clientes da empresa. | C | B | B | 1 |
| 09 | Usuários | Registro de todos os usuários - que também são funcionários da empresa. | C | A | M | 1 |
| 10 | Projetos | Registro de todos os projetos da empresa por cliente. | C | M | B | 1 |
| 11 | Módulos | Registro de todos os modulos de cada projeto. | I | M | M | 1 |
| 12 | Horas | Registro de horas trabalhadas de cada funcionário. | C | M | B | 1 |
| 13 | Relátório | Junção dos dados de horas trabalhados por projeto de cada cliente que será gerado. | C | M | B | 2 |
| 14 | Rewards | Contagem de bonificação para projetos entregues antes do prazo. | U | M | M | 2 |
| 15 | Admin | Página desenvolvida especificamente para a administração da empresa. | U | M | M | 2 |
| 16 | Emitir Nota fiscal | Função para emição de nota fiscal dos projetos para os clientes. | U | A | A | 3 |
| 17 | Enviar Nota fiscal | Enviar a nota fiscal para o email do cliente. | U | A | A | 3 |
| 18 | Visualizar Nota fiscal | Visualizar nota fiscal. | U | A | A | 3 |
| 19 | Horas contratadas por módulo | Registrar por módulo a quantidade de horas que o cliente contratou. | I | B | B | 1 |
| 20 | Horas contratadas por projeto | Registrar por projeto a quantidade de horas que o cliente contratou. | I | B | B | 1 |
| 21 | Aviso de excedimento de horas 1 | Alertar a empresa quando a quantidade de horas prestadas por módulo exceder. | U | M | M | 3 |
| 22 | Aviso de excedimento de horas 2 | Alertar a empresa quando a quantidade de horas prestadas por projeto exceder. | U | A | A | 3 |
| 23 | Aviso de excedimento de horas 3 | Alertar a gerência quando funcionários excederem a quantidade de horas prestadas no mês. | U | A | A | 3 |
| 24 | Visão do cliente | Página voltada ao cliente para monitoramento de projetos. | U | M | M | 3 |
| 25 | Registrar Pergunta | Registrar pergunta de usuário. | U | M | B | 4 |
| 26 | Registrar Resposta | Registrar resposta para pergunta. | U | M | B | 4 |
| 27 | Encerrar pergunta | Encerrar pergunta realizada. | U | B | B | 4 |
| 28 | Visualização dos lucros | o quanto cada projeto rendeu para empresa (visivel somente para a gerencia). | U | M | M | 4 |
| 29 | Buscar nota fiscal | Pesquisar nota fiscal por numero. | U | A | A | 3 |
| 30 | Calcular gastos | Registrar despesas gerais da empresa. | U | I | I | 4 |