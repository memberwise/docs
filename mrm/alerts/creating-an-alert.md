### MRM - Alerts - Creating an alert

To create an alert, you'll need Member Relationship Manager administrator access.

To get started with alerts, head to the MRM section of Managed Memberwise dashboard, [or click here](https://memberwise.io/dashboard/mrm/alerts).

Click "Create Alert" to start creating an alert.

You should then see the alert creation scree.

![alt text](../../assets/image5.png)

To begin, select the account record you'd like to have this alert be configured against.

![alt text](../../assets/image6.png)

You can select any of the base records that can be accessed in the MRM (more records coming soon).

For example, if you select "Share", the configured alert will only execute if a user has selected a share. Alerts will only ever be executed on the records they are configured for. This is true for names inside of shares, loans or cards.

Configure the title and description of the alert. As you fill out these fields, you will see the Alert Preview populate with your changes.

The severity is a training tool that gives users an at-a-glance view of any particularly egregious alerts.

You can force alerts to appear in a popup window that must be dismissed by enabling "Pop up alert".

You can add any number of rules to an alert, although it's best to keep your alert rules simple. Rules can be numbers, strings of text or dates.

All rules in an alert must evaluate to "true" for the alert to trigger.

The "field" option can be any item within a record, this includes items like warning codes, tracking records, etc. Below are some example alerts to help in your alert creation.

#### Account

| Field mnemonic        | Field value                           | Operator                 | Value      | Notes                                                                                    |
| --------------------- | ------------------------------------- | ------------------------ | ---------- | ---------------------------------------------------------------------------------------- |
| AFROZENCODE           | frozenCode                            | equals                   | 0          | If the account's frozen code value is "0", this will equate to true.                     |
| WARNING:20            | warningCode[*].warningCode            | contains                 | 5          | If the account record warnings list has a warning code of "5", this will equate to true. |
| AOPENDATE             | openDate                              | less_than_or_equal_to    | NOW(-180)  | If the account's open date is <= now - 180 days, this will equate to "true"              |
| AACTIVITYDATE         | activityDate                          | greater_than_or_equal_to | 2020-01-01 | If the account's activity date is on 01/01/2020, this will equate to true                |
| TRACKING:TYPE         | trackingList.tracking[*].type         | equals                   | 33         | If the account has a tracking type 33, this will equate to true.                         |
| TRACKING:USERAMOUNT12 | trackingList.tracking[*].userAmount12 | equals                   | 10000      | If the account account has a tracking userAmount12, this will equate to true.            |
| AFROZENCODE           | frozenCode                            | equals                   | 0          | If the account's frozen code value is "0", this will equate to true.                     |
