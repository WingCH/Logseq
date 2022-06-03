url:: https://bloclibrary.dev/#/flutterbloccoreconcepts?id=blocprovider

- ## How to use
- ### Two way
- 1. on top of `page` , so that a single instance of a bloc can be provided to multiple widgets within a subtree. 
  > when page is close, It will automatically handle closing the bloc.
  
  ```dart
  @override
  Widget build(BuildContext context) {
    return BlocProvider(
      create: (_) => HomeBloc(),
      child: const HomeView(),
    );
  }
  ```
- in subtree, we can use `context` get Bloc
  ```dart
  // with extensions
  context.read<HomeBloc>();
  // without extensions
  BlocProvider.of<HomeBloc>(context)
  ```
  then we can send `event`
  ```dart
   context.read<HomeBloc>().add(const HomeCameraTaped());
  ```
-
-
-
-
-