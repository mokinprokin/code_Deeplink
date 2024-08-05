# code_Deeplink
Код:
 Android Manifest:
         <meta-data android:name="flutter-deeplink" android:value="true"/>
            <intent-filter>
                <action android:name="android.intent.action.VIEW" />
                <category android:name="android.intent.category.DEFAULT" />
                <category android:name="android.intent.category.BROWSABLE" />

                <data
                    android:scheme="https"
                    android:host="YourHost"
                 />

            </intent-filter>
            <intent-filter android:autoVerify="true">
                <action android:name="android.intent.action.VIEW" />
                <category android:name="android.intent.category.DEFAULT" />
                <category android:name="android.intent.category.BROWSABLE" />

                <data
                    android:scheme="https"
                    android:host="YourHost"
                 />

            </intent-filter>
  Info.plist:
          <key>CFBundleURLTypes</key>
   <array>
	<dict>
       	   <key>CFBundleURLSchemes</key>
	   <array>
	   <string>https</string>
   </array>
</dict>
</array>
<key>com.apple.developer.associated-domains</key>
<array>
	<string>applinks:yourdomain.com</string>
</array>
     
   assetlinks.json:
           [{
    "relation": ["delegate_permission/common.handle_all_urls"],
    "target" : { "namespace": "android_app", "package_name":"com.example.crypto_list",
 "sha256_cert_fingerprints": ["yourSha256"] }
}]

