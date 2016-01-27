# KanvasShowcaseView
A ShowcaseView for Android themed with the look and feel of the Kanvas apps

This library is based on the MaterialShowcaseView for Android library [MaterialShowcaseView][1]

KanvasShowCase view has the look and feel of the Kanvas apps, introduces new helper methods and is compatiblke 

![live-tutorial](https://cloud.githubusercontent.com/assets/4109119/12628172/a2286b16-c520-11e5-8e26-f21197056e9f.png)

# How to use
--------
It's usage is very similar to the the MaterialShowcaseView, most of the moddified stuff is being handled inside the library

```java

	private void showHelp() {
        KanvasShowcaseView ksv = new KanvasShowcaseView.Builder(getActivity())
                .setTarget(mStickersModeButton)
                .setContentText(getResources().getText(R.string.live_tutorial_message))
                .setDismissText(getResources().getText(R.string.live_tutorial_dismiss))
                .renderOverNavigationBar() // Required for fullscreen on API >= 21
                .setListener(new IShowcaseListener() {
                    @Override
                    public void onShowcaseDisplayed(KanvasShowcaseView kanvasShowcaseView) {

                    }

                    @Override
                    public void onShowcaseDismissed(KanvasShowcaseView kanvasShowcaseView) {
                        // Do something when the showcase is dismessed
                    }
                })
                .build();

        ksv.getContentTextView().setTypeface(KanvasApplication.Fonts.ROBOTO_REGULAR);
        ksv.getDismissTextView().setTypeface(KanvasApplication.Fonts.ROBOTO_MEDIUM);
        ksv.show(getActivity());
    }
                
```





[1]: https://github.com/deano2390/MaterialShowcaseView
