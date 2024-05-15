---
uid: Connector_help_Telenor_Service_Overview_Manager
---

# Telenor Service Overview Manager

The Telenor Service Overview Manager allows operators to monitor the status of services at different headends.

This Service Overview Manager keeps a list of all the services at different headends and displays the summary of the statuses. It also allows operators to configure the probes in the headends and check if there are changes between the current setup and a desired setup. These changes can be uploaded to specific devices.

Root Cause Analysis is automatically configured on the services when a headend is selected. Two different chains will be generated:

- **TelenorSOM_SVCChain**
- **TelenorSOM_RHEChain**

The database of the Service Overview Manager contains a service monitoring schedule. That schedule tells the Service Overview Manager not only which services to monitor, but also when services are on air. As such, as soon as this schedule has been read into memory, the Service Overview Manager will disregard any alarm associated with a service that does not have to be monitored or that is not on air when the alarm is raised.

## About

### Version Info

| Range | Key Features | Based on | System Impact |
|--|--|--|--|
| 1.0.0.x [Obsolete] | Initial version. | - | - |
| 1.0.1.x [SLC Main] | Removed all BridgeTech references and functionality from the connector | 1.0.0.30 | All BridgeTech data tables have been removed. |

## Configuration

### Connections

This connector uses a virtual connection and does not require any input during element creation.

### Database connection

In order to retrieve the list of services, a connection has to be created with a database. The **Host**, **UserName** and **Password** can be set on the **Configuration** page.

### Time zone setup

In order to use the monitoring schedule, time settings have to be configured. These settings can be found on the **Configuration** page.

### User for RCA generation

In order to automatically generate the RCA, a DataMiner user and password need to be configured, with the right to configure RCAs. This needs to be done on the **Configuration** page.

## Usage \[version 1.0.0.x\]

### Service Page

Displays the list of the services found on the headends after reading the database. Also allows you to configure the Main Headend used in the RCA.

### CHE Page

Displays the list of the CHE services with the alarm level.

### RHE Page

Displays the list of the RHE services with the alarm level.

### Probe CHE Page

Displays the list of probes of the CHE services.

### Probe RHE Page

Displays the list of probes of the RHE services.

Via the **Add Probe** page button, you can add probes.

### Service/Probe/CHE Page

Displays a summary of the CHE services and their probes.

### Service/Probe/RHE Page

Displays a summary of the RHE services and their probes.

### Service/RHE Page

Displays a list of the RHE services and their status as they are found in the system. Also allows you to configure the Main Headend used in the RCA.

### Configuration Page

Allows you to configure the **Database**, **RCA** and **Time** settings, and perform the following actions:

- **Read Database**
- **Force RCA**
- **Read File**

Via **Configuration File**, you can read a probe configuration file into memory and compare it to the current configuration of a number of probes.

### Probe Configuration

Via the **Probe List** page button, you can define the probes that need to be configured.

You can compare the current configuration with a new one in the database. To compare a new configuration in the database with the current one on the probe, click the **Compare DB** button. This will result in a list of found changes in the **Config Difference** table. The **Changed Probes** table will contain a list of probes that have a different configuration than the one in the database.

Comparing can also be done from a file, in which case you should use the **Compare File** button. You can find the content of the file via the **File Content** page button.

Applying the configuration from the database can be done with the **Apply db conf.** button. To implement all listed changes to the probe, a configuration file generated by the database will be uploaded to it. Clicking the **Apply config** button will upload the configuration file selected on the Compare File page to the selected probe.

### Element Info

Displays all of the configured elements in the DataMiner System.

## Usage \[version 1.0.1.x\]

The information above is still valid for this range. However, BridgeTech tables and information have been removed (mainly on the "Probe Configuration" page).

## Notes

This connector should be used in DataMiner Cube with Visio files.