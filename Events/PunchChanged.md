# Punch Changed Event

<table align="center">
    <tr>
        <td>Description</td>
        <td>The HR system will raise an event when an employee's time punch is changed and includes the previous and new values.<br>If an employee's data is restricted, a secure callback URL will be provided for business applications that are authorized.</td>
    </tr>
    <tr>
        <td>Event Definition</td>
        <td>JSON Schema Definitions for Punch Changed</td>
    </tr>
    <tr>
        <td>Filters</td>
        <td>Punch Source. Possible values include: MBL, WEB, PIA, PHN, IOT, CLK</td>
    </tr>
    <tr>
        <td>Examples</td>
        <td>Sample for Punch Changed</td>
    </tr>
    <tr>
        <td>What other Applications raise an Event Type with this same contract</td>
        <td>N/A</td>
    </tr>
    <tr>
        <td>How do I Subscribe?</td>
        <td>Subscribe to Punch Changed Event</td>
    </tr>
    <tr>
        <td>How do I Unsubscribe?</td>
        <td>Unsubscribe from Punch Changed Event</td>
    </tr>
    <tr>
        <td>What does callback return?</td>
        <td>The callback URL will return Punch Code data for the specified byu_id.</td>
    </tr>
    <tr>
        <td>How do I access a history of these events?</td>
        <td>Retrieve the oldest 10 Punch Code Changed events from the Archive<br><br>curl -X GET<br>--header "Accept: application/json" <br>--header "Authorization: Bearer //Obtain Access Token in API Store//" <br>"https://<span></span>api.byu.edu:443/eventhub/1.0.0/events?count=10"</td>
    </tr>
    <tr>
        <td>Notes</td>
        <td>In the callback URL, you will need to replace the characters "%26" with the "&" (ampersand) character to make it a valid URL.</td>
    </tr>
</table>
