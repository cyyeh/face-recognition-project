# Face Recognition Inspired by FaceNet

## Abstract

Many ideas of this project comes from [FaceNet](https://arxiv.org/pdf/1503.03832.pdf). FaceNet learns a neural network that encodes a face image into a vector of 128 numbers. By comparing two such vectors, you can then determine if two pictures are of the same person.

## Introduction

Face recognition problems commonly fall into two categories:
- Face Verification: It's a 1:1 matching problem, such as using iPhone to unlock using your face.
- Face Recognition: It's a 1:K matching problem. It's a harder problem, since it needs to scan more data in the database to determine the result. However, it's more convenient in some usecases.

In this project, we would implement both categories. We utilize a pretrained model and it encodes a face image to a vector of 128 numbers. Then, by comparing two such vectors with a predetermined threshold, we can decide whether two faces are the same. In order to train the model, we use the triplet loss function, which tries to make the distance between two images of the same face as near as possible, and make the distance between two images of different faces as far as possible.