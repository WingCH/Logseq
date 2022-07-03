- ig
- ```dart
  BlocSelector<HomeBloc, HomeState, String>(
    selector: (state) {
      return state.qrCodeData;
    },
    builder: (context, qrCodeData) {
      return QrImage(
        data: qrCodeData,
        version: QrVersions.auto,
        size: 200.0,
      );
    },
  )
  ```