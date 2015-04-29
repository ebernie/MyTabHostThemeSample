# MyTabHostThemeSample

Example project on how to style a TabHost. Workflow:
<ol>
<li>Generate XMLs and resources from an <a href="http://jgilfelt.github.io/android-actionbarstylegenerator">ActionBar style generator</a></li>
<li>Copy all drawables into the project res folder. DO NOT use the generated styles.xml</li>
<li>Refer to the offical guide on how to <a href="https://developer.android.com/training/basics/actionbar/styling.html">customize the actionbar background</a></li>
</ol>


res/values/styles_mytabhost.xml<br/>


<resources>

    <style name="MyTheme" parent="@style/Theme.AppCompat.Light.DarkActionBar">
        <!-- styles tab host indicator -->
        <item name="android:actionBarTabStyle">@style/ActionBarTabStyle.Mytabhost</item>
        <item name="actionBarTabStyle">@style/ActionBarTabStyle.Mytabhost</item>

        <!--styles actionbar -->
        <item name="android:actionBarStyle">@style/MyActionBar</item>
        <item name="actionBarStyle">@style/MyActionBar</item>
    </style>

    <style name="MyActionBar" parent="@style/Widget.AppCompat.Light.ActionBar.Solid.Inverse">
        <!-- action bar background -->
        <item name="background">@drawable/ab_solid_mytabhost</item>

        <!-- needed for 'stacked' & 'split' action bar (used by tabhost) -->
        <item name="backgroundStacked">@drawable/ab_stacked_solid_mytabhost</item>
        <item name="backgroundSplit">@drawable/ab_bottom_solid_mytabhost</item>
    </style>

    <style name="ActionBarTabStyle.Mytabhost" parent="@style/Widget.AppCompat.ActionBar.TabView">
        <item name="background">@drawable/tab_indicator_ab_mytabhost</item>
        <item name="android:background">@drawable/tab_indicator_ab_mytabhost</item>
    </style>

</resources>