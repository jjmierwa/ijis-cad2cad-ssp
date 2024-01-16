# Integrated Justice Information System (IJIS) Institute <br />CAD-to-CAD (C2C) Interoperability Service Specification Package (SSP)
A Service Specification Package (SSP) for IJIS CAD to CAD 

|-------|-----|
|Release|1.0.2|
|URI||
|Creation Date:06/08/2022|
|Modified Date: 08/30/22|
|Status: Draft|

## Description
This service specifcation enables the exchange between:
- Computer Aided Dispatch (CAD) systems through automating the process of sending messages and notifications from subscribers and notifiers by facilitating the interactions inside a public-safety answering point (PSAP), between PSAPs, and between PSAPs and other entities, involved in sending and receiving, Emergency Incident Data Object (EIDO) message and CAD-to-CAD (C2C) Interoperability message, payloads.

This service specification supports the initiative known as the CAD-to-CAD (C2C) Interoperability Pilot Project to be set up across two pilot sites with 5 CAD-to-CAD User Stories or use cases for this project: Out of Jurisdiction Call, Active Shooter, Major Hurricane Across Multiple Counties, Pursuit/Car Chase Through Multiple Jurisdictions, Hazmat Incident Impacting Multiple Jurisdictions with Injuries and Requires Evacuation. 

