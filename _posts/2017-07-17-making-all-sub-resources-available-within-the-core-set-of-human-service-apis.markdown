---
published: true
layout: post
title: Making All Sub-Resources Available Within The Core Set Of Human Service APIs
date: 2017-07-17T09:00:00.000Z
tags:
  - API Evangelist
  - HSDS
  - HSDA
  - Cities
  - Definitions
  - Schema
image: >-
  https://s3.amazonaws.com/kinlane-productions/3D-Printing/regions/api-regions-global-map-from-google.png
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/open-referral/hsds-organization.png" align="right" width="40%" style="padding: 15px;" /></p>I had recently taken [the Human Services Data Specification (HSDS)](http://openreferral.readthedocs.io/en/latest/reference/) and exposed it as a set of API paths that provide access to about 95% of the schema, which we are calling the [Human Services Data API (HSDA)](https://openreferral.github.io/api-specification/definition/). When you make a call to the /organizations/ path, you receive an array collection of organizations that each match the HSDA organization schema. The same applies when you make a call to the /locations, /contacts, and /services, opening up access to the entire schema--minus three objects I pushed off until future releases.

After the core set of API paths /organization, /service, /location, /contact, there are a set of sub-resources available across those as it makes sense--including /phone, /programs, /physical_address, /postal_address, /regular_schedule, /holiday_schedule, /funding, /eligibility, /service_area, /required_document, /payment_accepted, /language, /accessiblity_for_disabilities, and /service_at_location_id. I took the HSDA schema, and published API paths for each sub-resource so that it exactly returned, and accepted HSDA compliant schema--making all aspects of the schema accessible via an API, with POST and PUT requests accepting compliant schema, and GET returning compliant schema.

One of the "stoppers" we received from several folks in the HSDS community during the feedback cycle going from version 1.0 of the API to version 1.1, was that the design was overly complex, and that it would serve any of the human services use cases on the table currently, unless you could get at all the sub resources directly with each core API path, eliminating the need for making additional call(s) to each sub-resource. You could get at everything about an /organization, /service, /location, and /contact in a single API URL.

Currently the core four API paths accept and return the following schema:

<p><strong>Organization</strong></p>
<table border="1" class="docutils">
<colgroup>
<col width="17%" />
<col width="17%" />
<col width="50%" />
<col width="8%" />
<col width="8%" />
</colgroup>
<thead valign="bottom">
<tr class="row-odd"><th class="head">Field Name</th>
<th class="head">Type (Format)</th>
<th class="head">Description</th>
<th class="head">Required?</th>
<th class="head">Unique?</th>
</tr>
</thead>
<tbody valign="top">
<tr class="row-even"><td>id</td>
<td>string (uuid)</td>
<td>Each organization must have a unique identifier.</td>
<td>True</td>
<td>True</td>
</tr>
<tr class="row-odd"><td>name</td>
<td>string</td>
<td>The official or public name of the organization.</td>
<td>True</td>
<td>False</td>
</tr>
<tr class="row-even"><td>alternate_name</td>
<td>string</td>
<td>Alternative or commonly used name for the organization.</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-odd"><td>description</td>
<td>string</td>
<td>A brief summary about the organization. It can contain markup such as HTML or Markdown.</td>
<td>True</td>
<td>False</td>
</tr>
<tr class="row-even"><td>email</td>
<td>string (email)</td>
<td>The contact e-mail address for the organization.</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-odd"><td>url</td>
<td>string (url)</td>
<td>The URL (website address) of the organization.</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-even"><td>tax_status</td>
<td>string</td>
<td>Government assigned tax designation for for tax-exempt organizations.</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-odd"><td>tax_id</td>
<td>string</td>
<td>A government issued identifier used for the purpose of tax administration.</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-even"><td>year_incorporated</td>
<td>date (%Y)</td>
<td>The year in which the organization was legally formed.</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-odd"><td>legal_status</td>
<td>string</td>
<td>The legal status defines the conditions that an organization is operating under; e.g. non-profit, private corporation or a government organization.</td>
<td>False</td>
<td>False</td>
</tr>
</tbody>
</table>

