BaseNavigationDrawer
====================

![title image](https://googledrive.com/host/0BwESwPCuXtw7eExwSFVLQkR2TTg/20130811_172720.jpg)

## General idea
A small application with a Navigation Drawer. This is really basic. You can create new xml-layouts of the items you want to have in the Navigation Drawer and add them in the code. An example of this is my example application fo the android-square-progressbar library: https://github.com/mrwonderman/android-square-progressbar

### Layout of a new item
Simply create a new XML-Layout and add a code like that:
```xml
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    style="@android:style/Theme.Holo.Light"
    android:layout_width="match_parent"
    android:layout_height="48dp" >

    <View
        android:id="@+id/item_separator"
        style="@android:style/Theme.Holo.Light"
        android:layout_width="match_parent"
        android:layout_height="@dimen/lvDividerHeight"
        android:layout_alignParentBottom="true"
        android:background="@color/lvDividerColor" />

    <android.widget.CheckBox
        android:id="@+id/checkBox1"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_above="@+id/item_separator"
        android:layout_alignParentLeft="true"
        android:layout_alignParentRight="true"
        android:layout_alignParentTop="true"
        android:text="@string/opacity"
        android:textColor="#000000" />

</RelativeLayout>
```
### Add it to the Navigation Drawer

Add this to the Base Adapter in the MainActivity. There is a switch which is for all the items in the list. Don't forget to modify the getCount return value, otherwise this will not display all items.
```java
	View styleItem = LayoutInflater.from(getApplicationContext()).inflate(R.layout.lv_style, parent, false);
```
