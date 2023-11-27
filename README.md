# Projects-using-Splunk

1. index="final_6_splunkproject" "Is Account Takeover"="TRUE"
| stats count by Country
| sort – count

2. index="final_6_splunkproject"
| search "Is Account Takeover"="TRUE"
| table "User ID", "Is Account Takeover", Country, "Device Type"

3. index="final_6_splunkproject" 
| search "Is Attack IP"="TRUE"
| stats count by "IP Address"
| sort - count
| head 10

4. index="final_6_splunkproject" 
| search "Is Attack IP"="TRUE" "Is Account Takeover"="TRUE"
| stats count by "IP Address", "Is Account Takeover"
| table "IP Address", "Is Account Takeover", count
| head 10

5. index=final_6_splunkproject "Is Attack IP"="TRUE"
| stats count by "Login Successful", "Is Attack IP"

6. index=final_6_splunkproject "Is Attack IP"="TRUE"
| top limit=10 "Browser Name and Version"

7. index=final_6_splunkproject "Is Attack IP"="TRUE"
| top limit=10 Country

8. index=final_6_splunkproject "Is Attack IP"="TRUE"
| top limit=10 "User Agent String"

9. index=final_6_splunkproject "Is Attack IP"="TRUE"
| stats count by "Is Account Takeover"
