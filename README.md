# ![LOGO](logo.png) Service Control **flow**ground Connector

## Description

A generated **flow**ground connector for the Service Control API (version v1).

Generated from: https://api.apis.guru/v2/specs/googleapis.com/servicecontrol/v1/swagger.json<br/>
Generated at: 2019-05-07T17:41:56+03:00

## API Description

Provides control plane functionality to managed services, such as logging, monitoring, and status checks.

## Authorization

Supported authorization schemes:
- OAuth2

For OAuth 2.0 you need to specify OAuth Client credentials as environment variables in the connector repository:
* `OAUTH_CLIENT_ID` - your OAuth client id
* `OAUTH_CLIENT_SECRET` - your OAuth client secret

## Actions

### Attempts to allocate quota for the specified consumer. It should be called<br/>
> before the operation is executed.<br/>
> <br/>
> This method requires the `servicemanagement.services.quota`<br/>
> permission on the specified service. For more information, see<br/>
> [Cloud IAM](https://cloud.google.com/iam).<br/>
> <br/>
> **NOTE:** The client **must** fail-open on server errors `INTERNAL`,<br/>
> `UNKNOWN`, `DEADLINE_EXCEEDED`, and `UNAVAILABLE`. To ensure system<br/>
> reliability, the server may inject these errors to prohibit any hard<br/>
> dependency on the quota functionality.

*Tags:* `services`

#### Input Parameters
* `serviceName` - _required_ - Name of the service as specified in the service configuration. For example,
`"pubsub.googleapis.com"`.

See google.api.Service for the definition of a service name.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Checks whether an operation on a service should be allowed to proceed<br/>
> based on the configuration of the service and related policies. It must be<br/>
> called before the operation is executed.<br/>
> <br/>
> If feasible, the client should cache the check results and reuse them for<br/>
> 60 seconds. In case of any server errors, the client should rely on the<br/>
> cached results for much longer time to avoid outage.<br/>
> WARNING: There is general 60s delay for the configuration and policy<br/>
> propagation, therefore callers MUST NOT depend on the `Check` method having<br/>
> the latest policy information.<br/>
> <br/>
> NOTE: the CheckRequest has the size limit of 64KB.<br/>
> <br/>
> This method requires the `servicemanagement.services.check` permission<br/>
> on the specified service. For more information, see<br/>
> [Cloud IAM](https://cloud.google.com/iam).

*Tags:* `services`

#### Input Parameters
* `serviceName` - _required_ - The service name as specified in its service configuration. For example,
`"pubsub.googleapis.com"`.

See
[google.api.Service](https://cloud.google.com/service-management/reference/rpc/google.api#google.api.Service)
for the definition of a service name.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Reports operation results to Google Service Control, such as logs and<br/>
> metrics. It should be called after an operation is completed.<br/>
> <br/>
> If feasible, the client should aggregate reporting data for up to 5<br/>
> seconds to reduce API traffic. Limiting aggregation to 5 seconds is to<br/>
> reduce data loss during client crashes. Clients should carefully choose<br/>
> the aggregation time window to avoid data loss risk more than 0.01%<br/>
> for business and compliance reasons.<br/>
> <br/>
> NOTE: the ReportRequest has the size limit of 1MB.<br/>
> <br/>
> This method requires the `servicemanagement.services.report` permission<br/>
> on the specified service. For more information, see<br/>
> [Google Cloud IAM](https://cloud.google.com/iam).

*Tags:* `services`

#### Input Parameters
* `serviceName` - _required_ - The service name as specified in its service configuration. For example,
`"pubsub.googleapis.com"`.

See
[google.api.Service](https://cloud.google.com/service-management/reference/rpc/google.api#google.api.Service)
for the definition of a service name.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

## License

**flow**ground :- Telekom iPaaS / googleapis-com-servicecontrol-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
