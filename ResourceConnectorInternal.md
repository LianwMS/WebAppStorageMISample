# Connection Overview
Connection is the key concept in the resource model of Azure Resource Connector. In Azure Resource Connector, a Connection is an abstraction of the link between two services. The following properties are defined on Connection.

| Property | Description |
|--------|-----------|
| Name | The name of the connection |
| Source Type | The source service instance type. E.g., Azure Web App Service, Azure Spring Cloud Service etc |
| Resource Type | The target resource type. E.g., Azure PostgreSQL, Azure Storage etc |
| Client Type | {Need Define Clearly} |
| Authentication Type | The authentication type used of connection. E.g., connection string, system assigned managed identity etc |

You can create multiple connections from one source service instance if your instance needs to connect multiple target resource. While the same targe resource can be connected from multiple source instances. Azure Resource Connector will manage all connections in the properties of their source instance. That’s means you can create, get, update, and delete the connections in portal or CLI command of their source service instance. 

The connection support cross subscription or tenant. Source and target service can belong to different subscription or tenant. 

# Create or Update Connection
Azure Resource Connector will do multiple steps while creating or updating a connection, including:
* Configure target resource network and firewall
* Configure connection information on source resource
* Configure authentication information on source and target if needed
* Create or update connection support rollback if failure. 

Since creating and updating a connection contains multiple steps. If one step fail, Azure Resource Connector will rollback previous steps to keep the initial settings in source and target instances.

# Validate Connection 
The following items will be checked while validating the connection:
* Validate whether source and target resources exist
* Validate target resource network and firewall
* Validate connection information on source resource
* Validate authentication information on source and target if needed

# Delete Connection
The connection information on source resource will be deleted when deleting connection. 
