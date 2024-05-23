# Gender_Classification_Task_3

Link to Google Drive : https://drive.google.com/drive/folders/1UbfelXXSTd9ikeNDut49V7nfPONpTUc5?usp=drive_link

### I could not upload files due to upload limit. Link to google drive for code and model : https://drive.google.com/drive/folders/1ZUqndWb1evjDuYN4jZgAoptWG1vdojQp?usp=drive_link


<br>FIRST<br> I found a data set on kaggle with $ \approx $ $23000$ labelled images.
<br> For example : </br>
[090544-jpg.jpg](https://postimg.cc/cgyzLPpM)
<br> The mask roughly covers half of the image and I t was the case for all other images too. So I thought of cropping the image in half and training the whole dataset.<br>
Now for the validation part I needed masked faces, so I needed to make datasets which was hectic. So, I dropped this dataset.
But I think this will work if we provided masked faces provided mask covers half of the image from bottom.
<br><br>SECOND<br>
I downloaded a dataset from kaggle having $ \approx $ $2000$ images. But those were unlabelled. So, I manually labelled thoose images into male and female folders named $1$ and $0$ respectively. I trained VGG16 $+$ added other layers to increase accuracy of the model. The model took about $72min$ to train.<br>
<br><br>APPROACH TO THE PROBLEM</br>

1. I had unlabelled data-set so I needed to separate them into two folders. For that I took help from ChatGPT because I could not figure out myself. I got a code using which I got prompt for each image and separated them manually. The two folders are in folder named "dataset".
2. Used image_height = image_width = 200
3. Used VGG16 as base model(freezed) and added MaxPool then a 128 sized Dense layer with softmax activation. Then unfreezed the base model and fine-tuned the model</br>

<br><br>ROAD-BLOCKS FACED</br>
1. <u>Un-labelled dataset</u> : Labelled them manually using help from the Net.
2. <u>Got very less number of models</u> : Used Data augmentation.
3. <u>Images were not of same size</u> : Data processing ro resize them to $200$ x $200$ pixels.


<br><br>HOW TO RUN THE CODE</br>
1. Download the files in repository.
2. There is a jupyter notebook named $ Use\_trained\_model.ipynb $.
3. The model is already trained, you may train a new model or use pre-trained one.
4. To use pre-trained model just replace $ base\_path $ with the path of the <u><b>folder</b></u> where testing images are stored.
5. Testing images along with predictions will be displayed.

