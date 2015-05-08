<link href="http://kevinburke.bitbucket.org/markdowncss/markdown.css" rel="stylesheet"></link>

#Legacy APIs#
The legacy APIs allowed you to query metadata about users, widgets, dashboards and server version. 
The API uses REST principles; you can use your browser to access URLs and interact with it.
The first section of this document provides a brief overview of the API, detailed explanations and use cases follow. 
##Base URL##
All examples in this document use the following base URL:

    https://localhost:8443/OWF/Preferences/ IS THIS RIGHT???!!!!????


##User API Overview##
You can use the User Preference APIs find (GET) a current user's information (MAKE MORE SPECIFIC) or update his or her preferences in a number of ways (DELETE, SET, etc.). 

<table style="width:55%">
  <thead>
    <td>Field </td>
    <td> Method </td>
    <td>Request URL</td>
    <td>Description </td>
  </thead>
  <tr>
    <td><b><a href=https://github.com/stephaniesaylor/Practice-Repo/blob/master/deleteUserPreference.md>"/deleteUserPreference(cfg)"</a></b></td>
    <td>POST 
        (Form_Method: Delete)</td> 
        <td>https://localhost:8443/owf/prefs/preference/com.company.widget/First%20President</td>
    <td>Deletes a user preference with the provided namespace and name.</td>
  </tr>
  <tr>
    <td><b>/doesUserPreferenceExist(cfg)</b></td>
    <td>GET</td> 
    <td>https://localhost:8443/owf/prefs/hasPreference/foo.bar.0/test%20path%20entry%200?version=7.14.1-v1&dojo.preventCache=1425324415713</td>
    <td>Description</td>
  </tr>
  <tr>
    <td><b>/getCurrentUser(cfg)</b></td>
    <td>GET</td> 
    <td>https://localhost:8443/owf/prefs/person/whoami?version=7.14.1-v1&dojo.preventCache=1425324499182</td>
    <td>Description</td>
  </tr>
  <tr>
    <td><b>/getUserPreference(cfg)</b></td>
    <td>GET</td> 
    <td>https://localhost:8443/owf/prefs/preference/com.company.widget/First%20President?version=7.14.1-v1&dojo.preventCache=1425328416823</td>
    <td>Description</td>
  </tr>
  <tr>
    <td><b>/setUserPreference(cfg)</b></td>
    <td>POST</td> 
    <td>https://localhost:8443/owf/prefs/preference/com.company.widget/First%20President</td>
    <td>Description</td>
  </tr>
</table>

##Widget API Overview##

<table style="width:100%">
  <thead>
    <td>Field </td>
    <td>Method </td>
    <td>Request URL</td>
    <td>Description</td>
  </thead>
  <tr>
    <td><b>/findWidgets(cfg)</b></td>
    <td>POST 
        (Form_Method: GET)</td> 
        <td>https://localhost:8443/owf/prefs/widget/listUserAndGroupWidgets</td>
    <td></td>
  </tr>
  <tr>
    <td><b>/getWidget(cfg)</b></td>
    <td>GET</td> 
    <td>https://localhost:8443/owf/prefs/widget/eb5435cf-4021-4f2a-ba69-dde451d12551?version=7.14.1-v1&dojo.preventCache=1425328472680</td>
    <td>Description</td>
  </tr>
  <tr>
    <td><b>/updateAndDeleteWidgets(cfg)</b></td>
    <td></td> 
    <td></td>
    <td>Description</td>
  </tr>
</table>


##Dashboard API Overview##
<table style="width:100%">
  <thead>
    <td>Field </td>
    <td>Method </td>
    <td>Request URL</td>
    <td>Description</td>
  </thead>
  <tr>
    <td><b>/cloneDashboard(cfg)</b></td>
    <td>POST</td> 
    <td>https://localhost:8443/owf/stack/addPage</td>
    <td></td>
  </tr>
  <tr>
    <td><b>/createOrUpdateDashboard(cfg)</b></td>
    <td>POST</td> 
    <td>https://localhost:8443/owf/stack/addPage</td>
    <td></td>
  </tr>
  <tr>
    <td><b>/createOrUpdateDashboard(cfg)</b></td>
    <td>POST</td> 
    <td>https://localhost:8443/owf/prefs/dashboard/9c01a5f5-b37e-47db-8c07-d733c368dab5</td>
    <td></td>
  </tr>
  <tr>
    <td><b>/deleteDashboard(cfg)</b></td>
    <td>POST
        Form_method: DELETE</td> 
    <td>https://localhost:8443/owf/prefs/dashboard/9c01a5f5-b37e-47db-8c07-d733c368dab5</td>
    <td></td>
  </tr>
  <tr>
    <td><b>/findDashboards(cfg)</b></td>
    <td>GET</td> 
    <td>https://localhost:8443/owf/prefs/dashboard?version=7.14.1-v1&dojo.preventCache=1425324449792</td>
    <td></td>
  </tr>
  <tr>
    <td><b>/findDashboardsByType(cfg)</b></td>
    <td>POST
      Form_method: PUT</td> 
    <td>https://localhost:8443/owf/prefs/dashboard/cbf2bd69-ad7e-44f7-bf75-c838048a9c43?isdefault=true</td>
    <td></td>
  </tr>
  <tr>
    <td><b>/getDashboard(cfg)</b></td>
    <td>GET</td> 
    <td>https://localhost:8443/owf/prefs/dashboard/43821977-fcfe-496a-a221-bc97967c3215?version=7.14.1-v1&dojo.preventCache=1425324659938</td>
    <td></td>
  </tr>
  <tr>
    <td><b>/getDefaultDashboard(cfg)</b></td>
    <td>POST</td> 
    <td>https://localhost:8443/owf/prefs/dashboard?isdefault=true</td>
    <td></td>
  </tr>
  <tr>
    <td><b>/setDefaultDashboard(cfg)</b></td>
    <td>POST
        Form_method: PUT</td> 
    <td>https://localhost:8443/owf/prefs/dashboard/cbf2bd69-ad7e-44f7-bf75-c838048a9c43?isdefault=true</td>
    <td></td>
  </tr>
  <tr>
    <td><b>/updateAndDeleteDashboards(cfg)</b></td>
    <td>???</td> 
    <td>https://localhost:8443/owf/prefs/dashboard/????</td>
    <td></td>
  </tr>
</table>

##MISC API Overview##
<table style="width:100%">
  <thead>
    <td>Field </td>
    <td>Method </td>
    <td>Request URL</td>
    <td>Description</td>
  </thead>
  <tr>
    <td><b>/getServerVersion(cfg)</b></td>
    <td>GET</td> 
    <td>https://localhost:8443/owf/prefs/server/resources?version=7.14.1-v1&dojo.preventCache=1425324688929</td>
    <td></td>
  </tr>
</table>







