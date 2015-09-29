

Usage
=====

```

SystemUiHelper uiHelper;
 
    @Override 
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.video);
        uiHelper = new SystemUiHelper(this, SystemUiHelper.LEVEL_LEAN_BACK, 0);
    } 
 
    @Override 
    public boolean onTouchEvent(MotionEvent event) {
        switch (event.getAction()){
            case MotionEvent.ACTION_UP:
                if (uiHelper.isShowing()){
                    uiHelper.hide();
                }else{ 
                    uiHelper.show();
                } 
                break; 
        } 
        return super.onTouchEvent(event);
    } 
```

Credits
=======

Chris Banes