# Tetris

A desktop Tetris game in Java Swing, built as a university software design project with an MVC architecture.

## Features

- **One or two players:** play solo, or turn on extended mode for two boards side by side
- **Three player types per board:** Human, AI or External
- **AI player:** scores every possible move by stack height, lines cleared, holes and bumpiness, then plays the best one
- **External player:** connects to a Tetris server on `localhost:3000` and plays the moves it sends back
- **Configurable games:** board width and height, starting level, music and sound effects, saved to `TetrisGameConfig.json`
- **High scores:** top scores for single and double games, saved to `TetrisHighScore.json`
- Splash screen, background music and sound effects, pause with `P`

## Structure

    src/model/        game state, blocks, scores and configuration
    src/view/         Swing screens and panels
    src/controller/   game loop, AI and external player
    src/utilities/    music, sound effects and label factories
    src/test/         JUnit tests

## Run it

Open the project in IntelliJ IDEA, add the JARs in `externalJar/` (Gson and JLayer) and JUnit 5 as libraries, then run `src/Main.java`.

The External player type needs a compatible Tetris server listening on `localhost:3000`.
