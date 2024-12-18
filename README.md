:::::::::::::::::::::::::::::::::::::::::::::::discribe:::::::::::::::::::::::::::::::::::::::::::::::  ::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::

웹크롤링을 이용하여 원하는 이미지를 수집하고 전처리 후 CNN 모델을 구성하여 훈련과정의 전체. 

::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::  
기본라이브러리 : numpy, matplotlib.pyplot, tensoflow, random, os
::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::
1. 크롤링 작업    
 Crawling/Craw_image_running :: main run    
 Crawling/Craw_image_google :: import   
 Crawling/Craw_image_naver :: import       
    이미지 저장경로, 검색어, 영문검색어(공백없어야함)    
    ::: 실습환경 :::     
    크롬 드라이버 필요
    (https://googlechromelabs.github.io/chrome-for-testing/)  
    win64 v131.0.6788.108  
    크롬 웹브라우저 필요 
      버전 131.0.6778.140(공식 빌드) (64비트)   
    
2. 데이터 증강 및 배경 제거   
 Preprocessing/preprocessing_running :: main run  
 Preprocessing/remove_background :: import  
 Preprocessing/util :: import 
    이미지 배경 제거 및 회전, 밝기조정, 확대 기법으로 이미지 
    데이터 증강   
    ::: 실습환경 :::  
    tf.image.random_brightness  
    tf.keras.layers.RandomRotation  
    tf.keras.layers.RandomFlip  
    tf.keras.layers.RandomZoom  
    rembg.remove   

3. 데이터 전처리 및 훈련 실행, 평가   
 Trainning/train_fit :: main run  
 Trainning/construct_Model :: import   
    이미지 전처리 및 훈련실행과 훈련결과 평가 
    훈련 실행시 최적값으로 조기종료 콜백 등록됨   
    :: 실습환경 :::   
    Sequential,Input,Dense,Conv2D,Dropout,MaxPool2D,  
    Flatten, confusion_matrix,classfication_report,heatmap   
* error 처리는 수행하지 않음.   
copy right - 2024.12.18 광주컴퓨터기술학원 (dmsgur) 
