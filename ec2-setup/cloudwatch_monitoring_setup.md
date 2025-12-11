# CloudWatch Monitoring (Enabled from EC2 Console)

No agent installation commands were used.

Instead, CloudWatch was activated directly from the EC2 Dashboard.

## Steps
1. Go to EC2 → Instances
2. Select your instance
3. Click “Monitoring” tab
4. Click “Manage detailed monitoring”
5. AWS automatically:
   - Installs CloudWatch Agent
   - Sends metrics
   - Uses the IAM Role you attached

Required IAM role:
- CloudWatchAgentServerPolicy
