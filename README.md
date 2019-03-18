# MyApplication
**

## 实验一 Android开发基础

截图如下：

![在这里插入图片描述](https://img-blog.csdnimg.cn/20190318192735917.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2tpbmdhZXRoZWxiYWxk,size_16,color_FFFFFF,t_70)
验证生命周期的源代码如下：
package com.example.a26081.myapplication;

import android.support.v7.app.AppCompatActivity;
import android.os.Bundle;
import android.util.Log;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        Log.i("MainActivityLife","调用onStartonCreate");

    }
    @Override
    protected void onStart(){
        super.onStart();
        Log.i("MainActivityLife","调用onStart");
    }
    @Override
    protected void onResume(){
        super.onResume();
        Log.i("MainActivityLife","调用onResume");
    }
    @Override
    protected void onPause(){
        super.onPause();
        Log.i("MainActivityLife","调用onPause");
    }
    @Override
    protected void onStop(){
        super.onStop();
        Log.i("MainActivityLife","调用onStop");
    }
    @Override
    protected void onDestroy(){
        super.onDestroy();
        Log.i("MainActivityLife","调用onDestroy");
    }
    @Override
    protected void onRestart(){
        super.onRestart();
        Log.i("MainActivityLife","调用onRestart");
    }

}
hello world 源代码：
<?xml version="1.0" encoding="utf-8"?>
<android.support.constraint.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Hello World!"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintLeft_toLeftOf="parent"
        app:layout_constraintRight_toRightOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

</android.support.constraint.ConstraintLayout>

## 实验二  Android布局
线性布局截图如下：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190318193550584.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2tpbmdhZXRoZWxiYWxk,size_16,color_FFFFFF,t_70)

利用ConstraintLayout实现截图如下：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190318193746414.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2tpbmdhZXRoZWxiYWxk,size_16,color_FFFFFF,t_70)

表格布局截图如下：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190318193908341.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2tpbmdhZXRoZWxiYWxk,size_16,color_FFFFFF,t_70)
线性布局源代码如下：


<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:orientation="vertical"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="#000000">
    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:orientation="horizontal">

        <Button
            android:layout_width="0dp"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            android:text="one,one"
            android:textColor="#ffffff" />
        <Button
            android:layout_width="0dp"
            android:layout_height="wrap_content"
            android:layout_weight="1.1"
            android:textColor="#ffffff"
            android:text="one,two" />
        <Button
            android:layout_width="0dp"
            android:layout_weight="1.2"
            android:layout_height="wrap_content"
            android:textColor="#ffffff"
           android:text="one,three" />
        <Button
            android:layout_width="0dp"
            android:layout_weight="1.2"
            android:layout_height="wrap_content"
            android:textColor="#ffffff"
            android:text="one,four" />
    </LinearLayout>
    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:orientation="horizontal">
        <Button
            android:layout_width="0dp"
            android:layout_height="wrap_content"
            android:layout_weight="1.03"
            android:textColor="#ffffff"
            android:text="two,one" />
        <Button
            android:layout_width="0dp"
            android:layout_height="wrap_content"
            android:layout_weight="1.1"
            android:textColor="#ffffff"
            android:text="two,two" />
        <Button
            android:layout_width="0dp"
            android:layout_height="wrap_content"
            android:textColor="#ffffff"
            android:layout_weight="1.2"
            android:text="two,three" />
        <Button
            android:layout_width="0dp"
            android:layout_height="wrap_content"
            android:textColor="#ffffff"
            android:layout_weight="1.2"
            android:text="two,four" />
    </LinearLayout>
    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:orientation="horizontal">
        <Button
            android:layout_width="0dp"
            android:layout_height="wrap_content"
            android:layout_weight="1.1"
            android:textColor="#ffffff"
            android:text="three,one" />
        <Button
            android:layout_width="0dp"
            android:layout_height="wrap_content"
            android:layout_weight="1.15"
            android:textColor="#ffffff"
            android:text="three,two" />
        <Button
            android:layout_width="0dp"
            android:layout_height="wrap_content"
            android:textColor="#ffffff"
            android:layout_weight="1.25"
            android:text="three,three" />
        <Button
            android:layout_width="0dp"
            android:layout_height="wrap_content"
            android:textColor="#ffffff"
            android:layout_weight="1.2"
            android:text="three,four" />
    </LinearLayout>
    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:orientation="horizontal">
        <Button
            android:layout_width="0dp"
            android:layout_height="wrap_content"
            android:layout_weight="0.999"
            android:textColor="#ffffff"
            android:text="four,one" />
        <Button
            android:layout_width="0dp"
            android:layout_height="wrap_content"
            android:layout_weight="1.035"
            android:textColor="#ffffff"
            android:text="four,two" />
        <Button
            android:layout_width="0dp"
            android:layout_height="wrap_content"
            android:textColor="#ffffff"
            android:layout_weight="1.171"
           android:text="four,three" />
        <Button
            android:layout_width="0dp"
            android:layout_height="wrap_content"
            android:textColor="#ffffff"
            android:layout_weight="1.06"
            android:text="four,four" />
    </LinearLayout>