<p><strong>Service</strong></p>
<table border="1" class="docutils">
<colgroup>
<col width="17%" />
<col width="17%" />
<col width="50%" />
<col width="8%" />
<col width="8%" />
</colgroup>
<thead valign="bottom">
<tr class="row-odd"><th class="head">Field Name</th>
<th class="head">Type (Format)</th>
<th class="head">Description</th>
<th class="head">Required?</th>
<th class="head">Unique?</th>
</tr>
</thead>
<tbody valign="top">
<tr class="row-even"><td>id</td>
<td>string</td>
<td>Each service must have a unique identifier.</td>
<td>True</td>
<td>True</td>
</tr>
<tr class="row-odd"><td>organization_id</td>
<td>string</td>
<td>The identifier of the organization that provides this service.</td>
<td>True</td>
<td>False</td>
</tr>
<tr class="row-even"><td>program_id</td>
<td>string</td>
<td>The identifier of the program this service is delivered under.</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-odd"><td>name</td>
<td>string</td>
<td>The official or public name of the service.</td>
<td>True</td>
<td>False</td>
</tr>
<tr class="row-even"><td>alternate_name</td>
<td>string</td>
<td>Alternative or commonly used name for a service.</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-odd"><td>description</td>
<td>string</td>
<td>A description of the service.</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-even"><td>url</td>
<td>string (url)</td>
<td>URL of the service</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-odd"><td>email</td>
<td>string (email)</td>
<td>Email address for the service</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-even"><td>status</td>
<td>string</td>
<td>The current status of the service.</td>
<td>True</td>
<td>False</td>
</tr>
<tr class="row-odd"><td>interpretation_services</td>
<td>string</td>
<td>A description of any interpretation services available for accessing this service.</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-even"><td>application_process</td>
<td>string</td>
<td>The steps needed to access the service.</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-odd"><td>wait_time</td>
<td>string</td>
<td>Time a client may expect to wait before receiving a service.</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-even"><td>fees</td>
<td>string</td>
<td>Details of any charges for service users to access this service.</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-odd"><td>accreditations</td>
<td>string</td>
<td>Details of any accreditations. Accreditation is the formal evaluation of an organization or program against best practice standards set by an accrediting organization.</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-even"><td>licenses</td>
<td>string</td>
<td>An organization may have a license issued by a government entity to operate legally. A list of any such licenses can be provided here.</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-odd"><td>taxonomy_ids</td>
<td>string</td>
<td>(Deprecated) A comma separated list of identifiers from the taxonomy table. This field is deprecated in favour of using the service_taxonomy table.</td>
<td>False</td>
<td>False</td>
</tr>
</tbody>
</table>

<p><strong>Location</strong></p>
<table border="1" class="docutils">
<colgroup>
<col width="17%" />
<col width="17%" />
<col width="50%" />
<col width="8%" />
<col width="8%" />
</colgroup>
<thead valign="bottom">
<tr class="row-odd"><th class="head">Field Name</th>
<th class="head">Type (Format)</th>
<th class="head">Description</th>
<th class="head">Required?</th>
<th class="head">Unique?</th>
</tr>
</thead>
<tbody valign="top">
<tr class="row-even"><td>id</td>
<td>string</td>
<td>Each location must have a unique identifier</td>
<td>True</td>
<td>False</td>
</tr>
<tr class="row-odd"><td>organization_id</td>
<td>string</td>
<td>Each location entry should be linked to a single organization. This is the organization that is responsible for maintaining information about this location. The identifier of the organization should be given here. Details of the services the organisation delivers at this location should be provided in the services_at_location table.</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-even"><td>name</td>
<td>string</td>
<td>The name of the location</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-odd"><td>alternate_name</td>
<td>string</td>
<td>An alternative name for the location</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-even"><td>description</td>
<td>string</td>
<td>A description of this location.</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-odd"><td>transportation</td>
<td>string</td>
<td>A description of the access to public or private transportation to and from the location.</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-even"><td>latitude</td>
<td>number</td>
<td>Y coordinate of location expressed in decimal degrees in WGS84 datum.</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-odd"><td>longitude</td>
<td>number</td>
<td>X coordinate of location expressed in decimal degrees in WGS84 datum.</td>
<td>False</td>
<td>False</td>
</tr>
</tbody>
</table>

<p><strong>Contact</strong></p>
<table border="1" class="docutils">
<colgroup>
<col width="17%" />
<col width="17%" />
<col width="50%" />
<col width="8%" />
<col width="8%" />
</colgroup>
<thead valign="bottom">
<tr class="row-odd"><th class="head">Field Name</th>
<th class="head">Type (Format)</th>
<th class="head">Description</th>
<th class="head">Required?</th>
<th class="head">Unique?</th>
</tr>
</thead>
<tbody valign="top">
<tr class="row-even"><td>id</td>
<td>string</td>
<td>Each contact must have a unique identifier</td>
<td>True</td>
<td>False</td>
</tr>
<tr class="row-odd"><td>organization_id</td>
<td>string</td>
<td>The identifier of the organization for which this is a contact</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-even"><td>service_id</td>
<td>string</td>
<td>The identifier of the service for which this is a contact</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-odd"><td>service_at_location_id</td>
<td>string</td>
<td>The identifier of the &#8216;service at location&#8217; table entry, when this contact is specific to a service in a particular location.</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-even"><td>name</td>
<td>string</td>
<td>The name of the person</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-odd"><td>title</td>
<td>string</td>
<td>The job title of the person</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-even"><td>department</td>
<td>string</td>
<td>The department that the person is part of</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-odd"><td>email</td>
<td>string (email)</td>
<td>The email address of the person</td>
<td>False</td>
<td>False</td>
</tr>
</tbody>
</table>

