# superheroworld
A java console game

This is a basic console application game. The below points summarises the current capabilities.  

- As a player I can create a character
  - User given options to enter the player name and create a player
 - As a player I can explore
    - User gets option to explore different worlds(eg Earth, Atlantis)
- As a player I can gain experience through fighting
    - Options to fight below opponents in corresponding world(eg Ultron in Earth, Loki in Asgard)
    - Once you fight experience increases
- As a player I can save and resume a game
    - option to save game any time
    - Reload saved game on start up

### How to run
 - build using `mvn clean package`
 - run using `java -jar target/super-hero-world-1.0.0-SNAPSHOT.jar` (_snapshot version to be updated as per pom_)

### Design Principles
 - Programming to interface has been followed through out for extensibility.
 - Application uses **command design pattern** to run various game operations
 - Command creation is via command factory.
 - The project uses **Factory Design Pattern**, **BuilderPattern** and **Singleton Pattern** for object creation
 - Opponent and Player Fight are controlled by **StrategyPattern**
 - Terminal interface implementation controls all read and write to console
 - UI components are packaged in `ui` package.
 
#### Test coverage
 The project uses jacoco for creating test reports.
 The report will be generated once you run `mvn clean package` or `mvn test`
 You can find the report at `target/site/jacoco/index.html`   
 
#### Logging
 Basic java logging has been provided. The log file can be found at `src/main/resources/game_application.log`
 
#### Sonar
 Sonar can be run in local ( _set up sonar in local - https://docs.sonarqube.org/latest/setup/get-started-2-minutes/_) by executing below command. 
 `mvn sonar:sonar -Dsonar.host.url=http://localhost:9000`

#### Screenshots
- Start Game
  ![Start Game](src/main/resources/screenshots/StartGame.png "Start Game")
- Create Player
  ![Create Player](src/main/resources/screenshots/CreatePlayer.png "Create Player")
- SelectWorld
  ![Select World](src/main/resources/screenshots/SelectWorld.png "Select world")
- Select Opponent  
  ![Select Opponent](src/main/resources/screenshots/SelectOpponent.png "Select Opponent")
- Fight Opponent
  ![Fight Opponent](src/main/resources/screenshots/FightOpponent.png "Fight Opponent")
