<!-- loio8509485251814213876223e332bfdcbb -->

# SAP Business Application Studio Availability

You can find the regions where SAP Business Application Studio is available and the relevant IP addresses.



<a name="loio8509485251814213876223e332bfdcbb__section_iv4_wwz_hqb"/>

## Outbound IP Address

Use an SAP Business Application Studio outbound IP address when connecting from SAP Business Application Studio to an outside service.

For example, you can use an outbound IP address for connecting SAP Business Application Studio to an SAP S/4HANA service or an ABAP Cloud System service.


<table>
<tr>
<th>

Region



</th>
<th>

IaaS Provider



</th>
<th>

Technical Key



</th>
<th>

SAP Business Application Studio

Outbound IP\*



</th>
</tr>
<tr>
<td>

Europe \(Frankfurt\)



</td>
<td>

AWS



</td>
<td>

eu10



</td>
<td>

18.158.7.155

18.192.47.220

18.194.253.116



</td>
</tr>
<tr>
<td>

Europe \(Frankfurt\)



</td>
<td>

AWS



</td>
<td>

eu10-trial



</td>
<td>

18.192.169.180

18.193.190.210

18.193.190.236



</td>
</tr>
<tr>
<td>

Europe \(Frankfurt\)



</td>
<td>

AWS



</td>
<td>

eu11



</td>
<td>

18.185.27.129

3.122.202.117

3.65.47.134



</td>
</tr>
<tr>
<td>

Europe \(Frankfurt\)



</td>
<td>

AWS



</td>
<td>

eu12



</td>
<td>

18.158.167.104

18.158.197.80

18.198.185.172



</td>
</tr>
<tr>
<td>

US East \(N. Virginia\)



</td>
<td>

AWS



</td>
<td>

us10



</td>
<td>

3.218.32.143

34.195.235.17

35.171.105.85



</td>
</tr>
<tr>
<td>

US East \(N. Virginia\)



</td>
<td>

AWS



</td>
<td>

us10-trial



</td>
<td>

100.25.71.121

34.198.58.151

54.172.162.6



</td>
</tr>
<tr>
<td>

Australia \(Sydney\)



</td>
<td>

AWS



</td>
<td>

ap10



</td>
<td>

3.105.48.137

3.106.19.99

3.24.68.98



</td>
</tr>
<tr>
<td>

Singapore



</td>
<td>

AWS



</td>
<td>

ap11



</td>
<td>

13.251.235.126

54.255.46.77

54.255.68.69



</td>
</tr>
<tr>
<td>

Seoul



</td>
<td>

AWS



</td>
<td>

ap12



</td>
<td>

3.35.61.218

3.36.186.108

52.78.62.199



</td>
</tr>
<tr>
<td>

Canada \(Montreal\)



</td>
<td>

AWS



</td>
<td>

ca10



</td>
<td>

3.96.106.101

3.96.253.248

99.79.177.154



</td>
</tr>
<tr>
<td>

Brazil \(Sao Paulo\)



</td>
<td>

AWS



</td>
<td>

br10



</td>
<td>

18.230.114.154

54.232.168.1

54.232.48.50



</td>
</tr>
<tr>
<td>

Japan \(Tokyo\)



</td>
<td>

AWS



</td>
<td>

jp10



</td>
<td>

52.198.200.83

52.68.68.77

54.64.113.216



</td>
</tr>
<tr>
<td>

Europe \(Netherlands\)



</td>
<td>

Azure



</td>
<td>

eu20



</td>
<td rowspan="6">

> ### Note:  
> SAP Business Application Studio doesn't currently support static IPs for Azure.

To determine the outbound IP address, perform the following steps:

1.  Open your dev space.
2.  Open the terminal.

    See the [Terminal](Terminal_c8b4ae9.md) topic for more information.

3.  Enter the following command from the terminal:

    ```
    dig +short myip.opendns.com @resolver1.opendns.com
    ```




</td>
</tr>
<tr>
<td>

US West \(Washington\)



</td>
<td>

Azure



</td>
<td>

us20



</td>
</tr>
<tr>
<td>

US East



</td>
<td>

Azure



</td>
<td>

us21



</td>
</tr>
<tr>
<td>

Japan \(Tokyo\)



</td>
<td>

Azure



</td>
<td>

jp20



</td>
</tr>
<tr>
<td>

Singapore



</td>
<td>

Azure



</td>
<td>

ap21



</td>
</tr>
<tr>
<td>

Singapore



</td>
<td>

Azure



</td>
<td>

ap21-trial



</td>
</tr>
</table>

\*NAT IPs \(egress, IPs for requests from an SAP Business Application Studio dev space\)



<a name="loio8509485251814213876223e332bfdcbb__section_nkt_twz_hqb"/>

## Inbound IP Address

Use an SAP Business Application Studio inbound IP address when connecting from a system outside of SAP Business Application Studio to your dev spaces within SAP Business Application Studio.

For example, when connecting to a service on your corporate SAP system, which is located within your corporate network, you might need to maintain the SAP Business Application Studio connectivity service host in your firewall.


<table>
<tr>
<th>

Region



</th>
<th>

IaaS Provider



</th>
<th>

Technical Key



</th>
<th>

SAP Business Application Studio

Connectivity Service Host



</th>
<th>

SAP Business Application Studio

Inbound IP



</th>
</tr>
<tr>
<td>

Europe \(Frankfurt\)



</td>
<td>

AWS



</td>
<td>

eu10



</td>
<td>

https://connectivity.eu10.applicationstudio.cloud.sap



</td>
<td>

18.159.70.155

18.159.232.22

18.156.27.245

18.193.62.167

52.58.227.227

3.66.10.126



</td>
</tr>
<tr>
<td>

Europe \(Frankfurt\)



