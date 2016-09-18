# Firebase Configuration

Description of and configuration for the Google Firebase Database used for the medical dispenser.

## Structure and Data

This database stores a simple JSON object, and can update fields within the JSON object.

The data is structured as follows:

```
{
  "patients" : [
    "3981820312" : {
      "alert" : false,
      "dosage" : 4,
      "name" : Jeffrey Leung"
    }
  ]
}
```

The arbitrary number represents the patient number which uniquely identifies each patient.

## Integration

The [Dashboard](https://lumohacks-med-disp.github.io/) contacts the Firebase server to store the newest scheduling and dosage data.

The [Dispenser](https://github.com/lumohacks-med-disp/dispenser) retrieves a push notification from the Firebase server and retrieves scheduling and dosage data when it has been updated.

## Setup

Navigate to the [Google Firebase console](https://firebase.google.com/console/). Create a new account if you don't have one already.

Click _Create New Project_, fill in the form, and click _Create project_.

Once you have your project set up, select _Database_.

Click on the 3-dot button on the right, choose _Import JSON_, and import the file `base_import.json`.

## Getting Data

TODO

## Setting Data

TODO
