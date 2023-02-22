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

![image](https://user-images.githubusercontent.com/91537767/220315481-12a2083f-d9af-4cd6-bb55-442867d732a9.png)
# III.	DETAIL ANALYSIS:
# 1.	Business process modeling notation (BPMN): 
1.1. Login application:

 ![image](https://user-images.githubusercontent.com/91537767/220315911-d0461ec6-310c-491a-8286-0a78a7b996c0.png)
 
- If the customer has an account, then login to the scan and payment system. On this page require customers to enter an account and password. During the input, the system will check the format of the input parameters: account, password and notify customers if they enter the wrong format. If wrong, the customer must re-enter them in the correct format.
- Then the system will check under the user database and confirm the account information, password. The user database will put the information for the login page and let the customer login successfully. Customers enter the system to start buying products.
- If login fails, the system will prompt an error message and the customer must re-enter account and password until they are all match with the user database. Or they can press “Forgot your password” to get the new password. 
- After pressing “Forgot your password”, the system will open a popup and the customer can get the new password by inputting the account and information. Same as login, the system will check the format of the input parameters, check under the user database and notify if the check fails. If nothing wrong, the system will confirm your new password by sending a link to your mail. If you don’t receive the mail, press “Resend mail” and the system will resend this link to your mail. After receiving and confirming the link, the user database will put the information for the login page and let the customer get the new password successfully. Customers enter the system to start buying products.

1.2. Register new account:

Do you have an account on our system yet? If not, Customer can create a new account by clicking the "Register" button. Then, a screen will pop up the registration page, customers enter their name, date of birth phone number, email, password. During the input, the system will check the format of the input parameters: birth date, phone number, email, password and notify customers if they enter the wrong format.
 ![image](https://user-images.githubusercontent.com/91537767/220316042-1fad4cc6-9309-4d9e-ae04-32af65ecf026.png)

If wrong, the customer must re-enter the birth date, phone number, email, password in the correct format. Then, the system will check under the customer database and notify the customer whether the email and phone number entered by the customer exist or not. If yes, customers must re-enter another phone number and email. After re-entering and checking successfully, the customer's account has been successfully created and displayed on the main screen.

1.3. Scan product:

To start adding new products to the shopping cart, customers click the "Scan" button to scan the barcode. Then display the scan screen. Customers select the products they want to buy, then scan the product's barcode. 

 ![image](https://user-images.githubusercontent.com/91537767/220316124-d894b98e-3cf5-4ee1-bb9c-e9e147d643ad.png)

The system will check the product identifier in the database. If the barcode is not valid, an error message is displayed to select another item. If the barcode is valid, the product information is displayed below the scanning screen, in this screen there will be buttons to add and delete product quantity.  Customers continue to buy and scan products until they no longer want to buy, then back to screen scan to check the products they want to buy and can edit the list of selected products. Once completed, customers can continue to the payment step.

1.4. Voucher and payment:

1.4.1 Voucher:

After finishing the scan product, In the order screen, Enter voucher code in the voucher textbox. Verify the voucher code down the Database. If the code is not valid, show an error message next to the textbox. After entering the correct voucher code, Check the value of voucher. There are 3 possibilities in checking voucher value: 
•	Enough: Automatic finish the order and exit the order screen.
•	Redundant: Display the redundant value. If customers want to use the voucher, they need to buy more to fit the redundant value or else they cannot use the voucher.
•	Not enough: Display the remaining value and continue to payment.

 ![image](https://user-images.githubusercontent.com/91537767/220316179-ababb005-3564-43d3-ad10-c78de8658c7f.png)

1.4.2. Payment methods:

After finishing adding the voucher (if not enough), we continue to pay. There are 3 main payment methods: Cash, Mobile wallet and Credit/Debit card
 ![image](https://user-images.githubusercontent.com/91537767/220316218-506280e3-1445-4feb-bd50-48c720a344a6.png)

1.4.2.1. Cash machine:

On the Cash machine, Scan the order number. On the Machine screen, show the price of overall order. Input money into the machine through a small receive gate under the machine screen, show money input on the screen right after that. If they have enough money or more, Press Done and return change if redundant. If they do not have enough money, inform them to choose another payment method under the money input row. After that, delete the order on the Machine’s screen.
 ![image](https://user-images.githubusercontent.com/91537767/220316258-4c2204c5-e86d-4d9e-9928-03f28261d752.png)

1.4.2.2. Mobile wallet:

 ![image](https://user-images.githubusercontent.com/91537767/220316285-3ec082a0-08e5-4995-8413-80cf92815d05.png)

First, the system will check your wallet if it has enough money to pay the bill. If it doesn't have enough money to pay, the system will ask if you want to continue this method, and you will have 2 choices: No and you will turn back to the payment screen to choose another method; Yes, and you will have to input your money to the wallet. After you input your money, you will have 3 ways to confirm your payment: check touch ID, enter PIN or enter OTP which is sent to your device. If you choose touch ID or enter PIN, the system will check your touch ID or your PIN which is presented and if it invalid, you can press the confirm button and pass to next step, if don`t, you can input them again. The last method is input the OTP which will be sent to your device after you choose this method, after you receive the OTP, you can input it and the system will check if it matched or not, if it wrong, the system will send you another OTP code and you can input it again. 

 ![image](https://user-images.githubusercontent.com/91537767/220316322-ef2cae2d-0a2d-4a11-adea-a7eb46a1c93d.png)

After you pass these steps, you will have to press the confirm button the last time for the system to confirm your payment, after that, the system will call API and will message you if the payment succeeded or not, if not, you will be shown an error message and turn back to the payment method.

1.4.2.3. E–banking:

![image](https://user-images.githubusercontent.com/91537767/220316339-7b8bb4f3-3346-4be4-b586-71fab0517de4.png) 

First, the system will check if you have declared your card, if you haven`t, you will be able to add your card to the system by putting your card information to the system and the system along with the bank will check your card information and message to you.

![image](https://user-images.githubusercontent.com/91537767/220316386-b06a7c41-cf62-4ebb-8fb8-a7e8eec35400.png) 

If you have your card declared, you can choose your type of card (bank, card type). After that, you will have 3 methods to confirm your payment just like mobile wallet.

![image](https://user-images.githubusercontent.com/91537767/220316419-49eef325-1bc3-42da-9660-d07f6b7d6157.png)
 
Finally, the system will send the bank the bill information to confirm your payment and message to you if the payment succeeded or not.

1.4.2.4. Gateway:

![image](https://user-images.githubusercontent.com/91537767/220316445-c795e137-34fa-41ff-8bb6-8d79f42c885e.png) 

The final part of this process, on this part, you will have to do some procedure to confirm your payment the last time and save it to the DB. First, the system will scan your customer code and check your code in the DB.

After that, the system will scan the barcode`s item in your bag and check all items if it matches with your order. If everything is correct, the system will save the bill into DB and the gateway will open and you can exit the app. Or if something is wrong, the system will send you notifications and the process will be back to the payment process that ask the customer if they want to pay for the items that lacked.

# 2.	Data Flow Diagram (DFD):
2.1. Context Diagram:

 ![image](https://user-images.githubusercontent.com/91537767/220316520-f8c018fd-08c5-4987-93d4-c92f28ccef04.png)

2.1.1. Diagram:

Context diagram DFD for the “Order and Payment” app includes:
	Process
- Order and payment

	External entity 
- Bank system
- Mobile wallet
- Cash machine

	Data store
- Customer
- Warehouse
- Products

2.1.2. Description:

•	The customer access the app by entering their customer account information (email/phone, password). 
•	The customer start to scan the products they want to buy by using app.
•	The app checks to see if the product barcode is valid or not by with data obtained from the data store.
•	After the customer finishes selecting products, in case the customer want to pay they will choose 1 of 3 payment methods on app (cash machine/ mobile wallet/ Card)
•	The app will send bill information to the bank, mobile wallet or cash machine system according to the payment method that the customer has chosen. 
•	The payment system that the customer choose will check customer bill information and return payment success or failure to the app system.
•	To get out the store, the customer open the app to take their Customer ID and then they just need to scan it through the screen on gateway.
•	The gateway system will send list of product barcode to the app if they are not paid. 

2.2. Level 0:

 ![image](https://user-images.githubusercontent.com/91537767/220316551-da7c482f-016d-436c-b529-932b16d59b3f.png)

2.2.1 Login/ Register:

- In case the customer already has an account, they just need to fill in 2 required fields including email/phone and password to log in. 
- In case the customer hasn’t has an account, they need to input some of their necessary information on the sign up page. 
- In both case, the app system will check validation of customer account information in the database Customer.
- In case of login, if successful, the app system will push the customer account information from database for order creation process and let the customer login. 
- In case of register, if successful, the app system will update/save the customer account into database Customer and push the customer information for order creation process
- Customers enter the system to start buying products.

2.2.2. Create order:

- The customer pick the products they want to buy and scan their barcode by scan screen.
- The app system will check the validation of product barcode in database Products. 
- Product that is scanned successfully will be added to the order created in FE. 
- After the customer finish scanning all the products they want to buy successfully, the order creation process also be completed.

2.2.3. Payment:

- After creating the order. The customer will choose the payment methods to conduct the payment process.
- In payment process, the app system will take the information from order details to create bill information.
- Then the app system will send the bill information to the bank, cash machine or mobile wallet system according to the payment method that the customer has chosen.
- The payment system that the customer choose will check customer bill information and return payment success or failure to the app system. 
- When payment process is successful, the app system will save the order details of the customer into database Order. 

2.2.4 Security:

- To get out the store, the customer open the app to take their Customer ID and then they just need to scan it through the screen on gateway.
- The security system of gateway get the order number of this customer from database Order to check if it is processing. 
- The gateway system will send list of product barcode to the app if they are not paid. 
- The app system push notification to show the missing products to the customer. 
- When finishing, the app system will update the order status in database Order and update inventory change in database Warehouse. 

2.3. Level 1:

 ![image](https://user-images.githubusercontent.com/91537767/220316577-d3dc081b-bb53-4b50-b8fc-9f2b04c7332d.png)

At the process sign in, customers will send their information. At the same time, from the database, customer data will be gotten to check whether there is a match or not.  If successful, customer info (customer ID) will be sent to the process Scan product.
At the process sign up, customers will send their information. If successful, a new account will be created and saved into the customer database. Plus, customer info (customer ID) will be sent to the process Scan product.
With customer info from the process Sign in/ Sign up, the process Create order will create a new order and send order number to the process Scan product. Besides, product barcodes from customer and product barcodes gotten from product database are input for the process Scan product to check the matching. Output of this process is order detail (order number, customer ID, list product, total amount, ...).
The order detail and payment method (by cash, by E-banking, by mobile wallet) is the input of the process Payment. Based on the payment method, bill info which is the output of the process will be given to the Cash machine or Mobile wallet, or bank system. After that, a payment message status will be sent from those entities to the process Payment. Output of this message is order detail which will be sent to the order database.
When customers leave the store, they have to check security at the gateway. They give their ID to the process Verify order and this process gets the order number from the order database to find the processing order. At the same time, gateway gives a list of barcode products to check the matching. 
•	If successful, this process sends the accepted order to the process Accept order. This process will: 
•	Update order status from Not checked security to Done.
•	Save order number into the Receipt database.
•	Give the inventory change to the Warehouse database to update related quantity products.
•	If not, send the rejected order to the process Rejected order. This process will show the missing product to customer.
# 3.	Usecase - Sequence Diagram:
3.1. Usecase:

![image](https://user-images.githubusercontent.com/91537767/220316676-4a74000b-3fee-432a-a130-202a5baef4f5.png)
 
This app has 6 main use cases (Register, Log in, Scan product, Create order, Make payment and Check security) and 5 actor (customer, cash machine, bank systems, mobile wallet, gateway).
When a customer registers a new account, the Register always calls Check FE and BE validations. When there is an error in FE or BE, the Show error will be called by Register. 
The Login is only used when the Register has been done before. Like Register, the Login also always calls Check FE and BE validations. When there is an error in FE or BE, the Show error will be called by Log in. But when the customer forgot the password, the Forgot password may be called by the Login.
The Create order is only used when the customer logs in successfully.
The Scan product is only used when the customer creates an order. It always calls the Check barcode valid to add items to order. The Show error may be called by the Scan product when the scan product fails.
The Make payment is only used when the customer has done scan all products. There are 3 choices to pay: Pay by cash, Pay by mobile wallet, Pay by E-banking. The Pay by cash always calls the Confirm payment successfully. But when there is an error in the payment process, the Show error message will be called. The other methods are similar.
The Check security always calls the Make payment when complete payment. When the customer leaves, the gateway will check the reality order. So the Confirm is always called by the Check security. If it finds missing products, the Show error will be called.

3.2. Sequence:

 ![image](https://user-images.githubusercontent.com/91537767/220316702-ecdf1c9e-d571-49d3-94f6-de3e20bd6c3c.png)
![image](https://user-images.githubusercontent.com/91537767/220316736-a61eae04-2908-4658-abfa-895afe5b49d4.png)

 
3.2.1. Register:

![image](https://user-images.githubusercontent.com/91537767/220316772-06b810a2-d0f8-42e4-85f6-1f1460255e6e.png)

In the register process, the customer fills the register field in the APP interface. Then, it will check the input format. 
•	 If FE invalid, the APP interface will show an error message.
•	 If not, continue to step Checking username existence at System and step Checking username existence at User Database. If the user is found, it sends this info to System, and from the System to APP interface to show an error message. Else, it sends info to System, and from the System to APP interface to show the message. Besides, save this account into the user database.

3.2.2. Log in:

![image](https://user-images.githubusercontent.com/91537767/220316816-0f9a2c6c-1e55-4e0f-a9e5-95ed36314e8b.png) 

In the login process, the customer fills the register field in the APP interface. Then, it will check the input format. 
•	If FE invalid, the APP interface will show an error message.
•	If not, continue to step Checking username existence at System and step Checking username existence at User Database. If the user is found, it sends this info to System, and from the System to APP interface to show homepage. Else, it sends info to System, and from the System to APP interface to show the error message. Next, the customer chooses the Forgot password and fills the textbox. All steps for checking FE and BE are the same as register. Particularly in the case of the user found, the customer must confirm the link sent to the mail. If not received link, customer choose resend link and this action will send to system and the system will resend link email to customer. Else, they confirm the link email and it is sent to the system. System will save new passwords under the database. At the same time, call show homepage to the APP interface to show homepage for customers.

3.2.3. Scan produce & Create order:

 ![image](https://user-images.githubusercontent.com/91537767/220316869-8cf8b26a-5c93-48cd-9952-7def2561fb7c.png)

First of all, the customer presses scan on the main screen. This action will create an order number on a local device. Next, the APP interface shows the scan screen. The customer will scan the product barcode. This action will call the system to check the barcode valid under the product database.
•	 If barcode is invalid, the product database returns failed status to system and system returns failed status to APP interface. The APP interface shows an error message to the customer.
•	If barcode is valid, the product database sends product info to the system to update order in the APP interface. A mini popup will show below the scan screen about product info. At popup, the customer can press “+ 'or “-” on purpose and the APP interface will update the order based on that action. The customer can press back to screen to see order detail. At that time, the customer can add or delete the product on purpose. The action adds or delete is optional.

3.2.4. Payment:

3.2.4.1 Voucher (Optional with customer)

 ![image](https://user-images.githubusercontent.com/91537767/220316926-a64c58bb-7a5b-41ef-b6c3-b2c4eb54bdec.png)

- Voucher in sequence is an optional choice, in case the customer has voucher, they can enter voucher code into the app. On the other hand, they can get straight to step choose payment methods.
- When customer entered voucher code, the FE or App interface will call system or BE to check validation of this voucher with those conditions like if it is available, belong to this store…
- When come to this step, there will be two cases. To describe these cases, use Alter condition (If condition).
	Case 1: Invalid
+ The app system checks the validation of the voucher code in database and return failed test result to the App interface. 
+ The App interface show error message to inform the customer that the voucher is not valid.
	Case 2: Valid
+ The app system checks the validation of the voucher code in database successfully and simultaneously update the value of the voucher in database.
+ In this case, there will be 3 cases include Not enough, Enough, Redundant. These 3 cases use to describe 3 situations in reality when the voucher code that the customer entered has the value is less than, more than or equal to the total amount of order.
•	Case 1: Not enough
The system will calculate the remaining amount of order after subtracting the value of the voucher in database.
The system will call App interface to inform the customer the remaining amount of order. 
The App interface push notification to show the customer the remaining amount of order after subtracting voucher.
•	Case 2: Enough
The system checks the value of the voucher in database and see that it is equal to the amount of the payment. 
The system subtracts the value of the voucher in database and save the successful payment into database.
The system calls App interface to inform the customer that the payment has been done successfully.
The App interface back to home screen.
•	Case 3: Redundant 
The system checks the value of the voucher in database and see that it is more than the amount of the payment.
The system will call App interface to inform the customer the remaining value of the voucher.
The App interface will show messages “Want to continue?” to the customer. 
Come to this step, there will be 2 cases to ask if the customer want to continue purchasing or not.

	Case 1: Yes

The App interface back to scan screen and let the customer continue their purchasing goods process. 
	Case 2: No

The system subtracts the value of the voucher in database and save the successful payment into data base.
The system calls App interface to inform the customer that the payment has been done successfully.
The App interface back to home screen.

3.2.4.2 Payment:

- In payment process, the customer will choose one of three payment methods on app. So the will be an Alternative condition for this situation with 3 cases.
	Case 1: Pay by cash machine

 ![image](https://user-images.githubusercontent.com/91537767/220317060-6665cf64-8c98-432c-b2e1-509a75c3592e.png)

 
+ The App interface will send the order number of the customer that has been created on FE to system (BE).
+ The system will send the order number to the cash machine system.
+ The customer scans the order number on screen’s app to cash machine.
+ The cash machine will show the total amount order on screen after the customer complete scanning the order number.
+ Simultaneously, the FE show the processing screen while the payment with cash machine is processing.
+ When the customer import money into cash machine, it shows the imported money on is screen.
+ Now, there will be 2 cases that is the money is enough or not enough.

•	Case 1: Not enough 
The cash machine system will call the app system that the payment is not completed.
The App system will call the back the FE that the payment is not complete.
The FE will get out of the processing screen and back to the payment screen. 

•	Case 2: Enough 
In this case, there will be 2 cases separately that is the money is equal to the order amount and the money is more than the order amount. With second case, the cash machine will return change. 

	Case 1: Yes (Return change)
The cash machine return change to the customer and call the app system that the payment has been done successfully.
The app system calls the App interface to inform the customer and save the successful payment order into database.
The App interface get out of processing screen and get back to home screen (auto done).

	Case 2: No (Not return change)
The cash machine calls the app system that the payment has been done successfully.
The app system calls the App interface to inform the customer and save the successful payment order into database.

	Case 2: Pay by the mobile wallet
 ![image](https://user-images.githubusercontent.com/91537767/220317109-8520506a-ac22-4cfe-8b3a-4032731ac79b.png)

+ The App interface will send the order number of the customer that has been created on FE to app system (BE).
+ The app system will send the order number to the mobile wallet system.
+ The customer open app. At this moment the App interface will send request call API to the app system and the app system will send request to mobile wallet system. 
+ The mobile wallet system will accept the payment request from app system and begin to handle the payment. 
+ After finishing the process, the mobile wallet will call the app system to show that the payment is successful or not. There will be 2 cases in this situation.
•	Case 1: Successful 

The app system will call the App interface to inform the customer that the payment has been done successfully and save the successful payment order into database.
The App interface backs to home screen (auto done).
•	Case 2: Not successful 

The mobile wallet system shows error message and call the app system that the payment is not completed.
The app system will call the App interface to inform the customer that the payment has been failed.
The App interface back to payment screen.

	Case 3: Pay by the E - banking 

 ![image](https://user-images.githubusercontent.com/91537767/220317137-d7b2c5e1-5676-4a1f-ae9e-2248ee5a3488.png)
 
+ First of all, to pay by E – banking the customer must declare the card of that bank. So the will be 2 cases in this situation and it will be put into a loop in case customer want to keep paying by E – banking method and want to retry if there was a system error during the declaring card process.
+ In a loop, there will be 2 choices for the customer is Add new card with one who hasn’t declared before and Choose card with the opposite situation. The loop will end until the choose card/add card process is successful.

•	Case 1: Add card 
In this case, there will be an optional condition is “Is 1st add or want to read?”
The customer will enter card information into App system and the App system will push these information to bank system.
The bank system will check validation of card and send feedback to the App system. 
In case it is failed the App system will call the FE to inform the customer.
The FE show error message on screen. 

•	Case 2: Choose card

In this case, there will be an optional condition is “Is 1st add or want to rechoose?”
The customer will choose the bank and confirm declared card and the App system will push confirmed information to bank system.
The bank system will check validation of card and send feedback to the App system. 
In case it is failed the App system will call the FE to inform the customer.
The FE show error message on screen.
+ When the loop ends (successful), the App interface will push bill information to the App system and the App system push bill information to bank system to begin payment. 
+ After finishing the process, the bank system calls the App system to show the payment is successful or not. There will be 2 cases in this situation.

•	Case 1: Successful 

The App system will call the App interface to inform the customer that the payment has been done successfully and save the successful payment order into database.
The App interface backs to home screen (auto done).

•	Case 2: Not Successful

The App system will call the App interface to inform the customer that the payment has been failed.
The App interface show error message and back to payment screen.

3.2.5. Security:

![image](https://user-images.githubusercontent.com/91537767/220317613-9d4e7088-6c2f-4176-bfe2-288826d62ed5.png)

When payment successfully, order number from local device (APP interface) send to System then send to Order database and finally send to gateway. The customer has to check security at the gateway to leave the store. The customer will scan customer code at gateway to check order processing. At the same time, the customer gives the gateway all barcode’s items in the bag. If all items in bags match order processing, gateway will return successful status to the system then to the APP interface to show the customer. Besides, the system updates order status from Not checked security to Done and updates warehouse, receipt. Else, return missing products to the system then to the APP interface to push notification to the customer. The customer can pay or not. If pay, press back to the payment screen and make the payment.

