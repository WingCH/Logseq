- ## Reason
- 1. [example](https://github.com/OneSignal/OneSignal-Flutter-SDK/tree/main/example) does not create custom channel, if no existing channel, OneSignal push notification will use `Miscellaneous` channel as default channel, but this channel does not have enable `Pop on screen`  permission, so the notification cannot show in screen
- ![image.png](../assets/image_1661350753568_0.png){:height 345, :width 191}
- ## Solution (not confirmed)
- create custom channel, and set `Importance` to **URGENT** which can auto enable `Pop on screen`
- two way to create channel
- 1. in OneSignal dashboard
  2. in app, https://developer.android.com/training/notify-user/channels
- > in android native, `Importance` to *HIGH* is ok
-