# Leave of Absence Changed Event

<table align="center">
    <tr>
        <td>Description</td>
        <td>The HR system will raise an event when there is a change to an employee's leave of absence information.<br>Because employee job information is not public, a secure callback URL is provided for business applications that are authorized.</td>
    </tr>
    <tr>
        <td>Filters</td>
        <td>Department ID</td>
    </tr>
    <tr>
        <td>Examples</td>
        <td>Sample for Leave of Absence Changed<br><pre>{
  "events": {
    "event": {
      "event_header": {
        "domain": "edu.byu",
        "entity": "HR_Personal_Action",
        "event_type": "Leave of Absence Changed",
        "source_dt": "2016-11-07-13.48.13.000000",
        "source_id": "HR",
        "event_id": "2016110713481378701"
      },
      "filters": {
        "filter": {
          "filter_name": "deptid",
          "filter_value": "2052"
        }
      },
      "event_body": {
        "byu_id": "123456789",
        "net_id": "gocougars",
        "effective_date": "2016-10-31",
        "callback": "https://api.byu.edu/domains/erp/hr/leave_of_absence/v1?byu_id=123456789%26effective_date=2016-10-31"
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
        <td>Subscribe to Leave of Absence Changed Event<br><pre>curl -X POST 
--header "Content-Type: application/json" 
--header "Accept: application/json" 
--header "Authorization: Bearer 26e94b41cf5a9b3f36435c1e0e35f3" 
-d "{
  \"subscription\": {
    \"event_type\": \"Leave of Absence Changed\",
    \"entity\": \"HR_Personal_Action\",
    \"domain\": \"edu.byu\"
  }
}" "https://api.byu.edu:443/domains/eventhub/1.0.0/subscriptions"</pre></td>
    </tr>
    <tr>
        <td>How do I Unsubscribe?</td>
        <td>Unsubscribe from Leave of Absence Changed Event<br><pre>curl -X DELETE 
--header "Accept: application/json" 
--header "Authorization: Bearer 26e94b41cf5a9b3f36435c1e0e35f3"
"https://api.byu.edu:443/domains/eventhub/1.0.0/subscriptions/edu.byu/HR_Personal_Action/Leave%20of%20Absence%20Changed"</pre></td>
    </tr>
    <tr>
        <td>What does callback return?</td>
        <td>The callback URL will return Leave of Absence Code data for the specified byu_id.</td>
    </tr>
    <tr>
        <td>How do I access a history of these events?</td>
        <td>Retrieve the oldest 10 Leave of Absence Code Changed events from the Archive<br><br>curl -X GET<br>--header "Accept: application/json" <br>--header "Authorization: Bearer //Obtain Access Token in API Store//" <br>"https://<span></span>api.byu.edu:443/eventhub/1.0.0/events?count=10"</td>
    </tr>
    <tr>
        <td>Notes</td>
        <td>In the callback URL, you will need to replace the characters "%26" with the "&" (ampersand) character to make it a valid URL.</td>
    </tr>
</table>
