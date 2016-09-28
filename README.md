DragListView
=======  
A dragable ListView for Android, used for reorder your datas.   
<br>
![image](https://raw.githubusercontent.com/lungerWang/draglistview/master/DragListView.gif)  


Download
--------

Download via Gradle:
```groovy
compile 'com.lunger.draglistview:draglistview:2.2.0'
```
or Maven:
```xml
<dependency>
  <groupId>com.lunger.draglistview</groupId>
  <artifactId>draglistview</artifactId>
  <version>2.2.0</version>
  <type>pom</type>
</dependency>
```


Usage
--------
```groovy
mDragListView.setDragListAdapter(new MyAdapter(this, mDatas));
//设置点击item哪个部位可触发拖拽（可不设置，默认是item任意位置长按可拖拽）
mDragListView.setDragger(R.id.iv_move);
//设置item悬浮背景色
mDragListView.setItemFloatColor("#A35151");
//设置item悬浮透明度
mDragListView.setItemFloatAlpha(0.65f);
//设置拖拽响应回调
mDragListView.setMyDragListener(new DragListView.MyDragListener() {
    @Override
    public void onDragFinish(int srcPositon, int finalPosition) {
          Toast.makeText(MainActivity.this, "beginPosition : " + srcPositon + "...endPosition : " + finalPosition, Toast.LENGTH_LONG).show();
    }
});
```
ProGuard
--------

If you are using ProGuard you might need to add the following option:
```
-dontwarn com.lunger.draglistview.**
```



License
--------

    Copyright 2013 Square, Inc.

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.


 [1]: http://square.github.io/picasso/
 [2]: https://search.maven.org/remote_content?g=com.squareup.picasso&a=picasso&v=LATEST
 [snap]: https://oss.sonatype.org/content/repositories/snapshots/