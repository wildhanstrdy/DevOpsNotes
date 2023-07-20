**Quick Initial Settings to Set Up AWS**

After create an account you can follow this checklist to make sure several things:
- [ ] Integrate your root account with your 2Auth Apps.
- [ ] Create IAM user instead of using root user for your daily use.
  - [ ] Change your password
  - [ ] Create account Alias to make login easier. Later on this alias will be a url to your IAM to logged in.
- [ ] Go to Billing menu then :
  - [ ] Go to Billing->Billing Preferences->Invoice Delivery Preference->Edit and check PDF invoices delivery by email.
  - [ ] Alert Preferences->Edit your free tier email.
- [ ] Create Billing Alert to maintain your billings in `Cloud Watch` Service.
  - [ ] Create Alarm-> Select Billing-> Estimated Charges-> Select currency for IDR
  - [ ] Put the limit on your alarm. For example it will alert you when it exceed 5$.
  - [ ] Enable your SNS(Simple Notification System) also create new topic for that.
- [ ] Create E2C virtual computer in AWS if you need a virtual computer.
- [ ] Create AWS Free Certificate
  - [ ] Put your domain name i.e. *.yourdomain.com (to support all of the sub domain as well).
  - [ ] Select DNS Validation
  - [ ] Let use the default value for the key algorithm
  - [ ] Then Click Request
  - [ ] Open the Certificate after its created. You will see `CNAME name` and `CNAME value`.
  - [ ] Go to your domain provider and manage your domain.
  - [ ] Go to the DNS settings and add a new record.
  - [ ] Choose `CNAME` type.
  - [ ] Put the `CNAME name` from AWS to your domain and please remove the domain name and `.` just fill the name.
  - [ ] Put the `CNAME value` from AWS and remove the last `.`(period) value. Then Save it. 
