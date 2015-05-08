#<b>API Object: /deleteUserPreference (cfg)</b>#

#####<i>Definition:</i> 
Use the `/deleteUserPreference` API to remove a user preference based on its namespace and name. The preference could be user metadata such as name, email, etc. IS THAT RIGHT????  

#####<i>How it works:</i>#####
A system makes a call to another system that asks to reference data instead of return it. To make this call, one of the following REST Calls will request user data from the user profile URI [IS THIS RIGHT?] 

#####<i>Request:</i>#####

#####<i>Response:</i>#####


#####<i>How to find it:</i>#####


#####<i>How to use it:</i>#####




<hr>
###<b>Example</b>###
The following is an example of a complete preference object passed to the onSuccess
function:

    {
    	"value":"true",
    	"path":"militaryTime",
    	"user":
    	{
    		"userId":"testAdmin1"
    	},
    	"namespace":"com.mycompany.AnnouncingClock"
    }

...

    function onSuccess(pref){
    	alert(pref.value);
    }
    
    function onFailure(error,status){
    	alert('Error ' + error);
    	alert(status);
    }
    
    OWF.Preferences.deleteUserPreference({
    	namespace:'com.company.widget',
    	name:'First President',
    	onSuccess:onSuccess,
    	onFailure:onFailure
    });



###Resource Information###
<table style="width:100%">
  <thead>
    <td>Parameter</td>
    <td>Description</td
  </thead>
  <tr>
    <td>{Object} cfg</td>
    <td>Use the following properties to configure the object. EXAMPLE???</td> 
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
<table style="width:100%">
  <thead>
    <td><b>Error</b></td>
    <td><b>Action</b></td>
  </thead>
  <tr>
    <td>401: You are not authorized to access this entity</td>
    <td>Seek authorization from the server administrator</td> 
  </tr> 
  <tr>
    <td>500: An unexpected error occurred</td>
    <td>Retry the call, then, if the error occurs a second time DO WHAT????</td> 
  </tr>
  <tr>
    <td>404: The user preference was not found</td>
    <td>The preference may not exist; to look for it DO WHAT????</td> 
  </tr>   
  <tr>
    <td>400: The requested entity failed to pass validation</td>
    <td>I HAVE NO IDEA????</td> 
  </tr>
 <tr>
</table> 