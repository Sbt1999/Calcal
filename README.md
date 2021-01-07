# Calcal
# Main.Activity.main
package com.calculator.calical;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;

public class MainActivity extends AppCompatActivity {

    EditText etFirstValue , etSecondValue ;
    TextView tvAns;
    Button add, subtract, multiply, divide;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        etFirstValue = findViewById(R.id.etFirstValue);
        etSecondValue = findViewById(R.id.etSecondValue);

        tvAns = findViewById(R.id.tvAns);
        add = findViewById(R.id.btnAdd);
        subtract = findViewById(R.id.btnSubtract);
        multiply = findViewById(R.id.btnDivide);
        divide = findViewById(R.id.btnMultiply);

        add.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                int firstValue , secondValue, ans;
                firstValue = Integer.parseInt(etFirstValue.getText().toString());
                secondValue = Integer.parseInt(etSecondValue.getText().toString());

                ans = firstValue + secondValue;
                tvAns.setText("Ans  is = " +ans);
            }
        });
        subtract.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                int firstValue , secondValue, ans;
                firstValue = Integer.parseInt(etFirstValue.getText().toString());
                secondValue = Integer.parseInt(etSecondValue.getText().toString());

                ans = firstValue - secondValue;
                tvAns.setText("Ans  is = " +ans);
            }
        });
        multiply.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                int firstValue , secondValue, ans;
                firstValue = Integer.parseInt(etFirstValue.getText().toString());
                secondValue = Integer.parseInt(etSecondValue.getText().toString());

                ans = firstValue * secondValue;
                tvAns.setText("Ans is = " +ans);
            }
        });
        divide.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                int firstValue , secondValue, ans;
                firstValue = Integer.parseInt(etFirstValue.getText().toString());
                secondValue = Integer.parseInt(etSecondValue.getText().toString());

                ans = firstValue % secondValue;
                tvAns.setText("Ans is = " +ans);
            }
        });
    }
}
# xml activity.
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:layout_gravity="center_horizontal"
    android:layout_marginStart="30dp"
    android:layout_marginLeft="30dp"
    android:layout_marginTop="5dp"
    android:layout_marginEnd="30dp"
    android:layout_marginRight="30dp"
    tools:context=".MainActivity">

    <ImageView
        android:id="@+id/imageView4"
        android:layout_width="140dp"
        android:layout_height="120dp"
        android:layout_marginStart="30dp"
        android:layout_marginLeft="30dp"
        android:layout_marginTop="40dp"
        android:layout_marginEnd="30dp"
        android:layout_marginRight="30dp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.498"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.003"
        app:srcCompat="@drawable/calculator" />

    <EditText
        android:id="@+id/etFirstValue"
        android:layout_width="308dp"
        android:layout_height="46dp"
        android:layout_marginStart="30dp"
        android:layout_marginLeft="30dp"
        android:layout_marginTop="10dp"
        android:layout_marginEnd="30dp"
        android:layout_marginRight="30dp"
        android:ems="10"
        android:hint="Enter first value"
        android:inputType="number"
        android:padding="10dp"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/imageView4" />

    <EditText
        android:id="@+id/etSecondValue"
        android:layout_width="311dp"
        android:layout_height="51dp"
        android:layout_marginStart="30dp"
        android:layout_marginLeft="30dp"
        android:layout_marginTop="5dp"
        android:layout_marginEnd="30dp"
        android:layout_marginRight="30dp"
        android:ems="10"
        android:hint="@string/enter_second_value"
        android:inputType="number"
        android:padding="10dp"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.502"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/etFirstValue" />

    <TextView
        android:id="@+id/tvAns"
        android:layout_width="311dp"
        android:layout_height="43dp"
        android:layout_marginStart="30dp"
        android:layout_marginLeft="30dp"
        android:layout_marginTop="10dp"
        android:layout_marginEnd="30dp"
        android:layout_marginRight="30dp"
        android:padding="10dp"
        android:textSize="18sp"
        android:textStyle="bold"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.498"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/etSecondValue" />

    <Button
        android:id="@+id/btnAdd"
        android:layout_width="344dp"
        android:layout_height="54dp"
        android:layout_marginStart="30dp"
        android:layout_marginLeft="30dp"
        android:layout_marginTop="60dp"
        android:layout_marginEnd="30dp"
        android:layout_marginRight="30dp"
        android:background="@android:color/black"
        android:padding="10dp"
        android:text="@string/Plus"
        android:textSize="18sp"
        android:textStyle="bold"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/etSecondValue" />

    <Button
        android:id="@+id/btnSubtract"
        android:layout_width="350dp"
        android:layout_height="53dp"
        android:layout_marginStart="30dp"
        android:layout_marginLeft="30dp"
        android:layout_marginTop="5dp"
        android:layout_marginEnd="30dp"
        android:layout_marginRight="30dp"
        android:background="@android:color/black"
        android:padding="10dp"
        android:text="@string/Minus"
        android:textSize="18sp"
        android:textStyle="bold"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/btnAdd" />

    <Button
        android:id="@+id/btnMultiply"
        android:layout_width="350dp"
        android:layout_height="49dp"
        android:layout_marginStart="30dp"
        android:layout_marginLeft="30dp"
        android:layout_marginTop="5dp"
        android:layout_marginEnd="30dp"
        android:layout_marginRight="30dp"
        android:background="@android:color/black"
        android:padding="10dp"
        android:text="@string/Division"
        android:textSize="18sp"
        android:textStyle="bold"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/btnSubtract"
        tools:text="*" />

    <Button
        android:id="@+id/btnDivide"
        android:layout_width="354dp"
        android:layout_height="50dp"
        android:layout_marginStart="30dp"
        android:layout_marginLeft="30dp"
        android:layout_marginTop="5dp"
        android:layout_marginEnd="30dp"
        android:layout_marginRight="30dp"
        android:background="@android:color/black"
        android:padding="10dp"
        android:text="@string/string_multiplication"
        android:textSize="18sp"
        android:textStyle="bold"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/btnMultiply"
        tools:text="/" />

</androidx.constraintlayout.widget.ConstraintLayout>
