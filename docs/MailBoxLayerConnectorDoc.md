## About the connector
Mailboxlayer simple and powerful API offering instant email address validation & verification via syntax checks, typo and spelling checks, SMTP checks, free and disposable provider filtering.This connector facilitates the automated operations email verification and check email validation.
<p>This document provides information about the Mailboxlayer Connector, which facilitates automated interactions, with a Mailboxlayer server using FortiSOAR&trade; playbooks. Add the Mailboxlayer Connector as a step in FortiSOAR&trade; playbooks and perform automated operations with Mailboxlayer.</p>

### Version information

Connector Version: 1.0.0


Authored By: spryIQ.co

Certified: No
## Installing the connector
<p>From FortiSOAR&trade; 5.0.0 onwards, use the <strong>Connector Store</strong> to install the connector. For the detailed procedure to install a connector, click <a href="https://docs.fortinet.com/document/fortisoar/0.0.0/installing-a-connector/1/installing-a-connector" target="_top">here</a>.<br>You can also use the following <code>yum</code> command as a root user to install connectors from an SSH session:</p>
`yum install cyops-connector-mailboxlayer`

## Prerequisites to configuring the connector
- You must have the URL of Mailboxlayer server to which you will connect and perform automated operations and credentials to access that server.
- The FortiSOAR&trade; server should have outbound connectivity to port 443 on the Mailboxlayer server.

## Minimum Permissions Required
- N/A

## Configuring the connector
For the procedure to configure a connector, click [here](https://docs.fortinet.com/document/fortisoar/0.0.0/configuring-a-connector/1/configuring-a-connector)
### Configuration parameters
<p>In FortiSOAR&trade;, on the Connectors page, click the <strong>Mailboxlayer</strong> connector row (if you are in the <strong>Grid</strong> view on the Connectors page) and in the <strong>Configurations&nbsp;</strong> tab enter the required configuration details:&nbsp;</p>
<table border=1><thead><tr><th>Parameter<br></th><th>Description<br></th></tr></thead><tbody><tr><td>Server URL<br></td><td>URL of the Threat Intelligence Platform connector to access the connector website.<br>
<tr><td>API key<br></td><td>Provide API token, used for user authentication.<br>
</tbody></table>

## Actions supported by the connector
The following automated operations can be included in playbooks and you can also use the annotations to access operations from FortiSOAR&trade; release 4.10.0 and onwards:
<table border=1><thead><tr><th>Function<br></th><th>Description<br></th><th>Annotation and Category<br></th></tr></thead><tbody><tr><td>Get Email Verification Detail<br></td><td>Retrieved data for the given email address.<br></td><td>email_verification_details <br/>Investigation<br></td></tr>
</tbody></table>

### operation: Get Email Verification Detail
#### Input parameters
<table border=1><thead><tr><th>Parameter<br></th><th>Description<br></th></tr></thead><tbody><tr><td>Email Address<br></td><td>Required email address whose email Validates data needs to be retrieved.<br>
</td></tr></tbody></table>

#### Output
The output contains the following populated JSON schema:
<code><br>{
</code><code><br>&nbsp;&nbsp;&nbsp;&nbsp;    "email": "",
</code><code><br>&nbsp;&nbsp;&nbsp;&nbsp;    "did_you_mean": "",
</code><code><br>&nbsp;&nbsp;&nbsp;&nbsp;    "user": "",
</code><code><br>&nbsp;&nbsp;&nbsp;&nbsp;    "domain": "",
</code><code><br>&nbsp;&nbsp;&nbsp;&nbsp;    "format_valid": "",
</code><code><br>&nbsp;&nbsp;&nbsp;&nbsp;    "mx_found": "",
</code><code><br>&nbsp;&nbsp;&nbsp;&nbsp;    "smtp_check": "",
</code><code><br>&nbsp;&nbsp;&nbsp;&nbsp;    "catch_all": "",
</code><code><br>&nbsp;&nbsp;&nbsp;&nbsp;    "role": "",
</code><code><br>&nbsp;&nbsp;&nbsp;&nbsp;    "disposable": "",
</code><code><br>&nbsp;&nbsp;&nbsp;&nbsp;    "free": "",
</code><code><br>&nbsp;&nbsp;&nbsp;&nbsp;    "score": ""
</code><code><br>}</code>
## Included playbooks
The `Sample - mailboxlayer - 1.0.0` playbook collection comes bundled with the Mailboxlayer connector. These playbooks contain steps using which you can perform all supported actions. You can see bundled playbooks in the **Automation** > **Playbooks** section in FortiSOAR<sup>TM</sup> after importing the Mailboxlayer connector.

- Get Email Verification Detail

**Note**: If you are planning to use any of the sample playbooks in your environment, ensure that you clone those playbooks and move them to a different collection, since the sample playbook collection gets deleted during connector upgrade and delete.