To ensure that all sub-resource area available as part of each of the requests and responses for all core API paths, we are going to have to evolve the HSDS schema to be:

<p><strong>Organization</strong></p>
<table border="1" class="docutils">
<colgroup>
<col width="17%" />
<col width="17%" />
<col width="50%" />
<col width="8%" />
<col width="8%" />
</colgroup>
<thead valign="bottom">
<tr class="row-odd"><th class="head">Field Name</th>
<th class="head">Type (Format)</th>
<th class="head">Description</th>
<th class="head">Required?</th>
<th class="head">Unique?</th>
</tr>
</thead>
<tbody valign="top">
<tr class="row-even"><td>id</td>
<td>string (uuid)</td>
<td>Each organization must have a unique identifier.</td>
<td>True</td>
<td>True</td>
</tr>
<tr class="row-odd"><td>name</td>
<td>string</td>
<td>The official or public name of the organization.</td>
<td>True</td>
<td>False</td>
</tr>
<tr class="row-even"><td>alternate_name</td>
<td>string</td>
<td>Alternative or commonly used name for the organization.</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-odd"><td>description</td>
<td>string</td>
<td>A brief summary about the organization. It can contain markup such as HTML or Markdown.</td>
<td>True</td>
<td>False</td>
</tr>
<tr class="row-even"><td>email</td>
<td>string (email)</td>
<td>The contact e-mail address for the organization.</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-odd"><td>url</td>
<td>string (url)</td>
<td>The URL (website address) of the organization.</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-even"><td>tax_status</td>
<td>string</td>
<td>Government assigned tax designation for for tax-exempt organizations.</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-odd"><td>tax_id</td>
<td>string</td>
<td>A government issued identifier used for the purpose of tax administration.</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-even"><td>year_incorporated</td>
<td>date (%Y)</td>
<td>The year in which the organization was legally formed.</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-odd"><td>legal_status</td>
<td>string</td>
<td>The legal status defines the conditions that an organization is operating under; e.g. non-profit, private corporation or a government organization.</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-odd"><td>services</td>
<td>array</td>
<td>Returns a collection of services for each organization</td>
<td>False</td>
<td>False</td>
</tr>  
<tr class="row-odd"><td>locations</td>
<td>array</td>
<td>Returns a collection of locations for each organization</td>
<td>False</td>
<td>False</td>
</tr>  
<tr class="row-odd"><td>contacts</td>
<td>array</td>
<td>Returns a collection of contacts for each organization</td>
<td>False</td>
<td>False</td>
</tr>    
<tr class="row-odd"><td>phones</td>
<td>array</td>
<td>Returns a collection of phones for each organization</td>
<td>False</td>
<td>False</td>
</tr>   
<tr class="row-odd"><td>programs</td>
<td>array</td>
<td>Returns a collection of programs for each organization</td>
<td>False</td>
<td>False</td>
</tr>   
<tr class="row-odd"><td>fundings</td>
<td>array</td>
<td>Returns a collection of fundings for each organization</td>
<td>False</td>
<td>False</td>
</tr>   
</tbody>
</table>