</td>
<td>

AWS



</td>
<td>

eu11



</td>
<td>

https://connectivity.eu11.applicationstudio.cloud.sap



</td>
<td>

18.158.123.221

18.193.170.223

18.157.124.219

35.156.170.248

3.64.94.185

3.68.127.205



</td>
</tr>
<tr>
<td>

Europe \(Frankfurt\)



</td>
<td>

AWS



</td>
<td>

eu12



</td>
<td>

https://connectivity.eu12.applicationstudio.cloud.sap



</td>
<td>

3.124.78.26

3.64.186.38

35.157.83.247

18.198.238.190

3.66.52.233

3.126.7.208



</td>
</tr>
<tr>
<td>

Europe \(Frankfurt\)



</td>
<td>

AWS



</td>
<td>

cry10cf.int



</td>
<td>

https://connectivity.cry10cf.int.applicationstudio.cloud.sap



</td>
<td>

18.192.167.232

18.198.211.102

18.196.140.56

18.193.50.247

18.156.62.37

3.68.133.153



</td>
</tr>
<tr>
<td>

US East \(N. Virginia\)



</td>
<td>

AWS



</td>
<td>

us10



</td>
<td>

https://connectivity.us10.applicationstudio.cloud.sap



</td>
<td>

100.24.163.249

54.243.145.188

18.210.189.221

44.193.236.153

3.91.126.136

34.236.221.171



</td>
</tr>
<tr>
<td>

Australia \(Sydney\)



</td>
<td>

AWS



</td>
<td>

ap10



</td>
<td>

https://connectivity.ap10.applicationstudio.cloud.sap



</td>
<td>

13.238.41.41

54.153.190.7

52.63.88.22

54.252.50.184

3.105.22.230

13.210.109.84



</td>
</tr>
<tr>
<td>

Singapore



</td>
<td>

AWS



</td>
<td>

ap11



</td>
<td>

https://connectivity.ap11.applicationstudio.cloud.sap



</td>
<td>

18.139.207.29

52.220.86.30

13.213.240.205

54.169.224.233

13.213.216.104

13.213.186.249



</td>
</tr>
<tr>
<td>

Seoul



</td>
<td>

AWS



</td>
<td>

ap12



</td>
<td>

https://connectivity.ap12.applicationstudio.cloud.sap



</td>
<td>

54.180.46.250

3.34.92.76

3.37.239.157

3.37.8.79

3.36.229.98

3.37.237.182



</td>
</tr>
<tr>
<td>

Canada \(Montreal\)



</td>
<td>

AWS



</td>
<td>

ca10



</td>
<td>

https://connectivity.ca10.applicationstudio.cloud.sap



</td>
<td>

3.98.238.174

52.60.170.25

3.97.151.56

3.97.151.215

35.183.175.160

3.98.191.85



</td>
</tr>
<tr>
<td>

Brazil \(Sao Paulo\)



</td>
<td>

AWS



</td>
<td>

br10



</td>
<td>

https://connectivity.br10.applicationstudio.cloud.sap



</td>
<td>

54.207.235.96

54.94.84.199

54.94.12.100

54.94.88.250

18.230.90.202

54.232.23.35



</td>
</tr>
<tr>
<td>

Japan \(Tokyo\)



</td>
<td>

AWS



</td>
<td>

jp10



</td>
<td>

https://connectivity.jp10.applicationstudio.cloud.sap



</td>
<td>

54.95.29.60

18.180.77.231

18.181.101.86

35.74.156.52

35.75.212.58

175.41.212.190



</td>
</tr>
<tr>
<td>

Europe \(Frankfurt\)



</td>
<td>

AWS



</td>
<td>

eu10-trial



</td>
<td>

https://connectivity.eu10cf.trial.applicationstudio.cloud.sap



</td>
<td rowspan="8">

> ### Note:  
> SAP Business Application Studio doesn't currently support static inbound IPs for trial environments and Azure.

To determine the inbound IP address, perform the following steps:

1.  Open the command prompt.
2.  Enter the following command:

    ```
    $ nslookup <connectivity_service_host>
    ```


> ### Note:  
> The inbound IPs may change over time. If you have trouble connecting from an outside system to SAP Business Application Studio, perform the steps above to determine the new inbound IP address.



</td>
</tr>
<tr>
<td>

US East \(N. Virginia\)



</td>
<td>

AWS



</td>
<td>

us10-trial



</td>
<td>

https://connectivity.us10cf.trial.applicationstudio.cloud.sap



</td>
</tr>
<tr>
<td>

Europe \(Netherlands\)



</td>
<td>

Azure



</td>
<td>

eu20



</td>
<td>

https://connectivity.eu20.applicationstudio.cloud.sap



</td>
</tr>
<tr>
<td>

US West \(Washington\)



</td>
<td>

Azure



</td>
<td>

us20



</td>
<td>

https://connectivity.us20.applicationstudio.cloud.sap



</td>
</tr>
<tr>
<td>

US East



</td>
<td>

Azure



</td>
<td>

us21



</td>
<td>

https://connectivity.us21.applicationstudio.cloud.sap



</td>
</tr>
<tr>
<td>

Japan \(Tokyo\)



</td>
<td>

Azure



</td>
<td>

jp20



</td>
<td>

https://connectivity.jp20.applicationstudio.cloud.sap



</td>
</tr>
<tr>
<td>

Singapore



</td>
<td>

Azure



</td>
<td>

ap21



</td>
<td>

https://connectivity.ap21.applicationstudio.cloud.sap



</td>
</tr>
<tr>
<td>

Singapore



</td>
<td>

Azure



</td>
<td>

ap21-trial



</td>
<td>

https://connectivity.ap21cf.trial.applicationstudio.cloud.sap



</td>
</tr>
</table>

