# Delivery Management System
class Customer:
    def __init__(self, name, contact, street, city, country):
        """Initialize recipient details"""
        # Protected attributes using naming convention
        self._name = name
        self._contact = contact
        self._street = street
        self._city = city
        self._country = country

    # Getters
    def get_name(self): 
        """Return recipient's full name"""
        return self._name
    def get_contact(self): 
        """Return contact information"""
        return self._contact
    def get_street(self): 
        """Return street address name"""
        return self._street
    def get_city(self): 
        """Return city name"""
        return self._city
    def get_country(self): 
        """return country name"""
        return self._country

    # Setters
    def set_name(self, name): 
        """Update recipient's name"""
        self._name = name
    def set_contact(self, contact): 
        """Update contact information"""
        self._contact = contact
    def set_street(self, street): 
        """Update street address"""
        self._street = street
    def set_city(self, city): 
        """Update city name"""
        self._city = city
    def set_country(self, country): 
        """Update country name"""
        self._country = country

    def format_address(self):
        """Combine address components into formatted string"""
        return f"{self._street}, {self._city}, {self._country}"

class Delivery:
    def __init__(self, order_num, ref_num, date, method, dimensions, weight):
        """Initialize delivery parameters"""
        self._order_num = order_num
        self._ref_num = ref_num
        self._date = date
        self._method = method
        self._dimensions = dimensions
        self._weight = weight

    # Getters
    def get_order_num(self): 
        """Retrieve order number"""
        return self._order_num
    def get_ref_num(self): 
        """Retrieve reference number"""
        return self._ref_num
    def get_date(self): 
        """Retrieve date"""
        return self._date
    def get_method(self): 
        """Retrieve method"""
        return self._method
    def get_dimensions(self): 
        """Retrieve dimensions"""
        return self._dimensions
    def get_weight(self): 
        """Retrieve weight"""
        return self._weight

    # Setters
    def set_order_num(self, num): 
        """Modify order number"""
        self._order_num = num
    def set_ref_num(self, num): 
        """Modify reference number"""
        self._ref_num = num
    def set_date(self, date): 
        """Modify date"""
        self._date = date
    def set_method(self, method): 
        """Modify nethod"""
        self._method = method
    def set_dimensions(self, dim): 
        """Modify dimensions"""
        self._dimensions = dim
    def set_weight(self, weight): 
        """Modify weight"""
        self._weight = weight

    def calculate_shipping_cost(self):
        """Calculate shipping cost based on weight and dimensions"""
        pass

class Item:
    def __init__(self, code, desc, qty, unit_price, total_price):
        """Initialize product item details"""
        self._code = code
        self._desc = desc
        self._qty = qty
        self._unit_price = unit_price
        self._total_price = total_price

    # Getters
    def get_code(self): 
        """Retrieve product code"""
        return self._code
    def get_desc(self): 
        """Retrieve product description"""
        return self._desc
    def get_qty(self): 
        """Retrieve product qauntity"""
        return self._qty
    def get_unit_price(self): 
        """Retrieve product unit price"""
        return self._unit_price
    def get_total_price(self): 
        """Retrieve total price"""
        return self._total_price

    # Setters
    def set_code(self, code): 
        """Update product code"""
        self._code = code
    def set_desc(self, desc): 
        """Update product description"""
        self._desc = desc
    def set_qty(self, qty): 
        """Update product quantity"""
        self._qty = qty
    def set_unit_price(self, price): 
        """Update product unit price"""
        self._unit_price = price
    def set_total_price(self, price): 
        """Update total price"""
        self._total_price = price

    def update_quantity(self, new_qty):
        """Update quantity and recalculate total price"""
        pass

