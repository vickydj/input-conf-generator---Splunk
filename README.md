# input-conf-generator---Splunk
splunk base app - automation for end-users to create conf files for inputs and serverclass and deploy them, so admins can focus on other works


## input_conf_generator_sh
This acts as wrapper for the automation, admin will set the parameters in the setup page.
This can also be done from the backend by editing the ds_info.conf
End-users (typically powerusers) will be able to fill the form with host, source, sourcetype and other details and submit the form.
The data is sent to DS as a json payload.

## input_conf_generator_ds
This is a simple TA that receives the information from user dashboard and process it into inputs.conf and serverclass.conf, duplicates are handled by the application logic.
No configuration is required on this TA.
