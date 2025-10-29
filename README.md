# Face to UPI Mapper  (Not a payment gateway)
- Redirecting UPI ID to some UPI Payment App (Gpay, phonepe, paytm etc)

## Registering Face

- Using 2 step process to register face

1. Face register - face_recognition
2.1. Liveness check(anti spoofing) - deepface-antispoofing
2.2. Challenge Response Layer
    - Randomized Challenges like "smile", "chin up", "look left" etc


## Storing UPI

- Two methods to store UPI
1. UPI ID       [using this for now]
2. QR - Code -> in turn returning a UPI ID

- storing UPI only on DB


## Retrieving UPI       -> Most Called

- Image Lookup for UPI ID


# Flow

## Auth Routes
- /sign-up
- /login

## User Routes
- /update-password
- /update-info

## UPI Routes
- /update-upi 
- /register-upi
- /get-upi              -> Video Streaming


## Schema Design

User
    uid
    name
    upi
    password    hashed + salted
    [faceid]

Face
    faceid
    uid

## FE Plan

a. Signup
b. Login
1. Screen 1 => Scan Face
2. Screen 2 => Record Face => Map face with UPI ID
3. Hamburger => Screen3 => Personal Info
4. 
