# escu_companion
The ESCU Companion Splunk App is built to support the organization's implementation of Splunk ESCU.

## author info
This Splunk App was created by [Brandon Sternfield (Optiv + ClearShark)](https://www.brandonsternfield.com)

## pre-requisites
Requires [Splunk Enterprise Security](https://splunkbase.splunk.com/app/263) version 8.0 or greater.

Requires [Splunk Enterprise Security Content Updates](https://splunkbase.splunk.com/app/3449) 4.31.0 or greater.

## Initial Setup
Upon initial load of the app, the admin must configure the included macro of `escu_companion_appfilter` with any custom apps that contain your detections. This macro is used heavily.

By default, the app ships with `access = read : [ * ], write : [ admin, sc_admin ]` meaning that all users can read and only admin/sc_admin can write. Change this as needed to your environment's requirements.

## App Contents

- **Dashboards**
     - Home
          - *Default app homepage, shows documentation, similiar to this github README*
     - Detection Scheduling
          - *Showcases all current scheduled correlation searches spread out over time, and recommends a time that is least used.* 
     - Explorer
          - *Able to browse content by Technique, Tactic, Analytic Story, Confidence, Impact, or if ESCU has a newer copy than your clone.* 
- **Alerts**
     - Update Alert
          - *Creates an alert when a version of an ESCU detection shows as different than the custom cloned copy.*
          - *This alert can be configured to send emails, or anything else that is desired. By default it will create messages in the Splunk UI that can be seen by anyone with the `edit_correlationsearches` capability which by default is `ess_admin` and `admin`/`sc_admin`.*  


``````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````
