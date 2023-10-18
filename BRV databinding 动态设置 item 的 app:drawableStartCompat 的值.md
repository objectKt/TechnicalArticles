```kotlin
        binding.vbList.grid(2).setup {
            addType<DividerModel>(R.layout.item_divider_vertical)
            onBind {
                @BindingAdapter("appDrawableStartCompat")
                fun setDrawableStartCompat(textView: AppCompatTextView, drawable: Drawable?) {
                    textView.setCompoundDrawablesWithIntrinsicBounds(drawable, null, null, null)
                }

                val binding = getBinding<ItemDividerVerticalBinding>()
                val drawable: Drawable? = (getModel() as DividerModel).drawable
                if (drawable != null) {
                    setDrawableStartCompat(binding.vbItemTitle, drawable)
                }
            }
        }.models = mutableListOf<Any?>().apply {
            repeat(4) {
                add(DividerModel().apply {
                    drawable = ContextCompat.getDrawable(requireContext(), R.mipmap.icon)
                })
            }
        }
```
