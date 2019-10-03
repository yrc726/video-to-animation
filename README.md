# video-to-animation


## related works
[ GAN ]
-  단순 image를 generation -> GAN에서도 style transfer를 시도
- cycle GAN, star GAN 등 다양한 모델이 제시 -> 대부분 image to image translation
- NVIDIA의 video-to-video synthesis -> paired dataset에 대해서만 학습이 가능하다는 한계
- GAN의 가장 치명적인 단점은 동일한 이미지를 input으로 주어도 styled 된 결과가 매번 달라진다는 것
- 각 frame마다 image-to-image translation을 거친 후 단순히 이어 붙이면 매우 부자연스러운 결과가 발생

[ style transfer ]
- GAN을 사용하지 않은 style transfer도대부분 video가 아닌 image 위주의 연구
- style을 적용하고자 하는 content image와 style image를 네트워크에 통과시킬 때 나온 각각의 feature map을 바탕으로 새롭게 합성될 영상의 feature map이 비슷하도록 최적화


[ linear style transfer ]
- NVIDIA
- 데이터 중심의 transformation matrix를 학습하는 universal style transfer
- content 연결성을 보존하는 효율적이고 유연한 style transfer model

## method
[ development environment ]
- pytorch
- os : window 10
- cpu : intel core i7-8700
- gpu : NVIDIA Geforce 1080ti
- dataset : COCO 2017 (118K) + Animation Style Image Dataset (100)
- training hours : 5 hours (10,00 iteration)
- inference time : 13.21 frame/s



