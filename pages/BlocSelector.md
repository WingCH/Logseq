- if builder widget not used selected state, the builder will not update forever
- bad example:
	- ```dart
	  BlocSelector<HomeBloc, HomeState, String>(
	    selector: (state) {
	      return state.qrCodeData;
	    },
	    builder: (context, qrCodeData) {
	      return Text('not use state (qrCodeData) here');
	    },
	  )
	  ```