## *creating and comparing result of dlib.simple_detector for multiple downsized_y, interpolation type, training_set_size*

**put your images (like http://www.ifp.illinois.edu/~vuongle2/helen/) to:**

> mkdir image_set

_now process  **image_set**, this will split them to train and test sets labeling training set with **dlib.frontal_face_detector** , labeling can be view  in **marked_image_view.xml**  images with 0 detected faces were removed, poor labelled image can be remove manually to improve training set_ 
> python3 ./train_test_models filter_set  


_train models due to (in train_test_models):_
>scaled_y_size = [100,200,300]  
>upsample_back_y_size = 400  
>interpols = [cv.INTER_NEAREST, cv.INTER_LANCZOS4, cv.INTER_AREA]  
>interpols_names = ["NEAREST", "LANCZOS4", "AREA"]  
>training_set_sizes = [50, 100, 150, 200]  #be carreful no to exceed training_images size  
>availabile_cores = 23  

_and save in **trained_models**_
> python3 ./train_test_models train_save  

  
_on **images_set/test_images** make detection with every trained model due to :
>test_img_size = 20  #be carreful not to exceed test_images size

and give result plots in pdf_

> python3 ./train_test_models result_pdf


