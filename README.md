 Hey there 👋😄

- 🔭 I’m currently working on  building a Mobile Application 📱💻

- 📌DESCRIPTION OF AN APP 📂  :

The mobile app that is user friendly for learners when they have to choose a career path 👨‍🏫⚕️👮👨‍🔬👩‍🌾👩‍🎤👩‍🎨👩‍💻 ,
It will have a welcome page which will enable them to also enter their names
then a learner will be able to enter their academic details(subjects and results)
the application will be able to output which faculty is their strong point based on their results
it will then ask if the person would like to see the suggested courses on that faculty or not, 
if they choose no they will have exit 🔚 option and an option to go back 🔙 and
if they choose yes it will show suggested courses and universities for that course with links to apply.

- Am currently Learning with 👩‍💻📚 :
 
 https://www.appoftheyear.co.za/app-academy/ in collaboration with https://online.itvarsity.org/
 
 
 

Creating a Splash Screen

activity_splash_screen.xml
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
android:backgroundcolor="@colorblack"
    tools:context=".SplashScreen">

    <ImageView
        android:id="@+id/imageView"
        android:layout_width="300dp"
        android:layout_height="200dp"
        app:srcCompat="@drawable/logo"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintLeft_toLeftOf="parent"
        app:layout_constraintRight_toRightOf="parent"
        app:layout_constraintTop_toTopOf="parent"
         />
</androidx.constraintlayout.widget.ConstraintLayout>

SplashScreen.kt
package com.mpumelelo.thuto_pele

import androidx.appcompat.app.AppCompatActivity
import android.os.Bundle
import android.content.Intent
import android.os.Handler
import android.view.WindowManager

@Suppress("DEPRECATION")

class SplashScreen : AppCompatActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_splash_screen)
        window.setFlags(
            WindowManager.LayoutParams.FLAG_FULLSCREEN ,
            WindowManager.LayoutParams.FLAG_FULLSCREEN
        )
        Handler().postDelayed ({
            val intent = Intent (this , MainActivity::class.java)
            startActivity(intent)
            finish()
        }, 3000)
    }
}

AndroidManifest.xml

<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    package="com.mpumelelo.thuto_pele">

    <application
        android:allowBackup="true"
        android:icon="@mipmap/ic_launcher"
        android:label="@string/app_name"
        android:roundIcon="@mipmap/ic_launcher_round"
        android:supportsRtl="true"
        android:theme="@style/Theme.Thutopele">
        <activity android:name=".homeActivity"></activity>
        <activity android:name=".RegisterActivity" />
        <activity android:name=".MainActivity" />
        <activity
            android:name=".SplashScreen"
            android:theme="@style/Theme.AppCompat.Light.NoActionBar">
            <intent-filter>
                <action android:name="android.intent.action.MAIN" />

                <category android:name="android.intent.category.LAUNCHER" />
            </intent-filter>
        </activity>
    </application>

</manifest>

Navigation Drawer
navigation_menu.xml
<?xml version="1.0" encoding="utf-8"?>
<menu xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    tools:ignore="HardcodedText">
 
    <item
        android:id="@+id/nav_home"
        android:title="home" />
 
    <item
        android:id="@+id/nav_search"
        android:title="search" />
 
    <item
        android:id="@+id/nav_logout"
        android:title="Logout" />
 
</menu>
mainActivity.xml

<?xml version="1.0" encoding="utf-8"?>
 
<!--the root view must be the DrawerLayout-->
<androidx.drawerlayout.widget.DrawerLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/my_drawer_layout"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity"
    tools:ignore="HardcodedText">
 
    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="match_parent">
 
        <TextView
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_marginTop="128dp"
            android:gravity="center"
            android:text="thuto"
            android:textSize="18sp" />
 
    </LinearLayout>
 
    <!--this the navigation view which draws
        and shows the navigation drawer-->
    <!--include the menu created in the menu folder-->
    <com.google.android.material.navigation.NavigationView
        android:layout_width="wrap_content"
        android:layout_height="match_parent"
        android:layout_gravity="start"
        app:menu="@menu/navigation_menu" />
 
</androidx.drawerlayout.widget.DrawerLayout>


Creating a theme
res/values/attrs.xml
<?xml version="1.0" encoding="utf-8"?>
<resources>
    <attr name="pageBackground" format="reference"/>
    <attr name="textLarge" format="reference"/>
    <attr name="textAppearanceSubtitle1" format="reference"/>
    <attr name="textRegular" format="reference"/>
    <attr name="whiteBackground" format="reference"/>
    <attr name="Button" format="reference"/>
    <attr name="whiteSmoke" format="color"/>
</resources>


res/values/dimens.xml

<?xml version="1.0" encoding="utf-8"?>

 
 
 

- 📫 How to reach me:

Email📥: 
  lelongozo9224@gmail.com
-->
