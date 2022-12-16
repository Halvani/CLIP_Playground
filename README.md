# CLIP Playground
A collection of useful jupyter notebooks that show the potential of Open AI's powerful multimodal model CLIP

## CLIP-based image categorizer
Given a folder containing unordered images, the <a href="CLIP_based_image_categorizer.ipynb">CLIP-based image categorizer</a> jupyter notebook allows you to categorize all the images according to the labels you specify. For example, imagine you have a folder with a bunch of photos of :cat: and :frog:. You first specify the path to this folder, and define the labels by which you want to categorize the photos (in this case ```labels = ["cat", "frog"]```. Depending on your hardware (gpu is recommended here) and the number of photos, the categorization process may take a while. The result looks similar to the following...

<center>
<div style="width:400px ; height:70%">
  <img src="assets/image_categorizer/cats_frogs_classifier.jpg" width=70% height=70% class="center">
<div>
<br>
</center>

As impressive as the result of automatic categorization is, there are of course some limitations here. If you define labels that do not adequately represent the images you provide, the images will inevitably be categorized incorrectly. In other words, there is no support for a *garbage class* at the moment. In addition, the image categorizer accepts only English texts as input, since the underlying model has been trained only on such texts. Another limitation is that the underlying model reflects the quality of the categorization. A weak model therefore leads to unfavorable results. Currently, the <a href="https://huggingface.co/sentence-transformers/clip-ViT-L-14">ViT-L/14</a> model is used, which according to my experiments has led to the most reliable results so far. If you want to try out other models have a look at the 
<a href="https://huggingface.co/openai">🤗 (Hugging Face) repo of Open AI</a>

Happy categorizing!
