url:: https://bloclibrary.dev/#/flutterbloccoreconcepts?id=blocprovider

- ## How to use
- ### Two way
- 1. on top of `page` , so that a single instance of a bloc can be provided to multiple widgets within a subtree. 
  > when page is close, It will automatically handle closing the bloc.
  
  ```dart
  BlocProvider(
    create: (BuildContext context) => BlocA(),
    child: ChildA(),
  );
  ```
-
-