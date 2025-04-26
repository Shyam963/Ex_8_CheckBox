# Ex No : 08
Develop an android application to display the images using gallery control.
## AIM:
To  Develop an android application to display the images using gallery control.

## EQUIPMENTS REQUIRED:

Android Studio(Min. required Artic Fox)


## ALGORITHM:
Step 1: Open Android Studio and then click on File -> New -> New project.

Step 2: Then type the Application name as SMSIntent and click Next.

Step 3: Select the Minimum SDK below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally, click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Once the Selected check box displayed to the user processed in MainActivity.java

Step 7: Save and run the application.


## Program:
 ```
/*
Program to create an Option Menu
Developed by: S Shyam
RegisterNumber: 212222220045
*/
```

## MainActivity.java:
```
package com.example.gallerycontrol;


import android.os.Bundle;
import android.view.Gravity;
import android.widget.ImageView;
import android.widget.LinearLayout;
import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

    int[] imageIds = {
            R.drawable.image1,
            R.drawable.image2,
            R.drawable.image3,
            R.drawable.image4
    };

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        LinearLayout galleryLayout = findViewById(R.id.galleryLayout);

        int[] imageIds = {
                R.drawable.image1,
                R.drawable.image2,
                R.drawable.image3,
                R.drawable.image4
        };

        for (int imageId : imageIds) {
            ImageView imageView = new ImageView(this);
            imageView.setImageResource(imageId);

            LinearLayout.LayoutParams params = new LinearLayout.LayoutParams(900, 900);
            params.setMargins(30, 30, 30, 30);
            params.gravity = Gravity.CENTER_VERTICAL; 

            imageView.setLayoutParams(params);
            galleryLayout.addView(imageView);
        }

    }

    }


```

## activity_main.xml:
```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    android:orientation="vertical"
    android:gravity="center"
    android:layout_width="match_parent"
    android:layout_height="match_parent">

    <HorizontalScrollView
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:fillViewport="true">

        <LinearLayout
            android:id="@+id/galleryLayout"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:gravity="center_vertical"
            android:orientation="horizontal"
            android:padding="16dp">

        </LinearLayout>
    </HorizontalScrollView>

</LinearLayout>
```


## Output

![Screenshot 2025-04-26 141519](https://github.com/user-attachments/assets/f9843e2b-d6b4-42d8-b883-766fa8d40d64)

![Screenshot 2025-04-26 141553](https://github.com/user-attachments/assets/aa92153b-f447-491b-b219-09b2263ae67e)

![Screenshot 2025-04-26 141809](https://github.com/user-attachments/assets/1314ef33-60c9-4398-bd68-ff75742b64b0)

## Result:
Thus a Simple Android Application to  Develop an android application to display the images using gallery control was developed and executed successfully.
