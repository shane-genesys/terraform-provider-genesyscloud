---
page_title: "genesyscloud_architect_ivr Resource - terraform-provider-genesyscloud"
subcategory: ""
description: |-
  Genesys Cloud IVR config
---
# genesyscloud_architect_ivr (Resource)

Genesys Cloud IVR config

## API Usage
The following Genesys Cloud APIs are used by this resource. Ensure your OAuth Client has been granted the necessary scopes and permissions to perform these operations:

* [GET /api/v2/architect/ivrs](https://developer.genesys.cloud/api/rest/v2/architect/#get-api-v2-architect-ivrs)
* [POST /api/v2/architect/ivrs](https://developer.genesys.cloud/api/rest/v2/architect/#post-api-v2-architect-ivrs)
* [GET /api/v2/architect/ivrs/{ivrId}](https://developer.genesys.cloud/api/rest/v2/architect/#get-api-v2-architect-ivrs--ivrId-)
* [PUT /api/v2/architect/ivrs/{ivrId}](https://developer.genesys.cloud/api/rest/v2/architect/#put-api-v2-architect-ivrs--ivrId-)
* [DELETE /api/v2/architect/ivrs/{ivrId}](https://developer.genesys.cloud/api/rest/v2/architect/#delete-api-v2-architect-ivrs--ivrId-)


## Example Usage

```terraform
resource "genesyscloud_architect_ivr" "test_ivr" {
  name                  = "Sample IVR"
  description           = "A sample IVR configuration"
  dnis                  = ["+13175550000", "+13175550001"]
  open_hours_flow_id    = "0d9e9ae3-28ed-476b-9364-585f896f4f9d"
  closed_hours_flow_id  = "c49e3d66-4014-49e6-9c6e-13e3e94e5700"
  holiday_hours_flow_id = "736e05d0-6b13-41f8-a2d0-cfba8e826ea3"
  schedule_group_id     = "decb6506-e534-4707-9329-293a3aca38d8"
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- **name** (String) Name of the IVR config.

### Optional

- **closed_hours_flow_id** (String) ID of inbound call flow for closed hours.
- **description** (String) IVR Config description.
- **dnis** (Set of String) The phone number(s) to contact the IVR by.
- **holiday_hours_flow_id** (String) ID of inbound call flow for holidays.
- **id** (String) The ID of this resource.
- **open_hours_flow_id** (String) ID of inbound call flow for open hours.
- **schedule_group_id** (String) Schedule group ID.

