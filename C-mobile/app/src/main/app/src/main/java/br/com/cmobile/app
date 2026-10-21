package br.com.cmobile.app

import android.app.Activity
import android.os.Bundle
import android.webkit.WebChromeClient
import android.webkit.WebView
import android.webkit.WebViewClient
import android.view.ViewGroup
import android.graphics.Color

class MainActivity : Activity() {
private lateinit var webView: WebView

@Suppress("SetJavaScriptEnabled")  
override fun onCreate(savedInstanceState: Bundle?) {  
    super.onCreate(savedInstanceState)  
    window.statusBarColor = Color.rgb(33, 34, 44)  
    window.navigationBarColor = Color.rgb(33, 34, 44)  
    webView = WebView(this)  
    webView.layoutParams = ViewGroup.LayoutParams(  
        ViewGroup.LayoutParams.MATCH_PARENT,  
        ViewGroup.LayoutParams.MATCH_PARENT  
    )  
    webView.settings.javaScriptEnabled = true  
    webView.settings.domStorageEnabled = true  
    webView.settings.allowFileAccess = true  
    webView.webViewClient = WebViewClient()  
    webView.webChromeClient = WebChromeClient()  
    setContentView(webView)  
    webView.loadUrl("file:///android_asset/index.html")  
}  

@Deprecated("Deprecated in Android, but needed for compatibility")  
override fun onBackPressed() {  
    if (::webView.isInitialized && webView.canGoBack()) webView.goBack()  
    else super.onBackPressed()  
}

}
