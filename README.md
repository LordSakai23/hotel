# Hotel Management
This is a code that displays the available rooms and the times its available in a hotel and also displays the resturaunt menus to the user while giving them the ability to book free rooms.
## Usage

```python
def Home():
  print("Welcome to the home page")
  print("Please select an option")
  menu = int(input("1. Available rooms \n 2. Resturaunts \n 3. Book a room \n 4. Exit"))
  if menu == 1:
    Rooms()
  elif menu == 2:
    Resturaunts()
  elif menu == 3:
    Booking()
  elif menu == 4:
    print("Thank you for visiting")
  else:
    print("Please select a valid option")
    Home()


def Rooms():
  open("roomba.csv", "r")
  print("These are all the available rooms")
  menu = int(input("1. Book a room \n 2. Return to home page"))
  if menu == 1:
    Booking()
  elif menu == 2:
    Home()
  else:
    print("Please select a valid option")


def Resturaunts():
  print("These are all the meals and drinks the resturaunt has in it's menu")
  g = open("Resturaunt_menu.csv", "r")
  g.close()

def Booking(): 
  name = input("Enter your name: ")
  address = input("Enter your address: ")
  phone_number = input("Enter your phone number: ")
  email_address = input("Enter your email address: ")
  room_type = input("Enter the type of room you would like to book: ")
  number_of_nights = input("Enter the number of nights you would like to stay: ")
  # Create a new booking
  booking = {
    "name": name,
    "address": address,
    "phone_number": phone_number,
    "email_address": email_address,
    "room_type": room_type,
    "number_of_nights": number_of_nights
  }
  # Add the booking to the database
  f = open("bookings.csv", "a")
  f.write(str(booking))
  f.close()
  print("Your booking has been confirmed.")

Home()
```