<p><strong>Service</strong></p>
<table border="1" class="docutils">
<colgroup>
<col width="17%" />
<col width="17%" />
<col width="50%" />
<col width="8%" />
<col width="8%" />
</colgroup>
<thead valign="bottom">
<tr class="row-odd"><th class="head">Field Name</th>
<th class="head">Type (Format)</th>
<th class="head">Description</th>
<th class="head">Required?</th>
<th class="head">Unique?</th>
</tr>
</thead>
<tbody valign="top">
<tr class="row-even"><td>id</td>
<td>string</td>
<td>Each service must have a unique identifier.</td>
<td>True</td>
<td>True</td>
</tr>
<tr class="row-odd"><td>organization_id</td>
<td>string</td>
<td>The identifier of the organization that provides this service.</td>
<td>True</td>
<td>False</td>
</tr>
<tr class="row-even"><td>program_id</td>
<td>string</td>
<td>The identifier of the program this service is delivered under.</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-odd"><td>name</td>
<td>string</td>
<td>The official or public name of the service.</td>
<td>True</td>
<td>False</td>
</tr>
<tr class="row-even"><td>alternate_name</td>
<td>string</td>
<td>Alternative or commonly used name for a service.</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-odd"><td>description</td>
<td>string</td>
<td>A description of the service.</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-even"><td>url</td>
<td>string (url)</td>
<td>URL of the service</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-odd"><td>email</td>
<td>string (email)</td>
<td>Email address for the service</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-even"><td>status</td>
<td>string</td>
<td>The current status of the service.</td>
<td>True</td>
<td>False</td>
</tr>
<tr class="row-odd"><td>interpretation_services</td>
<td>string</td>
<td>A description of any interpretation services available for accessing this service.</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-even"><td>application_process</td>
<td>string</td>
<td>The steps needed to access the service.</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-odd"><td>wait_time</td>
<td>string</td>
<td>Time a client may expect to wait before receiving a service.</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-even"><td>fees</td>
<td>string</td>
<td>Details of any charges for service users to access this service.</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-odd"><td>accreditations</td>
<td>string</td>
<td>Details of any accreditations. Accreditation is the formal evaluation of an organization or program against best practice standards set by an accrediting organization.</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-even"><td>licenses</td>
<td>string</td>
<td>An organization may have a license issued by a government entity to operate legally. A list of any such licenses can be provided here.</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-odd"><td>taxonomy_ids</td>
<td>string</td>
<td>(Deprecated) A comma separated list of identifiers from the taxonomy table. This field is deprecated in favour of using the service_taxonomy table.</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-odd"><td>contacts</td>
<td>array</td>
<td>Returns a collection of contacts for each service.</td>
<td>False</td>
<td>False</td>
</tr>   
<tr class="row-odd"><td>phones</td>
<td>array</td>
<td>Returns a collection of phones for each service.</td>
<td>False</td>
<td>False</td>
</tr>   
<tr class="row-odd"><td>regular_schedules</td>
<td>array</td>
<td>Returns a collection of regular schedules for each service.</td>
<td>False</td>
<td>False</td>
</tr>   
<tr class="row-odd"><td>holiday_schedules</td>
<td>array</td>
<td>Returns a collection of holiday schedules for each service.</td>
<td>False</td>
<td>False</td>
</tr>    
<tr class="row-odd"><td>fundings</td>
<td>array</td>
<td>Returns a collection of fundings for each service.</td>
<td>False</td>
<td>False</td>
</tr>   
<tr class="row-odd"><td>eligibilities</td>
<td>array</td>
<td>Returns a collection of eligibilities for each service.</td>
<td>False</td>
<td>False</td>
</tr>  
<tr class="row-odd"><td>service_areas</td>
<td>array</td>
<td>Returns a collection of service areas for each service.</td>
<td>False</td>
<td>False</td>
</tr>  
<tr class="row-odd"><td>required_documents</td>
<td>array</td>
<td>Returns a collection of required documents for each service.</td>
<td>False</td>
<td>False</td>
</tr>   
<tr class="row-odd"><td>payments_accepted</td>
<td>array</td>
<td>Returns a collection of payments accepted for each service.</td>
<td>False</td>
<td>False</td>
</tr>   
<tr class="row-odd"><td>languages</td>
<td>array</td>
<td>Returns a collection of languages for each service.</td>
<td>False</td>
<td>False</td>
</tr>   
</tbody>
</table>

