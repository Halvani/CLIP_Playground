# CLIP Playground
A collection of useful jupyter notebooks that show the potential of Open AI's powerful multimodal model CLIP

## CLIP-based image categorizer
Given a folder containing unordered images, the <a href="CLIP_based_image_categorizer.ipynb">CLIP-based image categorizer</a> jupyter notebook allows you to categorize all the images according to the labels you specify. For example, imagine you have a folder with a bunch of photos of :cat: and :frog:. You first specify the path to this folder, and define the labels by which you want to categorize the photos (in this case ```labels = ["cats", "frogs"]```. Depending on your hardware (gpu is recommended here) and the number of photos, the categorization process may take a while. The result looks similar to the following...

<center>
<div style="width:400px ; height:70%">
  <img src="assets/image_categorizer/cats_frogs_classifier.jpg" width=70% height=70% class="center">
<div>
<br><br>
</center>
    
Happy categorizing!
