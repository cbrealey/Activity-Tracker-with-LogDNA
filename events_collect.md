---

copyright:
  years: 2019, 2020
lastupdated: "2020-06-15"

keywords: IBM Cloud, LogDNA, Activity Tracker, events, global, regional, data, management

subcollection: Activity-Tracker-with-LogDNA

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip}
{:download: .download}
{:important: .important}
{:note: .note}


# Collecting events
{: #events_collect}

In {{site.data.keyword.at_full_notm}} (AT), events are collected automatically for most enabled-AT services. However, some services might require an upgrade of the service plan, a configuration setting, or both, for you to be able to collect and analyze them. 
{:shortdesc}

To collect and monitor activity in your account, you must provision the {{site.data.keyword.at_full_notm}} (AT) service in your account. Then, 
as soon as an instance of an AT-enabled service is provisioned, events are collected and available for monitoring.

You can differentiate events by scope as global or location-based events. The scope determines where an event is collected and available for analysis:

* **Collection of management events** is automatic for AT-enabled services, except Watson services that require a paid plan. 

* **Collection of data events** is also automatic with the exception of some services where you must opt-in to collect those events. To opt-in, you might need to configure the service, upgrade the service plan, or both.



## Collecting Global events
{: #events_collect_global}

[Global events](/docs/Activity-Tracker-with-LogDNA?topic=Activity-Tracker-with-LogDNA-event_types#event_types_global) are available through the Activity Tracker instance in Frankfurt. Therefore, to collect and view global events, you must provision an instance of the {{site.data.keyword.at_full_notm}} service in Frankfurt.


## Collecting Location-based events
{: #events_collect_location}

[Location-based events](/docs/Activity-Tracker-with-LogDNA?topic=Activity-Tracker-with-LogDNA-event_types#event_types_location) are available through the Activity Tracker instance that is available in the same region as the service. 

Consider the following scenarios that are exceptions to this behavior for location-based events:
* The {{site.data.keyword.at_full_notm}} service might not be available in a region where a service is provisioned. [Learn more about supported locations](/docs/Activity-Tracker-with-LogDNA?topic=Activity-Tracker-with-LogDNA-regions).

    Check the [Cloud services by location](/docs/Activity-Tracker-with-LogDNA?topic=Activity-Tracker-with-LogDNA-cloud_services_locations) documentation to find out if the service generates AT events in that region, and if it does, where are the events available for analysis.

* The service might not generate Activity Tracker events in the region where you have provisioned.

    Check the [Cloud services by location](/docs/Activity-Tracker-with-LogDNA?topic=Activity-Tracker-with-LogDNA-cloud_services_locations) documentation to confirm if events are available in that region.


## Defining the instances that I need to collect and monitor events in the account
{: #events_collect_define}

You can provison only 1 instance of the {{site.data.keyword.at_full_notm}} service per location. To get the list of locations where the service is available in the {{site.data.keyword.cloud_notm}}, see [Locations](/docs/Activity-Tracker-with-LogDNA?topic=Activity-Tracker-with-LogDNA-regions).


To monitor activity in your account, you need the following {{site.data.keyword.at_full_notm}} instances:
* 1 instance in Frankfurt to monitor global events
* 1 instance in each region where you operate

For example, you might have services in the US South location only. To monitor activity in your account, you need 1 instance in US South to monitor events that are generated by services that are running in that location. You need 1 instance in EU-DE (Frankfurt) to monitor global actions that happen in your account such as user management actions, and provisioning of service instances. 


## Viewing the instances that are available to monitor events in the account
{: #events_collect_view}

In the {{site.data.keyword.cloud_notm}}, you can click the **Menu** icon ![Menu icon](../icons/icon_hamburger.svg) &gt; **Observability** &gt; **Activity Tracker** to see the dashboard where all the instances that are provisioned in the account are listed. 

If you need to provision an instance, see [Provisioning an instance](/docs/Activity-Tracker-with-LogDNA?topic=Activity-Tracker-with-LogDNA-provision).




