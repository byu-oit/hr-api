# Faculty Profile API

The faculty profile web service takes the incoming web service request, applies security and access rights restrictions, and forwards the ammended request to the Digital Measures endpoint.  The response is then simply passed along to the calling application.

## Response Types
Because Digital Measures only supports XML responses, the Faculty Profile API only supports XML responses.

## Visibility Flags
As a developer, please be aware of the Visibility Flag and apply it's use in your application.

When a faculty member enters certain groups of data in Faculty Profile, there is a flag they can check that indicates “Make available for college Faculty Directory website.”  The help text reads:  “Some colleges use data from Faculty Profile for their faculty directory websites. If this is the practice in your college, please check this box if you want the college to include the data in this record.”