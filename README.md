# Hotel Management App
Simple and intuitive kivy application for hotel management. It maintains it's record in an excel workbook and uses it to display and modify information.
## Features
* Only a verified employee who is listed in excel sheet can use the app.
* On adding a new guest the data is stored along with the current date as the check in date and the username of the employee logged in as Receiver.
* While adding adding amount to bill or during final payment, the user can input the room number and press `Enter` which will automatically pick up the current occupant's details.
* While adding a new guest it throws a popup if the room assigned is already occupied.
* When the final payment is done check out date is set to current date automatically.
## Installation and Setup
The application requires kivy, kivyMD for the gui and openpyxl to work with excel workbook. Here is the link for [pyhon installation](https://www.python.org/downloads/)
To install kivy, kivyMD and openpyxl use the following commands in the terminal.<br>
`pip install kivy`<br>
`pip install kivymd`<br>
`pip install openpyxl`<br>
Clone the repository to your local machine and create a new excel sheet with one sheet containing the customers data and another containing the employees data.
Copy the path of the excel workbook to wb_address variable in the `management.py` file.
#### Customers Sheet
This sheet will have 10 columns namely *Name*,*EmailId*,*Phone No.*,*Number of Members*,*Room*,*Check in*,*Check out*,*Receiver*,*Bill*,*Available*.
Copy the sheets name to `ws_customer` variable in `management.py` file (if the sheets name is explicitly changed)
* ***Name*** : Name of the customer
* ***EmailID*** : Email id of the customer
* ***Phone No.*** : Phone number of the customer
* ***Number of members*** : Number of customers along with a customer
* ***Room*** : Room Number allotted to the customer
* ***Check in*** : Check in date of the customer
* ***Check out*** : Check out date of customer
* ***Receiver*** : Employee logged in while adding the customer
* ***Bill*** : Current bill of the customer
* ***Available*** : If the customer is still present in the hotel
#### Emplyees Sheet
This sheet will have 2 columns namely *Username*,*Password*.
Copy the sheets name to `ws_employee` variable in `management.py` file (if the sheets name is explicitly changed)
* ***Username*** : Username of the employee
* ***Password*** : Password of the employee<br>
***This sheet should have atleast one user to log into the app. This sheet cannot be manipulated via the app.***
## References
* [KivyMD Documentation](https://kivymd.readthedocs.io/en/latest/)
* [Kivy Documentation](https://kivy.org/doc/stable/)
* [Openpyxl Documentation](https://openpyxl.readthedocs.io/en/stable/)
