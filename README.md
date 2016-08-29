# morning-routine-button
Morning Routine AWS Lambda script for IoT Dash button

Take a look at this tutorial for setting up and registering the AWS IoT button: https://www.hackster.io/reanimationxp/amazon-re-invent-dash-button-aws-ifttt-infinibutton-daaf5d

Go to the AWS Lambda configuration wizard here: https://console.aws.amazon.com/lambda/home

The Amazon documentation is also useful: http://docs.aws.amazon.com/iot/latest/developerguide/iot-button-lambda.html

Create a new trigger, for the IoT Type, select IoT Button, then follow the steps on the screen.

Once the button is configured, select the Python runtime and paste the script from morning_routine.py

Only core libraries are used, so no additional setup for the codebase is needed, no libraries need to be installed.

Slack integration is done via the IRC gateway. No Slack app/token required. See here for connecting: https://get.slack.help/hc/en-us/articles/201727913-Connecting-to-Slack-over-IRC-and-XMPP

This will give you the values needed for slackhost, user, password in the script.

Step 4 of https://www.hackster.io/reanimationxp/amazon-re-invent-dash-button-aws-ifttt-infinibutton-daaf5d explains how to get the value needed for the iftttmakerkey variable in the script.

Step 5 of https://www.hackster.io/reanimationxp/amazon-re-invent-dash-button-aws-ifttt-infinibutton-daaf5d explains how to set up the IFTTT recipes. The script assumes the Event Name is 'IoT-button-SINGLE'