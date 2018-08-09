# Leave of Absence Changed Event

<table align="center">
    <tr>
        <td>Description</td>
        <td>The HR system will raise an event when there is a change to an employee's leave of absence information.<br>Because employee job information is not public, a secure callback URL is provided for business applications that are authorized.</td>
    </tr>
    <tr>
        <td>Event Definition</td>
        <td>JSON Schema Definitions for Leave of Absence Changed</td>
    </tr>
    <tr>
        <td>Filters</td>
        <td>None</td>
    </tr>
    <tr>
        <td>Examples</td>
        <td>Sample for Leave of Absence Changed</td>
    </tr>
    <tr>
        <td>What other Applications raise an Event Type with this same contract</td>
        <td>N/A</td>
    </tr>
    <tr>
        <td>How do I Subscribe?</td>
        <td>Subscribe to Leave of Absence Changed Event</td>
    </tr>
    <tr>
        <td>How do I Unsubscribe?</td>
        <td>Unsubscribe from Leave of Absence Changed Event</td>
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
