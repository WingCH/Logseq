- #bloc
-
- ## How to use
- 1. put `RepositoryProvider` on top of `MaterialApp`
  ```dart
  return RepositoryProvider.value(
        value: newCarRepository,
        child: MaterialApp(home: NewCarPage()),
      );
  ```
- 2. use `context` get Repository and inject to bloc as dependency
  
  ```dart
  Widget build(BuildContext context) {
      return Scaffold(
        appBar: AppBar(title: const Text('Flutter Dynamic Form')),
        body: BlocProvider(
          create: (_) => NewCarBloc(
            newCarRepository: context.read<NewCarRepository>(),
          )..add(const NewCarFormLoaded()),
          child: NewCarForm(),
        ),
      );
    }
  ```
-
-
-