# azure-logs-forwarder
Azure logs forwarding to PacketAI

# Installing PacketAI logs forwarders
* Open Azure Cloud Shell (PowerShell)
* Download the file `logs-forwarder.ps1`
    * `(New-Object System.Net.WebClient).DownloadFile("https://raw.githubusercontent.com/PacketAI/azure-logs-forwarder/main/logs-forwarder.ps1", "logs-forwarder.ps1")`
* Run the logs-forwarder.ps1 with the below parameters:
    * `./logs-forwarder.ps1 -SubscriptionId SID -PAI_IID YOUR_PAI_IID -PAI_TOKEN YOUR_PAI_TOKEN -PacketAISite https://vector-ingester-logpatterns.packetai.co - ResourceGroupLocation westeurope`
* This script will install eventhub namespace (packetai-ns-uid), eventhub(packetai-eventhub), function app(packetai-functionapp-uid) and function(packetai) in resource group (packetai-log-forwarder-rg)
