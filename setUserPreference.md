#<b>API Object: OWF.Preferences.setUserPreference(cfg)</b>#

#####<i>Definition:</i> 
Use the `/setUserPreference` API to change a user preference based on its namespace and name. The preference could be user metadata such as name, email, etc.
 

#####<i>How it works:</i>#####
A system makes a call to another system that asks to change data about a preference for example...ADD EXAMPLES.  

#####<i>Request URL:</i>#####

https://localhost:8443/owf/prefs/preference/com.company.widget/First%20President

#####<i>Request Method:</i>#####
POST <br>
Request Form Data _method:PUT <br>
value: some value???? GIVE EXAMPLE?

#####<i>Requirements:</i>#####

Requirements: namespace, name and value <br>

- If name or namespace are null, it will fill them in with “undefined” and create a preference using that information.
- If name or namespace are a non-null empty string, it will throw an HTML 404 error saying “The requested resource is not available.”
- If value is null, it will throw an HTML error.


#####<i>Response:</i>#####
If there is a preference matching the given namespace and name, it will change the value of the preference, if there is not it will create a new preference. Either way it will return the preference information, eg:

`{"id":157,"namespace":"com.company.widget","path":"First President","value":"fooval","user":{"userId":"testUser1"}}`



#####<i>How to use it:</i>#####
This API alls a remote system to create or update preferences. 

<hr>
###<b>Example</b>###

    function onSuccess(pref) {alert(pref.value)}
    function onFailure(error,status) {
	    alert('Error ' + error)
	    alert(status)
    }
    var cfg = {
        namespace: 'com.company.widget',
        name: 'First President',
        onSuccess: onSuccess,
        onFailure: onFailure,
        value: “some value”
    };

    OWF.Preferences.setUserPreference(cfg);

###Resource Information##
NOT SURE IF WE NEED THIS SECTION, if we do, it needs updated
<table style="width:100%">
  <thead>
    <td>Parameter</td>
    <td>Description</td
  </thead>
  <tr>
    <td>{Object} cfg</td>
    <td>Use the following properties to configure the object.</td> 
    </tr>
  <tr>
    <td>{String} cfg.namespace</td>
    <td>The namespace of the user preference.</td> 
  </tr>
  <tr>
    <td>{String} cfg.name</td>
    <td>The name of the user preference.</td> 
  </tr>
  <tr>
    <td>{Function} cfg.onSuccess</td>
    <td>The function that will be called if the user preference is successfully deleted from the database.</td> 
  </tr>
  <tr>
    <td>{Function} cfg.onFailure <i>Optional</i></td>
    <td>The system returns this function if the user preference cannot be deleted from the database or if the preference does not exist. If this function is not specified a default error message display.<br> 
    This function passes back the following parameters: <br>error: String
    <br>Status: The HTTP Status code</td> 
  </tr>
</table>


###<b>Possible Errors</b>###
<table style="width:75%">
  <thead>
    <td><b>Error</b></td>
    <td><b>Action</b></td>
  </thead>
  <tr>
    <td>HTTP status 400:”The requested entity failed to pass validation...on field 'path': rejected value [null]”</td>
    <td>Make sure that name is not an empty string.</td> 
  </tr> 
  <tr>
    <td>HTTP status 400:”The requested entity failed to pass validation...on field 'value': rejected value [null]”</td>
    <td>Make sure that value is set to a non-null string.</td> 
  </tr> 
  <tr>
    <td>HTTP Status 403: “Access to the specified resource has been forbidden.”</td>
    <td>Make sure namespace is not an empty string.</td> 
  </tr> 
</table> 
