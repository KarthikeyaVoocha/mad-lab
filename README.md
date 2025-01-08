# mad-lab

List of MAD LAB Programs: 
1. To develop a simple Android application to display “Hello world!!” 
2. To develop a simple Android application to raise a Toast on button click. 
3. To develop a simple Android application to change font size and color of text view. 
4. To develop a simple Android application to change image on click. 
5. To develop a simple Android application to change Background on click. 
6. To develop a simple Android application to Calculate Simple and Compound Interest. 
7. To develop a simple Android application to Calculate roots of a Quadratic equation. 
8. To develop a simple Android application to convert temperature between degree 
Celsius and Fahrenheit. 
9. To develop a simple Android application to validate Login form with Toast. 
10.  To develop a simple Android application to validate Login form with navigation. 
11. To develop a simple Android application to send message from one page to other. 
12. To develop a simple Android application to Navigate from one page to other. 
13. To develop a simple Android application to demonstrate the use of layout manager – 
Design ID Card. 
14. To develop a simple Android application that draws basic graphical primitives on the 
screen – Draw Smiley 
15. To develop a simple Android application that sends an Email. 
16. To develop a simple Android application that sends a SMS. 
17. To develop a simple Android application that sends a Native Notification. 
18. To develop a simple Android application that converts Text to Speech. 
19. To develop a simple Android application that displays GPS Location. 
20. To develop a simple Android application for Calculator. 
21. To develop a simple Android application that implements Multi threading. 
22. To develop a simple Android application that makes use of Databases. 
23. To develop a simple Android application that creates an alert Dialogue upon receiving a 
message. 
24. To develop a simple Android application that writes data to the SDCard. 
25. To develop a simple Android application that creates Alarm Clock. 
26. To develop a simple Android application that makes use of RSS Feed. 
EXPERIMENT NO.: 1 
Aim: To develop a simple Android application to display “Hello world!!” 
1.  Open android studio and select new android project by clicking Filemenu  New 
New Project. 
2. Choose the project as Empty Views Activity and click Next. 
3. Give project name (Start with a capital letter) as Helloworld  
4. Choose the language as Java. 
5. Choose the required android version (Minimum SDK) and select finish. 
6. Go to package explorer in the left hand side and select the project. 
7. Under the project, Go to res folder and select layout. 
8. Double click the activity_main.xml file and design the layout for the page. 
9. Select MainActivity.java file and type the program. 
10.  Now go to activity_main.xml and right click & select run as option and select run 
configuration OR select the virtual device and click on run icon. 
11.  Android output will be displayed on the android emulator. 
Both activity_main.xml and MainActivity.java files together make our application work. The 
activity_main.xml is responsible for the layout (Front end User Interface) of the application. And 
the file MainActivity is responsible for the actions and the performance of the application (back 
end). 
Code: 
activity_main.xml 
<?xml version="1.0" encoding="utf-8"?> 
<androidx.constraintlayout.widget.ConstraintLayout 
xmlns:android="http://schemas.android.com/apk/res/android" 
xmlns:app="http://schemas.android.com/apk/res-auto" 
xmlns:tools="http://schemas.android.com/tools" 
android:id="@+id/main" 
android:layout_width="match_parent" 
android:layout_height="match_parent" 
tools:context=".MainActivity"> 
<TextView 
android:layout_width="wrap_content" 
android:layout_height="wrap_content" 
android:text=" Hello World!" 
android:textColor="#E61F1F" 
android:textSize="48sp" 
android:textStyle="bold" 
app:layout_constraintBottom_toBottomOf="parent" 
app:layout_constraintEnd_toEndOf="parent" 
app:layout_constraintStart_toStartOf="parent" 
app:layout_constraintTop_toTopOf="parent" /> 
</androidx.constraintlayout.widget.ConstraintLayout> 
MainActivity.java 
package com.example.helloworld; 
import android.os.Bundle; 
import android.view.View; 
import android.widget.Button; 
import android.widget.Toast; 
import androidx.activity.EdgeToEdge; 
import androidx.appcompat.app.AppCompatActivity; 
import androidx.core.graphics.Insets; 
import androidx.core.view.ViewCompat; 
import androidx.core.view.WindowInsetsCompat; 
public class MainActivity extends AppCompatActivity { 
Button b ; 
@Override 
protected void onCreate(Bundle savedInstanceState) { 
super.onCreate(savedInstanceState); 
EdgeToEdge.enable(this); 
setContentView(R.layout.activity_main); 
ViewCompat.setOnApplyWindowInsetsListener(findViewById(R.id.main
 ), (v, insets) -> { 
Insets systemBars = 
insets.getInsets(WindowInsetsCompat.Type.systemBars()); 
v.setPadding(systemBars.left, systemBars.top, 
systemBars.right, systemBars.bottom); 
return insets; 
}); 
} 
} 
OUTPUT ON EMULATOR: 
EXPERIMENT NO.: 2 
Aim: To develop a simple Android application to raise a Toast on button click. 
1. Open android studio and select new android project by clicking Filemenu  New New 
Project. 
2. Choose the project as Empty Views Activity and click Next. 
3. Give project name (Start with a capital letter) as RaiseToast 
4. Choose the language as Java. 
5. Choose the required android version (Minimum SDK) and select finish. 
6. Go to package explorer in the left hand side and select the project. 
7. Under the project, Go to res folder and select layout. 
8. Double click the activity_main.xml file and design the layout for the page. 
9. Select MainActivity.java file and type the program. 
10.  Now go to activity_main.xml and right click & select run as option and select run 
configuration OR select the virtual device and click on run icon. 
11.  Android output will be displayed on the android emulator. 
Both activity_main.xml and MainActivity.java files together make our application work. The 
activity_main.xml is responsible for the layout (Front end User Interface) of the application. And 
the file MainActivity is responsible for the actions and the performance of the application (back 
end). 
Code: 
activity_main.xml 
<?xml version="1.0" encoding="utf-8"?> 
<androidx.constraintlayout.widget.ConstraintLayout 
xmlns:android="http://schemas.android.com/apk/res/android" 
xmlns:app="http://schemas.android.com/apk/res-auto" 
xmlns:tools="http://schemas.android.com/tools" 
android:id="@+id/main" 
android:layout_width="match_parent" 
android:layout_height="match_parent" 
tools:context=".MainActivity"> 
<TextView 
android:id="@+id/textView" 
android:layout_width="wrap_content" 
android:layout_height="wrap_content" 
android:text="Raise Toast" 
android:textColor="#E61F1F" 
android:textSize="48sp" 
android:textStyle="bold" 
app:layout_constraintBottom_toBottomOf="parent" 
app:layout_constraintEnd_toEndOf="parent" 
app:layout_constraintHorizontal_bias="0.496" 
app:layout_constraintStart_toStartOf="parent" 
app:layout_constraintTop_toTopOf="parent" 
app:layout_constraintVertical_bias="0.134" /> 
<Button 
android:id="@+id/button" 
android:layout_width="wrap_content" 
android:layout_height="wrap_content" 
android:layout_marginTop="300dp" 
android:text="Click Here" 
android:textSize="34sp" 
app:layout_constraintEnd_toEndOf="parent" 
app:layout_constraintStart_toStartOf="parent" 
app:layout_constraintTop_toTopOf="parent" /> 
</androidx.constraintlayout.widget.ConstraintLayout> 
MainActivity.java 
package com.example.raisetoast; 
import android.os.Bundle; 
import android.view.View; 
import android.widget.Button; 
import android.widget.Toast; 
import androidx.activity.EdgeToEdge; 
import androidx.appcompat.app.AppCompatActivity; 
import androidx.core.graphics.Insets; 
import androidx.core.view.ViewCompat; 
import androidx.core.view.WindowInsetsCompat; 
public class MainActivity extends AppCompatActivity { 
Button b ; 
@Override 
protected void onCreate(Bundle savedInstanceState) { 
super.onCreate(savedInstanceState); 
EdgeToEdge.enable(this); 
setContentView(R.layout.activity_main); 
ViewCompat.setOnApplyWindowInsetsListener(findViewById(R.id.main
 ), (v, insets) -> { 
Insets systemBars = 
insets.getInsets(WindowInsetsCompat.Type.systemBars()); 
v.setPadding(systemBars.left, systemBars.top, 
systemBars.right, systemBars.bottom); 
return insets; 
}); 
b = (Button) findViewById(R.id.button); 
b.setOnClickListener(new View.OnClickListener() { 
@Override 
public void onClick(View v) { 
Toast.makeText(getBaseContext(),"Hello All.. 
Welcome to MAD LAB", Toast.LENGTH_LONG).show(); 
} 
}); 
} 
} 
OUTPUT ON EMULATOR: 
EXPERIMENT NO.: 3 
Aim: To develop a simple Android application to change font size and color of Text Veiw 
1.  Open android studio and select new android project by clicking Filemenu  New 
New Project. 
2. Choose the project as Empty Views Activity and click Next. 
3. Give project name (Start with a capital letter) as GUIfontcolor  
4. Choose the language as Java. 
5. Choose the required android version (Minimum SDK) and select finish. 
6. Go to package explorer in the left hand side and select the project. 
7. Under the project, Go to res folder and select layout. 
8. Double click the activity_main.xml file and design the layout for the page. 
9. Select MainActivity.java file and type the program. 
10.  Now go to activity_main.xml and right click & select run as option and select run 
configuration OR select the virtual device and click on run icon. 
11.  Android output will be displayed on the android emulator. 
Both activity_main.xml and MainActivity.java files together make our application work. The 
activity_main.xml is responsible for the layout (Front end User Interface) of the application. And 
the file MainActivity is responsible for the actions and the performance of the application (back 
end). 
Code: 
activity_main.xml 
<?xml version="1.0" encoding="utf-8"?> 
<androidx.constraintlayout.widget.ConstraintLayout 
xmlns:android="http://schemas.android.com/apk/res/android" 
xmlns:app="http://schemas.android.com/apk/res-auto" 
xmlns:tools="http://schemas.android.com/tools" 
android:id="@+id/main" 
android:layout_width="match_parent" 
android:layout_height="match_parent" 
tools:context=".MainActivity"> 
<TextView 
android:id="@+id/textView" 
android:layout_width="wrap_content" 
android:layout_height="wrap_content" 
android:text="MVSREC ITD" 
android:textColor="#E61F1F" 
android:textSize="48sp" 
android:textStyle="bold" 
app:layout_constraintBottom_toBottomOf="parent" 
app:layout_constraintEnd_toEndOf="parent" 
app:layout_constraintHorizontal_bias="0.496" 
app:layout_constraintStart_toStartOf="parent" 
app:layout_constraintTop_toTopOf="parent" 
app:layout_constraintVertical_bias="0.236" /> 
<Button 
android:id="@+id/col" 
android:layout_width="wrap_content" 
android:layout_height="wrap_content" 
android:layout_marginTop="300dp" 
android:text="Change Color" 
android:textSize="34sp" 
app:layout_constraintEnd_toEndOf="parent" 
app:layout_constraintStart_toStartOf="parent" 
app:layout_constraintTop_toTopOf="parent" /> 
<Button 
android:id="@+id/font" 
android:layout_width="wrap_content" 
android:layout_height="wrap_content" 
android:layout_marginTop="408dp" 
android:text="Change Font" 
android:textSize="34sp" 
app:layout_constraintEnd_toEndOf="parent" 
app:layout_constraintStart_toStartOf="parent" 
app:layout_constraintTop_toTopOf="parent" /> 
</androidx.constraintlayout.widget.ConstraintLayout> 
MainActivity.java 
package com.example.guifontcolor; 
import android.graphics.Color; 
import android.os.Bundle; 
import android.view.View; 
import android.widget.Button; 
import android.widget.TextView; 
import androidx.activity.EdgeToEdge; 
import androidx.appcompat.app.AppCompatActivity; 
import androidx.core.graphics.Insets; 
import androidx.core.view.ViewCompat; 
import androidx.core.view.WindowInsetsCompat; 
public class MainActivity extends AppCompatActivity { 
TextView t1; 
    Button c,f; 
    int i=1; 
    float font = 30; 
 
    @Override 
    protected void onCreate(Bundle savedInstanceState) { 
        super.onCreate(savedInstanceState); 
        EdgeToEdge.enable(this); 
        setContentView(R.layout.activity_main); 
        
ViewCompat.setOnApplyWindowInsetsListener(findViewById(R.id.main
 ), (v, insets) -> { 
            Insets systemBars = 
insets.getInsets(WindowInsetsCompat.Type.systemBars()); 
            v.setPadding(systemBars.left, systemBars.top, 
systemBars.right, systemBars.bottom); 
            return insets; 
        }); 
 
        t1 = (TextView) findViewById(R.id.textView); 
        c = (Button) findViewById(R.id.col); 
        f = (Button) findViewById(R.id.font); 
 
        c.setOnClickListener(new View.OnClickListener() { 
            @Override 
            public void onClick(View v) { 
                switch (i) 
                { 
          case 1: t1.setTextColor(Color.parseColor("#0000FF")); 
                  i++; break; 
          case 2: t1.setTextColor(Color.parseColor("#00FF00")); 
                  i++; break; 
          case 3: t1.setTextColor(Color.parseColor("#FF0000"));  
                  i++; break; 
          case 4: t1.setTextColor(Color.parseColor("#00FFFF")); 
                  i++; break; 
          case 5: t1.setTextColor(Color.parseColor("#0FF0FF"));  
                  i++; break; 
                } 
                if(i==6) i=1; 
            } 
        }); 
 
        f.setOnClickListener(new View.OnClickListener() { 
            @Override 
            public void onClick(View v) { 
                t1.setTextSize(font); 
                font = font+5; 
                if(font==50) font=30; 
            } 
        }); 
    } 
} 
 
OUTPUT ON EMULATOR: 
   
 
 
 
 
 
 
 
 
 
 
 
 
 
 
EXPERIMENT NO.: 4 
Aim: To develop a simple Android application to change image on click 
1.  Open android studio and select new android project by clicking Filemenu  New 
New Project. 
2. Choose the project as Empty Views Activity and click Next. 
3. Give project name (Start with a capital letter) as ChangeImages  
4. Choose the language as Java. 
5. Choose the required android version (Minimum SDK) and select finish. 
6. Go to package explorer in the left hand side and select the project. 
7. Under the project, res folder, drawable folder add jpg or png images. 
8. Under the project, Go to res folder and select layout. 
9. Double click the activity_main.xml file and design the layout for the page. 
10. Select MainActivity.java file and type the program. 
11.  Now go to activity_main.xml and right click & select run as option and select run 
configuration OR select the virtual device and click on run icon. 
12.  Android output will be displayed on the android emulator. 
Both activity_main.xml and MainActivity.java files together make our application work. The 
activity_main.xml is responsible for the layout (Front end User Interface) of the application. And 
the file MainActivity is responsible for the actions and the performance of the application (back 
end). 
Code: 
activity_main.xml 
<?xml version="1.0" encoding="utf-8"?> 
<androidx.constraintlayout.widget.ConstraintLayout 
xmlns:android="http://schemas.android.com/apk/res/android" 
xmlns:app="http://schemas.android.com/apk/res-auto" 
xmlns:tools="http://schemas.android.com/tools" 
android:id="@+id/main" 
android:layout_width="match_parent" 
android:layout_height="match_parent" 
tools:context=".MainActivity"> 
<TextView 
android:id="@+id/textView" 
android:layout_width="wrap_content" 
android:layout_height="wrap_content" 
android:text="Cartoon Show" 
android:textColor="#E61F1F" 
android:textSize="48sp" 
android:textStyle="bold" 
app:layout_constraintBottom_toBottomOf="parent" 
app:layout_constraintEnd_toEndOf="parent" 
app:layout_constraintHorizontal_bias="0.496" 
app:layout_constraintStart_toStartOf="parent" 
app:layout_constraintTop_toTopOf="parent" 
app:layout_constraintVertical_bias="0.079" /> 
<Button 
android:id="@+id/img" 
android:layout_width="wrap_content" 
android:layout_height="wrap_content" 
android:layout_marginTop="520dp" 
android:text="Change Image" 
android:textSize="34sp" 
app:layout_constraintEnd_toEndOf="parent" 
app:layout_constraintHorizontal_bias="0.496" 
app:layout_constraintStart_toStartOf="parent" 
app:layout_constraintTop_toTopOf="parent" /> 
<ImageView 
android:id="@+id/imageView" 
android:layout_width="wrap_content" 
android:layout_height="wrap_content" 
android:layout_marginTop="72dp" 
android:layout_marginEnd="34dp" 
app:layout_constraintEnd_toEndOf="@+id/textView" 
app:layout_constraintTop_toBottomOf="@+id/textView" 
app:srcCompat="@drawable/c1" /> 
</androidx.constraintlayout.widget.ConstraintLayout> 
MainActivity.java 
package com.example.changeimage; 
import android.os.Bundle; 
import android.view.View; 
import android.widget.Button; 
import android.widget.ImageView; 
import androidx.activity.EdgeToEdge; 
import androidx.appcompat.app.AppCompatActivity; 
import androidx.core.graphics.Insets; 
import androidx.core.view.ViewCompat; 
import androidx.core.view.WindowInsetsCompat; 
public class MainActivity extends AppCompatActivity { 
Button b; 
ImageView iv; 
boolean flag = true; 
int img[] = { 
R.drawable.c1,R.drawable.c2,R.drawable.c3,R.drawable.c4}; 
int i=0; 
@Override 
protected void onCreate(Bundle savedInstanceState) { 
super.onCreate(savedInstanceState); 
EdgeToEdge.enable(this); 
setContentView(R.layout.activity_main); 
ViewCompat.setOnApplyWindowInsetsListener(findViewById(R.id.main
 ), (v, insets) -> { 
Insets systemBars = 
insets.getInsets(WindowInsetsCompat.Type.systemBars()); 
v.setPadding(systemBars.left, systemBars.top, 
systemBars.right, systemBars.bottom); 
return insets; 
}); 
b = (Button) findViewById(R.id.img); 
iv = (ImageView) findViewById(R.id.imageView); 
b.setOnClickListener(new View.OnClickListener() { 
@Override 
public void onClick(View v) { 
iv.setImageResource(img[i]); 
i++; 
if(i==4) i=0; 
} 
}); 
} 
} 
OUTPUT ON EMULATOR:  
   
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
EXPERIMENT NO.: 5 
Aim: To develop a simple Android application to Change background on click. 
1.  Open android studio and select new android project by clicking Filemenu  New 
New Project. 
2. Choose the project as Empty Views Activity and click Next. 
3. Give project name (Start with a capital letter) as Backgroundchange  
4. Choose the language as Java. 
5. Choose the required android version (Minimum SDK) and select finish. 
6. Go to package explorer in the left hand side and select the project. 
7. Under the project, Go to res folder and select layout. 
8. Double click the activity_main.xml file and design the layout for the page. 
9. Select MainActivity.java file and type the program. 
10.  Under res folder  values  colors.xml add red and green color. 
11.  Under res folder  drawable, add one jpeg image for background. 
12.  Now go to activity_main.xml and right click & select run as option and select run 
configuration OR select the virtual device and click on run icon. 
13.  Android output will be displayed on the android emulator. 
Both activity_main.xml and MainActivity.java files together make our application work. The 
activity_main.xml is responsible for the layout (Front end User Interface) of the application. And 
the file MainActivity is responsible for the actions and the performance of the application (back 
end). 
Code: 
activity_main.xml 
<?xml version="1.0" encoding="utf-8"?> 
<androidx.constraintlayout.widget.ConstraintLayout 
xmlns:android="http://schemas.android.com/apk/res/android" 
xmlns:app="http://schemas.android.com/apk/res-auto" 
xmlns:tools="http://schemas.android.com/tools" 
android:id="@+id/main" 
android:layout_width="match_parent" 
android:layout_height="match_parent" 
tools:context=".MainActivity"> 
<LinearLayout 
android:id="@+id/ll" 
android:layout_width="wrap_content" 
android:layout_height="0dp" 
android:orientation="vertical" 
app:layout_constraintBottom_toBottomOf="parent" 
app:layout_constraintStart_toStartOf="parent" 
        app:layout_constraintTop_toTopOf="parent"> 
 
        <TextView 
            android:id="@+id/textView2" 
            android:layout_width="401dp" 
            android:layout_height="wrap_content" 
            android:layout_marginTop="100dp" 
            android:layout_marginBottom="100dp" 
            android:text="Change Background" 
            android:textAlignment="center" 
            android:textColor="#FF9800" 
            android:textSize="48sp" 
            android:textStyle="bold" /> 
 
        <Button 
            android:id="@+id/red" 
            android:layout_width="120dp" 
            android:layout_height="wrap_content" 
            android:layout_marginLeft="140dp" 
            android:layout_marginBottom="50dp" 
            android:text="RED" 
            android:textColor="#E60F16" 
            android:textSize="34sp" 
            android:textStyle="bold" /> 
 
        <Button 
            android:id="@+id/green" 
            android:layout_width="wrap_content" 
            android:layout_height="wrap_content" 
            android:layout_marginLeft="120dp" 
            android:layout_marginBottom="50dp" 
            android:text="GREEN" 
            android:textColor="#1CCE23" 
            android:textSize="34sp" /> 
 
        <Button 
            android:id="@+id/img" 
            android:layout_width="wrap_content" 
            android:layout_height="wrap_content" 
            android:layout_marginLeft="130dp" 
            android:text="Image" 
            android:textColor="#FFC107" 
            android:textSize="34sp" /> 
    </LinearLayout> 
</androidx.constraintlayout.widget.ConstraintLayout> 
 
MainActivity.java 
package com.example. backgroundchange; 
import android.os.Bundle; 
import android.view.View; 
import android.widget.Button; 
import android.widget.LinearLayout; 
import androidx.activity.EdgeToEdge; 
import androidx.appcompat.app.AppCompatActivity; 
import androidx.core.graphics.Insets; 
import androidx.core.view.ViewCompat; 
import androidx.core.view.WindowInsetsCompat; 
public class MainActivity extends AppCompatActivity { 
Button red,green,img; 
LinearLayout ll; 
@Override 
protected void onCreate(Bundle savedInstanceState) { 
super.onCreate(savedInstanceState); 
EdgeToEdge.enable(this); 
setContentView(R.layout.activity_main); 
ViewCompat.setOnApplyWindowInsetsListener(findViewById(R.id.main
 ), (v, insets) -> { 
Insets systemBars = 
insets.getInsets(WindowInsetsCompat.Type.systemBars()); 
v.setPadding(systemBars.left, systemBars.top, 
systemBars.right, systemBars.bottom); 
return insets; 
}); 
red = (Button) findViewById(R.id.red); 
green = (Button) findViewById(R.id.green); 
img = (Button) findViewById(R.id.img); 
ll = (LinearLayout)findViewById(R.id.ll); 
red.setOnClickListener(new View.OnClickListener() { 
@Override 
public void onClick(View view) { 
ll.setBackgroundResource(R.color.RED); 
} 
}); 
green.setOnClickListener(new View.OnClickListener() { 
@Override 
public void onClick(View view) { 
ll.setBackgroundResource(R.color.GREEN); 
} 
}); 
img.setOnClickListener(new View.OnClickListener() { 
@Override 
public void onClick(View view) { 
ll.setBackgroundResource(R.drawable.background); 
} 
}); 
} 
} 
colors.xml 
<color name="RED">#EB1D1D</color> 
<color name="GREEN">#1CCE23</color> 
OUTPUT ON EMULATOR: 
EXPERIMENT NO.: 6 
Aim: To develop a simple Android application to Calculate Simple and Compound Interest. 
1. Open android studio and select new android project by clicking Filemenu  New New 
Project. 
2. Choose the project as Empty Views Activity and click Next. 
3. Give project name (Start with a capital letter) as Interestcalculator  
4. Choose the language as Java. 
5. Choose the required android version (Minimum SDK) and select finish. 
6. Go to package explorer in the left hand side and select the project. 
7. Under the project, Go to res folder and select layout. 
8. Double click the activity_main.xml file and design the layout for the page. 
9. Select MainActivity.java file and type the program. 
10.  Now go to activity_main.xml and right click & select run as option and select run 
configuration OR select the virtual device and click on run icon. 
11.  Android output will be displayed on the android emulator. 
Both activity_main.xml and MainActivity.java files together make our application work. The 
activity_main.xml is responsible for the layout (Front end User Interface) of the application. And 
the file MainActivity is responsible for the actions and the performance of the application (back 
end). 
Code: 
activity_main.xml 
<?xml version="1.0" encoding="utf-8"?> 
<androidx.constraintlayout.widget.ConstraintLayout 
xmlns:android="http://schemas.android.com/apk/res/android" 
xmlns:app="http://schemas.android.com/apk/res-auto" 
xmlns:tools="http://schemas.android.com/tools" 
android:id="@+id/main" 
android:layout_width="match_parent" 
android:layout_height="match_parent" 
android:background="#F4F6E5" 
tools:context=".MainActivity"> 
<TextView 
android:id="@+id/textView3" 
android:layout_width="wrap_content" 
android:layout_height="wrap_content" 
android:text="Interest Calculator" 
android:textColor="#D207F4" 
android:textSize="48sp" 
android:textStyle="bold" 
app:layout_constraintBottom_toBottomOf="parent" 
app:layout_constraintEnd_toEndOf="parent" 
        app:layout_constraintHorizontal_bias="0.454" 
        app:layout_constraintStart_toStartOf="parent" 
        app:layout_constraintTop_toTopOf="parent" 
        app:layout_constraintVertical_bias="0.038" /> 
 
    <EditText 
        android:id="@+id/p" 
        android:layout_width="wrap_content" 
        android:layout_height="wrap_content" 
        android:layout_marginTop="20dp" 
        android:ems="10" 
        android:hint="Enter Principal Amount" 
        android:inputType="text" 
        android:textSize="24sp" 
        app:layout_constraintEnd_toEndOf="parent" 
        app:layout_constraintHorizontal_bias="0.518" 
        app:layout_constraintStart_toStartOf="parent" 
        app:layout_constraintTop_toBottomOf="@+id/textView3" /> 
 
