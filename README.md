<samp>
    
# [Real-time-Vehicle-Detection-Python](https://kalebujordan.dev/real-time-vehicle-detection-using-python/)

Hello everyone, This repository contains the source code of a script designed to detect cars in video or camera frames and draw rectangular boxes around them.

The **ML algorithms** used for detecting cars and bounding boxes coordinates is a pretrained cascade model [Haarcascade car](https://github.com/Kalebu/Real-time-Vehicle-Dection-Python/blob/master/haarcascade_car.xml).

[![Become a patron](pictures/become_a_patron_button.png)](https://www.patreon.com/kalebujordan)

## Where is the full article ?

The full article for this project is originally published on [my blog](kalebujordan.dev) with an article with title [Real-time vehicle detection in python](https://kalebujordan.dev/real-time-vehicle-detection-using-python/)

## Getting started

To begin, we need to clone the project repository or download the project's zip file and extract it.

```bash
git clone https://github.com/Kalebu/Real-time-Vehicle-Dection-Python
cd Real-time-Vehicle-Dection-Python
Real-time-Vehicle-Dection-Python ->
```

## Dependencies

Now that we have the project repository in our local directory, let's proceed to install the dependencies required to run our script.

```bash
pip install opencv-python
```

## Sample video

The sample video we used in this project is [**cars.mp4**](https://github.com/Kalebu/Real-time-Vehicle-Dection-Python/blob/master/cars.mp4) which will come as you download or clone the repository. If you want to use a different video with a different filename, you may need to make some changes to the source code accordingly.

```python
def Simulator():
    CarVideo = cv2.VideoCapture('cars.mp4') # change cars.mp4 to name of your vidoe
    while CarVideo.isOpened():
        ret, frame = CarVideo.read()
        controlkey = cv2.waitKey(1)
        if ret:        
            cars_frame = detect_cars(frame)
            cv2.imshow('frame', cars_frame)
        else:
            break
        if controlkey == ord('q'):
            break

    CarVideo.release()
    cv2.destroyAllWindows()

```

## **[<img src="./pictures/rocket.png" width="50" height="50"/>](./pictures/rocket.png) running our script**

Now you can launch your scripts;

```bash
python app.py 
```

If you use the provided sample video, the output of the script will resemble the image depicted below:;

<img src="sample.png" alt="drawing" width="400" height="200"/>

## Issues ?

If you encounter any issues while running the script, please feel free to raise an issue on the project repository. I will promptly address the problem and provide a solution as soon as possible. Your feedback is valuable, and I am committed to ensuring a smooth experience.

## Credits

1. All the credits to [kalebu](github.com/kalebu)
2. Others