class Invoice:
    def __init__(self, subtotal, taxes, total_charges, currency):
        """Initialize financial details"""
        self._subtotal = subtotal
        self._taxes = taxes
        self._total_charges = total_charges
        self._currency = currency
        self._payment_status = "Unpaid"

    # Getters
    def get_subtotal(self): 
        """Retrieve pre-tax amount"""
        return self._subtotal
    def get_taxes(self): 
        """Get tax amount"""
        return self._taxes
    def get_total_charges(self): 
        """Return final total charges"""
        return self._total_charges
    def get_currency(self): 
        """Get currency type"""
        return self._currency
    def get_payment_status(self): 
        """Retrieve payment status"""
        return self._payment_status

    # Setters
    def set_subtotal(self, amount): 
        """update subtotal"""
        self._subtotal = amount
    def set_taxes(self, amount): 
        """update taxes"""
        self._taxes = amount
    def set_total_charges(self, amount): 
        """update total charges"""
        self._total_charges = amount
    def set_currency(self, currency): 
        """update currency"""
        self._currency = currency
    def set_payment_status(self, status): 
        """update payment status"""
        self._payment_status = status

    def generate_receipt(self):
        """Generate formatted receipt document"""
        pass

# Create objects (2 instances per class)
recipient1 = Customer(
    "Mohammed Ali",
    "mohammed.johnson@example.com",
    "45 Knowledge Avenue",
    "Dubai",
    "UAE"
)

delivery1 = Delivery(
    "DEL123456789",
    "DN-2025-001",
    "January 25, 2025",
    "Courier",
    "",
    "7 kg"
)

items1 = [
    Item("ITM001", "Wireless Keyboard", 1, 100.00, 100.00),
    Item("ITM002", "Wireless Mouse & Pad Set", 1, 75.00, 75.00),
    Item("ITM003", "Laptop Cooling Pad", 1, 120.00, 120.00),
    Item("ITM004", "Camera Lock", 3, 15.00, 45.00)
]
items2 = [
    Item("ITM005", "Wireless Keyboard", 1, 100.00, 100.00),
    Item("ITM006", "Wireless Mouse & Pad Set", 1, 75.00, 75.00),
    Item("ITM007", "Laptop Cooling Pad", 1, 120.00, 120.00),
    Item("ITM008", "Camera Lock", 3, 15.00, 45.00)
]


invoice1 = Invoice(270.00, 13.50, 283.50, "AED")
invoice2 = Invoice(290.00, 15.90, 120.50, "AED")

# Second set of objects (sample alternative)
recipient2 = Customer(
    "John Doe",
    "john.doe@example.com",
    "100 Tech Street",
    "Abu Dhabi",
    "UAE"
)

delivery2 = Delivery(
    "DEL987654321",
    "DN-2025-002",
    "February 1, 2025",
    "Standard",
    "30x20x15 cm",
    "5 kg"
)

# Generate delivery note for first order
def generate_delivery_note(recipient, delivery, items1, invoice):
    print("Customer Details:")
    print(f"Name: {recipient.get_name()}")
    print(f"Contact: {recipient.get_contact()}")
    print(f"Delivery Address: {recipient.format_address()}\n")

    print("Delivery Information:")
    print(f"Order Number: {delivery.get_order_num()}")
    print(f"Reference Number: {delivery.get_ref_num()}")
    print(f"Delivery Date: {delivery.get_date()}")
    print(f"Delivery Method: {delivery.get_method()}")
    print(f"Total Weight: {delivery.get_weight()}\n")

    print("Summary of Items Delivered:")
    print("| Item Code | Description                   | Quantity | Unit Price | Total Price |")
    for item in items1:
        print(f"| {item.get_code()} | {item.get_desc():<25} | {item.get_qty():>8} | {item.get_unit_price():>10.2f} | {item.get_total_price():>11.2f} |")

    print("\nFinancial Information:")
    print(f"Subtotal: {invoice.get_currency()} {invoice.get_subtotal():.2f}")
    print(f"Taxes and Fees: {invoice.get_currency()} {invoice.get_taxes():.2f}")
    print(f"Total Charges: {invoice.get_currency()} {invoice.get_total_charges():.2f}")

# Display the delivery note for the first order
generate_delivery_note(recipient1, delivery1, items1, invoice1)