    <EditText 
        android:id="@+id/r" 
        android:layout_width="wrap_content" 
        android:layout_height="wrap_content" 
        android:layout_marginTop="23dp" 
        android:ems="10" 
        android:hint="Enter rate of Interest" 
        android:inputType="text" 
        android:textSize="24sp" 
        app:layout_constraintStart_toStartOf="@+id/p" 
        app:layout_constraintTop_toBottomOf="@+id/p" /> 
 
    <EditText 
        android:id="@+id/t" 
        android:layout_width="wrap_content" 
        android:layout_height="wrap_content" 
        android:layout_marginStart="4dp" 
        android:layout_marginBottom="44dp" 
        android:ems="10" 
        android:hint="Enter time period" 
        android:inputType="text" 
        android:textSize="24sp" 
        app:layout_constraintBottom_toTopOf="@+id/t1" 
        app:layout_constraintStart_toStartOf="@+id/t1" /> 
 
    <TextView 
        android:id="@+id/t1" 
        android:layout_width="wrap_content" 
        android:layout_height="wrap_content" 
        android:layout_marginStart="64dp" 
android:layout_marginTop="164dp" 
android:layout_marginBottom="166dp" 
android:text="Interest:" 
android:textSize="34sp" 
app:layout_constraintBottom_toBottomOf="@+id/si" 
app:layout_constraintStart_toStartOf="parent" 
app:layout_constraintTop_toBottomOf="@+id/p" 
app:layout_constraintVertical_bias="1.0" /> 
<TextView 
android:id="@+id/t2" 
android:layout_width="wrap_content" 
android:layout_height="wrap_content" 
android:layout_marginTop="44dp" 
android:text="Total Amount:" 
android:textSize="34sp" 
app:layout_constraintStart_toStartOf="@+id/t1" 
app:layout_constraintTop_toBottomOf="@+id/t1" /> 
<Button 
android:id="@+id/si" 
android:layout_width="wrap_content" 
android:layout_height="wrap_content" 
android:layout_marginEnd="21dp" 
android:layout_marginBottom="23dp" 
android:text="Simple Interest" 
android:textSize="24sp" 
app:layout_constraintBottom_toTopOf="@+id/ci" 
app:layout_constraintEnd_toEndOf="@+id/ci" /> 
<Button 
android:id="@+id/ci" 
android:layout_width="wrap_content" 
android:layout_height="wrap_content" 
android:layout_marginEnd="65dp" 
android:layout_marginBottom="83dp" 
android:text="Compound Interest" 
android:textSize="24sp" 
app:layout_constraintBottom_toBottomOf="parent" 
app:layout_constraintEnd_toEndOf="parent" /> 
</androidx.constraintlayout.widget.ConstraintLayout> 
MainActivity.java 
package com.example.interestcalculator; 
import android.os.Bundle; 
import android.view.View; 
import android.widget.Button; 
import android.widget.EditText; 
import android.widget.TextView; 
import android.widget.Toast; 
import androidx.activity.EdgeToEdge; 
import androidx.appcompat.app.AppCompatActivity; 
import androidx.core.graphics.Insets; 
import androidx.core.view.ViewCompat; 
import androidx.core.view.WindowInsetsCompat; 
public class MainActivity extends AppCompatActivity { 
EditText p, t, r; 
TextView t1,t2; 
Button s, c; 
int p1, r1, time; 
float s1, c1, tot; 
@Override 
protected void onCreate(Bundle savedInstanceState) { 
super.onCreate(savedInstanceState); 
EdgeToEdge.enable(this); 
setContentView(R.layout.activity_main); 
ViewCompat.setOnApplyWindowInsetsListener(findViewById(R.id.main
 ), (v, insets) -> { 
Insets systemBars = 
insets.getInsets(WindowInsetsCompat.Type.systemBars()); 
v.setPadding(systemBars.left, systemBars.top, 
systemBars.right, systemBars.bottom); 
return insets; 
}); 
p = (EditText) findViewById(R.id.p); 
r = (EditText) findViewById(R.id.r); 
t = (EditText) findViewById(R.id.t); 
t1 = (TextView) findViewById(R.id.t1); 
t2 = (TextView) findViewById(R.id.t2); 
s = (Button) findViewById(R.id.si); 
c = (Button) findViewById(R.id.ci); 
s.setOnClickListener(new View.OnClickListener() { 
@Override 
public void onClick(View view) { 
p1 =Integer.parseInt(p.getText().toString()); 
r1 =Integer.parseInt(r.getText().toString()); 
time =Integer.parseInt(t.getText().toString()); 
s1 = (p1*r1*time)/100; 
tot = p1+s1; 
t1.setText("Interest is:"+String.valueOf(s1)); 
t2.setText("Total Amount 
is"+String.valueOf(tot)); 
} 
}); 
c.setOnClickListener(new View.OnClickListener() { 
@Override 
public void onClick(View view) { 
p1 =Integer.parseInt(p.getText().toString()); 
r1 =Integer.parseInt(r.getText().toString()); 
time =Integer.parseInt(t.getText().toString()); 
double total = p1*Math.pow(1 + (double) r1 /100, time); 
double c2 = total - p1; 
t1.setText("Interest is:"+String.valueOf(c2)); 
t2.setText("Total Amount is"+String.valueOf(total)); 
} 
}); 
} 
} 
OUTPUT ON EMULATOR: 
EXPERIMENT NO.: 7 
Aim: To develop a simple Android application to Calculate roots of a Quadratic equation. 
1. Open android studio and select new android project by clicking Filemenu  New New 
Project. 
2. Choose the project as Empty Views Activity and click Next. 
3. Give project name (Start with a capital letter) as Quadraticroots  
4. Choose the language as Java. 
5. Choose the required android version (Minimum SDK) and select finish. 
6. Go to package explorer in the left hand side and select the project. 
7. Under the project, Go to res folder and select layout. 
8. Double click the activity_main.xml file and design the layout for the page. 
9. Select MainActivity.java file and type the program. 
10.  Now go to activity_main.xml and right click & select run as option and select run 
configuration OR select the virtual device and click on run icon. 
11.  Android output will be displayed on the android emulator. 
Both activity_main.xml and MainActivity.java files together make our application work. The 
activity_main.xml is responsible for the layout (Front end User Interface) of the application. And 
the file MainActivity is responsible for the actions and the performance of the application (back 
end). 
Code: 
activity_main.xml 
<?xml version="1.0" encoding="utf-8"?> 
<androidx.constraintlayout.widget.ConstraintLayout 
xmlns:android="http://schemas.android.com/apk/res/android" 
xmlns:app="http://schemas.android.com/apk/res-auto" 
xmlns:tools="http://schemas.android.com/tools" 
android:id="@+id/main" 
android:layout_width="match_parent" 
android:layout_height="match_parent" 
tools:context=".MainActivity"> 
<TextView 
android:id="@+id/textView4" 
android:layout_width="wrap_content" 
android:layout_height="wrap_content" 
android:text="Quadratic Roots" 
android:textColor="#D91E1E" 
android:textSize="48sp" 
android:textStyle="bold" 
app:layout_constraintBottom_toBottomOf="parent" 
app:layout_constraintEnd_toEndOf="parent" 
        app:layout_constraintStart_toStartOf="parent" 
        app:layout_constraintTop_toTopOf="parent" 
        app:layout_constraintVertical_bias="0.056" /> 
 
    <EditText 
        android:id="@+id/a" 
        android:layout_width="wrap_content" 
        android:layout_height="wrap_content" 
        android:layout_marginTop="33dp" 
        android:layout_marginEnd="21dp" 
        android:ems="10" 
        android:hint="Enter Value of a" 
        android:inputType="text" 
        android:textSize="24sp" 
        app:layout_constraintEnd_toEndOf="@+id/textView4" 
        app:layout_constraintTop_toBottomOf="@+id/textView4" /> 
 
    <EditText 
        android:id="@+id/b" 
        android:layout_width="wrap_content" 
        android:layout_height="wrap_content" 
        android:layout_marginTop="37dp" 
        android:ems="10" 
        android:hint="Enter Value of B" 
        android:inputType="text" 
        android:textSize="24sp" 
        app:layout_constraintEnd_toEndOf="@+id/a" 
        app:layout_constraintStart_toStartOf="@+id/a" 
        app:layout_constraintTop_toBottomOf="@+id/a" /> 
 
    <EditText 
        android:id="@+id/c" 
        android:layout_width="wrap_content" 
        android:layout_height="wrap_content" 
        android:layout_marginTop="35dp" 
        android:ems="10" 
        android:hint="Enter Value of c" 
        android:inputType="text" 
        android:textSize="24sp" 
        app:layout_constraintStart_toStartOf="@+id/b" 
        app:layout_constraintTop_toBottomOf="@+id/b" /> 
 
    <TextView 
        android:id="@+id/r1" 
        android:layout_width="wrap_content" 
        android:layout_height="wrap_content" 
        android:layout_marginStart="10dp" 
        android:layout_marginTop="25dp" 
        android:text="Root 1:" 
android:textSize="24sp" 
app:layout_constraintStart_toStartOf="@+id/c" 
app:layout_constraintTop_toBottomOf="@+id/c" /> 
<TextView 
android:id="@+id/r2" 
android:layout_width="wrap_content" 
android:layout_height="wrap_content" 
android:layout_marginTop="29dp" 
android:text="Root 2:" 
android:textSize="24sp" 
app:layout_constraintStart_toStartOf="@+id/r1" 
app:layout_constraintTop_toBottomOf="@+id/r1" /> 
<TextView 
android:id="@+id/type" 
android:layout_width="wrap_content" 
android:layout_height="wrap_content" 
android:layout_marginTop="32dp" 
android:text="Roots are: " 
android:textSize="24sp" 
app:layout_constraintStart_toStartOf="@+id/r2" 
app:layout_constraintTop_toBottomOf="@+id/r2" /> 
<Button 
android:id="@+id/button" 
android:layout_width="wrap_content" 
android:layout_height="wrap_content" 
android:layout_marginStart="51dp" 
android:layout_marginBottom="87dp" 
android:text="Calculate Quad Roots" 
android:textSize="24sp" 
app:layout_constraintBottom_toBottomOf="parent" 
app:layout_constraintStart_toStartOf="parent" /> 
</androidx.constraintlayout.widget.ConstraintLayout> 
MainActivity.java 
package com.example.quadraticroots; 
import android.os.Bundle; 
import android.view.View; 
import android.widget.Button; 
import android.widget.EditText; 
import android.widget.TextView; 
import androidx.activity.EdgeToEdge; 
import androidx.appcompat.app.AppCompatActivity; 
import androidx.core.graphics.Insets; 
import androidx.core.view.ViewCompat; 
import androidx.core.view.WindowInsetsCompat; 
public class MainActivity extends AppCompatActivity { 
EditText a,b,c; 
TextView r1,r2,type; 
Button button; 
int a1,b1,c1; 
double root1,root2; 
@Override 
protected void onCreate(Bundle savedInstanceState) { 
super.onCreate(savedInstanceState); 
EdgeToEdge.enable(this); 
setContentView(R.layout.activity_main); 
ViewCompat.setOnApplyWindowInsetsListener(findViewById(R.id.main
 ), (v, insets) -> { 
Insets systemBars = 
insets.getInsets(WindowInsetsCompat.Type.systemBars()); 
v.setPadding(systemBars.left, systemBars.top, 
systemBars.right, systemBars.bottom); 
return insets; 
}); 
a = (EditText) findViewById(R.id.a); 
b = (EditText) findViewById(R.id.b); 
c = (EditText) findViewById(R.id.c); 
r1 = (TextView) findViewById(R.id.r1); 
r2 = (TextView) findViewById(R.id.r2); 
type = (TextView) findViewById(R.id.type); 
button = (Button) findViewById(R.id.button); 
button.setOnClickListener(new View.OnClickListener() { 
@Override 
public void onClick(View view) { 
a1 = Integer.parseInt(a.getText().toString()); 
b1 = Integer.parseInt(b.getText().toString()); 
c1 = Integer.parseInt(c.getText().toString()); 
double d = (b1*b1)-(4*a1*c1); 
if (d<0) 
{ 
r1.setText("Root 1:Not determined"); 
r2.setText("Root 2:Not determined "); 
type.setText("Root are imaginary "); 
} 
else { 
root1 = (-b1 + Math.sqrt(d)) / 2 * a1; 
root2 = (-b1 - Math.sqrt(d)) / 2 * a1; 
r1.setText("Root 1: " + String.valueOf(root1)); 
r2.setText("Root 2:" + String.valueOf(root2)); 
if (root1==root2) 
type.setText("Root are Equal"); 
else 
type.setText("Root are Distinct"); 
} 
} 
}); 
} 
} 
OUTPUT ON EMULATOR: 
EXPERIMENT NO.: 8 
Aim: To develop a simple Android application to convert temperature between degree Celsius 
and Fahrenheit. 
1. Open android studio and select new android project by clicking Filemenu  New New 
Project. 
2. Choose the project as Empty Views Activity and click Next. 
3. Give project name (Start with a capital letter) as TemperatureConvert  
4. Choose the language as Java. 
5. Choose the required android version (Minimum SDK) and select finish. 
6. Go to package explorer in the left hand side and select the project. 
7. Under the project, Go to res folder and select layout. 
8. Double click the activity_main.xml file and design the layout for the page. 
9. Select MainActivity.java file and type the program. 
10.  Now go to activity_main.xml and right click & select run as option and select run 
configuration OR select the virtual device and click on run icon. 
11.  Android output will be displayed on the android emulator. 
Both activity_main.xml and MainActivity.java files together make our application work. The 
activity_main.xml is responsible for the layout (Front end User Interface) of the application. And 
the file MainActivity is responsible for the actions and the performance of the application (back 
end). 
Code: 
activity_main.xml 
<?xml version="1.0" encoding="utf-8"?> 
<androidx.constraintlayout.widget.ConstraintLayout 
xmlns:android="http://schemas.android.com/apk/res/android" 
xmlns:app="http://schemas.android.com/apk/res-auto" 
xmlns:tools="http://schemas.android.com/tools" 
android:id="@+id/main" 
android:layout_width="match_parent" 
android:layout_height="match_parent" 
android:background="#C8EBD5" 
tools:context=".MainActivity"> 
<TextView 
android:id="@+id/textView3" 
android:layout_width="wrap_content" 
android:layout_height="wrap_content" 
android:layout_marginTop="45dp" 
android:layout_marginBottom="53dp" 
android:background="#FFEB3B" 
android:text="Temperature Convertor" 
android:textColor="#DE0C0C" 
        android:textSize="34sp" 
        android:textStyle="bold" 
        app:layout_constraintBottom_toTopOf="@+id/t" 
        app:layout_constraintEnd_toEndOf="parent" 
        app:layout_constraintStart_toStartOf="parent" 
        app:layout_constraintTop_toTopOf="parent" 
        app:layout_constraintVertical_bias="0.066" /> 
 
    <TextView 
        android:id="@+id/textView" 
        android:layout_width="wrap_content" 
        android:layout_height="wrap_content" 
        android:layout_marginStart="41dp" 
        android:layout_marginEnd="14dp" 
        android:text="Enter Temperature" 
        android:textSize="24sp" 
        app:layout_constraintBaseline_toBaselineOf="@+id/t" 
        app:layout_constraintEnd_toStartOf="@+id/t" 
        app:layout_constraintStart_toStartOf="parent" /> 
 
    <EditText 
        android:id="@+id/t" 
        android:layout_width="0dp" 
        android:layout_height="0dp" 
        android:layout_marginEnd="39dp" 
        android:layout_marginBottom="45dp" 
        android:ems="10" 
        android:inputType="text" 
        android:textSize="24sp" 
        app:layout_constraintBottom_toTopOf="@+id/res" 
        app:layout_constraintEnd_toEndOf="parent" 
        app:layout_constraintStart_toEndOf="@+id/textView" 
        app:layout_constraintTop_toBottomOf="@+id/textView3" /> 
 
    <TextView 
        android:id="@+id/res" 
        android:layout_width="wrap_content" 
        android:layout_height="wrap_content" 
        android:layout_marginStart="41dp" 
        android:layout_marginBottom="64dp" 
        android:text="Result:" 
        android:textSize="24sp" 
        app:layout_constraintBottom_toTopOf="@+id/radioGroup" 
        app:layout_constraintStart_toStartOf="parent" 
        app:layout_constraintTop_toBottomOf="@+id/t" /> 
 
    <RadioGroup 
        android:id="@+id/radioGroup" 
        android:layout_width="wrap_content" 
android:layout_height="wrap_content" 
android:layout_marginStart="33dp" 
android:layout_marginBottom="81dp" 
app:layout_constraintBottom_toTopOf="@+id/con" 
app:layout_constraintStart_toStartOf="parent" 
app:layout_constraintTop_toBottomOf="@+id/res"> 
<RadioButton 
android:id="@+id/cf" 
android:layout_width="match_parent" 
android:layout_height="wrap_content" 
android:text="Deg Celsius to Farhenheit" 
android:textSize="20sp" /> 
<RadioButton 
android:id="@+id/fc" 
android:layout_width="match_parent" 
android:layout_height="wrap_content" 
android:text="Farehenheit to Deg Celcius" 
android:textSize="20sp" /> 
</RadioGroup> 
<Button 
android:id="@+id/con" 
android:layout_width="wrap_content" 
android:layout_height="wrap_content" 
android:layout_marginEnd="41dp" 
android:layout_marginBottom="174dp" 
android:text="Convert" 
android:textSize="24sp" 
app:layout_constraintBottom_toBottomOf="parent" 
app:layout_constraintEnd_toEndOf="@+id/radioGroup" 
app:layout_constraintTop_toBottomOf="@+id/radioGroup" /> 
</androidx.constraintlayout.widget.ConstraintLayout> 
MainActivity.java 
package com.example.temperatureconvert; 
import android.os.Bundle; 
import android.view.View; 
import android.widget.Button; 
import android.widget.EditText; 
import android.widget.RadioButton; 
import android.widget.TextView; 
import androidx.activity.EdgeToEdge; 
import androidx.appcompat.app.AppCompatActivity; 
import androidx.core.graphics.Insets; 
import androidx.core.view.ViewCompat; 
import androidx.core.view.WindowInsetsCompat; 
public class MainActivity extends AppCompatActivity { 
EditText temp; 
TextView res; 
RadioButton cf,fc; 
Button con; 
@Override 
protected void onCreate(Bundle savedInstanceState) { 
super.onCreate(savedInstanceState); 
EdgeToEdge.enable(this); 
setContentView(R.layout.activity_main); 
ViewCompat.setOnApplyWindowInsetsListener(findViewById(R.id.main
 ), (v, insets) -> { 
Insets systemBars = 
insets.getInsets(WindowInsetsCompat.Type.systemBars()); 
v.setPadding(systemBars.left, systemBars.top, 
systemBars.right, systemBars.bottom); 
return insets; 
}); 
temp = (EditText) findViewById(R.id.t); 
res = (TextView) findViewById(R.id.res); 
cf = (RadioButton) findViewById(R.id.cf); 
fc = (RadioButton) findViewById(R.id.fc); 
con = (Button) findViewById(R.id.con); 
con.setOnClickListener(new View.OnClickListener() { 
@Override 
public void onClick(View v) { 
double r=0; 
int t = 
Integer.parseInt(temp.getText().toString()); 
if(cf.isChecked()) 
{ 
r = (double) (t*9)/5 + 32; 
} 
if(fc.isChecked()) 
{ 
r = (double) (t-32)*5/9; 
} 
                res.setText("Result is: "+String.valueOf(r)); 
            } 
        }); 
    } 
} 
 
OUTPUT ON EMULATOR: 
 
   
 
 
 
 
 
 
 
 
 
 
EXPERIMENT NO.: 9 
Aim: To develop a simple Android application to validate Login form with Toast. 
1. Open android studio and select new android project by clicking Filemenu  New New 
Project. 
2. Choose the project as Empty Views Activity and click Next. 
3. Give project name (Start with a capital letter) as LoginValidation  
4. Choose the language as Java. 
5. Choose the required android version (Minimum SDK) and select finish. 
6. Go to package explorer in the left hand side and select the project. 
7. Under the project, Go to res folder and select layout. 
8. Double click the activity_main.xml file and design the layout for the page. 
9. Select MainActivity.java file and type the program. 
10.  Now go to activity_main.xml and right click & select run as option and select run 
configuration OR select the virtual device and click on run icon. 
11.  Android output will be displayed on the android emulator. 
Both activity_main.xml and MainActivity.java files together make our application work. The 
activity_main.xml is responsible for the layout (Front end User Interface) of the application. And 
the file MainActivity is responsible for the actions and the performance of the application (back 
end). 
Code: 
activity_main.xml 
<?xml version="1.0" encoding="utf-8"?> 
<androidx.constraintlayout.widget.ConstraintLayout 
xmlns:android="http://schemas.android.com/apk/res/android" 
xmlns:app="http://schemas.android.com/apk/res-auto" 
xmlns:tools="http://schemas.android.com/tools" 
android:id="@+id/main" 
android:layout_width="match_parent" 
android:layout_height="match_parent" 
tools:context=".MainActivity"> 
<TextView 
android:id="@+id/textView3" 
android:layout_width="wrap_content" 
android:layout_height="wrap_content" 
android:text="Login Form" 
android:textColor="#E61616" 
android:textSize="48sp" 
android:textStyle="bold" 
app:layout_constraintBottom_toBottomOf="parent" 
app:layout_constraintEnd_toEndOf="parent" 
app:layout_constraintStart_toStartOf="parent" 
        app:layout_constraintTop_toTopOf="parent" 
        app:layout_constraintVertical_bias="0.052" /> 
 
    <TextView 
        android:id="@+id/textView" 
        android:layout_width="wrap_content" 
        android:layout_height="wrap_content" 
        android:layout_marginStart="16dp" 
        android:layout_marginTop="148dp" 
        android:layout_marginEnd="30dp" 
        android:layout_marginBottom="48dp" 
        android:text="Enter Username:" 
        android:textSize="20sp" 
        android:textStyle="bold" 
        app:layout_constraintBottom_toTopOf="@+id/textView2" 
        app:layout_constraintEnd_toStartOf="@+id/un" 
        app:layout_constraintStart_toStartOf="parent" 
        app:layout_constraintTop_toTopOf="parent" /> 
 
    <EditText 
        android:id="@+id/un" 
        android:layout_width="0dp" 
        android:layout_height="0dp" 
        android:layout_marginTop="148dp" 
        android:layout_marginEnd="31dp" 
        android:layout_marginBottom="28dp" 
        android:ems="10" 
        android:inputType="text" 
        android:textSize="24sp" 
        app:layout_constraintBottom_toTopOf="@+id/pwd" 
        app:layout_constraintEnd_toEndOf="parent" 
        app:layout_constraintStart_toEndOf="@+id/textView" 
        app:layout_constraintTop_toTopOf="parent" /> 
 
    <TextView 
        android:id="@+id/textView2" 
        android:layout_width="wrap_content" 
        android:layout_height="wrap_content" 
        android:layout_marginStart="15dp" 
        android:layout_marginEnd="34dp" 
        android:layout_marginBottom="118dp" 
        android:text="Enter Password:" 
        android:textSize="20sp" 
        android:textStyle="bold" 
        app:layout_constraintBottom_toTopOf="@+id/button" 
        app:layout_constraintEnd_toStartOf="@+id/pwd" 
        app:layout_constraintStart_toStartOf="parent" 
        app:layout_constraintTop_toBottomOf="@+id/textView" /> 
 
<EditText 
android:id="@+id/pwd" 
android:layout_width="0dp" 
android:layout_height="0dp" 
android:layout_marginEnd="43dp" 
android:layout_marginBottom="481dp" 
android:ems="10" 
android:inputType="textPassword" 
android:textSize="24sp" 
app:layout_constraintBottom_toBottomOf="parent" 
app:layout_constraintEnd_toEndOf="parent" 
app:layout_constraintStart_toEndOf="@+id/textView2" 
app:layout_constraintTop_toBottomOf="@+id/un" /> 
<Button 
android:id="@+id/button" 
android:layout_width="184dp" 
android:layout_height="0dp" 
android:layout_marginBottom="313dp" 
android:text="Login" 
android:textColorLink="#E21C1C" 
android:textSize="24sp" 
android:textStyle="bold" 
app:layout_constraintBottom_toBottomOf="parent" 
app:layout_constraintEnd_toEndOf="parent" 
app:layout_constraintStart_toStartOf="parent" 
app:layout_constraintTop_toBottomOf="@+id/textView2" /> 
</androidx.constraintlayout.widget.ConstraintLayout> 
MainActivity.java 
package com.example.loginvalidation; 
import android.os.Bundle; 
import android.view.View; 
import android.widget.Button; 
import android.widget.EditText; 
import android.widget.Toast; 
import androidx.activity.EdgeToEdge; 
import androidx.appcompat.app.AppCompatActivity; 
import androidx.core.graphics.Insets; 
import androidx.core.view.ViewCompat; 
import androidx.core.view.WindowInsetsCompat; 
public class MainActivity extends AppCompatActivity { 
 
