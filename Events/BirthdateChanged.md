# Birthdate Changed Event

<table align="center">
    <tr>
        <td>Description</td>
        <td>The HR system will raise an event when an employee's birthdate is added, changed, or deleted.<br>The birthdate is not considered public data so birthdate information is not included in the event message. A secure URL is provided for business applications that are authorized to access the unlisted information.</td>
    </tr>
    <tr>
        <td>Event Definition</td>
        <td>JSON Schema Definitions for Birthdate Changed:<br><pre>{   
   "birthdate":{   
      "employee":{   
         "byu_id": {
          "type": "string",
          "maxLength": 9
		},
	  "birthdate": {
          "type": "string",
          "format": "date-time"
          "maxLength": 10,
          "description": "This item will be left blank if 'unlisted' is set to 'Y'."       
        },
      }
   }
}</pre></td>
    </tr>
    <tr>
        <td>Filters</td>
        <td>None</td>
    </tr>
    <tr>
        <td>Examples</td>
        <td>Sample for Birthdate Changed:<br><pre>{
  "events": {
    "event": {
      "event_header": {
        "domain": "edu.byu",
        "entity": "HR_Personal_Action",
        "event_type": "Birthdate Changed",
        "source_dt": "2016-11-11-00.59.29.000000",
        "source_id": "HR",
        "event_id": "2016111100592949501"
      },
      "event_body": {
        "byu_id": "123456789",
        "net_id": "gocougars",
        "callback": "https://api.byu.edu/domains/erp/hr/birthdate/v1?byu_id=123456789"
      }
    }
  }
}</pre></td>
    </tr>
    <tr>
        <td>What other Applications raise an Event Type with this same contract</td>
        <td>N/A</td>
    </tr>
    <tr>
        <td>How do I Subscribe?</td>
        <td>Subscribe to Birthdate Changed Event<br><pre>curl -X POST --header "Content-Type: application/json" 
--header "Accept: application/json" 
--header "Authorization: Bearer //Obtain Access Token in API Store//" 
-d "{
  \"subscription\": {
    \"eca_identity_id\": \"\",
    \"entity\": \"HR_Personal_Action\",
    \"event_type\": \"Birthdate Changed\",
    \"domain\": \"edu.byu\",
    \"eca_identity_name\": \"\"
  }
}" "https://api.byu.edu:443/eventhub/1.0.0/subscriptions"</pre></td>
    </tr>
    <tr>
        <td>How do I Unsubscribe?</td>
        <td>Unsubscribe from Birthdate Changed Event<br><pre>curl -X DELETE --header "Accept: application/json" 
--header "Authorization: Bearer //Obtain Access Token in API Store//"
"https://api.byu.edu:443/eventhub/1.0.0/subscriptions/edu.byu/HR_Personal_Action/Birthdate%20Changed</pre></td>
    </tr>
    <tr>
        <td>What does callback return?</td>
        <td>The callback URL will return Birthdate Code data for the specified byu_id.</td>
    </tr>
    <tr>
        <td>How do I access a history of these events?</td>
        <td>Retrieve the oldest 10 Birthdate Changed events from the Archive<br><br>curl -X GET<br>--header "Accept: application/json" <br>--header "Authorization: Bearer //Obtain Access Token in API Store//" <br>"https://<span></span>api.byu.edu:443/eventhub/1.0.0/events?count=10"</td>
    </tr>
    <tr>
        <td>Notes</td>
        <td>In the callback URL, you will need to replace the characters "%26" with the "&" (ampersand) character to make it a valid URL.</td>
    </tr>
</table>
