### Person Contacts Service
   - This service returns personal information data to the UPoint Mobile Application.
   - This is a UPoint Mobile specific service and not a general use service.	
	
### OpenAPI Spec: 

https://bitbucket.alight.com/projects/UPN/repos/channel-personcontacts-service/browse/api/openapi.yaml

### Service Owner
 Mike Pozen <mike.pozen@alight.com>; Jeff Baisden <jeff.baisden@alight.com>; Melissa Johnson <melissa.johnson.2@alight.com>;
 
### Development Team
Adit Majmudar <adit.majmudar@alight.com >; Uday Chudasama <uday.chudasama.2@alight.com>; Sandip Patel <sandip.patel.2@alight.com>; Vinay Solanki <vinay.solanki@alight.com>; Rohit Parmar <rohit.parmar@alight.com>;
 
### Technical Contact: 
 Jeff Baisden <jeff.baisden@alight.com>;   Tarun Malhotra <tarun.malhotra.2@alight.com>;  Adit Majmudar <adit.majmudar@alight.com>;
 
### JIRA Type
https://jira.alight.com/projects/MBL/summary

### Support Contacts 
 UPoint Support (CTS Portal Support)
 
### Service Dependencies:

 - **channel-widgetconfigurations service** :   [https://bitbucket.alight.com/projects/UPN/repos/load-properties-service/browse](https://bitbucket.alight.com/projects/UPN/repos/load-properties-service/browse)
 - **channel-cache-clientconfigurations**  :[https://bitbucket.alight.com/projects/UPN/repos/channel-widgetconfigurations-service/browse](https://bitbucket.alight.com/projects/UPN/repos/channel-widgetconfigurations-service/browse)
 

### Backend Systems Interacted With: 

 - UPoint Configuration
 - UCE
 
### New Relic Dashboard

 - Prod: https://rpm.newrelic.com/accounts/752702/applications/120063341

### Angular Widgets Calling This Service: 
 This service is called from mobile application (Xamarin forms). The project for App is:  https://bitbucket.alight.com/projects/DIL/repos/upointappv2/browse
 
## Service Maps
### Service End-Point details
 - **Path Mapping**: /api/channel/personcontacts <br> 
 - The **/personcontacts** endpoint returns Personal contact information.
  Obtain alightRequestHeader and alightPersonSessionToken from this API https://bitbucket.alight.com/projects/UPN/repos/channel-logonperson-service/browse/readme.md. Details on the request payload as well as valid responses are in the OpenAPI  Specification at following location:
  - https://upoint-dv.alight.com/specmgmt/#/
	- Request Header
	```
			**alightRequestHeader : {"locale":"en_US","roleId":"19943_1.0-E:@PPT@","clientId":"19943","channelRequestData":"clientsetup::{\"clientId.DC\":\"19943\",\"clientId.DB\":\"19943\",\"primary.clientId\":\"19943\",\"business.HM\":\"19943_1.0\",\"clientId.CM\":\"19943\",\"business.CORE\":\"19943_portal\",\"clientId.HM\":\"19943\",\"udp.clientId\":\"19938\",\"business.DB\":\"19943_1.0\",\"business.DC\":\"19943_1.0\",\"business.CM\":\"19943_1.0\",\"business.Retirement4x\":\"19943_1.0\"}::gblsId::79299c35-98bc-4378-9856-8ab19f9c1a1c_2020-08-26-06.49.14.987000::sessionCreatedTimestamp::2020-08-26-06.49.14.987000::srcPlatform::upointmbl"}
			**alightPersonSessionToken : rBBiBXuHI3FdUVBZkObYFJc6R0T**********************************************...
	```
	- Query Parameter
	```
			NA
	```
	- Request Body
	```
			NA
	```
	- Response Header
	```
		   	NA 
	```
	- Response Body
	```
			{
			"emails": [
				{
					"isPreferred": false,
					"isMissing": true,
					"missingText": "Information not on file"
				}
			],
			"phones": [
				{
					"isPreferred": false,
					"isMissing": true,
					"missingText": "Information not on file"
				}
			],
			"addresses": [
				{
					"type": "home",
					"description": "Permanent Address",
					"lines": [
						"fdsgr",
						"dsfews"
					],
					"city": "CA",
					"state": "CA",
					"stateDescription": "California",
					"country": "United States of America",
					"zip": "12345",
					"isPreferred": false,
					"isBad": false
				}
			],
			"link": {
				"type": "sso",
				"url": "https://api.int.alight.com/api/channel/personsinglesignonlink?partner=Portal&pageCd=PRTL_PRSN_INFO",
				"text": "View More/Update"
			}
		}
	```
   
### Screen Shot:

 - This service returns a JSON structure containing the "emails", "phones", "addresses", and a "link" for the personal information page on the UPoint Mobile Application.
	![UPoint Mobile](img1.jpg)		 
