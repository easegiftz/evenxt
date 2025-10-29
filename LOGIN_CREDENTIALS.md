# EventNest Platform - Login Credentials & Access Guide

## 🔐 **System Overview**
The EventNest platform implements comprehensive role-based access control with multi-factor authentication. Each user type has specific security requirements and dashboard access levels.

---

## 👨‍💼 **ADMIN LOGIN DETAILS**

### **Security Level:** MAXIMUM (RED)
- **URL:** `/auth/admin`
- **Email:** `admin@eventnest.com`
- **Password:** `Admin@123`
- **Employee ID:** `ADM-001`
- **Security Features:**
  - ✅ CAPTCHA Required
  - ✅ OTP Authentication (SMS/Email)
  - ✅ Maximum Login Attempts: 3
  - ✅ Session Timeout: 30 minutes
  - ✅ Security Audit Logging

### **Demo OTP Numbers:**
- **Phone:** `+91-98765-43210`
- **Email:** `admin@eventnest.com`
- **OTP Code:** `123456` (Auto-generated in console)

### **Admin Dashboard Access:**
- Full system control and management
- Department analytics and user management
- Security monitoring dashboard
- Footer management system
- Vendor approval/removal controls
- Financial reports and analytics

---

## 👷‍♂️ **EMPLOYEE LOGIN DETAILS**

### **Security Level:** HIGH (ORANGE)
- **URL:** `/auth/employee`
- **Email:** `employee@eventnest.com`
- **Password:** `Emp@123`
- **Employee ID:** `EMP-001`
- **Security Features:**
  - ✅ CAPTCHA Required
  - ✅ OTP Authentication
  - ✅ Maximum Login Attempts: 5
  - ✅ Session Timeout: 60 minutes

### **Demo Employee Accounts:**
```
Support Team:
- Email: support@eventnest.com
- Employee ID: EMP-SUP-001
- Password: Support@123

Operations Team:
- Email: operations@eventnest.com  
- Employee ID: EMP-OPS-001
- Password: Operations@123

Finance Team:
- Email: finance@eventnest.com
- Employee ID: EMP-FIN-001
- Password: Finance@123
```

### **Employee Dashboard Access:**
- Event management and booking support
- Customer service tools
- Vendor management interface
- Department-specific operational tools
- Limited analytics access

---

## 🏢 **SUPPLIER LOGIN DETAILS**

### **Security Level:** MEDIUM (PURPLE)
- **URL:** `/auth/supplier`
- **Email:** `supplier@eventnest.com`
- **Password:** `Supplier@123`
- **Business Name:** `Premium Event Services`
- **Security Features:**
  - ✅ 2FA Authentication
  - ✅ Maximum Login Attempts: 5
  - ✅ Session Timeout: 120 minutes
  - ✅ Account Verification Required

### **Demo Supplier Categories:**
```
Catering Services:
- Email: catering@premiumfood.com
- Password: Catering@123
- Business: Premium Catering Co.

Photography:
- Email: photo@snapmoments.com
- Password: Photo@123
- Business: Snap Moments Photography

Event Decoration:
- Email: decor@eventdecor.com
- Password: Decor@123
- Business: Creative Event Decorators

Audio/Visual:
- Email: av@techsound.com
- Password: AV@123
- Business: TechSound AV Solutions
```

### **Supplier Dashboard Access:**
- Service portfolio management
- Booking requests and calendar
- Payment tracking and invoicing
- Customer communication tools
- Performance analytics

---

## 👥 **CUSTOMER LOGIN DETAILS**

### **Security Level:** LOW (BLUE)
- **URL:** `/auth/customer`
- **Email:** `customer@example.com`
- **Password:** `Customer@123`
- **Security Features:**
  - ❌ No CAPTCHA Required
  - ❌ No OTP Required
  - ✅ Maximum Login Attempts: 10
  - ✅ Session Timeout: 240 minutes

### **Demo Customer Accounts:**
```
Individual Customer:
- Email: john.doe@email.com
- Password: Customer@123
- Name: John Doe
- Phone: +91-98765-12345

Corporate Customer:
- Email: events@techcorp.com
- Password: Corporate@123
- Company: TechCorp Solutions
- Contact: Sarah Johnson

Wedding Customer:
- Email: bride@wedding.com
- Password: Wedding@123
- Event Type: Wedding Planning
- Contact: Emily & Michael
```

### **Customer Dashboard Access:**
- Event planning and booking interface
- Vendor discovery and comparison
- Booking history and status tracking
- Payment management
- Review and rating system

---

## 🔧 **QUICK ACCESS NAVIGATION**

### **Authentication URLs:**
- **Admin Portal:** `http://localhost:8080/auth/admin`
- **Employee Portal:** `http://localhost:8080/auth/employee`
- **Supplier Portal:** `http://localhost:8080/auth/supplier`
- **Customer Portal:** `http://localhost:8080/auth/customer`

### **Dashboard URLs:**
- **Admin Dashboard:** `http://localhost:8080/dashboard/admin`
- **Employee Dashboard:** `http://localhost:8080/dashboard/employee`
- **Supplier Dashboard:** `http://localhost:8080/dashboard/supplier`
- **Customer Dashboard:** `http://localhost:8080/dashboard/customer`

---

## 🛡️ **SECURITY FEATURES BY USER TYPE**

| Feature | Admin | Employee | Supplier | Customer |
|---------|-------|----------|----------|----------|
| CAPTCHA | ✅ | ✅ | ❌ | ❌ |
| OTP/SMS | ✅ | ✅ | ❌ | ❌ |
| 2FA | ❌ | ❌ | ✅ | ❌ |
| Max Attempts | 3 | 5 | 5 | 10 |
| Session (min) | 30 | 60 | 120 | 240 |
| Audit Log | ✅ | ✅ | ✅ | ❌ |

---

## 📱 **OTP/SMS TESTING**

### **Development Console Logs:**
When testing OTP functionality, check the browser console for generated codes:
```
SMS OTP sent to +91-98765-43210: 123456
Email OTP sent to admin@eventnest.com: 789012
```

### **Demo Phone Numbers:**
- Admin: `+91-98765-43210`
- Employee: `+91-98765-43211`
- Supplier: `+91-98765-43212`

---

## 🚀 **GETTING STARTED**

1. **Start the Application:**
   ```bash
   npm run dev
   # App runs on http://localhost:8080
   ```

2. **Choose Your Access Level:**
   - Navigate to the appropriate authentication portal
   - Use the provided demo credentials
   - Follow the multi-step authentication process

3. **Security Testing:**
   - Test OTP flow with demo numbers
   - Verify CAPTCHA integration
   - Check session timeout behavior
   - Test account lockout mechanisms

---

## 📞 **SUPPORT & TROUBLESHOOTING**

### **Common Issues:**
- **Account Locked:** Wait 15 minutes or contact admin
- **OTP Not Received:** Check console logs for demo codes
- **Session Expired:** Re-authenticate with credentials
- **Access Denied:** Verify user type and permissions

### **Development Notes:**
- All passwords follow the pattern: `[UserType]@123`
- OTP codes are logged to browser console in development
- CAPTCHA is simulated with checkbox in demo mode
- 2FA uses backup codes in development environment

---

*This document contains demonstration credentials for development and testing purposes only. In production, implement proper user registration, secure password policies, and real SMS/Email services.*
