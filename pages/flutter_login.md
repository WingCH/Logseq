title:: flutter_login

-
## Point
- 1. [[BlocListener]]
  listen auth status to drive navigator in widget part #navigator
  ```dart
  return BlocListener<AuthenticationBloc, AuthenticationState>(
    listener: (context, state) {
      switch (state.status) {
        case AuthenticationStatus.authenticated:
          _navigator.pushAndRemoveUntil<void>(
            HomePage.route(),
            (route) => false,
          );
          break;
        case AuthenticationStatus.unauthenticated:
          _navigator.pushAndRemoveUntil<void>(
            LoginPage.route(),
            (route) => false,
          );
          break;
        default:
          break;
      }
    },
    child: child,
  );
  ```
- 2. [[BlocSelector]]
  
  > Will only rebuild the widget when the property `user.id` of the Bloc state changes.
  
  ```dart
  Builder(
    builder: (context) {
      final userId = context.select(
        (AuthenticationBloc bloc) => bloc.state.user.id,
      );
      return Text('UserID: $userId');
    },
  ),
  ```
- 3. mix StreamController
  listen stream within bloc
-