# Deathdate Changed Event

<table align="center">
    <tr>
        <td>Description</td>
        <td>The HR system will raise an event when an employee's deathdate is added, changed, or deleted.<br>An employee's date of death is not public data. A secure URL is provided for business applications that are authorized to access the information.</td>
    </tr>
    <tr>
        <td>Event Definition</td>
        <td>JSON Schema Definitions for Deathdate Changed</td>
    </tr>
    <tr>
        <td>Filters</td>
        <td>None</td>
    </tr>
    <tr>
        <td>Examples</td>
        <td>Sample for Deathdate Changed<br><pre>{
  "events": {
    "event": {
      "event_header": {
        "domain": "edu.byu",
        "entity": "HR_Personal_Action",
        "event_type": "Deathdate Changed",
        "source_dt": "2016-10-17-14.03.51.000000",
        "source_id": "HR",
        "event_id": "2016101714035102701"
      },
      "event_body": {
        "byu_id": "123456789",
        "net_id": "gocougars",
        "callback": "https://api.byu.edu/domains/erp/hr/deathdate/v1?byu_id=123456789"
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
        <td>Subscribe to Deathdate Changed Event<br><pre>curl -X POST --header "Content-Type: application/json" 
--header "Accept: application/json" 
--header "Authorization: Bearer //Obtain Access Token in API Store//" 
-d "{
  \"subscription\": {
    \"eca_identity_id\": \"\",
    \"entity\": \"HR_Personal_Action\",
    \"event_type\": \"Deathdate Changed\",
    \"domain\": \"edu.byu\",
    \"eca_identity_name\": \"\"
  }
}" "https://api.byu.edu:443/eventhub/1.0.0/subscriptions"</pre></td>
    </tr>
    <tr>
        <td>How do I Unsubscribe?</td>
        <td>Unsubscribe from Deathdate Changed Event<br><pre>curl -X DELETE --header "Accept: application/json" 
--header "Authorization: Bearer //Obtain Access Token in API Store//" 
"https://api.byu.edu:443/eventhub/1.0.0/subscriptions/edu.byu/HR_Personal_Action/Deathdate%20Changed</pre></td>
    </tr>
    <tr>
        <td>What does callback return?</td>
        <td>The callback URL will return Deathdate Code data for the specified byu_id.</td>
    </tr>
    <tr>
        <td>How do I access a history of these events?</td>
        <td>Retrieve the oldest 10 Deathdate Code Changed events from the Archive<br><br>curl -X GET<br>--header "Accept: application/json" <br>--header "Authorization: Bearer //Obtain Access Token in API Store//" <br>"https://<span></span>api.byu.edu:443/eventhub/1.0.0/events?count=10"</td>
    </tr>
    <tr>
        <td>Notes</td>
        <td>In the callback URL, you will need to replace the characters "%26" with the "&" (ampersand) character to make it a valid URL.</td>
    </tr>
</table>
