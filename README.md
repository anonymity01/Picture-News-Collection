# Picture News Collection

Dataset for paper: Picture News Collection: A Dataset for Automatic Thumbnail Selection from Picture News ( Published at WISE2019 conference).

The Picture News Collection 0.1 version can be publicly available online at https://pan.baidu.com/s/1coR2p19l_xCpJTD7n5opIA .

The Picture News Collection contains more than 4 million images of 347,731 picture news from two famous news websites, Sina News and NetEase News.
Sina News part contains five hot news topics: fashion, history, Internet, sports and star.
NetEase News part contains five popular news topics: education, military, news, sports and star.
We reshaped each image in our Picture News Collection to a $224 \times 224$ pixels color image.

## Files in the Picture News Collection (2019/8/21)

* Picture News Collection
	* NetEase
		* education
			* annotation_Netease_education: json file, describing which subset each picture news belongs to ("subset"), images in each picture news ("context"), the thumbnail image of each picture news in the news website ("answer" or "label").

				example:
    				"Netease_education/2235205": {"subset": "training", "context": ["Netease_education/2235205/1.jpg", "Netease_education/2235205/2.jpg", "Netease_education/2235205/3.jpg", "Netease_education/2235205/4.jpg", "Netease_education/2235205/5.jpg", "Netease_education/2235205/6.jpg"], "answer": "Netease_education/2235205/1.jpg", "label": "1"}
    		* Other files: zip files. After decompression, each dir in NetEase_education/ is a piece of picture news, containing several images. 
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
