
# Ex.No:6 Design an android application Send SMS using Intent.


## AIM:

To create and design an android application Send SMS using Intent using Android Studio.

## EQUIPMENTS REQUIRED:

Android Studio(Latest Version)

## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as smsintent and click Next. 

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Send SMS and Display details give in MainActivity file.

Step 7: Save and run the application.

## PROGRAM:
```

Program to create and design an android application Send SMS using Intent.
Developed by: Sanjana J
Registeration Number : 212224230240
```
## Activity_main.xml
```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:gravity="center"
    android:padding="20dp">

    <Button
        android:id="@+id/btnSendSMS"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Send SMS"
        android:padding="12dp"
        android:textSize="18sp"/>
</LinearLayout>

```
## Main_activity.java
```
package com.example.sendsmsapp;

import android.content.Intent;
import android.net.Uri;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;

import androidx.activity.EdgeToEdge;
import androidx.appcompat.app.AppCompatActivity;
import androidx.core.graphics.Insets;
import androidx.core.view.ViewCompat;
import androidx.core.view.WindowInsetsCompat;

import com.example.sendsmsapp.R;

public class MainActivity extends AppCompatActivity {

    Button btnSendSMS;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        btnSendSMS = findViewById(R.id.btnSendSMS);

        btnSendSMS.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                // Define recipient number and message
                String phoneNumber = "9876543210"; // replace with test number
                String message = "Hello! This is a test SMS from my Android app.";

                // Use SMS Intent
                Intent smsIntent = new Intent(Intent.ACTION_VIEW);
                smsIntent.setData(Uri.parse("smsto:" + phoneNumber));
                smsIntent.putExtra("sms_body", message);

                // Start SMS app
                startActivity(smsIntent);
            }
        });
    }
}
```

## OUTPUT

<img width="1619" height="864" alt="Screenshot 2025-09-24 132740" src="https://github.com/user-attachments/assets/95144fcc-6fd1-49d1-9e45-1ab98a751ef2" />

<img width="1621" height="798" alt="Screenshot 2025-09-24 132759" src="https://github.com/user-attachments/assets/e3781902-0857-4001-96ea-d8e132314e03" />

<img width="1641" height="882" alt="Screenshot 2025-09-24 132827" src="https://github.com/user-attachments/assets/cf38de62-15ca-47b8-bfc7-638df3433c1a" />


## RESULT
Thus a Simple Android Application create and design an android application Send SMS using Intent using Android Studio is developed and executed successfully.