    EditText un,pwd; 
    Button login; 
    String user, pass; 
    @Override 
    protected void onCreate(Bundle savedInstanceState) { 
        super.onCreate(savedInstanceState); 
        EdgeToEdge.enable(this); 
        setContentView(R.layout.activity_main); 
        
ViewCompat.setOnApplyWindowInsetsListener(findViewById(R.id.main
 ), (v, insets) -> { 
            Insets systemBars = 
insets.getInsets(WindowInsetsCompat.Type.systemBars()); 
            v.setPadding(systemBars.left, systemBars.top, 
systemBars.right, systemBars.bottom); 
            return insets; 
        }); 
 
        un = (EditText) findViewById(R.id.un); 
        pwd = (EditText) findViewById(R.id.pwd); 
 
        login = (Button) findViewById(R.id.button); 
 
        login.setOnClickListener(new View.OnClickListener() { 
            @Override 
            public void onClick(View view) { 
 
                user = un.getText().toString(); 
                pass = pwd.getText().toString(); 
 
                if (user.equals("MVSREC") && pass.equals("itd")) 
                { 
                    Toast.makeText(MainActivity.this, "Login 
Successful", Toast.LENGTH_LONG).show(); 
                   
                } 
                else 
                { 
                    Toast.makeText(MainActivity.this, "Login 
Failed", Toast.LENGTH_LONG).show(); 
                } 
            } 
        }); 
 
 
    } 
} 
OUTPUT ON EMULATOR: 
EXPERIMENT NO.: 10 
Aim: To develop a simple Android application to validate Login form with navigation. 
1. Open android studio and select new android project by clicking Filemenu  New New 
Project. 
2. Choose the project as Empty Views Activity and click Next. 
3. Give project name (Start with a capital letter) as LoginwithNavigation  
4. Choose the language as Java. 
5. Choose the required android version (Minimum SDK) and select finish. 
6. Go to package explorer in the left hand side and select the project. 
7. To add a new activity file, Go to Menu at top left corner, Filemenu  new activity 
empty views activity. 
8. A new activity xml file, a java file will be added and new activity will be added to Andriod 
Manifest.xml file 
9. Add two activity files, success.xml and failure.xml and also Success.java and Failure.java.  
10. Under the project, Go to res folder and select layout. 
11. Double click the activity_main.xml file and design the layout for the page. 
12. Select MainActivity.java file and type the program. 
13.  Now go to activity_main.xml and right click & select run as option and select run 
configuration OR select the virtual device and click on run icon. 
14.  Android output will be displayed on the android emulator. 
Both activity_main.xml and MainActivity.java files together make our application work. The 
activity_main.xml is responsible for the layout (Front end User Interface) of the application. And 
the file MainActivity is responsible for the actions and the performance of the application (back 
end). 
Code: 
activity_main.xml 
<?xml version="1.0" encoding="utf-8"?> 
<androidx.constraintlayout.widget.ConstraintLayout 
xmlns:android="http://schemas.android.com/apk/res/android" 
xmlns:app="http://schemas.android.com/apk/res-auto" 
xmlns:tools="http://schemas.android.com/tools" 
android:id="@+id/main" 
android:layout_width="match_parent" 
android:layout_height="match_parent" 
tools:context=".MainActivity"> 
<TextView 
android:id="@+id/textView3" 
android:layout_width="wrap_content" 
android:layout_height="wrap_content" 
        android:text="Login Form" 
        android:textColor="#E61616" 
        android:textSize="48sp" 
        android:textStyle="bold" 
        app:layout_constraintBottom_toBottomOf="parent" 
        app:layout_constraintEnd_toEndOf="parent" 
        app:layout_constraintStart_toStartOf="parent" 
        app:layout_constraintTop_toTopOf="parent" 
        app:layout_constraintVertical_bias="0.052" /> 
 
    <TextView 
        android:id="@+id/textView" 
        android:layout_width="wrap_content" 
        android:layout_height="wrap_content" 
        android:layout_marginStart="16dp" 
        android:layout_marginTop="148dp" 
        android:layout_marginEnd="30dp" 
        android:layout_marginBottom="48dp" 
        android:text="Enter Username:" 
        android:textSize="20sp" 
        android:textStyle="bold" 
        app:layout_constraintBottom_toTopOf="@+id/textView2" 
        app:layout_constraintEnd_toStartOf="@+id/un" 
        app:layout_constraintStart_toStartOf="parent" 
        app:layout_constraintTop_toTopOf="parent" /> 
 
    <EditText 
        android:id="@+id/un" 
        android:layout_width="0dp" 
        android:layout_height="0dp" 
        android:layout_marginTop="148dp" 
        android:layout_marginEnd="31dp" 
        android:layout_marginBottom="28dp" 
        android:ems="10" 
        android:inputType="text" 
        android:textSize="24sp" 
        app:layout_constraintBottom_toTopOf="@+id/pwd" 
        app:layout_constraintEnd_toEndOf="parent" 
        app:layout_constraintStart_toEndOf="@+id/textView" 
        app:layout_constraintTop_toTopOf="parent" /> 
 
    <TextView 
        android:id="@+id/textView2" 
        android:layout_width="wrap_content" 
        android:layout_height="wrap_content" 
        android:layout_marginStart="15dp" 
        android:layout_marginEnd="34dp" 
        android:layout_marginBottom="118dp" 
        android:text="Enter Password:" 
android:textSize="20sp" 
android:textStyle="bold" 
app:layout_constraintBottom_toTopOf="@+id/button" 
app:layout_constraintEnd_toStartOf="@+id/pwd" 
app:layout_constraintStart_toStartOf="parent" 
app:layout_constraintTop_toBottomOf="@+id/textView" /> 
<EditText 
android:id="@+id/pwd" 
android:layout_width="0dp" 
android:layout_height="0dp" 
android:layout_marginEnd="43dp" 
android:layout_marginBottom="481dp" 
android:ems="10" 
android:inputType="textPassword" 
android:textSize="24sp" 
app:layout_constraintBottom_toBottomOf="parent" 
app:layout_constraintEnd_toEndOf="parent" 
app:layout_constraintStart_toEndOf="@+id/textView2" 
app:layout_constraintTop_toBottomOf="@+id/un" /> 
<Button 
android:id="@+id/button" 
android:layout_width="184dp" 
android:layout_height="0dp" 
android:layout_marginBottom="313dp" 
android:text="Login" 
android:textColorLink="#E21C1C" 
android:textSize="24sp" 
android:textStyle="bold" 
app:layout_constraintBottom_toBottomOf="parent" 
app:layout_constraintEnd_toEndOf="parent" 
app:layout_constraintStart_toStartOf="parent" 
app:layout_constraintTop_toBottomOf="@+id/textView2" /> 
</androidx.constraintlayout.widget.ConstraintLayout> 
success.xml 
<?xml version="1.0" encoding="utf-8"?> 
<androidx.constraintlayout.widget.ConstraintLayout 
xmlns:android="http://schemas.android.com/apk/res/android" 
xmlns:app="http://schemas.android.com/apk/res-auto" 
xmlns:tools="http://schemas.android.com/tools" 
android:id="@+id/main" 
android:layout_width="match_parent" 
android:layout_height="match_parent" 
android:background="#B4EBF2" 
tools:context=".Success"> 
<TextView 
android:id="@+id/textView5" 
android:layout_width="wrap_content" 
android:layout_height="wrap_content" 
android:text="Login Sucessfull" 
android:textColor="#E91E63" 
android:textSize="34sp" 
android:textStyle="bold" 
app:layout_constraintBottom_toBottomOf="parent" 
app:layout_constraintEnd_toEndOf="parent" 
app:layout_constraintHorizontal_bias="0.496" 
app:layout_constraintStart_toStartOf="parent" 
app:layout_constraintTop_toTopOf="parent" /> 
<TextView 
android:id="@+id/textView4" 
android:layout_width="wrap_content" 
android:layout_height="wrap_content" 
android:layout_marginTop="185dp" 
android:text="Home Page" 
android:textColor="#E91616" 
android:textSize="34sp" 
android:textStyle="bold" 
app:layout_constraintEnd_toEndOf="parent" 
app:layout_constraintStart_toStartOf="parent" 
app:layout_constraintTop_toTopOf="parent" /> 
</androidx.constraintlayout.widget.ConstraintLayout> 
failure.xml 
<?xml version="1.0" encoding="utf-8"?> 
<androidx.constraintlayout.widget.ConstraintLayout 
xmlns:android="http://schemas.android.com/apk/res/android" 
xmlns:app="http://schemas.android.com/apk/res-auto" 
xmlns:tools="http://schemas.android.com/tools" 
android:id="@+id/main" 
android:layout_width="match_parent" 
android:layout_height="match_parent" 
android:background="#EFE7B2" 
tools:context=".Failure"> 
<TextView 
android:id="@+id/textView6" 
android:layout_width="wrap_content" 
android:layout_height="wrap_content" 
android:text="Login Failed" 
android:textColor="#F44336" 
android:textSize="34sp" 
android:textStyle="bold" 
app:layout_constraintBottom_toBottomOf="parent" 
app:layout_constraintEnd_toEndOf="parent" 
app:layout_constraintHorizontal_bias="0.497" 
app:layout_constraintStart_toStartOf="parent" 
app:layout_constraintTop_toTopOf="parent" 
app:layout_constraintVertical_bias="0.206" /> 
<Button 
android:id="@+id/button2" 
android:layout_width="wrap_content" 
android:layout_height="wrap_content" 
android:layout_marginTop="297dp" 
android:text="Try Login Again" 
android:textSize="24sp" 
app:layout_constraintEnd_toEndOf="parent" 
app:layout_constraintStart_toStartOf="parent" 
app:layout_constraintTop_toTopOf="parent" /> 
</androidx.constraintlayout.widget.ConstraintLayout> 
MainActivity.java 
package com.example.loginnavigation; 
import android.content.Intent; 
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
EditText un,pwd; 
Button login; 
@Override 
protected void onCreate(Bundle savedInstanceState) { 
super.onCreate(savedInstanceState); 
EdgeToEdge.enable(this); 
setContentView(R.layout.activity_main); 
ViewCompat.setOnApplyWindowInsetsListener(findViewById(R.id.main
 ), (v, insets) -> { 
Insets systemBars = 
insets.getInsets(WindowInsetsCompat.Type.systemBars()); 
v.setPadding(systemBars.left, systemBars.top, 
systemBars.right, systemBars.bottom); 
return insets; 
}); 
un = (EditText) findViewById(R.id.un); 
pwd = (EditText) findViewById(R.id.pwd); 
login = (Button) findViewById(R.id.button); 
login.setOnClickListener(new View.OnClickListener() { 
@Override 
public void onClick(View view) { 
String user = un.getText().toString(); 
String pass = pwd.getText().toString(); 
if(user.equals("MVSREC") && pass.equals("itd")) 
{ 
Intent i = new Intent(getBaseContext(), Success.class); 
startActivity(i); 
} 
else { 
Intent i = new Intent(getBaseContext(), Failure.class); 
startActivity(i); 
} 
} 
}); 
} 
} 
Success.java 
package com.example.loginnavigation; 
import android.os.Bundle; 
import androidx.activity.EdgeToEdge; 
import androidx.appcompat.app.AppCompatActivity; 
import androidx.core.graphics.Insets; 
import androidx.core.view.ViewCompat; 
import androidx.core.view.WindowInsetsCompat; 
public class Success extends AppCompatActivity { 
@Override 
protected void onCreate(Bundle savedInstanceState) { 
super.onCreate(savedInstanceState); 
EdgeToEdge.enable(this); 
setContentView(R.layout.sucess); 
ViewCompat.setOnApplyWindowInsetsListener(findViewById(R.id.main
 ), (v, insets) -> { 
Insets systemBars = 
insets.getInsets(WindowInsetsCompat.Type.systemBars()); 
v.setPadding(systemBars.left, systemBars.top, 
systemBars.right, systemBars.bottom); 
return insets; 
}); 
} 
} 
Failure.java 
package com.example.loginnavigation; 
import android.content.Intent; 
import android.os.Bundle; 
import android.view.View; 
import android.widget.Button; 
import androidx.activity.EdgeToEdge; 
import androidx.appcompat.app.AppCompatActivity; 
import androidx.core.graphics.Insets; 
import androidx.core.view.ViewCompat; 
import androidx.core.view.WindowInsetsCompat; 
public class Failure extends AppCompatActivity { 
Button b; 
@Override 
protected void onCreate(Bundle savedInstanceState) { 
super.onCreate(savedInstanceState); 
EdgeToEdge.enable(this); 
setContentView(R.layout.failure); 
ViewCompat.setOnApplyWindowInsetsListener(findViewById(R.id.main
), (v, insets) -> { 
Insets systemBars = 
insets.getInsets(WindowInsetsCompat.Type.systemBars()); 
v.setPadding(systemBars.left, systemBars.top, 
systemBars.right, systemBars.bottom); 
return insets; 
}); 
b = (Button) findViewById(R.id.button2); 
b.setOnClickListener(new View.OnClickListener() { 
@Override 
public void onClick(View view) { 
Intent i = new Intent(getBaseContext(), MainActivity.class); 
startActivity(i); 
} 
}); 
} 
} 
AndroidManifest.xml 
<activity android:name=".Failure"></activity> 
<activity android:name=".Success"></activity> 
OUTPUT ON EMULATOR: 
EXPERIMENT NO.: 11 
Aim: To develop a simple Android application to send message from one page to other. 
1. Open android studio and select new android project by clicking Filemenu  New New 
Project. 
2. Choose the project as Empty Views Activity and click Next. 
3. Give project name (Start with a capital letter) as SendMessage  
4. Choose the language as Java. 
5. Choose the required android version (Minimum SDK) and select finish. 
6. To add a new activity file, go to Menu at top left corner, Filemenu  new activity 
empty views activity. 
7. A new activity xml file, a java file will be added and new activity will be added to Andriod 
Manifest.xml file 
8. One activity file, second.xml and Second.java will be added.  
9. Go to package explorer in the left hand side and select the project. 
10. Under the project, Go to res folder and select layout. 
11. Double click the activity_main.xml file and design the layout for the page. 
12. Select MainActivity.java file and type the program. 
13.  Now go to activity_main.xml and right click & select run as option and select run 
configuration OR select the virtual device and click on run icon. 
14.  Android output will be displayed on the android emulator. 
Both activity_main.xml and MainActivity.java files together make our application work. The 
activity_main.xml is responsible for the layout (Front end User Interface) of the application. And 
the file MainActivity is responsible for the actions and the performance of the application (back 
end). 
Code: 
activity_main.xml 
<?xml version="1.0" encoding="utf-8"?> 
<androidx.constraintlayout.widget.ConstraintLayout 
xmlns:android="http://schemas.android.com/apk/res/android" 
xmlns:app="http://schemas.android.com/apk/res-auto" 
xmlns:tools="http://schemas.android.com/tools" 
android:id="@+id/main" 
android:layout_width="match_parent" 
android:layout_height="match_parent" 
tools:context=".MainActivity"> 
<TextView 
android:id="@+id/textView" 
android:layout_width="wrap_content" 
android:layout_height="wrap_content" 
android:text="Send Message" 
android:textColor="#E91E63" 
android:textSize="34sp" 
android:textStyle="bold" 
app:layout_constraintBottom_toBottomOf="parent" 
app:layout_constraintEnd_toEndOf="parent" 
app:layout_constraintStart_toStartOf="parent" 
app:layout_constraintTop_toTopOf="parent" 
app:layout_constraintVertical_bias="0.142" /> 
<EditText 
android:id="@+id/msg" 
android:layout_width="252dp" 
android:layout_height="0dp" 
android:layout_marginTop="239dp" 
android:layout_marginBottom="86dp" 
android:ems="10" 
android:inputType="text" 
android:textSize="24sp" 
app:layout_constraintBottom_toTopOf="@+id/button" 
app:layout_constraintEnd_toEndOf="parent" 
app:layout_constraintStart_toStartOf="parent" 
app:layout_constraintTop_toTopOf="parent" /> 
<Button 
android:id="@+id/button" 
android:layout_width="wrap_content" 
android:layout_height="wrap_content" 
android:layout_marginBottom="271dp" 
android:text="Send Message" 
android:textSize="24sp" 
app:layout_constraintBottom_toBottomOf="parent" 
app:layout_constraintEnd_toEndOf="parent" 
app:layout_constraintStart_toStartOf="parent" 
app:layout_constraintTop_toBottomOf="@+id/msg" /> 
</androidx.constraintlayout.widget.ConstraintLayout> 
second.xml 
<?xml version="1.0" encoding="utf-8"?> 
<androidx.constraintlayout.widget.ConstraintLayout 
xmlns:android="http://schemas.android.com/apk/res/android" 
xmlns:app="http://schemas.android.com/apk/res-auto" 
xmlns:tools="http://schemas.android.com/tools" 
android:id="@+id/main" 
android:layout_width="match_parent" 
android:layout_height="match_parent" 
tools:context=".Second"> 
<TextView 
android:id="@+id/textView3" 
android:layout_width="wrap_content" 
android:layout_height="wrap_content" 
android:text="Second Page" 
android:textColor="#9C27B0" 
android:textSize="34sp" 
android:textStyle="bold" 
app:layout_constraintBottom_toBottomOf="parent" 
app:layout_constraintEnd_toEndOf="parent" 
app:layout_constraintHorizontal_bias="0.538" 
app:layout_constraintStart_toStartOf="parent" 
app:layout_constraintTop_toTopOf="parent" 
app:layout_constraintVertical_bias="0.15" /> 
<TextView 
android:id="@+id/textView2" 
android:layout_width="wrap_content" 
android:layout_height="wrap_content" 
android:layout_marginTop="269dp" 
android:text="Message is:" 
android:textColor="#E91A1A" 
android:textSize="24sp" 
app:layout_constraintEnd_toEndOf="parent" 
app:layout_constraintStart_toStartOf="parent" 
app:layout_constraintTop_toTopOf="parent" /> 
</androidx.constraintlayout.widget.ConstraintLayout> 
MainActivity.java 
package com.example.sendmessage; 
import android.content.Intent; 
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
EditText m; 
Button b; 
@Override 
protected void onCreate(Bundle savedInstanceState) { 
super.onCreate(savedInstanceState); 
EdgeToEdge.enable(this); 
setContentView(R.layout.activity_main); 
ViewCompat.setOnApplyWindowInsetsListener(findViewById(R.id.main
 ), (v, insets) -> { 
Insets systemBars = 
insets.getInsets(WindowInsetsCompat.Type.systemBars()); 
v.setPadding(systemBars.left, systemBars.top, 
systemBars.right, systemBars.bottom); 
return insets; 
}); 
m = (EditText) findViewById(R.id.msg); 
b = (Button) findViewById(R.id.button); 
b.setOnClickListener(new View.OnClickListener() { 
@Override 
public void onClick(View view) { 
String message = m.getText().toString(); 
Intent i = new Intent(getBaseContext(), Second.class); 
i.putExtra("key",message); 
startActivity(i); 
} 
}); 
} 
} 
Second.java 
package com.example.sendmessage; 
import android.content.Intent; 
import android.os.Bundle; 
import android.widget.TextView; 
import android.widget.Toast; 
import androidx.activity.EdgeToEdge; 
import androidx.appcompat.app.AppCompatActivity; 
import androidx.core.graphics.Insets; 
import androidx.core.view.ViewCompat; 
import androidx.core.view.WindowInsetsCompat; 
public class Second extends AppCompatActivity { 
TextView t; 
@Override 
protected void onCreate(Bundle savedInstanceState) { 
super.onCreate(savedInstanceState); 
EdgeToEdge.enable(this); 
setContentView(R.layout.second); 
ViewCompat.setOnApplyWindowInsetsListener(findViewById(R.id.main
 ), (v, insets) -> { 
Insets systemBars = 
insets.getInsets(WindowInsetsCompat.Type.systemBars()); 
v.setPadding(systemBars.left, systemBars.top, 
systemBars.right, systemBars.bottom); 
return insets; 
}); 
t = (TextView)findViewById(R.id.textView2); 
Intent i = getIntent(); 
String msg = i.getStringExtra("key"); 
t.setText("Message is: "+msg); 
Toast.makeText(getBaseContext(),"Received Msg from first 
Page",1).show(); 
} 
} 
OUTPUT ON EMULATOR: 
EXPERIMENT NO.: 12 
Aim: To develop a simple Android application to Navigate from one page to other. 
1. Open android studio and select new android project by clicking Filemenu  New New 
Project. 
2. Choose the project as Empty Views Activity and click Next. 
3. Give project name (Start with a capital letter) as Navigation  
4. Choose the language as Java. 
5. Choose the required android version (Minimum SDK) and select finish. 
6. To add a new activity file, go to Menu at top left corner, Filemenu  new activity 
empty views activity. 
7. A new activity xml file, a java file will be added and new activity will be added to Andriod 
Manifest.xml file 
8. Add two activity files, secondpage.xml and thirdpage.xml and also Secondpage.java and 
Thirdpage.java.  
9. Go to package explorer in the left hand side and select the project. 
10. Under the project, Go to res folder and select layout. 
11. Double click the activity_main.xml file and design the layout for the page. 
12. Select MainActivity.java file and type the program. 
13.  Now go to activity_main.xml and right click & select run as option and select run 
configuration OR select the virtual device and click on run icon. 
14.  Android output will be displayed on the android emulator. 
Both activity_main.xml and MainActivity.java files together make our application work. The 
activity_main.xml is responsible for the layout (Front end User Interface) of the application. And 
the file MainActivity is responsible for the actions and the performance of the application (back 
end). 
Code: 
activity_main.xml 
<?xml version="1.0" encoding="utf-8"?> 
<androidx.constraintlayout.widget.ConstraintLayout 
xmlns:android="http://schemas.android.com/apk/res/android" 
xmlns:app="http://schemas.android.com/apk/res-auto" 
xmlns:tools="http://schemas.android.com/tools" 
android:id="@+id/main" 
android:layout_width="match_parent" 
android:layout_height="match_parent" 
android:background="#D7EDBD" 
tools:context=".MainActivity"> 
<TextView 
android:id="@+id/textView" 
android:layout_width="wrap_content" 
android:layout_height="wrap_content" 
android:text="Home Page" 
android:textColor="#0C9AD9" 
android:textSize="34sp" 
android:textStyle="bold" 
app:layout_constraintBottom_toBottomOf="parent" 
app:layout_constraintEnd_toEndOf="parent" 
app:layout_constraintHorizontal_bias="0.589" 
app:layout_constraintStart_toStartOf="parent" 
app:layout_constraintTop_toTopOf="parent" 
app:layout_constraintVertical_bias="0.084" /> 
<Button 
android:id="@+id/button" 
android:layout_width="wrap_content" 
android:layout_height="wrap_content" 
android:layout_marginTop="311dp" 
android:layout_marginEnd="81dp" 
android:layout_marginBottom="310dp" 
android:text="Second Page" 
android:textSize="24sp" 
app:layout_constraintBottom_toBottomOf="parent" 
app:layout_constraintEnd_toEndOf="parent" 
app:layout_constraintTop_toTopOf="@+id/textView" /> 
<Button 
android:id="@+id/button2" 
android:layout_width="wrap_content" 
android:layout_height="wrap_content" 
android:layout_marginStart="11dp" 
android:layout_marginTop="31dp" 
android:text="Third Page" 
android:textSize="24sp" 
app:layout_constraintStart_toStartOf="@+id/button" 
app:layout_constraintTop_toBottomOf="@+id/button" /> 
</androidx.constraintlayout.widget.ConstraintLayout> 
activity_secondpage.xml 
<?xml version="1.0" encoding="utf-8"?> 
<androidx.constraintlayout.widget.ConstraintLayout 
xmlns:android="http://schemas.android.com/apk/res/android" 
xmlns:app="http://schemas.android.com/apk/res-auto" 
xmlns:tools="http://schemas.android.com/tools" 
android:id="@+id/main" 
android:layout_width="match_parent" 
android:layout_height="match_parent" 
android:background="#C4ADED" 
tools:context=".Secondpage"> 
<TextView 
android:id="@+id/textView" 
android:layout_width="wrap_content" 
android:layout_height="wrap_content" 
android:text="Second Page" 
android:textColor="#9C27B0" 
android:textSize="34sp" 
android:textStyle="bold" 
app:layout_constraintBottom_toBottomOf="parent" 
app:layout_constraintEnd_toEndOf="parent" 
app:layout_constraintHorizontal_bias="0.589" 
app:layout_constraintStart_toStartOf="parent" 
app:layout_constraintTop_toTopOf="parent" 
app:layout_constraintVertical_bias="0.084" /> 
<Button 
android:id="@+id/button" 
android:layout_width="wrap_content" 
android:layout_height="wrap_content" 
android:layout_marginTop="311dp" 
android:layout_marginEnd="81dp" 
android:layout_marginBottom="310dp" 
android:text="Home Page" 
android:textSize="24sp" 
app:layout_constraintBottom_toBottomOf="parent" 
app:layout_constraintEnd_toEndOf="parent" 
app:layout_constraintTop_toTopOf="@+id/textView" /> 
<Button 
android:id="@+id/button2" 
android:layout_width="wrap_content" 
android:layout_height="wrap_content" 
android:layout_marginStart="11dp" 
android:layout_marginTop="31dp" 
android:text="Third Page" 
android:textSize="24sp" 
app:layout_constraintStart_toStartOf="@+id/button" 
app:layout_constraintTop_toBottomOf="@+id/button" /> 
</androidx.constraintlayout.widget.ConstraintLayout> 
activity_thirdpage.xml 
<?xml version="1.0" encoding="utf-8"?> 
<androidx.constraintlayout.widget.ConstraintLayout 
xmlns:android="http://schemas.android.com/apk/res/android" 
xmlns:app="http://schemas.android.com/apk/res-auto" 
    xmlns:tools="http://schemas.android.com/tools" 
    android:id="@+id/main" 
    android:layout_width="match_parent" 
    android:layout_height="match_parent" 
    android:background="#EDBFB0" 
    tools:context=".Thirdpage"> 
 
