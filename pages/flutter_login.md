title:: flutter_login

- [Simulator Screen Recording - iPhone 13 Pro - 2022-06-03 at 20.54.21.mp4](../assets/Simulator_Screen_Recording_-_iPhone_13_Pro_-_2022-06-03_at_20.54.21_1654260881621_0.mp4)
- [:video {:controls true :src "/Users/wingch/Project/Logseq/assets/../assets/Simulator_Screen_Recording_-_iPhone_13_Pro_-_2022-06-03_at_20.54.21_1654260881621_0.mp4"}]
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
  listen stream and fire the event within bloc
  ```dart
  _authenticationRepository.status.listen(
        (status) => add(AuthenticationStatusChanged(status)),
  );
  ```
- 4. [[RepositoryProvider]] #repository_pattern
  StreamController within Repository
-