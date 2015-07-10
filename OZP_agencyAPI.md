#<b>API Object: marketplace.Agency</b>#

##<i>Definition</i> 
Use the `/agency` API to create, update, read or delete an agency in the system. 

##Resource Information##
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

</table>

 
##<i>Request URL</i>###

https://localhost:8443/marketplace/api/agency 

##<i>Request Methods</i>###
[POST](https://github.com/stephaniesaylor/Practice-Repo/blob/master/OZP_agencyAPI.md#POST),
[PUT](https://github.com/stephaniesaylor/Practice-Repo/blob/master/OZP_agencyAPI.md#PUT), 
[GET](https://github.com/stephaniesaylor/Practice-Repo/blob/master/OZP_agencyAPI.md#GET), [DELETE](https://github.com/stephaniesaylor/Practice-Repo/blob/master/OZP_agencyAPI.md#DELETE)
<br>
Each method will be explained in the following sections:

###<a name=POST>POST</a>####
<b>Request</b><br>
https://localhost:8443/marketplace/api/agency

    {"title":"Test Organization", 
    "shortName":"TORG"}

<b>Response Code:</b>
201

<b>Response</b> <br>

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

<b>Requirements</b> <br>
none
<br>
<br>



###<a name=PUT>PUT</a>###
<b>Request</b>
<br>
https://localhost:8443/marketplace/api/agency/{id}

    {"id":208,
    "title":"Updated Agency",
     "shortName":"sName"}

<b>Response Code:</b>
200

<b>Response</b>
<br>
    
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
<b>Requirements</b> <br>
none
<br>
<br>


###<a name=GET>GET</a>###
<b>Request</b><br>
Marketplace returns the matching agency ID, as shown below. However, if the ID is an empty string, Marketplace will return a list of all agencies.

https://localhost:8443/marketplace/api/agency/{id}

<b>Response Code:</b>
200

<b>Response</b>

    {
       "id":194,
       "shortName":"sName",
       "title":"123456",
       "_links":
       {
          "self":
          {
             "href":"https://localhost:8443/marketplace/api/agency/194"
          }
       }
    }

<b>Requirements</b> <br>
none
<br>Optional: offset, max
<br>
<br>
<br>

###<a name=DELETE>DELETE</a>###
<b>Requirements</b>
<br>https://localhost:8443/marketplace/api/agency/{id}
<br>

<b>Response Code:</b>
204

<b>Response</b>
<br>
no content<br>    
       
<b>Requirements</b> <br>
none

<br>
<br>




###<b>Possible Errors</b>###

This table lists common errors. Other errors may occur but these are the most likely:
<table style="width:100%">
  <thead>
    <td><b>Error</b></td>
    <td><b>Troubleshooting</b></td>
  </thead>
  <tr>
    <td>Agency cannot be deleted.
</td>
    <td>See if it is associated with a listing. If any listing is assigned to an agency, you cannot delete that agency.</td> 
  </tr>
  <tr>
    <td>User cannot create, edit, delete an agency.
</td>
    <td>Only administrators can create, edit, delete agencies.</td> 
  </tr>  
  <tr>
    <td>Agency cannot be created or updated.
</td>
    <td>The agency must include all required fields.</td> 
  </tr>
</table> 
