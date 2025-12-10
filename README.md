# Genesys-Cloud-CX-Voice

🟦 Genesys Cloud – Call Routing & Telephony Setup (Step-by-Step)

This project demonstrates how to set up end-to-end telephony using Genesys Cloud Voice including DIDs, routing, WebRTC phones, Architect flows, and inbound call handling.

This configuration assumes Genesys Cloud is used as your PSTN provider, therefore no external telecom carrier is required.

1️⃣ Overview

Genesys Cloud provides a fully cloud-based PSTN solution called Genesys Cloud Voice.

DID numbers purchased directly from Genesys

No external telecom carrier required

All inbound and outbound calling handled in cloud

Cloud PSTN + Cloud PBX + Cloud Routing

➡️ In this model, Genesys acts as your PSTN provider.

2️⃣ Create Users and Agents

Admin → People & Permissions → People

Create a user

Assign required roles

Enable agent permissions

Configure profile based on responsibility

Output:

User created
Agent profile assigned

3️⃣ Create Division

Admin → People & Permissions → Divisions

Create division

Assign users, queues, routes, and flows to the division

4️⃣ Create WebRTC Phone

Admin → Telephony → Phone Management

Create WebRTC Phone

Assign extension

Assign DID (after purchase)

Assign WebRTC phone to agent

5️⃣ Create and Verify Location

Admin → Locations

Create a location

Add proper address details

Ensure location gets verified by Genesys
(important for emergency services & telephony)

6️⃣ Create Group and Assign Members

Admin → Directory → Groups

Create group

Add users/agents

Use groups for organizing access & monitoring

7️⃣ Create Telephony Site

Admin → Telephony → Sites

Create site

Define name

Select location

Without assigning a location, site will not function.

8️⃣ Configure Number Plans & Outbound Routes

Inside Site → Number Plans

Define dial plan
(local, mobile, international patterns)

Outbound Routes

Specify outbound rules based on trunk

Choose outbound plan per site

9️⃣ Create and Configure Trunk

Admin → Telephony → Trunks

Name

Carrier type (BYOC if applicable)

SIP protocol

Termination identifier

Termination header (if required)

Under Number Plan:

Select site where inbound calls should land

Outbound

Define Outbound SIP Termination FQDN

Identity (Calling)

Disable:

Address Omit + Prefix

Identity (Caller)

Disable:

Address Omit + Prefix

🔟 Purchase DID Numbers

Purchase DID from Genesys Cloud Voice

Assign DID to:

WebRTC phone (direct agent calling)

Call Routing / Architect flow

1️⃣1️⃣ Create Architect Flow (Inbound Call)

Routing → Architect

Build inbound flow

Drag-and-drop design toolbox

Configure menu options

Queue transfers

Prompts

Data actions (optional)

Example use case:

Banking Customer Support Call Flow

Attach your diagram here: **find the image in file.**



1️⃣2️⃣ Create Call Routing

Admin → Routing → Call Routing

Create new route

Assign division

Select Architect flow

Assign DID number

1️⃣3️⃣ Test & Troubleshoot

Simulate call from test DID

Validate menu prompts

Confirm routing logic

Check agent WebRTC phone

Review call logs if call fails

If something is wrong:

Check telephony status

Check trunk configuration

Check number plan

Check DID assignment

Check routing + flow

📌 Conclusion

This configuration completes an end-to-end inbound calling scenario in Genesys Cloud using Genesys Cloud Voice, covering:

PSTN setup

Telephony configuration

Trunks

Number plans

Architect flow

Call routing

WebRTC Agents

No external telecom carrier is required.


🧑‍💻 Skills Demonstrated

Genesys Cloud CX Telephony

WebRTC provisioning

Call routing

PSTN using Genesys Cloud Voice

Architect flow design

Troubleshooting

Divisions & users

SIP configuration

DID assignment


**Thank You**



