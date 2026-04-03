CRM Application for Banquet Hall               
Booking (Salesforce-Based Solution) 
1. Understand the Goal: 
You need to build a Salesforce CRM System for Banquet Hall Booking 
that: - Automates booking and event management - Tracks hall availability in real-time - Improves customer experience - Manages event planning efficiently - Ensures data security - Provides reports & analytics 
2. Design the Data Model: 
Core Objects: - Customer (Account / Contact) - Banquet Hall - Booking - Booking Line Item (Services/Packages) - Event - Inventory (optional – décor, equipment) - Vendor (optional – catering, decoration) 
Relationships: - One Customer → Many Bookings - One Booking → One Event - One Booking → Many Services - One Hall → Many Bookings 
Example: 
Booking Object: - Booking ID 
- Event Date - Status - Total Amount 
Booking Line Item: - Service Name - Quantity - Price 
3. Create Fields: 
Booking Object: - Booking Status (Inquiry, Confirmed, Completed, Cancelled) - Event Date - Number of Guests - Total Amount (Formula) 
Banquet Hall Object: - Capacity - Availability Status - Price per Event 
4. Formula Fields: - Total Amount = Quantity × Price - Availability Check = IF(Hall_Booked = TRUE, "Unavailable", "Available") 
5. Validation Rules: - Guests ≤ 0 → Error - Event Date < Today → Error 
6. Automation: 
When Booking is Created: - Create task 
- Send email 
When Confirmed: - Block hall - Assign manager 
7.Apex: 
Trigger on Booking to check availability and update hall. 
8.SecurityRoles: - Admin - Sales Executive - Event Manager 
9. Reports & Dashboard: - Bookings by Status - Revenue - Events 
10.Use Case Flow: 
Inquiry → Booking → Availability Check → Confirmation → Planning → Event → Reports 
11.Submission: - Data Model - Fields - Automation - Apex - Security - Reports 
12.Author: 
Rachel R 
Parasuraman E 
Divakar R 
Sathyanarayanan S 
Theerthana R
