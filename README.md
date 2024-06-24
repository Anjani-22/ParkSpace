# ParkSpace

mobile web application for booking parking space using MERN, the UI will basically have sidebar with all options and profile icon on top right corer.
Option for custom styling using module.scss and common scss file with daisyUI.
Use formik for forms with otion for custom stylng, and vite for front end.

Parkowner register option-The park owner should be able to register his paking space with locatio, address, name , no of rows and colunmn or no of spots in each row with each spot getting auto populated with 1-1, 1-2, 1-3...etcwhere numerical no being row no and algabets beeing spots aur there own naming convention for row and columns.

upload pictures of parking space and submit, after submitting he will be asked to a form will open which will ask to upload live picture of parking spot or its recording, which will also capture its location and after video or picture is captured the form is submitted. the owner can add more picture by click add more in form.

park owner upcoming tickets- can see tickets which are coming
payment- can apply filter and check which tickets are paid or not, if tickets are not paid, then each ticket will have button to "mark as paid", in case payment is done in cash or personal UPI.

parkowner create role- park owner can create role such security, which will have access to scan ticket and permit entry and exit of vehicle, also can can see unpaid tickets and will mark the ticket as paid in case payment made in cash or UPI,

Edit parking space, price set for each spot

User flow- user can signup and book park space after serching for nearby parking space, with map, and booking details like arival time, departure time, vehicle no, price username. After booking and chooing any payment mode, the ticket will be gernated with all booking info, along with like payment status as paid or pending and each ticket will have QR code, which will be scanned at the time of parking by security guard and exit scan.
As long car is parked or park spcae is booked, the status can be seen by park owner in its homepage UI, with the car no, like available, booked, parked.

the total price is calculated based on exit time-entry time, if arrival time- entry time>10, then price calcualted is (exittime-arrivaltime-10)pricepermin, else (exit time-entry time)10,

at time of exit scan the ticket price is calculated, if there is extra time availed, then payment status will change to pending and ticket will have option button exmple "pay pending amount 30rupes", which will update the paid so far amount, same can be manually updated by, clicking on mark as paid in cash button on tikcet which appears on the UI for security guard.

after payment the modal appears to write feedback with star rating, connected with ticket.

have the option to download ticket, and show dirsction in map to navigate to parking space.

after scanning let the success or failure message come with updated ticket info

models-  
user -wil have reference to tickets array, name, phone, vehicle no, image, role
parking space-name, rows-colums basically parking spots 2-d aray, location, owner name, and ref to user for owner name, pics for maketing and livelocation pics and videos, price per spot per minutes, we can put differrnt price for under shade, or parkig space with ev charging etc
payment- ref to user if, ticket id, payment {satus, pending ammount}, paidsofar, total charge.

feebback -referrence to parking space, ticekt id, user i, content, stars, images

ticket - ref to userid,parkspcaeid, feedbackid, paymentid, bookedtime, arrival time, departure time, entry time, exit time, payment satus(from payment id reference), QR code, status booked/cancelled/paid

ticket will ahve optiion to cancel, after achargign cancelation charge, same wil be update in wallet.

also add notification for user, for upcoming parking, which naviagtes them to map showing direction for parking and also option to see ticket.

the ticket should also have option to show navigation for car owner to parking space address

use all free services,
the service I can tell, for mapleaflet, cloudinary to uplaod images, mongoose, razorpay, for sending ticket in mail etc.

ensure after scanning or clicking pictures the camera should close and should show some relavant UI componet or naigate to coorect route

also add role and route admin, whose UI will show all the parking requests, after the park owner has sumbmitted the form and live photos with location access, if the admin ok with parking space,it approves and parking space is registed and dded in db, else it updated the register form with commenst to fix, which then shown in reggister form option of park owner, the park owner edit the form and sends request again.

start writing with backedn code, then frontend
