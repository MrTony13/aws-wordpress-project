# Common Errors and Fixes

❌ Installed WordPress in /home  
✔ FIX: Always install in /var/www/html

❌ Restarted Apache using "service"  
✔ FIX: Correct command:
   sudo systemctl restart httpd

❌ CloudFront/Route53 not working  
✔ FIX: They are not used in this project

❌ CloudWatch manual config confusion  
✔ FIX: CloudWatch was enabled from EC2 Monitoring tab
