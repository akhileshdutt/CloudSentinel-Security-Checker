
<body>
  <h1>CloudSentinel Security Checker</h1>

  <p>
    <strong>CloudSentinel Security Checker</strong> is an automated cloud-security auditing tool designed to
    monitor and enforce essential security best practices across single or multi-account AWS
    environments.
  </p>
  <p>
    It performs daily checks on IAM users and root accounts to help you maintain a secure AWS posture by:
  </p>
  <ul>
    <li>Identifying old or stale API keys</li>
    <li>Detecting users who have not changed their passwords for a long time</li>
    <li>Checking which users do not have MFA enabled</li>
  </ul>
  <p>
    Additionally, it can automatically:
  </p>
  <ul>
    <li>Set a Service Control Policy (SCP) that denies root access on every child account in your organization</li>
    <li>Configure a secure account password policy</li>
  </ul>

  <h2>✨ Enhancements in CloudSentinel (This Fork)</h2>
  <p>
    This project is based on the original <code>aws-basic-security-checker</code> and customized under the
    name <strong>CloudSentinel Security Checker</strong> to make it easier to understand, set up, and extend.
  </p>
  <p>Key improvements:</p>
  <ul>
    <li>Clearer documentation and step-by-step setup instructions</li>
    <li>More descriptive project naming and structure for better readability</li>
    <li>Improved explanation of how AWS resources and Lambda checks work together</li>
    <li>Cleaner separation between configuration, infrastructure, and logic for future extensions</li>
  </ul>
  <p>
    <em>Note:</em> For compatibility, some internal Pulumi project identifiers still use the original
    <code>aws-basic-security-checker</code> name. Command examples below reflect that.
  </p>

  <h2>Installation</h2>

  <h3>Prerequisites</h3>
  <p>You will need:</p>
  <ul>
    <li>
      <strong>Pulumi</strong> (tested with v3.27.0) – used as Infrastructure as Code to create AWS resources.<br />
      Install Pulumi using:
      <pre><code>curl -sSL https://get.pulumi.com | sh</code></pre>
    </li>
    <li><strong>Node.js</strong> (tested with v12.18.3 and v17.8.0)</li>
    <li><strong>npm</strong> (tested with 6.14.8 and 8.5.5)</li>
    <li><strong>git</strong> – optional, used to download the source code</li>
    <li><strong>AWS credentials</strong> with permissions to create all required resources on the management (master) account</li>
    <li>
      <strong>Verified email or domain in AWS SES</strong><br />
      You should verify the admin email and each user's email, or preferably verify a domain.
    </li>
    <li>
      Child accounts in your AWS Organization must have the
      <code>OrganizationAccountAccessRole</code> which can be assumed from the management (master) account.
      This ro
