# MultiSub
Javascript library for watching two subtitles at the same time in any HTML5 video. Ideally created for showing two subtitles, one
in a foreign language, and another in native language in case that you had understanding context problems.

You just need to add the "data-multisub" attribute to any html5 video with tracks:
```Html
<video width="500" height="400" data-multisub="pink,yellow" controls>
    <source src=http://techslides.com/demos/sample-videos/small.mp4 type=video/mp4>
    <track kind="subtitles" src="../sub.vtt">
    <track kind="subtitles" src="../sub2.vtt">
    <track kind="subtitles" src="../sub2.vtt"><!--This subtitle won't be load (max=2)-->
</video>
  ```
Just add the <b>name of the css class</b> separated by commas in the attribute for css customization:
```Html
<video width="500" height="400" data-multisub="yellow,green,red" controls>
  ```
The css class will be applied to the subtitles in order, first class (yellow in this example) will be applied to the first subtitle, second to second...
The multisub.css file can be edited, so anyone can create their custom css classes.<br>
Behavior:<br>
  -<b>Right clicking</b> make showing/hiding all tracks except first, so it's perfect for watching some video in a foreign language, and in case of understanding context problems right clicking to see the translation.<br>
  -The <b>maximum</b> of simultaneous subtitles is 2, more subtitles at the same time is possible, but not practical, so this is the config for now.<br>
  -If you <b>drag a .srt or .vtt</b> subtitle file into a video, it will be loaded automatically. If there were 2 subtitles before the load, the last will be substituted.<br>
  -Only works in chrome for now.
