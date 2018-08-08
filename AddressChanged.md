# Addres Changed Event

<table align="center">
    <tr>
        <td>Description</td>
        <td>The HR system will raise an event when an address is added, changed, or deleted.<br>The address is considered public directory information and it is included in the event message. In the rare case that a person's record is restricted or the address is unlisted, a secure URL is provided for business applications that are authorized.</td>
    </tr>
    <tr>
        <td>Event Definition</td>
        <td>JSON Schema Definitions for Address Changed</td>
    </tr>
    <tr>
        <td>Filters</td>
        <td>None</td>
    </tr>
    <tr>
        <td>Examples</td>
        <td>Sample for Address Changed</td>
    </tr>
    <tr>
        <td>What other Applications raise an Event Type with this same contract</td>
        <td>N/A</td>
    </tr>
    <tr>
        <td>How do I Subscribe?</td>
        <td>Subscribe to Address Changed Event</td>
    </tr>
    <tr>
        <td>How do I Unsubscribe?</td>
        <td>Unsubscribe from Address Changed Event</td>
    </tr>
    <tr>
        <td>What does the secure_url return?</td>
        <td>The callback URL will return Address information for the specified byu_id as of the effective date specified.</td>
    </tr>
    <tr>
        <td>How do I access a history of these events?</td>
        <td>Retrieve the most recent 10 Address Changed events from the Archive</td>
    </tr>
    <tr>
        <td>Notes</td>
        <td>In the callback URL, you will need to replace the characters "%26" with the "&" (ampersand) character to make it a valid URL.</td>
    </tr>
</table>
