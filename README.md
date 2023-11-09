# Ex_5_Send-SMS-Using-Intent

Develop program to create and design an android application to Send SMS using Intent in Android Studio.

## AIM:
To create and design an android application Send SMS using Intent in Android Studio.

## EQUIPMENTS REQUIRED:

Android Studio(Min. required Artic Fox)


## ALGORITHM:
Step 1: Open Android Studio and then click on File -> New -> New project.

Step 2: Then type the Application name as SMSIntent and click Next.

Step 3: Select the Minimum SDK below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally, click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Send SMS and Display details given in the MainActivity file.

Step 7: Save and run the application.


## Program:
 ```
/*
Program to create and design an android application for Sending  SMS using Intent.
Developed by: Shaik Sameer Basha 
RegisterNumber:  212222240093
*/
```

## MainActivity.java:
```
package com.example.smsusingintent;

import androidx.appcompat.app.AppCompatActivity;

import android.annotation.SuppressLint;
import android.content.Intent;
import android.net.Uri;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;

public class MainActivity extends AppCompatActivity {

    @SuppressLint("MissingInflatedId")
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        Button btn;
        btn=findViewById(R.id.sendsms);
        btn.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                Intent inte =new Intent(Intent.ACTION_VIEW, Uri.fromParts("sms","9014356158",null));
                inte.putExtra("sms_body","SMS using Intent");
                startActivity(inte);
            }
        });
    }
}
```

## activity_main.xml:
```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity"
    android:gravity="center">

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="SEND SMS"
        android:id="@+id/sendsms"
        android:backgroundTint="#76E8DD"/>

</LinearLayout>
```
## AndroidMainfest.xml
```
<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools">

    <application
        android:allowBackup="true"
        android:dataExtractionRules="@xml/data_extraction_rules"
        android:fullBackupContent="@xml/backup_rules"
        android:icon="@mipmap/ic_launcher"
        android:label="@string/app_name"
        android:roundIcon="@mipmap/ic_launcher_round"
        android:supportsRtl="true"
        android:theme="@style/Theme.SMSusingIntent"
        tools:targetApi="31">
        <activity
            android:name=".MainActivity"
            android:exported="true">
            <intent-filter>
                <action android:name="android.intent.action.MAIN" />

                <category android:name="android.intent.category.LAUNCHER" />
            </intent-filter>
        </activity>
    </application>

</manifest>
```

## Output:
![5 1](https://github.com/shaikSameerbasha5404/Ex_5_Send-SMS-Using-Intent/assets/118707756/c1bd6b9b-af90-4822-aedc-262c4e85022f)


![5 2](https://github.com/shaikSameerbasha5404/Ex_5_Send-SMS-Using-Intent/assets/118707756/49d1f8d0-f94d-4237-8418-e20a095f2eda)


## Result:
Thus a Simple Android Application to create and design an android application for Sending SMS using Intent in Android Studio was developed and executed successfully.
