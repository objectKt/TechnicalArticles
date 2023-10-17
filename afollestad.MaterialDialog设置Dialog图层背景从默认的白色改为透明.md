```kotlin
val dialog = com.afollestad.materialdialogs.MaterialDialog(windowContext)
dialog.customView(R.layout.dialog_custom_input, null, scrollable = true, noVerticalPadding = true)
dialog.cancelOnTouchOutside(true)
// 如果没有下面这行代码，在布局文件 R.layout.dialog_custom_input 里的 rootView 设置 android:background="#00000000" 是无效的
dialog.dialogBehavior.setBackgroundColor(dialog.view, Color.TRANSPARENT, 0F)
```
