---
page_title: "genesyscloud_telephony_providers_edges_phonebasesettings Resource - terraform-provider-genesyscloud"
subcategory: ""
description: |-
  Genesys Cloud Phone Base Settings
---
# genesyscloud_telephony_providers_edges_phonebasesettings (Resource)

Genesys Cloud Phone Base Settings

## API Usage
The following Genesys Cloud APIs are used by this resource. Ensure your OAuth Client has been granted the necessary scopes and permissions to perform these operations:

* [GET /api/v2/telephony/providers/edges/phonebasesettings](https://developer.genesys.cloud/api/rest/v2/telephonyprovidersedge/#get-api-v2-telephony-providers-edges-phonebasesettings)
* [POST /api/v2/telephony/providers/edges/phonebasesettings](https://developer.genesys.cloud/api/rest/v2/telephonyprovidersedge/#post-api-v2-telephony-providers-edges-phonebasesettings)
* [GET /api/v2/telephony/providers/edges/phonebasesettings/{phoneBaseId}](https://developer.genesys.cloud/api/rest/v2/telephonyprovidersedge/#get-api-v2-telephony-providers-edges-phonebasesettings--phoneBaseId-)
* [DELETE /api/v2/telephony/providers/edges/phonebasesettings/{phoneBaseId}](https://developer.genesys.cloud/api/rest/v2/telephonyprovidersedge/#delete-api-v2-telephony-providers-edges-phonebasesettings--phoneBaseId-)
* [PUT /api/v2/telephony/providers/edges/phonebasesettings/{phoneBaseId}](https://developer.genesys.cloud/api/rest/v2/telephonyprovidersedge/#put-api-v2-telephony-providers-edges-phonebasesettings--phoneBaseId-)

## Example Usage

```terraform
resource "genesyscloud_telephony_providers_edges_phonebasesettings" "examplePhoneBaseSettings" {
  name               = "example phone base settings"
  description        = "test description"
  phone_meta_base_id = "generic_sip.json"
  properties {
    phone_label         = "Generic SIP Phone"
    phone_max_line_keys = 1
    phone_mwi_enabled   = true
    phone_mwi_subscribe = true
    phone_standalone    = false
    phone_stations      = ["station 1"]
  }
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- **name** (String) The name of the entity.
- **phone_meta_base_id** (String) A phone metabase is essentially a database for storing phone configuration settings, which simplifies the configuration process.

### Optional

- **capabilities** (Block List, Max: 1) Phone Capabilities. (see [below for nested schema](#nestedblock--capabilities))
- **description** (String) The resource's description.
- **id** (String) The ID of this resource.
- **line_base_settings_id** (String) Computed line base settings id
- **properties** (Block Set) phone base settings properties (see [below for nested schema](#nestedblock--properties))

<a id="nestedblock--capabilities"></a>
### Nested Schema for `capabilities`

Optional:

- **allow_reboot** (Boolean) Allow Reboot
- **cdm** (Boolean) CDM
- **dual_registers** (Boolean) Dual Registers
- **hardware_id_type** (String) HardwareId Type
- **media_codecs** (List of String) Media Codecs
- **no_cloud_provisioning** (Boolean) No Cloud Provisioning
- **no_rebalance** (Boolean) No Rebalance
- **provisions** (Boolean) Provisions
- **registers** (Boolean) Registers


<a id="nestedblock--properties"></a>
### Nested Schema for `properties`

Optional:

- **phone_ignore_on_secondary** (Boolean) Defaults to `true`.
- **phone_label** (String) Defaults to `WebRTC Phone Connections`.
- **phone_max_line_keys** (Number) Defaults to `1`.
- **phone_media_codecs** (List of String)
- **phone_media_dscp** (Number) Defaults to `46`.
- **phone_mwi_enabled** (Boolean) Defaults to `true`.
- **phone_mwi_subscribe** (Boolean) Defaults to `true`.
- **phone_sip_dscp** (Number) Defaults to `24`.
- **phone_standalone** (Boolean) Defaults to `false`.
- **phone_stations** (List of String)
