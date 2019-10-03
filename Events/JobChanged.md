# Job Changed Event

<table align="center">
    <tr>
        <td>Description</td>
        <td>The HR system will raise an event when an employee changes jobs.<br>Because employee job information is not public, a secure callback URL is provided for business applications that are authorized.</td>
    </tr>
    <tr>
        <td>Examples</td>
        <td>Sample for Job Changed<br><pre>{
  "events": {
    "event": {
      "event_header": {
        "domain": "edu.byu",
        "entity": "HR_Personal_Action",
        "event_type": "Job Changed",
        "event_id": "2016092108114722607"
      },
      "filters": {
        "filter": {
          "filter_name": "department_id",
          "filter_value": "0665"
        }
      },
      "event_body": {
        "byu_id": "123456789",
        "net_id": "gocougars",
        "effective_date": "2016-09-22",
        "callback": "https://api.byu.edu/domains/erp/hr/transfer/v1?byu_id=123456789"
      }
    }
  }
}</pre></td>
    </tr>
    <tr>
        <td>Filters</td>
        <td>Department ID</td>
    </tr>
    <tr>
        <td>What other Applications raise an Event Type with this same contract</td>
        <td>N/A</td>
    </tr>
    <tr>
        <td>How do I Subscribe?</td>
        <td>Subscribe to Job Changed Event<br><pre>curl -X POST 
--header "Content-Type: application/json" 
--header "Accept: application/json" 
--header "Authorization: Bearer 26e94b41cf5a9b3f36435c1e0e35f3" 
-d "{
  \"subscription\": {
    \"event_type\": \"Job Changed\",
    \"entity\": \"HR_Personal_Action\",
    \"domain\": \"edu.byu\"
  }
}" "https://api.byu.edu:443/domains/eventhub/1.0.0/subscriptions"</pre></td>
    </tr>
    <tr>
        <td>How do I Unsubscribe?</td>
        <td>Unsubscribe from Job Changed Event<br><pre>curl -X DELETE 
--header "Accept: application/json" 
--header "Authorization: Bearer 26e94b41cf5a9b3f36435c1e0e35f3"
"https://api.byu.edu:443/domains/eventhub/1.0.0/subscriptions/edu.byu/HR_Personal_Action/Job%20Changed"</pre></td>
    </tr>
    <tr>
        <td>What does callback return?</td>
        <td>The callback URL will return Job Code data for the specified byu_id.</td>
    </tr>
    <tr>
        <td>How do I access a history of these events?</td>
        <td>Retrieve the oldest 10 Job Code Changed events from the Archive<br><br>curl -X GET<br>--header "Accept: application/json" <br>--header "Authorization: Bearer //Obtain Access Token in API Store//" <br>"https://<span></span>api.byu.edu:443/eventhub/1.0.0/events?count=10"</td>
    </tr>
    <tr>
        <td>Notes</td>
        <td>In the callback URL, you will need to replace the characters "%26" with the "&" (ampersand) character to make it a valid URL.</td>
    </tr>
</table>
