# Ex.No:3a Develop program to create a text field and a button “Navigate”. When you enter “www.gmail.com” and press navigate button it should open google page using Implicit Intents.


## AIM:

To create a navigate button using Implicit Intent to display the gmail page using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:

1.Launch the Android application. 
2.Create an Implicit Intent object. 
3.Specify the required action (ACTION_VIEW, ACTION_DIAL, ACTION_SEND, etc.).
4.Attach the required data using Uri.parse(). 
5.Invoke startActivity() with the Intent. 
6.Android searches for a compatible application. 
7.Display the app chooser if multiple apps are available.
8.Launch the selected application.
9.Perform the requested action.

## PROGRAM:
```
/*
Program to print the text “Implicitintent”.
Developed by: Guru Prasad D.R.
Registeration Number :212225040104
*/
```
# MainActivity.java
```
package com.example.implicit;

import android.content.Intent;
import android.net.Uri;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;

import androidx.activity.EdgeToEdge;
import androidx.appcompat.app.AppCompatActivity;
import androidx.core.graphics.Insets;
import androidx.core.view.ViewCompat;
import androidx.core.view.WindowInsetsCompat;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {

        EditText editText;
        Button button;

        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        button = findViewById(R.id.button);
        editText =  findViewById(R.id.e1);

        button.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                String url=editText.getText().toString();
                Intent intent = new Intent(Intent.ACTION_VIEW, Uri.parse(url));
                startActivity(intent);
            }
        });
    }
}
```

# activity_main.xml
```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/main"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <EditText
        android:id="@+id/e1"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginBottom="168dp"
        android:ems="10"
        android:inputType="text"
        android:text="Enter"
        android:textSize="20sp"
        app:layout_constraintBottom_toTopOf="@+id/button"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent" />

    <Button
        android:id="@+id/button"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginBottom="176dp"
        android:text="Search"
        android:textSize="16sp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent" />

    <TextView
        android:id="@+id/textView3"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Implicit Activity"
        android:textSize="20sp"
        app:layout_constraintBottom_toTopOf="@+id/e1"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />
</androidx.constraintlayout.widget.ConstraintLayout>
```
## OUTPUT
<img width="1917" height="971" alt="Screenshot 2026-10-27 075622" src="https://github.com/user-attachments/assets/18ebfb7f-684b-42eb-afc0-807146dd8671" />
<img width="1915" height="1021" alt="Screenshot 2026-10-27 075554" src="https://github.com/user-attachments/assets/5c408cd1-7071-43a5-bfe2-1706efb2a099" />
<img width="1917" height="1018" alt="Screenshot 2026-10-27 075516" src="https://github.com/user-attachments/assets/76929e05-2eb6-4275-b838-03242d735687" />





## RESULT
Thus a Simple Android Application create a navigate button using Implicit Intent to display the gmail page using Android Studio is developed and executed successfully.


