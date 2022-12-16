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

As impressive as the result of automatic categorization is, there are of course some **limitations** here: 

* The main limitation is that the underlying model reflects the quality of the categorization. Consequently, a weak model leads to unfavorable results. Currently, the image categorizer makes use of the <a href="https://huggingface.co/sentence-transformers/clip-ViT-L-14">ViT-L/14 model</a>, which according to my experiments has led to the most reliable results so far. You can find other models at the <a href="https://huggingface.co/openai">🤗 (Hugging Face) repo of Open AI</a>

* In addition, the image categorizer accepts only English texts as input, since the underlying ViT-L/14 model has been trained only on such texts. However, you can replace it with the <a href="https://huggingface.co/sentence-transformers/clip-ViT-B-32-multilingual-v1">multilingual clip-ViT-B-32 model</a>, but this comes at the expense of performance. 

* Another limitation concerns the way you define the labels. When these do not adequately represent the images you provide, the images can be categorized incorrectly. In other words, there is currently no support for a <a href="https://discuss.huggingface.co/t/how-to-create-other-garbage-class-for-classifier-e-g-covid-19-classifier/4249">garbage class</a>.

Happy categorizing!