    <TextView 
        android:id="@+id/textView" 
        android:layout_width="wrap_content" 
        android:layout_height="wrap_content" 
        android:text="Third Page" 
        android:textColor="#EF3F08" 
        android:textSize="34sp" 
        android:textStyle="bold" 
        app:layout_constraintBottom_toBottomOf="parent" 
        app:layout_constraintEnd_toEndOf="parent" 
        app:layout_constraintHorizontal_bias="0.589" 
        app:layout_constraintStart_toStartOf="parent" 
        app:layout_constraintTop_toTopOf="parent" 
        app:layout_constraintVertical_bias="0.084" /> 
 
    <Button 
        android:id="@+id/button" 
        android:layout_width="wrap_content" 
        android:layout_height="wrap_content" 
        android:layout_marginTop="311dp" 
        android:layout_marginEnd="81dp" 
        android:layout_marginBottom="310dp" 
        android:text="Home Page" 
        android:textSize="24sp" 
        app:layout_constraintBottom_toBottomOf="parent" 
        app:layout_constraintEnd_toEndOf="parent" 
        app:layout_constraintTop_toTopOf="@+id/textView" /> 
 
    <Button 
        android:id="@+id/button2" 
        android:layout_width="wrap_content" 
        android:layout_height="wrap_content" 
        android:layout_marginStart="11dp" 
        android:layout_marginTop="32dp" 
        android:text="Second Page" 
        android:textSize="24sp" 
        app:layout_constraintStart_toStartOf="@+id/button" 
        app:layout_constraintTop_toBottomOf="@+id/button" /> 
</androidx.constraintlayout.widget.ConstraintLayout> 
 
 
MainActivity.java 
package com.example.navigation123; 
import android.content.Intent; 
import android.os.Bundle; 
import android.view.View; 
import android.widget.Button; 
import androidx.activity.EdgeToEdge; 
import androidx.appcompat.app.AppCompatActivity; 
import androidx.core.graphics.Insets; 
import androidx.core.view.ViewCompat; 
import androidx.core.view.WindowInsetsCompat; 
public class MainActivity extends AppCompatActivity { 
Button b1,b2; 
@Override 
protected void onCreate(Bundle savedInstanceState) { 
super.onCreate(savedInstanceState); 
EdgeToEdge.enable(this); 
setContentView(R.layout.activity_main); 
ViewCompat.setOnApplyWindowInsetsListener(findViewById(R.id.main
 ), (v, insets) -> { 
Insets systemBars = 
insets.getInsets(WindowInsetsCompat.Type.systemBars()); 
v.setPadding(systemBars.left, systemBars.top, 
systemBars.right, systemBars.bottom); 
return insets; 
}); 
b1 = (Button) findViewById(R.id.button); 
b2 = (Button) findViewById(R.id.button2); 
b1.setOnClickListener(new View.OnClickListener() { 
@Override 
public void onClick(View view) { 
Intent i = new Intent(getBaseContext(), Secondpage.class); 
startActivity(i); 
} 
}); 
b2.setOnClickListener(new View.OnClickListener() { 
@Override 
public void onClick(View view) { 
Intent i = new Intent(getBaseContext(), Thirdpage.class); 
startActivity(i); 
} 
}); 
} 
} 
Secondpage.java 
package com.example.navigation123; 
import android.content.Intent; 
import android.os.Bundle; 
import android.view.View; 
import android.widget.Button; 
import androidx.activity.EdgeToEdge; 
import androidx.appcompat.app.AppCompatActivity; 
import androidx.core.graphics.Insets; 
import androidx.core.view.ViewCompat; 
import androidx.core.view.WindowInsetsCompat; 
public class Secondpage extends AppCompatActivity { 
Button b1,b2; 
@Override 
protected void onCreate(Bundle savedInstanceState) { 
super.onCreate(savedInstanceState); 
EdgeToEdge.enable(this); 
setContentView(R.layout.activity_secondpage); 
ViewCompat.setOnApplyWindowInsetsListener(findViewById(R.id.main
 ), (v, insets) -> { 
Insets systemBars = 
insets.getInsets(WindowInsetsCompat.Type.systemBars()); 
v.setPadding(systemBars.left, systemBars.top, 
systemBars.right, systemBars.bottom); 
return insets; 
}); 
b1 = (Button) findViewById(R.id.button); 
b2 = (Button) findViewById(R.id.button2); 
b1.setOnClickListener(new View.OnClickListener() { 
@Override 
public void onClick(View view) { 
Intent i = new Intent(getBaseContext(),MainActivity.class); 
startActivity(i); 
} 
}); 
b2.setOnClickListener(new View.OnClickListener() { 
@Override 
public void onClick(View view)Intent i = new 
Intent(getBaseContext(), Thirdpage.class); 
startActivity(i); 
} 
}); 
} 
} 
Thirdpage.java 
package com.example.navigation123; 
import android.content.Intent; 
import android.os.Bundle; 
import android.view.View; 
import android.widget.Button; 
import androidx.activity.EdgeToEdge; 
import androidx.appcompat.app.AppCompatActivity; 
import androidx.core.graphics.Insets; 
import androidx.core.view.ViewCompat; 
import androidx.core.view.WindowInsetsCompat; 
public class Thirdpage extends AppCompatActivity { 
Button b1,b2; 
@Override 
protected void onCreate(Bundle savedInstanceState) { 
super.onCreate(savedInstanceState); 
EdgeToEdge.enable(this); 
setContentView(R.layout.activity_thirdpage); 
ViewCompat.setOnApplyWindowInsetsListener(findViewById(R.id.main
 ), (v, insets) -> { 
Insets systemBars = 
insets.getInsets(WindowInsetsCompat.Type.systemBars()); 
v.setPadding(systemBars.left, systemBars.top, 
systemBars.right, systemBars.bottom); 
return insets; 
}); 
b1 = (Button) findViewById(R.id.button); 
b2 = (Button) findViewById(R.id.button2); 
b1.setOnClickListener(new View.OnClickListener() { 
@Override 
public void onClick(View view) { 
Intent i = new Intent(getBaseContext(), MainActivity.class); 
startActivity(i); 
}); 
} 
b2.setOnClickListener(new View.OnClickListener() { 
@Override 
public void onClick(View view) { 
Intent i = new Intent(getBaseContext(), Secondpage.class); 
startActivity(i); 
} 
}); 
} 
} 
AndroidManifest.xml 
<activity 
android:name=".Thirdpage" 
android:exported="false" /> 
<activity 
android:name=".Secondpage" 
android:exported="false" /> 
OUTPUT 
EXPERIMENT NO.: 13 
Aim: To develop a simple Android application to demonstrate the use of Layoutmanager – 
Design your ID Card. 
1. Open android studio and select new android project by clicking Filemenu  New New 
Project. 
2. Choose the project as Empty Views Activity and click Next. 
3. Give project name (Start with a capital letter) as IDCard  
4. Choose the language as Java. 
5. Choose the required android version (Minimum SDK) and select finish. 
6. Go to package explorer in the left hand side and select the project. 
7. Under the project, Go to res folder and select layout. 
8. Double click the activity_main.xml file and design the layout for the page. 
9. Select MainActivity.java file and type the program. 
10.  Now go to activity_main.xml and right click & select run as option and select run 
configuration OR select the virtual device and click on run icon. 
11.  Android output will be displayed on the android emulator. 
Both activity_main.xml and MainActivity.java files together make our application work. The 
activity_main.xml is responsible for the layout (Front end User Interface) of the application. And 
the file MainActivity is responsible for the actions and the performance of the application (back 
end). 
Code: 
activity_main.xml 
<?xml version="1.0" encoding="utf-8"?> 
<androidx.constraintlayout.widget.ConstraintLayout 
xmlns:android="http://schemas.android.com/apk/res/android" 
xmlns:app="http://schemas.android.com/apk/res-auto" 
xmlns:tools="http://schemas.android.com/tools" 
android:id="@+id/main" 
android:layout_width="match_parent" 
android:layout_height="match_parent" 
tools:context=".MainActivity"> 
<TextView 
android:id="@+id/textView3" 
android:layout_width="414dp" 
android:layout_height="157dp" 
android:background="#1C3C9B" 
android:text="MVSR" 
android:textAlignment="center" 
        android:textColor="#FFEBEE" 
        android:textSize="34sp" 
        android:textStyle="bold" 
        app:layout_constraintEnd_toEndOf="parent" 
        app:layout_constraintStart_toStartOf="parent" 
        tools:layout_editor_absoluteY="-3dp" /> 
 
    <TextView 
        android:id="@+id/textView4" 
        android:layout_width="wrap_content" 
        android:layout_height="wrap_content" 
        android:text="ENGINEERING COLLEGE" 
        android:textColor="#FFEBEE" 
        android:textSize="28sp" 
        android:textStyle="bold" 
        tools:layout_editor_absoluteX="61dp" 
        tools:layout_editor_absoluteY="45dp" /> 
 
    <TextView 
        android:id="@+id/textView5" 
        android:layout_width="166dp" 
        android:layout_height="21dp" 
        android:background="#FFEBEE" 
        android:text="UGC AUTONOMOUS" 
        android:textAlignment="center" 
        android:textColor="#ED0A0A" 
        android:textSize="16sp" 
        android:textStyle="bold" 
        tools:layout_editor_absoluteX="128dp" 
        tools:layout_editor_absoluteY="83dp" /> 
 
    <TextView 
        android:id="@+id/textView7" 
        android:layout_width="wrap_content" 
        android:layout_height="wrap_content" 
        android:text="(Sponsored by Matrusri Education 
Society,Estd.1980)" 
        android:textColor="#FFEBEE" 
        android:textSize="14sp" 
        android:textStyle="normal" 
        tools:layout_editor_absoluteX="26dp" 
        tools:layout_editor_absoluteY="107dp" /> 
 
    <TextView 
        android:id="@+id/textView8" 
        android:layout_width="wrap_content" 
        android:layout_height="wrap_content" 
        android:text="Affiliated to Osmania University" 
        android:textAlignment="center" 
        android:textColor="#FFEBEE" 
        tools:layout_editor_absoluteX="98dp" 
        tools:layout_editor_absoluteY="126dp" /> 
 
    <TextView 
        android:id="@+id/textView9" 
        android:layout_width="418dp" 
        android:layout_height="99dp" 
        android:background="#1C3C9B" 
        android:text="NADERGUL VILLAGE,BALAPUR 
MANDAL(NEW),SAROORNAGAR" 
        android:textAlignment="center" 
        android:textColor="#FFEBEE" 
        tools:layout_editor_absoluteX="-4dp" 
        tools:layout_editor_absoluteY="635dp" /> 
 
    <TextView 
        android:id="@+id/textView10" 
        android:layout_width="wrap_content" 
        android:layout_height="wrap_content" 
        android:text="MANDAL(OLD)HYDERABAD-501510 TELANGANA" 
        android:textColor="#FFEBEE" 
        tools:layout_editor_absoluteX="57dp" 
        tools:layout_editor_absoluteY="658dp" /> 
 
    <TextView 
        android:id="@+id/textView11" 
        android:layout_width="wrap_content" 
        android:layout_height="wrap_content" 
        android:text="WEBSITE:mvsrec.edu.in" 
        android:textColor="#FFEBEE" 
        tools:layout_editor_absoluteX="131dp" 
        tools:layout_editor_absoluteY="684dp" /> 
 
    <Button 
        android:id="@+id/button" 
        android:layout_width="wrap_content" 
        android:layout_height="wrap_content" 
        android:text="IDENTITY CARD" 
        tools:layout_editor_absoluteX="130dp" 
        tools:layout_editor_absoluteY="182dp" /> 
 
    <ImageView 
        android:id="@+id/imageView" 
        android:layout_width="175dp" 
        android:layout_height="183dp" 
        app:srcCompat="@drawable/mvsr" 
        tools:layout_editor_absoluteX="118dp" 
        tools:layout_editor_absoluteY="238dp" /> 
<TextView 
android:id="@+id/textView12" 
android:layout_width="193dp" 
android:layout_height="27dp" 
android:text="Student Name" 
android:textAlignment="center" 
android:textColor="#D32525" 
android:textSize="24sp" 
android:textStyle="bold" 
tools:layout_editor_absoluteX="109dp" 
tools:layout_editor_absoluteY="431dp" /> 
<TextView 
android:id="@+id/textView13" 
android:layout_width="wrap_content" 
android:layout_height="wrap_content" 
android:text="Roll No : 2451-22-737-XXX" 
android:textColor="#101010" 
android:textSize="20sp" 
android:textStyle="bold" 
tools:layout_editor_absoluteX="35dp" 
tools:layout_editor_absoluteY="492dp" /> 
<TextView 
android:id="@+id/textView14" 
android:layout_width="wrap_content" 
android:layout_height="wrap_content" 
android:text="Branch : IT" 
android:textColor="#0F0E0E" 
android:textSize="20sp" 
android:textStyle="bold" 
tools:layout_editor_absoluteX="35dp" 
tools:layout_editor_absoluteY="538dp" /> 
</androidx.constraintlayout.widget.ConstraintLayout> 
MainActivity.java 
package com.example.idcard; 
import android.os.Bundle; 
import androidx.activity.EdgeToEdge; 
import androidx.appcompat.app.AppCompatActivity; 
import androidx.core.graphics.Insets; 
import androidx.core.view.ViewCompat; 
import androidx.core.view.WindowInsetsCompat; 
public class MainActivity extends AppCompatActivity { 
@Override 
protected void onCreate(Bundle savedInstanceState) { 
super.onCreate(savedInstanceState); 
EdgeToEdge.enable(this); 
setContentView(R.layout.activity_main); 
ViewCompat.setOnApplyWindowInsetsListener(findViewById(R.id.main
 ), (v, insets) -> { 
Insets systemBars = 
insets.getInsets(WindowInsetsCompat.Type.systemBars()); 
v.setPadding(systemBars.left, systemBars.top, 
systemBars.right, systemBars.bottom); 
return insets; 
}); 
} 
} 
OUTPUT ON EMULATOR: 
EXPERIMENT NO.: 14 
Aim: To develop a simple Android application that draws basic graphical primitives on the 
screen 
1. Open android studio and select new android project by clicking Filemenu  New New 
Project. 
2. Choose the project as Empty Views Activity and click Next. 
3. Give project name (Start with a capital letter) as DrawGraphics  
4. Choose the language as Java. 
5. Choose the required android version (Minimum SDK) and select finish. 
6. Go to package explorer in the left hand side and select the project. 
7. Under the project, Go to res folder and select layout. 
8. Double click the activity_main.xml file and design the layout for the page. 
9. Select MainActivity.java file and type the program. 
10.  Now go to activity_main.xml and right click & select run as option and select run 
configuration OR select the virtual device and click on run icon. 
11.  Android output will be displayed on the android emulator. 
Both activity_main.xml and MainActivity.java files together make our application work. The 
activity_main.xml is responsible for the layout (Front end User Interface) of the application. And 
the file MainActivity is responsible for the actions and the performance of the application (back 
end). 
Code: 
activity_main.xml 
<?xml version="1.0" encoding="utf-8"?> 
<androidx.constraintlayout.widget.ConstraintLayout 
xmlns:android="http://schemas.android.com/apk/res/android" 
xmlns:app="http://schemas.android.com/apk/res-auto" 
xmlns:tools="http://schemas.android.com/tools" 
android:id="@+id/main" 
android:layout_width="match_parent" 
android:layout_height="match_parent" 
tools:context=".MainActivity"> 
<ImageView 
android:id="@+id/imageView" 
android:layout_width="match_parent" 
android:layout_height="match_parent" 
app:layout_constraintBottom_toBottomOf="parent" 
app:layout_constraintStart_toStartOf="parent" /> 
</androidx.constraintlayout.widget.ConstraintLayout> 
MainActivity.java 
package com.example.graphics; 
import android.graphics.Bitmap; 
import android.graphics.Canvas; 
import android.graphics.Color; 
import android.graphics.Paint; 
import android.graphics.drawable.BitmapDrawable; 
import android.os.Bundle; 
import android.widget.ImageView; 
import androidx.activity.EdgeToEdge; 
import androidx.appcompat.app.AppCompatActivity; 
import androidx.core.graphics.Insets; 
import androidx.core.view.ViewCompat; 
import androidx.core.view.WindowInsetsCompat; 
public class MainActivity extends AppCompatActivity { 
@Override 
protected void onCreate(Bundle savedInstanceState) { 
super.onCreate(savedInstanceState); 
EdgeToEdge.enable(this); 
setContentView(R.layout.activity_main); 
ViewCompat.setOnApplyWindowInsetsListener(findViewById(R.id.main
 ), (v, insets) -> { 
Insets systemBars = 
insets.getInsets(WindowInsetsCompat.Type.systemBars()); 
v.setPadding(systemBars.left, systemBars.top, 
systemBars.right, systemBars.bottom); 
return insets; 
}); 
Bitmap bg = Bitmap.createBitmap(720, 1280, 
Bitmap.Config.ARGB_8888); 
//Setting the Bitmap as background for the ImageView 
ImageView i = (ImageView) findViewById(R.id.imageView); 
i.setBackgroundDrawable(new BitmapDrawable(bg)); 
//Creating the Canvas Object 
Canvas canvas = new Canvas(bg); 
//Creating the Paint Object and set its color & TextSize 
Paint paint = new Paint(); 
paint.setColor(Color.BLUE); 
paint.setTextSize(50); 
//To draw a Rectangle 
canvas.drawText("Rectangle", 420, 150, paint); 
paint.setColor(Color.RED); 
canvas.drawRect(400, 200, 650, 700, paint); 
//To draw a Circle 
canvas.drawText("Circle", 120, 150, paint); 
paint.setColor(Color.YELLOW); 
canvas.drawCircle(200, 350, 150, paint); 
paint.setColor(Color.BLACK); 
canvas.drawCircle(150, 320, 20, paint); 
paint.setColor(Color.BLACK); 
canvas.drawCircle(250, 320, 20, paint); 
paint.setColor(Color.RED); 
canvas.drawArc(120, 375, 275,460,0,180,false, paint); 
//To draw a Square 
canvas.drawText("Square", 120, 800, paint); 
paint.setColor(Color.YELLOW); 
canvas.drawRect(50, 850, 350, 1150, paint); 
//To draw a Line 
canvas.drawText("Line", 480, 800, paint); 
paint.setColor(Color.CYAN); 
canvas.drawLine(520, 850, 520, 1150, paint); 
} 
} 
OUTPUT ON EMULATOR: 
EXPERIMENT NO.: 15 
Aim: To develop a simple Android application to send an Email. 
1. Open android studio and select new android project by clicking Filemenu  New New 
Project. 
2. Choose the project as Empty Views Activity and click Next. 
3. Give project name (Start with a capital letter) as SendEmail  
4. Choose the language as Java. 
5. Choose the required android version (Minimum SDK) and select finish. 
6. Go to package explorer in the left hand side and select the project. 
7. Under the project, Go to res folder and select layout. 
8. Double click the activity_main.xml file and design the layout for the page. 
9. Select MainActivity.java file and type the program. 
10.  Now go to activity_main.xml and right click & select run as option and select run 
configuration OR select the virtual device and click on run icon. 
11.  Android output will be displayed on the android emulator. 
Both activity_main.xml and MainActivity.java files together make our application work. The 
activity_main.xml is responsible for the layout (Front end User Interface) of the application. And 
the file MainActivity is responsible for the actions and the performance of the application (back 
end). 
Code: 
activity_main.xml 
activity_main.xml 
<?xml version="1.0" encoding="utf-8"?> 
<androidx.constraintlayout.widget.ConstraintLayout 
xmlns:android="http://schemas.android.com/apk/res/android" 
xmlns:app="http://schemas.android.com/apk/res-auto" 
xmlns:tools="http://schemas.android.com/tools" 
android:id="@+id/main" 
android:layout_width="match_parent" 
android:layout_height="match_parent" 
tools:context=".MainActivity"> 
<TextView 
android:id="@+id/textView" 
android:layout_width="wrap_content" 
android:layout_height="wrap_content" 
android:layout_marginTop="69dp" 
android:layout_marginBottom="53dp" 
        android:fontFamily="cursive" 
        android:text="Send Email" 
        android:textColor="#E91E63" 
        android:textSize="48sp" 
        android:textStyle="bold" 
        app:layout_constraintBottom_toTopOf="@+id/email" 
        app:layout_constraintEnd_toEndOf="parent" 
        app:layout_constraintStart_toStartOf="parent" 
        app:layout_constraintTop_toTopOf="parent" /> 
 
    <TextView 
        android:id="@+id/textView2" 
        android:layout_width="wrap_content" 
        android:layout_height="wrap_content" 
        android:layout_marginStart="46dp" 
        android:layout_marginEnd="86dp" 
        android:text="To" 
        android:textSize="24sp" 
        android:textStyle="bold" 
        app:layout_constraintBaseline_toBaselineOf="@+id/email" 
        app:layout_constraintEnd_toStartOf="@+id/email" 
        app:layout_constraintStart_toStartOf="parent" /> 
 
    <TextView 
        android:id="@+id/textView3" 
        android:layout_width="wrap_content" 
        android:layout_height="wrap_content" 
        android:layout_marginStart="46dp" 
        android:layout_marginTop="13dp" 
        android:layout_marginEnd="37dp" 
        android:text="Subject" 
        android:textSize="24sp" 
        android:textStyle="bold" 
        app:layout_constraintEnd_toStartOf="@+id/sub" 
        app:layout_constraintStart_toStartOf="parent" 
        app:layout_constraintTop_toTopOf="@+id/sub" /> 
 
    <EditText 
        android:id="@+id/sub" 
        android:layout_width="0dp" 
        android:layout_height="0dp" 
        android:layout_marginEnd="35dp" 
        android:layout_marginBottom="44dp" 
        android:ems="10" 
        android:inputType="text" 
        android:textSize="24sp" 
        app:layout_constraintBottom_toTopOf="@+id/body" 
        app:layout_constraintEnd_toEndOf="parent" 
        app:layout_constraintStart_toEndOf="@+id/textView3" 
        app:layout_constraintTop_toBottomOf="@+id/email" /> 
 
    <TextView 
        android:id="@+id/textView4" 
        android:layout_width="wrap_content" 
        android:layout_height="wrap_content" 
        android:layout_marginStart="46dp" 
        android:layout_marginTop="13dp" 
        android:layout_marginEnd="59dp" 
        android:text="Body" 
        android:textSize="24sp" 
        android:textStyle="bold" 
        app:layout_constraintEnd_toStartOf="@+id/body" 
        app:layout_constraintStart_toStartOf="parent" 
        app:layout_constraintTop_toTopOf="@+id/body" /> 
 
    <EditText 
        android:id="@+id/body" 
        android:layout_width="0dp" 
        android:layout_height="0dp" 
        android:layout_marginEnd="25dp" 
        android:layout_marginBottom="45dp" 
        android:ems="10" 
        android:inputType="text" 
        android:textSize="24sp" 
        app:layout_constraintBottom_toTopOf="@+id/button" 
        app:layout_constraintEnd_toEndOf="parent" 
        app:layout_constraintStart_toEndOf="@+id/textView4" 
        app:layout_constraintTop_toBottomOf="@+id/sub" /> 
 
    <Button 
        android:id="@+id/button" 
        android:layout_width="wrap_content" 
        android:layout_height="wrap_content" 
        android:layout_marginEnd="112dp" 
        android:layout_marginBottom="144dp" 
        android:text="Send Email" 
        android:textSize="24sp" 
        app:layout_constraintBottom_toBottomOf="parent" 
        app:layout_constraintEnd_toEndOf="@+id/body" 
        app:layout_constraintTop_toBottomOf="@+id/body" /> 
 
