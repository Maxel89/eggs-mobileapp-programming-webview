
# Report WebView ##
## Rename your App. Hint: `res/values/strings.xml`

## Enable Internet access for your App. Hint: `AndroidManifest.xml`
Added the following line to the the AndroidManifest.xml 

    "<uses-permission android:name="android.permission.INTERNET" />"

## Create a WebView element in the layout file `content_main.xml` by replacing the existing `TextView`
Followed the instruction se code bellow.

    <WebView
        android:id="@+id/my_webview"

## Give the WebView an ID. Hint: `android:id="@+id/my_webview"`
Added the hinted code to content_main.xml se code above.

## Create a private member variable called `myWebView` of the type `WebView` and instantiate it in `onCreate()`. Hint: `findViewById()`
See code bellow.
    
    WebView myWebView;
    ...
    myWebView = findViewById(R.id.my_webview);

## Locate the WebView element created in step 1 using the WebView ID
See above.

## Enable Javascript execution in your WebViewClient. Hint: `getSettings()` and `setJavaScriptEnabled()`
Added the following line to onCreate. 

    myWebView.getSettings().setJavaScriptEnabled(true);

## Add a html page as an asset.
Created an asset directory and added ayy.html to it as well as the TheFonz.jpg, see code of ayy.html bellow.

    <h1>ayy&nbsp; html page</h1>
    <p><img src="TheFonz.jpg" alt="The Fonz (Fonzie) Ayyy / Eyyy ; Happy Days ~M:M~" /></p>

## Implement `showExternalWebPage()` and `showInternalWebPage()`. Hint: `loadUrl()`.
Implemented the to functions in MainActivity.java, see code bellow.

    public void showExternalWebPage(){
            myWebView.loadUrl("https://youtu.be/mghhLqu31cQ");
    }

    public void showInternalWebPage(){
            myWebView.loadUrl("file:///android_asset/ayy.html");
    }

## Call `showExternalWebPage()` and `showInternalWebPage()` when menu dropdown is clicked. Hint: `onOptionsItemSelected()`.
Updated onOptionsItemSelected() in MainActivity.java, see code bellow.
        if (id == R.id.action_external_web) {
            //Log.d("==>","Will display external web page");
            showExternalWebPage();
            return true;
        }
        if (id == R.id.action_internal_web) {
            //Log.d("==>","Will display internal web page");
            showInternalWebPage();
            return true;


## Internal webpage
![](printscreens/Screenshot from 2021-04-16 16-53-05.png)

## External webpage
![](printscreens/Screenshot from 2021-04-16 16-53-05.png)