<p><strong>Location</strong></p>
<table border="1" class="docutils">
<colgroup>
<col width="17%" />
<col width="17%" />
<col width="50%" />
<col width="8%" />
<col width="8%" />
</colgroup>
<thead valign="bottom">
<tr class="row-odd"><th class="head">Field Name</th>
<th class="head">Type (Format)</th>
<th class="head">Description</th>
<th class="head">Required?</th>
<th class="head">Unique?</th>
</tr>
</thead>
<tbody valign="top">
<tr class="row-even"><td>id</td>
<td>string</td>
<td>Each location must have a unique identifier</td>
<td>True</td>
<td>False</td>
</tr>
<tr class="row-odd"><td>organization_id</td>
<td>string</td>
<td>Each location entry should be linked to a single organization. This is the organization that is responsible for maintaining information about this location. The identifier of the organization should be given here. Details of the services the organisation delivers at this location should be provided in the services_at_location table.</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-even"><td>name</td>
<td>string</td>
<td>The name of the location</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-odd"><td>alternate_name</td>
<td>string</td>
<td>An alternative name for the location</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-even"><td>description</td>
<td>string</td>
<td>A description of this location.</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-odd"><td>transportation</td>
<td>string</td>
<td>A description of the access to public or private transportation to and from the location.</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-even"><td>latitude</td>
<td>number</td>
<td>Y coordinate of location expressed in decimal degrees in WGS84 datum.</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-odd"><td>longitude</td>
<td>number</td>
<td>X coordinate of location expressed in decimal degrees in WGS84 datum.</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-odd"><td>phones</td>
<td>array</td>
<td>Returns a collection of phones for each location.</td>
<td>False</td>
<td>False</td>
</tr>  
<tr class="row-odd"><td>physical_addresses</td>
<td>array</td>
<td>Returns a collection of physical addresses for each location.</td>
<td>False</td>
<td>False</td>
</tr>    
<tr class="row-odd"><td>postal_addresses</td>
<td>array</td>
<td>Returns a collection of postal addresses for each location.</td>
<td>False</td>
<td>False</td>
</tr>   
<tr class="row-odd"><td>regular_schedules</td>
<td>array</td>
<td>Returns a collection of regular schedules for each location.</td>
<td>False</td>
<td>False</td>
</tr>   
<tr class="row-odd"><td>holiday_schedules</td>
<td>array</td>
<td>Returns a collection of holiday schedules for each location.</td>
<td>False</td>
<td>False</td>
</tr>  
<tr class="row-odd"><td>languages</td>
<td>array</td>
<td>Returns a collection of languages for each location.</td>
<td>False</td>
<td>False</td>
</tr>    
<tr class="row-odd"><td>accessiblity_for_disabilities</td>
<td>array</td>
<td>Returns a collection of accessiblity_for_disabilities for each location.</td>
<td>False</td>
<td>False</td>
</tr>    
</tbody>
</table>

<p><strong>Contact</strong></p>
<table border="1" class="docutils">
<colgroup>
<col width="17%" />
<col width="17%" />
<col width="50%" />
<col width="8%" />
<col width="8%" />
</colgroup>
<thead valign="bottom">
<tr class="row-odd"><th class="head">Field Name</th>
<th class="head">Type (Format)</th>
<th class="head">Description</th>
<th class="head">Required?</th>
<th class="head">Unique?</th>
</tr>
</thead>
<tbody valign="top">
<tr class="row-even"><td>id</td>
<td>string</td>
<td>Each contact must have a unique identifier</td>
<td>True</td>
<td>False</td>
</tr>
<tr class="row-odd"><td>organization_id</td>
<td>string</td>
<td>The identifier of the organization for which this is a contact</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-even"><td>service_id</td>
<td>string</td>
<td>The identifier of the service for which this is a contact</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-odd"><td>service_at_location_id</td>
<td>string</td>
<td>The identifier of the &#8216;service at location&#8217; table entry, when this contact is specific to a service in a particular location.</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-even"><td>name</td>
<td>string</td>
<td>The name of the person</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-odd"><td>title</td>
<td>string</td>
<td>The job title of the person</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-even"><td>department</td>
<td>string</td>
<td>The department that the person is part of</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-odd"><td>email</td>
<td>string (email)</td>
<td>The email address of the person</td>
<td>False</td>
<td>False</td>
</tr>
<tr class="row-odd"><td>phones</td>
<td>array</td>
<td>Returns a collection of phones for each contact</td>
<td>False</td>
<td>False</td>
</tr>  
</tbody>
</table>

Once we add all relevant sub-resources added as arrays to the HSDS schema, we can allow API consumers to POST and PUT, or GET using as little, or as much of the schema using the path, header, or parameter. Allowing for reading and writing HSDS at the granular level, or everything at once using a single path.

Next we need to consider this updated schema as part of the 1.2 release of HSDS. If we update HSDA to allow for filtering the schema across /organization, /service, /location, and /contact, and return each sub-resource as part of the API request or response, it will be out of sync with HSDS. Ideally, both HSDS, and HSDA move forward in sync with each version. I'm curious why this expanded schema became such an issue once we got to the API phase--it seems like it should have been part of v1.1 of HSDS, making the schema drive the API instead of the other way around.

I'm guessing that these concerns about schema don't come into focus until we start talking about access to the schema, and data. [Making the separation and relationships between HSDS and HSDA all the more important](http://apievangelist.com/2017/07/13/quantifying-the-difference-between-human-services-data-specification-hsds-and-its-api/), providing a framework to move the schema forward in a way that is rooted in how it will actually be accessed. Which is why we do APIs...
