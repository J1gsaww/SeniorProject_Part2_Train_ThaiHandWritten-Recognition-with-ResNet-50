## Senior Project | Thai Hand Written Recognition using CNN (ResNet50)
This is just one part of my Senior Project, the preprocessing phase."

## ACKNOWLEDGEMENTS
The research team extends heartfelt thanks to everyone who supported us. 
<br> We are grateful to Assoc. Prof. Dr. Chomthip Pornpanomchai for invaluable guidance and advice, 
<br> as well as to all teachers, senior colleagues, and parents for their unwavering support

## Objectives
The goal of Thai handwritten recognition is to create technology that accurately converts handwritten Thai script into digital text. This involves using deep learning techniques like Convolutional Neural Networks (CNNs) to improve accuracy. By leveraging machine learning methods and large datasets of handwritten Thai characters, we aim to develop systems capable of recognizing diverse writing styles. Ultimately, our research aims to make Thai handwritten recognition a valuable tool for various industries and individuals in the digital age.

## Members
Mr. Thanawath 		Huayhongthong		6388016 
<br> `Resposible on GUI Displaying`
<br><br>
Mr. Dhammawat		Siribunchawan		6388055
<br> `Resposible on Trainning and Devleoping member process`
<br><br>
Mr. Naphat			Sookjitsumrarn		6388059
<br> `Resposible on Evaluating`

## System Structure Chart
<img src="/Snapshot/System Structure Chart.png" alt="SystemArc"> <br>

**Our project consist of 4 parts including:** <br>

- Preprocessing | You can explore our repository [here](https://github.com/J1gsaww/SeniorProject_Part1_Data-Preprocessing).<br>
- Training | Current repository <br>
- Evaluating | You can visit our repository  [here](https://github.com/J1gsaww/SeniorProject_SeniorProject-Part3-Evaluation.git). <br>
- Displaying | You can look out our repository [here](https://github.com/J1gsaww/SeniorProject_SeniorProject_Part4_GUI-Demo.git). <br>

## Training
This script is running on my colab notebook
<br>Original file is located at [this link](https://colab.research.google.com/drive/1VV5tb3bgXdo0JY_WBPFgWmOsKrp8EZuK).
<br>Ensure you have the necessary dependencies installed (NumPy, Matplotlib, Keras).
<br> This is a usage of transfer learning of Convolutional Neural Network with ResNet-50
<br> The essential poit is adjusting the Feature Extraction part that match the data and set trainable to false (However, the provide script is the experimental of both traiable true and false)
<br> Model Summary (Trainable False)
<br> Model: "sequential"
<br> _________________________________________________________________
<br> Layer (type)                Output Shape              Param #   
<br> =================================================================
<br>  resnet50 (Functional)       (None, 4, 4, 2048)        23587712  
<br> flatten (Flatten)           (None, 32768)             0                                                                      
<br> dense (Dense)               (None, 256)               8388864                                                                
<br> dropout (Dropout)           (None, 256)               0                                                                       
<br> dense_1 (Dense)             (None, 128)               32896                                                                 
<br> dropout_1 (Dropout)         (None, 128)               0                                                                      
<br> dense_2 (Dense)             (None, 57)                7353                                                                    
<br> =================================================================
<br> Total params: 32016825 (122.13 MB)
<br> Trainable params: 8429113 (32.15 MB)
<br> Non-trainable params: 23587712 (89.98 MB)
<br> _________________________________________________________________
<br>
<br>
The Average Early Stopping is around 30 - 40 Epochs

## Snapshot
**The highest accuracy we can reach is 96.7%**
`Data chosen`<br>
<img src="/Snapshot/Accuracy.png" alt="acc">
<br><br><br>
`Data with black space`<br>
<img src="/Snapshot/Loss.png" alt="loss">