    <EditText 
        android:id="@+id/email" 
        android:layout_width="0dp" 
        android:layout_height="0dp" 
        android:layout_marginEnd="21dp" 
        android:layout_marginBottom="31dp" 
        android:ems="10" 
android:inputType="textEmailAddress" 
android:textSize="24sp" 
app:layout_constraintBottom_toTopOf="@+id/sub" 
app:layout_constraintEnd_toEndOf="parent" 
app:layout_constraintStart_toEndOf="@+id/textView2" 
app:layout_constraintTop_toBottomOf="@+id/textView" /> 
</androidx.constraintlayout.widget.ConstraintLayout> 
MainActivity.java 
package com.example.sendemail; 
import android.content.Intent; 
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
Button send; 
EditText to, subject, body; 
@Override 
protected void onCreate(Bundle savedInstanceState) { 
super.onCreate(savedInstanceState); 
EdgeToEdge.enable(this); 
setContentView(R.layout.activity_main); 
ViewCompat.setOnApplyWindowInsetsListener(findViewById(R.id.main
 ), (v, insets) -> { 
Insets systemBars = 
insets.getInsets(WindowInsetsCompat.Type.systemBars()); 
v.setPadding(systemBars.left, systemBars.top, 
systemBars.right, systemBars.bottom); 
return insets; 
}); 
to = findViewById(R.id.email); 
subject = findViewById(R.id.sub); 
body = findViewById(R.id.body); 
send = findViewById(R.id.button); 
send.setOnClickListener(new View.OnClickListener() { 
@Override 
public void onClick(View view) { 
String emailsend = to.getText().toString(); 
String emailsubject = subject.getText().toString(); 
String emailbody = body.getText().toString(); 
Intent i = new Intent(Intent.ACTION_SEND); 
i.putExtra(Intent.EXTRA_EMAIL, new String[]{emailsend}); 
i.putExtra(Intent.EXTRA_SUBJECT, emailsubject); 
i.putExtra(Intent.EXTRA_TEXT, emailbody); 
i.setType("message/rfc822"); 
startActivity(Intent.createChooser(i, "Choose an 
Email client :")); 
} 
}); 
} 
} 
OUTPUT ON EMULATOR: 
EXPERIMENT NO.: 16 
Aim: To develop a simple Android application to send a SMS. 
1. Open android studio and select new android project by clicking Filemenu  New New 
Project. 
2. Choose the project as Empty Views Activity and click Next. 
3. Give project name (Start with a capital letter) as SendSMS  
4. Choose the language as Java. 
5. Choose the required android version (Minimum SDK) and select finish. 
6. Go to package explorer in the left hand side and select the project. 
7. Under the project, Go to res folder and select layout. 
8. Double click the activity_main.xml file and design the layout for the page. 
9. Select MainActivity.java file and type the program. 
10.  Now go to activity_main.xml and right click & select run as option and select run 
configuration OR select the virtual device and click on run icon. 
11.  Android output will be displayed on the android emulator. 
Both activity_main.xml and MainActivity.java files together make our application work. The 
activity_main.xml is responsible for the layout (Front end User Interface) of the application. And 
the file MainActivity is responsible for the actions and the performance of the application (back 
end). 
Code: 
activity_main.xml 
<?xml version="1.0" encoding="utf-8"?> 
<androidx.constraintlayout.widget.ConstraintLayout 
xmlns:android="http://schemas.android.com/apk/res/android" 
xmlns:app="http://schemas.android.com/apk/res-auto" 
xmlns:tools="http://schemas.android.com/tools" 
android:id="@+id/main" 
android:layout_width="match_parent" 
android:layout_height="match_parent" 
tools:context=".MainActivity"> 
<TextView 
android:id="@+id/textView" 
android:layout_width="wrap_content" 
android:layout_height="wrap_content" 
android:layout_marginTop="69dp" 
android:fontFamily="cursive" 
android:text="Send SMS" 
android:textColor="#E91E63" 
android:textSize="48sp" 
android:textStyle="bold" 
        app:layout_constraintEnd_toEndOf="parent" 
        app:layout_constraintStart_toStartOf="parent" 
        app:layout_constraintTop_toTopOf="parent" /> 
 
    <Button 
        android:id="@+id/button" 
        android:layout_width="wrap_content" 
        android:layout_height="wrap_content" 
        android:layout_marginBottom="188dp" 
        android:text="Send SMS" 
        android:textSize="24sp" 
        app:layout_constraintBottom_toBottomOf="parent" 
        app:layout_constraintEnd_toEndOf="parent" 
        app:layout_constraintStart_toStartOf="parent" /> 
 
    <TextView 
        android:id="@+id/textView2" 
        android:layout_width="wrap_content" 
        android:layout_height="wrap_content" 
        android:layout_marginStart="31dp" 
        android:layout_marginEnd="15dp" 
        android:text="Mobile No:" 
        android:textSize="24sp" 
        android:textStyle="bold" 
        app:layout_constraintBaseline_toBaselineOf="@+id/pno" 
        app:layout_constraintEnd_toStartOf="@+id/pno" 
        app:layout_constraintStart_toStartOf="parent" /> 
 
    <TextView 
        android:id="@+id/textView3" 
        android:layout_width="wrap_content" 
        android:layout_height="wrap_content" 
        android:layout_marginStart="35dp" 
        android:layout_marginTop="3dp" 
        android:layout_marginEnd="37dp" 
        android:text="Message" 
        android:textSize="24sp" 
        android:textStyle="bold" 
        app:layout_constraintEnd_toStartOf="@+id/msg" 
        app:layout_constraintStart_toStartOf="parent" 
        app:layout_constraintTop_toTopOf="@+id/msg" /> 
 
    <EditText 
        android:id="@+id/pno" 
        android:layout_width="0dp" 
        android:layout_height="0dp" 
        android:layout_marginTop="247dp" 
        android:layout_marginEnd="28dp" 
        android:layout_marginBottom="51dp" 
android:ems="10" 
android:inputType="phone" 
android:textSize="24sp" 
app:layout_constraintBottom_toTopOf="@+id/msg" 
app:layout_constraintEnd_toEndOf="parent" 
app:layout_constraintStart_toEndOf="@+id/textView2" 
app:layout_constraintTop_toTopOf="parent" /> 
<EditText 
android:id="@+id/msg" 
android:layout_width="0dp" 
android:layout_height="0dp" 
android:layout_marginEnd="42dp" 
android:layout_marginBottom="292dp" 
android:ems="10" 
android:inputType="text" 
android:textSize="24sp" 
app:layout_constraintBottom_toBottomOf="parent" 
app:layout_constraintEnd_toEndOf="parent" 
app:layout_constraintStart_toEndOf="@+id/textView3" 
app:layout_constraintTop_toBottomOf="@+id/pno" /> 
</androidx.constraintlayout.widget.ConstraintLayout> 
AndroidManifest.xml 
<uses-permission 
android:name="android.permission.SEND_SMS"></uses-permission> 
MainActivity.java 
package com.example.sendsms; 
import android.Manifest; 
import android.content.pm.PackageManager; 
import android.os.Build; 
import android.os.Bundle; 
import android.telephony.SmsManager; 
import android.view.View; 
import android.widget.Button; 
import android.widget.EditText; 
import android.widget.Toast; 
import androidx.activity.EdgeToEdge; 
import androidx.appcompat.app.AppCompatActivity; 
import androidx.core.app.ActivityCompat; 
import androidx.core.content.ContextCompat; 
import androidx.core.graphics.Insets; 
import androidx.core.view.ViewCompat; 
import androidx.core.view.WindowInsetsCompat; 
public class MainActivity extends AppCompatActivity { 
EditText phone,msg; 
Button sms; 
@Override 
protected void onCreate(Bundle savedInstanceState) { 
super.onCreate(savedInstanceState); 
EdgeToEdge.enable(this); 
setContentView(R.layout.activity_main); 
ViewCompat.setOnApplyWindowInsetsListener(findViewById(R.id.main
 ), (v, insets) -> { 
Insets systemBars = 
insets.getInsets(WindowInsetsCompat.Type.systemBars()); 
v.setPadding(systemBars.left, systemBars.top, 
systemBars.right, systemBars.bottom); 
return insets; 
}); 
if (Build.VERSION.SDK_INT >= 
Build.VERSION_CODES.TIRAMISU) { 
if (ContextCompat.checkSelfPermission(this, 
android.Manifest.permission.POST_NOTIFICATIONS) != 
PackageManager.PERMISSION_GRANTED) { 
ActivityCompat.requestPermissions(this, new 
String[]{Manifest.permission.SEND_SMS}, 100); 
} 
} 
phone = (EditText)findViewById(R.id.pno); 
msg = (EditText)findViewById(R.id.msg); 
sms = (Button)findViewById(R.id.button); 
sms.setOnClickListener(new View.OnClickListener() { 
@Override 
public void onClick(View v) { 
try{ 
SmsManager smgr = SmsManager.getDefault(); 
smgr.sendTextMessage(phone.getText().toString(),null,msg.getText
 ().toString(),null,null); 
Toast.makeText(MainActivity.this, "SMS Sent Successfully", 
Toast.LENGTH_SHORT).show(); 
} 
catch (Exception e){ 
Toast.makeText(MainActivity.this, "SMS Failed to Send, Please 
try again", Toast.LENGTH_SHORT).show(); 
} 
} 
}); 
} 
} 
OUTPUT ON EMULATOR: 
EXPERIMENT NO.: 17 
Aim: To develop a simple Android application that sends a Notification. 
1. Open android studio and select new android project by clicking Filemenu  New New 
Project. 
2. Choose the project as Empty Views Activity and click Next. 
3. Give project name (Start with a capital letter) as SendNotification  
4. Choose the language as Java. 
5. Choose the required android version (Minimum SDK) and select finish. 
6. Go to package explorer in the left hand side and select the project. 
7. Under the project, Go to res folder and select layout. 
8. Double click the activity_main.xml file and design the layout for the page. 
9. Select MainActivity.java file and type the program. 
10.  Now go to activity_main.xml and right click & select run as option and select run 
configuration OR select the virtual device and click on run icon. 
11.  Android output will be displayed on the android emulator. 
Both activity_main.xml and MainActivity.java files together make our application work. The 
activity_main.xml is responsible for the layout (Front end User Interface) of the application. And 
the file MainActivity is responsible for the actions and the performance of the application (back 
end). 
Code: 
Android Manifest file 
<uses-permission 
android:name="android.permission.POST_NOTIFICATIONS"> 
</uses-permission> 
Activity_main.xml 
<?xml version="1.0" encoding="utf-8"?> 
<androidx.constraintlayout.widget.ConstraintLayout 
xmlns:android="http://schemas.android.com/apk/res/android" 
xmlns:app="http://schemas.android.com/apk/res-auto" 
xmlns:tools="http://schemas.android.com/tools" 
android:id="@+id/main" 
android:layout_width="match_parent" 
android:layout_height="match_parent" 
tools:context=".MainActivity"> 
<TextView 
android:id="@+id/textView" 
android:layout_width="wrap_content" 
android:layout_height="wrap_content" 
android:fontFamily="cursive" 
android:text="Notification" 
android:textColor="#E91E63" 
android:textSize="48sp" 
android:textStyle="bold" 
tools:layout_editor_absoluteX="105dp" 
tools:layout_editor_absoluteY="88dp" /> 
<EditText 
android:id="@+id/msg" 
android:layout_width="297dp" 
android:layout_height="98dp" 
android:layout_marginTop="211dp" 
android:hint="message" 
android:textSize="34sp" 
app:layout_constraintEnd_toEndOf="parent" 
app:layout_constraintStart_toStartOf="parent" 
app:layout_constraintTop_toTopOf="parent" /> 
<Button 
android:id="@+id/send" 
android:layout_width="wrap_content" 
android:layout_height="wrap_content" 
android:layout_marginTop="112dp" 
android:text="Send Notification" 
android:textSize="24sp" 
app:layout_constraintEnd_toEndOf="parent" 
app:layout_constraintStart_toStartOf="parent" 
app:layout_constraintTop_toBottomOf="@+id/msg" /> 
</androidx.constraintlayout.widget.ConstraintLayout> 
MainActivity.java 
package com.example.sendnotification; 
import android.Manifest; 
import android.app.NotificationChannel; 
import android.app.NotificationManager; 
import android.app.PendingIntent; 
import android.content.Context; 
import android.content.Intent; 
import android.content.pm.PackageManager; 
import android.os.Build; 
import android.os.Bundle; 
import android.view.View; 
import android.widget.Button; 
import android.widget.EditText; 
import androidx.activity.EdgeToEdge; 
import androidx.appcompat.app.AppCompatActivity; 
import androidx.core.app.ActivityCompat; 
import androidx.core.app.NotificationCompat; 
import androidx.core.content.ContextCompat; 
import androidx.core.graphics.Insets; 
import androidx.core.view.ViewCompat; 
import androidx.core.view.WindowInsetsCompat; 
public class MainActivity extends AppCompatActivity { 
EditText msg; 
Button send; 
@Override 
protected void onCreate(Bundle savedInstanceState) { 
super.onCreate(savedInstanceState); 
EdgeToEdge.enable(this); 
setContentView(R.layout.activity_main); 
ViewCompat.setOnApplyWindowInsetsListener(findViewById(R.id.main
 ), (v, insets) -> { 
Insets systemBars = 
insets.getInsets(WindowInsetsCompat.Type.systemBars()); 
v.setPadding(systemBars.left, systemBars.top, 
systemBars.right, systemBars.bottom); 
return insets; 
}); 
if (Build.VERSION.SDK_INT >= 
Build.VERSION_CODES.TIRAMISU) { 
if (ContextCompat.checkSelfPermission(this, 
android.Manifest.permission.POST_NOTIFICATIONS) != 
PackageManager.PERMISSION_GRANTED) { 
ActivityCompat.requestPermissions(this, new 
String[]{Manifest.permission.POST_NOTIFICATIONS}, 100); 
} 
} 
msg = findViewById(R.id.msg); 
send = findViewById(R.id.send); 
send.setOnClickListener(new View.OnClickListener() { 
@Override 
public void onClick(View v) { 
String message = msg.getText().toString(); 
int notificationId = (int) 
System.currentTimeMillis(); 
Intent notificationIntent = new 
Intent(MainActivity.this, MainActivity.class); 
PendingIntent pendingIntent = 
PendingIntent.getActivity(MainActivity.this, 0, 
notificationIntent, PendingIntent.FLAG_UPDATE_CURRENT | 
PendingIntent.FLAG_IMMUTABLE); 
NotificationCompat.Builder builder = new 
NotificationCompat.Builder(MainActivity.this, 
"notificationChannel") 
.setSmallIcon(android.R.drawable.ic_dialog_info) 
.setContentTitle("Simple Notification") 
.setContentText(message) 
.setAutoCancel(true) 
.setContentIntent(pendingIntent); 
NotificationManager notificationManager = (NotificationManager) 
MainActivity.this.getSystemService(Context.NOTIFICATION_SERVICE)
 ; 
if (notificationManager != null) { 
notificationManager.notify(notificationId, 
builder.build()); // Unique notification ID 
} 
// Create the notification channel (required for Android 8.0 and 
above) 
if (Build.VERSION.SDK_INT >= Build.VERSION_CODES.O) { 
NotificationChannel channel = new 
NotificationChannel("notificationChannel", "Notification", 
NotificationManager.IMPORTANCE_HIGH); 
notificationManager.createNotificationChannel(channel); 
} 
} 
}); 
} 
} 
OUTPUT ON EMULATOR: 
EXPERIMENT NO.: 18 
1. Aim: To develop a simple Android application that converts Text to Speech. 
1. Open android studio and select new android project by clicking Filemenu  New New 
Project. 
2. Choose the project as Empty Views Activity and click Next. 
3. Give project name (Start with a capital letter) as TexttoSpeech 
4. Choose the language as Java. 
5. Choose the required android version (Minimum SDK) and select finish. 
6. Go to package explorer in the left hand side and select the project. 
7. Under the project, Go to res folder and select layout. 
8. Double click the activity_main.xml file and design the layout for the page. 
9. Select MainActivity.java file and type the program. 
10.  Now go to activity_main.xml and right click & select run as option and select run 
configuration OR select the virtual device and click on run icon. 
11.  Android output will be displayed on the android emulator. 
Both activity_main.xml and MainActivity.java files together make our application work. The 
activity_main.xml is responsible for the layout (Front end User Interface) of the application. And 
the file MainActivity is responsible for the actions and the performance of the application (back 
end). 
Code: 
activity_main.xml 
<?xml version="1.0" encoding="utf-8"?> 
<androidx.constraintlayout.widget.ConstraintLayout 
xmlns:android="http://schemas.android.com/apk/res/android" 
    xmlns:app="http://schemas.android.com/apk/res-auto" 
    xmlns:tools="http://schemas.android.com/tools" 
    android:id="@+id/main" 
    android:layout_width="match_parent" 
    android:layout_height="match_parent" 
    tools:context=".MainActivity"> 
 
    <TextView 
        android:id="@+id/textView" 
        android:layout_width="274dp" 
        android:layout_height="132dp" 
        android:layout_marginTop="120dp" 
        android:layout_marginBottom="50dp" 
        android:fontFamily="cursive" 
        android:text="Text to Speech Converter" 
        android:textAlignment="center" 
        android:textColor="#E91E63" 
        android:textSize="40sp" 
        android:textStyle="bold" 
        app:layout_constraintBottom_toTopOf="@+id/editText" 
        app:layout_constraintEnd_toEndOf="parent" 
        app:layout_constraintHorizontal_bias="0.401" 
        app:layout_constraintStart_toStartOf="parent" 
        app:layout_constraintTop_toTopOf="parent" 
        app:layout_constraintVertical_bias="0.28" /> 
 
    <Button 
        android:id="@+id/button" 
        android:layout_width="212dp" 
        android:layout_height="99dp" 
        android:layout_marginTop="144dp" 
        android:text="TexttoSpeech" 
        android:textSize="24sp" 
        app:layout_constraintEnd_toEndOf="parent" 
        app:layout_constraintHorizontal_bias="0.498" 
        app:layout_constraintStart_toStartOf="parent" 
        app:layout_constraintTop_toBottomOf="@+id/textView" /> 
 
    <EditText 
        android:id="@+id/editText" 
        android:layout_width="wrap_content" 
        android:layout_height="wrap_content" 
        android:layout_marginEnd="76dp" 
        android:layout_marginBottom="393dp" 
        android:ems="10" 
        android:hint="Enter Text" 
        android:inputType="text" 
        android:textSize="24sp" 
        app:layout_constraintBottom_toBottomOf="parent" 
app:layout_constraintEnd_toEndOf="parent" 
app:layout_constraintTop_toBottomOf="@+id/textView" /> 
</androidx.constraintlayout.widget.ConstraintLayout> 
MainActivity.java 
package com.example.texttospeech; 
import android.os.Bundle; 
import android.speech.tts.TextToSpeech; 
import android.view.View; 
import android.widget.Button; 
import android.widget.EditText; 
import android.widget.Toast; 
import androidx.activity.EdgeToEdge; 
import androidx.appcompat.app.AppCompatActivity; 
import androidx.core.graphics.Insets; 
import androidx.core.view.ViewCompat; 
import androidx.core.view.WindowInsetsCompat; 
import java.util.Locale; 
public class MainActivity extends AppCompatActivity { 
TextToSpeech t1; 
EditText e1; 
Button b; 
@Override 
protected void onCreate(Bundle savedInstanceState) { 
super.onCreate(savedInstanceState); 
EdgeToEdge.enable(this); 
setContentView(R.layout.activity_main); 
ViewCompat.setOnApplyWindowInsetsListener(findViewById(R.id.main
 ), (v, insets) -> { 
Insets systemBars = 
insets.getInsets(WindowInsetsCompat.Type.systemBars()); 
v.setPadding(systemBars.left, systemBars.top, 
systemBars.right, systemBars.bottom); 
return insets; 
}); 
e1 = (EditText)findViewById(R.id.editText); 
b = (Button)findViewById(R.id.button); 
t1 = new TextToSpeech(getApplicationContext(), new 
TextToSpeech.OnInitListener() { 
@Override 
public void onInit(int status) { 
if (status!=TextToSpeech.ERROR){ 
} 
} 
t1.setLanguage(Locale.UK); 
}); 
b.setOnClickListener(new View.OnClickListener() { 
@Override 
public void onClick(View view) { 
String tospeak = e1.getText().toString(); 
Toast.makeText(getBaseContext(),tospeak,Toast.LENGTH_LONG).show(
 ); 
t1.speak(tospeak,TextToSpeech.QUEUE_FLUSH,null); 
} 
}); 
} 
} 
OUTPUT ON EMULATOR: 
EXPERIMENT NO.: 19 
Aim: To develop a simple Android application that displays GPS Location. 
1. Open android studio and select new android project by clicking Filemenu  New New 
Project. 
2. Choose the project as Empty Views Activity and click Next. 
3. Give project name (Start with a capital letter) as GPS 
4. Choose the language as Java. 
5. Choose the required android version (Minimum SDK) and select finish. 
6. Go to package explorer in the left hand side and select the project. 
7. Under the project, Go to res folder and select layout. 
8. Double click the activity_main.xml file and design the layout for the page. 
9. Select MainActivity.java file and type the program. 
10.  Now go to activity_main.xml and right click & select run as option and select run 
configuration OR select the virtual device and click on run icon. 
11.  Android output will be displayed on the android emulator. 
Both activity_main.xml and MainActivity.java files together make our application work. The 
activity_main.xml is responsible for the layout (Front end User Interface) of the application. And 
the file MainActivity is responsible for the actions and the performance of the application (back 
end). 
Code: 
activity_main.xml 
<?xml version="1.0" encoding="utf-8"?> 
<androidx.constraintlayout.widget.ConstraintLayout 
xmlns:android="http://schemas.android.com/apk/res/android" 
xmlns:app="http://schemas.android.com/apk/res-auto" 
xmlns:tools="http://schemas.android.com/tools" 
android:id="@+id/main" 
android:layout_width="match_parent" 
android:layout_height="match_parent" 
tools:context=".MainActivity"> 
<TextView 
android:id="@+id/textView" 
android:layout_width="wrap_content" 
android:layout_height="wrap_content" 
android:fontFamily="cursive" 
android:text="GPS Location" 
android:textColor="#2C7C74" 
android:textSize="48sp" 
android:textStyle="bold" 
app:layout_constraintBottom_toBottomOf="parent" 
app:layout_constraintEnd_toEndOf="parent" 
app:layout_constraintStart_toStartOf="parent" 
app:layout_constraintTop_toTopOf="parent" 
app:layout_constraintVertical_bias="0.2" /> 
<Button 
android:id="@+id/button" 
android:layout_width="wrap_content" 
android:layout_height="wrap_content" 
android:layout_marginTop="321dp" 
android:text="Get GPS Location" 
android:textSize="24sp" 
app:layout_constraintEnd_toEndOf="parent" 
app:layout_constraintStart_toStartOf="parent" 
app:layout_constraintTop_toTopOf="parent" /> 
<TextView 
android:id="@+id/loc" 
android:layout_width="wrap_content" 
android:layout_height="wrap_content" 
android:layout_marginStart="45dp" 
android:layout_marginTop="72dp" 
android:text="Location: " 
android:textSize="24sp" 
app:layout_constraintStart_toStartOf="parent" 
app:layout_constraintTop_toBottomOf="@+id/button" /> 
</androidx.constraintlayout.widget.ConstraintLayout> 
MainActivity.java 
package com.example.gps; 
import android.content.Context; 
import android.location.Location; 
import android.location.LocationManager; 
import android.os.Bundle; 
import android.view.View; 
import android.widget.Button; 
import android.widget.TextView; 
import androidx.activity.EdgeToEdge; 
import androidx.appcompat.app.AppCompatActivity; 
import androidx.core.app.ActivityCompat; 
import androidx.core.graphics.Insets; 
import androidx.core.view.ViewCompat; 
import androidx.core.view.WindowInsetsCompat; 
public class MainActivity extends AppCompatActivity { 
private static final int REQUEST_LOCATION = 1; 
Button gps; 
TextView loc; 
LocationManager locationManager; 
String latitude, longitude; 
@Override 
protected void onCreate(Bundle savedInstanceState) { 
super.onCreate(savedInstanceState); 
EdgeToEdge.enable(this); 
setContentView(R.layout.activity_main); 
ViewCompat.setOnApplyWindowInsetsListener(findViewById(R.id.main
 ), (v, insets) -> { 
Insets systemBars = 
insets.getInsets(WindowInsetsCompat.Type.systemBars()); 
v.setPadding(systemBars.left, systemBars.top, 
systemBars.right, systemBars.bottom); 
return insets; 
}); 
gps = (Button) findViewById(R.id.button); 
loc = (TextView) findViewById(R.id.loc); 
ActivityCompat.requestPermissions(this, 
new 
String[]{android.Manifest.permission.ACCESS_FINE_LOCATION}, 
REQUEST_LOCATION); 
gps.setOnClickListener(new View.OnClickListener() { 
@Override 
public void onClick(View v) { 
locationManager = (LocationManager) 
getSystemService(Context.LOCATION_SERVICE); 
Location locationGPS = 
locationManager.getLastKnownLocation(LocationManager.GPS_PROVIDE
 R); 
if (locationGPS != null) { 
double lat = locationGPS.getLatitude(); 
double longi = locationGPS.getLongitude(); 
latitude = String.valueOf(lat); 
longitude = String.valueOf(longi); 
loc.setText("Longitude=" + longitude + "\n" + "Latitude=" + 
latitude + "\n"); 
} else { 
loc.setText("Unable to find GPS location"); 
                } 
            } 
        }); 
    } 
} 
 
OUTPUT ON EMULATOR: 
 
        
 
 
 
 
 
 
 
 
 
 
EXPERIMENT NO.: 20 
Aim:  a) To develop a simple Android application for Scientific calculator. 
1. Open android studio and select new android project by clicking Filemenu  New New 
Project. 
2. Choose the project as Empty Views Activity and click Next. 
3. Give project name (Start with a capital letter) as Calculator 
4. Choose the language as Java. 
5. Choose the required android version (Minimum SDK) and select finish. 
6. Go to package explorer in the left hand side and select the project. 
7. Under the project, Go to res folder and select layout. 
8. Double click the activity_main.xml file and design the layout for the page. 
9. Select MainActivity.java file and type the program. 
10.  Now go to activity_main.xml and right click & select run as option and select run 
configuration OR select the virtual device and click on run icon. 
11.  Android output will be displayed on the android emulator. 
Both activity_main.xml and MainActivity.java files together make our application work. The 
activity_main.xml is responsible for the layout (Front end User Interface) of the application. And 
the file MainActivity is responsible for the actions and the performance of the application (back 
end). 
Code: 
activity_main.xml 
<?xml version="1.0" encoding="utf-8"?> 
<androidx.constraintlayout.widget.ConstraintLayout 
xmlns:android="http://schemas.android.com/apk/res/android" 
xmlns:app="http://schemas.android.com/apk/res-auto" 
xmlns:tools="http://schemas.android.com/tools" 
android:id="@+id/main" 
android:layout_width="match_parent" 
android:layout_height="match_parent" 
tools:context=".MainActivity"> 
<LinearLayout 
android:layout_width="match_parent" 
android:layout_height="match_parent" 
android:layout_marginTop="40dp" 
android:orientation="vertical" 
app:layout_constraintTop_toTopOf="parent"> 
<TextView 
android:layout_width="match_parent" 
android:layout_height="wrap_content" 
android:text="Scientific Calculator" 
            android:textAlignment="center" 
            android:textStyle="bold" 
            android:textColor="#FF008C" 
            android:textSize="40sp" /> 
    </LinearLayout> 
 
    <TableLayout 
        android:layout_width="match_parent" 
        android:layout_height="match_parent" 
        android:layout_marginStart="50dp" 
        android:layout_marginTop="100dp" 
        android:layout_marginEnd="50dp" 
        app:layout_constraintEnd_toEndOf="parent" 
        app:layout_constraintStart_toStartOf="parent" 
        app:layout_constraintTop_toTopOf="parent"> 
 
