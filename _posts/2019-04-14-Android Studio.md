---
defaults:
  # _posts
  - scope:
      path: ""
      type: posts
    values:
      layout: single
      author_profile: true
      read_time: true
      comments: true
      share: true
      related: true
title:  "Note for Android Studio 1"
---

## Creating your new project  ##

- Application Name: Capitalize first letter in each word + Space
- Package Name: all lower case
- Activity Name: Capitalize MainActivity (standard name)

## MainActivity ##
Focus on "Android" (what Android cares about)
1. Manifests (can specify which activity is the starter activity
2. java -> put java code here
3. res (layout/values)

i.e.
- MyFirstApp/app/src/main/res/layout/activity_main.xml
- MyFirstApp/app/java/com/kaopu/myfirstapp/MainActivity.java

## auto import ##

Files -> Settings -> Editor -> General -> auto import 

check "Optimize imports on the fly" and "Add unambiguous imports on the fly"

## Adding a breaking point ##

Run -> debug... 
Run -> Step Over/Step Into/Step Out
"Could not find gem 'tzinfo-data x64-mingw32' in any of the gem sources listed in your Gemfile. (Bundler::GemNotFound)" 

## java name ##
类型名  写全 + 首字母大写
变量名  缩写 + 首字母大写 -> 和resource ID保持一致
resource ID名 首字母小写，其他单词首字母大写

## setOnClickListner() ##
Button AddBtn = (Button) findViewById(R.id.AddBtn);
AddBtn.setOnClickListener(new View.onClickListener(){

  @override
  public void onclick(View v){
  
  EditText FirstNumPlainText = (EditText) findIdByView(R.id.firstNumPlainText);
  EditText SecNumPlainText = (EditText) findIdByView(R.id.secNumEditText);
  
  TextView ResultTextView = (TextView) findIdByView(R.id.resultTextView);
  
  int num1 = Integer.parseInt(FirstNumPlainText.getText().toString());
  int num2 = Integer.parseInt(SecNumEditText.getText().toString());
  
  int sum = num1 + num2;
  ResultTextView.setText(sum + "");
  })
};

## Core Elements ##

Activity - A rectangular area that displays something
Intent - An action being requested that the device should try to perform
IntentService - Services that can handle Intent requests and process the work to be done
BroadcaseReceivers - Receives an Intent from a sendBoardcast method often indicating that some work has been completed.


       

