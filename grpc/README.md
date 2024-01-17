# gRPC and Protocol Buffers

## Introduction

gRPC is  open source high performance **Remote Procedure Call** framework created from Google. It can connect services in and across data centers with pluggable support. gRPC can use **protocol buffers** as both its Interface Definition Language (**IDL**) and as its underlying message interchange format. 

![fig1](img/fig1.svg)


## Difference between REST API

They have different ways to develop APIs. For those who do not know about API, you can think API as menu in the restaurant. To communicate between cheif and customer, you will need menu. Menu will act as displaying chief choices, provide customers' choices. 

So without APIs, the applications or software services can not be communicated. gRPC and REST are two different types of API architectures. 

REST API, a client can send only one API request to server and receives single response. Until client receive message from server, client must wait. We call this as a unary data connection (1 to 1). Where using gRPC, a client can send one or multiple API requests and receives one or more response from the server. Therefore, the data connections can be unary, sever-streaming, client-streaming, or bidirectional streaming mode. This is because gRPC is based on *HTTP 2*.

REST is the most popular API architecutre for web services and microservice architecutres, where gRPC allows developers to create high-performance APIs for microservice architecutres. So it is suitable for internal systems like real-time streaming and large data loads are required. 

## Co