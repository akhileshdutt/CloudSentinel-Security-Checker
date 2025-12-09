<h1>CloudSentinel Security Checker</h1>

<p>
  <strong>CloudSentinel Security Checker</strong> is an automated cloud security auditing tool designed to 
  monitor, detect, and correct common security weaknesses inside AWS organizations. 
  The tool focuses on strengthening IAM hygiene, enforcing MFA usage, auditing access keys, 
  and applying foundational security policies across multiple AWS accounts.
</p>

<p>
  In modern cloud environments, misconfigurations are one of the biggest causes of security breaches. 
  CloudSentinel helps organizations maintain a secure baseline by performing <strong>daily automated checks</strong> 
  across all AWS accounts and notifying both administrators and users about security issues that require attention.
</p>

<p>
  This project is ideal for demonstrating understanding of <strong>cloud security, IAM best practices, 
  automation with AWS Lambda, Pulumi infrastructure-as-code, and multi-account governance</strong>.
</p>

<h2>✨ What CloudSentinel Does</h2>
<p>CloudSentinel performs continuous security validation across your AWS environment. It checks for:</p>

<ul>
  <li>IAM users with <strong>old or stale access keys</strong></li>
  <li>Users who have <strong>not changed passwords</strong> for a long time</li>
  <li>Users who do <strong>not have MFA enabled</strong></li>
  <li>Root users with missing security controls</li>
  <li>Accounts that do not meet the password policy requirements</li>
</ul>

<p>Additionally, it can automatically apply:</p>
<ul>
  <li>A <strong>Service Control Policy (SCP)</strong> that restricts dangerous root actions</li>
  <li>A secure <strong>password policy</strong> for every AWS account</li>
  <li>IAM group assignments to enforce MFA setup</li>
</ul>

<h2>🚀 How CloudSentinel Works</h2>

<p>
  CloudSentinel deploys a series of AWS resources across the management account and child accounts 
  using Pulumi (Infrastructure as Code). Once deployed, the system becomes <strong>fully automated</strong>.
</p>

<h3>Daily Automated Security Scans</h3>
<p>
  Every day at <strong>10 AM UTC</strong>, a set of AWS Lambda functions run to perform checks such as:
</p>
<ul>
  <li>Verifying MFA status for root and user accounts</li>
  <li>Checking access key age (90-day and 120-day thresholds)</li>
  <li>Enforcing login restrictions for non-compliant users</li>
  <li>Sending email notifications to users and administrators</li>
  <li>Automatically correcting misconfigurations (if not in dry-run mode)</li>
</ul>

<p>
  These Lambda functions assume a cross-account role to inspect IAM resources in every AWS account
  within the organization, making CloudSentinel suitable for <strong>large-scale multi-account environments</strong>.
</p>

<h2>✨ Enhancements Added in CloudSentinel (My Contributions)</h2>
<ul>
  <li>Renamed and restructured the project for better clarity and professional presentation</li>
  <li>Improved explanations of the workflow and architecture</li>
  <li>Enhanced documentation to simplify setup for new users</li>
  <li>Added more intuitive naming and project organization for easier extension</li>
  <li>Defined future scope for additional AWS checks (S3, SG misconfigurations, IAM role audits)</li>
</ul>

<h2>📌 Why This Project Matters</h2>
<p>
  CloudSentinel demonstrates strong understanding of:
</p>
<ul>
  <li><strong>AWS IAM Security</strong></li>
  <li><strong>Cloud Misconfiguration Detection</strong></li>
  <li><strong>Automation using AWS Lambda</strong></li>
  <li><strong>Pulumi & Infrastructure as Code (IaC)</strong></li>
  <li><strong>Multi-account AWS governance</strong></li>
</ul>

<p>
  Having such a project on your resume shows you can think like a security engineer, understand cloud security risks,
  automate governance tasks, and implement secure multi-account practices — which are highly valued in cybersecurity roles.
</p>
