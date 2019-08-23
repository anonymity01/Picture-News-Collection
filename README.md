# Picture-News-Collection
## Dataset for paper: Picture News Collection: A Dataset for Automatic Thumbnail Selection from Picture News.\<br>
The Picture News Collection contains more than 4 million images of 347,731 picture news from two famous news websites, Sina News and NetEase News.\<br>

Sina News part contains five hot news topics: fashion, history, Internet, sports and star.\<br>
NetEase News part contains five popular news topics: education, military, news, sports and star.\<br>

Before building the Picture News Collection, we did several steps to pre-process the original picture news dataset crawled from the websites. For both the above two parts of the dataset, we discarded picture news with pixel damaged images, and we also removed a small part of the picture news whose thumbnail is different from any images in it.\<br>

In addition, most of the images in the original dataset have high pixels, which requires a lot of storage space. Besides, the size of the pixel matrix of raw images is usually different, making it difficult to directly use them as inputs of neural network methods. For these reasons, we reshaped each image in our Picture News Collection to a $224 \times 224$ pixels color image.\<br>

## Files (2019/8/21)

* Picture News Collection
	* NetEase
		* education
			* annotation_Netease_education: json file, describing which subset each picture news belongs to ("subset"), which images are in each picture news ("context"), which image is the thumbnail of each picture news in the news website ("answer" or "label").
				example:
    				"Netease_education/2235205": {"subset": "training", "context": ["Netease_education/2235205/1.jpg", "Netease_education/2235205/2.jpg", "Netease_education/2235205/3.jpg", "Netease_education/2235205/4.jpg", "Netease_education/2235205/5.jpg", "Netease_education/2235205/6.jpg"], "answer": "Netease_education/2235205/1.jpg", "label": "1"}
    		* other files: zip files. After decompression, each dir in NetEase_education/ is a piece of picture news, containing several images. 
    			* NetEase_education/label.txt : labels of each picture. Each line represtents a piece of picture news. 
    				A sample of each line: picture news ID \t label ID (begin with 1) \t picture news url --> 2235190 10  http://edu.163.com/photoview/3Q0N0029/2235190.html
		* military: files are similar to education dir.
		* news
		* sports
		* star
	* Sina
		* fashion
		* history
		* internet
		* sports
		* star
