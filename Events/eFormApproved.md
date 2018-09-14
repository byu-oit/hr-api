# eForm Approved Event

<table align="center">
    <tr>
        <td>Description</td>
        <td>The HR system will raise an event when an eForm is approved at the front desk.</td>
    </tr>
    <tr>
        <td>Event Definition</td>
        <td>JSON Schema Definitions for Address Changed:<br><pre></pre></td>
    </tr>
    <tr>
        <td>Filters</td>
        <td>None</td>
    </tr>
    <tr>
        <td>Examples</td>
        <td>Sample for eForm Approved by the Front Desk:<br><pre>{
  "events": {
    "event": {
      "event_header": {
        "domain": "edu.byu",
        "entity": "HR_Personal_Action",
        "event_type": "eForm Approved at Front Desk",
        "source_dt": "2018-06-29T07:46:38.000000-06:00",
        "event_dt": null,
        "source_id": "HR",
        "dispatch_id": null,
        "event_id": "1234567890123456789"
      },
      "filters": [
        "filter": {
          "filter_name": null,
          "filter_value": null
        }
      ],
      "event_body": {
        "byu_id": "123456789",
        "net_id": "cougar",
        "updated_by": "brigham",
        "callback": "https://api.byu.edu/domains/erp/hr/eform/v1?form_id=1234567",
        "form_id": "1234567",
        "effective_date": "2018-07-23"
      },
      "history": {
        
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
        <td>Subscribe to eForm Approved by the Front Desk Event<br><pre></pre>curl -X POST 
--header "Content-Type: application/json" 
--header "Accept: application/json" 
--header "Authorization: Bearer xxxxxx" 
-d "{
  \"subscription\": {
    \"event_type\": \"eForm Approved by the Front Desk\",
    \"entity\": \"HR_Personal_Action\",
    \"domain\": \"edu.byu\"
  }
}" "https://api.byu.edu:443/domains/eventhub/1.0.0/subscriptions"</td>
    </tr>
    <tr>
        <td>How do I Unsubscribe?</td>
        <td>Unsubscribe from eForm Approved by the Front Desk  Event<br><pre>curl -X DELETE 
--header "Accept: application/json" 
--header "Authorization: Bearer xxxxxx"
"https://api.byu.edu:443/domains/eventhub/1.0.0/subscriptions/edu.byu/HR_Personal_Action/eForm%20Approved%20by%20the%20Front%20Desk"</pre></td>
    </tr>
    <tr>
        <td>What does the secure_url return?</td>
        <td>The callback URL will return the eForm sepecified by the response.</td>
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
