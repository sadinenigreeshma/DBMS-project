# DBMS-project
# OBJECTIVE:
To create an Art Gallery Management System that keeps record of the artists, their paintings, art gallery details, exhibition details and showcase pictures of paintings to the customers

# ABSTRACT: 
Many art gallery exhibitions are held for exhibiting paintings by various artists in order to showcase their talent. As a part of this various customers will be visiting the Art gallery to buy paintings and there are few customers who have keen interest about the paintings will observe each and every art in the art gallery.
A Customer who visits the Art Gallery will be asked for Customer id. The Customer should enter his Name, Email id, Password, Customer ID given to him, Phone Number and Address it has to get reflected on the customer’s table. After entering into the gallery, each art consists of Art id, Art name, Type of painting. If the customer wants to know the painting’s details he can contact the Artist by the Artist Name, Artist id, Phone Number and Address. If he wants to buy these paintings, he can order them via Billing which consists the Date of Purchase. These orders must have a Bill ID, Cost of each painting and Total Cost. When ordering, the customer can attain Discount by some percentage which when deducted determines the total Amount. The Art Gallery may organize an Exhibition to which the Customer can Register with the Date of Registration. The Exhibition organised by the Art Gallery has an Exhibition Name, Exhibition ID, Duration, Start Time and End Time. The Artist from the Art Gallery can also participate in the following. Apart from the Customer who visits the Art Gallery, Visitants are also allowed to visit on the day of the Exhibition by registering with giving their Visitor ID, Visitor Name and Email ID.

# REQUIREMENT ANALYSIS:
Let us consider traditional system where the data is stored in files. The drawback of this system is it is very difficult to retrieve the data from case files. It is difficult to retrieve the data from case files. It is difficult to handle the whole system manually  and it is less accurate to keep the data in case files because the files may get destroyed. Redundancy of data may occur and this lead to the inconsistency. It is time consuming.
   The proposed system is easy to operate. Speed and accuracy are the main advantages of proposed system. There is no redundancy of data. The data are stored in the computer’s secondary memories like hard disk etc. it can be easily receive and used at any time. The proposed system will easily handle all the data and the work done by the existing system. The proposed system eliminate the drawbacks of the existing system to a great extent and it provides tight security to data.

# MODULE DESCRIPTION: 
•	CUSTOMERS MODULE: Customers will come to the gallery to visit the paintings and as each person has to enter their email, name, password, id, address initially when they visit if they are existing users then there is no need to enter the details, he can directly proceed to visit the gallery after giving id.

•	ART GALLERY MODULE: After entering to the gallery, it has artistid, artname, artid, type of painting for every individual painting presented in the gallery. We have various paintings in the gallery.

•	ORDERS MODULE: Customer can order the paintings which contains the date of purchase, Artname of the painting, Order name, cost of every painting which he chose and also the total cost of the paintings which he ordered.

•	DISCOUNT MODULE: Customer can receive discount on their orders for a certain percentage of the cost and the total amount is determined.

•	EXHIBITON MODULE: The Art Gallery can organise an Exhibition with ExhibitionID, ExhibitionName, Duration, Start Time and End Time which can be attended by both customers and visitors. The Artists can also take part in this Exhibition.

•	VISITANT: Visitors can also visit the exhibition by registering with their VisitorID, VisitorName, EmailID, and the date of their visit.

•	ARTIST MODULE: If the customer who visited Artgallery liked one particular painting then he can have the paintings details like who is the artist painted 
the painting their Artistid, Artistname, his address and also his Phonenumber.


## CONCEPTUAL DATABASE DESIGN:

# ER MODEL:
 ![image](https://user-images.githubusercontent.com/71624353/180633359-afc4d338-42c4-4080-b0df-fbd94bc39cd3.png)

 

# ENTITIES: 
Customers, Art Gallery, Administration, Orders, Discount, Artist, Exhibition, Visitant

# SCHEMA: 
Customers (Email char(20) , CustomerName char(20), CustomerID int, Address char(20), PhoneNumber int)
Art Gallery (ArtID int, ArtName char(20), TypeOfPainting char(20), NumberOfCopies int)
Artists (ArtistID int, ArtistName char(20), Address char(20), PhoneNumber int)
Orders (OrderID int, Cost int, TotalCost int)
Discount (Amount int, Percentage int)
Exhibition (ExhibitionID int, ExhibitionName char(20), Duration int, Starttime int, Endtime int)
Visitant (VisitorID int, VisitorName char(20), EmailID char(20)

# RELATIONAL DATABASE SCHEME:
# ENTITY	     RELATIONSHIP  	ENTITY	     CARDINALITY
Customer	   Signup	        Art Gallery	  Many to Many
Art Gallery	 Bill	          Orders	      Many to Many
Orders	     Attain	        Discount	    Many to one
Customer	   Register	      Exhibition	  Many to many
Visitant	   Visits	        Exhibition	  Many to many
Art Gallery	 Organises	    Exhibition	  Many to one
Artist	     Participates	  Exhibition	  Many to many








