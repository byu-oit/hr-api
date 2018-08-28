# Addres Changed Event

<table align="center">
    <tr>
        <td>Description</td>
        <td>The HR system will raise an event when an address is added, changed, or deleted.<br>The address is considered public directory information and it is included in the event message. In the rare case that a person's record is restricted or the address is unlisted, a secure URL is provided for business applications that are authorized.</td>
    </tr>
    <tr>
        <td>Event Definition</td>
        <td>JSON Schema Definitions for Address Changed:<br><pre>{ "address":
   { "employee":
      { "byu_id":
      { "type": "string",
        "maxLength": 9 },
        "address":
      { "type": "string",
        "maxLength": 40,
        "description": "This item will be left blank if 'unlisted' is set to 'Y'."},
        "address_type": { "type": "string", "maxLength": 3, "enum": ["MAL","PRM","RES","WRK"] },
        "country":
      { "type": "string",
        "maxLength": 3, 
        "description": "This item will be left blank if 'unlisted' is set to 'Y'."},
        "effective_date":
      { "type": "string",
        "format": "date-time" },
        "city": { "type": "string",
        "maxLength": 30,
        "description": "This item will be left blank if 'unlisted' is set to 'Y'." },
        "state":
      { "type": "string",
        "maxLength": 6,
        "description": "This item will be left blank if 'unlisted' is set to 'Y'." },
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
        <td>Sample for Address Changed:<br><pre>
  "events": {
    "event": [
      {
        "event_header": {
          "domain": "edu.byu",
          "entity": "HR_Personal_Action",
          "event_type": "Address Changed",
          "event_id": "2016111100592953701",
          "source_dt": "2016-11-11-00.59.29.000000"
        },
        "event_body" :{ 
        "byu_id": "123456789",
        "net_id": "gocougars",
        "callback": "https://api.byu.edu/domains/erp/hr/address?byu_id=123456789"
        }
      }
        ]
     }
    }</pre></td>
    </tr>
    <tr>
        <td>What other Applications raise an Event Type with this same contract</td>
        <td>N/A</td>
    </tr>
    <tr>
        <td>How do I Subscribe?</td>
        <td>Subscribe to Address Changed Event<br><pre>curl -X POST
        --header "Content-Type: application/json"
        --header "Accept: application/json"
        --header "Authorization: Bearer //Obtain Access Token in API Store//"
        -d "{ \"subscription\":  
                {   
                    \"eca_identity_id\": \"\",
                    \"entity\": \"HR_Personal_Action\",
                    \"event_type\": \"Address Changed\",
                    \"domain\": \"edu.byu\",
                    \"eca_identity_name\": \"\" 
                } 
            }"
        "https://api.byu.edu:443/eventhub/1.0.0/subscriptions"</pre></td>
    </tr>
    <tr>
        <td>How do I Unsubscribe?</td>
        <td>Unsubscribe from Address Changed Event<br><pre>curl -X DELETE
        --header "Accept: application/json"
        --header "Authorization: Bearer //Obtain Access Token in API Store//" 
        "https://api.byu.edu:443/eventhub/1.0.0/subscriptions/edu.byu/HR_Personal_Action/Address%20Changed</pre></td>
    </tr>
    <tr>
        <td>What does the secure_url return?</td>
        <td>The callback URL will return Address information for the specified byu_id as of the effective date specified.</td>
    </tr>
    <tr>
        <td>How do I access a history of these events?</td>
        <td>Retrieve the most recent 10 Address Changed events from the Archive<br>curl -X GET<br>--header "Accept: application/json"<br> --header "Authorization: Bearer //Obtain Access Token in API Store//" <br>"htt<span></span>ps://api.byu.edu:443/eventhub/1.0.0/events?count=10"</td>
    </tr>
    <tr>
        <td>Notes</td>
        <td>In the callback URL, you will need to replace the characters "%26" with the "&" (ampersand) character to make it a valid URL.</td>
    </tr>
</table>
