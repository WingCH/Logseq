- **[flutter_inappwebview](https://github.com/pichillilorenzo/flutter_inappwebview)**
- use local html show youtube iframe
-
- ```html
  <!DOCTYPE html>
  <html>
  
  <head>
      <style>
          html {
              height: 100%;
          }
  
          body {
              margin: 0px;
              height: 100%;
          }
  
          .main-container {
              display: flex;
              justify-content: center;
              align-items: center;
              height: 100%;
              width: 100%;
          }
  
          .auto-resizable-iframe {
              width: 100%;
              padding-bottom: 56.25%;
              position: relative;
          }
  
          .iframe-container {
              position: absolute;
              width: 100%;
              height: 100%;
          }
  
          iframe {
              width: 100%;
              height: 100%;
          }
      </style>
  </head>
  
  <body>
      <div class="main-container">
          <div class="auto-resizable-iframe">
              <div class="iframe-container">
                  <iframe class="youtube-player" frameborder="0" allowfullscreen=""
                      src="https://www.youtube.com/embed/5Peo-ivmupE?enablejsapi=1"></iframe>
              </div>
          </div>
      </div>
      <script>
          function pauseVideo() {
              const youtubes = document.querySelectorAll(
                  '.youtube-player',
              );
              if (youtubes.length > 0) {
                  youtubes[0].contentWindow.postMessage(
                      '{"event":"command","func":"' + 'pauseVideo' + '","args":""}',
                      '*',
                  );
              }
          }
      </script>
  </body>
  
  </html>
  ```
-
-
- ## Platform Cycle
- ### iOS
- flutter: [debug] onWebViewCreated
  flutter: [debug] onLoadStart about:blank
  flutter: [debug] onLoadStop about:blank
  flutter: [debug] shouldOverrideUrlLoading about:blank
  flutter: [debug] shouldOverrideUrlLoading about:blank
  flutter: [debug] shouldOverrideUrlLoading https://www.youtube.com/watch?v=5Peo-ivmupE&feature=emb_logo
-
- iOS will automatically trigger `shouldOverrideUrlLoading` when loading local html
-
- ### Android
- I/flutter: [debug] onWebViewCreated
- I/flutter: [debug] onLoadStart about:blank
- I/flutter: [debug] onLoadStop about:blank