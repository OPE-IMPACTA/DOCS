# Lista de Características
### (Priorizada x Esforço x Risc x Baseline)

Legenda:

    (P): Prioridade da característica definida pelo cliente.

    (C): Crítica (não tem sentido desenvolver esta versão do sistema sem esta característica)

    (I): Importante (podemos conviver sem esta característica nesta versão do sistema)

    (U): Útil (esta característica pode ser útil, mas não fará falta nesta versão do sistema)

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

| # | Nome | Descrição | (P) | (E) | (R) | (B)
:----|:-----|:----|:----:|:----:|:----:|:----:|:----:
| 01 | Login | Controle de acessos do sistema | C | M | B | 1 |
| 02 | Controle de ponto | Registros de entrada e sáida dos funcionários | I | B | M | 2 |
| 03 | Atividades | Registro das atividades dos funcionários | C | A | M | 1 |
| 04 | Clientes | Registro dos clientes da empresa | C | M | B | 1 |
| 05 | Usuários | Registro de todos os usuários - que também são funcionários da empresa | C | A | M | 1 |
| 06 | Projetos | Registro de todos os projetos da empresa por cliente | C | M | B | 1 |
| 07 | Módulos | Registro de todos os modulos de cada projeto | C | M | M | 1 |
| 08 | Horas | Registro de horas trabalhadas de cada funcionário. | C | A | M | 1 |
| 09 | Relátório |  Junção dos dados de horas trabalhados por projeto de cada cliente que será gerado | C | A | M | 1 |
| 10 | Rewards | Cálculo de bonificação para horas poupadas no projeto | I | M | M | 2 |
| 11 | Admin | Página desenvolvida específicamente para a administração da empresa | U | A | M | 2 |
| 12 | Nota fiscal | Função para emição de nota fiscal para os clientes | I | A | A | 3 |
| 13 | Horas contratadas | Registrar por módulo o quanto de horas o cliente contratou para controle | I | M | M | 2 |
| 14 | Aviso de Horas Extras | Alertar a empresa quando o as horas trabalhadas em módulo de um projeto exceder as horas contratadas |  |  |  |  |