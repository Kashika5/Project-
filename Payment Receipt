pip install reportlab

from reportlab.lib.pagesizes import letter
from reportlab.pdfgen import canvas

def create_payment_receipt(customer_name, amount_paid, payment_date):
    file_name = f"payment_receipt_{customer_name.replace(' ', '_')}.pdf"
    
    c = canvas.Canvas(file_name, pagesize=letter)
    
    c.drawString(100, 750, "Payment Receipt")
    
    c.drawString(100, 700, f"Customer: {customer_name}")
    c.drawString(100, 675, f"Amount Paid: ${amount_paid}")
    c.drawString(100, 650, f"Payment Date: {payment_date}")
    
    c.save()
    
    print(f"Payment receipt saved as {file_name}")

def main():
    customer_name = input("Enter customer's name: ")
    amount_paid = input("Enter amount paid: ")
    payment_date = input("Enter payment date: ")
    
    create_payment_receipt(customer_name, amount_paid, payment_date)

if __name__ == "__main__":
    main()
