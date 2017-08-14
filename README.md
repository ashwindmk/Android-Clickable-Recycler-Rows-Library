# Android Clickable Recycler Rows

Android library for quickly adding click listeners to your recycler view rows.

[![Release](https://jitpack.io/v/ashwindmk/Android-Clickable-Recycler-Rows-Library.svg)](https://jitpack.io/#ashwindmk/Android-Clickable-Recycler-Rows-Library)

This library allows you to perform click and long click actions on your simple recycler view.

### Setup

Add the jitpack.io repository in your project-level build.gradle file:
```gradle
allprojects {
    repositories {
        ...
        maven { url 'https://jitpack.io' }
    }
}
```

Add the following dependency in your app/build.gradle file:
```gradle
compile 'com.github.ashwindmk:Android-Clickable-Recycler-Rows-Library:0.1'
```

### Usage

In your activity or fragment:
```gradle
public class MainActivity extends AppCompatActivity {
    ...
    @Override
    public void onCreate() {
        super.onCreate();
        setContentView(R.layout.activity_main);
        ...
        recyclerView.addOnItemTouchListener(new RecyclerTouchListener(getApplicationContext(), recyclerView, new RecyclerTouchListener.ClickListener() {
                    @Override
                    public void onClick(View view, int position) {
                        // You got the position in your arraylist
                        // Add your logic here
                    }

                    @Override
                    public void onLongClick(View view, int position) {
                        // You got the position in your arraylist
                        // Add your logic here
                    }
                }));
    }
}
```