        <TableRow 
            android:layout_width="match_parent" 
            android:layout_height="match_parent"> 
 
            <TextView 
                android:id="@+id/textView" 
                style="@style/Widget.AppCompat.TextView" 
                android:layout_width="wrap_content" 
                android:layout_height="wrap_content" 
                android:text="Number1" 
                android:textSize="24sp"/> 
 
            <EditText 
                android:id="@+id/e1" 
                android:layout_width="wrap_content" 
                android:layout_height="wrap_content" 
                android:ems="10" 
                android:inputType="numberDecimal" 
                android:text="" /> 
        </TableRow> 
 
        <TableRow 
            android:layout_width="match_parent" 
            android:layout_height="match_parent"> 
 
            <TextView 
                android:id="@+id/textView2" 
                android:layout_width="wrap_content" 
                android:layout_height="wrap_content" 
                android:text="Number2" 
                android:textSize="24sp" /> 
 
            <EditText 
                android:id="@+id/e2" 
                android:layout_width="wrap_content" 
                android:layout_height="wrap_content" 
                android:ems="10" 
                android:inputType="numberDecimal" 
                android:text="" /> 
        </TableRow> 
 
        <TableRow 
            android:layout_width="match_parent" 
            android:layout_height="match_parent"> 
 
            <TextView 
                android:id="@+id/textView3" 
                android:layout_width="wrap_content" 
                android:layout_height="wrap_content" 
                android:text="Result" 
                android:textSize="24sp" /> 
 
            <EditText 
                android:id="@+id/e3" 
                android:layout_width="wrap_content" 
                android:layout_height="wrap_content" 
                android:ems="10" 
                android:inputType="numberDecimal" 
                android:text="" /> 
        </TableRow> 
 
    </TableLayout> 
 
    <TableLayout 
        android:layout_width="match_parent" 
        android:layout_height="match_parent" 
        android:layout_marginStart="50dp" 
        android:layout_marginTop="275dp" 
        android:layout_marginEnd="20dp" 
        app:layout_constraintEnd_toEndOf="parent" 
        app:layout_constraintStart_toStartOf="parent" 
        app:layout_constraintTop_toTopOf="parent"> 
 
        <TableRow 
            android:layout_width="match_parent" 
            android:layout_height="match_parent"> 
 
            <Button 
                android:id="@+id/add" 
                android:layout_width="wrap_content" 
                android:layout_height="wrap_content" 
                android:text="+" 
                android:textSize="40sp" 
                android:onClick="doSum"/> 
 
            <Button 
                android:id="@+id/sub" 
                android:layout_width="wrap_content" 
                android:layout_height="wrap_content" 
                android:text="-" 
                android:onClick="doSub" 
                android:textSize="40sp" /> 
 
            <Button 
                android:id="@+id/mul" 
                android:layout_width="wrap_content" 
                android:layout_height="wrap_content" 
                android:text="*" 
                android:onClick="doMul" 
                android:textSize="40sp" /> 
        </TableRow> 
 
        <TableRow 
            android:layout_width="match_parent" 
            android:layout_height="match_parent"> 
 
            <Button 
                android:id="@+id/div" 
                android:layout_width="wrap_content" 
                android:layout_height="wrap_content" 
                android:text="/" 
                android:onClick="doDiv" 
                android:textSize="40sp" /> 
 
            <Button 
                android:id="@+id/mod" 
                android:layout_width="wrap_content" 
                android:layout_height="wrap_content" 
                android:text="%" 
                android:onClick="doMod" 
                android:textSize="40sp" /> 
 
            <Button 
                android:id="@+id/pow" 
                android:layout_width="wrap_content" 
                android:layout_height="wrap_content" 
                android:text="^^" 
                android:onClick="doPow" 
                android:textSize="40sp" /> 
        </TableRow> 
 
        <TableRow 
            android:layout_width="match_parent" 
            android:layout_height="match_parent"> 
 
            <Button 
                android:id="@+id/sq" 
                android:layout_width="wrap_content" 
                android:layout_height="wrap_content" 
                android:text="SQRT" 
                android:onClick="doSqrt" 
                android:textSize="30sp" /> 
 
            <Button 
                android:id="@+id/exp" 
                android:layout_width="wrap_content" 
                android:layout_height="wrap_content" 
                android:text="EXP" 
                android:onClick="doExp" 
                android:textSize="30sp" /> 
 
            <Button 
                android:id="@+id/log" 
                android:layout_width="wrap_content" 
                android:layout_height="wrap_content" 
                android:text="LOG" 
                android:onClick="doLog" 
                android:textSize="30sp" /> 
        </TableRow> 
        <TableRow 
            android:layout_width="match_parent" 
            android:layout_height="match_parent"> 
 
            <Button 
                android:id="@+id/sin" 
                android:layout_width="wrap_content" 
                android:layout_height="wrap_content" 
                android:text="SIN" 
                android:onClick="doSin" 
                android:textSize="30sp" /> 
 
            <Button 
                android:id="@+id/cos" 
                android:layout_width="wrap_content" 
                android:layout_height="wrap_content" 
                android:text="COS" 
                android:onClick="doCos" 
                android:textSize="30sp" /> 
 
            <Button 
android:id="@+id/tan" 
android:layout_width="wrap_content" 
android:layout_height="wrap_content" 
android:text="TAN" 
android:onClick="doTan" 
android:textSize="30sp" /> 
</TableRow> 
</TableLayout> 
</androidx.constraintlayout.widget.ConstraintLayout> 
MainActivity.java 
package com.example.calculator; 
import android.os.Bundle; 
import android.view.View; 
import android.widget.EditText; 
import androidx.activity.EdgeToEdge; 
import androidx.appcompat.app.AppCompatActivity; 
import androidx.core.graphics.Insets; 
import androidx.core.view.ViewCompat; 
import androidx.core.view.WindowInsetsCompat; 
public class MainActivity extends AppCompatActivity { 
public EditText e1,e2,e3; 
int num1, num2; 
public boolean getNumbers() { 
e1 = (EditText) findViewById(R.id.e1); 
e2 = (EditText) findViewById(R.id.e2); 
e3 = (EditText)findViewById(R.id.e3); 
String s1 = e1.getText().toString(); 
String s2 = e2.getText().toString(); 
if(s1.equals("") || s2.equals("")) 
{ 
String result = "Please enter required values"; 
e3.setText(result); 
return false; 
} 
else 
{ 
} 
num1 = Integer.parseInt(s1); 
num2 = Integer.parseInt(s2); 
return true; 
} 
 
    public boolean getNumber() { 
        e1 = (EditText) findViewById(R.id.e1); 
        e2 = (EditText) findViewById(R.id.e2); 
        e3 = (EditText)findViewById(R.id.e3); 
        String s1 = e1.getText().toString(); 
        String s2 = e2.getText().toString(); 
 
        if(s1.equals("")) 
        { 
            String result = "Please enter required value in 
Number1"; 
            e3.setText(result); 
            return false; 
        } 
        else if(!s1.equals("") && !s2.equals("")) 
        { 
            String result = "Enter value Only in Number1"; 
            e3.setText(result); 
            return false; 
        } 
        else 
        { 
            num1 = Integer.parseInt(s1); 
            // num2 = Integer.parseInt(s2); 
            return true; 
        } 
    } 
    public void doSum(View v) { 
 
        if (getNumbers()) { 
            int sum = num1 + num2; 
            e3.setText(Integer.toString(sum)); 
        } 
    } 
 
    public void doSub(View v) { 
 
        if (getNumbers()) { 
            int sum = num1 - num2; 
            e3.setText(Integer.toString(sum)); 
        } 
 
    } 
 
    public void doMul(View v) { 
 
        if (getNumbers()) { 
            int sum = num1 * num2; 
            e3.setText(Integer.toString(sum)); 
        } 
 
    } 
 
    public void doDiv(View v) { 
        if (getNumbers()) { 
            double sum = num1 / (num2 * 1.0); 
            e3.setText(Double.toString(sum)); 
        } 
 
    } 
 
    public void doMod(View v) { 
        if (getNumbers()) { 
            double sum = num1 % num2; 
            e3.setText(Double.toString(sum)); 
        } 
    } 
 
    public void doPow(View v) { 
 
        if (getNumbers()) { 
            double sum = Math.pow(num1, num2); 
            e3.setText(Double.toString(sum)); 
        } 
    } 
 
    public void doSqrt(View v) { 
 
        if (getNumber()) { 
            double sum = Math.sqrt(num1); 
            e3.setText(Double.toString(sum)); 
        } 
    } 
 
    public void doExp(View v) { 
 
        if (getNumber()) { 
            double sum = Math.exp(num1); 
            e3.setText(Double.toString(sum)); 
        } 
    } 
 
    public void doLog(View v) { 
 
        if (getNumber()) { 
            double sum = Math.log(num1); 
            e3.setText(Double.toString(sum)); 
        } 
    } 
 
    public void doSin(View v) { 
 
        if (getNumber()) { 
            double sum = Math.sin(num1); 
            e3.setText(Double.toString(sum)); 
        } 
    } 
    public void doCos(View v) { 
 
        if (getNumber()) { 
            double sum = Math.cos(num1); 
            e3.setText(Double.toString(sum)); 
        } 
    } 
    public void doTan(View v) { 
 
        if (getNumber()) { 
            double sum = Math.tan(num1); 
            e3.setText(Double.toString(sum)); 
        } 
    } 
 
    @Override 
    protected void onCreate(Bundle savedInstanceState) { 
        super.onCreate(savedInstanceState); 
        EdgeToEdge.enable(this); 
        setContentView(R.layout.activity_main); 
        
ViewCompat.setOnApplyWindowInsetsListener(findViewById(R.id.main
 ), (v, insets) -> { 
            Insets systemBars = 
insets.getInsets(WindowInsetsCompat.Type.systemBars()); 
            v.setPadding(systemBars.left, systemBars.top, 
systemBars.right, systemBars.bottom); 
            return insets; 
        }); 
    } 
} 
 
 
 
 
OUTPUT ON EMULATOR: 
 
 
Aim:  b) To develop a simple Android application for Basic calculator. 
Code: 
activity_main.xml 
<?xml version="1.0" encoding="utf-8"?> 
<androidx.constraintlayout.widget.ConstraintLayout 
xmlns:android="http://schemas.android.com/apk/res/android" 
xmlns:app="http://schemas.android.com/apk/res-auto" 
xmlns:tools="http://schemas.android.com/tools" 
android:id="@+id/main" 
android:layout_width="match_parent" 
android:layout_height="match_parent" 
tools:context=".MainActivity"> 
<LinearLayout 
xmlns:android="http://schemas.android.com/apk/res/android" 
android:orientation="vertical" 
android:layout_width="match_parent" 
        android:layout_height="match_parent" 
        android:layout_margin="20dp"> 
 
        <TextView 
            android:id="@+id/textView2" 
            android:layout_width="match_parent" 
            android:layout_height="wrap_content" 
            android:layout_marginBottom="100dp" 
            android:fontFamily="cursive" 
            android:text="Basic Calculator" 
            android:textAlignment="center" 
            android:textColor="#F44811" 
            android:textSize="48sp" 
            android:textStyle="bold" /> 
 
        <LinearLayout 
            android:id="@+id/linearLayout1" 
            android:layout_width="match_parent" 
            android:layout_height="wrap_content" 
            android:layout_margin="20dp"> 
 
            <EditText 
                android:id="@+id/editText1" 
                android:layout_width="match_parent" 
                android:layout_height="wrap_content" 
                android:layout_weight="1" 
                android:inputType="numberDecimal" 
                android:textSize="20sp" /> 
 
            <EditText 
                android:id="@+id/editText2" 
                android:layout_width="match_parent" 
                android:layout_height="wrap_content" 
                android:layout_weight="1" 
                android:inputType="numberDecimal" 
                android:textSize="20sp" /> 
 
        </LinearLayout> 
 
        <LinearLayout 
            android:id="@+id/linearLayout2" 
            android:layout_width="match_parent" 
            android:layout_height="wrap_content" 
            android:layout_margin="20dp"> 
 
            <Button 
                android:id="@+id/Add" 
                android:layout_width="match_parent" 
                android:layout_height="wrap_content" 
                android:layout_weight="1" 
                android:text="+" 
                android:textSize="30sp"/> 
 
            <Button 
                android:id="@+id/Sub" 
                android:layout_width="match_parent" 
                android:layout_height="wrap_content" 
                android:layout_weight="1" 
                android:text="-" 
                android:textSize="30sp"/> 
 
            <Button 
                android:id="@+id/Mul" 
                android:layout_width="match_parent" 
                android:layout_height="wrap_content" 
                android:layout_weight="1" 
                android:text="*" 
                android:textSize="30sp"/> 
 
            <Button 
                android:id="@+id/Div" 
                android:layout_width="match_parent" 
                android:layout_height="wrap_content" 
                android:layout_weight="1" 
                android:text="/" 
                android:textSize="30sp"/> 
 
        </LinearLayout> 
 
        <TextView 
            android:id="@+id/textView" 
            android:layout_width="match_parent" 
            android:layout_height="wrap_content" 
            android:layout_marginTop="50dp" 
            android:text="Answer is" 
            android:textSize="30sp" 
            android:gravity="center"/> 
 
    </LinearLayout> 
 
 
</androidx.constraintlayout.widget.ConstraintLayout> 
 
 
 
MainActivity.java 
package com.example.basiccalculator123; 
import android.os.Bundle; 
import android.text.TextUtils; 
import android.view.View; 
import android.widget.Button; 
import android.widget.EditText; 
import android.widget.TextView; 
import androidx.activity.EdgeToEdge; 
import androidx.appcompat.app.AppCompatActivity; 
import androidx.core.graphics.Insets; 
import androidx.core.view.ViewCompat; 
import androidx.core.view.WindowInsetsCompat; 
public class MainActivity extends AppCompatActivity { 
EditText Num1,Num2; 
Button Add, Sub, Mul, Div; 
TextView Result; 
@Override 
protected void onCreate(Bundle savedInstanceState) { 
super.onCreate(savedInstanceState); 
EdgeToEdge.enable(this); 
setContentView(R.layout.activity_main); 
ViewCompat.setOnApplyWindowInsetsListener(findViewById(R.id.main
 ), (v, insets) -> { 
Insets systemBars = 
insets.getInsets(WindowInsetsCompat.Type.systemBars()); 
v.setPadding(systemBars.left, systemBars.top, 
systemBars.right, systemBars.bottom); 
return insets; 
}); 
Num1 = (EditText) findViewById(R.id.editText1); 
Num2 = (EditText) findViewById(R.id.editText2); 
Add = (Button) findViewById(R.id.Add); 
Sub = (Button) findViewById(R.id.Sub); 
Mul = (Button) findViewById(R.id.Mul); 
Div = (Button) findViewById(R.id.Div); 
Result = (TextView) findViewById(R.id.textView); 
Add.setOnClickListener(this::onClick); 
Sub.setOnClickListener(this::onClick); 
Mul.setOnClickListener(this::onClick); 
        Div.setOnClickListener(this::onClick); 
    } 
 
    public void onClick(View v) 
    { 
        float num1 = 0; 
        float num2 = 0; 
        float result = 0; 
        String oper = ""; 
        // check if the fields are empty 
        if (TextUtils.isEmpty(Num1.getText().toString()) || 
TextUtils.isEmpty(Num2.getText().toString())) 
            return; 
        // read EditText and fill variables with numbers 
        num1 = Float.parseFloat(Num1.getText().toString()); 
        num2 = Float.parseFloat(Num2.getText().toString()); 
 
        if (v == Add) 
        { 
            oper = "+"; 
            result = num1 + num2; 
        } 
        if (v == Sub) 
        { 
            oper = "-"; 
            result = num1 - num2; 
        } 
        if (v == Mul) 
        { 
            oper = "*"; 
            result = num1 * num2; 
        } 
        if (v == Div) 
        { 
            oper = "/"; 
            result = num1 / num2; 
        } 
        // form the output line 
     Result.setText(num1 + " " + oper + " " + num2 + " = " + result); 
    } 
} 
 