</LinearLayout>

利用ConstraintLayout源代码如下：

<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:minHeight="0dp"
    android:background="#000000"
    android:orientation="horizontal">

    <Button
        android:id="@+id/b1"
        android:layout_width="80dp"
        android:layout_height="wrap_content"
        android:background="#ff0000"
        android:textColor="#000000"
        android:text="Red" />

    <Button
        android:id="@+id/b2"
        android:layout_width="80dp"
        android:layout_height="wrap_content"
        android:layout_marginLeft="150dp"
        android:background="#ff8247"
        android:textColor="#000000"
        android:text="orange" />

    <Button
        android:id="@+id/b3"
        android:layout_width="80dp"
        android:layout_height="wrap_content"
        android:layout_marginLeft="300dp"
        android:background="#fff000"
        android:textColor="#000000"
        android:text="yellow" />

    <Button
        android:id="@+id/b4"
        android:layout_width="80dp"
        android:layout_height="wrap_content"
        android:layout_marginLeft="60dp"
        android:layout_marginTop="100dp"
        android:background="#43ee3a"
        android:textColor="#000000"
        android:text="green" />

    <Button
        android:id="@+id/b5"
        android:layout_width="80dp"
        android:layout_height="wrap_content"
        android:layout_marginLeft="150dp"
        android:layout_marginTop="100dp"
        android:background="#6495ED"
        android:textColor="#000000"
        android:text="blue" />

    <Button
        android:id="@+id/b6"
        android:layout_width="80dp"
        android:layout_height="wrap_content"
        android:layout_marginLeft="240dp"
        android:layout_marginTop="100dp"
        android:background="#4b0082"
        android:textColor="#000000"
        android:text="indigo" />

    <Button
        android:id="@+id/b7"
        android:layout_width="match_parent"
        android:layout_height="80dp"
        android:layout_marginTop="200dp"
        android:background="#BA55D3"
        android:textColor="#000000"
        android:text="violef" />
</RelativeLayout>

表格布局源代码如下：

<?xml version="1.0" encoding="utf-8"?>
<TableLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:stretchColumns="1"
    android:background="#000000">

    <TableRow>
        <TextView
            android:layout_column="1"
            android:text="Open..."
            android:padding="3dip"
            android:textColor="#ffffff"/>
        <TextView
            android:text="Ctrl-O"
            android:gravity="right"
            android:padding="3dip"
            android:textColor="#ffffff"/>

    </TableRow>

    <TableRow>
        <TextView
            android:layout_column="1"
            android:text="Save..."
            android:padding="3dip"
            android:textColor="#ffffff"/>
        <TextView
            android:text="Ctrl-S"
            android:gravity="right"
            android:padding="3dip"
            android:textColor="#ffffff"/>
    </TableRow>

    <TableRow>
        <TextView
            android:layout_column="1"
            android:text="Save As..."
            android:padding="3dip"
            android:textColor="#ffffff"/>
        <TextView
            android:text="Ctrl-Shift-S"
            android:gravity="right"
            android:padding="3dip"
            android:textColor="#ffffff"/>
    </TableRow>

    <View
        android:layout_height="2dip"
        android:background="#ffffff"/>
    <TableRow>
        <TextView
            android:text="X"
            android:textColor="#ffffff"
            android:padding="3dip"/>
        <TextView
            android:text="Import..."
            android:textColor="#ffffff"
            android:padding="3dip"/>
    </TableRow>
    <TableRow>
        <TextView
            android:text="X"
            android:textColor="#ffffff"
            android:padding="3dip"/>
        <TextView
            android:text="Emport..."
            android:textColor="#ffffff"
            android:padding="3dip"/>
        <TextView
            android:text="Ctrl-E"
            android:gravity="right"
            android:textColor="#ffffff"
            android:padding="3dip"/>
    </TableRow>
    <View
        android:layout_height="2dip"

        android:background="#ffffff"/>
    <TableRow>
        <TextView
            android:layout_column="1"
            android:textColor="#ffffff"
            android:text="Quit"
            android:padding="3dip"/>
    </TableRow>
</TableLayout>

