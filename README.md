class Order:
    def __init__(self, orderID, deliveryAddress, recipientName, packageDetails, deliveryDate, status):
        # Constructor with required attributes
        self.orderID = orderID
        self.deliveryAddress = deliveryAddress
        self.recipientName = recipientName
        self.packageDetails = packageDetails
        self.deliveryDate = deliveryDate
        self.status = status

    # Getter methods
    def get_orderID(self):
        return self.orderID

    def get_deliveryAddress(self):
        return self.deliveryAddress

    def get_recipientName(self):
        return self.recipientName

    def get_packageDetails(self):
        return self.packageDetails

    def get_deliveryDate(self):
        return self.deliveryDate

    def get_status(self):
        return self.status

    # Setter methods
    def set_orderID(self, orderID):
        self.orderID = orderID

    def set_deliveryAddress(self, deliveryAddress):
        self.deliveryAddress = deliveryAddress

    def set_recipientName(self, recipientName):
        self.recipientName = recipientName

    def set_packageDetails(self, packageDetails):
        self.packageDetails = packageDetails

    def set_deliveryDate(self, deliveryDate):
        self.deliveryDate = deliveryDate

    def set_status(self, status):
        self.status = status

    # Method to calculate total charges (stub for now)
    def calculate_total_charges(self):
        pass  # This function should calculate the total charges for the order.


class Customer:
    def __init__(self, customerID, name, email, phone, address):
        # Constructor with required attributes
        self.customerID = customerID
        self.name = name
        self.email = email
        self.phone = phone
        self.address = address

    # Getter methods
    def get_customerID(self):
        return self.customerID

    def get_name(self):
        return self.name

    def get_email(self):
        return self.email

    def get_phone(self):
        return self.phone

    def get_address(self):
        return self.address

    # Setter methods
    def set_customerID(self, customerID):
        self.customerID = customerID

    def set_name(self, name):
        self.name = name

    def set_email(self, email):
        self.email = email

    def set_phone(self, phone):
        self.phone = phone

    def set_address(self, address):
        self.address = address

    # Method to log in (stub for now)
    def log_in(self):
        pass  # This function should handle the customer's login.


class Employee:
    def __init__(self, employeeID, role, name, workSchedule):
        # Constructor with required attributes
        self.employeeID = employeeID
        self.role = role
        self.name = name
        self.workSchedule = workSchedule

    # Getter methods
    def get_employeeID(self):
        return self.employeeID

    def get_role(self):
        return self.role

    def get_name(self):
        return self.name

    def get_workSchedule(self):
        return self.workSchedule

    # Setter methods
    def set_employeeID(self, employeeID):
        self.employeeID = employeeID

    def set_role(self, role):
        self.role = role

    def set_name(self, name):
        self.name = name

    def set_workSchedule(self, workSchedule):
        self.workSchedule = workSchedule

    # Method to assign delivery agent (stub for now)
    def assign_delivery_agent(self):
        pass  # This function should assign a delivery agent to the order.


class Payment:
    def __init__(self, paymentID, amount, paymentStatus, paymentMethod):
        # Constructor with required attributes
        self.paymentID = paymentID
        self.amount = amount
        self.paymentStatus = paymentStatus
        self.paymentMethod = paymentMethod

    # Getter methods
    def get_paymentID(self):
        return self.paymentID

    def get_amount(self):
        return self.amount

    def get_paymentStatus(self):
        return self.paymentStatus

    def get_paymentMethod(self):
        return self.paymentMethod

    # Setter methods
    def set_paymentID(self, paymentID):
        self.paymentID = paymentID

    def set_amount(self, amount):
        self.amount = amount

    def set_paymentStatus(self, paymentStatus):
        self.paymentStatus = paymentStatus

    def set_paymentMethod(self, paymentMethod):
        self.paymentMethod = paymentMethod

    # Method to verify payment (stub for now)
    def verify_payment(self):
        pass  # This function should verify the payment status.


# Create objects of the classes
order = Order(orderID="ORD12345", deliveryAddress="45 Knowledge Avenue, Dubai, UAE", recipientName="Sarah Johnson",
              packageDetails="Laptop, Wireless Mouse & Pad Set", deliveryDate="2025-01-25", status="Pending")
customer = Customer(customerID="CUST1001", name="Sarah Johnson", email="sarah.johnson@example.com",
                    phone="0501234567", address="45 Knowledge Avenue, Dubai, UAE")
employee = Employee(employeeID="EMP101", role="Delivery Agent", name="John Doe", workSchedule="9AM - 5PM")
payment = Payment(paymentID="PAY1001", amount=283.50, paymentStatus="Verified", paymentMethod="Credit Card")

# Simulate generating a Delivery Note using the objects
def generate_delivery_note():
    # Display the Delivery Note Information
    print(f"Delivery Note for Order ID: {order.get_orderID()}")
    print(f"Recipient: {order.get_recipientName()}")
    print(f"Delivery Address: {order.get_deliveryAddress()}")
    print(f"Package Details: {order.get_packageDetails()}")
    print(f"Delivery Date: {order.get_deliveryDate()}")
    print(f"Status: {order.get_status()}")
    print(f"Payment Status: {payment.get_paymentStatus()}")
    print(f"Payment Method: {payment.get_paymentMethod()}")
    print(f"Total Charges: {payment.get_amount()} AED")
    print(f"Employee Name: {employee.get_name()}")
    print(f"Assigned Delivery Agent: {employee.get_name()}")

# Generate the Delivery Note
generate_delivery_note()
