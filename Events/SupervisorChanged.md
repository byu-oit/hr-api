# Supervisor Changed Event

<table align="center">
  <tr>
    <td>Description</td>
    <td>The HR system will raise an event for all subordinates of a person when they change, or for the person themself if it is known that their supervisor has changed.<br>Because employee job information is not public, a secure callback URL is provided for business applications that are authorized.</td>
  </tr>
  <tr>
    <td>Examples</td>
    <td>Sample for Supervisor Changed<br><pre>{
  "events": {
    "event": {
      "event_header": {
        "domain": "edu.byu",
        "entity": "HR_Personal_Action",
        "event_type": "Supervisor Changed",
        "event_id": "2021020916565390201"
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
        "effective_date": "2021-02-09"
        "callback": "https://api.byu.edubyuapi/employees/v1/123456789/jobs"
      }
    }
  }
}</pre></td>
  </tr>
  <tr>
    <td>Filters</td>
    <td>Department</td>
  </tr>
  <tr>
    <td>What other applications raise an event type with this same contract?</td>
    <td>N/A</td>
  </tr>
  <tr>
    <td>How do I subscribe?</td>
    <td>Subscribe to the Supervisor Changed event<be><pre>curl -X POST
--header "Content-Type: application/json"
--header "Accept: application/json"
--header "Authorization: Bearer *****************"
-d "{
  \"subscription\": {
    \"event_type\": \"Supervisor Changed\",
    \"entity\": \"HR_Personal_Action\",
    \"domain\": \"edu.byu\"
  }
}" "https://api.byu.edu/domains/eventhub/v1/subscriptions/edu.byu/HR_Personal_Action/Supervisor%20Changed"</pre></td>
  </tr>
  <tr>
    <td>What does the callback return?</td>
    <td>The callback URL will return Supervisor Changed data for the specified byu_id.</td>
  </tr>
</table>
