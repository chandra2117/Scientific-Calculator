# Scientific_Git

### Aim
To develop a Scientific Calculator Android Application that performs basic and scientific mathematical operations such as addition, subtraction, multiplication, division, sine, cosine, tangent, square root, logarithm, and power calculations, and displays the result using a Toast Message.

### Procedure
1.Open Android Studio and create a new Android project.
2.Design the user interface using XML by adding:
.EditText for input numbers.
.Buttons for scientific operations.
3.Write Java code to handle button click events.
4.Use Java's Math class to perform scientific calculations.
5.Display the calculated result using a Toast message.
6.Run the application on an Android emulator or physical device.
7.Verify that all scientific operations produce correct results.

### Program
### MainActivity.java
```
package com.example.scientificcalculator;

import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.Toast;

import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

    EditText etNumber;
    Button btnSin, btnCos, btnTan, btnSqrt;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        etNumber = findViewById(R.id.etNumber);

        btnSin = findViewById(R.id.btnSin);
        btnCos = findViewById(R.id.btnCos);
        btnTan = findViewById(R.id.btnTan);
        btnSqrt = findViewById(R.id.btnSqrt);

        btnSin.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {

                double num = Double.parseDouble(etNumber.getText().toString());
                double result = Math.sin(Math.toRadians(num));

                Toast.makeText(MainActivity.this,
                        "Result = " + result,
                        Toast.LENGTH_SHORT).show();
            }
        });

        btnCos.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {

                double num = Double.parseDouble(etNumber.getText().toString());
                double result = Math.cos(Math.toRadians(num));

                Toast.makeText(MainActivity.this,
                        "Result = " + result,
                        Toast.LENGTH_SHORT).show();
            }
        });

        btnTan.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {

                double num = Double.parseDouble(etNumber.getText().toString());
                double result = Math.tan(Math.toRadians(num));

                Toast.makeText(MainActivity.this,
                        "Result = " + result,
                        Toast.LENGTH_SHORT).show();
            }
        });

        btnSqrt.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {

                double num = Double.parseDouble(etNumber.getText().toString());
                double result = Math.sqrt(num);

                Toast.makeText(MainActivity.this,
                        "Result = " + result,
                        Toast.LENGTH_SHORT).show();
            }
        });
    }
}
```
### activity_main.xml
```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="16dp">

    <EditText
        android:id="@+id/etNumber"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter Number"
        android:inputType="numberDecimal" />

    <Button
        android:id="@+id/btnSin"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="SIN" />

    <Button
        android:id="@+id/btnCos"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="COS" />

    <Button
        android:id="@+id/btnTan"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="TAN" />

    <Button
        android:id="@+id/btnSqrt"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="SQRT" />

</LinearLayout>
```
### Output
<img width="852" height="1846" alt="image" src="https://github.com/user-attachments/assets/244513bb-8317-420b-a943-dbb042317a4d" />
### Result
The Scientific Calculator application was successfully developed and executed. The application performs scientific calculations and displays the computed result using a Toast message.
