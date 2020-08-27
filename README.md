### Person Stories Service
   - This service returns content articles called Stories on the Go for UPoint Mobile application.
   - This is a UPoint Mobile specific service and not a general use service.	
	
### OpenAPI Spec: 

https://bitbucket.alight.com/projects/UPN/repos/channel-personstories-service/browse/api/openapi.yaml

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
 - **channel-client-articles-service:** :  [https://bitbucket.alight.com/projects/UPN/repos/channel-client-articles-service/browse](https://bitbucket.alight.com/projects/UPN/repos/channel-client-articles-service/browse)
 

### Backend Systems Interacted With: 

 - UPoint Configuration
 - UCE
 
### New Relic Dashboard

 - Prod: https://rpm.newrelic.com/accounts/752702/applications/120063341

### Angular Widgets Calling This Service: 
 This service is called from mobile application (Xamarin forms). The project for App is:  https://bitbucket.alight.com/projects/DIL/repos/upointappv2/browse
 
## Service Maps
### Service End-Point details
 - **Path Mapping**: /api/channel/personstories <br> 
 - The **/personstories** endpoint returns current Stories on the Go for the user.
  Obtain alightRequestHeader and alightPersonSessionToken from this API https://bitbucket.alight.com/projects/UPN/repos/channel-logonperson-service/browse/readme.md Details on the request payload as well as valid responses are in the OpenAPI  Specification at following location: https://upoint-dv.alight.com/specmgmt/#/
  
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
			[
				{
					"id": "FA940A42-BD06-41E1-9F5B-38D4288F4764",
					"title": "Stories on the Go",
					"body": "https://api.int.alight.com/api/channel/personstories?articleId=FA940A42-BD06-41E1-9F5B-38D4288F4764",
					"img": "https://litlb105.upoint.alight.com/documents/13153/1321049/save_with_HCFSA.jpg/7756ba54-9042-4f5b-81c2-2323928bb01a"
				}
			]
	```
  
### Service End-Point details
 - **Path Mapping**: /api/channel/articleId=articleId <br> 
 - The **/articleId** endpoint get ths detailed information for particular article based on article id. Information contains image url/title/description.
 Obtain alightRequestHeader and alightPersonSessionToken from this API https://bitbucket.alight.com/projects/UPN/repos/channel-logonperson-service/browse/readme.md. Details on the request payload as well as valid responses are in the OpenAPI  Specification at following location: https://upoint-dv.alight.com/specmgmt/#/
 
	- Request Header
	```
			**alightRequestHeader :   {"locale":"en_US","roleId":"19943_1.0-E:@PPT@","clientId":"19943","channelRequestData":"clientsetup::{\"clientId.DC\":\"19943\",\"clientId.DB\":\"19943\",\"primary.clientId\":\"19943\",\"business.HM\":\"19943_1.0\",\"clientId.CM\":\"19943\",\"business.CORE\":\"19943_portal\",\"clientId.HM\":\"19943\",\"udp.clientId\":\"19938\",\"business.DB\":\"19943_1.0\",\"business.DC\":\"19943_1.0\",\"business.CM\":\"19943_1.0\",\"business.Retirement4x\":\"19943_1.0\"}::gblsId::79299c35-98bc-4378-9856-8ab19f9c1a1c_2020-08-26-06.49.14.987000::sessionCreatedTimestamp::2020-08-26-06.49.14.987000::srcPlatform::upointmbl"}
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
			[
				{
					"id": "FA940A42-BD06-41E1-9F5B-38D4288F4764",
					"title": "Stories on the Go",
					"body": "https://api.int.alight.com/api/channel/personstories?articleId=FA940A42-BD06-41E1-9F5B-38D4288F4764",
					"img": "https://litlb105.upoint.alight.com/documents/13153/1321049/save_with_HCFSA.jpg/7756ba54-9042-4f5b-81c2-2323928bb01a"
				}
			]
	```
   
### Screen Shot:

 - This service returns Stories on the Go for the user. Stories can include client specific announcements or educational content highlighted on the application and are configured via UCE (UPoint Content Editor). The story data includes a title, body text and image URLs for display. At this time, stories will only support public links and does not support population variation.
	![UPoint Mobile](img1.jpg)		 

-  The service also returns article details for a specific story when an article id value is passed to it as a parameter.
	![UPoint Mobile](img2.jpg)
