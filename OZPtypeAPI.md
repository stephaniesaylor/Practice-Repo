#<b>API Object: marketplace.type</b>#

#####<i>Definition:</i> 
Use the `/type` API to create or return a type or list of types in the system. 
 

#####<i>How it works:</i>#####
A system makes a call to Marketplace asking to create or view a type or list of types. To make this call, one of the following REST Calls will request a type media type. **????Is this right?**  

#####<i>Request URL:</i>#####

https://localhost:8443/marketplace/api/type 

#####<i>Request Method:</i>#####
POST, GET, Form_Method:none  **???? where do i find form method?**

#####<i>Requirements:</i>#####
none

Optional: offset, max

#####<i>Response:</i>#####
Marketplace returns the matching type ID, as shown below. However, if the ID is an empty string, Marketplace will return a list of all types.

{
  "id": 1,
  "description": "A small or highly specialized application",
  "title": "Widget",
  "_links": {
    "self": {
      "href": "https://localhost:8443/marketplace/api/type/1"
    }
  }
}




#####<i>How to use it:</i>#####
Use it to create or identify information about a type or view all types data in Marketplace.  

<hr>
###<b>Example</b>###


The following is an example of a call to get a type ID:
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
    <td>The numerical ID associated with the type object.</td> 
    </tr>
  <tr>
    <td>description</td>
    <td>Information about the type that is provided by an administrator.</td> 
  </tr>
  <tr>
    <td>title</td>
    <td>The name of the type.</td> 
  </tr>
  <tr>
    <td>"_links": {<br>
        				"self": { <br>
					"href":</td>
    <td>The link that identifies a specific type by ID.</td> 
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
