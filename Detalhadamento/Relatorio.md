1. Descrição do Projeto
O StartupGame é um simulador de rodadas de decisões para startups, onde o jogador gerencia indicadores como caixa, reputação, receita e moral ao longo de várias rodadas, aplicando estratégias fundamentadas em POO e padrões de projeto. O sistema conta agora com automação de jogadas (bot) e exportação dos resultados para relatório CSV.

2. Itens obrigatórios implementados
 Separação de responsabilidades: Classes divididas por pacote (domínio, engine, ações, relatórios, persistência, interface).

 Leitura de configurações: Uso do game.properties para parâmetros de rodadas e decisões.

 Persistência em banco H2: Startups, rodadas e decisões salvas no banco local, esquema definido em schema.sql.

 Padrão Strategy: Todas as decisões implementadas via Strategy, com fábrica de estratégias.

 Value Objects (VO): Modelagem segura, imutável e validada de Dinheiro, Percentual e Humor.

3. Itens opcionais implementados
 Exportação de relatório CSV: Ao fim do jogo, gera automaticamente relatorio_ranking.csv contendo nome da startup, caixa, receita base, reputação, moral e score final, pronto para análise externa ou entrega.

 Bot automático para decisões: Jogador pode optar por modo automático; Bot toma decisões aleatórias e reproducíveis em cada rodada, permitindo executar partidas sem interação manual. O modo Bot garante resultados determinísticos por uso de seed fixa.

 src/main/java/Main.java                    // Entrada do jogo
src/main/java/ui/ConsoleApp.java           // Interface e lógica do Bot
src/main/java/report/CSVExporter.java      // Exportação de ranking CSV
src/main/java/model/Startup.java           // Modelagem da startup
src/main/java/model/vo/                    // Value Objects (Dinheiro, Percentual, Humor)
src/main/java/engine/                      // Motor do jogo (GameEngine, ScoreService)
src/main/java/persistence/                 // Repositórios, DataSourceProvider
src/main/java/actions/                     // Estratégias de decisão e Factory
src/main/resources/game.properties         // Configuração do jogo
src/main/resources/schema.sql              // Esquema SQL do banco H2

4. Fluxo e Novas Funcionalidades
Ao iniciar, o usuário escolhe entre modo manual ou modo Bot.

Bot toma decisões para as startups de forma automática e informada ao usuário.

Resultados finais (score e indicadores) exportados automaticamente para CSV.

Persistência total dos dados e fácil re-jogo.
