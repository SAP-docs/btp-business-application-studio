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

3.65.235.145

3.68.253.57

18.193.62.167



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

18.157.69.102

3.126.1.137

3.69.188.52



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

18.158.167.239

18.192.41.236

3.68.62.167



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

107.23.185.214

18.235.6.188

34.202.247.115



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

13.237.126.245

54.66.136.70

54.66.49.132



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

18.142.61.29

3.1.255.127

54.179.99.46



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

15.165.92.14

3.37.142.13

52.78.126.220



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

3.96.12.36

3.98.118.119

35.183.248.246



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

54.207.137.216

54.94.190.187

54.94.95.72



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

13.113.231.142

35.76.193.116

35.76.58.2



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

51.105.219.227

20.50.59.1

20.50.59.78



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

40.91.127.201

20.57.129.173

20.57.129.190



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

52.224.72.175

20.62.163.90

20.62.163.97



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

20.44.164.134

20.78.56.84

20.78.56.93



</td>
</tr>
<tr>
<td>

Australia \(Sydney\)



</td>
<td>

Azure



</td>
<td>

ap20



</td>
<td>

20.193.34.40

20.92.248.254

20.92.249.110



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

20.43.174.229

20.198.241.28

20.198.241.53



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

20.195.35.183

20.195.27.211

20.195.28.39



</td>
</tr>
</table>

\*NAT IPs \(egress, IPs for requests from an SAP Business Application Studio dev space\)



<a name="loio8509485251814213876223e332bfdcbb__section_nkt_twz_hqb"/>

## Inbound IP Address

If your corporate network is protected by a corporate proxy or firewall, extend your allowlist to enable connections from the corporate network to your dev spaces in SAP Business Application Studio.

For example, when connecting to a service on your corporate SAP system, which is located within your corporate network, you might need to maintain the SAP Business Application Studio connectivity service host in your firewall.

Use the host listed in the Connectivity Service Host column of the table below, according to your region.

The Cloud Connector should also be connected to this service host.

If your network restriction also requires explicit IPs, use the IPs listed in the Inbound IP column of the table below, according to your region.


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
<td rowspan="3">

> ### Note:  
> SAP Business Application Studio doesn't currently support static inbound IPs for trial environments.

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
<td>

20.76.191.246

20.93.214.159



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
<td>

20.109.144.108

20.109.145.6



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
<td>

20.81.5.143

20.81.5.181



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
<td>

20.89.185.253

20.89.185.115



</td>
</tr>
<tr>
<td>

Australia \(Sydney\)



</td>
<td>

Azure



</td>
<td>

ap20



</td>
<td>

https://connectivity.ap20.applicationstudio.cloud.sap



</td>
<td>

20.193.1.52

20.193.0.203



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
<td>

20.198.213.162

20.198.212.10



</td>
</tr>
</table>

