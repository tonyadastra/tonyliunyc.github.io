# Configure LTI 1.3 Tool in Canvas LMS

<!-- 1. Canvas was installed locally in Docker using default manual:

https://github.com/instructure/canvas-lms/wiki/Quick-Start#automated-setup -->

1. Enable LTI 1.3 in "Settings / Feature Options" in your Canvas environment:

![](https://raw.githubusercontent.com/dmitry-viskov/repos-assets/master/pylti1p3/examples/canvas-lms/001.png)

3. Go to the “Developer Keys” section and create new LTI Key:
![](https://raw.githubusercontent.com/dmitry-viskov/repos-assets/master/pylti1p3/examples/canvas-lms/002.png)

**Key Name**: Bulletin LTI Developer Key

**Owner Email**: tonyliunyc@gmail.com

**Title**: Bulletin LTI

**Description**: An LTI 1.3 tool as for the school bulletin

**Redirect URIs**: https://lti1p0-bulletin.herokuapp.com/start/

**Target Link URI**: https://lti1p0-bulletin.herokuapp.com/start/ 

**OpenID Connect Initiation Url**: https://lti1p0-bulletin.herokuapp.com/login/

**JWK Method**: (Select Public JWK URL) https://lti1p0-bulletin.herokuapp.com/jwks/  

**LTI Advantage Services**: Enable all toggles

**Placements**: Choose "Global Navigation", "Course Navigation", etc. as needed

<!-- **Assignment Selection / Target Link URI**: https://lti1p0-bulletin.herokuapp.com/start/ 
**Assignment Selection / Select Message Type**: LtiDeepLinkingRequest   -->

![](https://raw.githubusercontent.com/dmitry-viskov/repos-assets/master/pylti1p3/examples/canvas-lms/003.png)

4. Change "State" from **OFF** to **ON** for the new created key

5. Record the "Client ID" of the newly genereated LTI 1.3 Developer Key

5. Create new External App: "Settings -> Apps -> +App"  
Choose "Configuration Type: by Client ID"
Insert the "Client ID" recorded earlier

![](https://raw.githubusercontent.com/dmitry-viskov/repos-assets/master/pylti1p3/examples/canvas-lms/009.png)

6. Record the "Deployment ID":

![](https://raw.githubusercontent.com/dmitry-viskov/repos-assets/master/pylti1p3/examples/canvas-lms/004.png)
--
![](https://raw.githubusercontent.com/dmitry-viskov/repos-assets/master/pylti1p3/examples/canvas-lms/005.png)

7. Make sure the client ID and deployment ID are added to this [Google Doc](https://docs.google.com/document/d/1mwhy09JLR443XsRbP3Ik5F3b6nwXzOLGZhBN1da9QuQ/edit?sharingaction=ownershiptransfer#). If no access, please share them to tonyliunyc@gmail.com

8. Wait for the update confirmation. After that, your Bulletin LTI 1.3 should be ready to go!

The above content is adapted from the [original wiki by Dmitry Viskov](https://github.com/dmitry-viskov/pylti1.3/wiki/Configure-Canvas-as-LTI-1.3-Platform)