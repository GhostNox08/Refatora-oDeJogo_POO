#StartupGame

Simulação turn-based de rodadas de decisões em startups utilizando Java, Maven, H2, boas práticas de POO e padrões de projeto.

#Sobre o Projeto

O StartupGame é um jogo de simulação onde o usuário gerencia uma startup, toma decisões estratégicas (Marketing, Produto, Equipe, Investidores, Cortar Custos) e acompanha o impacto financeiro, reputacional e motivacional ao longo de várias rodadas.
O score final e o ranking são calculados automaticamente, com persistência dos dados em banco H2.

#Tecnologia Utilizadas

Tecnologias Utilizadas,Java 17,Maven,H2 Database,JUnit 5 (testes),POO avançada,Pattern Strategy, Factory,Repository,Configuração via game.properties

#Como compilar

git clone <URL_DO_REPOSITORIO>
cd StartupGame

Instale as dependências e compile
mvn clean install

mvn exec:java -Dexec.mainClass="Main"
