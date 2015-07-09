#<b>API Object: marketplace.AgencyResource</b>#

#####<i>Definition:</i> 
Use the `/agency` API to create, update, read or delete an agency in the system. 
 

#####<i>How it works:</i>#####
A system makes a call to Marketplace regarding an agency. To make this call, one of the following REST Calls will request an agency media type. **????Is this right?**  

#####<i>Request URL:</i>#####

https://localhost:8443/marketplace/api/agency 

#####<i>Request Method:</i>#####
POST, PUT, GET, DELETE 
Form_Method:none  **???? where do i find form method?**

#####<i>Requirements:</i>#####
none

Optional: offset, max

#####<i>Response:</i>#####
Marketplace returns the matching agency ID, as shown below. However, if the ID is an empty string, Marketplace will return a list of all agencies.

{
  "id": 1,
  "shortName": "TORG",
  "title": "Test Organization",
  "_links": {
    "self": {
      "href": "https://localhost:8443/marketplace/api/agency/1"
    }
  }
}




#####<i>How to use it:</i>#####
Use it to find, update or delete specific information about an agency or view all agency data in Marketplace.  

<hr>
###<b>Example</b>###


The following is an example of a call to get an agency ID:
**???? I don't know how to do this**

    This is **NOT** accurate--just placeholder

    var onSuccess = function(obj) {
        if (obj.value) {
            alert(obj.value.namespace);
        }
    };

    var onFailure = function(error) {
        alert(error);
    };

    OWF.Preferences.getWidget({
        widgetId:'eb5435cf-4021-4f2a-ba69-dde451d12551',
        onSuccess:onSuccess,
        onFailure:onFailure
    });

    



###Resource Information###
<table style="width:100%">
  <thead>
    <td><b>Parameter</b></td>
    <td><b>Description</b></td
  </thead>
  <tr>
    <td>id</td>
    <td>The numerical ID associated with the agency object.</td> 
    </tr>
  <tr>
    <td>shortName</td>
    <td>The abbreviation used to identify the agency on listings' short and detailed views.</td> 
  </tr>
  <tr>
    <td>title</td>
    <td>The name of the agency.</td> 
  </tr>
  <tr>
    <td>"_links": {<br>
        				"self": { <br>
					"href":</td>
    <td>The link that identifies a specific agency by ID.</td> 
  </tr>
</table>


###<b>Possible Errors</b>###

**???? where do i find the errors? NOT ACCURATE**
<table style="width:100%">
  <thead>
    <td><b>Error</b></td>
    <td><b>Action</b></td>
  </thead>
  <tr>
    <td>This will happen when getWidget is called using a widgetId that doesn't exist.
HTTP Status 404: “...Widget with guid of undefined not found.”
</td>
    <td>Make sure widgetId is set to a non-null string.</td> 
  </tr> 
</table> 
