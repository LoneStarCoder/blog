Status: Resolved

SCOM Alert: Operations_Manager_Failed_to_Access_the_Windows_Event_Log


Alert Description:
   Alert Monitor:    Failed Accessing Windows Event Log 

  The Windows Event Log Provider is still unable to open the DhcpAdminEvents event log on computer 'dhcp.domain.local'.
  The Provider has been unable to open the DhcpAdminEvents event log for 720 seconds.
  
  Most recent error details: Access is denied.
  
  One or more workflows were affected by this. 
    
  Workflow name: many
  
  Instance name: many
  
  Instance ID: many
 
I found this:
https://jurelab.wordpress.com/2015/02/18/failed-accessing-windows-event-log-on-management-server-warning-state-event-id-26004/
For some reason, SCOM is accessing the event log remotely from the management server instead of locally, so just add the action account to the event log readers group.
