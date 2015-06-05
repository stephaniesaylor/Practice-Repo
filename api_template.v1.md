

#Legacy APIs#
The legacy APIs allowed you to query metadata about users, widgets, dashboards and server version. 
The API uses REST principles; you can use your browser to access URLs and interact with it.
The first section of this document provides a brief overview of the API, detailed explanations and use cases follow. 
##Base URL##
All examples in this document use the following base URL:

    https://localhost:8443/marketplace/api/prefs/


##User API Overview##
You can use the User Preference APIs find (GET) a current user's information (MAKE MORE SPECIFIC) or update his or her preferences in a number of ways (DELETE, SET, etc.). 

<table style="width:55%">
  <thead>
    <td>Call </td>
    <td> Response Description </td>
  </thead>
  <tr>
    <td><b>/getCurrentUser(cfg)</b></td>
    <td></td> 
  </tr>
</table>

##Preference API Overview##
You can use the User Preference APIs find (GET) a current user's information (MAKE MORE SPECIFIC) or update his or her preferences in a number of ways (DELETE, SET, etc.). 

<table style="width:100%">
  <thead>
    <td><b>Call</b></td>
    <td><b>Response Description and Example</b></td>
  </thead>
  <tr>
    <td><b><a href=https://github.com/stephaniesaylor/Practice-Repo/blob/master/deleteUserPreference.md>"OWF.Preferences.deleteUserPreference(cfg)"</a></b></td>
    <td> The preference was deleted.
    <br>
    var cfg = { <br>
  	<b>namespace:</b> 'com.company.widget', <br>
	<b>name:</b> 'First President', <br>
	<b>onSuccess:</b> onSuccess, <br>
	<b>onFailure:</b> onFailure 
};

</td> 
        
  </tr>
  <tr>
    <td><b><a href=https://github.com/stephaniesaylor/Practice-Repo/blob/master/doesUserPreferenceExist.md>"OWF.Preferences.doesUserPreferenceExist(cfg)"</a></b></td></td>
    <td> {"preferenceExist":true,"statusCode":200}</td> 
  </tr>
  <tr>
    <td><b><a href=https://github.com/stephaniesaylor/Practice-Repo/blob/master/getUserPreference.md>"OWF.Preferences.getUserPreference(cfg)"</a></b></td>
    <td>{
	"<b>id</b>":157,<br>
	"<b>namespace</b>":"foo.bar.0",<br>
	"<b>path</b>":"testpath0",<br>
	"<b>value</b>":"fooval",<br>
	"<b>user</b>":{
		"userId":"testAdmin1"
	}
}
 </td> 
  </tr>
  <tr>
    <td><b><a href=https://github.com/stephaniesaylor/Practice-Repo/blob/master/setUserPreference.md>"OWF.Preferences.setUserPreference(cfg)"</a></b></td>
    <td>Returns the preference that was set. <br>
    {
	"<b>id</b>":157,<br>
	"<b>namespace</b>":"foo.bar.0",<br>
	"<b>path</b>":"testpath0",<br>
	"<b>value</b>":"fooval",<br>
	"<b>user</b>":{
		"userId":"testAdmin1"
	}
}
</td> 
  </tr>
</table>

##Widget API Overview##
You can use the Widget APIs to get specific information about a widget, find a widget or update and delete widgets.

<table style="width:100%">
  <thead>
    <td><b>Call</td>
    <td><b>Response Description and Example</b></td>
  </thead>
  <tr>
    <td><b><a href=https://github.com/stephaniesaylor/Practice-Repo/blob/master/findWidget.md>"OWF.Preferences.findWidget(cfg)"</a></b></td>
    <td>The whole widgetID (this includes all of the widgets metadata) for every widget in the system.</b></td>
  </tr>
  <tr>
    <td><b><a href=https://github.com/stephaniesaylor/Practice-Repo/blob/master/getWidget.md>"OWF.Preferences.getWidget(cfg)"</a></b></td>
    <td>The whole widgetID (this includes all of the widgets metadata)</td> 
  </tr>
  <tr>
    <td><b>/updateAndDeleteWidgets(cfg)</b></td>
    <td></td> 
  </tr>
</table>


##Dashboard API Overview##
<table style="width:100%">
  <thead>
  <thead>
    <td><b>Call</td>
    <td><b>Response Description and Example</b></td>
  </thead>
  <tr>
    <td>/cloneDashboard(cfg)</td>
    <td>...</td> 
  </tr>
  <tr>
    <td>/createOrUpdateDashboard(cfg)</td>
    <td>...</td> 
  </tr>
  <tr>
    <td>/createOrUpdateDashboard(cfg)</td>
    <td>...</td> 
  </tr>
  <tr>
    <td>/deleteDashboard(cfg)</td>
    <td>...</td> 
  </tr>
  <tr>
    <td>/findDashboards(cfg)</td>
    <td>...</td> 
  </tr>
  <tr>
    <td>/findDashboardsByType(cfg)</td>
    <td>...</td> 
  </tr>
  <tr>
    <td>/getDashboard(cfg)</td>
    <td>...</td> 
  </tr>
  <tr>
    <td>/getDefaultDashboard(cfg)</td>
    <td>...</td> 
  </tr>
  <tr>
    <td>/setDefaultDashboard(cfg)</td>
    <td>...</td> 
  </tr>
  <tr>
    <td>/updateAndDeleteDashboards(cfg)</td>
    <td>...</td> 
  </tr>
</table>

##MISC API Overview##
<table style="width:100%">
  <thead>
    <td><b>Call</b></td>
    <td><b>Response Description and Example </b></td>
  </thead>
  <tr>
    <td>/getServerVersion(cfg)</td>
    <td>...</td> 
  </tr>
</table>







