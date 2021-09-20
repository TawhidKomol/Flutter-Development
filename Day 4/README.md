# Day 4

Day 4 practice

## Adding an image

First create a folder outside "lib" naming "assets"

For removing comment from pubspec.yaml press: control+/

Format of assets: 
  assets:
    - assets/nike.jpg

If everything ok without any error then press: control+s

Note: Must follow indentation

[Command to run in Chrome: flutter run -d Chrome]

After that, Go back to your "main.dart" and give some spaces following the indentations;
Then, take widget "body" and then take property "Image.asset" and provide the image path in double quatation;
body: Image.asset("assets/nike.jpg"),

## Image shaping
You can shape the image just apply it's width and height like below:
body: Image.asset(
        "assets/nike.jpg",
        width: 250,
        height: 250,
      ),

## Centering the image
Take Center widget 
[Shortcut: click on previous widget "Image" of body, then press the suggestion bulb at left; then take the wrap center; it will make Image child and will create Center widget inside body like below:

body: Center(
        child: Image.asset(
          "assets/nike.jpg",
          width: 250,
          height: 250,
        ),
    ),

##  Using image from net

Let's take a dummy image; In future we will take image from Rest.api

Take a link from flutter.dev website:
https://picsum.photos/250?image=9

code would be like this: 
body: Center(
          child: Image.network(
            "https://picsum.photos/250?image=9",
            width: 200,
            height: 200,
          ),
        ),

## Making circle avatar from Image

First click on previous "Image" and then press the suggestion bulb at left; then take the wrap with widget; 

then rename the widget CircleAvatar; it will make Center child and will create CircleAvatar inside body and then take "backgroundImage:"  & then "NetworkImage("https://picsum.photos/250?image=9")" and finally choose the suitable radius.. 

The code would look like below:

body: Center(
          child: CircleAvatar(
            radius: 80,
            backgroundImage: NetworkImage("https://picsum.photos/250?image=9"),
          ),
        ),

