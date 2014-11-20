mySample1
=========

cocos2dx-2.x Android obb expansion sample v1.1

cocos2dx-2.x系にAndroid obb 拡張ファイルの使用サンプルプロジェクトになります。

cocos2dx-2.2.5のサンプルプロジェクトHelloCppを使用

▪️必要なライブラリー

android-sdk/sdk/extras/google/play_apk_expansion_zip_file

▪️修正したファイル  コメント：obb expansionで検索可

1:mySample1/obb-expansion-cocos2dx2.2.5/projects/HelloCpp/proj.android/src/org/cocos2dx/lib/Cocos2dxHelper.java

2:mySample1/obb-expansion-cocos2dx2.2.5/projects/HelloCpp/proj.android/src/org/cocos2dx/lib/Cocos2dxMusic.java

3:mySample1/obb-expansion-cocos2dx2.2.5/projects/HelloCpp/proj.android/src/org/cocos2dx/lib/Cocos2dxSound.java

▪️手順

1:mySample1/obb-expansion-cocos2dx2.2.5/projects/HelloCpp/assets/ 作成

2:mySample1/obb-expansion-cocos2dx2.2.5/projects/HelloCpp/Resources/* Resources下のフォルダおよびファイルを
上記1:assets下にコピー、そして、Resources下に空する

3:mac termianlで

a: $cd mySample1/obb-expansion-cocos2dx2.2.5/projects/HelloCpp/

b: $ zip -rn .ogg:.mp3:.wav assets.zip assets/

c: $ mv assets.zip main.2.org.cocos2dx.hellocpp.obb

d: $ mkdir org.cocos2dx.hellocpp

e: $ mv main.2.org.cocos2dx.hellocpp.obb org.cocos2dx.hellocpp/

4:上記3で作成したorg.cocos2dx.hellocppをAndroid デバイスにコピー
僕の場合、eclipse DDMS File ExplorerでAndroid AQUOS PHONE SHARP SHL21の/storage/sdcard0/Android/obb/に入れる
/storage/sdcard0/Android/obb/org.cocos2dx.hellocpp/main.2.org.cocos2dx.hellocpp.obbのようになります

5: AndroidManifest.xml修正

a: android:versionCode="2"にする

b: <uses-permission android:name="android.permission.READ_EXTERNAL_STORAGE"/>追加

7: デバイスに実行

注意：xcode ios実行したい場合はmySample1/obb-expansion-cocos2dx2.2.5/projects/HelloCpp/Resources/* Resources下のフォルダおよびファイルを元に戻す


