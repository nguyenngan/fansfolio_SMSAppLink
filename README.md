# [fansfolio_SMSAppLink](https://myinnos.github.io/fansfolio_SMSAppLink/ "View Website - fansfolio_SMSAppLink")

[fans folio](https://ff.app.link/gt_get_app "fans folio Official Website") is a free app to maintain folio for your idols(film stars, cricket stars etc..,). It's the easiest way to connect and talk about your idol. You can share anything about your idol and make him/her famous around the world.

[![Get it on Google Play](https://raw.github.com/repat/README-template/master/googleplay.png)](https://ff.app.link/gt_get_app)

Kindly use the following links to use this library:

```java
allprojects {
  repositories {
			...
		maven { url "https://jitpack.io" }
	}
}
```
And then in the other gradle file(may be your app gradle or your own module library gradle, but never add in both of them to avoid conflict.)
```java
dependencies {
	compile 'com.github.myinnos:fansfolio_SMSAppLink:v1.0'
}
```
## Example

![fans folio Text SMS Link](https://s19.postimg.org/t8gshavj7/fansfolio_smsapp.png)

##### Create Android Project (set name fansfolio_SMSAppLink)

##### Add permissions to AndroidManifest.xml

```xml
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
```
##### Copy this code in to activity_main.xml

```xml
<?xml version="1.0" encoding="utf-8"?>
<ScrollView xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="fill_parent"
    android:layout_height="fill_parent"
    android:fitsSystemWindows="true">

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:orientation="vertical"
        android:paddingLeft="24dp"
        android:paddingRight="24dp"
        android:paddingTop="56dp">

        <TextView
            android:layout_width="fill_parent"
            android:layout_height="wrap_content"
            android:layout_marginBottom="24dp"
            android:gravity="center"
            android:text="SEND APP TO MOBILE"
            android:textColor="@android:color/black"
            android:textSize="20dip" />

        <ImageView
            android:layout_width="wrap_content"
            android:layout_height="72dp"
            android:layout_gravity="center_horizontal"
            android:layout_marginBottom="5dp"
            android:src="@drawable/fansfolio_logo" />

        <TextView
            android:layout_width="fill_parent"
            android:layout_height="wrap_content"
            android:layout_marginBottom="40dp"
            android:gravity="center"
            android:text="fans folio"
            android:textSize="18dip" />

        <TextView
            android:layout_width="fill_parent"
            android:layout_height="wrap_content"
            android:gravity="center"
            android:layout_marginBottom="5dp"
            android:text="add country code | ex: '+919123456789'"
            android:textSize="12dip" />

        <EditText
            android:id="@+id/etMobileNumber"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:hint="Mobile Number"
            android:inputType="phone" />

        <Button
            android:id="@+id/btSend"
            android:layout_width="fill_parent"
            android:layout_height="wrap_content"
            android:layout_marginBottom="24dp"
            android:layout_marginTop="24dp"
            android:padding="12dp"
            android:text="Text Me App"
            android:textAllCaps="true" />

        <TextView
            android:layout_width="fill_parent"
            android:layout_height="wrap_content"
            android:layout_marginBottom="24dp"
            android:gravity="center"
            android:text="You will recieve a one time SMS to download the app"
            android:textSize="16dip" />

    </LinearLayout>
</ScrollView>
```
##### Copy this code in to MainActivity.java

```java
public class MainActivity extends AppCompatActivity {

    private EditText etMobileNumber;
    private Button btSend;
    private String mobileNumber;

    @Override
    protected void onCreate(@Nullable Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        // initializing variables
        etMobileNumber = (EditText) findViewById(R.id.etMobileNumber);
        btSend = (Button) findViewById(R.id.btSend);

        // send button on click listener
        btSend.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {

                mobileNumber = etMobileNumber.getText().toString();
                //calling library funtion
                TextMefansfolioApp.make(MainActivity.this, mobileNumber, "one time SMS Sent! to "+ mobileNumber);
            }
        });
    }
}
```
## Apps using [fansfolio_SMSAppLink](https://myinnos.github.io/fansfolio_SMSAppLink/ "View Website - fansfolio_SMSAppLink")
If you are using fansfolio_SMSAppLink in your app and would like to be listed here, please let us know by opening a [new issue](https://github.com/myinnos/fansfolio_SMSAppLink/issues/new)!

 * [Pawan Kalyan : PSPK Fans Adda](https://play.google.com/store/apps/details?id=com.myinnos.pawankalyan "Pawan Kalyan : PSPK Fans Adda")

 * [Chiranjeevi : Fans Adda](https://play.google.com/store/apps/details?id=com.myinnos.chiru "Chiranjeevi : Fans Adda")
 
 * [Niharika Konidela](https://play.google.com/store/apps/details?id=com.fansfolio.niharika "Niharika Konidela")
 
 * [fans folio: Celebrity Lovers](https://play.google.com/store/apps/details?id=in.myinnos.fansfolio "fans folio: Celebrity Lovers")

## Contact
#### Prabhakar Thota
* :globe_with_meridians: Website: [myinnos.in](http://www.myinnos.in "Prabhakar Thota")
* :email: e-mail: contact@myinnos.in
* :mag_right: LinkedIn: [PrabhakarThota](https://www.linkedin.com/in/prabhakarthota "Prabhakar Thota on LinkedIn")
* :thumbsup: Twitter: [@myinnos](https://twitter.com/myinnos "Prabhakar Thota on twitter")

[![Flattr this git repo](http://api.flattr.com/button/flattr-badge-large.png)](https://flattr.com/submit/auto?user_id=username&url=https://github.com/myinnos/fansfolio_SMSAppLink&title=fansfolio_SMSAppLink&language=&tags=github&category=software) 

License
-------

    Copyright 2017 MyInnos

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
