# Punch Occurred Event

<table align="center">
    <tr>
        <td>Description</td>
        <td>The HR system will raise an event when an employee's time punch is entered or created.<br>If an employee's data is restricted, a secure callback URL will be provided for business applications that are authorized.</td>
    </tr>
    <tr>
        <td>Filters</td>
        <td>Punch Source. Possible values include: MBL, WEB, PIA, PHN, IOT, CLK</td>
    </tr>
    <tr>
        <td>Examples</td>
        <td>Sample for Punch Occurred<br><pre>{
  "events": {
    "event": {
      "event_header": {
        "domain": "edu.byu",
        "entity": "HR_Personal_Action",
        "event_type": "Punch Occurred",
        "source_dt": "2017-05-22-09.53.22.000000",
        "source_id": "HR",
        "event_id": "2017052209532258601"
      },
      "filters": {
        "filter": {
          "filter_name": "punch_source",
          "filter_value": "PIA"
        }
      },
      "event_body": {
        "byu_id": "999999999",
        "net_id": "gocougars",
        "employee_record": "0",
        "punch_date": "2017-05-22",
        "punch_time": "13:30:00",
        "punch_type": "Out",
        "sequence_number": "6"
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
        <td>Subscribe to Punch Occurred Event<br><pre>curl -X POST 
--header "Content-Type: application/json" 
--header "Accept: application/json" 
--header "Authorization: Bearer xxxxx" 
-d "{
  \"subscription\": {
    \"event_type\": \"Punch Occurred\",
    \"entity\": \"HR_Personal_Action\",
    \"domain\": \"edu.byu\"
  }
}" "https://api.byu.edu:443/domains/eventhub/1.0.0/subscriptions"</pre></td>
    </tr>
    <tr>
        <td>How do I Unsubscribe?</td>
        <td>Unsubscribe from Punch Occurred Event<br><pre>curl -X DELETE 
--header "Accept: application/json" 
--header "Authorization: Bearer xxxxx"
"https://api.byu.edu:443/domains/eventhub/1.0.0/subscriptions/edu.byu/HR_Personal_Action/Punch%20occurred"</pre></td>
    </tr>
    <tr>
        <td>What does callback return?</td>
        <td>The callback URL will return Punch Occurred data for the specified byu_id.</td>
    </tr>
    <tr>
        <td>How do I access a history of these events?</td>
        <td>Retrieve the oldest 10 Punch Occurred events from the Archive<br><br>curl -X GET<br>--header "Accept: application/json" <br>--header "Authorization: Bearer //Obtain Access Token in API Store//" <br>"https://<span></span>api.byu.edu:443/eventhub/1.0.0/events?count=10"</td>
    </tr>
    <tr>
        <td>Notes</td>
        <td>In the callback URL, you will need to replace the characters "%26" with the "&" (ampersand) character to make it a valid URL.</td>
    </tr>
</table>