OUTPUT ON EMULATOR: 
   
 
  
 
 
 
EXPERIMENT NO.: 21 
Aim:  To develop a simple Android application that implements Multi threading. 
1. Open android studio and select new android project by clicking Filemenu  New New 
Project. 
2. Choose the project as Empty Views Activity and click Next. 
3. Give project name (Start with a capital letter) as Multithreading 
4. Choose the language as Java. 
5. Choose the required android version (Minimum SDK) and select finish. 
6. Go to package explorer in the left hand side and select the project. 
7. Under the project, Go to res folder and select layout. 
8. Double click the activity_main.xml file and design the layout for the page. 
9. Select MainActivity.java file and type the program. 
10.  Now go to activity_main.xml and right click & select run as option and select run 
configuration OR select the virtual device and click on run icon. 
11.  Android output will be displayed on the android emulator. 
Both activity_main.xml and MainActivity.java files together make our application work. The 
activity_main.xml is responsible for the layout (Front end User Interface) of the application. And 
the file MainActivity is responsible for the actions and the performance of the application (back 
end). 
Code: 
activity_main.xml 
<?xml version="1.0" encoding="utf-8"?> 
<androidx.constraintlayout.widget.ConstraintLayout 
xmlns:android="http://schemas.android.com/apk/res/android" 
xmlns:app="http://schemas.android.com/apk/res-auto" 
xmlns:tools="http://schemas.android.com/tools" 
android:id="@+id/main" 
android:layout_width="match_parent" 
android:layout_height="match_parent" 
tools:context=".MainActivity"> 
<TextView 
android:id="@+id/textView2" 
android:layout_width="wrap_content" 
android:layout_height="wrap_content" 
android:fontFamily="cursive" 
android:text="Multithreading" 
android:textColor="#673AB7" 
android:textSize="48sp" 
android:textStyle="bold" 
app:layout_constraintBottom_toBottomOf="parent" 
app:layout_constraintEnd_toEndOf="parent" 
app:layout_constraintStart_toStartOf="parent" 
app:layout_constraintTop_toTopOf="parent" 
app:layout_constraintVertical_bias="0.057" /> 
<Button 
android:id="@+id/button" 
android:layout_width="wrap_content" 
android:layout_height="wrap_content" 
android:layout_marginTop="19dp" 
android:text="Start Multithreading" 
android:textSize="24sp" 
app:layout_constraintStart_toStartOf="@+id/textView2" 
app:layout_constraintTop_toBottomOf="@+id/textView2" /> 
<TextView 
android:id="@+id/textView" 
android:layout_width="wrap_content" 
android:layout_height="wrap_content" 
android:layout_marginStart="55dp" 
android:layout_marginTop="18dp" 
android:text="Main Thread" 
android:textSize="20sp" 
app:layout_constraintStart_toStartOf="@+id/button" 
app:layout_constraintTop_toBottomOf="@+id/button" /> 
</androidx.constraintlayout.widget.ConstraintLayout> 
MainActivity.java 
package com.example.multithreading; 
import android.os.Bundle; 
import android.os.Handler; 
import android.view.View; 
import android.widget.Button; 
import android.widget.TextView; 
import androidx.activity.EdgeToEdge; 
import androidx.appcompat.app.AppCompatActivity; 
import androidx.core.graphics.Insets; 
import androidx.core.view.ViewCompat; 
import androidx.core.view.WindowInsetsCompat; 
public class MainActivity extends AppCompatActivity { 
Button mt; 
TextView th; 
private static final int t1 = 1; 
private static final int t2 = 2; 
private static final int t3 = 3; 
    @Override 
    protected void onCreate(Bundle savedInstanceState) { 
        super.onCreate(savedInstanceState); 
        EdgeToEdge.enable(this); 
        setContentView(R.layout.activity_main); 
        
ViewCompat.setOnApplyWindowInsetsListener(findViewById(R.id.main
 ), (v, insets) -> { 
            Insets systemBars = 
insets.getInsets(WindowInsetsCompat.Type.systemBars()); 
            v.setPadding(systemBars.left, systemBars.top, 
systemBars.right, systemBars.bottom); 
            return insets; 
        }); 
 
        mt = (Button) findViewById(R.id.button); 
        th = (TextView) findViewById(R.id.textView); 
            Handler handler = new Handler() { 
                public void handleMessage(android.os.Message 
msg) { 
                    if (msg.what == t1) { 
                        th.append("\nIn Thread 1"); 
                    } 
                    if (msg.what == t2) { 
                        th.append("\nIn Thread 2"); 
                    } 
                    if (msg.what == t3) { 
                        th.append("\nIn Thread 3"); 
                    } 
                }    }; 
       Thread thread1 = new Thread(new Runnable() { 
            @Override 
            public void run() 
            { 
                for (int i = 0; i < 5; i++) 
                { 
                    try { Thread.sleep(1000); 
                    } catch(InterruptedException e) 
                    { e.printStackTrace(); } 
                    handler.sendEmptyMessage(t1); 
                }}}); 
 
        Thread thread2 = new Thread(new Runnable() { 
            @Override public void run() 
            { for (int i = 0; i < 5; i++) 
            { 
                try { Thread.sleep(1000); } 
                catch(InterruptedException e) 
                { e.printStackTrace(); } 
handler.sendEmptyMessage(t2); 
} } }); 
Thread thread3 = new Thread(new Runnable() 
{ 
@Override 
public void run() 
{ for (int i = 0; i < 5; i++) 
{ try { Thread.sleep(1000); } 
catch(InterruptedException e) 
{ e.printStackTrace(); } 
handler.sendEmptyMessage(t3); } } }); 
mt.setOnClickListener(new View.OnClickListener() { 
@Override 
public void onClick(View view) { 
th.setText("Main thread"); 
thread1.start(); 
thread2.start(); 
thread3.start(); 
} 
}); 
} 
} 
OUTPUT ON EMULATOR: 
EXPERIMENT NO.: 22 
Aim:  a) To develop a simple Android application that makes use of Databases. 
Student Dabase 
1. Open android studio and select new android project by clicking Filemenu  New New 
Project. 
2. Choose the project as Empty Views Activity and click Next. 
3. Give project name (Start with a capital letter) as StudentDatabase 
4. Choose the language as Java. 
5. Choose the required android version (Minimum SDK) and select finish. 
6. Go to package explorer in the left hand side and select the project. 
7. Under the project, Go to res folder and select layout. 
8. Double click the activity_main.xml file and design the layout for the page. 
9. Select MainActivity.java file and type the program. 
10.  Now go to activity_main.xml and right click & select run as option and select run 
configuration OR select the virtual device and click on run icon. 
11.  Android output will be displayed on the android emulator. 
Both activity_main.xml and MainActivity.java files together make our application work. The 
activity_main.xml is responsible for the layout (Front end User Interface) of the application. And 
the file MainActivity is responsible for the actions and the performance of the application (back 
end). 
Code: 
activity_main.xml 
<?xml version="1.0" encoding="utf-8"?> 
<androidx.constraintlayout.widget.ConstraintLayout 
xmlns:android="http://schemas.android.com/apk/res/android" 
xmlns:app="http://schemas.android.com/apk/res-auto" 
xmlns:tools="http://schemas.android.com/tools" 
android:id="@+id/main" 
android:layout_width="match_parent" 
android:layout_height="match_parent" 
tools:context=".MainActivity"> 
<LinearLayout android:layout_width="match_parent" 
android:layout_height="match_parent" 
android:orientation="vertical"> <LinearLayout 
android:layout_width="match_parent" 
android:layout_height="match_parent" 
android:orientation="vertical"> <TextView 
android:layout_width="match_parent" 
android:layout_height="wrap_content" 
android:layout_x="43dp" android:layout_y="32dp" 
android:background="#59DBEC" android:text="Student Details" 
android:textAlignment="center" 
android:textAppearance="@style/TextAppearance.AppCompat.Large" 
android:textColor="#DD2323" android:textSize="34sp" 
android:textStyle="bold" android:visibility="visible" />  
</LinearLayout> </LinearLayout>  
<TableLayout android:layout_width="match_parent" 
android:layout_height="match_parent" 
android:layout_marginStart="20dp" 
android:layout_marginTop="100dp" 
app:layout_constraintStart_toStartOf="parent" 
app:layout_constraintTop_toTopOf="parent"> <TableRow 
android:layout_width="match_parent" 
android:layout_height="match_parent"> <TextView 
android:layout_width="wrap_content" 
android:layout_height="wrap_content" android:layout_x="20dp" 
android:layout_y="110dp" android:text="Enter Rollno:" 
android:textSize="24sp" /> <EditText android:id="@+id/Rollno" 
android:layout_width="150dp" 
android:layout_height="wrap_content" android:layout_x="175dp" 
android:layout_y="100dp" android:inputType="number" 
android:textSize="20sp" /> </TableRow> <TableRow 
android:layout_width="match_parent" 
android:layout_height="match_parent"> <TextView 
android:layout_width="wrap_content" 
android:layout_height="wrap_content" android:layout_x="20dp" 
android:layout_y="160dp" android:text="Enter Name:" 
android:textSize="24sp" /> <EditText android:id="@+id/Name" 
android:layout_width="150dp" 
android:layout_height="wrap_content" android:layout_x="175dp" 
android:layout_y="150dp" 
android:inputType="text" android:textSize="20sp" /> 
</TableRow> <TableRow android:layout_width="match_parent" 
android:layout_height="match_parent"> <TextView 
android:layout_width="wrap_content" 
android:layout_height="wrap_content" android:layout_x="20dp" 
android:layout_y="210dp" android:text="Enter Marks:" 
android:textSize="24sp" /> <EditText android:id="@+id/Marks" 
android:layout_width="150dp" 
android:layout_height="wrap_content" android:layout_x="175dp" 
android:layout_y="200dp" android:inputType="number" 
android:textSize="20sp" /> </TableRow> <TableRow 
android:layout_width="match_parent" 
android:layout_height="match_parent"> <Button 
android:id="@+id/Insert" android:layout_width="94dp" 
android:layout_height="wrap_content" android:layout_x="25dp" 
android:layout_y="300dp" android:text="Insert" 
android:textSize="24sp" /> <Button android:id="@+id/Delete" 
android:layout_width="150dp" 
android:layout_height="wrap_content" android:layout_x="200dp" 
android:layout_y="300dp" android:text="Delete" 
android:textSize="24sp" /> </TableRow> <TableRow 
android:layout_width="match_parent" 
android:layout_height="match_parent"> <Button 
android:id="@+id/Update" android:layout_width="150dp" 
android:layout_height="wrap_content" android:layout_x="25dp" 
android:layout_y="400dp" android:text="Update" 
android:textSize="24sp" /> 
<Button android:id="@+id/View" android:layout_width="150dp" 
android:layout_height="wrap_content" android:layout_x="200dp" 
android:layout_y="400dp" android:text="View" 
android:textSize="24sp" /> </TableRow> <TableRow 
android:layout_width="match_parent" 
android:layout_height="match_parent"> <Button 
android:id="@+id/ViewAll" android:layout_width="200dp" 
android:layout_height="wrap_content" android:layout_x="100dp" 
android:layout_y="500dp" android:text="View All" 
android:textSize="24sp" /> </TableRow> </TableLayout> 
</androidx.constraintlayout.widget.ConstraintLayout> 
MainActivity.java 
package com.example.studentdatabase; 
import android.content.Context; 
import android.database.Cursor; 
import android.database.sqlite.SQLiteDatabase; 
import android.os.Bundle; 
import android.widget.Button; 
import android.widget.EditText; 
import android.app.AlertDialog.Builder; 
import android.view.View; 
import androidx.activity.EdgeToEdge; 
import androidx.appcompat.app.AppCompatActivity; 
import androidx.core.graphics.Insets; 
import androidx.core.view.ViewCompat; 
import androidx.core.view.WindowInsetsCompat; 
public class MainActivity extends AppCompatActivity { 
EditText Rollno, Name, Marks; 
Button Insert, Delete, Update, View1, ViewAll; 
SQLiteDatabase db; 
@Override 
protected void onCreate(Bundle savedInstanceState) { 
super.onCreate(savedInstanceState); 
EdgeToEdge.enable(this); 
setContentView(R.layout.activity_main); 
ViewCompat.setOnApplyWindowInsetsListener(findViewById(R.id.main
 ), (v, insets) -> { 
Insets systemBars = 
insets.getInsets(WindowInsetsCompat.Type.systemBars()); 
v.setPadding(systemBars.left, systemBars.top, 
systemBars.right, systemBars.bottom); 
return insets; 
}); 
Rollno = (EditText) findViewById(R.id.Rollno); 
Name = (EditText) findViewById(R.id.Name); 
Marks = (EditText) findViewById(R.id.Marks); 
Insert = (Button) findViewById(R.id.Insert); 
Delete = (Button) findViewById(R.id.Delete); 
Update = (Button) findViewById(R.id.Update); 
View1 = (Button) findViewById(R.id.View); 
ViewAll = (Button) findViewById(R.id.ViewAll); 
Insert.setOnClickListener(this::onClick); 
Delete.setOnClickListener(this::onClick); 
Update.setOnClickListener(this::onClick); 
View1.setOnClickListener(this::onClick); 
ViewAll.setOnClickListener(this::onClick); 
// Creating database and table 
db = openOrCreateDatabase("StudentDB", 
Context.MODE_PRIVATE, null); 
db.execSQL("CREATE TABLE IF NOT EXISTS student(rollno 
VARCHAR,name VARCHAR,marks VARCHAR);"); 
} 
public void onClick(View view) { 
// Inserting a record to the Student table 
if (view == Insert) { 
// Checking for empty fields 
if (Rollno.getText().toString().trim().length() == 0 
|| Name.getText().toString().trim().length() == 0 || 
Marks.getText().toString().trim().length() == 0) { 
showMessage("Error", "Please enter all values"); 
return; 
} 
db.execSQL("INSERT INTO student VALUES('" + 
Rollno.getText() + "','" + Name.getText() + "','" + 
Marks.getText() + "');"); 
showMessage("Success", "Record added"); 
clearText(); 
} 
// Deleting a record from the Student table 
        if (view == Delete) { 
            // Checking for empty roll number 
            if (Rollno.getText().toString().trim().length() == 
0) { 
                showMessage("Error", "Please enter Rollno"); 
                return; 
            } 
 
            Cursor c = db.rawQuery("SELECT * FROM student WHERE 
rollno='" + Rollno.getText() + "'", null); 
            if (c.moveToFirst()) { 
                db.execSQL("DELETE FROM student WHERE rollno='" 
+ Rollno.getText() + "'"); 
                showMessage("Success", "Record Deleted"); 
            } else { 
                showMessage("Error", "Invalid Rollno"); 
            } 
            clearText(); 
        } 
        // Updating a record in the Student table 
        if (view == Update) { // Checking for empty roll number 
            if (Rollno.getText().toString().trim().length() == 
0) { 
                showMessage("Error", "Please enter Rollno"); 
                return; 
            } 
            Cursor c = db.rawQuery("SELECT * FROM student WHERE 
rollno='" + Rollno.getText() + "'", null); 
            if (c.moveToFirst()) { 
                db.execSQL("UPDATE student SET name='" + 
Name.getText() + "',marks='" + Marks.getText() + "' WHERE 
rollno='" + Rollno.getText() + "'"); 
                showMessage("Success", "Record Modified"); 
            } else { 
                showMessage("Error", "Invalid Rollno"); 
            } 
            clearText(); 
        } 
        // Display a record from the Student table 
        if (view == View1) { 
            // Checking for empty roll number 
            if (Rollno.getText().toString().trim().length() == 
0) { 
                showMessage("Error", "Please enter Rollno"); 
                return; 
            } 
            Cursor c = db.rawQuery("SELECT * FROM student WHERE 
rollno='" + Rollno.getText() + "'", null); 
            if (c.moveToFirst()) { 
                Name.setText(c.getString(1)); 
                Marks.setText(c.getString(2)); 
            } else { 
                showMessage("Error", "Invalid Rollno"); 
                clearText(); 
            } 
        } 
        // Displaying all the records 
        if (view == ViewAll) { 
            Cursor c = db.rawQuery("SELECT * FROM student", 
null); 
            if (c.getCount() == 0) { 
                showMessage("Error", "No records found"); 
                return; 
            } 
            StringBuffer buffer = new StringBuffer(); 
            while (c.moveToNext()) { 
                buffer.append("Rollno: " + c.getString(0) + 
"\n"); 
                buffer.append("Name: " + c.getString(1) + "\n"); 
                buffer.append("Marks: " + c.getString(2) + 
"\n\n"); 
            } 
            showMessage("Student Details", buffer.toString()); 
        } 
    } 
 
    public void showMessage(String title, String message) { 
        Builder builder = new Builder(this); 
        builder.setCancelable(true); 
        builder.setTitle(title); 
        builder.setMessage(message); 
        builder.show(); 
    } 
 
    public void clearText() { 
        Rollno.setText(""); 
        Name.setText(""); 
        Marks.setText(""); 
        Rollno.requestFocus(); 
    } 
} 
 
OUTPUT ON EMULATOR: 
b) To develop a simple Android application that makes use of Product Databases. 
activity_main.xml 
<?xml version="1.0" encoding="utf-8"?> 
<androidx.constraintlayout.widget.ConstraintLayout 
xmlns:android="http://schemas.android.com/apk/res/android" 
xmlns:app="http://schemas.android.com/apk/res-auto" 
xmlns:tools="http://schemas.android.com/tools" 
android:id="@+id/main" 
android:layout_width="match_parent" 
android:layout_height="match_parent" 
tools:context=".MainActivity"> 
<TextView 
android:id="@+id/textView4" 
android:layout_width="wrap_content" 
android:layout_height="wrap_content" 
android:fontFamily="cursive" 
        android:text="Product Database" 
        android:textColor="#0993A6" 
        android:textSize="48sp" 
        android:textStyle="bold" 
        app:layout_constraintBottom_toBottomOf="parent" 
        app:layout_constraintEnd_toEndOf="parent" 
        app:layout_constraintStart_toStartOf="parent" 
        app:layout_constraintTop_toTopOf="parent" 
        app:layout_constraintVertical_bias="0.057" /> 
 
    <TextView 
        android:id="@+id/textView" 
        android:layout_width="wrap_content" 
        android:layout_height="wrap_content" 
        android:layout_marginStart="28dp" 
        android:layout_marginEnd="54dp" 
        android:text="Product ID:" 
        android:textSize="24sp" 
        app:layout_constraintBaseline_toBaselineOf="@+id/pid" 
        app:layout_constraintEnd_toStartOf="@+id/pid" 
        app:layout_constraintStart_toStartOf="parent" /> 
 
    <TextView 
        android:id="@+id/textView2" 
        android:layout_width="wrap_content" 
        android:layout_height="wrap_content" 
        android:layout_marginStart="28dp" 
        android:layout_marginTop="16dp" 
        android:layout_marginEnd="11dp" 
        android:text="Product Name:" 
        android:textSize="24sp" 
        app:layout_constraintEnd_toStartOf="@+id/pname" 
        app:layout_constraintStart_toStartOf="parent" 
        app:layout_constraintTop_toTopOf="@+id/pname" /> 
 
    <TextView 
        android:id="@+id/textView3" 
        android:layout_width="wrap_content" 
        android:layout_height="wrap_content" 
        android:layout_marginStart="28dp" 
        android:layout_marginEnd="32dp" 
        android:text="Product Price:" 
        android:textSize="24sp" 
        app:layout_constraintBaseline_toBaselineOf="@+id/price" 
        app:layout_constraintEnd_toStartOf="@+id/price" 
        app:layout_constraintStart_toStartOf="parent" /> 
 
    <EditText 
        android:id="@+id/pid" 
        android:layout_width="0dp" 
        android:layout_height="0dp" 
        android:layout_marginTop="170dp" 
        android:layout_marginEnd="7dp" 
        android:layout_marginBottom="49dp" 
        android:ems="10" 
        android:inputType="text" 
        android:textSize="24sp" 
        app:layout_constraintBottom_toTopOf="@+id/pname" 
        app:layout_constraintEnd_toEndOf="parent" 
        app:layout_constraintStart_toEndOf="@+id/textView" 
        app:layout_constraintTop_toTopOf="parent" /> 
 
    <EditText 
        android:id="@+id/pname" 
        android:layout_width="0dp" 
        android:layout_height="0dp" 
        android:layout_marginEnd="12dp" 
        android:layout_marginBottom="54dp" 
        android:ems="10" 
        android:inputType="text" 
        android:textSize="24sp" 
        app:layout_constraintBottom_toTopOf="@+id/price" 
        app:layout_constraintEnd_toEndOf="parent" 
        app:layout_constraintStart_toEndOf="@+id/textView2" 
        app:layout_constraintTop_toBottomOf="@+id/pid" /> 
 
    <EditText 
        android:id="@+id/price" 
        android:layout_width="0dp" 
        android:layout_height="0dp" 
        android:layout_marginEnd="14dp" 
        android:layout_marginBottom="86dp" 
        android:ems="10" 
        android:inputType="text" 
        android:textSize="24sp" 
        app:layout_constraintBottom_toTopOf="@+id/display" 
        app:layout_constraintEnd_toEndOf="parent" 
        app:layout_constraintStart_toEndOf="@+id/textView3" 
        app:layout_constraintTop_toBottomOf="@+id/pname" /> 
 
    <Button 
        android:id="@+id/insert" 
        android:layout_width="wrap_content" 
        android:layout_height="wrap_content" 
        android:layout_marginStart="15dp" 
        android:layout_marginEnd="12dp" 
        android:text="Insert Data" 
        android:textSize="24sp" 
app:layout_constraintBaseline_toBaselineOf="@+id/display" 
app:layout_constraintEnd_toStartOf="@+id/display" 
app:layout_constraintHorizontal_chainStyle="packed" 
app:layout_constraintStart_toStartOf="parent" /> 
<Button 
android:id="@+id/display" 
android:layout_width="wrap_content" 
android:layout_height="wrap_content" 
android:layout_marginBottom="175dp" 
android:text="Display Data" 
android:textSize="24sp" 
app:layout_constraintBottom_toBottomOf="parent" 
app:layout_constraintEnd_toEndOf="parent" 
app:layout_constraintStart_toEndOf="@+id/insert" 
app:layout_constraintTop_toBottomOf="@+id/price" /> 
</androidx.constraintlayout.widget.ConstraintLayout> 
MainActivity.java 
package com.example.productdatabase; 
import android.app.AlertDialog; 
import android.content.Context; 
import android.database.Cursor; 
import android.database.sqlite.SQLiteDatabase; 
import android.os.Bundle; 
import android.view.View; 
import android.widget.Button; 
import android.widget.EditText; 
import android.widget.Toast; 
import androidx.activity.EdgeToEdge; 
import androidx.appcompat.app.AppCompatActivity; 
import androidx.core.graphics.Insets; 
import androidx.core.view.ViewCompat; 
import androidx.core.view.WindowInsetsCompat; 
public class MainActivity extends AppCompatActivity { 
EditText pid,pname,price; 
Button insert, display; 
SQLiteDatabase db; 
@Override 
protected void onCreate(Bundle savedInstanceState) { 
super.onCreate(savedInstanceState); 
EdgeToEdge.enable(this); 
setContentView(R.layout.activity_main); 
ViewCompat.setOnApplyWindowInsetsListener(findViewById(R.id.main
 ), (v, insets) -> { 
Insets systemBars = 
insets.getInsets(WindowInsetsCompat.Type.systemBars()); 
v.setPadding(systemBars.left, systemBars.top, 
systemBars.right, systemBars.bottom); 
return insets; 
}); 
pid = (EditText) findViewById(R.id.pid); 
pname = (EditText) findViewById(R.id.pname); 
price = (EditText) findViewById(R.id.price); 
insert = (Button) findViewById(R.id.insert); 
display = (Button) findViewById(R.id.display); 
db = openOrCreateDatabase("ProductDB", Context.MODE_PRIVATE, 
null); 
db.execSQL("CREATE TABLE IF NOT EXISTS product(pid 
VARCHAR,pname VARCHAR,price VARCHAR);"); 
insert.setOnClickListener(new View.OnClickListener() { 
@Override 
public void onClick(View view) { 
if (pid.getText().toString().trim().length() == 0 || 
pname.getText().toString().trim().length() == 0 || 
price.getText().toString().trim().length() == 0) { 
// Toast.makeText(getBaseContext(),"Enter all 
values",Toast.LENGTH_LONG); 
showMessage("Error", "Please enter all values"); 
return; 
} 
db.execSQL("INSERT INTO product VALUES('" + 
pid.getText() + "','" + pname.getText() + "','" + 
price.getText() + "');"); 
// Toast.makeText(getBaseContext(),"Record added 
successfully",Toast.LENGTH_LONG); 
}); 
} 
showMessage("Success", "Record added"); 
display.setOnClickListener(new View.OnClickListener() { 
@Override 
public void onClick(View view) { 
Cursor c = db.rawQuery("SELECT * FROM product", null); 
if (c.getCount() == 0) { 
// Toast.makeText(getBaseContext()," Error : 
No records found",Toast.LENGTH_LONG); 
showMessage("Error", "No records found"); 
return; 
} 
StringBuffer buffer = new StringBuffer(); 
while (c.moveToNext()) { 
buffer.append("PID: " + c.getString(0) + "\n"); 
buffer.append("PNAME: " + c.getString(1) + "\n"); 
buffer.append("PRICE: " + c.getString(2) + "\n\n"); 
} 
// Toast.makeText(getBaseContext(),"Product 
Details" + buffer.toString(),Toast.LENGTH_LONG); 
showMessage("Product Details", buffer.toString()); 
} 
}); 
} 
public void showMessage(String title, String message) { 
AlertDialog.Builder builder = new AlertDialog.Builder(this); 
builder.setCancelable(true); 
builder.setTitle(title); 
builder.setMessage(message); 
builder.show(); 
} 
} 
OUTPUT ON EMULATOR: 
   
 
 
 
 
 
 
 
 
 
 
 
 
EXPERIMENT NO.: 23 
Aim:  To develop a simple Android application that creates an alert Dialogue upon receiving a 
message. 
1. Open android studio and select new android project by clicking Filemenu  New New 
Project. 
2. Choose the project as Empty Views Activity and click Next. 
3. Give project name (Start with a capital letter) as AlertDialogue 
4. Choose the language as Java. 
5. Choose the required android version (Minimum SDK) and select finish. 
6. Go to package explorer in the left hand side and select the project. 
7. Under the project, Go to res folder and select layout. 
8. Double click the activity_main.xml file and design the layout for the page. 
9. Select MainActivity.java file and type the program. 
10.  Now go to activity_main.xml and right click & select run as option and select run 
configuration OR select the virtual device and click on run icon. 
11.  Android output will be displayed on the android emulator. 
Both activity_main.xml and MainActivity.java files together make our application work. The 
activity_main.xml is responsible for the layout (Front end User Interface) of the application. And 
the file MainActivity is responsible for the actions and the performance of the application (back 
end). 
Code: 
activity_main.xml 
<?xml version="1.0" encoding="utf-8"?> 
<androidx.constraintlayout.widget.ConstraintLayout 
xmlns:android="http://schemas.android.com/apk/res/android" 
xmlns:tools="http://schemas.android.com/tools" 
xmlns:app="http://schemas.android.com/apk/res-auto" 
android:id="@+id/main" 
android:layout_width="match_parent" 
android:layout_height="match_parent" 
tools:context=".MainActivity"> 
<LinearLayout 
android:layout_width="match_parent" 
android:layout_height="match_parent" 
android:layout_marginStart="100dp" 
android:layout_marginTop="100dp" 
android:layout_marginEnd="100dp" 
android:layout_marginBottom="100dp" 
android:orientation="vertical" 
app:layout_constraintBottom_toBottomOf="parent" 
app:layout_constraintEnd_toEndOf="parent" 
app:layout_constraintStart_toStartOf="parent" 
app:layout_constraintTop_toTopOf="parent"> 
<TextView 
android:id="@+id/textView" 
android:layout_width="232dp" 
android:layout_height="wrap_content" 
android:layout_marginBottom="100dp" 
android:fontFamily="cursive" 
android:text="Alert Dialogue" 
android:textColor="#E90F0F" 
android:textSize="34sp" /> 
<TextView 
android:layout_width="wrap_content" 
android:layout_height="wrap_content" 
android:text="Enter Message" 
android:textAlignment="center" 
android:textColor="#3F51B5" 
android:textSize="24sp" /> 
<EditText 
android:id="@+id/e1" 
android:layout_width="match_parent" 
android:layout_height="wrap_content" 
android:ems="10" 
android:inputType="textPersonName" /> 
<Button 
android:id="@+id/button" 
android:layout_width="match_parent" 
android:layout_height="wrap_content" 
android:text="Submit" 
android:textSize="24sp" /> 
<Button 
android:id="@+id/button2" 
android:layout_width="match_parent" 
android:layout_height="wrap_content" 
android:text="Close App" 
android:textSize="24sp" /> 
</LinearLayout> 
</androidx.constraintlayout.widget.ConstraintLayout> 
MainActivity.java 
package com.example.alertdialogue; 
import android.content.DialogInterface; 
import android.os.Bundle; 
import android.view.View; 
import android.widget.Button; 
import android.widget.EditText; 
import android.widget.Toast; 
import androidx.activity.EdgeToEdge; 
import androidx.appcompat.app.AlertDialog; 
import androidx.appcompat.app.AppCompatActivity; 
import androidx.core.graphics.Insets; 
import androidx.core.view.ViewCompat; 
import androidx.core.view.WindowInsetsCompat; 
public class MainActivity extends AppCompatActivity { 
Button submitButton, closeButton; 
EditText e1; 
AlertDialog.Builder builder; 
@Override 
protected void onCreate(Bundle savedInstanceState) { 
super.onCreate(savedInstanceState); 
EdgeToEdge.enable(this); 
setContentView(R.layout.activity_main); 
ViewCompat.setOnApplyWindowInsetsListener(findViewById(R.id.main
 ), (v, insets) -> { 
Insets systemBars = 
insets.getInsets(WindowInsetsCompat.Type.systemBars()); 
v.setPadding(systemBars.left, systemBars.top, 
systemBars.right, systemBars.bottom); 
return insets; 
}); 
e1 = (EditText) findViewById(R.id.e1); 
submitButton = (Button) findViewById(R.id.button); 
closeButton = (Button)findViewById(R.id.button2); 
builder = new AlertDialog.Builder(this); 
submitButton.setOnClickListener(new 
View.OnClickListener() { 
@Override 
public void onClick(View v) { 
builder.setMessage(R.string.dialog_message) 
.setTitle(R.string.dialog_title); 
//Setting message manually and performing action on button click 
builder.setMessage("Do you want to submit your 
Message ?") 
.setCancelable(false) 
.setPositiveButton("Yes", new 
DialogInterface.OnClickListener() { 
public void onClick(DialogInterface 
dialog, int id) { 
String s1 = " Your Message: 
"+e1.getText().toString()+" has been submitted successfully"; 
// finish(); 
dialog.cancel(); 
Toast.makeText(getApplicationContext(),s1,Toast.LENGTH_SHORT).sh
 ow(); 
} 
}) 
.setNegativeButton("No", new 
DialogInterface.OnClickListener() { 
public void onClick(DialogInterface 
dialog, int id) { 
// Action for 'NO' Button 
dialog.cancel(); 
Toast.makeText(getApplicationContext(),"You choosen not to send 
message", Toast.LENGTH_SHORT).show(); 
} 
}); 
//Creating dialog box 
AlertDialog alert = builder.create(); 
//Setting the title manually 
alert.setTitle("Alert Dialog"); 
alert.show(); 
} 
}); 
closeButton.setOnClickListener(new 
View.OnClickListener() { 
@Override 
public void onClick(View v) { 
//Uncomment the below code to Set the message and title from the 
strings.xml file 
builder.setMessage(R.string.dialog_message).setTitle(R.string.di
 alog_title); 
//Setting message manually and performing action on button click 
builder.setMessage("Do you want to close this 
application ?").setCancelable(false) 
.setPositiveButton("Yes", new 
DialogInterface.OnClickListener() { 
public void onClick(DialogInterface dialog, int id) { 
finish(); 
Toast.makeText(getApplicationContext(), "Your App has been 
Closed", Toast.LENGTH_SHORT).show(); 
} 
}) 
.setNegativeButton("No", new 
DialogInterface.OnClickListener() { 
public void onClick(DialogInterface dialog, int id) { 
// Action for 'NO' Button 
dialog.cancel(); 
Toast.makeText(getApplicationContext(), "You choosen not to 
close App",Toast.LENGTH_SHORT).show(); 
} 
}); 
AlertDialog alert = builder.create(); 
//Setting the title manually 
alert.setTitle("Alert Dialog"); 
alert.show(); 
} 
}); 
} 
} 
Strings.xml 
<resources> 
<string name="app_name">AlertDialogue</string> 
<string name="dialog_message">Welcome to Alert Dialog</string> 
<string name="dialog_title">Alert Dialog</string> 
</resources> 
OUTPUT ON EMULATOR: 
    
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
EXPERIMENT NO.: 24 
Aim:  a) To develop a simple Android application that writes data to the SDCard (External 
Storage). 
1. Open android studio and select new android project by clicking Filemenu  New New 
Project. 
2. Choose the project as Empty Views Activity and click Next. 
3. Give project name (Start with a capital letter) as ExternalfileReadWrite 
4. Choose the language as Java. 
5. Choose the required android version (Minimum SDK) and select finish. 
6. Go to package explorer in the left hand side and select the project. 
7. Under the project, Go to res folder and select layout. 
8. Double click the activity_main.xml file and design the layout for the page. 
9. Select MainActivity.java file and type the program. 
10.  Now go to activity_main.xml and right click & select run as option and select run 
configuration OR select the virtual device and click on run icon. 
11.  Android output will be displayed on the android emulator. 
Both activity_main.xml and MainActivity.java files together make our application work. The 
activity_main.xml is responsible for the layout (Front end User Interface) of the application. And 
the file MainActivity is responsible for the actions and the performance of the application (back 
end). 
Code: 
activity_main.xml 
AndroidManifest.xml 
<uses-permission 
android:name="android.permission.WRITE_EXTERNAL_STORAGE"></uses
permission> 
<uses-permission 
android:name="android.permission.READ_EXTERNAL_STORAGE"></uses
permission> 
Activity_main.xml 
<?xml version="1.0" encoding="utf-8"?> 
<androidx.constraintlayout.widget.ConstraintLayout 
xmlns:android="http://schemas.android.com/apk/res/android" 
xmlns:app="http://schemas.android.com/apk/res-auto" 
xmlns:tools="http://schemas.android.com/tools" 
android:id="@+id/main" 
android:layout_width="match_parent" 
android:layout_height="match_parent" 
tools:context=".MainActivity"> 
 
    <TextView 
        android:id="@+id/textView" 
        android:layout_width="wrap_content" 
        android:layout_height="wrap_content" 
        android:layout_marginTop="43dp" 
        android:layout_marginBottom="79dp" 
        android:text="External Storage File Read / Write Demo" 
        android:textAlignment="center" 
        android:textColor="#0895A8" 
        android:textSize="38sp" 
        android:textStyle="bold" 
        app:layout_constraintBottom_toTopOf="@+id/data" 
        app:layout_constraintEnd_toEndOf="parent" 
        app:layout_constraintHorizontal_bias="0.2" 
        app:layout_constraintStart_toStartOf="parent" 
        app:layout_constraintTop_toTopOf="parent" 
        app:layout_constraintVertical_bias="0.064" /> 
 
    <EditText 
        android:id="@+id/data" 
        android:layout_width="0dp" 
        android:layout_height="0dp" 
        android:layout_marginStart="55dp" 
        android:layout_marginEnd="55dp" 
        android:layout_marginBottom="36dp" 
        android:ems="10" 
        android:inputType="text" 
        android:textSize="24sp" 
        app:layout_constraintBottom_toTopOf="@+id/write" 
        app:layout_constraintEnd_toEndOf="parent" 
        app:layout_constraintStart_toStartOf="parent" 
        app:layout_constraintTop_toBottomOf="@+id/textView" /> 
 
    <Button 
        android:id="@+id/write" 
        android:layout_width="wrap_content" 
        android:layout_height="wrap_content" 
        android:layout_marginBottom="38dp" 
        android:text="Write Data" 
        android:textSize="30sp" 
        app:layout_constraintBottom_toTopOf="@+id/read" 
        app:layout_constraintEnd_toEndOf="parent" 
        app:layout_constraintStart_toStartOf="parent" 
        app:layout_constraintTop_toBottomOf="@+id/data" /> 
 
    <Button 
        android:id="@+id/read" 
        android:layout_width="wrap_content" 
android:layout_height="wrap_content" 
android:layout_marginBottom="259dp" 
android:text="Read Data" 
android:textSize="30sp" 
app:layout_constraintBottom_toBottomOf="parent" 
app:layout_constraintEnd_toEndOf="@+id/write" 
app:layout_constraintTop_toBottomOf="@+id/write" /> 
<TextView 
android:id="@+id/Responce" 
android:layout_width="wrap_content" 
android:layout_height="wrap_content" 
android:layout_marginStart="24dp" 
android:layout_marginTop="51dp" 
android:text="Response" 
android:textColor="#E91E63" 
android:textSize="34sp" 
app:layout_constraintStart_toStartOf="@+id/read" 
app:layout_constraintTop_toBottomOf="@+id/read" /> 
</androidx.constraintlayout.widget.ConstraintLayout> 
MainActivity.java 
package com.example.externalstorage; 
import android.os.Bundle; 
import android.os.Environment; 
import android.view.View; 
import android.widget.Button; 
import android.widget.EditText; 
import android.widget.TextView; 
import androidx.activity.EdgeToEdge; 
import androidx.appcompat.app.AppCompatActivity; 
import androidx.core.graphics.Insets; 
import androidx.core.view.ViewCompat; 
import androidx.core.view.WindowInsetsCompat; 
import java.io.BufferedReader; 
import java.io.DataInputStream; 
import java.io.File; 
import java.io.FileOutputStream; 
import java.io.FileInputStream; 
import java.io.IOException; 
import java.io.InputStreamReader; 
public class MainActivity extends AppCompatActivity { 
EditText data; 
Button save,read; 
TextView res; 
private String filename = "SampleFile.txt"; 
private String filepath = "MyFileStorage"; 
File myExternalFile; 
String myData = ""; 
@Override 
protected void onCreate(Bundle savedInstanceState) { 
super.onCreate(savedInstanceState); 
EdgeToEdge.enable(this); 
setContentView(R.layout.activity_main); 
ViewCompat.setOnApplyWindowInsetsListener(findViewById(R.id.main
 ), (v, insets) -> { 
Insets systemBars = 
insets.getInsets(WindowInsetsCompat.Type.systemBars()); 
v.setPadding(systemBars.left, systemBars.top, 
systemBars.right, systemBars.bottom); 
return insets; 
}); 
data = (EditText) findViewById(R.id.data); 
res = (TextView) findViewById(R.id.Responce); 
save = (Button) findViewById(R.id.write); 
save.setOnClickListener(new View.OnClickListener() { 
@Override 
public void onClick(View view) { 
try { 
FileOutputStream fos = new 
FileOutputStream(myExternalFile); 
fos.write(data.getText().toString().getBytes()); 
fos.close(); 
} catch (IOException e) { 
e.printStackTrace(); 
} 
data.setText(""); 
res.setText("SampleFile.txt saved to External 
Storage..."); 
} 
}); 
read = (Button) findViewById(R.id.read); 
read.setOnClickListener(new View.OnClickListener() { 
@Override 
public void onClick(View view) { 
try { 
FileInputStream fis = new 
FileInputStream(myExternalFile); 
DataInputStream in = new 
DataInputStream(fis); 
BufferedReader br = new BufferedReader(new 
InputStreamReader(in)); 
String strLine; 
while ((strLine = br.readLine()) != null) { 
myData = myData + strLine; 
} 
in.close(); 
} catch (IOException e) { 
e.printStackTrace(); 
} 
data.setText(myData); 
res.setText("SampleFile.txt data retrieved from 
Internal Storage..."); 
} 
}); 
if (!isExternalStorageAvailable() || 
isExternalStorageReadOnly()) { 
save.setEnabled(false); 
} 
else { 
myExternalFile = new 
File(getExternalFilesDir(filepath), filename); 
} 
} 
private static boolean isExternalStorageReadOnly() { 
String extStorageState = 
Environment.getExternalStorageState(); 
if 
(Environment.MEDIA_MOUNTED_READ_ONLY.equals(extStorageState)) { 
return true; 
} 
return false; 
} 
private static boolean isExternalStorageAvailable() { 
String extStorageState = 
Environment.getExternalStorageState(); 
if (Environment.MEDIA_MOUNTED.equals(extStorageState)) { 
return true; 
} 
return false; 
} 
} 
OUTPUT ON EMULATOR: 
b) To develop a simple Android application that writes data to Internal Storage. 
activity_main.xml 
<?xml version="1.0" encoding="utf-8"?> 
<androidx.constraintlayout.widget.ConstraintLayout 
xmlns:android="http://schemas.android.com/apk/res/android" 
xmlns:app="http://schemas.android.com/apk/res-auto" 
xmlns:tools="http://schemas.android.com/tools" 
android:id="@+id/main" 
android:layout_width="match_parent" 
android:layout_height="match_parent" 
tools:context=".MainActivity"> 
<TextView 
android:id="@+id/textView" 
android:layout_width="wrap_content" 
android:layout_height="wrap_content" 
android:layout_marginTop="43dp" 
android:layout_marginBottom="79dp" 
android:text="File Read / Write Demo" 
        android:textColor="#0895A8" 
        android:textSize="38sp" 
        android:textStyle="bold" 
        app:layout_constraintBottom_toTopOf="@+id/data" 
        app:layout_constraintEnd_toEndOf="parent" 
        app:layout_constraintHorizontal_bias="0.473" 
        app:layout_constraintStart_toStartOf="parent" 
        app:layout_constraintTop_toTopOf="parent" 
        app:layout_constraintVertical_bias="0.064" /> 
 
    <EditText 
        android:id="@+id/data" 
        android:layout_width="0dp" 
        android:layout_height="0dp" 
        android:layout_marginStart="55dp" 
        android:layout_marginEnd="55dp" 
        android:layout_marginBottom="36dp" 
        android:ems="10" 
        android:inputType="text" 
        android:textSize="24sp" 
        app:layout_constraintBottom_toTopOf="@+id/write" 
        app:layout_constraintEnd_toEndOf="parent" 
        app:layout_constraintStart_toStartOf="parent" 
        app:layout_constraintTop_toBottomOf="@+id/textView" /> 
 
    <Button 
        android:id="@+id/write" 
        android:layout_width="wrap_content" 
        android:layout_height="wrap_content" 
        android:layout_marginBottom="38dp" 
        android:text="Write Data" 
        android:textSize="30sp" 
        app:layout_constraintBottom_toTopOf="@+id/read" 
        app:layout_constraintEnd_toEndOf="parent" 
        app:layout_constraintStart_toStartOf="parent" 
        app:layout_constraintTop_toBottomOf="@+id/data" /> 
 
    <Button 
        android:id="@+id/read" 
        android:layout_width="wrap_content" 
        android:layout_height="wrap_content" 
        android:layout_marginBottom="259dp" 
        android:text="Read Data" 
        android:textSize="30sp" 
        app:layout_constraintBottom_toBottomOf="parent" 
        app:layout_constraintEnd_toEndOf="@+id/write" 
        app:layout_constraintTop_toBottomOf="@+id/write" /> 
 
</androidx.constraintlayout.widget.ConstraintLayout> 
MainActivity.java 
package com.example.filereadwrite; 
import android.os.Bundle; 
import android.view.View; 
import android.widget.Button; 
import android.widget.EditText; 
import android.widget.Toast; 
import java.io.BufferedReader; 
import java.io.FileInputStream; 
import java.io.FileNotFoundException; 
import java.io.FileOutputStream; 
import java.io.IOException; 
import java.io.InputStreamReader; 
import androidx.activity.EdgeToEdge; 
import androidx.appcompat.app.AppCompatActivity; 
import androidx.core.graphics.Insets; 
import androidx.core.view.ViewCompat; 
import androidx.core.view.WindowInsetsCompat; 
public class MainActivity extends AppCompatActivity { 
EditText data; 
Button read, write; 
private static final String FILE_NAME = "example.txt"; 
@Override 
protected void onCreate(Bundle savedInstanceState) { 
super.onCreate(savedInstanceState); 
EdgeToEdge.enable(this); 
setContentView(R.layout.activity_main); 
ViewCompat.setOnApplyWindowInsetsListener(findViewById(R.id.main
 ), (v, insets) -> { 
Insets systemBars = 
insets.getInsets(WindowInsetsCompat.Type.systemBars()); 
v.setPadding(systemBars.left, systemBars.top, 
systemBars.right, systemBars.bottom); 
return insets; 
}); 
data = (EditText) findViewById(R.id.data); 
read = (Button) findViewById(R.id.read); 
write = (Button) findViewById(R.id.write); 
read.setOnClickListener(new View.OnClickListener() { 
            @Override 
            public void onClick(View view) { 
                FileInputStream fis = null; 
                try { 
                    fis = openFileInput(FILE_NAME); 
                    InputStreamReader isr = new 
InputStreamReader(fis); 
                    BufferedReader br = new BufferedReader(isr); 
                    StringBuilder sb = new StringBuilder(); 
                    String text; 
                    while ((text = br.readLine()) != null) { 
                        sb.append(text).append("\n"); 
                    } 
                    data.setText(sb.toString()); 
                } catch (FileNotFoundException e) { 
                    e.printStackTrace(); 
                } catch (IOException e) { 
                    e.printStackTrace(); 
                } finally { 
                    if (fis != null) { 
                        try { 
                            fis.close(); 
                        } catch (IOException e) { 
                            e.printStackTrace(); 
                        } 
                    } 
                } 
            } 
        }); 
 
        write.setOnClickListener(new View.OnClickListener() { 
            @Override 
            public void onClick(View view) { 
                String text = data.getText().toString(); 
                FileOutputStream fos = null; 
                try { 
                    fos = openFileOutput(FILE_NAME, 
MODE_PRIVATE); 
                    fos.write(text.getBytes()); 
                    data.getText().clear(); 
                    
Toast.makeText(getApplicationContext(),"Saved to " + 
getFilesDir() + "/" + FILE_NAME, Toast.LENGTH_LONG).show(); 
                } catch (FileNotFoundException e) { 
                    e.printStackTrace(); 
                } catch (IOException e) { 
                    e.printStackTrace(); 
                } finally { 
                    if (fos != null) { 
                        try { 
                            fos.close(); 
                        } catch (IOException e) { 
                            e.printStackTrace(); 
                        } 
                    } 
                } 
            } 
        }); 
    } 
} 
 
OUTPUT ON EMULATOR: 
    
 
 
 
 
 
 
 
 
EXPERIMENT NO.: 25 
Aim:  To develop a simple Android application that creates Alarm Clock. 
12. Open android studio and select new android project by clicking Filemenu  New New 
Project. 
13. Choose the project as Empty Views Activity and click Next. 
14. Give project name (Start with a capital letter) as AlarmClock 
15. Choose the language as Java. 
16. Choose the required android version (Minimum SDK) and select finish. 
17. Go to package explorer in the left hand side and select the project. 
18. Under the project, Go to res folder and select layout. 
19. Double click the activity_main.xml file and design the layout for the page. 
20. Select MainActivity.java file and type the program. 
21.  Now go to activity_main.xml and right click & select run as option and select run 
configuration OR select the virtual device and click on run icon. 
22.  Android output will be displayed on the android emulator. 
Both activity_main.xml and MainActivity.java files together make our application work. The 
activity_main.xml is responsible for the layout (Front end User Interface) of the application. And 
the file MainActivity is responsible for the actions and the performance of the application (back 
end). 
Code: 
activity_main.xml 
<?xml version="1.0" encoding="utf-8"?> 
<androidx.constraintlayout.widget.ConstraintLayout 
xmlns:android="http://schemas.android.com/apk/res/android" 
xmlns:app="http://schemas.android.com/apk/res-auto" 
xmlns:tools="http://schemas.android.com/tools" 
android:id="@+id/main" 
android:layout_width="match_parent" 
android:layout_height="match_parent" 
tools:context=".MainActivity"> 
<LinearLayout 
android:layout_width="match_parent" 
android:layout_height="match_parent" 
android:orientation="vertical"> 
<!--Added Time picker just to pick the alarm time--> <!--gravity is aligned to center--> 
<TextView 
android:id="@+id/textView" 
android:layout_width="match_parent" 
android:layout_height="wrap_content" 
android:text="Alarm Clock" 
android:textAlignment="center" 
android:textSize="48sp" 
android:textStyle="bold" /> 
<TimePicker 
android:id="@+id/timePicker" 
android:layout_width="wrap_content" 
android:layout_height="wrap_content" 
android:layout_gravity="center" /> 
<!--Added Toggle Button to set the alarm on or off--> 
<!--ByDefault toggleButton is set to false--> 
<ToggleButton 
android:id="@+id/toggleButton" 
android:layout_width="wrap_content" 
android:layout_height="wrap_content" 
android:layout_gravity="center" 
android:layout_margin="20dp" 
android:checked="false" 
android:onClick="OnToggleClicked" /> 
<!--"OnToggleClicked" method will be implemented in 
MainActivity.java --> 
</LinearLayout> 
</androidx.constraintlayout.widget.ConstraintLayout> 
MainActivity.java 
package com.example.alarmclock; 
import android.app.AlarmManager; 
import android.app.PendingIntent; 
import android.content.Intent; 
import android.os.Bundle; 
import android.view.View; 
import android.widget.TimePicker; 
import android.widget.Toast; 
import android.widget.ToggleButton; 
import androidx.activity.EdgeToEdge; 
import androidx.appcompat.app.AppCompatActivity; 
import androidx.core.graphics.Insets; 
import androidx.core.view.ViewCompat; 
import androidx.core.view.WindowInsetsCompat; 
import java.util.Calendar; 
public class MainActivity extends AppCompatActivity { 
TimePicker alarmTimePicker; 
PendingIntent pendingIntent; 
AlarmManager alarmManager; 
@Override 
protected void onCreate(Bundle savedInstanceState) { 
super.onCreate(savedInstanceState); 
EdgeToEdge.enable(this); 
setContentView(R.layout.activity_main); 
ViewCompat.setOnApplyWindowInsetsListener(findViewById(R.id.main
 ), (v, insets) -> { 
Insets systemBars = 
insets.getInsets(WindowInsetsCompat.Type.systemBars()); 
v.setPadding(systemBars.left, systemBars.top, 
systemBars.right, systemBars.bottom); 
return insets; 
}); 
alarmTimePicker = (TimePicker) findViewById(R.id.timePicker); 
alarmManager = (AlarmManager) getSystemService(ALARM_SERVICE); 
} 
public void OnToggleClicked(View view) 
{ 
long time; 
if (((ToggleButton)view).isChecked()) 
{ 
Toast.makeText(MainActivity.this, "ALARM ON", 
Toast.LENGTH_SHORT).show(); 
Calendar calendar = Calendar.getInstance(); 
calendar.set(Calendar.HOUR_OF_DAY, 
alarmTimePicker.getCurrentHour()); 
calendar.set(Calendar.MINUTE, 
alarmTimePicker.getCurrentMinute()); 
Intent intent = new Intent(this, 
AlarmReceiver.class); 
//startActivity(intent); 
PendingIntent pendingIntent = 
PendingIntent.getBroadcast(this, 0, intent, 
PendingIntent.FLAG_IMMUTABLE); 
time = (calendar.getTimeInMillis() - 
(calendar.getTimeInMillis() % 60000)); 
if (System.currentTimeMillis() > time) 
{ 
if (Calendar.AM_PM == 0) 
time = time + (1000 * 60 * 60 * 12); 
else time = time + (1000 * 60 * 60 * 24); 
} 
alarmManager.setRepeating(AlarmManager.RTC_WAKEUP, time, 
10000, pendingIntent); 
//   alarmManager.set(AlarmManager.RTC_WAKEUP, 
System.currentTimeMillis() + (time * 1000), pendingIntent); 
} 
else { alarmManager.cancel(pendingIntent); 
Toast.makeText(MainActivity.this, "ALARM OFF", 
Toast.LENGTH_SHORT).show(); 
} 
} 
} 
AlarmReceiver.java 
package com.example.alarmclock; 
import android.content.BroadcastReceiver; 
import android.content.Context; 
import android.content.Intent; 
import android.media.Ringtone; 
import android.media.RingtoneManager; 
import android.net.Uri; 
import android.os.Build; 
import android.os.Vibrator; 
import android.widget.Toast; 
import androidx.annotation.RequiresApi; 
public class AlarmReceiver extends BroadcastReceiver 
{ 
// @RequiresApi(api = Build.VERSION_CODES.Q) 
@Override // implement onReceive() method 
public void onReceive(Context context, Intent intent) 
{ 
// we will use vibrator first 
Vibrator vibrator = (Vibrator) 
context.getSystemService(Context.VIBRATOR_SERVICE); 
vibrator.vibrate(4000); 
Toast.makeText(context, "Alarm! Wake up! Wake up!", 
Toast.LENGTH_LONG).show(); 
Uri alarmUri = 
RingtoneManager.getDefaultUri(RingtoneManager.TYPE_ALARM); 
if (alarmUri == null) 
{ 
alarmUri = 
RingtoneManager.getDefaultUri(RingtoneManager.TYPE_NOTIFICATION); 
} 
// setting default ringtone 
Ringtone ringtone = RingtoneManager.getRingtone(context, 
alarmUri); 
// play ringtone 
ringtone.play(); 
} 
} 
Androidmanifest.xml 
<?xml version="1.0" encoding="utf-8"?> 
<manifest 
xmlns:android="http://schemas.android.com/apk/res/android" 
xmlns:tools="http://schemas.android.com/tools"> 
<uses-permission android:name="android.permission.VIBRATE" 
/> 
<application 
android:allowBackup="true" 
android:dataExtractionRules="@xml/data_extraction_rules" 
android:fullBackupContent="@xml/backup_rules" 
android:icon="@mipmap/ic_launcher" 
android:label="@string/app_name" 
android:roundIcon="@mipmap/ic_launcher_round" 
android:supportsRtl="true" 
android:theme="@style/Theme.Alarmclock" 
tools:targetApi="31"> 
<receiver 
android:name=".AlarmReceiver" /> 
<activity 
android:name=".MainActivity" 
android:exported="true"> 
<intent-filter> 
<action 
android:name="android.intent.action.MAIN" /> 
<category 
android:name="android.intent.category.LAUNCHER" /> 
</intent-filter> 
</activity> 
</application> 
</manifest> 
OUTPUT ON EMULATOR: 
   
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
EXPERIMENT NO.: 26 
Aim:  To develop a simple Android application that makes use of RSS Feed. 
1. Open android studio and select new android project by clicking Filemenu  New New 
Project. 
2. Choose the project as Empty Views Activity and click Next. 
3. Give project name (Start with a capital letter) as AlarmClock 
4. Choose the language as Java. 
5. Choose the required android version (Minimum SDK) and select finish. 
6. Go to package explorer in the left hand side and select the project. 
7. Under the project, Go to res folder and select layout. 
8. Double click the activity_main.xml file and design the layout for the page. 
9. Select MainActivity.java file and type the program. 
10.  Now go to activity_main.xml and right click & select run as option and select run 
configuration OR select the virtual device and click on run icon. 
11.  Android output will be displayed on the android emulator. 
Both activity_main.xml and MainActivity.java files together make our application work. The 
activity_main.xml is responsible for the layout (Front end User Interface) of the application. And 
the file MainActivity is responsible for the actions and the performance of the application (back 
end). 
Code: 
activity_main.xml 
<?xml version="1.0" encoding="utf-8"?> 
<androidx.constraintlayout.widget.ConstraintLayout 
xmlns:android="http://schemas.android.com/apk/res/android" 
xmlns:app="http://schemas.android.com/apk/res-auto" 
xmlns:tools="http://schemas.android.com/tools" 
android:id="@+id/main" 
android:layout_width="match_parent" 
android:layout_height="wrap_content" 
tools:context=".MainActivity"> 
<LinearLayout 
android:layout_width="match_parent" 
android:layout_height="match_parent" 
android:orientation="vertical"> 
<TextView 
android:id="@+id/textView" 
android:layout_width="match_parent" 
android:layout_height="wrap_content" 
android:layout_marginBottom="50dp" 
android:text="RSS Feed" 
android:textAlignment="center" 
android:textColor="#E91E63" 
android:textSize="34sp" /> 
<ListView 
android:id="@+id/listView" 
android:layout_width="match_parent" 
android:layout_height="match_parent" /> 
</LinearLayout> 
</androidx.constraintlayout.widget.ConstraintLayout> 
MainActivity.java 
package com.example.rssfeed; 
import android.content.Intent; 
import android.net.Uri; 
import android.os.AsyncTask; 
import android.os.Bundle; 
import android.view.View; 
import android.widget.ArrayAdapter; 
import android.widget.ListView; 
import androidx.activity.EdgeToEdge; 
import androidx.appcompat.app.AppCompatActivity; 
import androidx.core.graphics.Insets; 
import androidx.core.view.ViewCompat; 
import androidx.core.view.WindowInsetsCompat; 
import org.xmlpull.v1.XmlPullParser; 
import org.xmlpull.v1.XmlPullParserException; 
import org.xmlpull.v1.XmlPullParserFactory; 
import java.io.IOException; 
import java.io.InputStream; 
import java.net.MalformedURLException; 
import java.net.URL; 
import java.util.ArrayList; 
import java.util.List; 
import android.app.ListActivity; 
public class MainActivity extends AppCompatActivity { 
List headlines; 
List links; 
@Override 
protected void onCreate(Bundle savedInstanceState) { 
super.onCreate(savedInstanceState); 
EdgeToEdge.enable(this); 
setContentView(R.layout.activity_main); 
ViewCompat.setOnApplyWindowInsetsListener(findViewById(R.id.main
 ), (v, insets) -> { 
Insets systemBars = 
insets.getInsets(WindowInsetsCompat.Type.systemBars()); 
v.setPadding(systemBars.left, systemBars.top, 
systemBars.right, systemBars.bottom); 
return insets; 
}); 
new MyAsyncTask().execute(); 
} 
class MyAsyncTask extends AsyncTask<Object,Void, 
ArrayAdapter> 
{ 
@Override 
protected ArrayAdapter doInBackground(Object[] params) 
{ 
headlines = new ArrayList(); 
links = new ArrayList(); 
try 
{ 
URL url = new URL("https://codingconnect.net/feed"); 
// URL url = new URL("https://xkcd.com/rss.xml"); 
XmlPullParserFactory factory = 
XmlPullParserFactory.newInstance(); 
factory.setNamespaceAware(false); 
XmlPullParser xpp = factory.newPullParser(); 
// We will get the XML from an input stream 
xpp.setInput(getInputStream(url), "UTF_8"); 
boolean insideItem = false; 
// Returns the type of current event: START_TAG, END_TAG, etc.. 
int eventType = xpp.getEventType(); 
while (eventType != XmlPullParser.END_DOCUMENT) 
{ 
if (eventType == XmlPullParser.START_TAG) 
{ 
if 
(xpp.getName().equalsIgnoreCase("item")) 
{ 
insideItem = true; 
} 
else if 
(xpp.getName().equalsIgnoreCase("title")) 
{ 
if (insideItem) 
headlines.add(xpp.nextText()); 
//extract the headline 
                        } 
                        else if 
(xpp.getName().equalsIgnoreCase("link")) 
                        { 
                            if (insideItem) 
                                links.add(xpp.nextText()); 
//extract the link of article 
                        } 
                    } 
                    else if(eventType==XmlPullParser.END_TAG && 
xpp.getName().equalsIgnoreCase("item")) 
                    { 
                        insideItem=false; 
                    } 
                    eventType = xpp.next(); //move to next 
element 
                } 
            } 
            catch (MalformedURLException e) 
            { 
                e.printStackTrace(); 
            } 
            catch (XmlPullParserException e) 
            { 
                e.printStackTrace(); 
            } 
            catch (IOException e) 
            { 
                e.printStackTrace(); 
            } 
            return null; 
        } 
        protected void onPostExecute(ArrayAdapter adapter) 
        { 
            adapter = new ArrayAdapter(MainActivity.this, 
android.R.layout.simple_list_item_1,headlines); 
            ListView lv = (ListView)findViewById(R.id.listView); 
            lv.setAdapter(adapter); 
        } 
    } 
 
    protected void onListItemClick(ListView l, View v, int 
position, long id) 
    { 
        Uri uri = Uri.parse((links.get(position)).toString()); 
        Intent intent = new Intent(Intent.ACTION_VIEW, uri); 
        startActivity(intent); 
    } 
public InputStream getInputStream(URL url) 
{ 
try 
{ 
return url.openConnection().getInputStream(); 
} 
catch (IOException e) 
{ 
return null; 
} 
} 
} 
Android Manifest file 
<uses-permission 
android:name="android.permission.INTERNET"></uses-permission> 
OUTPUT ON EMULATOR: 
