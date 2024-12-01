# Natours-API
#### I created api with node.js,express.js, mongoDB. this api for booking tours by users and also can  implement more than 23 routes contains three collection tours , users , reviews  in this api you can do any thing for booking tour by any user.
# Overview:
## Natours
#### This api about natours contain three collection tours that you can book it , users collection who boot these tours and finally reviews which user can give it for each tour
## 1)tours
#### we can here get all tours , create tour , get one tour based on a specific id, update tour , delete tour , make some default quires , get the most month with tours , get all tour at specific geometry , calculate each distance for each tour from a specific point , get some statistics about tours
### a)special 
#### this folder for special request for tours
![GET](https://img.shields.io/badge/GET-blue)  defaultQueries.
##### `natours.io/api/v1/tours/default/querystring`
`in this request i made default queries i limited the docs to 5 in one page , and sort them by price , ratingsAverage and selected this fields name,price,rating,ratingsAverage,difficulty form each dpcument.`
 ##### ![Sort](https://img.shields.io/badge/Sort-price,_ratingsAverage-yellow) 
![GET](https://img.shields.io/badge/GET-blue) get all tours
##### `natours.io/api/v1/tours?price[lt]=1000&&ratingsAverage[gte]=4`
 ##### ![sort](https://img.shields.io/badge/Sort-price,_ratingsAverage-yellow) 
![POST](https://img.shields.io/badge/GET-blue) create tour
##### `natours.io/api/v1/tours`


```json
{
  "rating": 5,
  "ratingsAverage": 4.8,
  "ratingsQuantity": 6,
  "images": [
    "tour-2-1.jpg",
    "tour-2-2.jpg",
    "tour-2-3.jpg"
  ],
  "createdAT": "2024-08-30T23:40:09.517Z",
  "startDates": [
    "2021-06-19T09:00:00.000Z",
    "2021-07-20T09:00:00.000Z",
    "2021-08-18T09:00:00.000Z"
  ],
  "name": "test tour number four",
  "duration": 7,
  "maxGroupSize": 15,
  "difficulty": "easy",
  "price": 497,
  "summary": "Exploring the jaw-dropping US east coast by foot and by boat",
  "description": "anananann",
  "imageCover": "tour-2-cover.jpg",
  "startLocation": {
    "type": "Point",
    "description": "Miami, USA",
    "coordinates": [-80.185942, 25.774772],
    "address": "301 Biscayne Blvd, Miami, FL 33132, USA"
  },
  "locations": [
    {
      "type": "Point",
      "description": "Miami, Egypt",
      "coordinates": [-45.185942, 67.774772],
      "address": "301 Biscayne Blvd, Miami, FL 33132, USA",
      "day": 1
    },
    {
      "type": "Point",
      "description": "Miami, USA",
      "coordinates": [-43.185942, 56.774772],
      "address": "301 Biscayne Blvd, Miami, FL 33132, USA",
      "day": 2
    },
    {
      "type": "Point",
      "description": "Miami, Palestine",
      "coordinates": [-34.185942, 55.774772],
      "address": "301 Biscayne Blvd, Miami, FL 33132, USA",
      "day": 3
    }
  ]
}
```
`there are many routes about tours you can see them from the link at the bottom.`
## 2)users
#### this folder collection about all types of users that can register into database.
##### a) authentications
###### this folder for all authentications and all authorization (signup,login,forgetPassword.resetPassword,updatemyPassword)
![POST](https://img.shields.io/badge/GET-blue)  sign up
###### `natours.ioapi/v1/users/signup`
```
{
    "name":"guideTwo",
    "email":"guide2@gmail.com",
    "password":"test1234",
    "passwordConfirm":"test1234",
    "changePasswordAt":"2020-09-22",
    "role":"guide"
}
```
![POST](https://img.shields.io/badge/GET-blue)  login
###### `natours.ioapi/v1/users/login`
```
{
      "email":"sophie@example.com",
      "password":"test1234"
}
```
![POST](https://img.shields.io/badge/GET-blue) forgot password
###### `natours.ioapi/v1/users/forgotpassword`
```
{
    "email":"test@gmail.com"
}
```
![PATCH](https://img.shields.io/badge/GET-blue) reset Password
##### `natours.ioapi/v1/users/resetpassword/c8ae2d53d606f787899d2143f3542d2d7884414ae01e6bd22bd7fbf285d4d17d`
```
{
    "password":"anwaranwar",
    "passwordConfirm":"anwaranwar"
}
```
![PATCH](https://img.shields.io/badge/GET-blue) update my password
##### `natours.ioapi/v1/users/updateMyPassword`
```
{
    "currentPassword":"333444",
    "password":"123456",
    "passwordConfirm":"123456"
}
```
`there are many routes about users you can see them from the link at the bottom.`
## 3) reviews
##### this folder collection enable you to create review , get review based on its id , get all reviews , delete review and update review.
![POST](https://img.shields.io/badge/GET-blue) create review
##### `natours.ioapi/v1/reviews`
```
{
    "review":"great tour",
    "rating":3,
    "tour":"670708c6bf81d0516c9f95e7",
    "user":"6707094cbf81d0516c9f95ed"
}
```
![GET](https://img.shields.io/badge/GET-blue) get all reviews
##### `natours.ioapi/v1/reviews`
![DELETE](https://img.shields.io/badge/GET-blue) delete review
##### `natours.ioapi/v1/reviews/6707025fefb8656b90305e3e`
![PATCH](https://img.shields.io/badge/GET-blue)  update review
##### `natours.ioapi/v1/reviews/6707025fefb8656b90305e3e`
```
{
    "review":"bad!!!!!!!!"
}
```
![POST](https://img.shields.io/badge/GET-blue) create reviews on tour
##### `natours.ioapi/v1/tours/6712baa63ba2f28c94ce4305/reviews`
```
{
    "review":"baaaaad!!!!",
    "rating":1.5
}
```
<div align="center" style="background-color: yellow; padding: 10px; border-radius: 5px;">
  If you want to use this API for your own uses, it's okay, but do not use it for courses on YouTube and your tutorials.
</div>

### **links**
[go to Postman](https://documenter.getpostman.com/view/34856142/2sAXxWbA31)
