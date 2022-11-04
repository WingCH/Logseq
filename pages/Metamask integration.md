- Tutorial:
- https://dev.to/bhaskardutta/building-with-flutter-and-metamask-8h5
-
-
- `Wallet Connect` deeplink and universal link doc
- https://docs.walletconnect.com/mobile-linking#wallet-support
-
- MetaMask staff suggest use `Wallet Connect`
- https://github.com/MetaMask/metamask-mobile/issues/4500
-
-
- **Code:**
- https://github.com/WingCH/Learning/tree/main/Flutter/metamask_integration
-
- ---
-
- ## PeerMeta Behavior
-
- ||MetaMask|Exodus|Defi Wallet (Crypto.com)|Trust Wallet|
  |--|--|--|--|--|
  |android| ![photo1667554471.jpeg](../assets/photo1667554471_1667555373930_0.jpeg) | ![photo1667554472.jpeg](../assets/photo1667554472_1667555471367_0.jpeg) | ![photo1667554474.jpeg](../assets/photo1667554474_1667555480829_0.jpeg) | ![photo1667554470.jpeg](../assets/photo1667554470_1667555493493_0.jpeg) |
  |iOS|||||
- Android
- ```dart
  PeerMeta(
    name: packageInfo.appName,
    url: 'https://artazine.com',
    icons: ['https://assets.artazine.com/favicon.png'],
  ),
  ```
-
-