# Shape Image View
Provides a set of custom shaped imageview components, and a framework to define more shapes. Implements both *shader* based and *bitmap mask* based image views. Shader based ones uses *canvas draw methods* and *Path* construct, while bitmap mask uses xfremode to draw image on bitmaps defined by android shape XML's or resource bitmaps.

<div>
<a href="images/shader-buble.png" style="float:left;">
<img src="images/shader-buble.png" alt="Chat Bubble Image" height="600px"/>
</a>
<a href="images/all-samples.png" >
<img src="images/all-samples.png" alt="Shape Image View" height="600px"/>
</a>
</div>

There are many projects online implementing such components, however one goal of this project is to provide a performant/smooth scrolling view component framework to define different shapes for bitmap. 

**For use with recycling view such as ListView or GridView please use shader based implementations.**

## Usage 
####BubbleImageView
![Android Bubble ImageView](images/small-bubble.png)
```XML
<com.github.siyamed.shapeimageview.BubbleImageView
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:src="@drawable/neo"
    app:arrowPosition="right"
    app:square="true"/>
```

####RoundedImageView
![Android Rounded Rectangle ImageView](images/small-rounded.png)
```XML
<com.github.siyamed.shapeimageview.RoundedImageView
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:src="@drawable/neo"
    app:radius="6dp"
    app:borderWidth="6dp"
    app:borderColor="@color/darkgray"
    app:square="true"/>
```

####CircularImageView
![Android Circular ImageView](images/small-circle.png)
```XML
<com.github.siyamed.shapeimageview.CircularImageView
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:src="@drawable/neo"
    app:borderWidth="6dp"
    app:borderColor="@color/darkgray"/>
```
####PorterShapeImageView
* With mask bitmap

![Android Star Shape ImageView ](images/small-mask-star.png)
```XML
<com.github.siyamed.shapeimageview.shape.PorterShapeImageView
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    app:shape="@drawable/star"
    android:src="@drawable/neo"
    app:square="true"/>
```

* With shape XML

![Android Star Shape ImageView ](images/small-xmlshape-rounded.png)

```XML
<com.github.siyamed.shapeimageview.shape.PorterShapeImageView
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    app:shape="@drawable/shape_rounded_rectangle"
    android:src="@drawable/neo"
    app:square="true"/>
```

rounded rectangle shape definition in XML: 

```XML
<shape android:shape="rectangle" xmlns:android="http://schemas.android.com/apk/res/android">
    <corners
        android:topLeftRadius="18dp"
        android:topRightRadius="18dp"
        android:bottomLeftRadius="18dp"
        android:bottomRightRadius="18dp" />
    <solid android:color="@color/black" />
</shape>
```

## References
* [MostafaGazar/CustomShapeImageView](https://github.com/MostafaGazar/CustomShapeImageView) 