# Android-
Android开发容易忽略的小技巧

## PopWindow避免消失后再次自动弹出
```
mPopupWindow.setTouchInterceptor((v, event) -> {
            if(event.getAction()== MotionEvent.ACTION_OUTSIDE){
                mPopupWindow.dismiss();
                return true;
            }
            return false;
        });
```
