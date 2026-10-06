Auto Ticket Classification using Flow Designer

📌 Project Overview

Auto Ticket Classification using Flow Designer is a ServiceNow-based automation project designed for a school IT helpdesk.

The system automatically classifies IT support tickets based on keywords in the ticket's Short Description. It assigns the appropriate Category and Subcategory without manual intervention and sends an email notification to the caller.

The project is implemented using ServiceNow Flow Designer as a no-code solution.

🎯 Objectives

- Automatically classify IT incidents when they are created.
- Reduce manual work for IT support staff.
- Improve ticket routing efficiency.
- Maintain consistent ticket classification.
- Send automatic email confirmation to the caller.
- Provide an easy-to-maintain and scalable solution.

🛠️ Technologies Used

- ServiceNow
- Flow Designer
- Custom Tables
- ServiceNow Update Sets
- Email Notifications
- Choice & Reference Fields
- No-Code Automation

⚙️ How It Works

1. A student or teacher creates an IT support ticket.
2. The ticket contains a Caller and Short Description.
3. Flow Designer is triggered when the record is created.
4. The flow checks the Short Description for predefined keywords.
5. Category and Subcategory are automatically assigned.
6. An email confirmation is sent to the caller.

🔄 Ticket Classification Logic

Keyword / Issue| Category| Subcategory
WiFi / Network| Network| Wi-Fi
Projector| Hardware| Projector
Password / Login| Access| Forgot Password
Slow / Hanging| Performance| Slow Computer

The classification logic is implemented through Flow Designer conditions and Update Record actions.

🗂️ Ticket Fields

The custom Incident Workflow table contains fields such as:

- Number
- Caller
- Category
- Subcategory
- Short Description
- Description
- State
- Assigned Group
- Assigned To

Category, Subcategory, and State use choice fields, while Caller, Assigned Group, and Assigned To use reference fields.

🔗 Category & Subcategory Dependency

The Subcategory field is configured as a dependent field of Category.

Examples:

- Network → Wi-Fi
- Hardware → Projector
- Access → Forgot Password
- Performance → Slow Computer

This ensures that the available subcategory is based on the selected category.

📧 Email Notification

After ticket classification, Flow Designer sends an email notification to the caller.

Subject:
"Your Request for the issue has been submitted."

This provides immediate confirmation that the support request has been created.

🧪 Testing

Test Case 1 – Wi-Fi Issue

Short Description:
"WiFi not working in library"

Expected Result:

- Category → Network
- Subcategory → WiFi
- Email → Sent to caller

Test Case 2 – Projector Issue

Short Description:
"Projector not turning on"

Expected Result:

- Category → Hardware
- Subcategory → Projector
- Email → Sent to caller

📦 Deployment

The project configuration is maintained using a ServiceNow Update Set.

After development and testing:

1. Change the Update Set state from In Progress to Complete.
2. Save the Update Set.
3. Export the Update Set as XML.
4. The XML file can be transferred and used in another ServiceNow environment.

✅ Benefits

- Reduces manual ticket classification.
- Improves ticket routing.
- Provides consistent categorization.
- Reduces human errors.
- Automatically notifies users.
- Easy to maintain.
- Scalable for future requirements.
- Does not require complex scripting or machine learning.

🚀 Future Enhancements

The project can be extended with:

- Automatic assignment to support groups
- SLA tracking
- Priority prediction
- Advanced ticket routing
- Predictive intelligence
- Additional issue categories

📌 Conclusion

This project demonstrates how ServiceNow Flow Designer can be used to build a scalable and maintainable IT helpdesk automation solution. It automatically classifies tickets, maintains structured data, and improves communication through email notifications.
