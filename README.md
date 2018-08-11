# KalmanFilter
卡爾曼濾波器

參考來源 https://github.com/yjsunwl/KalmanFilter#kalmanfilter

关于卡尔曼滤波器的原理，网上有很多，这里就不做过多介绍，此demo为一阶卡尔曼滤波器的实现。

主要为五个公式 （后面为一阶滤波器的系数）

X(k|k-1) = AX(k-1|k-1) + BU(k) + W(k), A=1,BU(k) = 0
P(k|k-1) = AP(k-1|k-1)A' + Q(k) ,A=1
Kg(k)=P(k|k-1)H'/[HP(k|k-1)H' + R],H=1
X(k|k) = X(k|k-1) + Kg(k)[Z(k) - HX(k|k-1)], H=1
P(k|k) = (1 - Kg(k)H)P(k|k-1), H=1
