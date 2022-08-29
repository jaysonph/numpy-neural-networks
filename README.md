# numpy-neural-networks
This repository is my hobby project. It consists of low-level implementation of neural networks and some machine learning algorithms or techniques in numpy. The purpose of this project is for myself to consolidate my understanding of working principle of different machine learning things behind the scene.

# Network notation
<p align="center">
  <img src="https://user-images.githubusercontent.com/40629085/187185620-a75757b0-4824-4c9b-863e-d31ab53b688b.png" width="700" height="500"><br>
  <img src="https://latex.codecogs.com/svg.image?\large&space;z_{k}^{(L)}=\sum_{i}^{}w_{ki}^{(L)}a_{i}^{(L-1)}&plus;b^{(L)}&space;" /><br>
  <img src="https://latex.codecogs.com/svg.image?\large&space;a_{k}^{(L)}=h(z_{k}^{(L)})" /><br>
</p>

# Gradient Calculations
### Scalar form
<p align="center">
  <img src="https://latex.codecogs.com/svg.image?\large&space;\delta&space;&space;z_{k}^{(last)}=\frac{\partial&space;E}{\partial&space;z_{k}^{(last)}}" /><br>
  <img src="https://latex.codecogs.com/svg.image?\large&space;\delta&space;z_{k}^{(L)}=\frac{\partial&space;E}{\partial&space;z_{k}^{(L)}}=\delta&space;a_{k}^{(L)}\cdot&space;h^{(L)^{'}}(z_{k}^{(L)})" /><br>
  <img src="https://latex.codecogs.com/svg.image?\large&space;\delta&space;a_{k}^{(L)}=\frac{\partial&space;E}{\partial&space;a_{k}^{(L)}}=\sum_{i}^{}\delta&space;z_{i}^{(L&plus;1)}\cdot&space;w_{ik}^{(L&plus;1)}" /><br>
  <img src="https://latex.codecogs.com/svg.image?\large&space;\delta&space;&space;w_{kn}^{(L)}=\frac{\partial&space;E}{\partial&space;w_{kn}^{(L)}}=\delta&space;z_{k}^{(L)}\cdot&space;a_{n}^{(L-1)}" /><br>
  <img src="https://latex.codecogs.com/svg.image?\large&space;\delta&space;&space;b_{k}^{(L)}=\frac{\partial&space;E}{\partial&space;b_{k}^{(L)}}=\delta&space;z_{k}^{(L)}" /><br>
</p>

### Matrix form (single input)
<p align="center">
  <img src="https://latex.codecogs.com/svg.image?\large&space;\delta&space;z^{(last)}" />&nbsp;&nbsp;&nbsp;depends on loss function<br>
  <img src="https://latex.codecogs.com/svg.image?\large&space;\delta&space;z^{(L)}=\delta&space;a^{(L)}\odot&space;h^{(L)^{'}}(z_{k}^{(L)})" /><br>
  <img src="https://latex.codecogs.com/svg.image?\large&space;\delta&space;a^{(L)}=w^{(L&plus;1)^{T}}\delta&space;z^{(L&plus;1)}" /><br>
  <img src="https://latex.codecogs.com/svg.image?\large&space;\delta&space;w^{(L)}=\delta&space;z^{(L)}a^{(L-1)^{T}}" /><br>
  <img src="https://latex.codecogs.com/svg.image?\large&space;\delta&space;b^{(L)}=\delta&space;z^{(L)}" /><br>
</p>
