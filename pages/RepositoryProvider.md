- #bloc
-
- ## How to use
- 1. put `RepositoryProvider` on top of `MaterialApp`
  ```
  return RepositoryProvider.value(
        value: newCarRepository,
        child: MaterialApp(home: NewCarPage()),
      );
  ```
- 2. use `context` get Repository and inject to bloc as dependency in 
  ```
  ```
-