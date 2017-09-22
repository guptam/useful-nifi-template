# useful-nifi-template
Useful NiFi Templates

## 1. Azure Resource Monitoring using NiFi
This will create a flow that periodically fetches details of all your Azure Resources (within your subscription), and sends and out an email. For VMs, it also identifies their Power State. Can be used for monitoring, mainitaining a log of all your usage, advance alerting, or any other use case you can think of (maintenance, cost control etc.).

#### Instructions:
Before running/scheduling this flow:
* Install Azure CLI
* Do Azure login with Oauth "az login"

#### Notes:
- Filename: Azure-Resources-Monitor-Alert.xml
- This will work only on windows. For Linux, change cmd to sh.
- Will generate report for one subscription only.
- Instead of sending an email, you can maintain entire log in a datastore.
- In "Enrich with metadata" processor, add any Resource Type specific logic (for instance - Azure VM or SQL Database)
- All Data flows in JSON format