[Link Text](https://mcp911gov.sharepoint.com/:x:/r/sites/DataIntegrationServices-IJISCADtoCADInteroperability/_layouts/15/doc2.aspx?sourcedoc=%7B83120108-89DF-43C9-BF1A-F97A3B8314DF%7D&file=IJIS%20ToDos.xlsx&action=default&mobileredirect=true)!

The Integrated Justice Information System (IJIS) Institutewill implement a series of exchanges in a laboratory development environment to validate the standards supporting interoperability among the nation's Computer Aided Dispatch (CAD) systems. This initiative is known as the CAD-to-CAD (C2C) Interoperability Pilot Project. It will be comprised of web socket services for transferring emergency incident data between CAD systems using the Emergency Incident Data Object (EIDO) (2) and the EIDO Conveyance (3) specifications as the basis.

The EIDO Conveyance defines the behavior for transferring incident data between CAD systems using a series of predefined operations. The behavior and implementation for this will be using five initial CAD-to-CAD User Stories or use cases for this project: Out of Jurisdiction Call, Active Shooter, Major Hurricane Across Multiple Counties, Pursuit/Car Chase Through Multiple Jurisdictions, Hazmat Incident Impacting Multiple Jurisdictions with Injuries and Requires Evacuation (4) (5) (6).

Each use case/user story will be validated with messages exchanged between CAD systems. Each message will be conformant to the operational guidelines, described elsewhere in the document, allowing for specific payload information to be communicated. Benefits to standardizing the sharing of CAD incident information may include improved communication between government agencies and the alignment of business and information technology (IT) requirements to achieve interoperability among organizations. To accomplish business-IT alignment, a stable approach must be defined to identify, describe, and package services and their interactions in many environments that span multiple levels of government and organizations. Overall, this initiative will help to improve interagency collaboration, reduce response times, and ultimately improve public safety outcomes by providing data for more informed decisions in responding to incidents. IJIS has adopted an information-sharing architecture based on the concepts of Service-Oriented Architecture (SOA) and guidelines provided by the US Department of Justice's Global Justice Advisory Committee (Global). Global supports the Global Reference Architecture (GRA). The format of this specification is established by the _Global Reference Architecture Service Specification Guideline, version 1.2.0_ (1)_._

The CAD-to-CAD Service enables the process of sending messages and notifications between subscribers and notifiers by facilitating the interactions inside a public-safety answering point (PSAP), among multiple PSAPs, and between a PSAP and other entities. This depends on the characteristics and requirements set by the use case scenarios which will trigger a variety of operations and responses from this service. Routing information supplied in the message header, described in this Service Specification Package (SSP), will enable delivery to the appropriate endpoint systems. By specifying use case scenarios, IJIS intends to enable this C2C Pilot Project interaction directly between two pilot sites.

The business processes are modeled in a Business Process Modeling Notation (BPMN) diagram.

Sequence diagrams illustrate the messaging required between agencies to accomplish the exchange of relevant data payloads. These are part of the Service Specification Package (SSP) governing each exchange. The IJIS C2C Project publishes specifications to govern the design, implementation, and support of each of these use case data exchanges.

The BPMN and Sequence Diagrams comprise the service's Behavior Model. They are discussed later in this document.

The exchange data is described in an Information Exchange Package Documentation (IEPD), a structured means of communicating the standards for this data exchange. This includes artifacts such as Class Diagrams and Data-Mapping spreadsheets to help give a clear picture of the data to be exchanged –and the underlying enterprise data model on which all IJIS C2C Services are founded. The CAD-to-CAD (C2C) Information Exchange Package Documentation (IEPD) is specific to the messages enabling the data transfer between CAD systems, while the Emergency Incident Data Object (EIDO) IEPD defines the actual data that is being communicated between CAD systems.

## 2.2CAD-to-CAD Use Case Scenarios

The data to be exchanged within each process flow varies depending on the use case scenario. Different combination of push and subscription operations will satisfy the needs of a particular scenario. IJIS has published high level Business Process Modeling Notation (BPMN) diagrams to illustrate each use case scenario flow. As previously mentioned, the following five initial use cases will be used for the pilot CAD systems working with these specifications.

1. **Out of Jurisdiction Call**

A dispatch center receiving a call outside of their jurisdiction. This call information is entered in the dispatch center's CAD system and then transferred to the correct jurisdiction's CAD system.

1. **Active Shooter**

An active shooter situation at a small to medium sized agency with limited resources. The dispatch center checks and requests resources to be dispatched from other dispatch centers, including Law Enforcement (LE), Special Weapons and Tactics (SWAT) team, Fire Department (FD), Emergency Medical Services (EMS), and Mutual Aid.

1. **Major Hurricane Across Multiple Counties**

A complex and severe situation of a major hurricane across multiple counties in the state. One such hurricane was Sandy in New Jersey in 2012. The State or Regional PSAP receives numerous calls reporting severe damages throughout a wide region spread across multiple counties.

1. **Pursuit/Car Chase Through Multiple Jurisdictions**

A suspect vehicle pursuit across multiple jurisdictions running into other counties and across the border in the next state. The primary dispatch patrolling on the interstate, in a marked vehicle, notices a suspiciously moving vehicle weaving in and out of lanes and at a considerable speed. Having an efficient CAD-to-CAD data exchange, between all assisting CAD systems allows all agencies to obtain correct details of the pursuit that can be relayed to the units on the call and help devise a proper strategy in managing this serious situation.

1. **Hazmat Incident Impacting Multiple Jurisdictions with Injuries and Requires Evacuation**

A hazardous material (Hazmat) incident, as defined in 10 CFR, has been identified to not be properly contained or disposed of properly and has impacted multiple jurisdictions with injuries and requires evacuation.

## Service Interoperability Requirements

Per the GRA: "While service descriptions are technology-agnostic and do not detail the physical model of a service, certain requirements need to be outlined to increase the likelihood of interoperability across services based on the same service description. This section outlines those requirements, describing the service interaction requirements, relevant assumptions and dependencies, and policies and contracts."
## 3.1Service Interaction Requirements

To facilitate service interoperability, the following requirements must be addressed. Because the details for this interoperability have not yet been fully decided, some of these requirements are outside the scope of phase 1 of the IJIS project. The details of these will be worked out by the completion of phase 1.

**Table 3: Service Interoperability**

| **Requirements ** | **Required (Yes/No) ** | **Specification** |
| --- | --- | --- |
| Service Consumer Authentication | Y | TBD |
| _Service Consumer Authorization _ | Y | SAML1 |
| _Identity and Attribute Assertion Transmission _ | Y | SAML1 |
| _Service Provider Authentication _ | Y | Server Certificates |
| _Message Nonrepudiation _ | Y | TBD1 |
| _Message Integrity _ | Y | TBD1 |
| _Message Confidentiality _ | Y | TLS version 1.3 |
| _Message Addressing _ | N |
 |
| _Reliability _ | Y | Web Sockets |
| _Transaction Support _ | Y | Web sockets |
| _Service Metadata Availability _ | N |
 |
| _Interface Description Requirements _ | Y | Async API Specification 2.4.0 (7) |
| _Message Exchange Patterns_ | Y | Section 5.2 of this document |

### 3.1.1Service Interoperability Details

1. **Service Consumer Authentication.** Service _consumers_, who are calling a web service, will be required to authenticate against a service prior to interacting with it. This will be based on Section 5, "Security" in NENA-STA-010.3 (8).
2. **Service Consumer Authorization.** The means by which usage of a service or access to an incident is granted to a service consumer. This will be based on Section 5, "Security" in NENA-STA-010.3 (8).
3. **Identity and Attribute Assertion Transmission.** The means by which a user's identity and role related information will be communicated. This will be based on Section 5, "Security" in NENA-STA-010.3 (8).
4. **Service Provider Authentication.** Separate certificates are required on each inbound and outbound connection. Service _providers_, who host a service from an IJIS-provided Open Async API (7), are required to issue a CA-signed server certificate and provide Service _consumers_ with the public key for implementation.
5. **Message Nonrepudiation.** The means by which a message is guaranteed to have been sent by the party the message purports it to be. This will be based on Section 5, "Security" in NENA-STA-010.3 (8).
6. **Message Integrity.** The means by which a message is guaranteed to not have been tampered with. This will be based on Section 5, "Security" in NENA-STA-010.3 (8).
7. **Message Confidentiality.** Transport Layer Security (TLS) version 1.3 is used to secure and encrypt messages end-to-end from every requestor to each web service.
8. **Message Addressing.** The C2C payloads include the id of the destination endpoint for a message. This is not used in Web Sockets **.**
9. **Reliability.** The guarantee of message delivery to an endpoint in the correct order. This is inherent in the web socket protocol, ' **emergency-ent**' in EIDO Conveyance (3).
10. **Transaction Support.** Web Sockets are inherently transactional and fully duplex. Behavior relating to the transactions is part of the web socket protocol, ' **emergency-ent**' in EIDO Conveyance (3).
11. **Service Metadata Availability.** This is a means to enable service discovery by having service metadata registered into a central location.
12. **Interface Description Requirements** are expressed in the AsyncAPI YAML file in the "json/webSockets" folder of this SSP. Note that there are also REST and WSDL interfaces that are defined for informational purposes at this point and discussed later.
13. **Message Exchange Patterns** _ **.** _ The description of how two different parts of an application, or different systems connect and communicate with each other.
14. **WS-Security** encryption details, when used in a SOAP based XML are as follows:
  1. Authentication Type is Mutual Certificate
  2. Signature - RSA-SHA1
  3. Encryption - AES256
  4. The message is digitally signed first and then encrypted. This is referred to as the Message Protection Order.

## 3.2Service Assumptions

- Service _Consumers_ have the capability to produce IJIS data packages for C2C and EIDO as well as the technical ability to consume the IJIS C2C web socket service.
- Service _Providers_ have the capability to host the IJIS C2C web socket service and the technical capability to process the Incident messages and return valid results in a Response message.
- The web socket service and a client to call the web socket service can both be produced from the Open Async API service description provided in this SSP.
- Implementation of these services assumes JSON as the data format for the payload.
- JSON submissions will be conformant with the JSON schema definition included in this IEPD specification.

## 3.3Service Dependencies

None.

## 3.4Policies and Contracts

Implementers may incorporate this level of information sharing in existing memoranda of understanding and/or mutual aid agreements. Alternatively, implementers may need to create and adopt similar types of governing documents.

## 3.5Security

See Section 3.1

## 3.6Privacy

Service providers should enact any privacy restrictions in the data sets provided to service consumers.

## 3.7Other Requirements

This section intentionally left blank.

# 4Additional Information

This section intentionally left blank.

# 5Service Model

This section describes the distinct specifications and schemas that define the technical implementation of the services described above. It outlines the specific inputs, outputs, and behaviors of each action that correspond to the Capabilities listed above. The service model is composed of an Information Model and a Behavior Model. Each is described in detail in the following subsections.

## 5.1Information Model

The Information Model is described following the National Information Exchange Model (NIEM) guidelines for Information Exchange Package Documentation (IEPD). The JSON schemas provided in the information model are mandatory for the formatting of the data to be exchanged.

Per the GRA: "The Information Model describes the data that comprises the inputs and outputs of the service and its actions." It is a complete description of the data to be exchanged (including the distinction between required and optional data elements).

### 5.1.1IEPD Reference

A NIEM-conformant schema set is used to specify each data model, as depicted in the respective IEPD. The data model includes attributes that can be modified to accommodate the specific data elements required per use case. Payload information that is exchanged must validate against each of the schemas provided in the respective IEPDs, see Table 2 below for reference.

Table 2: Overview of the IEPDs required for the IJIS C2C Service.

| **Payload Type** | **IEPDs** | **Notes** |
| --- | --- | --- |
| Exchanges | C2C | Describes operation level schemas only. |
| Incident | EIDO | The Incident payload lies within the Exchanges payload. |

A sending agency's CAD system (i.e., the service consumer) will provide the input into the C2C Service. Inputs consist of the:

- The data making up the construct of the message
- The EIDO payload schema, when required by the message

The IEPD files can be found in the folder:

_ijis-cad-to-cad-ssp\artifacts\service\_model\information\_model\C2C IEPD_

_ijis-cad-to-cad-ssp\artifacts\service\_model\information\_model\EIDO IEPD_

## 5.2Behavior Model

Per the GRA: "The behavior model describes the behavior of the service. The behavior model consists of two components – action model and process model."

The Business Process Modeling Notation (BPMN) diagrams in the Behavior model illustrate the points in the business process where these inputs are to be created. These diagrams provide a high-level overview of interactions between senders and recipients. They can be accessed through the catalog.html file or in the following location:

_ijis-cad-to-cad-ssp\artifacts\service\_model\behavior\_model_

### 5.2.1Action Model (Service Operations)

Because the underlying specification for the project is being used (3) which is web socket based, all requests and response messages are discrete events that operate independently of one another. Note that none of the individual operations defined contains a synchronous response message. This is because each operation is treated as a one-way message. To achieve an understanding of model and its, behavior, each must be viewed with an understanding of the message pattern to which it belongs. What follows below is every discrete message that is used. All messages described here are condensations of the EIDO Conveyance Specification (3) and must conform to the details therein.

Because this is a peer-level service between CAD systems, each endpoint in the system must implement the complete service (i.e., the service and all duplex operations).

#### 5.2.1.1 **Push Messages**

As mentioned previously, Push operations are unsolicited requests for help from one CAD to another.

##### 5.2.1.1.1 **requestForService Message**

| **Message Name** | _ **requestForService** _ |
| --- | --- |
| **Purpose** |
| A request to a responder agency to request assistance with an incident, where the sending agency does not need to specify exactly what is needed. This operation is a Request Message Exchange Pattern. Below are some use cases to which this operation applies:
1. A call handling agency sends a request to a dispatch agency to dispatch resources to an incident based on the dispatch agency's policies.
2. Primary PSAP to a secondary PSAP where the secondary PSAP dispatches resources to an incident based on the secondary PSAP's policies.
3. **Primary PSAP to an out-of-area primary PSAP where the out-of-area primary PSAP dispatches resources to an incident based on out-of-area primary PSAP's policies.**
 |
| **Inputs** | **Outputs** |
| _A request message built according to the definition of '__requestType'_._ **The requestType must contain a valid EIDO payload.** _ | _None._ _Note that the Request Message Exchange Pattern will invoke the following operations in response to this one:_
1. _Acknowledgement_
2. _ResponseNotification_

 |
| **Data Provenance** |
| _The data used to build the EIDO incident is a current snapshot of the incident as it exists in the sending CAD system._ |

##### 5.2.1.1.2 **requestForResource Message**

| **Message Name** |
#### _ **requestForResource** _
 |
| --- | --- |
| **Purpose** |
| A request when sending agency needs to identify a specific resource, inquire about availability of a resource, or manage dispatched resources. This operation is a Request Message Exchange Pattern. |
| **Inputs** | **Outputs** |
| _A request message built according to the definition of ' __resourceRequestType'_._ **The requestType must contain a valid EIDO payload.**__ The request type_ _must_ _contain a valid EDXL resource management message_ (9)_._ | _None._ _Note that the Request Message Exchange Pattern will invoke the following operations in response to this one:_
1. _Acknowledgment -_ An intermediate response indicating that a message has been accepted for processing in the receiving system.
2. _ResponseNotification -_ a response to a request.
 |
| **Data Provenance** |
| _The data used to build the EIDO incident is a current snapshot of the incident as it exists in the sending CAD system.__The data used to build the EDXL-RM message is obtained from the CAD system that triggers the exchange in the application._ |

##### 5.2.1.1.3 **requestForAwareness Message**

| **Message Name** | **_requestForAwareness_** |
| --- | --- |
| **Purpose** |
| Is used when no incident-level response or action by the recipient is requested. If, after the RequestAwareness, action is desired, another Push MUST be made with either a RequestForService or RequestForResource command regardless of whether the recipient of the RequestAwareness established a subscription to the incident. This operation is a Request Message Exchange Pattern. |
| **Inputs** | **Outputs** |
| _A request message built according to the definition of '__requestType'_._ **The requestType must contain a valid EIDO payload.** _
 | _None._ _Note that the Request Message Exchange Pattern will invoke the following operations in response to this one:_
1. _Acknowledgment -_ An intermediate response indicating that a message has been accepted for processing in the receiving system.
2. _ResponseNotification -_ a response to a request.
 |
| **Data Provenance** |
| _The data used to build the EIDO incident is a current snapshot of the incident as it exists in the sending CAD system._ |

##### 5.2.1.1.4 **cancelRequest Message**

| **Message Name** | _ **cancelRequest** _ |
| --- | --- |
| **Purpose** |
| A request has previously been sent but is no longer needed. This operation is a Request Message Exchange Pattern. |
| **Inputs** | **Outputs** |
| _A request message built according to the definition of '__requestType'_._The requestType must not contain an EIDO payload._ | _None._ _Note that the Request Message Exchange Pattern will invoke the following operations in response to this one:_
1. _Acknowledgment -_ An intermediate response indicating that a message has been accepted for processing in the receiving system.
2. _ResponseNotification -_ a response to a request.
 |
| **Data Provenance** |
| _The request ID from the previous request being cancelled must be used for the requestID._ |

##### 5.2.1.1.5 **responseNotification Message**

| **Message Name** | _ **responseNotification** _ |
| --- | --- |
| **Purpose** |
| An agency that receives and processes any of the above Operations sends a response to the Requestor to convey status or report errors in processing requests This operation is a part of the Request Message Exchange Pattern. |
| **Inputs** | **Outputs** |
| _The results of processing_ | _None_ |
| **Data Provenance** |
| _The request ID from the previous request must be used for the requestID._ |

##### 5.2.1.1.6 **acknowledgement Message**

| **Message Name** | _ **responseNotification** _ |
| --- | --- |
| **Purpose** |
| A simple acknowledgement sent by the receiving CAD to acknowledge whether the receiving CAD accepted a request to be processed. This operation is a part of the Request Message Exchange Pattern. |
| **Inputs** | **Outputs** |
| _None_ | _None_ |
| **Data Provenance** |
| _None_ |

#### 5.2.1.2 **Subscription Messages**

These two messages (and the sub-messages therein) facilitate the management of subscriptions between two CAD systems. There are two sides in a subscription operation:

1. A CAD that wants to receive incident updates from another CAD. This is referred to as the subscriber.
2. A CAD that manages what CAD systems are interested in an incident and sends an incident to those CAD systems when a qualifying incident is updated. This is referred to as the notifier.

##### 5.2.1.2.1 **submitSubscriberMessage**

| **Message Name** | _ **submitSubscriberMessage** _ |
| --- | --- |
| **Purpose** |
| A top-level message used by a CAD system to inform another CAD endpoint of initiating and managing requests to keep informed of an incident or incidents in other CAD systems. The structure of the message contains the four following subscriber sub-messages.
1. subscribe - Request updates from another CAD system about an emergency incident.
2. unsubscribe - Request to stop receiving incident updates.
3. eventResponse - An asynchronous response to a received incident update.
4. terminateResponse - An asynchronous response to a received notification that no more incident updates will be received.
 |
| **Inputs** | **Outputs** |
| _One of the four sub-messages listed above. The one used is dependent on whether this is a new subscription message or whether it is a response to a notification message._ | _None.__These sub-messages follow a traditional request-response message pattern but are sent back and forth as standalone messages. Within this context, only the subscribe and unsubscribe will expect a response back to fulfill the message pattern._ |
| **Data Provenance** |
| _None_ |

##### 5.2.1.2.2 **submitNotifierMessage**

| **Message Name** | _ **submitSubscriberMessage** _ |
| --- | --- |
| **Purpose** |
| A top-level message used by a CAD system to inform a previously subscribed CAD endpoint of updates to an emergency incident. The structure of the message contains the four following notifier messages.
1. subscribeResponse- A response communicating the result of a subscription request.
2. unsubscribeResponse- A response communicating the result of a unsubscribe request.
3. event- A update to an emergency incident that has been subscribed to.
4. terminate- A notification to a subscribing CAD system that a subscribed incident has either been closed of the subscription has met it expiration criteria.
 |
| **Inputs** | **Outputs** |
| _One of the four sub-messages listed above. For an 'event' sub-message type, the EIDO must contain a valid EIDO payload_ | _None.__These sub-messages follow a traditional request-response message pattern but are sent back and forth as standalone messages. Within this context, only the event and terminate will expect a response back to fulfill the message pattern._ |
| **Data Provenance** |
| _The data used to build the EIDO incident is a current snapshot of the incident as it exists in the sending CAD system._ |

## 5.3Process Model

### 5.3.1Message Exchange Patterns

Each of the above messages are used in a specific order to implement specific message patterns. The two message exchange patterns used by the service are:

- Request/Response – A message is sent out and a near immediate (synchronous) response is sent back to the sender. This pattern is typically used where the processing involved is fully autonomous without queuing or the like.
- Asynchronous Request/Response – This pattern extends the Request/Response message pattern. A message is sent out and a near immediate (synchronous) response is sent back to the sender. This response is typically viewed as an acknowledgement. At some time in the future, after a higher-level business process has been completed, a second Response is sent back to the sending with the processing results of the request.

As mentioned earlier, each request and response is treated as a discrete message because a web socket is used as the transport for the service. Therefore, each of the above message patterns is implemented with two or more discrete messages. The implementation of the '_ **emergency-ent** _' web socket protocol is what ensures that the web socket behaves in accordance with both, the message patterns, and the specifications.

#### 5.3.1.1 **Push Model**

The push model is the series of discrete operations that piece together one or more Asynchronous Request/Response message exchange patterns to fulfill the need of requesting services from an external CAD system. There are four basic operations that are needed to fulfill this need:

1. Request For Service
2. Request For Resource
3. Request for Awareness
4. Cancel Operation

Note that each of these operations have a corresponding message listed above.

##### 5.3.1.1.1 **Request for Service**

The request for service is invoked when the Sending CAD does not need to specify a specific resource. The receiving agency will know what kind of service is needed based on the type of request.

![](RackMultipart20240115-1-tu845r_html_892c6a0a56a10e81.png)

##### 5.3.1.1.2 **Request for Resource**

This request is used when a sending CAD needs to request a specific resource, inquire about availability of a resource, or manage dispatched resources.

![](RackMultipart20240115-1-tu845r_html_6231d310ec6e9fc5.png)

The request for resources is a series of Asynchronous Request/Response exchanges between the sending and receiving CAD systems to manage the resource requests. This operation embeds the EDXL-RM message which itself is part of a negotiation for requesting resources.

The Receiving CAD responds with its own requestForResource message with an EDXL-RM message of ResponseToResourceRequest to let the requestor know whether the resource is available and assigned.

Note that the behavior of the Sending and Receiving CAD must implement the behavior documented in the EDXL-RM specification so that the resource negotiation occurs correctly. The full list of possible EDXL-RM messages is as follows:

- RequestResource
- ResponseToRequestResource
- RequisitionResource
- CommitResource
- RequestInformation
- ResponseToRequestInformation
- OfferUnsolicitedResource
- ReleaseResource
- RequestReturn
- ResponseToRequestReturn
- RequestQuote
- ResponseToRequestQuote
- RequestResourceDeploymentStatus
- ReportResourceDeploymentStatus
- RequestExtendedDeploymentDuration
- ResponseToRequestExtendedDeploymentDuration

##### 5.3.1.1.3 **Request For Awareness**

This request is used when no incident-level response or action by the recipient is being requested. It is an alert to a jurisdiction that a current incident may be of interest to them. After reviewing the incident, the Receiving CAD may either accept the incident and open the incident in their system or turn down the request (if they can't be of any aid in the incident due to resource limitations or whatever other reason).

If the incident is accepted, the Receiving CAD may also request updates to the incident from the sending CAD by means of a subscription message. The Sending CAD may also request to receive updates from the Receiving CAD by means of a subscription message.

If an action is needed after a requestForAwareness has been sent, either a requestForService or requestForResource command must be invoked, regardless of whether or not the receiving CAD has established a subscription to the incident after receiving the requestForAwareness.

![](RackMultipart20240115-1-tu845r_html_27f8ee9d2cadc0e.png)

##### 5.3.1.1.4 **Cancel Request**

This request is sent when a sending CAD no longer needs the previously requested service or resource.

![](RackMultipart20240115-1-tu845r_html_e448a06e1bbfb45d.png)

#### 5.3.1.2 **Subscription Model**

The subscription model is a series of operations that are implemented with the Request/Response message exchange pattern. In the subscription model, the endpoints are described in terms of a subscriber and notifier. A CAD that wants to receive incident updates from another CAD system is referred to as the Subscriber CAD. A CAD system that manages requests to receive incident updates as well as the sending of an incident is referred to as the Notifier CAD. The two subscription messages described above implement four different actions:

- Subscribe
- Unsubscribe
- Send Event Notification
- Terminate

The subscription message cover 5 different usage cases which are illustrated in the diagram below.

1. The CAD that wants to receive incident updates (Subscriber CAD) sends a subscribe message to the CAD system with the incident of interest (Notifier CAD). The message can specify filter, update frequency and expiration criteria.
2. Changes to the emergency incident in the Notifier CAD system are sent based on the update frequency criteria.
3. if the Subscriber wants to change the subscription (Re-subscribe) by modifying the filters, etc., it resends the subscribe message.
4. When the subscriber no longer needs updates on an incident, it sends an unsubscribe message.
5. If the incident in the Notifier CAD is closed, or if the expiration criteria in the subscribe message is met, then the Notifier CAD sends a terminate to inform the subscriber that the subscription has been closed.

Note that this diagram shows the relevant subscription message in conjunction with the relevant sub message to show the expected behavior of the subscription model.

![](RackMultipart20240115-1-tu845r_html_d507796343af3990.png)

## 5.4Use Case Sequence Diagrams

The Process Model for the IJIS C2C Service is designed to meet five specific Use Case Scenarios. To illustrate how the process model satisfies the scenarios, reference the sequence diagrams below. In addition, these diagrams are accessible independently via 'IJIS Sequence Diagrams', under "Artifacts" on the catalog.html web page or in the following location in the package:

_ijis-cad-to-cad-ssp\artifacts\service\_model\behavior\_model_

### 5.4.1Out of Jurisdiction Call

A dispatch center receiving a call outside of their jurisdiction. This call information is entered in the dispatch center's CAD system and then transferred to the correct jurisdiction's CAD system.

![](RackMultipart20240115-1-tu845r_html_184953a8612e14d8.png)

### 5.4.2Active Shooter

An active shooter situation at a small to medium sized agency with limited resources. The dispatch center checks and requests resources to be dispatched from other dispatch centers, including Law Enforcement (LE), Special Weapons and Tactics (SWAT) team, Fire Department (FD), Emergency Medical Services (EMS), and Mutual Aid.

Note that the diagram shows subscribe messages being sent by all the involved systems. This behavior is optional and based on the business requirements of each system. They are included because in the example, it is assumed that each system will want to be updated with what is happening in the other CAD systems.

![](RackMultipart20240115-1-tu845r_html_365a5fded6416ff8.png)

### 5.4.3Major Hurricane Across Multiple Counties

A complex and severe situation of a major hurricane across multiple counties in the state. One such hurricane was Sandy in New Jersey in 2012. The State or Regional PSAP receives numerous calls reporting severe damages throughout a wide region spread across multiple counties.

![](RackMultipart20240115-1-tu845r_html_c657c8e80223111d.png)

### 5.4.4Pursuit/Car Chase Through Multiple Jurisdictions

A suspect vehicle pursuit across multiple jurisdictions running into other counties and across the border in the next state. The primary dispatch patrolling on the interstate, in a marked vehicle, notices a suspiciously moving vehicle weaving in and out of lanes and at a considerable speed. Having an efficient CAD-to-CAD data exchange, between all assisting CAD systems allow all agencies to obtain correct details of the pursuit that can be relayed to the units on the call and help devise a proper strategy in managing this serious situation.

![](RackMultipart20240115-1-tu845r_html_a2e9383d54061f79.png)

### 5.4.5Hazmat Incident Impacting Multiple Jurisdictions with Injuries and Requires Evacuation

A hazardous material (Hazmat), as defined in 10 CFR, incident has been identified to not be properly contained or disposed of properly and has impacted multiple jurisdictions with injuries and requires evacuation.

![](RackMultipart20240115-1-tu845r_html_c3bb941c799ac40a.png)

# 6Transitional Architectures

T ![](RackMultipart20240115-1-tu845r_html_f7b998a069c1fbae.png)
 he implementation as described in this specification mandates the use of web sockets with JSON payload messages. The rationale is that eventually, all CAD systems will eventually migrate to next generation 911 systems and will be running on interconnected Emergency Services IP Networks (ESInet). It is, however, unrealistic to assume that such a transition will happen in a timely fashion and as such, the interconnect with other CAD systems will need to consider other types of interfaces where budgetary, resource and other constraints prevent being able to implement a full web socket/JSON service to support this specification. To facilitate the discussion a very simplified network diagram is shown below.

A gateway web server will need to exist at the edge of one or the other network to transform between the transport protocol and possibly the payload format. As can be seen in the diagram, the interworking falls into two cases:

- Web Socket/JSON to and from REST/JSON
- Web Socket/JSON to and from SOAP/XML

For Web Socket/JSON to and from REST/JSON, only transformation of the transport layer is needed since the JSON payload sits on top of the transport in both cases. Interworking with SOAP/XML is a greater challenge because a conversion is needed between JSON and XML in both directions in addition to the transport. To mitigate some of the effort in providing this interworking, the SSP also provides a REST/JSON openAPI definition of the interface as well as a SOAP/XML WSDL and schema set representing the XML equivalent of the EIDO. The mapping spreadsheets in the relevant IEPDs provide columns that facilitate going between the JSON and XML.

Note that the greater difficulty in any interworking is anticipated to be with Service Interaction Requirements in Section 3.1, particularly with authentication and authorization components. These will need to be addressed in the future.

Interworking with NLETs may require additional transformation if their XML interpretation of the EIDO is different from that in this SSP. Any issues there will be addressed outside of the scope of the first phase of this project.

# 7References

1. **Council, Global Standards.** The Global Reference Architecture (GRA) Service Specification Guideline V 1.2.0. _Bureau of Justice Administration, Office of Justice Programs._ [Online] May 2015. https://bja.ojp.gov/library/publications/global-reference-architecture-gra-service-specification-guideline-v-120.

2. **National Emergency Number Association (NENA).**_NENA Standard for Emergency Incident Data Object (EIDO)._ s.l. : NENA, 10/20/2021. doc. NENA-STA-021.1-2021 .

3. —. _NENA Standard for the Conveyance of Emergency Incident Data Objects (EIDOs) between Next Generation (NG9‑1‑1) Systems and Applications._ s.l. : NENA, MM/DD/202Y. doc. (Working Draft). ANS CANDIDATE NENA-STA-024.2-202Y.

4. **Department of Homeland Security.** _CAD Interoperability - Operations & Techmical Requirements, CAD-to-CAD User Stories._ Science and Technology Directorate. 9/29/2021. pdf.

5. —. _HAZMAT 033022._ Science and Technology Directorate. 6/1/2022. pdf. Hazmat incident table explanation.

6. **Mission Critical Partners LLC (MCP).**_Inferred Hazmat Use Case Scenario._ s.l. : MCP, 6/7/2022. pdf. Inferred model based on use case table information.

7. **Initiative, AsyncAPI.** AsyncAPI Specification. [Online] https://www.asyncapi.com/docs/specifications/v2.0.0.

8. **Inc., National Emergency Number Association.** _NENA i3 Standard for Next Generation, NENA-STA-010.3a-2021._ 10/7/2021. NENA-STA-010.3a-2021.

9. **OASIS.** Emergency Data Exchange Language Resource Messaging (EDXL-RM) 1.0 OASIS Standard incorporating Approved Errata. _https://www.oasis-open.org/._ [Online] 12 22, 2009. https://docs.oasis-open.org/emergency/edxl-rm/v1.0/errata/EDXL-RM-v1.0-OS-errata-os.pdf. EDXL-RM-v1.0.

10. **Integrated Justice Information System (IJIS) Institute.**_IJIS-CAD Functional Specifications Package._ 9/29/2021. File Folder.

11. —. _CAD-to-CAD Interoperability, Information Exchange Connectivity (Lab Environment) And Pilot Sites Implementation Support._ s.l. : IJIS, 9/29/2021. pdf.

12. **National Emergency Number Association (NENA).**_NENA Standard for Emergency Incident Data Object (EIDO)._ s.l. : NENA, MM/DD/202Y. doc. (Working Draft). ANS CANDIDATE NENA-STA-021.1-202Y.

13. **APCO/NENA.** _NG9-1-1 Emergency Incident Data Document (EIDD)._ 9/19/2016. pdf. Candidate APCO / NENA 2.105.1-201x.

[1](#sdfootnote1anc) Out of scope for phase 1. To be determined during phase 1 and implemented in a later phase to be defined.

**MissionCriticalPartners.com**

Denver Office | 1512 Larimer Street. Suite 950 | Denver, CO 80202 | 888.8.MCP.911 or 888.862.7911