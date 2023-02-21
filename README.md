# Supermarket-Payment
# I.	OVERVIEW PROJECT:
# 1.	Description:
In this era of technology, electronic payment has become popular and especially in Vietnam, it is present everywhere and has become a habit of many Vietnamese people. We can see that this form possesses many outstanding utilities such as: convenient, fast, suitable for the market; easy to monitor and control; limit risks when using cash.
Seeing the security, easy-to-use operation, fast transaction, and convenient control when needed, our team has explored and researched to come up with suitable mobile application development solutions. Since then, our team has chosen the topic for the project as "Mobile application for retail supermarkets, allowing customers to automatically create invoices and pay directly on the phone, no need to go to the cashier counter. ".
Based on the current buying situation, it takes a lot of time and effort. This topic will help fix that with 3 main parts:
Part I: Overview project.
Part II: Overview analysis.
Part III: Detailed analysis.
# 2.	Objectives:
 This project is built with the aim of applying the learned knowledge and self-learning explore to create an iOS-based and Android-based mobile application for customer purchases and payment with retail supermarkets or convenience stores, help users making transaction fast and conveniently.
This application will have a simple interface, diverse and comprehensive payment methods, simple registration procedures, scan the QR code at the last step after each payment so as not to inconvenience customers when going. gate pass. such as preventing product theft or fraud.
This application allows users to use the necessary functions: login / account registration, view information about store products, pay transactions, save information, print e-invoices or send invoices. to the user's email. Specifically, after registering for membership or logging in to an existing account on the system, users can choose products on the application to put in the shopping cart and make purchases. After selecting the goods, customers switch to payment by choosing the forms of payment: by voucher, e-wallet, credit / debit card. After finishing the transaction, customers click confirm to complete the transaction. The app will confirm the successful payment and send the user a QR code and the user will scan this QR code at the entrance.
# II.	OVERVIEW ANALYSIS:
# 1.	Business requirement:
In order for the system to operate smoothly, to meet the set objectives and minimize system failures, the following requirements must be met:
	System components need to be closely and optimally linked to ensure software works properly, saving processing time and labor.
	When saving data, it is necessary to ensure that the data is arranged properly, the storage memory of the data warehouse must be large enough to hold information, avoiding information noise and information overload.
	Simple interface, easy to get used to and use aim to help users making transaction fast and conveniently without cashier.
# 2.	Overall flow:
-	BPMN include: Application, Cash machine, Mobile wallet, Mobile POS
-	In application include following function: 
•	Scan and show information about products of the store
•	Manage the shopping cart that the customer is choosing
•	Error notification: Display an error that the customer has not made the payment when going out the door
-	In cash machine:
•	Support receiving and paying in cash for customers
-	In Mobile wallet:
•	Payment support through e-wallets for customers
-	In Mobile POS:
•	Used when customers pay by swiping credit/debit card
